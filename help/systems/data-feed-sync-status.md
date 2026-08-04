---
title: Monitorare lo stato di sincronizzazione dei feed dati in Commerce
description: Tracciare le esportazioni. Diagnosticare i problemi di sincronizzazione per  [!DNL Catalog Service], [!DNL Live Search], [!DNL Product Recommendations] e [!DNL Adobe Commerce Optimizer Connector].
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# Monitoraggio dello stato di sincronizzazione dei feed di dati

La pagina [!UICONTROL Data Feed Sync Status] consente agli amministratori di Commerce di monitorare l&#39;integrità delle esportazioni per i feed di dati di prodotti e categorie nell&#39;area di amministrazione.

## Pubblico e disponibilità {#audience}

La pagina Stato di sincronizzazione feed dati è disponibile senza costi aggiuntivi per gli esercenti Commerce con una licenza attiva per uno dei seguenti servizi:

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/it/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/it/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/it/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/it/docs/commerce/aco-optimizer-connector/overview)

La pagina Stato di sincronizzazione feed dati è disponibile automaticamente nelle configurazioni dei servizi Commerce supportate. Per le distribuzioni on-premise e con Adobe Commerce su infrastruttura cloud, se la pagina risulta mancante dopo l’abilitazione di un servizio o connettore idoneo, segui le istruzioni di installazione manuali riportate di seguito. Non utilizzare la procedura di installazione del Compositore per le esperienze SaaS gestite dal prodotto.

## Accedere alla pagina dello stato di sincronizzazione {#access-data-feed-sync-status-page}

Dall&#39;area di amministrazione, passare a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**.

