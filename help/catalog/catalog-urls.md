---
title: URL di cataloghi e prodotti
description: Scopri i tipi di formato URL per i prodotti del catalogo e come configurarli.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 11d78b7d7b548c373cfe0ec398814994c3e99e7a
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# URL di cataloghi e prodotti

Gli URL assegnati ai prodotti e alle categorie svolgono un ruolo importante nel determinare il livello di indicizzazione del sito da parte dei motori di ricerca. Prima di iniziare a creare il catalogo, considera le opzioni disponibili. Per visualizzare il formato URL corrente, passa alla vetrina e passa a qualsiasi prodotto del catalogo. Il formato dell’URL dipende dalle impostazioni di configurazione e dal metodo correnti utilizzati per trovare la pagina.

## Formati URL

### URL dinamico

Viene creato un URL dinamico _al volo_ e potrebbero includere una stringa di query con variabili per l’ID prodotto, l’ordinamento e la pagina in cui è stata effettuata la richiesta. Quando un cliente cerca un prodotto nel tuo negozio, l’URL risultante potrebbe essere simile al seguente:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### URL statico

Un URL statico è un indirizzo fisso per una pagina specifica. Un URL statico può essere visualizzato in un formato compatibile con i motori di ricerca o in un formato che fa riferimento a prodotti e categorie per ID. Questi URL includono parole che gli utenti potrebbero utilizzare per cercare un prodotto e richiedono l’attivazione delle riscritture del server web. I file con URL statici vengono comunemente utilizzati per pagine di prodotti e categorie, pagine di contenuti e [risorse tema](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## Componenti URL

### Chiave URL

Il codice URL è la parte di un URL statico che descrive il prodotto o la categoria. Quando crei un prodotto o una categoria, viene generato automaticamente un codice URL iniziale, in base al nome. Per modificare la chiave URL, vedi [Ottimizzazione motore di ricerca](product-search-engine-optimization.md) sezione delle informazioni sul prodotto.

>[!NOTE]
>
>Per impostazione predefinita, i caratteri speciali accentati vengono sostituiti automaticamente dalle normali versioni non accentate nella chiave URL. Ad esempio: `ñ` viene sostituito automaticamente da `n`. Questo comportamento può essere disattivato impostando _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_opzione di configurazione per `No`. Consulta [Configurare gli URL del catalogo](#configure-catalog-urls).

La chiave URL deve essere costituita da caratteri minuscoli con trattini non finali tra questi caratteri per separare le parole. I trattini non sono consentiti all’inizio o alla fine della chiave URL. Una chiave URL ben progettata e &quot;compatibile con i motori di ricerca&quot; potrebbe includere il nome del prodotto e le parole chiave per migliorarne l’indicizzazione da parte dei motori di ricerca. La chiave URL può essere configurata per creare un reindirizzamento automatico se cambia la chiave URL.

>[!NOTE]
>
>Per estendere le personalizzazioni degli URL, ad esempio gli URL localizzati, consulta [Riscritture URL](../merchandising-promotions/url-rewrite.md) per ulteriori informazioni.

### Suffisso HTML

Il catalogo può essere configurato in modo da includere o escludere il suffisso come parte degli URL di categorie e prodotti. Ci sono vari motivi per cui le persone possono scegliere di utilizzare o omettere il suffisso. Alcuni ritengono che il suffisso non abbia più uno scopo utile e che le pagine senza suffisso siano indicizzate in modo più efficace dai motori di ricerca. Tuttavia, la tua azienda potrebbe avere un formato standardizzato per gli URL che richiede un suffisso.

Poiché il suffisso è controllato dalla configurazione di sistema, non è mai consigliabile digitarlo direttamente nella chiave URL di una categoria o di un prodotto. In questo modo si otterrà un doppio suffisso alla fine dell’URL. Che tu decida di utilizzare o meno il suffisso, cerca di essere coerente e di utilizzare la stessa impostazione per tutte le pagine di prodotti e categorie. Di seguito sono riportati alcuni esempi di URL con e senza suffisso.

#### URL con suffisso HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL senza suffisso HTML

- `http://mystore.com/helena-hooded-fleece`

### Percorso categoria

Puoi configurare l’URL in modo da includere o escludere il percorso della categoria. Per impostazione predefinita, il percorso della categoria è incluso in tutte le pagine relative a categorie e prodotti. Gli esempi seguenti mostrano lo stesso URL di prodotto con e senza il percorso della categoria.

#### URL con percorso categoria

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL senza percorso categoria

- `http://mystore.com/helena-hooded-fleece.html`

Per evitare che i motori di ricerca indicizzino più URL che conducono allo stesso contenuto, puoi escludere il percorso della categoria dall’URL. Un altro metodo consiste nell’utilizzare un tag meta canonico per comunicare ai motori di ricerca gli URL da indicizzare e quelli da ignorare. Per impostazione predefinita, Commerce non include il percorso della categoria negli URL del prodotto.

## Configurare gli URL del catalogo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimizations]** e impostare le opzioni:

   - Imposta **[!UICONTROL Product URL Suffix]** a `html` o `htm`. Immettere il suffisso senza un punto, in quanto viene applicato automaticamente.

   - Imposta **[!UICONTROL Category URL Suffix]** a `html` o `htm`. Immettere il suffisso senza un punto, in quanto viene applicato automaticamente.

   - Imposta **[!UICONTROL Use Categories Path for Product URLs]** secondo le tue preferenze.

   ![Ottimizzazione motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Ottimizzazione motore di ricerca](../configuration-reference/catalog/catalog.md#search-engine-optimization) nel _Riferimento configurazione_.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiorna la cache non valida.

   ![Aggiorna cache](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Per ulteriori informazioni su queste opzioni, vedi [Aggiorna cache](../systems/cache-management.md#refresh-specific-caches).

## Configurare il formato URL del catalogo multimediale

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Url Options]** e impostare le opzioni:

![Web > Opzioni generali](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Globale | Se sono abilitate le riscritture del server web, l’abilitazione di questa impostazione inserisce nell’URL il codice store della vista corrente. Opzioni: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Globale | (Per le impostazioni per un singolo archivio) Se sul sito è presente un collegamento interrotto, il traffico viene reindirizzato all’URL di base anziché a una pagina con il messaggio &quot;404 Page Not Found&quot; (Pagina 404 non trovata). Opzioni: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Importante!_**Non utilizzare il reindirizzamento automatico all&#39;URL di base per le impostazioni in più store. |
| [!UICONTROL Catalog media URL format] | Globale | Definisce il formato URL assegnato a prodotti e categorie. Opzioni: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definisce il nome del file convertito come valore hash univoco.<br />**[!UICONTROL Image optimization based on query parameters]** - Definisce [ottimizzazione immagine](../content-design/media-gallery-image-optimization.md) processo che dipende dai parametri di query. |

{style="table-layout:auto"}
