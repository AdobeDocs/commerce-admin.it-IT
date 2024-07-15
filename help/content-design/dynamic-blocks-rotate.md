---
title: Aggiungere un blocco dinamico rotante
description: Presenta una presentazione di contenuti interattivi nella vetrina aggiungendo più blocchi dinamici a un rotatore.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# Aggiungere un blocco dinamico rotante

{{ee-feature}}

Per presentare una presentazione di contenuti interattivi, puoi aggiungere più [blocchi dinamici](dynamic-blocks.md) a un rotatore. Lo strumento [widget](widgets.md) viene utilizzato per posizionare il rotatore in un punto specifico di una singola pagina o di più pagine in tutto l&#39;archivio.

![Rotatore blocco dinamico](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Passaggio 1: creare singoli blocchi dinamici

Per [creare i blocchi dinamici](dynamic-blocks.md) che si desidera inserire nel rotatore, seguire le istruzioni seguenti:

## Passaggio 2: aggiungere un widget di rotazione a blocchi dinamici

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Widget]**.

1. In _Impostazioni_, impostare **[!UICONTROL Type]** su `Dynamic Blocks Rotator`.

1. Scegliere il **[!UICONTROL Design Theme]** corrente dell&#39;archivio.

   Questa impostazione identifica il pacchetto corrente o il [tema](themes.md) che determina il layout di pagina dell&#39;archivio.

1. Fare clic su **[!UICONTROL Continue]**.

   ![Impostazioni di rotazione blocchi dinamici](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Passaggio 3: completare le opzioni

1. In _Proprietà vetrina_, impostare le opzioni:

   - Immettere **[!UICONTROL Title]** per il rotatore.

   - Nell&#39;elenco **[!UICONTROL Assign to Store Views]**, selezionare le [visualizzazioni store](../getting-started/websites-stores-views.md) in cui è disponibile il rotatore.

   - (Facoltativo) Immettere un numero **[!UICONTROL Sort Order]** per determinare la posizione del rotatore nel contenitore di destinazione. È relativo ad altri widget che potrebbero essere assegnati allo stesso contenitore.

   ![Proprietà vetrina rotatore](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. In _Opzioni layout_, fare clic su **[!UICONTROL Add Layout Update]** ed eseguire le operazioni seguenti:

   - Impostare **[!UICONTROL Display on]** sulla pagina o sul tipo di pagina in cui verrà visualizzato il rotatore.

      - `Categories` - Visualizza il rotatore su [pagine di ancoraggio](../catalog/navigation-layered.md) o su pagine della categoria non di ancoraggio. Opzioni: Categorie di ancoraggio / Categorie non di ancoraggio
      - `Products` - Visualizza il rotatore su un tipo specifico di pagina di prodotto o su tutte le pagine di prodotto. Opzioni: Tutti I Tipi Di Prodotto / [Prodotto Semplice](../catalog/product-create-simple.md) / [Prodotto Virtuale](../catalog/product-create-virtual.md) / [Prodotto In Bundle](../catalog/product-create-bundle.md) / [Prodotto Scaricabile](../catalog/product-create-downloadable.md) / [Scheda Regalo](../catalog/product-gift-card-create.md) / [Prodotto Configurabile](../catalog/product-create-configurable.md) / [Prodotto Raggruppato](../catalog/product-create-grouped.md)
      - `Generic Pages` - Visualizza il rotatore su tutte le pagine, su una pagina specifica o solo sulle pagine con un determinato layout. Opzioni: `All Pages` / `Specified Page` / `Page Layouts`

     Nell&#39;esempio, il rotatore deve essere posizionato su un `Specified Page`.

   - Selezionare l&#39;elemento **[!UICONTROL Page]** specifico in cui verrà visualizzato il rotatore.

   - Imposta **[!UICONTROL Container]** sulla parte del [layout di pagina](page-layout.md#standard-page-layouts) in cui verrà visualizzato il rotatore.

     Se altri widget sono assegnati allo stesso contenitore, vengono visualizzati in sequenza in base all&#39;ordinamento.

   - Accettare `Dynamic Block Template` come predefinito **[!UICONTROL Template]**.

     Questa impostazione determina il modello utilizzato per formattare il rotatore, a seconda che il rotatore debba essere posizionato da solo o all&#39;interno del testo esistente.

     ![Aggiornamenti layout rotatore](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Fare clic su **[!UICONTROL Save and Continue Edit]**.

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Per **[!UICONTROL Dynamic Blocks to Display]**, accettare `Specified Dynamic Blocks`.

   Questa impostazione determina il tipo di blocchi dinamici inclusi nel rotatore.

   - `Specified Dynamic Blocks` - Include solo blocchi dinamici specifici.
   - `Cart Price Rule Related` - Include solo blocchi dinamici associati a una regola prezzo carrello.
   - `Catalog Price Rule Related` - Include solo blocchi dinamici associati a una regola del prezzo di catalogo.

1. Per **[!UICONTROL Restrict the Dynamic Block Types]** che può essere utilizzato con il widget, selezionare `Content Area`.

   Questa impostazione limita il banner a una parte specifica del layout di pagina.

   - `Content Area` - Posiziona il blocco dinamico nell&#39;area del contenuto principale della pagina.
   - `Footer` - Inserisce il blocco dinamico nel piè di pagina della pagina.
   - `Header` - Inserisce il blocco dinamico nell&#39;intestazione della pagina.
   - `Left Column` - Posiziona il blocco dinamico nella colonna sinistra del layout di pagina, se disponibile.
   - `Right Column` - Posiziona il blocco dinamico nella colonna destra del layout di pagina, se disponibile.

1. Imposta **[!UICONTROL Rotation Mode]** su uno dei seguenti:

   - `Display all instead of rotating` - Visualizza una pila di blocchi dinamici, dove sono tutti visibili.
   - `One at a time, Random` - Visualizza i blocchi dinamici specificati in ordine casuale. Quando la pagina viene aggiornata, viene visualizzato un blocco dinamico diverso (e casuale).
   - `One at the time, Series` - Visualizza i blocchi dinamici specificati nella sequenza in cui sono stati aggiunti. Quando la pagina viene aggiornata, viene visualizzato il blocco dinamico successivo nella sequenza.
   - `One at the time, Shuffle` - Visualizza un blocco dinamico alla volta in ordine casuale. Questa opzione è simile all&#39;opzione `One at a time, Random`, con la differenza che lo stesso blocco dinamico non viene ripetuto.

     ![Opzioni widget rotatore](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. Nella griglia **[!UICONTROL Specify Dynamic Blocks]** selezionare la casella di controllo di ogni blocco dinamico che si desidera includere nel rotatore.

1. Al termine, fare clic su **[!UICONTROL Save]**.
