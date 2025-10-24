---
title: Monitoraggio dello stato di sincronizzazione dei feed di dati
description: Monitora la sincronizzazione dell'esportazione dei dati e identifica eventuali problemi o ritardi nell'elaborazione dei feed per  [!DNL Catalog Service], [!DNL Live Search] e [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 4cc5f5842e772ead9785b8280557a7b5b8f26419
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 0%

---


# Monitoraggio dello stato di sincronizzazione dei feed di dati

Gli amministratori di Adobe Commerce possono monitorare lo stato di sincronizzazione dei dati esportati da Adobe Commerce ai servizi Commerce connessi utilizzando la pagina Stato sincronizzazione feed dati in Amministratore Commerce.

![Pagina dei dettagli sullo stato di sincronizzazione dei feed di dati con il reporting sullo stato degli elementi del feed](assets/data-feed-sync-status.png)

Questa pagina fornisce informazioni in tempo reale sullo stato e sulle prestazioni dei feed di esportazione dei dati che trasferiscono i dati di prodotti e categorie da Commerce a servizi esterni quali [!DNL Product Recommendations], [!DNL Live Search] e [!DNL Catalog Service].

La pagina Stato di sincronizzazione mostra solo lo stato di esportazione. Uno stato di operazione riuscita indica che i dati sono stati esportati correttamente e saranno infine disponibili nei servizi Commerce connessi. Utilizza il [dashboard di gestione dati](data-dashboard.md) per visualizzare lo stato effettivo della sincronizzazione delle entità.

Il monitoraggio dello stato dei feed consente di garantire la coerenza dei dati e di risolvere rapidamente eventuali problemi che si verificano durante il processo di esportazione. Gli amministratori possono:

* **Visualizza lo stato di sincronizzazione** per tutti i feed di dati
* **Identificare e risolvere gli errori** nell&#39;elaborazione dei feed
* **Accedi a informazioni dettagliate sullo stato** per singoli elementi del feed

Lo stato viene tracciato per i seguenti feed:

* Feed prodotti
* Feed attributi prodotto
* Feed categorie
* Feed sostituzioni prodotto
* Feed prezzi prodotto
* Feed varianti prodotto

>[!TIP]
>
>Per ulteriori informazioni sul processo di sincronizzazione dei dati, vedere [Sincronizzare i dati con l&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/data-synchronization)nella *Guida all&#39;esportazione dei dati SaaS*.

## Installare l’estensione

La pagina Stato feed dati è disponibile per tutti i commercianti Commerce con licenze attive per i seguenti servizi Commerce:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/it/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/it/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/it/docs/commerce/catalog-service/guide-overview) con una licenza attiva.

**Requisiti**

