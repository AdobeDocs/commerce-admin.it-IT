---
title: Widget carosello eventi catalogo
description: Scopri come utilizzare un widget carosello eventi catalogo per visualizzare un cursore dei prossimi eventi su una pagina.
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Widget carosello eventi catalogo

{{ee-feature}}

Un widget carosello eventi catalogo visualizza un cursore dei prossimi eventi con un ticker conto alla rovescia per ogni evento. Puoi scegliere le pagine e l’area del layout di pagina in cui visualizzare il carosello e controllare la larghezza e il numero di eventi che vengono visualizzati contemporaneamente. Il risultato ottenuto dipende dal tema, dalla posizione in cui viene visualizzato nella pagina e dalle opzioni selezionate.

![Carosello eventi nella barra laterale a sinistra](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## Passaggio 1: abilitare il widget carosello catalogo

Prima di iniziare, segua le istruzioni [istruzioni](../merchandising-promotions/event-configure.md) per configurare _Evento catalogo_ widget in modo che sia abilitato per la vetrina.

![Configurazione evento catalogo](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## Passaggio 2: creare il widget

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Widget]**.

1. In _[!UICONTROL Settings]_eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Type]** a `Catalog Events Carousel`.

   - Scegli la **[!UICONTROL Design Theme]** che viene utilizzato dal negozio.

1. Clic **[!UICONTROL Continue]**.

   ![Impostazioni del widget per un carosello di eventi](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. In _[!UICONTROL Storefront Properties]_eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immetti un titolo descrittivo per il widget.

     Questo titolo è visibile solo dal _Amministratore_.

   - Per **[!UICONTROL Assign to Store Views]**, selezionare le visualizzazioni dello store in cui si desidera rendere visibile il widget.

     Puoi selezionare una visualizzazione specifica dello store, oppure `All Store Views`. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di visualizzazione di questo elemento con altri nella stessa parte della pagina. (`0` = innanzitutto, `1` = secondo, `3` = terzo e così via.)

     ![Proprietà vetrina widget](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## Passaggio 3: scegliere la posizione

1. In _Aggiornamenti del layout_ , fare clic su **[!UICONTROL Add Layout Update]**.

1. Imposta **[!UICONTROL Display On]** a `Specified Page`.

1. Imposta **[!UICONTROL Page]** a `CMS Home Page`.

1. Imposta **[!UICONTROL Container]** uno dei seguenti elementi:

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >I risultati variano in base al tema e al layout della pagina. È inoltre necessario specificare _[!UICONTROL Catalog Events Carousel Default Template]_nella configurazione della categoria.

1. Se desideri che il carosello degli eventi venga visualizzato in un’altra posizione nella vetrina, fai clic su **[!UICONTROL Add Layout Update]** e ripeti questi passaggi per quella posizione.

   ![Aggiornamenti del layout](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save and Continue Edit]**.

   Per il momento, puoi ignorare il messaggio per aggiornare la cache.

## Passaggio 4: configurare le opzioni

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Per **[!UICONTROL Frame Size]**, immettere il numero di eventi che si desidera elencare nel dispositivo di scorrimento contemporaneamente.

   Per visualizzare un solo evento alla volta, immetti `1`.

1. Per **[!UICONTROL Scroll]**, immetti il numero di elenchi di eventi da scorrere per clic.

   Per scorrere fino all&#39;evento successivo, immetti `1`.

1. Per una larghezza personalizzata, immetti il numero di pixel per **[!UICONTROL Block Custom Width]**.

   Nella pagina di esempio seguente, la larghezza personalizzata è impostata su 250 pixel.

   ![Opzioni widget larghezza personalizzata](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, fai clic sul collegamento nel messaggio nella parte superiore della pagina e segui le istruzioni.
