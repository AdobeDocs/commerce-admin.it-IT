---
title: Configurare l’integrazione di Experience Cloud per l’amministratore di Commerce
description: Scopri come configurare un progetto Commerce per abilitare l’accesso come amministratore tramite Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# Configurare l’integrazione di Experience Cloud con l’amministratore di Commerce

Inizia a usare l’integrazione di Experience Cloud con Commerce Admin configurando l’applicazione Commerce per l’utilizzo delle estensioni Commerce Admin Unified Experience e Commerce Events.


## Prerequisiti

- Adobe Commerce deve essere configurato per l&#39;utilizzo di [autenticazione Adobe IMS](../getting-started/adobe-ims-config.md)
- Provisioning account e autorizzazioni: gli amministratori devono disporre di un [profilo aziendale di Adobe](https://helpx.adobe.com/it/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) con accesso alle risorse seguenti per configurare l&#39;integrazione di Experience Cloud:
   - [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/admin-guide.html)—Aggiungi e gestisci gli account utente e sviluppatore di Adobe per l&#39;organizzazione
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/): accesso per sviluppatori o amministratori di sistema per creare progetti App Builder e generare le credenziali di connessione e la configurazione del progetto per utilizzare il servizio Adobe I/O Events
   - [Progetto Commerce su infrastruttura cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html?lang=it#get-started-with-the-project-web-interface): installazione dei moduli richiesti e configurazione del server applicazioni Commerce tramite Adobe Commerce CLI
   - [Amministratore Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html?lang=it): aggiorna la configurazione dell&#39;archivio e gestisci gli account utente di Commerce

## Panoramica sulla configurazione

Abilita l’integrazione completando le seguenti attività:

1. [Controllare l&#39;ambiente Commerce e la configurazione dell&#39;applicazione](#check-the-commerce-environment-and-application-configuration).

1. [Abilita l&#39;estensione Commerce Admin Unified Experience](#enable-the-commerce-admin-unified-experience-extension).

1. [Configura Adobe I/O Events per Commerce](#set-up-adobe-io-events).

1. [Verifica l&#39;integrazione](#test-the-integration).

## Controllare l&#39;ambiente Commerce e la configurazione dell&#39;applicazione

Prima di configurare l’integrazione di Experience Cloud, verifica che il progetto e l’applicazione Commerce soddisfino i requisiti.

1. Sulla workstation locale, passa alla directory del progetto per il progetto Commerce.

1. Consulta il ramo dell’ambiente per l’istanza da integrare con Experience Cloud.

1. Verifica che Adobe IMS sia abilitato.

   - Utilizzare l&#39;[URL di accesso SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=it) per l&#39;ambiente per connettersi al server applicazioni Commerce.

   - Dalla riga di comando, utilizza Adobe Commerce CLI per verificare lo stato del modulo IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Se il modulo non è abilitato, [attivalo utilizzando l&#39;organizzazione e le credenziali per il progetto di integrazione IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Verifica che l’utente Admin possa accedere a Commerce Admin utilizzando il proprio Adobe ID.

   - Passa all’URL dell’amministratore di Commerce.

   - Se hai effettuato l’accesso, disconnettiti.

   - Assicurati che l’utente Admin venga reindirizzato per l’accesso utilizzando il proprio Adobe ID.

     ![Accesso ad Adobe Commerce tramite Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Dalla directory del progetto cloud sulla workstation locale, verifica che sia installata l’estensione Commerce Admin Unified Experience.

   ```bash
   composer show *unified-experience*
   ```

   Se l&#39;estensione è installata, Composer restituisce il nome e la descrizione dell&#39;estensione.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Se l&#39;estensione non è installata, utilizza Composer per installarla. Quindi, esegui il commit delle modifiche e ridistribuisci l’ambiente cloud.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Abilita esperienza unificata amministrazione Commerce

Abilita l’estensione Commerce Admin Unified Experience, quindi accedi tramite Experience Cloud.

>[!NOTE]
>
>Queste istruzioni mostrano come un amministratore di progetto Commerce Cloud può abilitare l’estensione utilizzando Adobe Commerce CLI. Gli utenti di Commerce Admin possono inoltre abilitare l&#39;estensione aggiornando le [impostazioni di configurazione dell&#39;archivio Commerce](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Dalla directory principale dell&#39;ambiente di progetto Cloud sulla workstation locale, utilizza lo strumento CLI [magento-cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html?lang=it) per accedere al server applicazioni Commerce.

   ```bash
   magento-cloud ssh
   ```

1. Abilitare l&#39;estensione `magento/module-unified-experience` utilizzando Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Cancella la cache.

   ```bash
   bin/magento cache:clean
   ```

## Configurare Adobe I/O Events per Commerce

Quando l’integrazione Experience Cloud è abilitata, il servizio Adobe I/O Events invia i dati dell’evento Commerce ad Experience Cloud per gestire l’accesso degli amministratori ai progetti Commerce. La configurazione del servizio richiede l&#39;abilitazione dell&#39;estensione Adobe I/O Events for Commerce (`magento/commerce-eventing`) e la configurazione del servizio Adobe I/O Events in Admin.

### Abilita eventi Commerce

Abilitare l&#39;estensione Commerce Events (`magento/commerce-eventing`) per inviare dati evento personalizzati dall&#39;applicazione Commerce al servizio Adobe I/O Events.

>[!NOTE]
>
>Per Commerce 2.4.6 e versioni successive, l’estensione Commerce Events viene installata per impostazione predefinita. Per i progetti Commerce con Commerce 2.4.5, utilizzare innanzitutto Composer per [installare l&#39;estensione](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce), quindi abilitarla.

1. Nell&#39;ambiente di sviluppo del progetto Commerce locale, aggiungere la seguente configurazione al file `.magento.env.yaml`.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. Aggiungere, eseguire il commit e distribuire `.magento.env.yaml file` aggiornato nell&#39;ambiente cloud.

>[!TIP]
>
>Per informazioni dettagliate sulla configurazione e la gestione delle variabili di ambiente tramite il file `.magento.env.yaml`, vedere [Configurare le variabili di ambiente per la distribuzione](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html?lang=it).

### Configurare l’integrazione di Commerce Events

Configura l’integrazione degli eventi di Commerce completando le seguenti attività. Per istruzioni dettagliate, consulta la documentazione per gli sviluppatori di [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/).

1. [Crea un progetto App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) per ricevere i dati dell&#39;evento dall&#39;istanza Commerce.

   Per configurare l’integrazione in Commerce Admin, sono necessari le credenziali e i dati di configurazione del progetto App Builder.

1. Configura Adobe Commerce per utilizzare Adobe I/O Events.

   - [Aggiorna le impostazioni di configurazione dell&#39;archivio per il servizio Adobe I/O Events](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configurare un provider di eventi per inviare eventi Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Aggiorna il progetto App Builder per ricevere i dati evento dall&#39;istanza Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Non registrarti o iscriverti a eventi dall’istanza di Commerce. La registrazione dell’evento viene inviata al progetto App Builder quando configuri il provider di eventi per l’applicazione Commerce.

   Dopo aver collegato il provider di eventi al progetto App Builder, abbonati all&#39;evento `observer.uex_commerce_instance_update` e salva le modifiche.

1. Per stabilire la connessione, invia un evento al consumatore tramite il provider di eventi.

   - Dalla riga di comando nella directory del progetto cloud locale, [utilizzare SSH per connettersi al server applicazioni Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=it#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Invia i dati dell’evento controllando lo stato dell’estensione Admin Unified Experience tramite Adobe Commerce CLI.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Testare l’integrazione

Verifica che un amministratore di Commerce possa accedere ad Experience Cloud per visualizzare i progetti Commerce disponibili e accedere all’amministratore e allo storefront per ciascun progetto.

1. [Accedi ad Experience Cloud](https://experiencecloud.adobe.com/library) utilizzando l&#39;Adobe ID e l&#39;organizzazione associate all&#39;istanza di Commerce.

   ![Accedere ai progetti Commerce dalla home page di Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Visualizza progetti Commerce disponibili selezionando **[!UICONTROL Commerce]**.

   ![Area di lavoro Progetti Commerce per Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Aprire l&#39;amministratore per un&#39;istanza selezionando **[!UICONTROL Open]**.

   ![Visualizzazione amministratore Commerce con integrazione Experience Cloud abilitata](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Verifica di poter eseguire le attività di amministrazione come previsto.

   I flussi di lavoro nell’amministratore di Commerce devono seguire la stessa procedura. Se riscontri modifiche o errori del flusso di lavoro dopo aver abilitato l&#39;integrazione di Experience Cloud, contatta l&#39;amministratore di sistema Commerce o [invia un ticket di supporto Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=it#submit-ticket).

Dopo aver configurato l’integrazione di Experience Cloud, verifica che gli account amministratore dispongano del provisioning corretto per accedere ai progetti Commerce tramite Experience Cloud. Consulta [Gestione utenti amministratori](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
