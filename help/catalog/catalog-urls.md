---
title: URL di cataloghi e prodotti
description: Scopri i tipi di formato URL per i prodotti del catalogo e come configurarli.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# URL di cataloghi e prodotti

Gli URL assegnati ai prodotti e alle categorie svolgono un ruolo importante nel determinare il livello di indicizzazione del sito da parte dei motori di ricerca. Prima di iniziare a creare il catalogo, considera le opzioni disponibili. Per visualizzare il formato URL corrente, passa alla vetrina e passa a qualsiasi prodotto del catalogo. Il formato dell’URL dipende dalle impostazioni di configurazione e dal metodo correnti utilizzati per trovare la pagina.

## Formati URL

### URL dinamico

Un URL dinamico viene creato _al volo_ e potrebbe includere una stringa di query con variabili per l&#39;ID prodotto, l&#39;ordinamento e la pagina in cui è stata effettuata la richiesta. Quando un cliente cerca un prodotto nel tuo negozio, l’URL risultante potrebbe essere simile al seguente:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### URL statico

Un URL statico è un indirizzo fisso per una pagina specifica. Un URL statico può essere visualizzato in un formato compatibile con i motori di ricerca o in un formato che fa riferimento a prodotti e categorie per ID. Questi URL includono parole che gli utenti potrebbero utilizzare per cercare un prodotto e richiedono l’attivazione delle riscritture del server web. I file con URL statici vengono comunemente utilizzati per pagine di prodotti e categorie, pagine di contenuti e [risorse tema](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## Componenti URL

### Chiave URL

Il codice URL è la parte di un URL statico che descrive il prodotto o la categoria. Quando crei un prodotto o una categoria, viene generato automaticamente un codice URL iniziale, in base al nome. Per modificare la chiave URL, vedere la sezione [Ottimizzazione motore di ricerca](product-search-engine-optimization.md) delle informazioni sul prodotto.

>[!NOTE]
>
>Per impostazione predefinita, i caratteri speciali accentati vengono sostituiti automaticamente dalle normali versioni non accentate nella chiave URL. Ad esempio, `ñ` viene sostituito automaticamente da `n`. È possibile disabilitare questo comportamento impostando l&#39;opzione di configurazione _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;su `No`. Vedi [Configurare gli URL del catalogo](#configure-catalog-urls).

La chiave URL deve essere costituita da caratteri minuscoli con trattini non finali tra questi caratteri per separare le parole. I trattini non sono consentiti all’inizio o alla fine della chiave URL. Una chiave URL ben progettata e &quot;compatibile con i motori di ricerca&quot; potrebbe includere il nome del prodotto e le parole chiave per migliorarne l’indicizzazione da parte dei motori di ricerca. La chiave URL può essere configurata per creare un reindirizzamento automatico se cambia la chiave URL.

>[!NOTE]
>
>Per estendere le personalizzazioni degli URL, ad esempio gli URL localizzati, vedere [Riscritture URL](../merchandising-promotions/url-rewrite.md) per ulteriori informazioni.

### Suffisso HTML

Il catalogo può essere configurato in modo da includere o escludere il suffisso come parte degli URL di categorie e prodotti. Ci sono vari motivi per cui le persone possono scegliere di utilizzare o omettere il suffisso. Alcuni ritengono che il suffisso non abbia più uno scopo utile e che le pagine senza suffisso siano indicizzate in modo più efficace dai motori di ricerca. Tuttavia, la tua azienda potrebbe avere un formato standardizzato per gli URL che richiede un suffisso.

Poiché il suffisso è controllato dalla configurazione di sistema, non è mai consigliabile digitarlo direttamente nella chiave URL di una categoria o di un prodotto. In questo modo si otterrà un doppio suffisso alla fine dell’URL. Che tu decida di utilizzare o meno il suffisso, cerca di essere coerente e di utilizzare la stessa impostazione per tutte le pagine di prodotti e categorie. Di seguito sono riportati alcuni esempi di URL con e senza suffisso.

#### URL con suffisso HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL senza suffisso HTML

- `http://mystore.com/helena-hooded-fleece`

### Percorso categoria

Puoi configurare gli URL del prodotto in modo da includere o escludere il percorso della categoria in base alle tue preferenze. Per impostazione predefinita, il percorso della categoria non è incluso negli URL del prodotto. Tuttavia, le categorie nidificate visualizzeranno sempre l’intero percorso delle categorie nei loro URL nella vetrina, garantendo chiarezza e coerenza nella navigazione delle categorie. Gli esempi seguenti mostrano lo stesso URL di prodotto con e senza il percorso della categoria.

#### URL prodotto con percorso categoria

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL prodotto senza percorso categoria

- `http://mystore.com/helena-hooded-fleece.html`

Per evitare che i motori di ricerca indicizzino più URL che conducono allo stesso contenuto, puoi escludere il percorso della categoria dall’URL. Un altro metodo consiste nell’utilizzare un tag meta canonico per comunicare ai motori di ricerca gli URL da indicizzare e quelli da ignorare. Per impostazione predefinita, Commerce non include il percorso della categoria negli URL del prodotto.

## Configurare gli URL del catalogo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimizations]** e impostare le opzioni:

   - Imposta **[!UICONTROL Product URL Suffix]** su `html` o `htm`. Immettere il suffisso senza un punto, in quanto viene applicato automaticamente.

   - Imposta **[!UICONTROL Category URL Suffix]** su `html` o `htm`. Immettere il suffisso senza un punto, in quanto viene applicato automaticamente.

   - Imposta **[!UICONTROL Use Categories Path for Product URLs]** sulla tua preferenza.

   ![Ottimizzazione motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Ottimizzazione motore di ricerca](../configuration-reference/catalog/catalog.md#search-engine-optimization) nella _Guida di riferimento configurazione_.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, fare clic sul collegamento **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiornare la cache non valida.

   ![Aggiorna cache](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Per ulteriori informazioni su queste opzioni, vedere [Aggiorna cache](../systems/cache-management.md#refresh-specific-caches).

## Configurare il formato URL del catalogo multimediale

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL Web]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Url Options]** e impostare le opzioni:

![Web > Opzioni generali](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Globale | Se sono abilitate le riscritture del server web, l’abilitazione di questa impostazione inserisce nell’URL il codice store della vista corrente. Opzioni: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Globale | (Per le impostazioni per un singolo archivio) Se sul sito è presente un collegamento interrotto, il traffico viene reindirizzato all’URL di base anziché a una pagina con il messaggio &quot;404 Page Not Found&quot; (Pagina 404 non trovata). Opzioni: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Importante!_**&#x200B;Non utilizzare il reindirizzamento automatico all&#39;URL di base per le impostazioni multi-store. |
| [!UICONTROL Catalog media URL format] | Globale | Definisce il formato URL assegnato a prodotti e categorie. Opzioni: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definisce il nome file convertito come valore hash univoco.<br />**[!UICONTROL Image optimization based on query parameters]** - Definisce il processo di [ottimizzazione immagine](../content-design/media-gallery-image-optimization.md) in base ai parametri di query. |

{style="table-layout:auto"}
