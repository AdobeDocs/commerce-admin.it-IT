---
title: Installare e configurare l’integrazione di Experience Manager Assets
description: Scopri come installare e configurare  [!DNL AEM Assets Integration for Adobe Commerce]  in un'istanza di Adobe Commerce.
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: a2b9fc6584b9d8a57f24d87a9b5ebcdc2f29cbae
workflow-type: tm+mt
source-wordcount: '1387'
ht-degree: 0%

---

# Installare e configurare l’integrazione di AEM Assets per Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Preparare l&#39;ambiente Commerce per l&#39;utilizzo dell&#39;integrazione AEM Assets per Commerce installando l&#39;estensione PHP `aem-assets-integration`. Quindi, aggiorna la configurazione Amministratore per abilitare la comunicazione e i flussi di lavoro tra Adobe Commerce e AEM Assets.

## Requisiti di sistema

L’integrazione di AEM Assets per Commerce prevede i seguenti requisiti di sistema e configurazione.

**Requisiti software**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Compositore: 2.x

**Requisiti di configurazione**

- Provisioning account e autorizzazioni:

   - [Amministratore progetto cloud Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) - Installa le estensioni richieste e configura il server applicazioni Commerce dall&#39;amministratore o dalla riga di comando

   - [Amministratore Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview): aggiorna la configurazione dell&#39;archivio e gestisci gli account utente di Commerce

>[!TIP]
>
> È possibile configurare Adobe Commerce per l&#39;utilizzo dell&#39;autenticazione [Adobe IMS](/help/getting-started/adobe-ims-config.md).

## Panoramica sulla configurazione

Abilita l’integrazione completando le seguenti attività:

