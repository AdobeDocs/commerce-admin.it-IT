---
title: Pagine
description: Scopri i dettagli sulle pagine di contenuti di base incluse nel [!DNL Commerce] nell'archivio demo e la modifica della configurazione Pagine predefinite.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# Pagine

Il contenuto può essere visualizzato in termini di durata, come qualsiasi prodotto in un negozio. Lo sapevi che la durata utile dei contenuti sui social media è inferiore alle 24 ore? La potenziale durata dei contenuti creati può essere utile per decidere dove investire le risorse.

I contenuti con una lunga durata di conservazione sono a volte indicati come _contenuto sempreverde_. Esempi di contenuti fissi sono le storie di successo dei clienti, _come_ e le domande frequenti (FAQ). Al contrario, i contenuti che per loro natura sono deperibili includono eventi, notizie del settore e comunicati stampa.

![La pagina Informazioni su di noi inclusa nell’archivio Luma di esempio ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Pagine contenuto core

Il [!DNL Commerce] nell’archivio demo sono presenti esempi di pagine di contenuti di base utili per iniziare. Puoi modificare tutte queste pagine in base alle tue esigenze. Guarda le pagine seguenti del tuo negozio e assicurati che il contenuto trasmetta il messaggio, la voce e il marchio.

### Home

Demo [Home](../getting-started/storefront.md#home-page) La pagina include un banner, un carosello di immagini, diversi blocchi statici con collegamenti e un elenco di nuovi prodotti.

### Informativa sulla privacy

Il negozio [Informativa sulla privacy](../getting-started/privacy-policy.md) La pagina deve essere aggiornata con le tue informazioni. Come best practice, l’informativa sulla privacy deve spiegare ai clienti il tipo di informazioni raccolte dalla tua azienda e come vengono utilizzate.

### 404 Non trovato

La pagina 404 Pagina non trovata prende il nome dal codice di risposta restituito quando non è possibile trovare una pagina. I reindirizzamenti URL riducono il numero di volte in cui viene visualizzata la pagina. Tuttavia, per i momenti in cui è necessario, si potrebbe anche sfruttare l&#39;opportunità di offrire alcuni collegamenti a prodotti che il cliente potrebbe trovare interessante.

### Accesso negato

{{b2b-feature}}

Il [Accesso negato](../b2b/account-company-roles-permissions.md) viene visualizzata quando le autorizzazioni assegnate a un utente dell’azienda impediscono l’accesso alla pagina.

### Abilita cookie

Il [Abilita cookie](../getting-started/compliance-cookie-law.md) viene visualizzata quando i visitatori del sito non hanno i cookie abilitati nei loro browser. La pagina fornisce istruzioni dettagliate e illustrate per abilitare i cookie per i browser più diffusi.

### Servizio non disponibile

Il [Servizio 503 non disponibile](../configuration-reference/general/general.md) La pagina viene denominata in base al codice di risposta restituito quando il server non è disponibile.

### Chi siamo

La pagina Informazioni su di noi è collegata dal piè di pagina del tuo negozio. Puoi includere immagini, video, collegamenti a comunicati stampa e annunci. La pagina di esempio ha un&#39;immagine a destra e una decorativa per indicare la fine della pagina.

### Servizio clienti

La pagina Servizio clienti è un altro nodo nella gerarchia delle pagine. Il contenuto delle due intestazioni della pagina diventa visibile solo quando il cliente fa clic sull’intestazione.

![Pagina Assistenza clienti nella vetrina](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Configurare le pagine predefinite

Il _Pagine predefinite_ determina la pagina di destinazione associata al [URL di base](../stores-purchase/store-urls.md) e la home page corrispondente. Inoltre, determina quale pagina viene visualizzata quando un _Pagina non trovata_ e se si verifica un errore [percorso breadcrumb](../catalog/navigation-breadcrumb-trail.md) viene visualizzato nella parte superiore di ogni pagina.

1. Il giorno _Amministratore_ barra laterale, vai a  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Default Pages]** sezione.

   ![Pagine predefinite](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Visualizzazione store | Indica la pagina di destinazione associata all’URL di base. Per impostazione predefinita, questo campo è impostato su `cms` per indicare una pagina da [!DNL Commerce] sistema di gestione dei contenuti. Puoi anche utilizzare un tipo diverso di pagina di destinazione, ad esempio un blog. Ad esempio, se un blog è installato sul server in `magento/blog`, è possibile immettere il nome della cartella `blog` come percorso relativo per la selezione delle pagine. |
   | [!UICONTROL CMS Home Page] | Visualizzazione store | Per scegliere la home page del negozio, seleziona semplicemente la pagina CMS dall’elenco. Per impostazione predefinita, la home page del CMS elenca l’intera selezione di pagine CMS disponibili per lo store. |
   | [!UICONTROL Default No-route URL] | Visualizzazione store | Contiene l&#39;URL della pagina predefinita che si desidera visualizzare quando `404 Page not Found` si verifica un errore. Il valore predefinito è `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Visualizzazione store | Identifica una pagina CMS specifica che si desidera visualizzare quando si verifica un errore Pagina 404 non trovata. La pagina predefinita è `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Visualizzazione store | Identifica una pagina CMS specifica che viene visualizzata quando i cookie non sono abilitati per il browser. La pagina spiega perché vengono utilizzati i cookie e come abilitarli per ogni browser. La pagina predefinita è `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Visualizzazione store | Determina se un percorso di breadcrumb viene visualizzato su tutte le pagine CMS del catalogo. Opzioni: `Yes` / `No` |

   {style="table-layout:auto"}

1. Per **[!UICONTROL Default Web URL]**, immetti il percorso relativo della cartella in [!DNL Commerce] installazione che contiene la pagina di destinazione.

   L&#39;impostazione predefinita `cms`, indica una pagina da [!DNL Commerce] sistema di gestione dei contenuti.

   >[!NOTE]
   >
   >Per una visualizzazione specifica dello store, cancella **[!UICONTROL Use Default]** casella di controllo accanto a _[!UICONTROL Default Web URL]_e qualsiasi altra impostazione predefinita da modificare.

1. Imposta **[!UICONTROL CMS Home Page]** nella pagina CMS da utilizzare come home page. Altre pagine create possono essere utilizzate come home page, ad esempio:

   - Benvenuto nel negozio online esclusivo
   - Punti premio
   - Chi siamo
   - Servizio clienti
   - Abilita cookie
   - Informativa sulla privacy
   - Società: accesso negato

1. Per **[!UICONTROL Default No-route URL]**, immetti il percorso relativo della cartella in [!DNL Commerce] installazione in cui la pagina viene reindirizzata quando un _Pagina 404 non trovata_ si verifica un errore.

   Il valore predefinito è `cms/index/noRoute`.

1. Imposta **[!UICONTROL CMS No Route Page]** alla pagina CMS visualizzata quando un _Pagina 404 non trovata_ si verifica un errore.

1. Imposta **[!UICONTROL CMS No Cookies Page]** alla pagina CMS visualizzata quando i cookie sono disabilitati nel browser. La pagina spiega perché vengono utilizzati i cookie e come abilitarli per ogni browser. La pagina predefinita è `Enable Cookies`.

1. Se desideri che una traccia delle breadcrumb venga visualizzata nella parte superiore di tutte le pagine CMS, imposta **[!UICONTROL Show Breadcrumbs for CMS Pages]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
