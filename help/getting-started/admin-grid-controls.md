---
title: Controlli griglia di amministrazione
description: Scopri come utilizzare le pagine di amministrazione che gestiscono i dati per visualizzare una raccolta di record in una griglia.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Controlli griglia di amministrazione

Le pagine di amministrazione che gestiscono i dati visualizzano una raccolta di record in una griglia. I controlli nella parte superiore di ogni colonna possono essere utilizzati per ordinare i dati. L&#39;ordinamento corrente è indicato da una freccia crescente o decrescente nell&#39;intestazione della colonna. È possibile specificare le colonne da visualizzare nella griglia e trascinarle in posizioni diverse. Puoi anche salvare diverse disposizioni di colonna come viste, che possono essere utilizzate in un secondo momento. Nella colonna **[!UICONTROL Action]** sono elencate le operazioni che è possibile applicare a un singolo record. Inoltre, è possibile esportare la data della visualizzazione corrente della maggior parte delle griglie in un file [CSV](../systems/data-csv.md) o XML.

![Pagina Ordini - visualizzazione griglia](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Ordinare l’elenco

1. Fai clic su un’intestazione di colonna qualsiasi.

   La freccia indica che l&#39;ordine corrente è crescente o decrescente.

1. Utilizzare i controlli di impaginazione per visualizzare ulteriori pagine dell&#39;insieme.

   ![Visualizzazione griglia - controlli pagina](./assets/pagination-controls.png){width="300"}

## Impaginare l’elenco

1. Impostare il controllo **[!UICONTROL Pagination]** sul numero di record che si desidera visualizzare per pagina.

1. Fare clic su **[!UICONTROL Next]** e **[!UICONTROL Previous]** per scorrere l&#39;elenco oppure immettere un **[!UICONTROL Page Number]** specifico.

## Filtrare l’elenco

1. Fare clic su **[!UICONTROL Filters]**.

1. Completare tutti i filtri necessari per descrivere il record che si desidera trovare.

1. Fare clic su **[!UICONTROL Apply Filters]**.

   ![Elenco ordini - controlli filtro](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Esporta dati

1. Selezionare i record da esportare.

   >[!NOTE]
   >
   >Impossibile esportare i dati di prodotto dalla griglia. Per ulteriori informazioni, consulta [Esporta](../systems/data-export.md).

1. Nel menu _Esporta_ (![Selettore menu](../assets/icon-export.png)) nell&#39;angolo superiore destro, scegli uno dei seguenti formati di file:

   - `CSV`
   - `Excel XML`

   ![Elenco ordini - opzioni di esportazione](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Fare clic su **[!UICONTROL Export]**.

1. Cerca il file scaricato dei dati esportati nel percorso utilizzato per i download dal browser.

## Layout griglia

La selezione delle colonne e il loro ordine nella griglia possono essere modificati in base alle tue preferenze e salvati come _visualizzazione_. È possibile controllare gli attributi visualizzati nella griglia nella configurazione dei singoli attributi. La visualizzazione di molti attributi nella griglia del prodotto può influire sul tempo di caricamento e sulle prestazioni dell’amministratore.

![Ordina colonne griglia](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Modificare la selezione delle colonne

1. Nell&#39;angolo superiore destro fare clic sul controllo _Colonne_ (![Controllo colonne](../assets/icon-columns.png)).

1. Modifica le selezioni delle colonne:

   - Selezionare la casella di controllo delle colonne che si desidera aggiungere alla griglia.
   - Deselezionare la casella di controllo delle colonne che si desidera rimuovere dalla griglia.
   - Per restituire la visualizzazione griglia predefinita, fare clic su **[!UICONTROL Reset]**.

Assicurati di scorrere verso il basso per visualizzare tutte le colonne disponibili.

### Spostare una colonna

1. Fai clic sull’intestazione della colonna e tieni premuto.

1. Trascinare la colonna nella nuova posizione e rilasciare.

### Salvare una vista griglia

1. Fare clic sul controllo _Visualizza_ (![Visualizza controllo](../assets/icon-view-eye.png)).

1. Fare clic su **[!UICONTROL Save Current View]**.

1. Immettere **[!UICONTROL name]** per la visualizzazione.

1. Per salvare tutte le modifiche, fare clic sulla _freccia_ (![Salva tutte le modifiche](../assets/icon-arrow-save.png)).

   Il nome della vista viene ora visualizzato come vista corrente.

### Modificare la visualizzazione della griglia

1. Fare clic sul controllo _Visualizza_ (![Visualizza icona](../assets/icon-view-eye.png)).

1. Effettuare una delle seguenti operazioni:

   - Per utilizzare una visualizzazione diversa, fare clic sul nome della visualizzazione.
   - Per modificare il nome di una visualizzazione, fare clic sull&#39;icona _Modifica_ (![Modifica icona](../assets/icon-edit-pencil.png)) e aggiornare il nome.
   - Per eliminare una visualizzazione, fare clic sull&#39;icona _Modifica_ (![Icona Modifica](../assets/icon-edit-pencil.png)), quindi fare clic sull&#39;icona _Elimina_ (![Icona Elimina](../assets/icon-delete-trashcan-solid.png)).
