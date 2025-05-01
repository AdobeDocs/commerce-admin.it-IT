---
title: Panoramica di Visual Merchandiser
description: Scopri gli strumenti di Visual Merchandiser che ti consentono di posizionare i prodotti e determinare quali prodotti visualizzare nell’elenco delle categorie.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_Visual Merchandiser_ è un set di strumenti avanzati che consente di posizionare i prodotti e applicare condizioni che determinano quali prodotti vengono visualizzati nell&#39;elenco delle categorie. Il risultato può essere una selezione dinamica di prodotti che si adatta alle modifiche nel catalogo. È possibile lavorare in _modalità visiva_, che mostra ogni prodotto come una sezione su una griglia, oppure lavorare da un elenco di prodotti della categoria. Gli stessi strumenti sono disponibili in ogni modalità e puoi utilizzare i pulsanti nell’angolo superiore destro per passare da un tipo di visualizzazione all’altro.

![Categoria prodotti nella visualizzazione affiancata](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Accedere a Visual Merchandiser

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Espandere la struttura delle categorie e fare clic sulla categoria da modificare.

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Products in Category]**.

1. Fai clic sul pulsante _Visualizza come riquadri_ ( ![Visualizza come riquadri](../assets/icon-view-tiles.png) ) per visualizzare i prodotti come griglia.

1. Al termine, fare clic su **[!UICONTROL Save Category]**.

## Modificare la posizione di un prodotto

1. Utilizza l&#39;[ordinamento](../catalog/navigation-product-listings.md) per visualizzare il prodotto che desideri spostare.

   - **Metodo 1: trascinamento**

     Acquisisci il controllo _Trascina_ (![Trascina icona](../assets/icon-move.png)) nell&#39;angolo superiore destro del riquadro del prodotto e rilascia il prodotto nella posizione desiderata. Il numero di ciascun prodotto viene regolato in base alla nuova posizione.

   - **Metodo 2: Imposta valore posizione**

     Nel controller _Position_ (![Position field](../assets/control-position.png)) del riquadro del prodotto, immettere il numero in cui si desidera visualizzare il prodotto. Immetti `0` per posizionare il prodotto all&#39;inizio dell&#39;elenco.

1. Al termine, fare clic su **[!UICONTROL Save Category]**.

>[!NOTE]
>
>In un&#39;installazione pulita, Adobe Commerce riserva l&#39;ID di categoria `2` per il catalogo principale dell&#39;archivio predefinito. In Visual Merchandiser è possibile utilizzare solo categorie con un numero di ID pari a `3` o superiore.

## Controlli Workspace

| Controllo | Descrizione |
|--- |--- |
| ![Icona Visualizza elenco](../assets/icon-view-list.png) | Visualizza come elenco |
| ![Icona Visualizza come sezioni](../assets/icon-view-tiles.png) | Visualizza come sezioni |
| ![Attiva/Disattiva corrispondenza per regola - No](../assets/toggle-no.png) | Corrispondenza per regola - no |
| ![Attiva/Disattiva corrispondenza per regola - sì](../assets/toggle-yes.png) | Corrispondenza per regola - sì |
| ![Icona Sposta](../assets/icon-move.png) | Trascina |
| ![Controller posizione](../assets/control-position.png) | Posizione |
| ![Icona Rimuovi da categoria](../assets/icon-delete-x.png) | Rimuovi dalla categoria |
| ![Elementi per controllo pagina](../assets/control-items-per-page.png) | Visualizza per pagina |
| ![Cambia visualizzazione pagina](../assets/control-page-display.png) | Vai a successivo/precedente |

{style="table-layout:auto"}