![Pagina Stato sincronizzazione feed dati che riepiloga l&#39;attività di esportazione del feed dati](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> Questa pagina riporta solo lo stato di esportazione. Uno stato di operazione riuscita indica che i dati sono stati esportati correttamente e non conferma che i dati siano disponibili nei servizi connessi. Per ulteriori informazioni, vedere [Conferma dati nei servizi connessi](#confirm-data-in-connected-services).

## Feed di esportazione disponibili

L’elenco dei feed di esportazione disponibili che è possibile gestire dalla pagina Stato di sincronizzazione dati dipende dai servizi Commerce connessi.

- **Per [!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service] con servizi Commerce configurati:** Vedere [Feed supportati](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds) nella _Guida all&#39;esportazione dei dati SaaS_.

- **Per le distribuzioni Adobe Commerce on-premise o sul cloud configurate con [!DNL Adobe Commerce Optimizer Connector]:** Consulta [Feed supportati](https://experienceleague.adobe.com/it/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds) nella _Guida al connettore Adobe Commerce Optimizer_.


## Riepilogo stato sincronizzazione feed dati {#data-feed-sync-status-summary}

La griglia di riepilogo elenca ogni feed e i relativi conteggi di esportazione.

| Campo | Descrizione |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nome feed** | Indicizzatore feed per un’entità o parte di un’entità (prodotto, prezzo del prodotto). |
| **Record Source** | Numero di record Commerce che richiedono la sincronizzazione. Può superare il conteggio della griglia di amministrazione perché gli elementi del feed hanno un ambito (ad esempio, codice Visualizzazione archivio). |
| **Record inviati correttamente** | Numero di elementi di feed inviati correttamente da Commerce all’endpoint del servizio configurato. Questo non conferma l’acquisizione a valle o la disponibilità del catalogo. Se si verificano errori di sincronizzazione, questo numero potrebbe essere inferiore al numero di record di origine. |
| **Record non riusciti** | Numero di record che non è stato possibile inviare ai servizi Commerce connessi. |
| **Azione** | Selezionare **[!UICONTROL Details]** per visualizzare l&#39;attività di sincronizzazione per un feed. |

## Dettagli sullo stato di sincronizzazione del feed dati {#data-feed-sync-status-details}

Dalla pagina di riepilogo, selezionare un nome di feed o selezionare **[!UICONTROL Details]** per visualizzare lo stato di esportazione per ogni elemento di feed:

![Pagina dei dettagli sullo stato di sincronizzazione dei feed di dati con report sullo stato degli elementi del feed](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| Campo | Descrizione |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID elemento feed** | Identificatore generato automaticamente utilizzato a scopo di sistema |
| **ID entità** | L’identificatore univoco dell’entità di origine (ID prodotto, ID categoria e così via) |
| **Identificatori feed** | Identificatori univoci per l’elemento del feed. Ad esempio, SKU e codice della vista store per il feed dei prodotti. I valori variano in base al feed. |
| **Stato esportazione** | [stato di sincronizzazione](#export-status-types) dell&#39;elemento di feed, con indicatori codificati a colori |
| **Data ultima sincronizzazione** | Data e ora dell’ultimo tentativo di esportazione o invio da Commerce. Questo timestamp non conferma la disponibilità a valle. |
| **L&#39;entità è stata eliminata?** | Indica se l’entità è stata eliminata in Adobe Commerce. Gli elementi eliminati vengono visualizzati solo se la sincronizzazione non è riuscita. |
| **ID richiesta** | ID univoco della richiesta di sincronizzazione. Forniscilo al Supporto tecnico quando si risolvono i problemi relativi agli aggiornamenti delle entità. |
| **Errore** | Informazioni dettagliate sugli errori di sincronizzazione |

Potete gestire la vista utilizzando i seguenti controlli:

- [!UICONTROL Mass Action] per pianificare la risincronizzazione per gli elementi feed selezionati
- [!UICONTROL Filters] e [!UICONTROL Columns]
- [!UICONTROL Default View] per creare e salvare una visualizzazione filtrata e passare da una visualizzazione all&#39;altra

### Indicatori di salute dei mangimi {#feed-health-indicators}

| **Indicatore** | **Descrizione** |
| ------------- | --------------- |
| Stato indicizzatore | <ul><li>**Pronto**: indicizzatore aggiornato. Non è richiesta alcuna reindicizzazione.</li><li>**Reindicizzazione richiesta**: dati Source modificati. Esegui una reindicizzazione per acquisire le modifiche recenti.</li><li>**Elaborazione**: indicizzazione in corso.</li></ul> |
| Backlog di Changelog | <ul><li>**Tutti sincronizzati**: nessuna modifica in sospeso da elaborare.</li><li>**Elementi nel backlog**: numero di modifiche in sospeso in attesa di elaborazione. Un backlog di più di 1.000 elementi può indicare problemi di prestazioni.</li></ul> |
| Modalità indicizzatore | <ul><li>**Modalità pianificazione** (consigliata): l&#39;indicizzatore viene eseguito secondo la pianificazione, riducendo il rischio di perdita di dati.</li><li>**Aggiornamento al salvataggio** (in tempo reale): viene visualizzato come avviso nella pagina. La modalità in tempo reale non è prevista e aumenta il rischio di perdita di dati sotto carico.</li></ul> |

>[!TIP]
>
> Per ulteriori informazioni sull&#39;elaborazione dell&#39;indice, vedere l&#39;argomento [Gestione indice](index-management.md).

### Esporta tipi di stato {#export-status-types}

| **Stato** | **Descrizione** | **Azione richiesta** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **Inviato al servizio** | L&#39;elemento di feed è stato inviato correttamente da Commerce per l&#39;elaborazione a valle. | Nessuno |
| **Operazione non riuscita, verrà eseguito un nuovo tentativo** | Impossibile inviare, ma il sistema tenterà di inviare di nuovo. | Monitor per la risoluzione |
| **Operazione non riuscita, richiede attenzione** | Non riuscito a causa di un errore di applicazione o dati. | Esaminare e risolvere il problema nella colonna [!UICONTROL Error] |
| **In attesa dell&#39;invio** | Modifiche rilevate nel registro modifiche ma non ancora elaborate. | Stato di elaborazione normale |

## Monitorare lo stato del feed dati

Quando si aggiornano entità relative a prodotti e categorie nel database di Commerce, i dati vengono trasferiti ai servizi di Commerce in base alla configurazione del feed. È possibile monitorare l&#39;attività di esportazione e il relativo stato corrente dalla pagina di riepilogo [!UICONTROL Data Feed Sync Status].

>[!IMPORTANT]
>
> Il tempo necessario per completare la sincronizzazione dei dati varia in base alle dimensioni del catalogo, al volume di dati aggiornati e alle prestazioni del servizio esterno.

Quando il conteggio inviato correttamente corrisponde al conteggio dell’origine per un feed e nessun elemento rimane in attesa di invio o non è riuscito, Commerce ha completato l’esportazione per quel feed. Utilizza il dashboard appropriato per [confermare la disponibilità downstream](#confirm-data-in-connected-services).

>[!NOTE]
>
> Adobe fornisce inoltre strumenti di interfaccia della riga di comando e registri di sistema che gli sviluppatori e gli integratori di sistemi possono utilizzare per gestire e tenere traccia delle operazioni di sincronizzazione. Per informazioni dettagliate, vedere la [Guida all&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/overview).

### Gestione esportazioni non riuscite {#manage-failed-exports}

Per esaminare le esportazioni non riuscite e pianificare una risincronizzazione:

1. Dalla pagina di riepilogo, individua il feed con record non riusciti.
1. Selezionare **[!UICONTROL Details]**.
1. Esaminare i messaggi di errore nella colonna [!UICONTROL Error].
1. Selezionare i record da risincronizzare utilizzando le caselle di controllo.
1. Dal menu [!UICONTROL Mass Action], selezionare **[!UICONTROL Schedule Resync]**, selezionare **[!UICONTROL Submit]** e confermare l&#39;operazione.
1. Monitora le modifiche di stato nella pagina dei dettagli.

Il sistema esegue automaticamente nuovi tentativi per alcuni errori.

#### Quando risincronizzare manualmente {#resync-feed-items}

Risincronizzazione manuale in questi casi:

- Persistenza degli errori di autenticazione o autorizzazione (codici di stato 401 o 403)
- Sono stati risolti i problemi di formato dei dati che causavano errori di payload
- Configurazione di un servizio esterno o endpoint modificati
- Sono state distribuite personalizzazioni che influiscono sull’esportazione dei dati

### Conferma dati in servizi connessi {#confirm-data-in-connected-services}

Per verificare la sincronizzazione end-to-end al termine dell&#39;esportazione, utilizzare uno dei metodi seguenti. Per informazioni sui limiti dello stato di esportazione di questa pagina, vedi la [nota precedente](#export-status-scope).

- **[!DNL Adobe Commerce as a Cloud Service]con i servizi Commerce:** Controlla il [Dashboard di gestione dati](data-dashboard.md) applicabile per confermare la disponibilità a valle.
- **Adobe Commerce su Cloud o On-Premises con Adobe Commerce Optimizer Connector**: controlla prima lo stato di esportazione dell&#39;amministratore di Commerce, quindi controlla la [pagina di sincronizzazione dati](https://experienceleague.adobe.com/it/docs/commerce/optimizer/setup/data-sync) in [!DNL Commerce Optimizer Studio]
- **[!DNL Adobe Commerce Optimizer] (autonomo):** Dati non esportati dal backend Commerce. Utilizzare la [pagina di sincronizzazione dati](https://experienceleague.adobe.com/it/docs/commerce/optimizer/setup/data-sync) in [!DNL Commerce Optimizer Studio] per confermare la disponibilità dei dati.

>[!TIP]
>
> Per ulteriori informazioni sul processo di sincronizzazione dei dati, vedere [Sincronizzare i dati con l&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process) nella *Guida all&#39;esportazione dei dati SaaS*.

## Best practice {#best-practices}

- Rivedi la pagina di riepilogo ogni giorno per i feed con tassi di errore elevati.
- Esaminare i dettagli settimanalmente per i feed critici, come prodotti e prezzi.
- Tieni traccia delle tendenze di successo delle esportazioni mensilmente per identificare i problemi ricorrenti.

## Risolvere i problemi comuni {#troubleshoot-common-issues}

| Problema | Sintomi | Cosa fare |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Elevate percentuali di errori | Molti record mostrano *Non riuscito, richiede attenzione* stato | <ul><li>Verifica lo stato e la configurazione del servizio esterno</li><li>Rivedi i messaggi di errore per i pattern nella colonna [!UICONTROL Error]</li><li>Dopo aver risolto il problema sottostante, vedere [Gestire e risincronizzare le esportazioni non riuscite](#manage-failed-exports)</li><li>Se necessario, contatta il supporto di servizi esterni</li></ul> |
| Prestazioni di esportazione lente | Backlog del changelog elevato o aggiornamenti dello stato lenti | <ul><li>Controlla [indicatori di integrità del feed](#feed-health-indicators) per lo stato dell&#39;indicizzatore e del backlog</li><li>Esegui nuovamente l&#39;indicizzazione se **è richiesta la reindicizzazione**</li><li>Monitorare i tempi di risposta del servizio esterno</li><li>Se possibile, pianifica le esportazioni nelle ore non di punta</li><li>Esaminare le risorse e le prestazioni del sistema</li></ul> |
| Errori di autenticazione | Codici di stato 401 o 403 nella colonna [!UICONTROL Error] | <ul><li>Verifica credenziali API e token</li><li>Verifica le autorizzazioni dell’account del servizio esterno</li><li>Rinnovare i token scaduti o contattare il provider di servizi</li><li>Dopo il ripristino delle credenziali, [risincronizza record interessati](#manage-failed-exports)</li></ul> |
| Pagina Stato di sincronizzazione feed dati mancante | **[!UICONTROL Data Feed Sync Status]** non è elencato in **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** dopo l&#39;attivazione di un servizio connesso | <ul><li>Per Commerce as a Cloud Service, verificare che un servizio idoneo sia abilitato (vedere [Pubblico e disponibilità](#audience))</li><li>Solo per Commerce su cloud o locale, [Installa l&#39;estensione manualmente](#install-the-extension)</li></ul> |

Adobe Commerce su infrastruttura cloud o on-premise: verifica che sia abilitato un servizio idoneo o il connettore Adobe Commerce Optimizer; se la pagina risulta ancora mancante, segui le istruzioni di installazione manuali.
ACCS o Adobe Commerce Optimizer: non installare il modulo manualmente; utilizza l’esperienza di sincronizzazione gestita dal prodotto o contatta il team di supporto del servizio appropriato.

## Installare l’estensione {#install-the-extension}

L&#39;installazione manuale è necessaria per le distribuzioni Adobe Commerce on Cloud o on-premise solo se la pagina [!UICONTROL Data Feed Sync Status] non è presente nell&#39;area di amministrazione dopo l&#39;abilitazione di un servizio idoneo. Consulta [Pubblico e disponibilità](#audience).

### Prerequisiti

- Adobe Commerce 2.4.4+. Per i requisiti dettagliati, vedere [Requisiti di sistema](https://experienceleague.adobe.com/it/docs/commerce-operations/installation-guide/system-requirements).
- [Estensione Adobe Commerce Data Export](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/reference/manage-extension), versione 103.4.15 o successiva
- Chiavi di autenticazione con autorizzazione per scaricare il pacchetto richiesto dall’archivio Adobe Commerce. Per creare le chiavi di autenticazione e ottenere l&#39;accesso al pacchetto necessario, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/it/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Per le installazioni cloud, consulta la [Guida di Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/develop/authentication-keys).
- Accedere alla riga di comando del server applicazioni Adobe Commerce.

### Passaggi per l’installazione

Aggiungi il modulo `magento/module-data-exporter-status` tramite Compositore:

```shell
composer require magento/module-data-exporter-status
```

Per i passaggi dettagliati dell’installazione, consulta le seguenti guide:

- [Installazione dell’estensione per Adobe Commerce su infrastruttura cloud](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [Installare l’estensione su Adobe Commerce on-premise](https://experienceleague.adobe.com/it/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [Dashboard di gestione dati](data-dashboard.md)
> - [Guida all&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/overview)
