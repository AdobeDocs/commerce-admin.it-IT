---
title: Ordinare i prodotti di categoria
description: Scopri come definire manualmente il posizionamento dei prodotti in una categoria o applicando un criterio di ordinamento predefinito.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Ordinare i prodotti di categoria

{{ee-feature}}

La posizione dei prodotti in una categoria può essere specificata manualmente trascinando i prodotti nella posizione desiderata o applicando un ordinamento predefinito. Per impostazione predefinita, i prodotti possono essere ordinati per livello di stock, età, colore, nome, SKU e prezzo. L&#39;ordinamento automatico sostituisce l&#39;ordinamento corrente e reimposta le posizioni di trascinamento impostate manualmente. L&#39;ordinamento dei colori e il livello minimo di scorte che possono essere richiesti per i prodotti da includere nell&#39;elenco sono impostati nel [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) configurazione.

>[!NOTE]
>
>Nelle pagine delle categorie, `Out of stock` i prodotti sono sempre visualizzati **_dopo_** `In Stock` prodotti nell’elenco dei prodotti con tutti i tipi di ordinamento.

È possibile impostare le opzioni delle categorie separatamente per ciascuna categoria [visualizzazione store](../stores-purchase/stores.md#add-stores) per determinare la selezione dei prodotti, la loro posizione relativa nell’elenco e gli attributi disponibili per le regole di categoria. Tuttavia, esiste un unico **_globale_** l&#39;ordinamento e la posizione del prodotto nel catalogo e sono condivisi tra tutti [visualizzazioni store](../stores-purchase/store-views.md), store e siti Web.

## Passaggio 1: impostare l’ambito della configurazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Se necessario, scegliere il **[!UICONTROL Store View]** dove si applicano le impostazioni.

   Per un&#39;installazione in più store, _[!UICONTROL Store View]_Questa impostazione applica l&#39;ordinamento a tutte le visualizzazioni disponibili nello store.

1. Nell&#39;albero delle categorie a sinistra, scegliere la categoria che si desidera modificare.

   ![Albero categoria](./assets/category-selected.png){width="700" zoomable="yes"}

## Passaggio 2: ordinare i prodotti

>[!NOTE]
>
>Quando si ordina una categoria in base a un attributo di prodotto, anche i prodotti con gli stessi valori di attributo vengono ordinati in base al rispettivo _[!UICONTROL Product ID]_in ordine crescente.

In _[!UICONTROL Products in Category]_, fare clic sulle tessere ( ![Visualizza riquadri](../assets/icon-view-tiles.png) ) per mostrare le sezioni del prodotto in una griglia. Utilizzare il metodo manuale o automatico per ordinare i prodotti.

![Riquadri prodotto](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Metodo 1: ordinamento manuale

1. Imposta **[!UICONTROL Sort Order]** secondo le tue preferenze.

   ![Ordinamento](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Per applicare il nuovo ordinamento, fare clic su **[!UICONTROL Sort]**.

1. Per salvare l&#39;ordinamento, fare clic su **[!UICONTROL Save Category]**.

1. Quando richiesto, aggiorna eventuali indicizzatori non validi.

### Metodo 2: ordinamento automatico

1. Imposta **[!UICONTROL Match products by rule]** (![Attiva/disattiva sì](../assets/toggle-yes.png)) a `Yes`.


1. Imposta **[!UICONTROL Automatic Sorting]** secondo le tue preferenze.

1. Per creare una regola di categoria, seguire le istruzioni del passaggio successivo.

## Passaggio 3: creare una regola di categoria

1. Imposta **[!UICONTROL Match products by rule]** (![Attiva/disattiva sì](../assets/toggle-yes.png)) a `Yes`.

1. Clic **[!UICONTROL Add Condition]**.

1. Scegli la **[!UICONTROL Attribute]** questa è la base della condizione.

1. Imposta **[!UICONTROL Operator]** a uno dei seguenti elementi:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Immetti il valore appropriato **[!UICONTROL Value]**.

   ![Condizione categoria](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Per aggiungere un’altra condizione, fai clic su **[!UICONTROL Add Condition]** e ripetere il processo.

## Passaggio 4: salvare, aggiornare e verificare

1. Al termine, fai clic su **[!UICONTROL Save Category]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** e aggiorna ogni cache non valida.

1. Nella vetrina, verifica che le regole di selezione, ordinamento e categoria del prodotto funzionino correttamente.

   Se è necessario apportare modifiche, modificarle e riprovare.
