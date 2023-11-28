---
title: Categoria principale e gerarchia
description: Scopri la gerarchia delle categorie e la categoria principale, che funge da contenitore per il menu principale nella struttura delle categorie.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Categoria principale e gerarchia

I prodotti nel menu principale sono determinati dalla categoria principale assegnata al [archiviare](../stores-purchase/stores.md#add-stores). La categoria principale è fondamentalmente un contenitore per il menu principale nella struttura delle categorie. Puoi creare una categoria principale con un set completamente nuovo di prodotti o copiare prodotti da una categoria principale esistente. La categoria principale può essere assegnata all’archivio corrente o a qualsiasi altro archivio nello stesso sito web.

![Diagramma della gerarchia del catalogo](./assets/catalog-hierarchy-scope.svg){width="550"}

In Admin, la struttura delle categorie è simile a una struttura capovolta, con la directory principale in alto. La directory principale ha un nome, ma non una chiave URL e non viene visualizzata nella [navigazione superiore](navigation-top.md) del negozio. Tutte le altre categorie nel menu sono nidificate sotto la directory principale. Poiché la categoria principale è il livello più alto del catalogo, l’archivio può avere una sola categoria principale attiva alla volta. È tuttavia possibile creare ulteriori categorie principali per strutture di catalogo alternative e archivi diversi.

Nell&#39;esempio seguente viene illustrato come creare una categoria radice e assegnarla a un altro archivio.

## Passaggio 1: creare una categoria principale

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. A sinistra, fai clic su **[!UICONTROL Add Root Category]**.

   ![Nuova categoria principale](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Immetti un **[!UICONTROL Category Name]**.

   Il nome scelto viene inizialmente assegnato a tutte le visualizzazioni dello store.

1. Se si desidera aggiungere prodotti al catalogo dal catalogo corrente, eseguire le operazioni seguenti:

   - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _Prodotti nella categoria_ sezione.

   - Utilizza il [filtri di ricerca](../getting-started/admin-grid-controls.md) per trovare i prodotti desiderati e selezionare la casella di controllo relativa a ciascun prodotto da copiare nel nuovo catalogo.

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Passaggio 2: creare il menu principale

1. A sinistra, seleziona la nuova categoria principale creata nel passaggio precedente.

1. Per creare [struttura delle categorie](category-create.md) nel menu principale, fai clic su **[!UICONTROL Add Subcategory]** e seguire le istruzioni.

## Passaggio 3: assegnare la categoria principale all&#39;archivio

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. In _Negozi_ nella griglia, fare clic sull&#39;archivio a cui si desidera assegnare il nuovo catalogo.

1. Imposta **[!UICONTROL Root Category]** alla nuova categoria principale creata.

1. Assicurati che il negozio abbia **[!UICONTROL Default Store View]** assegnato.

   Il negozio deve avere almeno un [visualizzazione store](../stores-purchase/store-views.md).

1. Al termine, fai clic su **[!UICONTROL Save Store]**.

1. Per verificare che l&#39;archivio disponga di un nuovo catalogo, eseguire le operazioni seguenti:

   - Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Tutti i prodotti copiati nel nuovo catalogo vengono visualizzati nella griglia.

   - Per verificare che il nuovo catalogo e il menu principale funzionino correttamente, visita la vetrina.
