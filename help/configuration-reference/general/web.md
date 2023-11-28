---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL General] &gt; [!UICONTROL Web] pagina dell’amministratore di Commerce.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Opzioni generali](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Campo | Ambito | Descrizione |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Globale | Se sono abilitate le riscritture del server Web, inserisce nell&#39;URL il codice store della visualizzazione corrente. Opzioni: `Yes` / `No`. <br />Quando questo campo è impostato su `Yes`, è necessario includere i codici store negli URL del browser per garantire che le riscritture URL siano mappate correttamente e che tutte le pagine siano aperte correttamente. Questo evita _Pagina 404 non trovata_ errori. |
| [!UICONTROL Auto-redirect to Base URL] | Visualizzazione store | (Per le impostazioni per un singolo archivio) Se sul sito è presente un collegamento interrotto, reindirizza il traffico all’URL di base anziché a una pagina con il messaggio &quot;404 Page Not Found&quot; (Pagina 404 non trovata). Opzioni:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Importante:_**Non utilizzare il reindirizzamento automatico all&#39;URL di base per le impostazioni in più store. |
| [!UICONTROL Catalog media URL format] | Globale | Definisce il [Formato URL](../../catalog/catalog-urls.md) assegnati a prodotti e categorie. Opzioni: hash univoco per variante di immagine (modalità legacy) definisce il nome del file convertito come un valore hash univoco. L’ottimizzazione dell’immagine in base ai parametri di query definisce [ottimizzazione immagine](../../content-design/media-gallery-image-optimization.md) processo che dipende dai parametri di query. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Optimization]

![Web > Ottimizzazione motore di ricerca](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://docs.magento.com/user-guide/marketing/url-rewrite.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Visualizzazione store | I sistemi basati su PHP in genere includono un file denominato `index.php` nella cartella principale. Per impostazione predefinita, il nome del file viene visualizzato nell’URL subito dopo il nome della cartella principale. Quando è attivata, il sistema omette `index.php` dall’URL. Questa best practice sull’usabilità rende ogni URL più conciso e non ha alcun impatto sulle prestazioni o sulla classificazione del sito. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Base URLs]

![Web > URL di base](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Base URL] | Visualizzazione store | L’indirizzo completo della cartella principale di Commerce che non viene eseguita su un canale crittografato (SSL). L’URL deve terminare con una barra. |
| [!UICONTROL Base Link URL] | Visualizzazione store | Tag di markup utilizzato come segnaposto per l&#39;URL di base. |
| [!UICONTROL Base URL for Static View Files] | Visualizzazione store | Percorso che punta alla posizione dei file statici utilizzati dal tema, ad esempio css, font, immagini e JavaScript. Un segnaposto viene utilizzato per rappresentare l’URL di base. Se nell’installazione di Commerce sono presenti più siti con la stessa struttura di cartelle, puoi creare una cartella diversa per ciascun sito. Impostare l&#39;ambito di configurazione sul sito corretto prima di immettere l&#39;URL di base per i file di visualizzazione statica. Puoi anche specificare una cartella al di fuori dell’installazione di Commerce. |
| [!UICONTROL Base URL for User Media Files] | Visualizzazione store | Percorso che punta alla posizione delle immagini del catalogo e di altri file multimediali. Un segnaposto viene utilizzato per rappresentare l’URL di base. Se nell’installazione di Commerce sono presenti più siti con la stessa struttura di cartelle, puoi creare una cartella multimediale diversa per ciascuno di essi. In questo modo è possibile eseguire separatamente il backup e il rollback di ogni cartella multimediale. Puoi anche specificare una cartella di file multimediali al di fuori dell’installazione di Commerce. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Base URLs (Secure)]

