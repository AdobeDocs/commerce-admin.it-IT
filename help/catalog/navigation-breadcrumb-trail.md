---
title: Tracce breadcrumb
description: Scopri i diversi modelli di percorso delle breadcrumb e come configurarli per visualizzarli nelle pagine di contenuto e catalogo.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Tracce breadcrumb

A _percorso breadcrumb_ è un set di collegamenti che mostra al cliente dove si trova in relazione ad altre pagine del negozio. Può fare clic su qualsiasi collegamento nella traccia delle breadcrumb per tornare alla pagina precedente.

È possibile configurare la traccia delle breadcrumb in modo che venga visualizzata sulle pagine di contenuto e sulle pagine di catalogo. Il formato e la posizione della traccia delle breadcrumb variano in base al tema, ma in genere si trova appena sotto l’intestazione. Per impostazione predefinita, la traccia delle breadcrumb viene visualizzata sulle pagine CMS.

![Traccia delle breadcrumb visualizzata nella vetrina](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## Tipi generali di briciole di pane

Le breadcrumb possono essere suddivise in tre tipi principali, che differiscono nel loro scopo. L&#39;essenza e i principi fondamentali dell&#39;attuazione di ogni tipo di briciole di pane sono descritti di seguito.

### Breadcrumb basato su gerarchia

Questo tipo di breadcrumb si basa sulla gerarchia delle categorie impostata sul sito. Le catene presentate indicano all’utente dove si trovano all’interno della struttura. In questo caso, ogni collegamento di testo è destinato a una pagina superiore di un livello rispetto al precedente.

Esempio: `Men > Tops > Hoodies & Sweatshirts`

Il vantaggio di questo tipo è che gli utenti possono vedere facilmente a quale livello di categoria appartengono e accedere facilmente alla navigazione tra le pagine del catalogo.

### Breadcrumb basate sulla cronologia

La navigazione basata su cronologia o percorso è simile al pulsante Indietro in un browser. Questo tipo di navigazione consente agli utenti di tornare rapidamente alle pagine precedenti visitate senza apportare modifiche.

Il vantaggio di questo tipo è che è più utile quando i clienti desiderano tornare a una pagina precedente dopo aver selezionato più filtri in una pagina categoria.

Esempio: `Home > What's New > Gear > Bags`

### Breadcrumb basato su attributi

Questo tipo di breadcrumb visualizza gli attributi selezionati nella pagina categoria. La differenza principale rispetto agli altri tipi consiste nel fatto che le breadcrumb basate su attributi rappresentano i filtri e le opzioni selezionati dal cliente nel livello di navigazione per alcuni prodotti (ad esempio prezzo, qualità e colore).

Esempio: `Home > Suits > All Suits > Refined by > Slim Fit`

## Aggiungere/rimuovere le breadcrumb dalle pagine CMS

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

   ![Mostra breadcrumb per pagine CMS](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Espandi _[!UICONTROL Default Pages]_sezione.

1. Deseleziona il **[!UICONTROL Use system value]** casella di controllo.

1. Imposta **[!UICONTROL Show Breadcrumbs for CMS Pages]** a `No` o `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

>[!NOTE]
>
>La categoria principale non viene visualizzata nella traccia Breadcrumb, nella pagina della categoria secondaria, quando `Browsing Category`= `Deny` [autorizzazione categoria](category-permissions.md) impostazioni.
