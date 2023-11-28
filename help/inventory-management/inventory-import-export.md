---
title: Importare ed esportare le scorte
description: Utilizzare le funzioni di importazione ed esportazione native con [!DNL Inventory Management] opzioni per aggiornare le origini e le quantità in base allo SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Importare ed esportare le scorte

Per i cataloghi con molti prodotti, utilizza le funzioni di importazione ed esportazione native con [!DNL Inventory Management] opzioni per aggiornare le origini e le quantità in base allo SKU. Con queste opzioni è possibile aggiungere nuove origini e aggiornare le quantità di magazzino per tutte le origini o per una determinata origine. Ad esempio, è possibile esportare i prodotti per un&#39;origine in Germania senza influire sulle informazioni sui prodotti per le origini in Francia, Inghilterra o Stati Uniti.

- [!DNL Commerce] assegna automaticamente l&#39;origine predefinita ai prodotti durante l&#39;aggiornamento [!DNL Commerce] o importare nuovi prodotti. Se si importano prodotti a cui è stata assegnata un&#39;origine personalizzata, l&#39;origine predefinita viene comunque aggiunta con una quantità pari a 0. Per aggiornare origini e quantità, utilizzare queste istruzioni di importazione.

- I commercianti con una sola origine utilizzano l’importazione per aggiornare solo le quantità di prodotto. Tutti i prodotti esistenti e aggiunti vengono assegnati all&#39;origine predefinita.

- I commercianti multi-sorgente utilizzano l’importazione per aggiungere più origini e quantità per riga per SKU.

Per importare gli aggiornamenti, esporta innanzitutto un file CSV per una sorgente specifica o per tutte le sorgenti. Modifica il file CSV e aggiungi una riga per SKU per ogni origine e quantità. È necessario il codice sorgente quando si aggiunge un&#39;origine e si aggiungono quantità di scorte. Non è possibile aggiungere o aggiornare scorte utilizzando le funzioni di importazione-esportazione.

## Contenuto file CSV

Il file di esportazione-importazione include le seguenti informazioni in base alla sorgente:

- `source_code` - Il codice delle sorgenti in [!DNL Commerce]. Esiste una riga per ogni sorgente e SKU.
- `sku` - SKU per il prodotto in [!DNL Commerce]. Lo SKU deve corrispondere a un prodotto nel negozio per un aggiornamento corretto [!DNL Inventory Management] dati.
- `status` - 0 per Esaurito. 1 per In Stock. Il valore deve essere 1 per acquistare le scorte da questa origine.
- `quantity` - Quantità totale di scorte disponibili per lo SKU e l&#39;origine.

Utilizza un file CSV per aggiornare rapidamente più prodotti e origini assegnate per aggiornare e correggere eventuali imprecisioni nei record di inventario anziché una alla volta tramite l’interfaccia dell’applicazione. Per un file di base, esportate prima e aggiornate secondo necessità.

![Esempio di file CSV per l’importazione - esportazione di dati di inventario](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Esporta dati prodotto per tutte le origini

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Per **[!UICONTROL Entity Type]**, scegli `Stock Sources`.

   L’esportazione estrae solo i dati per i prodotti con una SKU.

1. Clic **[!UICONTROL Continue]**.

   Il file viene generato e scaricato per essere aperto e modificato.

Dopo aver aggiornato le quantità di magazzino e i dati di prodotto, importa nuovamente il file in [!DNL Commerce].

![Esporta origini scorte per dati e origini prodotto](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Esporta dati prodotto per un&#39;origine specifica

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Per **[!UICONTROL Entity Type]**, scegli `Stock Sources`.

   L’esportazione estrae solo i dati per i prodotti con una SKU.

1. Utilizza il **[!UICONTROL Entity Attributes]** per filtrare i prodotti esportati per un&#39;origine specifica.

   Per `source_code`, immetti il codice dell’origine nel campo del filtro.

1. Clic **[!UICONTROL Continue]**.

   Il file viene generato e scaricato per essere aperto e modificato.

Dopo aver aggiornato le quantità di magazzino e i dati di prodotto, importa nuovamente il file in [!DNL Commerce].

## Importare dati prodotto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Per **[!UICONTROL Entity Type]**, scegli `Stock Sources`.

   L’esportazione estrae solo i dati per i prodotti con una SKU.

1. Seleziona le configurazioni per **[!UICONTROL Import Behavior]**.

1. Selezionare il file .csv da importare.

1. Clic **[!UICONTROL Check Data]** e completare l&#39;importazione.

![Importare dati e origini prodotto](assets/inventory-import-sources.png){width="600" zoomable="yes"}
