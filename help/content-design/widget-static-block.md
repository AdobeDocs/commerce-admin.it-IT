---
title: Utilizzare un widget per posizionare un blocco
description: Scopri come utilizzare un widget di blocchi statici per inserire un contenuto esistente quasi ovunque all’interno del tuo store.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Utilizzare un widget per posizionare un blocco

Il _blocco statico di CMS_ [widget](widgets.md) consente di inserire un [blocco di contenuto](blocks.md) esistente in qualsiasi punto dell&#39;archivio.

![Widget](./assets/widgets.png){width="700" zoomable="yes"}

## Passaggio 1: scegliere il tipo di widget

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Widget]**.

1. Nella sezione _Impostazioni_, impostare **[!UICONTROL Type]** su `CMS Static Block` e fare clic su **[!UICONTROL Continue]**.

1. Verificare che **[!UICONTROL Design Theme]** sia impostato sul tema corrente e fare clic su **[!UICONTROL Continue]**.

   ![Impostazioni widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Nella sezione _[!UICONTROL Storefront Properties]_eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immettere un titolo descrittivo per il widget.

     Questo titolo è visibile solo da _Admin_.

   - Per **[!UICONTROL Assign to Store Views]**, selezionare le visualizzazioni dello store in cui è visibile il widget.

     È possibile selezionare una visualizzazione archivio specifica o `All Store Views`. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di visualizzazione di questo elemento con altri nella stessa parte della pagina. (`0` = primo, `1` = secondo, `3` = terzo e così via).

     ![Proprietà vetrina](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Passaggio 2: completare gli aggiornamenti del layout dei widget

1. Nella sezione _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**.

1. Impostare **[!UICONTROL Display On]** sulla categoria, sul prodotto o sulla pagina in cui si desidera visualizzare il blocco.

1. Per posizionare il blocco su una pagina specifica, eseguire le operazioni seguenti:

   - Scegliere **[!UICONTROL Page]** dove si desidera visualizzare il blocco.

   - Scegliere **[!UICONTROL Block Reference]** che identifica il punto in cui il blocco viene visualizzato nella pagina.

   - Accettare l&#39;impostazione predefinita per **[!UICONTROL Template]**, impostata su `CMS Static Block Default Template`.

     ![Aggiornamenti layout](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Opzioni di aggiornamento del layout

| Campo | Descrizione |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Visualizza il widget nella pagina della categoria di ancoraggio.<br/>**[!UICONTROL Categories]**- Categorie in cui viene visualizzato l&#39;ancoraggio. Opzioni: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Impostare il contenitore sulla parte del layout di pagina in cui si desidera visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |
| [!UICONTROL Non-Anchor Categories] | Visualizza il widget nella pagina della categoria non di ancoraggio.<br/>**[!UICONTROL Categories]**- Categorie in cui viene visualizzato l&#39;ancoraggio. Opzioni: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Impostare il contenitore sulla parte del layout di pagina in cui si desidera visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |
| **_[!UICONTROL Products]_** |  |
| Tutti i tipi di prodotto | Visualizza il widget su una pagina di prodotto specifica o su tutte le pagine di prodotto. <br/>**[!UICONTROL Products]**- Prodotti per i quali viene visualizzato il widget. Opzioni: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Impostare il contenitore sulla parte del layout di pagina in cui si desidera visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Visualizza il widget su tutte le pagine. <br/>**[!UICONTROL Container]**- Impostare il contenitore sulla parte del layout di pagina in cui si desidera visualizzare il widget.<br/>**[!UICONTROL Template]** - Determina il tema del layout. |
| [!UICONTROL Specified Page] | Visualizza il widget su una pagina specifica. Opzioni:<br/>**[!UICONTROL Page]**- Pagine per le quali viene visualizzato il widget.<br/>**[!UICONTROL Container]** - Impostare il contenitore sulla parte del layout di pagina in cui si desidera visualizzare il widget.<br/>**Modello** - Determina il tema del layout. |
| [!UICONTROL Page Layouts] | Visualizza il widget nelle pagine con un determinato layout. <br/>**[!UICONTROL Page]**- Pagine per le quali viene visualizzato il widget.<br/>**[!UICONTROL Container]** - Impostare il contenitore sulla parte del layout di pagina in cui si desidera visualizzare il widget.<br/>**[!UICONTROL Template]**- Determina il tema del layout. |

{style="table-layout:auto"}

## Passaggio 3: posizionare il blocco

1. Nel pannello a sinistra, seleziona **[!UICONTROL Widget Options]**.

1. Fare clic su **[!UICONTROL Select Block…]** e scegliere il blocco che si desidera inserire dall&#39;elenco.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   L’app ora viene visualizzata nell’elenco.

1. Quando richiesto, segui le istruzioni nella parte superiore della pagina per aggiornare l’indice e la cache delle pagine.

1. Torna alla vetrina per verificare che il blocco sia visualizzato nella posizione corretta.

   Per spostare il blocco, puoi riaprire il widget o provare un riferimento a una pagina o a un blocco diverso.
