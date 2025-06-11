---
title: Layout di pagina
description: Scopri le sezioni di layout di pagina e come configurare i layout predefiniti.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# Layout di pagina

Il layout di ogni pagina del punto vendita è costituito da sezioni o contenitori distinti che definiscono l&#39;intestazione, il piè di pagina e le aree di contenuto della pagina. A seconda del layout, ogni pagina può avere una, due, tre colonne o più. È possibile considerare il layout come la _piantina_ della pagina e assegnare un layout specifico da utilizzare come predefinito per le pagine CMS, prodotto e categoria.

Nella pagina, i blocchi di contenuto vengono spostati per riempire lo spazio disponibile, in base alla sezione del [layout di pagina](layout-updates.md) a cui sono assegnati. Se si modifica il layout da un layout a tre colonne a un layout a due colonne, il contenuto dell&#39;area principale si espande fino a riempire lo spazio disponibile. Inoltre, eventuali blocchi associati alla barra laterale non utilizzata sembrano scomparire. Tuttavia, se ripristini il layout a tre colonne, i blocchi vengono nuovamente visualizzati. Questo approccio fluido, o _layout liquido_, consente di modificare il layout della pagina senza dover rielaborare il contenuto. Se si è abituati a lavorare con singole pagine HTML, questo approccio modulare _blocco predefinito_ richiede un modo di pensare diverso.

![Standard a due colonne con layout di pagina barra sinistra](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Configurare i layout predefiniti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Default Layouts]**.

   ![Layout predefiniti](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Scegliere **[!UICONTROL Default Product Layout]** da utilizzare per le pagine di prodotti.

   Questa impostazione determina il layout utilizzato per impostazione predefinita per le pagine di prodotto.

   - `No layout updates` - Gli aggiornamenti del layout non sono disponibili per le pagine di prodotto.
   - `Empty` - Utilizza un layout vuoto per le pagine di prodotti.
   - `1 column` - Utilizza un layout a colonna singola per le pagine di prodotto.
   - `2 columns with left bar` - Utilizza un layout a due colonne con barra laterale a sinistra per le pagine di prodotti.
   - `2 columns with right bar` - Utilizza un layout a due colonne con barra laterale a destra per le pagine di prodotti.
   - `3 columns` - Utilizza un layout a tre colonne con barre laterali a sinistra e a destra per le pagine di prodotti.

   Quando [Page Builder](../page-builder/introduction.md) è abilitato, sono disponibili altre opzioni a larghezza intera. Puoi quindi utilizzare gli strumenti di contenuto Page Builder per progettare il layout delle pagine di prodotto.

   - `Page -- Full Width` - Utilizza il layout _Pagina - Larghezza intera_ per le pagine di prodotto.
   - `Category -- Full Width` - Utilizza il layout _Categoria - Larghezza intera_ per le pagine di prodotti.
   - `Product -- Full Width` - (Consigliato) Utilizza il layout _Prodotto - Larghezza intera_ per le pagine di prodotti.

1. Scegliere **[!UICONTROL Default Category Layout]** da utilizzare per le pagine delle categorie.

   Questa impostazione determina il layout utilizzato per impostazione predefinita per le pagine delle categorie.

   - `No layout updates` - Gli aggiornamenti del layout non sono disponibili per le pagine delle categorie.
   - `Empty` - Utilizza un layout vuoto per le pagine delle categorie.
   - `1 column` - Utilizza un layout a colonna singola per le pagine delle categorie.
   - `2 columns with left bar` - Utilizza un layout a due colonne con barra laterale a sinistra per le pagine delle categorie.
   - `2 columns with right bar` - Utilizza un layout a due colonne con barra laterale a destra per le pagine delle categorie.
   - `3 columns` - Utilizza un layout a tre colonne con barre laterali a sinistra e a destra per le pagine delle categorie.

   Quando [Page Builder](../page-builder/introduction.md) è abilitato, sono disponibili altre opzioni a larghezza intera. Puoi quindi utilizzare gli strumenti di contenuto Page Builder per progettare il layout delle pagine delle categorie.

   - `Page -- Full Width` - Utilizza il layout _Pagina - Larghezza intera_ per le pagine delle categorie.
   - `Category -- Full Width` - (Consigliato) Utilizza il layout _Categoria - Larghezza intera_ per le pagine delle categorie.
   - `Product -- Full Width` - Utilizza il layout _Prodotto - Larghezza intera_ per le pagine delle categorie.

1. Scegliere **[!UICONTROL Default Page Layout]** da utilizzare per le pagine CMS.

   Questa impostazione determina il layout utilizzato per impostazione predefinita per le pagine CMS.

   - `No layout updates` - Gli aggiornamenti del layout non sono disponibili per le pagine CMS.
   - `Empty` - Utilizza un layout vuoto per le pagine CMS.
   - `1 column` - Utilizza un layout a colonna singola per le pagine CMS.
   - `2 columns with left bar` - Utilizza un layout a due colonne con barra laterale a sinistra per le pagine CMS.
   - `2 columns with right bar` - Utilizza un layout a due colonne con barra laterale a destra per le pagine CMS.
   - `3 columns` - Utilizza un layout a tre colonne con barre laterali a sinistra e a destra per le pagine CMS.

   Quando [Page Builder](../page-builder/introduction.md) è abilitato, sono disponibili altre opzioni a larghezza intera. È quindi possibile utilizzare gli strumenti di contenuto Page Builder per progettare il layout delle pagine CMS.

   - `Page -- Full Width` - (Consigliato) Utilizza il layout _Pagina - Larghezza intera_ per le pagine CMS.
   - `Category - Full Width` - Utilizza il layout _Categoria - Larghezza intera_ per le pagine CMS.
   - `Product - Full Width` - Utilizza il layout _Prodotto - Larghezza intera_ per le pagine CMS.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Layout di pagina standard

### Una colonna

![Diagramma - layout a una colonna](./assets/layout-1-col-th.png){zoomable="yes"}

Il layout _[!UICONTROL 1 Column]_può essere utilizzato per creare una home page di grandi dimensioni con un&#39;immagine di grandi dimensioni o un punto focale. È inoltre una buona scelta per una pagina di destinazione o qualsiasi altra pagina con una combinazione di testo, immagini e video.

### Due colonne con barra a sinistra

![Diagramma - layout a due colonne con barra a sinistra](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

Il layout _[!UICONTROL 2 Columns with Left Bar]_viene spesso utilizzato per le pagine con navigazione a sinistra, ad esempio un catalogo o pagine dei risultati di ricerca con navigazione a livelli. Si tratta inoltre di una scelta eccellente per le home page che richiedono una navigazione aggiuntiva o blocchi di contenuto di supporto a sinistra.

### Due colonne con barra a destra

![Diagramma - layout a due colonne con barra destra](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

Con un layout _[!UICONTROL 2 Columns with Right Bar]_, l&#39;area del contenuto principale è sufficientemente grande da consentire la visualizzazione di immagini o banner accattivanti. Questo layout viene spesso utilizzato anche per le pagine di prodotto con blocchi di contenuto di supporto a destra.

### Tre colonne

![Diagramma - layout a tre colonne](./assets/layout-3-col-th.png){zoomable="yes"}

Il layout _[!UICONTROL 3 Column]_ha una colonna centrale sufficientemente ampia per il testo principale della pagina, con spazio su ciascun lato per ulteriori elementi di navigazione e blocchi di contenuto di supporto.

### Vuoto

![Diagramma - layout vuoto](./assets/layout-blank-th.png){zoomable="yes"}

Il layout _[!UICONTROL Empty]_può essere utilizzato per definire layout di pagina personalizzati.
