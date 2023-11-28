---
title: Categorie - Impostazioni contenuto
description: Scopri come utilizzare il [!UICONTROL Content] per definire eventuali contenuti aggiuntivi visualizzati nella pagina categoria.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Categorie - Impostazioni contenuto

Il _[!UICONTROL Content]_le impostazioni determinano la visualizzazione di eventuali contenuti aggiuntivi nella pagina categoria. Oltre all’elenco dei prodotti della categoria, la pagina può includere un’immagine, una descrizione e un blocco CMS. È possibile utilizzare [[!DNL Page Builder]](../page-builder/introduction.md) strumenti di contenuto per definire la descrizione della categoria.

## Aggiungi la descrizione della categoria in [!DNL Page Builder]

1. Apri la categoria in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** sezione.

   ![Contenuto categoria](./assets/category-content.png){width="600" zoomable="yes"}

1. In alto a destra nella **[!UICONTROL Description]** , fare clic su **[!UICONTROL Edit with Page Builder]**.

1. Utilizza il [[!DNL Page Builder]](../page-builder/introduction.md) strumenti di contenuto per [modificare il testo esistente](../page-builder/text.md) e aggiungi altro contenuto (se necessario).

## [!DNL Page Builder] anteprima

Quando si espande _Contenuto_ sezione per una categoria esistente in cui è presente contenuto creato con [!DNL Page Builder], visualizza un’anteprima del **[!UICONTROL Description]** contenuto come apparirebbe nella pagina della categoria. Facendo clic sull’area del contenuto si apre [!DNL Page Builder] in cui è possibile apportare gli aggiornamenti necessari.

![Anteprima descrizione](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Per impostazione predefinita, questa anteprima di contenuto è abilitata per i moduli di prodotti e categorie. Se le prestazioni diminuiscono a causa del caricamento dell’anteprima, puoi disabilitare l’anteprima in [Configurazione gestione contenuti](../configuration-reference/general/content-management.md#advanced-content-tools) impostazioni.

## Aggiungi la descrizione della categoria nell’editor

Immettere solo caratteri ASCII normali nella casella di testo. Se si incolla testo da un elaboratore di testi, salvarlo innanzitutto come file TXT semplice per rimuovere eventuali caratteri di controllo invisibili.

Per ulteriori informazioni, consulta [Editor WYSIWYG](../content-design/editor.md).

1. Apri la categoria in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** sezione.

   ![Contenuto categoria](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Immetti la categoria **[!UICONTROL Description]** e utilizza [barra degli strumenti dell’editor](../content-design/editor.md) per formattare in base alle esigenze.

   È possibile trascinare l&#39;angolo inferiore destro per modificare l&#39;altezza della casella di testo.

## Aggiungere un blocco CMS alla pagina della categoria

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la categoria che si desidera modificare.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** sezione.

1. Per **[!UICONTROL Add the CMS block]**, seleziona il blocco da aggiungere.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Display Settings]** sezione.

1. Imposta il **[!UICONTROL Display Mode]** a uno dei seguenti elementi:

   - `Static block only`
   - `Static block and products`

1. Al termine, fai clic su **[!UICONTROL Save]** e controlla la visualizzazione del blocco sulla vetrina (richiede l’aggiornamento della cache).

## Riferimento per le impostazioni del contenuto

| Impostazione | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Category Image] | Visualizzazione store | Specifica un&#39;immagine per la parte superiore della pagina della categoria. Metodi: <br/><br/>**[!UICONTROL Upload]**: carica un file di immagine dal computer locale alla raccolta e lo utilizza come immagine della categoria.<br/><br/>**[!UICONTROL Select from Gallery]** - Richiede di scegliere un&#39;immagine esistente dalla raccolta. <br/><br/>![Icona della fotocamera di Page Builder](../assets/icon-camera.png) - Trascinate un file di immagine sul riquadro della fotocamera o individuate l&#39;immagine e selezionatela dal file system locale. |
| [!UICONTROL Description] | Visualizzazione store | Specifica una descrizione visualizzata nella pagina della categoria. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Apre il [[!DNL Page Builder] workspace](../page-builder/workspace.md), in cui è possibile modificare la descrizione.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Attiva o disattiva la visualizzazione tra le modalità WYSIWYG Editor e HTML. |
| [!UICONTROL Add CMS Block] | Visualizzazione store | Aggiunge un [Blocco CMS](../content-design/blocks.md) alla pagina categoria. |

{style="table-layout:auto"}
