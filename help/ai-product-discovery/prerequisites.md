---
title: Prerequisiti per l’individuazione dei prodotti AI
description: Rivedi i requisiti per l’arricchimento del catalogo e l’arricchimento PDP e installa l’estensione di arricchimento condiviso su Adobe Commerce sull’infrastruttura cloud o on-premise.
role: Admin, Developer
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# Prerequisiti

Prima di utilizzare l’arricchimento del catalogo o PDP, conferma i requisiti applicabili a ogni distribuzione, quindi completa la configurazione per la piattaforma Commerce.

## Requisiti per tutte le implementazioni {#all-deployments}

| Requisito | Applicabile a | Dettagli |
| --- | --- | --- |
| Ottimizza in Edge | Arricchimento PDP | Obbligatorio. Ottimizza in Edge fornisce i dati di prodotto arricchiti agli agenti di intelligenza artificiale. Consulta la [Guida all&#39;ottimizzazione in Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). |
| Inoltro registro | Entrambi i flussi di lavoro | Facoltativo. Abilita le raccomandazioni di arricchimento in base al traffico agente. In caso contrario, sarà comunque possibile selezionare manualmente prodotti o pagine di prodotti. Consulta la [Guida all&#39;inoltro dei registri](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview). |
| Vetrina indicizzabile | Arricchimento del catalogo | Obbligatorio per i consigli basati sul scansiono. I bot attivi e orientati verso LLM devono essere in grado di accedere alle pagine dei prodotti. |
| Accesso a [!DNL Adobe Admin Console] | Arricchimento del catalogo | Obbligatorio. Durante l&#39;installazione, [!DNL Adobe Commerce] controlla se l&#39;organizzazione ha firmato il driver GenAI o ha rinunciato ai servizi di IA sottostanti. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
TBD (SME): Confirm whether the Admin Console and GenAI rider check also applies to PDP enrichment.
-->

## Configurare la piattaforma Commerce {#set-up}

>[!BEGINTABS]

>[!TAB Commerce sull&#39;infrastruttura cloud o on-premise]

Per [!DNL Adobe Commerce] sull&#39;infrastruttura cloud o on-premise, installare l&#39;estensione di arricchimento condiviso, che consente sia l&#39;arricchimento del catalogo che l&#39;arricchimento PDP.

**Prima di iniziare:**

- [!DNL Adobe Commerce] 2.4.7 o versione successiva su PHP 8.3 o versione successiva. Consulta le [note sulla versione](release-notes.md).
- Organizzazione [!DNL Adobe IMS]. Se la tua organizzazione non ne dispone, consulta la [Panoramica sull&#39;integrazione Adobe IMS](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). L’arricchimento del catalogo utilizza il token di accesso IMS dell’utente amministratore connesso. L&#39;accesso con un solo nome utente e una sola password Commerce non fornisce questo token.
- Accesso alla riga di comando al server applicazioni di Commerce e autorizzazione per il download di pacchetti da `repo.magento.com`.

**Installa e verifica:**

1. Se né [!DNL Live Search] né [!DNL Product Recommendations] sono abilitati, aggiungi [!DNL Catalog Service] dalla directory del progetto Commerce:

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service] è installato automaticamente con [!DNL Live Search] e [!DNL Product Recommendations], quindi ignora questo passaggio se uno dei servizi è abilitato.

1. Se non è già configurato per un altro servizio Commerce, configurare [Connettore servizi Commerce](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) con chiavi API e spazio dati SaaS.

1. Aggiungi l’estensione di arricchimento condivisa:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Distribuisci le modifiche:

   - **Infrastruttura cloud:** Eseguire il commit e il push delle modifiche in `composer.json` e `composer.lock`.
   - **Locale:** Aggiornare l&#39;applicazione e cancellare la cache:

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. In Amministrazione, vai a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]** e conferma che Commerce esporta i dati del catalogo.

   Il numero di record di prodotto inviati correttamente deve corrispondere ai record di origine, senza invii non riusciti o in attesa. Per i record non riusciti, esaminare i dettagli dell&#39;errore, risolvere il problema e pianificare una risincronizzazione per i record interessati.

1. Vai a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]** e verifica che i dati del catalogo previsti siano disponibili in [!DNL Catalog Service].

Per informazioni sullo stato e per la risoluzione dei problemi, vedere [Monitorare lo stato del feed dati](/help/systems/data-feed-sync-status.md#monitor-data-feed-status).

>[!TAB Adobe Commerce as a Cloud Service]

Per [!DNL Adobe Commerce as a Cloud Service], l&#39;installazione di [!DNL Catalog Service], l&#39;arricchimento del catalogo e l&#39;arricchimento PDP vengono gestiti automaticamente durante il provisioning dell&#39;account.

Completa i [requisiti per tutte le distribuzioni](#all-deployments) che si applicano ai flussi di lavoro che intendi utilizzare.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## Passaggio successivo {#next-step}

[Configura le impostazioni di arricchimento](settings.md) per connettere l&#39;istanza di Commerce all&#39;individuazione di prodotti AI.
