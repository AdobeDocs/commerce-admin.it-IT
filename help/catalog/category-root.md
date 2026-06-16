---
title: Categoria principale e gerarchia
description: Scopri la gerarchia delle categorie e la categoria principale, che funge da contenitore per il menu principale nella struttura delle categorie.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/nkUEOu8IqMM21waPwmkp76YckH6cToL6MiaSK--klho
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# Categoria principale e gerarchia

I prodotti nel menu principale sono determinati dalla categoria principale assegnata all&#39;archivio [store](../stores-purchase/stores.md#add-stores). La categoria principale è fondamentalmente un contenitore per il menu principale nella struttura delle categorie. Puoi creare una categoria principale con un set completamente nuovo di prodotti o copiare prodotti da una categoria principale esistente. La categoria principale può essere assegnata all’archivio corrente o a qualsiasi altro archivio nello stesso sito web.

![Diagramma della gerarchia del catalogo](./assets/catalog-hierarchy-scope.svg){width="550"}

In Admin, la struttura delle categorie è simile a una struttura capovolta, con la directory principale in alto. La directory principale ha un nome, ma non una chiave URL e non viene visualizzata nella [navigazione superiore](navigation-top.md) dell&#39;archivio. Tutte le altre categorie nel menu sono nidificate sotto la directory principale. Poiché la categoria principale è il livello più alto del catalogo, l’archivio può avere una sola categoria principale attiva alla volta. È tuttavia possibile creare ulteriori categorie principali per strutture di catalogo alternative e archivi diversi.

Nell&#39;esempio seguente viene illustrato come creare una categoria radice e assegnarla a un altro archivio.

## Passaggio 1: creare una categoria principale

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. A sinistra, fare clic su **[!UICONTROL Add Root Category]**.

   ![Nuova categoria principale](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Immetti **[!UICONTROL Category Name]**.

   Il nome scelto viene inizialmente assegnato a tutte le visualizzazioni dello store.

1. Se si desidera aggiungere prodotti al catalogo dal catalogo corrente, eseguire le operazioni seguenti:

   - Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione _Prodotti nella categoria_.

   - Utilizza i [filtri di ricerca](../getting-started/admin-grid-controls.md) per trovare i prodotti desiderati e seleziona la casella di controllo per ogni prodotto da copiare nel nuovo catalogo.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Passaggio 2: creare il menu principale

1. A sinistra, seleziona la nuova categoria principale creata nel passaggio precedente.

1. Per creare la [struttura di categoria](category-create.md) per il menu principale, fare clic su **[!UICONTROL Add Subcategory]** e seguire le istruzioni.

## Passaggio 3: assegnare la categoria principale all&#39;archivio

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Nella colonna _Archivi_ della griglia fare clic sull&#39;archivio a cui si desidera assegnare il nuovo catalogo.

1. Impostare **[!UICONTROL Root Category]** sulla nuova categoria radice creata.

1. Assicurarsi che all&#39;archivio sia assegnato **[!UICONTROL Default Store View]**.

   L&#39;archivio deve avere almeno una [visualizzazione archivio](../stores-purchase/store-views.md).

1. Al termine, fare clic su **[!UICONTROL Save Store]**.

1. Per verificare che l&#39;archivio disponga di un nuovo catalogo, eseguire le operazioni seguenti:

   - Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Tutti i prodotti copiati nel nuovo catalogo vengono visualizzati nella griglia.

   - Per verificare che il nuovo catalogo e il menu principale funzionino correttamente, visita la vetrina.