![Web > URL di base (protetto)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Visualizzazione store | L’indirizzo completo della cartella principale di Commerce distribuita con il protocollo crittografato protetto (SSL/TLS). L’URL deve terminare con una barra. |
| [!UICONTROL Secure Base Link URL] | Visualizzazione store | Tag di markup utilizzato come segnaposto per l&#39;URL di base eseguito su un canale sicuro. |
| [!UICONTROL Secure Base URL for Static View Files] | Visualizzazione store | Tag di markup che punta alla posizione di file statici come CSS, font, immagini e JavaScript utilizzati dal tema. I file possono trovarsi su un canale non sicuro o protetto. Se nell’installazione di Commerce sono presenti più siti con la stessa struttura di cartelle, puoi creare una cartella diversa per ciascun sito. Impostare l&#39;ambito di configurazione sul sito corretto prima di immettere l&#39;URL di base per i file di visualizzazione statica. Puoi anche specificare una cartella al di fuori dell’installazione di Commerce. |
| [!UICONTROL Secure Base URL for User Media Files] | Visualizzazione store | Percorso che punta alla posizione delle immagini del catalogo e di altri file multimediali. I file possono trovarsi su un canale non sicuro o protetto. Un segnaposto viene utilizzato per rappresentare l’URL di base. Se nell’installazione di Commerce sono presenti più siti con la stessa struttura di cartelle, puoi creare una cartella multimediale diversa per ciascuno di essi. In questo modo è possibile eseguire separatamente il backup e il rollback di ogni cartella multimediale. Puoi anche specificare una cartella di file multimediali al di fuori dell’installazione di Commerce. |
| [!UICONTROL Use Secure URLs on Storefront] | Visualizzazione store | Se il dominio dispone di un certificato di sicurezza, puoi scegliere di eseguire la vetrina, con o senza crittografia SSL. Opzioni:<br />**`Yes`**- Gli URL dell’archivio iniziano con `https` per indicare che la pagina viene consegnata con un protocollo crittografato e sicuro.<br />**`No`** - Gli URL dell’archivio iniziano con `http` per indicare che la pagina viene consegnata senza un protocollo sicuro. |
| [!UICONTROL Use Secure URLs in Admin] | Globale | Se il dominio dispone di un certificato di sicurezza, puoi scegliere di eseguire l’amministrazione dello store, con o senza crittografia SSL. Opzioni: <br />**`Yes`**- Gli URL dell’amministratore iniziano con `https` per indicare che la pagina viene consegnata con un protocollo crittografato e sicuro.<br />**`No`** - Gli URL dell’amministratore iniziano con `http` per indicare che la pagina viene consegnata senza un protocollo sicuro.<br /> Quando gli URL protetti sono abilitati sia per l’archivio che per l’amministratore, vengono visualizzati due campi aggiuntivi per abilitare e configurare `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Visualizzazione store | Quando è attivata, [`HSTS`][1] fornisce una misura di sicurezza contro gli attacchi di tipo &quot;man in the middle&quot; e impedisce agli utenti di ignorare il messaggio &quot;invalid certificate&quot;. Opzioni: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Visualizzazione store | Se attivata, converte in non protetto (`HTTP`) richieste ricevute dal browser al protetto (`HTTPS`). Opzioni: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Globale | Specifica il `offloader_header` valore nella configurazione del server per identificare il protocollo tra il client e il load balancer. La maggior parte delle installazioni di Commerce utilizza il valore predefinito, `X-Forwarded-Proto` (XFP) per identificare il protocollo come `HTTP` o `HTTPS`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Pages]

![Web > Pagine predefinite](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://docs.magento.com/user-guide/cms/pages-default.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Visualizzazione store | Indica la pagina di destinazione associata all’URL di base. Per impostazione predefinita, questo valore è impostato su &quot;cms&quot; per indicare una pagina del sistema di gestione dei contenuti di Commerce (CMS). Puoi anche utilizzare un tipo diverso di pagina di destinazione, ad esempio un blog. Ad esempio, se un blog è installato sul server in `magento/blog`, è possibile immettere il nome della cartella &quot;blog&quot; come percorso relativo per la selezione delle pagine. |
| [!UICONTROL CMS Home Page] | Visualizzazione store | Per scegliere la home page del negozio, seleziona semplicemente la pagina CMS dall’elenco. Per impostazione predefinita, la home page del CMS elenca l’intera selezione di pagine CMS disponibili per lo store. |
| [!UICONTROL Default No-route URL] | Visualizzazione store | Contiene l&#39;URL della pagina predefinita che si desidera visualizzare quando `404 Page not Found` si verifica un errore. Il valore predefinito è `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Visualizzazione store | Identifica una pagina CMS specifica che si desidera visualizzare quando si verifica un errore Pagina 404 non trovata. La pagina predefinita è 404 Non trovato. |
| [!UICONTROL CMS No Cookies Page] | Visualizzazione store | Identifica una pagina CMS specifica che viene visualizzata quando i cookie non sono abilitati per il browser. La pagina spiega perché vengono utilizzati i cookie e come abilitarli per ogni browser. La pagina predefinita è Abilita cookie. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Visualizzazione store | Determina se un percorso di breadcrumb viene visualizzato su tutte le pagine CMS del catalogo. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Layouts]