1. [Installare l&#39;estensione dell&#39;integrazione di AEM Assets (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Configura Commerce Services Connector](#configure-the-commerce-services-connector) per connettere l&#39;istanza Adobe Commerce e i servizi che consentono la trasmissione dei dati tra Adobe Commerce e AEM Assets.
1. [Configurare eventi di Adobe I/O per Commerce](#configure-adobe-io-events-for-commerce)
1. [Ottenere le credenziali di autenticazione per l’accesso API](#get-authentication-credentials-for-api-access)

## Installare l’estensione per l’integrazione di AEM Assets

>[!BEGINSHADEBOX]

**Prerequisito**

- Accedi a [repo.magento.com](https://repo.magento.com/admin/dashboard) per installare l&#39;estensione.

  Per generare le chiavi e ottenere i diritti necessari, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Per le installazioni cloud, consulta la [Guida di Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Accedere alla riga di comando del server applicazioni Adobe Commerce.

>[!ENDSHADEBOX]

Installa la versione più recente dell&#39;estensione per l&#39;integrazione di AEM Assets (`aem-assets-integration`) in un&#39;istanza di Adobe Commerce con versione Adobe Commerce 2.4.5+. L&#39;integrazione delle risorse AEM viene distribuita come metapacchetto del compositore dall&#39;archivio [repo.magento.com](https://repo.magento.com/admin/dashboard).

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
>Durante la distribuzione in produzione, è consigliabile non cancellare il codice compilato per risparmiare tempo. Eseguire sempre il backup del sistema prima di apportare modifiche.

>[!ENDTABS]

## Configurare Commerce Services Connector

Il connettore dei servizi di Commerce consente la sincronizzazione dei dati e la comunicazione tra l’istanza di Commerce, il servizio Asset Rule Engine e altri servizi di supporto.

>[!NOTE]
>
>L&#39;installazione di Commerce Services Connector è un processo unico necessario per utilizzare [i servizi SaaS di Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices). Se il connettore è già stato configurato per un altro servizio, è possibile visualizzare la configurazione esistente dall&#39;amministratore di Commerce selezionando **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**.

Per trasmettere i dati tra l’istanza di Adobe Commerce e i servizi che abilitano l’integrazione di AEM Assets, configura il connettore dei servizi Commerce con quanto segue:

- Chiavi API di produzione e sandbox per l’autenticazione.
- Imposta uno spazio dati (identificatore SaaS) per l’archiviazione cloud sicura.
- Specifica l’ID organizzazione IMS in cui viene eseguito il provisioning degli ambienti Commerce e AEM Assets.

Per istruzioni dettagliate, vedere [Connettore servizi Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

Dopo aver configurato Commerce Services Connector, il sistema genera gli ID database e progetto SaaS che identificano l&#39;ambiente di archiviazione cloud sicuro per i servizi Commerce e visualizzano gli ID nella configurazione amministratore. Questi valori sono necessari per completare il processo di onboarding per la sincronizzazione delle risorse.

![ID progetto SaaS e spazio dati per integrazione AEM Assets](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Configurare eventi di Adobe I/O per Commerce

L’integrazione di AEM Assets utilizza il servizio Adobe I/O Events per inviare dati evento personalizzati tra l’istanza di Commerce e l’Experience Cloud. I dati dell’evento vengono utilizzati per coordinare i flussi di lavoro per l’integrazione AEM Assets.

>[!BEGINSHADEBOX]

**Prerequisito**

- Assicurati che RabbitMQ sia abilitato e in ascolto degli eventi.
   - [Installazione di RabbitMQ per Adobe Commerce locale](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [Configurazione di RabbitMQ per Adobe Commerce nell&#39;infrastruttura cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - Verificare che [processi cron siano abilitati](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration). Sono necessari processi Cron per la comunicazione e i flussi di lavoro per l’integrazione AEM Assets.

>[!NOTE]
>
> Per i progetti in Commerce versione 2.4.5, è necessario [installare i moduli Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce). In Commerce versione 2.4.6+, questi moduli vengono caricati automaticamente. Per l’integrazione di AEM Assets per Commerce, è sufficiente installare i moduli. La configurazione di App Builder non è richiesta.

>[!ENDSHADEBOX]

### Abilita framework eventi Commerce

Abilita il framework degli eventi da Commerce Admin.

1. Dall&#39;amministratore, vai a **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Eventi di Adobe I/O**.

1. Espandere **[!UICONTROL Commerce events]**.

1. Imposta **[!UICONTROL Enabled]** su `Yes`.

   ![Configurazione amministratore Commerce eventi Adobi I/O - abilita eventi Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

1. Immettere il nome della società esercente in **[!UICONTROL Merchant ID]** e il nome dell&#39;ambiente nei campi **[!UICONTROL Environment ID]**. Utilizzare solo caratteri alfanumerici e trattini bassi per impostare questi valori.

>[!BEGINSHADEBOX]

**Configura VCL personalizzato per bloccare le richieste**

Se si utilizza un frammento VCL personalizzato per bloccare richieste in ingresso sconosciute, potrebbe essere necessario includere l&#39;intestazione HTTP `X-Ims-Org-Idheader` per consentire le connessioni in ingresso dal servizio AEM Assets Integration for Commerce.

>[!TIP]
>
> Puoi utilizzare il modulo Fastly CDN per creare un ACL di Edge con un elenco di indirizzi IP che desideri bloccare.

Il seguente codice snippet VCL personalizzato (formato JSON) mostra un esempio con un&#39;intestazione di richiesta `X-Ims-Org-Id`.

```json
{
  "name": "blockbyuseragent",
  "dynamic": "0",
  "type": "recv",
  "priority": "5",
  "content": "if ( req.http.X-ims-org ~ \"<YOUR-IMS-ORG>\" ) {error 405 \"Not allowed\";}"
}
```

Prima di creare uno snippet basato su questo esempio, esaminare i valori per determinare se è necessario apportare modifiche:

- `name`: nome dello snippet VCL. In questo esempio è stato utilizzato il nome `blockbyuseragent`.

- `dynamic`: imposta la versione dello snippet. In questo esempio è stato utilizzato `0`. Per informazioni dettagliate sul modello dati, vedere [Frammenti VCL](https://www.fastly.com/documentation/reference/api/vcl-services/snippet/).

- `type`: specifica il tipo di snippet VCL, che determina la posizione del snippet nel codice VCL generato. In questo esempio, abbiamo utilizzato `recv`, consulta il [riferimento frammento VCL ](https://docs.fastly.com/api/config#api-section-snippet) per l&#39;elenco dei tipi di frammento.

- `priority`: determina quando viene eseguito lo snippet VCL. In questo esempio viene utilizzata la priorità `5` per eseguire immediatamente e verificare se una richiesta dell&#39;amministratore proviene da un indirizzo IP consentito.

- `content`: snippet di codice VCL da eseguire, che controlla l&#39;indirizzo IP del client. Se l&#39;IP si trova nell&#39;ACL di Edge, l&#39;accesso viene bloccato con un errore `405 Not allowed` per l&#39;intero sito Web. A tutti gli altri indirizzi IP client è consentito l&#39;accesso.

Per informazioni dettagliate sull&#39;utilizzo dei snippet VCL per bloccare le richieste in ingresso, vedere [VCL personalizzato per bloccare le richieste](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-blocking) nella _Guida di Commerce sull&#39;infrastruttura cloud_.

>[!ENDSHADEBOX]

## Ottenere le credenziali di autenticazione per l’accesso API

L’integrazione di AEM Assets per Commerce richiede le credenziali di autenticazione OAuth per consentire l’accesso API all’istanza di Commerce. Queste credenziali sono necessarie per autenticare le richieste API durante la gestione delle risorse tramite l’integrazione AEM Assets.

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

   1. Selezionare la risorsa multimediale esterna **[!UICONTROL Catalog > Inventory > Products > External Media]**.

      ![Configurazione integrazione amministratore per risorse API](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save]**.

### Genera credenziali

Nella pagina Integrazioni, genera le credenziali di autenticazione OAuth facendo clic su **Attiva** per l&#39;integrazione Assets. Queste credenziali sono necessarie per registrare il progetto Commerce con il servizio Motore regole di Assets e per inviare richieste API per gestire le risorse tra Adobe Commerce e AEM Assets.

1. Dalla pagina Integrazioni, generare le credenziali facendo clic su **[!UICONTROL Activate]**.

   ![Attiva la configurazione Commerce per l&#39;integrazione Assets](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Se prevedi di utilizzare l’API, salva le credenziali per la chiave consumer e il token di accesso per configurare l’autenticazione nel client API.

   ![Credenziali OAuth per autenticare le richieste API](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Done]**.

>[!NOTE]
>
>Puoi anche generare le credenziali di autenticazione utilizzando le API di Adobe Commerce. Per informazioni dettagliate su questo processo e ulteriori informazioni sull&#39;autenticazione basata su OAuth per Adobe Commerce, vedi [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione di Adobe Developer.