* PHP 8.1, 8.2, 8.3 o 8.4
* Adobe Commerce 2.4.4+
* [Estensione Adobe Commerce Data Export](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/manage-extension), versione 103.4.15 o successiva
* Accedi a [repo.magento.com](https://repo.magento.com)

  Per generare le chiavi e ottenere i diritti necessari, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/it/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Per le installazioni cloud, consulta la [Guida di Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Accedere alla riga di comando del server applicazioni Adobe Commerce.

### Passaggi per l’installazione

Aggiungi il modulo `magento/module-data-exporter-status` tramite Compositore:

```shell
composer require magento/module-data-exporter-status
```

Per i passaggi dettagliati dell’installazione, consulta le seguenti guide:

* [Installa estensione su Adobe Commerce su infrastruttura cloud](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Installa l&#39;estensione Adobe Commerce on-premise](https://experienceleague.adobe.com/it/docs/commerce-operations/installation-guide/tutorials/extensions)

## Accedere alla pagina Stato feed dati

Dall&#39;amministratore di Commerce, accedere alla pagina Stato feed dati dall&#39;amministratore di Commerce in **[!DNL System]** > Trasferimento dati > **[!DNL Data Feed Sync Status]**.

![Pagina Stato sincronizzazione feed dati che riepiloga l&#39;attività di esportazione del feed dati](assets/data-feed-sync-status.png)

Il monitoraggio dello stato dei feed dati fornisce due interfacce:

* [Pagina di riepilogo dello stato di sincronizzazione dei feed dati](#data-feed-sync-status-summary) in cui sono elencati i feed disponibili e lo stato corrente
* [Stato sincronizzazione feed dati - Pagina dettagli](#data-feed-sync-status-details) che mostra informazioni dettagliate su un feed selezionato.

## Riepilogo stato sincronizzazione feed dati

La pagina di riepilogo dello stato di sincronizzazione dei feed fornisce informazioni sull’attività di esportazione dei feed di dati, tra cui le seguenti:

| Campo | Descrizione |
|-------|-------------|
| **Nome feed** | Il nome dell’indicizzatore del feed responsabile della sincronizzazione di un’entità specifica o di una sua parte, ad esempio il prezzo del prodotto o del prodotto. |
| **Record Source** | Numero di record disponibili per l&#39;esportazione dal database di Commerce. Questo numero può essere maggiore del numero di record visualizzati nell’amministratore di Commerce, in quanto ogni elemento di feed appartiene a un ambito specifico, ad esempio il codice della visualizzazione archivio. |
| **Record inviati correttamente** | Numero di record trasmessi correttamente a SaaS Commerce per ulteriore elaborazione. Se si sono verificati errori durante la trasmissione, il numero di record trasmessi correttamente ai servizi esterni. |
| **Record non riusciti** | Numero di record che non è stato possibile esportare e che richiedono attenzione. |
| **Azione** | Selezionare **[!UICONTROL Details]** per visualizzare l&#39;attività di sincronizzazione per un feed. |

## Dettagli sullo stato di sincronizzazione del feed dati

Dalla pagina di riepilogo dello stato dei feed dati, fare clic su un nome di feed o utilizzare l&#39;azione [!DNL View Details] per accedere a informazioni dettagliate sui singoli record all&#39;interno di un feed.

![[!UICONTROL Data Feed Sync Status - Details] pagina con report sullo stato degli elementi di feed](assets/data-feed-sync-status-details.png)

La vista Dettaglio fornisce le seguenti informazioni per ciascun elemento del feed:

| Campo | Descrizione |
|-------|-------------|
| **ID elemento feed** | Identificatore interno del record del feed |
| **ID entità** | L’ID dell’entità sorgente (ID prodotto, ID categoria e così via) |
| **Stato esportazione** | [stato di sincronizzazione](#export-status-types) dell&#39;elemento del feed. Stato corrente del tentativo di esportazione con indicatori codificati a colori |
| **Data ultima sincronizzazione** | Timestamp dell&#39;ultimo invio del record a Commerce Services |
| **L&#39;entità è stata eliminata?** | Indica se l’entità o la sua parte (ad esempio, prezzo del prodotto o del prodotto) è stata eliminata in Adobe Commerce. Gli elementi vengono visualizzati solo se si è verificato un errore durante la sincronizzazione. |
| **ID richiesta** | Identificatore univoco della richiesta di sincronizzazione. Fornisci questo ID per il supporto durante la risoluzione dei problemi relativi agli aggiornamenti di entità specifiche. |
| **Errore** | Informazioni dettagliate sull’errore in caso di mancata sincronizzazione dell’elemento del feed. |

Potete gestire la vista utilizzando i seguenti controlli:

* [!DNL Mass Action] per pianificare la risincronizzazione per gli elementi feed selezionati
* [!DNL Filters]
* [!DNL Default View] per creare e salvare una visualizzazione filtrata e passare da una visualizzazione all&#39;altra
* [!DNL Columns] per mostrare e nascondere le colonne nella tabella.

### Indicatori di salute dei mangimi

Nella parte superiore di ogni pagina dei dettagli dei feed, gli indicatori di integrità critici forniscono lo stato del sistema per ciascun feed:

#### Stato indicizzatore

* **Valido**: dati sincronizzati. Non è richiesta alcuna reindicizzazione.
* **Non valido**: i dati originali sono stati modificati. L&#39;indice deve essere aggiornato.
* **Elaborazione**: indicizzazione in corso.

>[!TIP]
>
>Per ulteriori informazioni sull&#39;elaborazione dell&#39;indice, vedere l&#39;argomento [Gestione indice](https://experienceleague.adobe.com/it/docs/commerce-admin/systems/tools/index-management).

#### Backlog di Changelog

* **Tutti sincronizzati**: nessuna modifica in sospeso da elaborare
* **Elementi nel backlog**: numero di modifiche in sospeso in attesa di elaborazione

### Esporta tipi di stato

Il sistema fornisce indicatori di stato che consentono di identificare rapidamente i problemi:

#### Categorie di stato

| **Stato** | **Descrizione** | **Azione richiesta** |
|--------|-----------|-------------|
| **Inviato al servizio** | Elemento feed esportato correttamente nel servizio Commerce. | Nessuno |
| **Operazione non riuscita, verrà eseguito un nuovo tentativo** | Errore temporaneo. Il sistema riproverà automaticamente. | Monitor per la risoluzione |
| **Operazione non riuscita, richiede attenzione** | Non riuscito a causa di un errore di applicazione o dati. | Esaminare e risolvere il problema nella colonna [!DNL Error] |
| **In attesa dell&#39;invio** | Accodato per l’esportazione ma non ancora elaborato. | Stato di elaborazione normale |

## Monitorare lo stato del feed dati

Quando si aggiornano entità relative a prodotti e categorie nel database di Commerce, i dati vengono trasferiti ai servizi di Commerce in base alla configurazione del feed. Puoi monitorare questo processo in tempo reale dalla pagina di riepilogo dello stato di sincronizzazione dei feed di dati.

>[!IMPORTANT]
>
>Il tempo necessario per completare la sincronizzazione dei dati varia in base alle dimensioni del catalogo, al volume di dati aggiornati e alle prestazioni del servizio esterno.

Quando il numero di record inviati correttamente corrisponde al numero di record di origine, indica che la sincronizzazione è stata completata e che tutti i dati sono stati trasmessi correttamente.

>[!NOTE]
>
>Adobe fornisce inoltre strumenti di interfaccia della riga di comando e registri di sistema che gli sviluppatori e gli integratori di sistemi possono utilizzare per gestire e tenere traccia delle operazioni di sincronizzazione. Per informazioni dettagliate, vedere la [Guida all&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce-merchant-services/saas-data-export/overview).

### Gestione delle esportazioni non riuscite

Per visualizzare i dettagli delle esportazioni non riuscite e intraprendere azioni correttive:

1. Nella pagina Stato sincronizzazione feed, individua il feed con record non riusciti.
1. Fare clic su **[!DNL Details]**.

1. Esaminare i messaggi di errore per motivi specifici.

1. Utilizzare le azioni di massa per pianificare le operazioni di risincronizzazione per gli elementi non riusciti.

### Risincronizzazione dei dati non riuscita

È possibile risincronizzare manualmente i feed di dati con errori o problemi utilizzando il menu [!DNL Actions] nella pagina [!DNL Data Feed Sync Status - Details].

Mentre il sistema esegue automaticamente nuovi tipi di guasti, può essere necessario un intervento manuale nei seguenti scenari:

* Si verificano errori di autenticazione o autorizzazione (codici di stato 401, 403).
* Dopo aver risolto i problemi di formato dei dati che causavano errori di payload.
* I seguenti aggiornamenti alle configurazioni di servizio o agli endpoint esterni.
* Stai distribuendo personalizzazioni che influiscono sui processi di esportazione dei dati.

Monitorando in modo proattivo lo stato dei feed e risolvendo tempestivamente gli errori, puoi mantenere la coerenza e l’affidabilità dei dati nell’ecosistema Commerce.

#### Risincronizza manualmente elementi feed

Se è necessario risincronizzare elementi di feed specifici:

1. **Seleziona record**: utilizzare le caselle di controllo per selezionare i record non riusciti che richiedono attenzione.
2. **Scegli azione**: seleziona **[!DNL Schedule Resync]** dal menu a discesa Azione di massa.
3. **Conferma**: fare clic su **[!DNL Submit]** e confermare l&#39;operazione di risincronizzazione.
4. **Monitora risultati**: controlla il messaggio di operazione riuscita e monitora le modifiche di stato.

## Best practice

### Monitoraggio regolare

1. **Controlli giornalieri**: controlla la pagina della panoramica ogni giorno per eventuali feed che mostrano tassi di errore elevati
1. **Approfondimento settimanale**: esamina lo stato dettagliato dei feed critici (prodotti, prezzi)
1. **Analisi mensile**: tieni traccia delle tendenze nelle percentuali di successo e nelle prestazioni delle esportazioni

### Risoluzione dei problemi del flusso di lavoro

1. **Identifica problemi**: cerca errori e conteggi di errori elevati
1. **Verifica stato indicizzatore**: verificare che gli indicizzatori siano validi e che il backlog sia gestibile
1. **Rivedi dettagli errore**: fai clic sui record con errori per visualizzare messaggi di errore specifici
1. **Pianifica risincronizzazione**: utilizza azioni di massa per ritentare le esportazioni non riuscite
1. **Risoluzione monitor**: verificare che gli elementi risincronizzati mostrino uno stato corretto

### Correggi i problemi comuni

#### Elevate percentuali di errori

**Sintomi**: un numero elevato di record indica lo stato &quot;Non riuscito, richiede attenzione&quot;

**Possibili cause**:

* Modifiche alla configurazione del servizio esterno
* Incompatibilità del formato dei dati
* Problemi di autenticazione o autorizzazione

**Passaggi di risoluzione**:

1. Verifica lo stato e la configurazione del servizio esterno
1. Revisione dei messaggi di errore per i modelli
1. Verifica credenziali di autenticazione
1. Se necessario, contatta il supporto di servizi esterni

#### Prestazioni di esportazione lente

**Sintomi**: backlog del registro modifiche elevato, aggiornamenti dello stato lenti

**Possibili cause**:

* Problemi di prestazioni dell’indicizzatore
* Volume di dati elevato
* Limitazione della frequenza dei servizi esterni

**Passaggi risoluzione**:

1. Controlla lo stato dell’indicizzatore ed esegui di nuovo se non valido
2. Monitorare i tempi di risposta del servizio esterno
3. Pianificazione delle esportazioni durante le ore di minore utilizzo
4. Esaminare le risorse e le prestazioni del sistema

#### Errori di autenticazione

**Sintomi**: codici di stato 401 o 403

**Passaggi risoluzione**:

1. Verifica credenziali API e token
1. Verifica le autorizzazioni dell’account del servizio esterno
1. Rinnovare token di autenticazione scaduti
1. Contattare il provider di servizi per problemi di accesso

>[!MORELIKETHIS]
>
>* [Dashboard di gestione dati](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [Guida all&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce-merchant-services/saas-data-export/overview)
