---
title: Metadati
description: Scopri come immettere metadati ricchi di parole chiave per migliorare il modo in cui i motori di ricerca indicizzano il sito Commerce.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Metadati

Il tuo archivio è caricato di luoghi in cui puoi immettere metadati ricchi di parole chiave per migliorare il modo in cui i motori di ricerca indicizzano il sito. Durante la configurazione del negozio, è possibile immettere metadati preliminari, con l&#39;intenzione di completarli in un secondo momento. Nel tempo, puoi perfezionare i metadati per adattarli ai modelli di acquisto e alle preferenze dei clienti.

![Impostazioni del prodotto - Ottimizzazione del motore di ricerca](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Meta title

Il metatitolo viene visualizzato nella barra del titolo e nella scheda del browser e nell’elenco dei risultati della ricerca. Il metatitolo deve essere univoco per la pagina e contenere meno di 70 caratteri.

![Esempio di vetrina - meta title](./assets/storefront-home-page-meta-title.png){width="600"}

## Parole chiave meta

Anche se alcuni motori di ricerca ignorano le parole chiave meta, altri continuano a utilizzarle. La best practice corrente consiste nell’incorporare parole chiave di alto valore nel metatitolo e nella descrizione.

![Ricerca nel browser web - parole chiave meta](./assets/storefront-meta-description.png){width="500"}

## Meta descrizione

Le metadescrizioni forniscono una breve panoramica della pagina per l’elenco dei risultati di ricerca. Idealmente, una metadescrizione dovrebbe avere una lunghezza compresa tra 150 e 160 caratteri, anche se il campo accetta fino a 255 caratteri.

## Frammenti avanzati

I frammenti avanzati forniscono informazioni dettagliate per l&#39;elenco dei risultati di ricerca e altre applicazioni. Per impostazione predefinita, il markup dei dati strutturati basato su [schema.org][1] standard viene aggiunto al modello di prodotto del negozio. Di conseguenza, sono disponibili ulteriori informazioni che i motori di ricerca possono includere come _snippet avanzati_ negli elenchi di prodotti.

## Tag meta canonico

Alcuni motori di ricerca penalizzano i siti web che hanno più URL che puntano allo stesso contenuto. Il metatag canonico indica ai motori di ricerca la pagina da indicizzare quando più URL hanno contenuto identico o simile. L’utilizzo del tag meta canonico può migliorare la classificazione del sito e le visualizzazioni di pagina aggregate. Il tag meta canonico viene inserito nel `<head>` blocco di una pagina di prodotto o categoria. Fornisce un collegamento all’URL preferito, quindi i motori di ricerca gli attribuiscono un peso maggiore.

### Esempio 1: il percorso della categoria crea URL duplicati

Ad esempio, se il catalogo è configurato per includere il percorso della categoria negli URL del prodotto, lo store genera più URL che puntano alla stessa pagina del prodotto.

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### Esempio 2: URL completo pagina categoria

Quando i metatag canonici per le categorie sono abilitati, la pagina delle categorie del tuo store include un URL canonico per l’URL completo della categoria:

    http://mystore.com/gear/bags/

### Esempio 3: URL completo della pagina di prodotto

Quando i metatag canonici per i prodotti sono abilitati, la pagina del prodotto include un URL canonico per nome di dominio/product-url-key, perché i codici URL del prodotto sono globalmente univoci.

    http://mystore.com/driven-backpack.html

Se includi anche il percorso della categoria negli URL del prodotto, l’URL canonico rimane nome di dominio/codice Product-url-key. Tuttavia, è possibile accedere al prodotto anche utilizzando il relativo URL completo, che include la categoria. Ad esempio, se il codice Product URL è `driven-backpack` ed è assegnato alla categoria Gear > Bags, è possibile accedere al prodotto utilizzando uno dei due URL.

Puoi evitare di essere penalizzato dai motori di ricerca omettendo la categoria dall’URL o utilizzando il metatag canonico per indirizzare i motori di ricerca all’indicizzazione per prodotto o categoria. Come best practice, si consiglia di abilitare i metatag canonici sia per le categorie che per i prodotti.

### Abilita il tag meta canonico

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **Ottimizzazione motore di ricerca** sezione.

   Per modificare i valori dei campi, è necessario prima cancellare **Usa valore di sistema** dopo ogni campo.

   ![Configurazione del catalogo - Ottimizzazione del motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Se si desidera che i motori di ricerca indicizzino solo le pagine delle categorie utilizzando il percorso completo delle categorie, eseguire le operazioni seguenti:

   - Imposta **Usa metatag collegamento canonico per categorie** a `Yes`.

   - Imposta **Utilizza il tag meta di collegamento canonico per i prodotti** a `No`.

1. Se si desidera che i motori di ricerca indicizzino le pagine di prodotti utilizzando solo il formato nome di dominio/prodotto-url-chiave, eseguire le operazioni seguenti:

   - Imposta **Utilizza il tag meta di collegamento canonico per i prodotti** a `Yes`.

   - Imposta **Usa metatag collegamento canonico per categorie** a `No`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Demo sui metadati

Guarda questo video per scoprire come gestire i metadati SEO (Search Engine Optimization):

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12)

[1]: https://schema.org/
