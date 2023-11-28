---
title: Utilizzare un widget per posizionare un blocco
description: Scopri come utilizzare un widget di blocchi statici per inserire un contenuto esistente quasi ovunque all’interno del tuo store.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Utilizzare un widget per posizionare un blocco

Il _Blocco statico CMS_ [widget](widgets.md) consente di inserire un elemento esistente [blocco di contenuto](blocks.md) praticamente ovunque nel tuo negozio.

![Widget](./assets/widgets.png){width="700" zoomable="yes"}

## Passaggio 1: scegliere il tipo di widget

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Widget]**.

1. In _Impostazioni_ sezione, set **[!UICONTROL Type]** a `CMS Static Block` e fai clic su **[!UICONTROL Continue]**.

1. Verificare che **[!UICONTROL Design Theme]** è impostato sul tema corrente e fai clic su **[!UICONTROL Continue]**.

   ![Impostazioni widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. In _[!UICONTROL Storefront Properties]_eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immetti un titolo descrittivo per il widget.

     Questo titolo è visibile solo dal _Amministratore_.

   - Per **[!UICONTROL Assign to Store Views]**, selezionare le visualizzazioni dello store in cui è visibile il widget.

     Puoi selezionare una visualizzazione specifica dello store, oppure `All Store Views`. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di visualizzazione di questo elemento con altri nella stessa parte della pagina. (`0` = innanzitutto, `1` = secondo, `3` = terzo e così via.)

     ![Proprietà vetrina](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Passaggio 2: completare gli aggiornamenti del layout dei widget

1. In _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**.

1. Imposta **[!UICONTROL Display On]** alla categoria, al prodotto o alla pagina in cui si desidera visualizzare il blocco.

1. Per posizionare il blocco su una pagina specifica, eseguire le operazioni seguenti:

   - Scegli la **[!UICONTROL Page]** dove si desidera visualizzare il blocco.

   - Scegli la **[!UICONTROL Block Reference]** che identifica il punto in cui il blocco viene visualizzato sulla pagina.

   - Accetta l&#39;impostazione predefinita per **[!UICONTROL Template]**, impostato su `CMS Static Block Default Template`.

     ![Aggiornamenti del layout](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Opzioni di aggiornamento del layout

| Campo | Descrizione |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Visualizza il widget nella pagina della categoria di ancoraggio.<br/>**[!UICONTROL Categories]**- Categorie in cui viene visualizzato l&#39;ancoraggio. Opzioni: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** : imposta il contenitore sulla parte del layout di pagina in cui desideri visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |
| [!UICONTROL Non-Anchor Categories] | Visualizza il widget nella pagina della categoria non di ancoraggio.<br/>**[!UICONTROL Categories]**- Categorie in cui viene visualizzato l&#39;ancoraggio. Opzioni: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** : imposta il contenitore sulla parte del layout di pagina in cui desideri visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |
| **_[!UICONTROL Products]_** |  |
| Tutti i tipi di prodotto | Visualizza il widget su una pagina di prodotto specifica o su tutte le pagine di prodotto. <br/>**[!UICONTROL Products]**- Prodotti per i quali viene visualizzato il widget. Opzioni: `All` /` Specific Products`<br/>**[!UICONTROL Container]** : imposta il contenitore sulla parte del layout di pagina in cui desideri visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Visualizza il widget su tutte le pagine. <br/>**[!UICONTROL Container]**: imposta il contenitore sulla parte del layout di pagina in cui desideri visualizzare il widget.<br/>**[!UICONTROL Template]** - Determina il tema del layout. |
| [!UICONTROL Specified Page] | Visualizza il widget su una pagina specifica. Opzioni:<br/>**[!UICONTROL Page]**- Pagine per le quali viene visualizzato il widget.<br/>**[!UICONTROL Container]** : imposta il contenitore sulla parte del layout di pagina in cui desideri visualizzare il widget.<br/>**Modello** - Determina il tema del layout. |
| [!UICONTROL Page Layouts] | Visualizza il widget nelle pagine con un determinato layout. <br/>**[!UICONTROL Page]**- Pagine per le quali viene visualizzato il widget.<br/>**[!UICONTROL Container]** : imposta il contenitore sulla parte del layout di pagina in cui desideri visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |

{style="table-layout:auto"}

## Passaggio 3: posizionare il blocco

1. Nel pannello a sinistra, seleziona **[!UICONTROL Widget Options]**.

1. Clic **[!UICONTROL Select Block…]** e scegli il blocco che desideri inserire dall’elenco.

1. Al termine, fai clic su **[!UICONTROL Save]**.

   L’app ora viene visualizzata nell’elenco.

1. Quando richiesto, segui le istruzioni nella parte superiore della pagina per aggiornare l’indice e la cache delle pagine.

1. Torna alla vetrina per verificare che il blocco sia visualizzato nella posizione corretta.

   Per spostare il blocco, puoi riaprire il widget o provare un riferimento a una pagina o a un blocco diverso.
