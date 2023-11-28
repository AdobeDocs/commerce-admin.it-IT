---
title: Configurare l’integrazione Experience Cloud per l’amministratore di Commerce
description: Scopri come configurare un progetto Commerce per abilitare l’accesso come amministratore tramite Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 0%

---

# Configurare l’integrazione di Experience Cloud con l’amministratore di Commerce

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Inizia a usare l’integrazione di Experience Cloud con Commerce Admin configurando l’applicazione Commerce per l’utilizzo delle estensioni Commerce Admin Unified Experience and Commerce Events.


## Prerequisiti

- Adobe Commerce deve essere configurato per utilizzare [Autenticazione Adobe IMS](../getting-started/adobe-ims-config.md)
- Provisioning e autorizzazioni degli account: gli amministratori devono disporre di [profilo aziendale Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) con accesso alle seguenti risorse per configurare l’integrazione Experience Cloud:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html): aggiunta e gestione di account utente e sviluppatore Adobi per l&#39;organizzazione
   - [Console Adobe Developer](https://developer.adobe.com/developer-console/docs/guides/getting-started/): accesso per sviluppatori o amministratori di sistema per creare progetti App Builder e generare le credenziali di connessione e la configurazione del progetto per utilizzare il servizio Adobe I/O Events
   - [Progetto di infrastruttura cloud per Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface): installa i moduli richiesti e configura il server applicazioni Commerce utilizzando Adobe Commerce CLI
   - [Amministratore Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html): aggiornamento della configurazione dell’archivio e gestione degli account utente di Commerce

## Panoramica sulla configurazione

Abilita l’integrazione completando le seguenti attività:

1. [Controllare l’ambiente Commerce e la configurazione dell’applicazione](#check-the-commerce-environment-and-application-configuration).

1. [Abilitare l’estensione per l’esperienza unificata dell’amministratore di Commerce](#enable-the-commerce-admin-unified-experience-extension).

1. [Configurare eventi Adobe I/O per Commerce](#set-up-adobe-io-events).

1. [Testare l’integrazione](#test-the-integration).

## Controllare l’ambiente Commerce e la configurazione dell’applicazione

Prima di configurare l’integrazione Experience Cloud, verifica che il progetto e l’applicazione Commerce soddisfino i requisiti.

1. Sulla workstation locale, passa alla directory del progetto per il progetto Commerce.

1. Consulta il ramo dell’ambiente per l’istanza da integrare con Experience Cloud.

1. Verifica che Adobe IMS sia abilitato.

   - Utilizza il [URL di accesso SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) per consentire all’ambiente di connettersi al server applicazioni Commerce.

   - Dalla riga di comando, utilizza Adobe Commerce CLI per verificare lo stato del modulo IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Se il modulo non è abilitato, [abilitarlo utilizzando l’organizzazione e le credenziali per il progetto di integrazione IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module). Se non hai le credenziali, [invia un ticket di supporto Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

1. Verifica che l’utente Admin possa accedere a Commerce Admin utilizzando il proprio Adobe ID.

   - Vai all’URL dell’amministratore di Commerce.

   - Se hai effettuato l’accesso, disconnettiti.

   - Assicurati che l’utente Admin venga reindirizzato per l’accesso utilizzando il proprio Adobe ID.

     ![Accesso ad Adobe Commerce tramite Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Dalla directory del progetto cloud sulla workstation locale, verifica che l’estensione Commerce Admin Unified Experience sia installata.

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
>Queste istruzioni mostrano come un amministratore di progetto Commerce Cloud può abilitare l’estensione utilizzando Adobe Commerce CLI. Gli utenti Commerce Admin possono anche abilitare l’estensione aggiornando il [Impostazioni di configurazione dell’archivio commerciale](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Dalla directory principale dell’ambiente di progetto Cloud sulla workstation locale, utilizza [strumento CLI magento-cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) per accedere al server applicazioni Commerce.

   ```bash
   magento-cloud ssh
   ```

1. Abilita `magento/module-unified-experience` tramite Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Cancella la cache.

   ```bash
   bin/magento cache:clean
   ```

## Configurare eventi Adobe I/O per Commerce

Quando l’integrazione Experience Cloud è abilitata, il servizio Adobe I/O Events invia i dati dell’evento Commerce ad Experience Cloud per gestire l’accesso degli amministratori ai progetti Commerce. La configurazione del servizio richiede l’abilitazione dell’estensione Adobe I/O Events for Commerce (`magento/commerce-eventing`) e la configurazione del servizio Adobe I/O Events in Admin.

### Abilita eventi Commerce

Abilitare l’estensione Commerce Events (`magento/commerce-eventing`) per inviare dati evento personalizzati dall’applicazione Commerce al servizio Adobe I/O Events.

>[!NOTE]
>
>Per Commerce 2.4.6 e versioni successive, l’estensione Commerce Events è installata per impostazione predefinita. Per i progetti Commerce con Commerce 2.4.5, utilizza innanzitutto Compositore per [installare l’estensione](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce), quindi attivalo.

1. Dall’ambiente di sviluppo del progetto Commerce locale, aggiungi la seguente configurazione alla `.magento.env.yaml` file.

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

1. Aggiungi, esegui il commit e distribuisci il file aggiornato `.magento.env.yaml file` nell’ambiente cloud.

>[!TIP]
>
>Per informazioni dettagliate sulla configurazione e la gestione delle variabili di ambiente mediante `.magento.env.yaml` file, vedi [Configurare le variabili di ambiente per la distribuzione](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Configurare l’integrazione di Commerce Events

Configura l’integrazione degli eventi Commerce completando le seguenti attività. Per istruzioni dettagliate, consulta [Adobe I/O di eventi per Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/) documentazione per gli sviluppatori.

1. [Creare un progetto App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) per ricevere i dati dell’evento dall’istanza Commerce.

   Per configurare l’integrazione in Commerce Admin, sono necessari credenziali e dati di configurazione dal progetto App Builder.

1. Configura Adobe Commerce per utilizzare gli eventi Adobe I/O.

   - [Aggiorna le impostazioni di configurazione dell&#39;archivio per il servizio Eventi Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configurare un provider di eventi per l’invio di eventi Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Aggiorna il progetto App Builder per ricevere i dati dell’evento dall’istanza Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Non registrarti o iscriverti a eventi dall’istanza Commerce. La registrazione dell’evento viene inviata al progetto App Builder quando configuri il provider di eventi per l’applicazione Commerce.

   Dopo aver collegato il provider di eventi al progetto App Builder, abbonati al `observer.uex_commerce_instance_update` e salva le modifiche.

1. Per stabilire la connessione, invia un evento al consumatore tramite il provider di eventi.

   - Dalla riga di comando nella directory del progetto cloud locale, [utilizzare SSH per connettersi al server applicazioni Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Invia i dati dell’evento controllando lo stato dell’estensione Admin Unified Experience tramite Adobe Commerce CLI.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Testare l’integrazione

Verifica che un amministratore Commerce possa accedere ad Experience Cloud per visualizzare i progetti Commerce disponibili e accedere ad Admin e Storefront per ciascun progetto.

1. [Accedi all’Experience Cloud](https://experiencecloud.adobe.com/library) utilizzando l’Adobe ID e l’organizzazione associate all’istanza Commerce.

   ![Accedere ai progetti Commerce dalla home page di Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Visualizza i progetti Commerce disponibili selezionando **[!UICONTROL Commerce]**.

   ![Area di lavoro Progetti Commerce, ad Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Apri l’Amministratore per un’istanza selezionando **[!UICONTROL Open]**.

   ![Vista dell’amministratore di Commerce con integrazione Experience Cloud abilitata](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Verifica di poter eseguire le attività di amministrazione come previsto.

   I flussi di lavoro nell’amministratore di Commerce devono seguire la stessa procedura. Se riscontri modifiche o errori del flusso di lavoro dopo aver abilitato l’integrazione Experience Cloud, contatta l’amministratore di sistema Commerce oppure [invia un ticket di supporto Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Dopo aver configurato l’integrazione di Experience Cloud, verifica che gli account amministratore dispongano del provisioning corretto per accedere ai progetti Commerce tramite Experience Cloud. Consulta [Gestire gli utenti amministratori](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
