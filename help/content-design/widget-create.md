---
title: Creare e gestire i widget
description: Scopri come creare e gestire i widget che aggiornano automaticamente i contenuti nel tuo store.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# Creare e gestire i widget

I widget sono componenti riutilizzabili. Puoi creare facilmente widget e modificare quelli esistenti per aggiornare automaticamente il contenuto nel tuo store. È inoltre possibile eliminare i widget non più in uso.

![Widget](./assets/widgets.png){width="700" zoomable="yes"}

## Creare un widget

Il processo di creazione di un widget è quasi lo stesso per ciascuno [tipo di widget](widgets.md#widget-types). È possibile seguire la prima parte delle istruzioni e quindi completare l&#39;ultima parte per il tipo specifico di widget desiderato.

### Passaggio 1: scegliere il tipo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Clic **[!UICONTROL Add Widget]**.

1. In _[!UICONTROL Settings]_sezione:

   - Imposta **[!UICONTROL Type]** al tipo di widget che si desidera creare.

   - Verificare che **[!UICONTROL Design Theme]** è impostato sul tema corrente.

     ![Impostazioni widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Continue]**.

### Passaggio 2: specificare le proprietà e il layout della vetrina

1. In _[!UICONTROL Storefront Properties]_sezione:

   - Per **[!UICONTROL Widget Title]**, immetti un titolo descrittivo per il widget.

     Questo titolo è visibile solo dall’amministratore.

   - Per **[!UICONTROL Assign to Store Views]**, selezionare le visualizzazioni dello store in cui si desidera rendere visibile il widget.

     Puoi selezionare una visualizzazione specifica dello store, oppure `All Store Views`. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di visualizzazione di questo elemento con altri nella stessa parte della pagina. (`0` = innanzitutto, `1` = secondo, `3` = terzo e così via.)

     ![Proprietà vetrina](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. In _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**.

1. Imposta **[!UICONTROL Display On]** al tipo di pagina in cui deve essere visualizzata.

1. In **[!UICONTROL Container]** , scegliere l&#39;area del layout di pagina in cui deve essere posizionato.

   ![Aggiornamenti del layout](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Se il widget è un collegamento, imposta **[!UICONTROL Template]** a uno dei seguenti elementi:

   - `Block Template` - Formatta il contenuto in modo che possa essere posizionato come unità indipendente sulla pagina.
   - `Inline Template` - Formatta il contenuto in modo che possa essere inserito all&#39;interno di altri contenuti. Ad esempio, un collegamento che si trova all&#39;interno di un paragrafo di testo.

### Passaggio 3: completare le opzioni widget

Le opzioni per ogni tipo di widget variano leggermente, ma il processo è sostanzialmente lo stesso. Nell&#39;esempio seguente viene visualizzato l&#39;elenco dei prodotti per una categoria specifica, con controlli di impaginazione.

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Clic **[!UICONTROL Select Block]**.

1. Immetti un **[!UICONTROL Title]** sopra l&#39;elenco, ad esempio `Featured Products`.

1. Per i controlli di impaginazione, impostare **[!UICONTROL Display Page Control]** a `Yes`  ed effettuare le seguenti operazioni:

   - Inserisci il **[!UICONTROL Number of Products per Page]**.

   - Immetti il totale **[!UICONTROL Number of Products to Display]**.

   - Imposta **[!UICONTROL Condition]** alla categoria di prodotti da presentare.

     Il processo equivale a impostare una condizione per un [regola di prezzo](../merchandising-promotions/price-rules-catalog.md).

### Passaggio 4: Salvare e verificare il risultato

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando richiesto, segui le istruzioni nella parte superiore dell’area di lavoro per aggiornare la cache in base alle esigenze.

1. Torna alla vetrina per verificare che il widget funzioni correttamente.

   Per spostarlo in una posizione diversa, puoi riaprire il widget e provare un riferimento a una pagina o a un blocco diverso.

## Demo sulla creazione di widget

Per informazioni sulla creazione di widget, guarda questo video:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## Modificare un widget

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Individuate il widget utilizzando i filtri sopra la griglia, quindi fate clic sul nome del widget.

1. Apporta le modifiche necessarie.

   Per informazioni sulle opzioni del widget, consultate i passaggi per la creazione di un widget.

1. Fai clic su **[!UICONTROL Save]**.

## Eliminare un widget

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Individuate i widget utilizzando i filtri sopra la griglia, quindi selezionate la casella di controllo dei widget da eliminare.

1. Nell&#39;angolo superiore sinistro dell&#39;elenco, impostare **[!UICONTROL Actions]** a `Delete`.

1. Al termine, fai clic su **[!UICONTROL Submit]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.
