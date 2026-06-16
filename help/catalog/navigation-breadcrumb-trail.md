---
title: Tracce breadcrumb
description: Scopri i diversi modelli di percorso delle breadcrumb e come configurarli per visualizzarli nelle pagine di contenuto e catalogo.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
TQID: https://experienceleague.adobe.com/v1hA4y0MmxxTtH3WbspqosZM1JMk4PMyhK1xeLxALOE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# Tracce breadcrumb

Un _percorso breadcrumb_ è un insieme di collegamenti che mostrano al cliente dove si trova in relazione ad altre pagine dell&#39;archivio. Può fare clic su qualsiasi collegamento nella traccia delle breadcrumb per tornare alla pagina precedente.

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

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

   ![Mostra breadcrumb per pagine CMS](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Espandere la sezione _[!UICONTROL Default Pages]_.

1. Deselezionare la casella di controllo **[!UICONTROL Use system value]**.

1. Imposta **[!UICONTROL Show Breadcrumbs for CMS Pages]** su `No` o `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

>[!NOTE]
>
>La categoria padre non viene visualizzata nella traccia delle breadcrumb, nella pagina della categoria figlio, quando dispone delle impostazioni `Browsing Category`= `Deny` [autorizzazione categoria](category-permissions.md).