![Layout predefiniti](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://docs.magento.com/user-guide/design/page-layout.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Globale | Determina la [layout](../../content-design/page-layout.md) utilizzato per impostazione predefinita per le pagine di prodotti. Opzioni: <br/>**`No layout updates`**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per le pagine di prodotto.<br/>**`Empty`** - Per impostazione predefinita, utilizza un layout vuoto per le pagine dei prodotti. <br/>**`1 column`**- Per impostazione predefinita, utilizza un layout a colonna singola per le pagine di prodotto.<br/>**`2 columns with left bar`** - Per impostazione predefinita, utilizza un layout a due colonne con la barra laterale a sinistra per le pagine dei prodotti. <br/>**`2 columns with right bar`**- Per impostazione predefinita, utilizza un layout a due colonne con la barra laterale a destra per le pagine dei prodotti.<br/>**`3 columns`** - Per impostazione predefinita, utilizza un layout a tre colonne con barre laterali a sinistra e a destra per le pagine dei prodotti.<br/>**`Page -- Full Width`**- (Richiede [!DNL Page Builder]) Per impostazione predefinita, per le pagine di prodotto viene utilizzato il layout Pagina - Larghezza intera.<br/>**`Category - Full Width`** - (Richiede [!DNL Page Builder]) Per impostazione predefinita, per le pagine dei prodotti viene utilizzato il layout Categoria - Larghezza intera. <br/>**`Product - Full Width`**- (Richiede [!DNL Page Builder]) Per impostazione predefinita, per le pagine dei prodotti viene utilizzato il layout Prodotto - Larghezza intera. |
| [!UICONTROL Default Category Layout] | Globale | Determina la [layout](../../content-design/page-layout.md) utilizzato per impostazione predefinita per le pagine delle categorie. Opzioni: <br/>**`No layout updates`**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per le pagine delle categorie.<br/>**`Empty`** - Per impostazione predefinita, utilizza un layout vuoto per le pagine delle categorie. <br/>**`1 column`**- Per impostazione predefinita, utilizza un layout a colonna singola per le pagine delle categorie.<br/>**`2 columns with left bar`** - Per impostazione predefinita, utilizza un layout a due colonne con la barra laterale a sinistra per le pagine delle categorie. <br/>**`2 columns with right bar`**- Per impostazione predefinita, utilizza un layout a due colonne con la barra laterale a destra per le pagine delle categorie.<br/>**`3 columns`** - Per impostazione predefinita, utilizza un layout a tre colonne con barre laterali a sinistra e a destra per le pagine delle categorie.<br/>**`Page - Full Width`**- (Richiede [!DNL Page Builder]) Per impostazione predefinita, per le pagine delle categorie viene utilizzato il layout Pagina - Larghezza intera.<br/>**`Category - Full Width`** - (Richiede [!DNL Page Builder]) Per impostazione predefinita, per le pagine delle categorie viene utilizzato il layout Categoria - Larghezza intera. <br/>**`Product - Full Width`**- (Richiede [!DNL Page Builder]) Per impostazione predefinita, per le pagine delle categorie viene utilizzato il layout Prodotto - Larghezza intera. |
| Layout di pagina predefinito | Globale | Determina la [layout](../../content-design/page-layout.md) utilizzato per impostazione predefinita per le pagine CMS. Opzioni: <br/>**`No layout updates`**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per le pagine CMS.<br/>**`Empty`** - Per impostazione predefinita, utilizza un layout vuoto per le pagine CMS. <br/>**`1 column`**- Per impostazione predefinita, utilizza un layout a colonna singola per le pagine CMS.<br/>**`2 columns with left bar`** - Per impostazione predefinita, utilizza un layout a due colonne con la barra laterale a sinistra per le pagine CMS.<br/>**`2 columns with right bar`**- Per impostazione predefinita, utilizza un layout a due colonne con la barra laterale a destra per le pagine CMS.<br/>**`3 columns`** - Per impostazione predefinita, utilizza un layout a tre colonne con barre laterali a sinistra e a destra per le pagine CMS.<br/>**`Page - Full Width`**- (Richiede [!UICONTROL Page Builder]) Per impostazione predefinita, utilizza il layout Pagina - Larghezza intera per le pagine CMS.<br/>**`Category - Full Width`** - (Richiede [!UICONTROL Page Builder]) Per impostazione predefinita, utilizza il layout Categoria - Larghezza intera per le pagine CMS. <br/>**`Product - Full Width`**- (Richiede [!DNL Page Builder]) Per impostazione predefinita, utilizza il layout Prodotto - Larghezza intera per le pagine CMS. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Cookie Settings]

