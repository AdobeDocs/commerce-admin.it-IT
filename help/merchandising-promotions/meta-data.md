---
title: Dati Meta
description: Scopri come immettere metadati ricchi di parole chiave per migliorare il modo in cui i motori di ricerca indicizzano il sito Commerce.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/hl0i6mlFJY5r5bIWNG6gQMGlWQMmaWOWBnt8pCpKT50
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 747
ht-degree: 0%

---

# Dati Meta

>[!TIP]
>
>Per Adobe Commerce as a Cloud Service, consulta le [linee guida sui metadati](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/metadata/?lang=it) nella documentazione di Commerce Storefront

Il tuo archivio è caricato di luoghi in cui puoi immettere metadati ricchi di parole chiave per migliorare il modo in cui i motori di ricerca indicizzano il sito. Durante la configurazione del negozio, è possibile immettere metadati preliminari, con l&#39;intenzione di completarli in un secondo momento. Nel tempo, puoi perfezionare i metadati per adattarli ai modelli di acquisto e alle preferenze dei clienti.

![Impostazioni prodotto - Ottimizzazione motore di ricerca](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Titolo Meta

Il metatitolo viene visualizzato nella barra del titolo e nella scheda del browser e nell’elenco dei risultati della ricerca. Il metatitolo deve essere univoco per la pagina e contenere meno di 70 caratteri.

![Esempio di vetrina - titolo meta](./assets/storefront-home-page-meta-title.png){width="600"}

## Parole chiave di Meta

Anche se alcuni motori di ricerca ignorano le parole chiave meta, altri continuano a utilizzarle. La best practice corrente consiste nell’incorporare parole chiave di alto valore nel metatitolo e nella descrizione.

![Ricerca nel browser Web - Parole chiave meta](./assets/storefront-meta-description.png){width="500"}

## Descrizione di Meta

Le descrizioni di Meta forniscono una breve panoramica della pagina per l’elenco dei risultati della ricerca. Idealmente, una metadescrizione dovrebbe avere una lunghezza compresa tra 150 e 160 caratteri, anche se il campo accetta fino a 255 caratteri.

## Frammenti avanzati

I frammenti avanzati forniscono informazioni dettagliate per l&#39;elenco dei risultati di ricerca e altre applicazioni. Per impostazione predefinita, al modello di prodotto dell&#39;archivio viene aggiunto il markup di dati strutturati basato sullo standard [schema.org](https://schema.org/). Di conseguenza, sono disponibili ulteriori informazioni per i motori di ricerca da includere come _frammenti avanzati_ negli elenchi di prodotti.

## Tag meta canonico

Alcuni motori di ricerca penalizzano i siti web che hanno più URL che puntano allo stesso contenuto. Il metatag canonico indica ai motori di ricerca la pagina da indicizzare quando più URL hanno contenuto identico o simile. L’utilizzo del tag meta canonico può migliorare la classificazione del sito e le visualizzazioni di pagina aggregate. Il metatag canonico si trova nel blocco `<head>` di una pagina di prodotto o categoria. Fornisce un collegamento all’URL preferito, quindi i motori di ricerca gli attribuiscono un peso maggiore.

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

Se includi anche il percorso della categoria negli URL del prodotto, l’URL canonico rimane nome di dominio/codice Product-url-key. Tuttavia, è possibile accedere al prodotto anche utilizzando il relativo URL completo, che include la categoria. Ad esempio, se il codice URL del prodotto è `driven-backpack` e viene assegnato alla categoria Ingranaggio > Bagagli, è possibile accedere al prodotto utilizzando uno di questi URL.

Puoi evitare di essere penalizzato dai motori di ricerca omettendo la categoria dall’URL o utilizzando il metatag canonico per indirizzare i motori di ricerca all’indicizzazione per prodotto o categoria. Come best practice, si consiglia di abilitare i metatag canonici sia per le categorie che per i prodotti.

### Abilita il tag meta canonico

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **Ottimizzazione motore di ricerca**.

   Per modificare i valori dei campi, è necessario deselezionare la casella di controllo **Usa valore di sistema** dopo ogni campo.

   ![Configurazione del catalogo - ottimizzazione motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Se si desidera che i motori di ricerca indicizzino solo le pagine delle categorie utilizzando il percorso completo delle categorie, eseguire le operazioni seguenti:

   - Imposta **Usa tag Meta collegamento canonico per le categorie** su `Yes`.

   - Imposta **Usa tag Meta collegamento canonico per i prodotti** su `No`.

1. Se si desidera che i motori di ricerca indicizzino le pagine di prodotti utilizzando solo il formato nome di dominio/prodotto-url-chiave, eseguire le operazioni seguenti:

   - Imposta **Usa tag Meta collegamento canonico per i prodotti** su `Yes`.

   - Imposta **Usa tag Meta collegamento canonico per le categorie** su `No`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Demo sui dati di Meta

Guarda questo video per scoprire come gestire i metadati SEO (Search Engine Optimization):

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12&learn=on)
