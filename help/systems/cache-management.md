---
title: Gestione della cache
description: Scopri come utilizzare gli strumenti di gestione della cache, che offrono un modo semplice per migliorare le prestazioni del sito.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# Gestione della cache

Adobe Commerce e Magento Open Source Cache Management System offrono un modo semplice per migliorare le prestazioni del sito. Ogni volta che una cache richiede un aggiornamento, nella parte superiore dell’area di lavoro viene visualizzato un avviso che ti guida attraverso il processo. Segui il collegamento a Gestione cache e aggiorna le cache non valide.

![Salva attributo prodotto - messaggio di aggiornamento cache](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>Quando vengono modificate le entità catalogo, questo può influenzare altre pagine e annullare la validità di più cache contemporaneamente. Quando si controlla la pagina di gestione della cache, è possibile che vengano visualizzati elementi non validi che richiedono l&#39;aggiornamento quando _**non modificato direttamente**_. Ad esempio, l’annullamento della validità si verifica quando si modifica un prodotto nel catalogo che viene assegnato a qualsiasi categoria o quando si modifica una regola di prodotto correlata.

Il _[!UICONTROL Cache Management]_mostra lo stato di ciascuna cache principale e del relativo tag associato. I pulsanti grandi nell’angolo in alto a destra possono essere utilizzati per effettuare il flushing della cache o dell’archiviazione cache completa. Nella parte inferiore della pagina sono disponibili pulsanti aggiuntivi per svuotare la cache delle immagini del prodotto del catalogo e la cache JavaScript/CSS.

Dopo aver cancellato una cache, aggiorna sempre il browser per assicurarti di poter visualizzare i file più recenti. La cancellazione della cache di Commerce non comporta la cancellazione della cache del browser Web. Per visualizzare il contenuto aggiornato, potrebbe essere necessario cancellare la cache del browser.

Per ulteriori informazioni tecniche, consulta [Panoramica sulla cache](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} nella _Guida allo sviluppo di Commerce Frontend_.

Accedere a _[!UICONTROL Cache Management]_eseguendo una delle operazioni seguenti:

- Fai clic su **[!UICONTROL Cache Management]** nel messaggio sopra l’area di lavoro.
- Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Gestione della cache](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Best practice per il caching

La reindicizzazione e il caching hanno scopi diversi in Commerce. [Indici](index-management.md) tenere traccia delle informazioni del database per migliorare le prestazioni di ricerca, velocizzare il recupero dei dati per gli storefront e altro ancora. Le cache consentono di salvare i dati caricati, le immagini, i formati e così via per migliorare le prestazioni di caricamento e accesso alla vetrina.

- Svuota sempre la cache dopo aver installato estensioni/moduli. Puoi installare una o più estensioni, quindi svuotare la cache.
- Svuota la cache dopo l’installazione di Commerce. Per le nuove installazioni, è inoltre necessario reindicizzare.
- Svuota la cache dopo l’aggiornamento da una versione di Open Source o Commerce a un’altra.
- Quando si scaricano le cache, considerare il tipo di cache e pianificare lo scaricamento durante gli orari non di picco. Ad esempio, scegli un’ora in cui pochi clienti possono accedere al sito, ad esempio la sera tardi o la mattina presto. La cancellazione di alcuni tipi di cache durante i periodi di picco causa un carico elevato per l’amministratore e può causare l’inattività del sito fino al completamento.
- Quando [reindicizzazione](index-management.md), non è necessario eseguire anche una cache di scaricamento.

## Risorse del ruolo Gestione cache

L’accesso a specifiche azioni di manutenzione della cache può essere assegnato agli utenti per ruolo, incluse le opzioni per visualizzare, attivare e disattivare le cache. L’Adobe consiglia di abilitare le azioni di svuotamento solo per gli utenti a livello di amministratore. L&#39;accesso a tutte le funzioni di gestione della cache può influire sulle prestazioni della vetrina.

![Risorse per ruolo - Gestione cache](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Per informazioni sull’assegnazione di risorse per concedere l’accesso agli account utente amministratore, consulta [Risorse per il ruolo](permissions-user-roles.md#role-resources). Le risorse seguenti controllano l’accesso agli strumenti di gestione della cache:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Aggiorna cache specifiche

1. Per ogni cache da aggiornare, seleziona la casella di controllo all’inizio della riga.

1. Imposta **[!UICONTROL Actions]** a `Refresh` e fai clic su **[!UICONTROL Submit]**.

## Esegui aggiornamento di massa delle azioni

1. Per selezionare un gruppo di cache, impostare **[!UICONTROL Mass Actions]** a uno dei seguenti elementi:

   - `Select All`
   - `Select Visible`

1. Seleziona la casella di controllo di ogni cache di destinazione dell’azione.

1. Imposta **[!UICONTROL Actions]** a `Refresh` e fai clic su **[!UICONTROL Submit]**.

## Svuota la cache delle immagini del prodotto

1. Sotto _[!UICONTROL Additional Cache Management]_, fai clic su **[!UICONTROL Flush Catalog Images Cache]**per cancellare i file immagine del prodotto pregenerati.

   Il `Image cache was cleaned` nella parte superiore dell&#39;area di lavoro.

1. Cancella la cache del browser.

## Scaricare la cache JavaScript/CSS

1. Sotto _[!UICONTROL Additional Cache Management]_, fai clic su **[!UICONTROL Flush JavaScript/CSS Cache]**per cancellare tutti i file JavaScript e CSS che sono stati uniti in un singolo file.

   Il `The JavaScript/CSS cache has been cleaned` nella parte superiore dell&#39;area di lavoro.

1. Cancella la cache del browser.

## Svuota utilizzando la riga di comando

Commerce fornisce opzioni aggiuntive di svuotamento della cache utilizzando la riga di comando. Per il completamento di queste opzioni potrebbe essere necessario il supporto degli sviluppatori. Per informazioni dettagliate e opzioni di comando, vedere [Gestire la cache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){:target=&quot;_blank&quot;} nella _Guida alla configurazione_.

## Controlli

| Controllo | Descrizione |
|--- |--- |
| [!UICONTROL Mass Actions] | Seleziona la casella di controllo di più cache. Opzioni: <br/>**[!UICONTROL Select All]**— seleziona la casella di controllo di tutte le cache.<br/>** Deseleziona tutto **— Deseleziona la casella di controllo di tutte le cache.<br/>**[!UICONTROL Select Visible]** — seleziona la casella di controllo di tutte le cache visibili. <br/>**[!UICONTROL Unselect Visible]**— deseleziona la casella di controllo di tutte le cache visibili. |
| [!UICONTROL Actions] | Determina l&#39;azione da applicare a tutte le cache selezionate. Opzioni: <br/>**[!UICONTROL Enable]**— Attiva tutte le cache selezionate.<br/>**[!UICONTROL Disable]** — Disattiva tutte le cache selezionate. <br/>**[!UICONTROL Refresh]**— Aggiorna tutte le cache selezionate. |
| [!UICONTROL Submit] | Applica l&#39;azione a tutte le cache selezionate. |

{style="table-layout:auto"}

### Pulsanti

| Pulsante | Descrizione |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | Rimuove tutti gli elementi nella cache di Commerce predefinita (`var/cache`), in base ai tag Commerce associati. |
| [!UICONTROL Flush Cache Storage] | Rimuove tutti gli elementi dalla cache, indipendentemente dal tag di Commerce. Se il sistema utilizza un percorso di cache alternativo, tutti i file memorizzati in cache utilizzati da altre applicazioni vengono rimossi durante il processo. |
| [!UICONTROL Flush Catalog Images Cache] | Rimuove tutte le immagini di catalogo ridimensionate e filigranate automaticamente memorizzate in `media/catalog/product/cache`. Se le immagini caricate di recente non sono incluse nel catalogo, prova a scaricare il catalogo e ad aggiornare il browser. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Rimuove la copia unita dei file JavaScript e CSS dalla cache. Se le modifiche recenti al foglio di stile o al JavaScript non vengono riportate nell’archivio, prova a svuotare la cache JavaScript/CSS e ad aggiornare il browser. |
| [!UICONTROL Flush Static Files Cache] | Rimuove i file di visualizzazione preelaborati e i file statici. |

{style="table-layout:auto"}

### Cache

| Cache | Descrizione | Tag associato |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | Varie configurazioni XML raccolte tra moduli e unite.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | Istruzioni per la creazione di layout. | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | Pagina blocca HTML. | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | File di dati di raccolta. | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | Cancella i dati di riflessione dell’interfaccia API, in genere generati durante il runtime. | `REFLECTION` |
| [!UICONTROL Database DDL operations] | Risultati di query DDL, ad esempio la descrizione di tabelle o indici. | `DB_DDL` |
| [!UICONTROL Compiled Config] | Risultati della compilazione del codice. | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | Cache della dichiarazione dei tipi di entità. | `EAV` |
| [!UICONTROL Customer Notification] | Notifiche temporanee visualizzate nell’interfaccia utente. | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | File di configurazione dell’integrazione. | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | File di configurazione dell’API Integrazioni. | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | Memorizzazione in cache di pagine intere. | `FPC` |
| [!UICONTROL Translations] | File di traduzione. | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | Configurazioni REST e SOAP, file WSDL generato. | `WEBSERVICE` |
| [!UICONTROL Target Rule] | Indice delle regole di destinazione | `TARGET_RULE` |

{style="table-layout:auto"}

## Memorizzazione in cache a pagina intera

Adobe Commerce e Magento Open Source utilizzano il caching a pagina intera sul server per visualizzare rapidamente le pagine per categorie, prodotti e CMS. La memorizzazione nella cache a pagina intera migliora i tempi di risposta e riduce il carico sul server. Senza la memorizzazione nella cache, ogni pagina potrebbe dover eseguire blocchi di codice e recuperare informazioni dal database. Tuttavia, con il caching a pagina intera abilitato, una pagina completamente generata può essere letta direttamente dalla cache.

>[!NOTE]
>
>Si consiglia di: [Cache vernice](https://varnish-cache.org/){:target=&quot;_blank&quot;} può essere utilizzato solo in un ambiente di produzione.

Il contenuto nella cache può essere utilizzato per elaborare le richieste provenienti da tipi di visite simili. Di conseguenza, le pagine mostrate a un visitatore occasionale potrebbero essere diverse da quelle mostrate a un cliente. Ai fini del caching, ogni visita è di tre tipi:

- `Non-sessioned` - Durante una visita senza sessione, l’acquirente visualizza le pagine, ma non interagisce con il negozio. Il sistema memorizza in cache il contenuto di ogni pagina visualizzata e le distribuisce ad altri acquirenti non sessionati.
- `Sessioned` - Durante una visita in sessione, agli acquirenti che interagiscono con il negozio, attraverso attività come il confronto dei prodotti o l’aggiunta di prodotti al carrello, viene assegnato un ID sessione. Le pagine in cache generate durante la sessione vengono utilizzate solo da quell’acquirente durante la sessione.
- `Customer` - Le sessioni per i clienti vengono create per coloro che si sono registrati per un account presso il negozio e il negozio durante l&#39;accesso ai loro account. Durante la sessione, ai clienti possono essere presentate offerte speciali, promozioni e prezzi basati sul gruppo di clienti assegnato.

Per informazioni tecniche, consulta [Configurare e utilizzare vernice](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} e [Usa Redis per la pagina Commerce e la cache predefinita](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} nella _Guida alla configurazione_.

**_Per configurare la cache a pagina intera:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Full Page Cache]** sezione.

   ![Configurazione avanzata: cache a pagina intera](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Caching Application]** a uno dei seguenti elementi:

   - `Built-in Application`
   - `Varnish Caching`

1. Per impostare il timeout per la cache della pagina, immetti **[!UICONTROL TTL for public content]**. Il valore predefinito è `86400`)

1. Se si utilizza la vernice, completare il **[!UICONTROL Varnish Configuration]** come segue:

   - **[!UICONTROL Access list]** - Immetti gli indirizzi IP che possono eliminare la configurazione Vernice per generare un file di configurazione. Separa più voci con una virgola. Il valore predefinito è `localhost`.

   - **[!UICONTROL Backend host]** - Immettere l&#39;indirizzo IP dell&#39;host backend che genera i file di configurazione. Il valore predefinito è `localhost`.

   - **[!UICONTROL Backend port]** - Identifica la porta back-end utilizzata per generare i file di configurazione. Il valore predefinito è: `8080`.

   - **[!UICONTROL Grace period]** - Specifica il numero di secondi da utilizzare come periodo di tolleranza per generare i file di configurazione. Consulta [Configurazione vernice avanzata](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) nel _Guida alla configurazione_.

   - Per esportare la configurazione come `varnish.vcl` file, fare clic sul pulsante relativo alla versione di Vernice utilizzata.

   ![Configurazione avanzata: vernice per cache a pagina intera](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
