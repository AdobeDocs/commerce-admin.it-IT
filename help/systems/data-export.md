---
title: Esporta dati
description: Scopri i filtri e gli attributi di esportazione dei dati e come esportare i dati dal tuo archivio.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Esporta dati

Il modo migliore per acquisire familiarità con la struttura del database consiste nell&#39;esportare i dati e aprirli in un foglio di calcolo. Una volta acquisita familiarità con il processo, è possibile utilizzarlo come metodo efficiente per gestire grandi quantità di informazioni.

I caratteri speciali, ad esempio il segno di uguale, i simboli maggiore e minore di, le virgolette singole e doppie, la barra rovesciata, la barra verticale e i simboli della e commerciale, possono causare problemi durante il trasferimento dei dati. Per garantire la corretta interpretazione di tali caratteri speciali, è possibile contrassegnarli come _sequenza di escape_. Ad esempio, se i dati includono una stringa di testo come `code="str"`, `code="str2"`, racchiudendo il testo tra virgolette doppie si garantisce che le virgolette doppie originali siano considerate parte dei dati: `"code="str""`. Quando il sistema rileva una doppia serie di virgolette doppie, è possibile comprendere che il set esterno di virgolette doppie racchiude i dati effettivi.

L’esportazione dei dati è un’operazione asincrona, eseguita in background in modo da poter continuare a lavorare in Admin senza attendere il completamento dell’operazione. Il sistema visualizza un messaggio al completamento dell&#39;operazione.

## Criteri di esportazione

I filtri di esportazione vengono utilizzati per specificare i dati da inserire nel file di esportazione, in base al valore dell’attributo. Inoltre, puoi specificare quali dati attributo desideri includere o escludere dall’esportazione.

![Criteri di esportazione dati](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Esporta filtri

Puoi utilizzare i filtri per determinare quali SKU sono inclusi nel file di esportazione. Ad esempio, se inserisci un valore nel filtro Paese di produzione, il file CSV esportato include solo i prodotti fabbricati in tale paese.

Il tipo di filtro corrisponde al tipo di dati. Per i campi data, è possibile scegliere la data dall&#39;icona Calendario ![Calendario](../assets/icon-calendar.png). Per ulteriori informazioni, vedere [Tipi di input attributo](../catalog/attributes-input-types.md).

Il formato della data è determinato dalle [impostazioni locali](../getting-started/store-details.md#locale-options).

Per includere solo i record con un valore specifico, ad esempio uno SKU, immettere il valore nel campo Filtro. Alcuni campi, ad esempio Prezzo, Peso e Imposta prodotto come nuovo, hanno un intervallo di valori iniziale/finale.

### Escludi attributi

La casella di controllo nella prima colonna viene utilizzata per escludere gli attributi dal file di esportazione. Se un attributo viene escluso, la colonna associata nei dati di esportazione viene inclusa, ma vuota.

| Escludi | Filtro | Risultato |
|--- |--- |--- |
| ![Casella di controllo deselezionata](../assets/checkbox-clear.png) | No | Il file esportato contiene ogni attributo per tutti i record esistenti. |
| ![Casella di controllo deselezionata](../assets/checkbox-clear.png) | Sì | Il file di esportazione contiene ogni attributo con solo i record consentiti dal filtro. |
| ![Casella di controllo selezionata](../assets/checkbox-selected.png) | No | Il file di esportazione non include la colonna per l’attributo escluso, ma tutti i record esistenti. |
| ![Casella di controllo selezionata](../assets/checkbox-selected.png) | Sì | Il file di esportazione non include la colonna per l’attributo escluso e contiene solo i record consentiti dal filtro. |

{style="table-layout:auto"}

## Esporta dati

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Nella sezione _Esporta impostazioni_, impostare **[!UICONTROL Entity Type]** su una delle opzioni seguenti:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Impostazioni di esportazione dati](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Accettare il valore predefinito **[!UICONTROL Export File Format]** del file CSV.

1. Se si desidera racchiudere i caratteri speciali eventualmente presenti nei dati come _sequenza di escape_, selezionare la casella di controllo **[!UICONTROL Fields Enclosure]**.

1. Se necessario, modifica la visualizzazione degli attributi di entità.

   Per impostazione predefinita, la sezione Attributi entità elenca tutti gli attributi disponibili in ordine alfabetico. È possibile utilizzare i [controlli elenco](../getting-started/admin-grid-controls.md) standard per cercare attributi specifici e ordinare l&#39;elenco. I controlli Ricerca e Ripristina filtro controllano la visualizzazione dell&#39;elenco, ma non hanno alcun effetto sulla selezione degli attributi da includere nel file di esportazione.

   ![Attributi di entità filtrata per l&#39;esportazione dei dati](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Per filtrare i dati esportati in base al valore dell&#39;attributo, eseguire le operazioni seguenti:

   - Per esportare solo record con valori di attributo specifici, immettere il valore richiesto nella colonna **[!UICONTROL Filter]**. Nell&#39;esempio seguente viene esportato solo uno SKU specifico.

   - Per omettere un attributo dall&#39;esportazione, selezionare la casella di controllo **[!UICONTROL Exclude]** all&#39;inizio della riga. Ad esempio, per esportare solo le colonne `sku` e `image`, selezionare la casella di controllo di ogni altro attributo. La colonna viene visualizzata nel file di esportazione, ma senza alcun valore.

1. Scorri verso il basso e fai clic su **[!UICONTROL Continue]** nell&#39;angolo inferiore destro della pagina.

   Al termine dell’operazione, il file viene elaborato tramite una coda di messaggi (assicurati che il processo cron sia in esecuzione). Il file esportato è stato salvato in `var/export/ folder`. Per ulteriori informazioni sulla coda di messaggi, vedere [Gestione delle code di messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=it) nella _Guida alla configurazione_.

   Puoi salvare o aprire il file CSV esportato come foglio di calcolo, quindi modificare i dati e importarli nuovamente nell’archivio.

   >[!NOTE]
   >
   >Per impostazione predefinita, tutti i file esportati si trovano nella cartella `<Magento-root-directory>/var/export`. Se il modulo di archiviazione remota è abilitato, tutti i file esportati si trovano nella cartella `<remote-storage-root-directory>/import_export/export`.

## Risorse per la risoluzione dei problemi

Per assistenza nella risoluzione dei problemi relativi all&#39;esportazione dei dati, vedere i seguenti articoli della Knowledge Base di supporto Commerce:

- [Il file .csv dei prodotti esportati non viene visualizzato](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html?lang=it)
