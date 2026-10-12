---
title: Panoramica di Visual Merchandiser
description: Scopri gli strumenti di Visual Merchandiser che ti consentono di posizionare i prodotti e determinare quali prodotti visualizzare nell’elenco delle categorie.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: 'https://experienceleague.adobe.com/MbeCfIBdepAr5U2B1I-lfFGNm1b5DiKGevM5365brpo'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '394'
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
