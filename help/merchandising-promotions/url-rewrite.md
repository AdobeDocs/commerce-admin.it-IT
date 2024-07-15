---
title: Riscritture URL
description: Scopri come riscrivere gli URL e come utilizzare lo strumento di riscrittura URL di Commerce per modificare gli URL associati a una pagina di prodotto, categoria o CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# Riscritture URL

Lo strumento di riscrittura URL consente di modificare qualsiasi URL associato a un prodotto, una categoria o una pagina CMS. Quando la riscrittura diventa effettiva, tutti i collegamenti che puntano all’URL precedente vengono reindirizzati al nuovo indirizzo.

>[!NOTE]
>
>Per aggiornare le riscritture URL per più o tutti i prodotti contemporaneamente, fare riferimento a [Più riscritture URL](url-rewrite-product.md#multiple-url-rewrites).

I termini _rewrite_ e _redirect_ vengono spesso utilizzati in modo intercambiabile, ma fanno riferimento a processi leggermente diversi. La riscrittura di un URL cambia il modo in cui un URL viene visualizzato nel browser. Un reindirizzamento URL aggiorna l’URL memorizzato sul server. Un reindirizzamento URL può essere temporaneo o permanente. Il tuo store utilizza i reindirizzamenti e le riscritture URL per facilitare la modifica del codice URL di un prodotto, di una categoria o di una pagina e per mantenere i collegamenti esistenti.

Per impostazione predefinita, [i reindirizzamenti URL automatici](url-redirect-product-automatic.md) sono abilitati per l&#39;archivio e la casella di controllo **Crea reindirizzamento permanente per il vecchio URL** è selezionata nel campo chiave URL di ciascun prodotto.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Ottimizzazione motore di ricerca - crea reindirizzamento URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## URL canonici

Ai fini SEO, è consigliabile che ogni pagina web abbia un solo URL distinto.

Se disponi di una singola pagina accessibile da più URL o da pagine diverse con contenuto simile, Google le considera come versioni duplicate della stessa pagina. Google sceglie un URL come versione canonica e esegue la ricerca per indicizzazione, mentre tutti gli altri URL vengono considerati URL duplicati e vengono sottoposti a ricerca per indicizzazione con minore frequenza.

Se non dici esplicitamente a Google quale URL è canonico, effettua la scelta o potrebbe considerarli entrambi di peso uguale. Ciò potrebbe causare un comportamento indesiderato, con il rischio di un budget di ricerca per indicizzazione inefficace e di collegamenti in background distribuiti ridotti.

A seconda di come configuri il sito web, nell’indice possono essere presenti più versioni del sito, tra cui:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Per specificare una pagina canonica, vedere [Documentazione di Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## Configurare le riscritture URL

L’abilitazione di Apache Rewrite per il server web fa parte della configurazione iniziale di Commerce. Commerce utilizza di solito le riscritture URL per rimuovere il nome file `index.php` che normalmente viene visualizzato nell&#39;URL subito dopo la cartella principale. Quando le riscritture del server Web sono abilitate, il sistema riscrive ogni URL per omettere `index.php`. La riscrittura rimuove le parole che non trasmettono nulla di valore ai motori di ricerca o ai clienti e non ha alcun impatto sulle prestazioni o sulla classificazione del sito.

URL senza riscrittura server Web

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL con riscrittura server Web

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in cui è espanso **[!UICONTROL General]**, scegli **[!UICONTROL Web]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

   ![Configurazione generale - ottimizzazione motore di ricerca Web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Use Web Server Rewrites]** sulla tua preferenza.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Crea riscritture URL

Puoi utilizzare lo strumento di riscrittura URL per creare riscritture di prodotti e categorie e riscritture personalizzate per qualsiasi pagina del Negozio. Quando la riscrittura entra in vigore, tutti i collegamenti esistenti che puntano all’URL precedente vengono reindirizzati direttamente al nuovo indirizzo.

Le riscritture URL possono essere utilizzate per aggiungere parole chiave di alto valore per migliorare il modo in cui il prodotto viene indicizzato dai motori di ricerca. È inoltre possibile utilizzare le riscritture per creare URL aggiuntivi per una modifica stagionale temporanea o permanente. Le riscritture possono essere create per qualsiasi percorso valido, comprese le pagine di contenuto CMS. Internamente, il sistema fa sempre riferimento a prodotti e categorie in base al loro ID. Indipendentemente dalla frequenza con cui l’URL cambia, l’ID rimane lo stesso. Di seguito sono riportati alcuni modi in cui puoi utilizzare una riscrittura URL:

URL di sistema

    http://www.example.com/catalog/category/id/6

URL originale

    http://www.example.com/peripherals/keyboard.html

URL prodotto reindirizzato

    http://www.example.com/ergonomic-keyboard.html

URL categoria aggiuntivi

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL riscrive griglia](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce offre i seguenti tipi di riscrittura URL:

* [Riscritture prodotto](url-rewrite-product.md)
* [Riscritture categoria](url-rewrite-category.md)
* [Riscritture pagina CMS](url-rewrite-cms-page.md)
* [Riscritture personalizzate](url-rewrite-custom.md)

## URL riscrive demo

Guarda questo video per scoprire come gestire le riscritture URL:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