![Web > Impostazioni cookie predefinite](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://docs.magento.com/user-guide/stores/compliance-cookie-law.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Visualizzazione store | Determina per quanto tempo un cookie può esistere prima che venga eliminato automaticamente. Il valore predefinito è 3600 secondi (1 ora) |
| [!UICONTROL Cookie Path] | Visualizzazione store | Specifica le cartelle sul server in cui è possibile utilizzare i cookie Commerce. Per rendere i cookie di Commerce disponibili ovunque nell’installazione, imposta il percorso del cookie su una singola barra: `/`. Questo valore può contenere solo il percorso del cookie e **_non può_** contiene altri parametri dei cookie. |
| [!UICONTROL Cookie Domain] | Visualizzazione store | Determina se i cookie Commerce sono disponibili per i sottodomini. Ad esempio, per supportare `mysubdomain`.domain.com, inserisci il nome del dominio con un punto all’inizio, come `.domain.com`. Questo valore può contenere solo il dominio del cookie e **_non può_** contiene altri parametri dei cookie. |
| [!UICONTROL Use HTTP Only] | Visualizzazione store | Determina se i cookie Commerce possono essere utilizzati solo su un canale non sicuro (http) o anche su un canale crittografato (https). Opzioni: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Sito Web | Determina se la modalità di restrizione dei cookie è abilitata. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Session Validation Settings]

![Web > Convalida sessione](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://docs.magento.com/user-guide/stores/security-session-validation.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Globale | Verifica che l’indirizzo IP di una richiesta corrisponda a `$_SESSION` dati. La sessione termina se viene rilevato un indirizzo IP diverso. Opzioni: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Globale | Verifica i dati proxy in arrivo e verifica che l’indirizzo proxy di una richiesta corrisponda `$_SESSION` dati. La sessione termina se viene rilevato un indirizzo proxy diverso. Opzioni: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Globale | Verifica i dati proxy in uscita e verifica che l&#39;indirizzo inoltrato di una richiesta corrisponda  `$_SESSION` dati. La sessione termina se viene rilevato un indirizzo inoltrato diverso. Opzioni: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Globale | `USER_AGENT` fa riferimento al browser o al dispositivo utilizzato per accedere al sito web. Verifica che il nome e la versione del browser e del sistema operativo corrispondano `$_SESSION` dati. La sessione termina se viene rilevato un agente utente diverso da una richiesta a un’altra nella stessa sessione. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Browser Capabilities Detection]

![Web > Rilevamento funzionalità browser](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://docs.magento.com/user-guide/stores/security-browser-capabilities-detection.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Visualizzazione store | Se i cookie sono disabilitati dal browser, viene automaticamente reindirizzato alla pagina CMS senza cookie. Opzioni: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Visualizzazione store | Se JavaScript è disabilitato dal browser, visualizza un avviso che chiede all’utente di abilitare le opzioni JavaScript: `Yes` / `No` (disabilita) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Visualizzazione store | Visualizza un messaggio se la cache locale è disabilitata. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
