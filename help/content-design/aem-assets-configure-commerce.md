---
title: Installare e configurare l’integrazione di Experience Manager Assets
description: Scopri come installare e configurare  [!DNL AEM Assets Integration for Adobe Commerce]
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: da98c253d0d3f773551c7b58b5eedbb1db622ac6
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Installare e configurare l’integrazione di AEM Assets per Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Installa e configura l’integrazione di AEM Assets per Commerce aggiungendo l’estensione all’applicazione Commerce, connettendoti ai servizi Commerce SaaS, ad Adobe I/O il servizio Eventi e infine al servizio Commerce SaaS.

## Requisiti di sistema

**Requisiti software**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Compositore: 2.x

**Requisiti di configurazione**

- Adobe Commerce deve essere configurato per l&#39;utilizzo dell&#39;autenticazione [Adobe IMS](/help/getting-started/adobe-ims-config.md).
- Provisioning e autorizzazioni dell’account
   - [Amministratore progetto cloud Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) - Installa le estensioni richieste e configura il server applicazioni Commerce dall&#39;amministratore o dalla riga di comando
   - [Amministratore Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview): aggiorna la configurazione dell&#39;archivio e gestisci gli account utente di Commerce

## Panoramica sulla configurazione

Abilita l’integrazione completando le seguenti attività:

1. [Installare l&#39;estensione dell&#39;integrazione di AEM Assets (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Configura Commerce Service Connector](#configure-the-commerce-services-connector) per connettere l&#39;istanza Adobe Commerce e i servizi che consentono la trasmissione dei dati tra Adobe Commerce e AEM Assets.
1. [Configurare eventi di Adobe I/O per Commerce](#configure-adobe-io-events-for-commerce)
1. [Ottenere le credenziali di autenticazione per l’accesso API](#get-authentication-credentials-for-api-access)

## Installare l’estensione per l’integrazione di AEM Assets

>[!BEGINSHADEBOX]

**Prerequisito**

- Accedi a [repo.magento.com](https://repo.magento.com/admin/dashboard) per installare l&#39;estensione. Per generare le chiavi e ottenere i diritti necessari, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Per le installazioni cloud, consulta la [Guida di Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Accedere alla riga di comando del server applicazioni Adobe Commerce.

>[!ENDSHADEBOX]

Installare la versione più recente dell&#39;estensione di integrazione di AEM Assets (`aem-assets-integration`) in un Adobe Commerce che esegue Adobe Commerce 2.4.4 o versione successiva. L&#39;integrazione delle risorse AEM viene distribuita come metapacchetto del compositore dall&#39;archivio [repo.magento.com](https://repo.magento.com/admin/dashboard).

>[!BEGINTABS]

>[!TAB Infrastruttura cloud]

Utilizzare questo metodo per installare l&#39;estensione [!DNL AEM Assets Integration] per un&#39;istanza Commerce Cloud.

1. Sulla workstation locale, passa alla directory del progetto per il progetto Adobe Commerce su infrastruttura cloud.

   >[!NOTE]
   >
   >Per informazioni sulla gestione locale degli ambienti di progetto Commerce, vedere [Gestione dei rami con CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) nella _Guida utente di Adobe Commerce on Cloud Infrastructure_.

1. Consulta il ramo dell’ambiente da aggiornare utilizzando Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Aggiungi l’estensione AEM Assets Integration for Commerce.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Aggiornare le dipendenze del pacchetto.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Modifiche al codice di commit e push per i file `composer.json` e `composer.lock`.

1. Aggiungere, eseguire il commit e inviare le modifiche al codice per i file `composer.json` e `composer.lock` all&#39;ambiente cloud.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   Inviando gli aggiornamenti si avvia il [processo di distribuzione cloud di Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) per applicare le modifiche. Controllare lo stato della distribuzione dal [registro distribuzione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB Locale]

Utilizzare questo metodo per installare l&#39;estensione [!DNL AEM Assets Integration] per un&#39;istanza locale.

1. Utilizza Composer per aggiungere al progetto l’estensione AEM Assets Integration for Commerce:

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Aggiorna le dipendenze e installa l’estensione:

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Aggiorna Adobe Commerce:

   ```shell
   bin/magento setup:upgrade
   ```

1. Cancella la cache:

   ```shell
   bin/magento cache:clean
   ```

   >[!TIP]
   >
   >In alcuni casi, in particolare durante la distribuzione in produzione, potrebbe essere opportuno evitare di cancellare il codice compilato perché potrebbe richiedere del tempo. Prima di apportare qualsiasi modifica, assicurati di eseguire il backup del sistema.

>[!ENDTABS]

## Configurare Commerce Services Connector

Il connettore dei servizi di Commerce consente la sincronizzazione dei dati e la comunicazione tra l’istanza di Commerce, il servizio Asset Rule Engine e altri servizi di supporto.

>[!NOTE]
>
>L&#39;installazione di Commerce Services Connector è un processo unico necessario per utilizzare [i servizi SaaS di Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices). Se il connettore è già stato configurato per un altro servizio, è possibile visualizzare la configurazione esistente dall&#39;amministratore di Commerce selezionando **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**.

Per trasmettere i dati tra l’istanza di Adobe Commerce e i servizi che abilitano l’integrazione di AEM Assets, configura il connettore dei servizi Commerce con quanto segue:

- Configura l’istanza Commerce con le chiavi API di produzione e sandbox per l’autenticazione.
- Specifica uno spazio di dati (identificatore SaaS) per l’archiviazione cloud sicura.
- Accedi alla stessa organizzazione IMS che utilizzi per accedere ad AEM Assets e stabilire la connessione tra il set di dati e Adobe Experience Platform.

Per istruzioni dettagliate, vedere [Connettore servizi Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

Quando si configura Commerce Services Connector, il sistema genera gli ID progetto e database SaaS. Sono necessari durante il processo di onboarding del tenant.

![ID progetto SaaS e spazio dati per integrazione AEM Assets](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Configurare eventi di Adobe I/O per Commerce

L’integrazione di AEM Assets utilizza il servizio Adobe I/O Events per inviare dati evento personalizzati tra l’istanza di Commerce e l’Experience Cloud. I dati dell’evento vengono utilizzati per coordinare i flussi di lavoro per l’integrazione AEM Assets.

>[!BEGINSHADEBOX]

**Prerequisito**

- Assicurati che RabbitMQ sia abilitato e in ascolto degli eventi.
   - [Installazione di RabbitMQ per Adobe Commerce locale](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [Configurazione di RabbitMQ per Adobe Commerce nell&#39;infrastruttura cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Per informazioni dettagliate sugli eventi di Adobe I/O per Commerce, consulta la documentazione sugli [eventi di Adobe I/O per Commerce](https://developer.adobe.com/commerce/extensibility/events/) sul sito Adobe Developer.

La configurazione richiede i seguenti passaggi.

1. Abilita il framework Eventi di Commerce configurando gli eventi di Adobe I/O sul server applicazioni e nell’amministratore.
1. Abilita la sincronizzazione dei dati tra Adobe Commerce e AEM Assets utilizzando l’API del servizio Motore di regole di Assets per configurare la connessione.
1. Abilita l’integrazione di AEM Assets in Admin.

### Abilita framework eventi Commerce

Abilita il framework eventi di Commerce utilizzando le istruzioni per l’ambiente in cui viene distribuito il progetto Commerce.

>[!BEGINTABS]

>[!TAB Infrastruttura cloud]

1. Abilitare il servizio Adobe I/O Events dal menu [!DNL Store Settings Configuration].

   1. Dall&#39;amministratore, vai a **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Eventi di Adobe I/O**.

   1. Espandere **[!UICONTROL Commerce events]**.

   1. Imposta **[!UICONTROL Enabled]** su `Yes`.

      ![Configurazione amministratore Commerce eventi Adobi I/O - abilita eventi Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[Abilita cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) in modo che Commerce possa inviare eventi agli endpoint API per gestire le comunicazioni e i flussi di lavoro per l&#39;integrazione.

1. Aggiorna la configurazione del progetto cloud.

   1. Aggiungi il file `app/etc/config.php` all&#39;archivio di lavoro:

   ```shell
   git add app/etc/config.php
   ```

   1. Esegui il comando `composer info magento/ece-tools` per determinare la versione di ece-tools in uso. Se la versione è inferiore a `2002.1.13`, [aggiorna alla versione più recente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package).

   1. Abilita evento nel file `.magento.env.yaml`:

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. Esegui il commit e invia i file aggiornati all’ambiente Cloud.

>[!TAB Locale]

1. Abilitare il servizio Adobe I/O Events dal menu [!DNL Store Settings Configuration].

   1. Dall&#39;amministratore, vai a **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Eventi di Adobe I/O**.

   1. Espandere **[!UICONTROL Commerce events]**.

   1. Imposta **[!UICONTROL Enabled]** su `Yes`.

      ![Configurazione amministratore Commerce eventi Adobi I/O - abilita eventi Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[Abilita i processi cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) in modo che Commerce possa inviare eventi per gestire le comunicazioni e i flussi di lavoro tra risorse AEM e Commerce.

>[!ENDTABS]

## Ottenere le credenziali di autenticazione per l’accesso API

L’integrazione di AEM Assets per Commerce richiede le credenziali di autenticazione OAuth per consentire l’accesso API all’istanza di Commerce. Queste credenziali sono necessarie per registrare il progetto Commerce con il servizio Assets Rule Engine durante l’onboarding del tenant e per inviare richieste API per gestire le risorse tra Adobe Commerce e AEM Assets.

Per generare le credenziali, aggiungi l’integrazione all’istanza di Commerce e attivala.

### Aggiungere l’integrazione all’ambiente Commerce

1. Dall&#39;amministratore, vai a **Sistema** > Estensioni > **Integrazioni**, quindi fai clic su **Aggiungi nuova integrazione**.

1. Immetti informazioni sull’integrazione.

   Nella sezione **General**, specifica solo l&#39;integrazione **Name** e **Email**. Utilizza l’e-mail per un account Adobe IMS con accesso all’organizzazione in cui vengono distribuiti Commerce e Experience Manager Assets.

   ![Integrazione di AEM Assets per la configurazione dell&#39;amministratore di Commerce](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Verificare l&#39;identità facendo clic su **Conferma identità**.

   Il sistema verifica la tua identità autenticandosi per l&#39;Experience Cloud con il tuo ID Adobe.

1. Configurare le risorse API.

   1. Nel pannello sinistro fare clic su **[!UICONTROL API]**.
E
   1. Selezionare la risorsa multimediale esterna **[!UICONTROL Catalog > Inventory > Products > External Media]**.

   ![Configurazione integrazione amministratore per risorse API](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save]**.

### Genera credenziali

Nella pagina Integrazioni, genera le credenziali di autenticazione OAuth facendo clic su **Attiva** per l&#39;integrazione Assets. Queste credenziali sono necessarie per registrare il progetto Commerce con il servizio Motore regole di Assets e per inviare richieste API per gestire le risorse tra Adobe Commerce e AEM Assets.

1. Dalla pagina Integrazioni, generare le credenziali facendo clic su **[!UICONTROL Activate]**.

   ![Attiva la configurazione Commerce per l&#39;integrazione Assets](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Salva le credenziali per la chiave consumer e il token di accesso per un uso successivo.

![Credenziali OAuth per autenticare le richieste API](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Done]**.

>[!NOTE]
>
>Puoi anche generare le credenziali di autenticazione utilizzando le API di Adobe Commerce. Per informazioni dettagliate su questo processo e ulteriori informazioni sull&#39;autenticazione basata su OAuth per Adobe Commerce, vedi [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione di Adobe Developer.
