---
title: Reindirizzamenti a termine di ricerca e indirizzamento vetrina
description: Scopri come scegliere i reindirizzamenti a termine di ricerca, le riscritture URL, le regole di Live Search o il routing della vetrina in base alla distribuzione per Adobe Commerce e Edge Delivery Services.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# Reindirizzamenti a termine di ricerca e indirizzamento della vetrina

I reindirizzamenti a termine di ricerca, i reindirizzamenti URL e il merchandising di ricerca risolvono diversi problemi. Utilizzare questa guida per scegliere la funzionalità corretta per la ricerca [!DNL Adobe Commerce] standard, [!DNL Live Search] e [!DNL Commerce Storefront] con tecnologia [!DNL Edge Delivery Services].

## Comprendere i tipi di reindirizzamento

Queste funzionalità differiscono per quanto riguarda gli elementi che attivano il comportamento e ciò che vede l’acquirente:

* Un reindirizzamento a **termine di ricerca** invia un acquirente che immette un termine di ricerca specifico a una pagina designata.

* Un reindirizzamento **URL** invia una richiesta per un URL precedente a un nuovo URL, in genere con una risposta HTTP 301 o 302. La barra degli indirizzi del browser diventa il nuovo URL.

* **Il merchandising di Search** modifica i prodotti visualizzati, o il loro ordine, nei risultati di ricerca senza modificare l&#39;URL richiesto.

* Una **riscrittura URL** associa un URL a un altro sul server. Lo strumento di riscrittura URL [!DNL Adobe Commerce] crea un reindirizzamento permanente (301) per l&#39;URL precedente. Per ulteriori informazioni, vedere [Riscritture URL](url-rewrite.md).

## Scegliere una funzionalità di routing

Utilizza le seguenti indicazioni per identificare la funzionalità che soddisfa le tue esigenze:

| Requisito | Funzionalità consigliata |
| --- | --- |
| Invia una query specifica dalla ricerca [!DNL Adobe Commerce] standard a una pagina | Configura un termine di ricerca in [Gestisci termini di ricerca](../catalog/search-terms.md), se supportato. |
| Modificare la classificazione del prodotto o la visibilità nei risultati di ricerca | Utilizza [!DNL Live Search] [sinonimi](https://experienceleague.adobe.com/it/docs/commerce/live-search/live-search-admin/synonyms/synonyms) o [regole di merchandising](https://experienceleague.adobe.com/it/docs/commerce/live-search/live-search-admin/rules/rules-add). |
| Reindirizzare un URL di prodotto, categoria o CMS precedente | Utilizza lo strumento Commerce [URL Rewrite](url-rewrite.md) quando applicabile alla distribuzione. |
| Reindirizza un percorso [!DNL Edge Delivery Services] | Utilizza il routing storefront o CDN. |
| Mantenere gli URL legacy dopo una migrazione della vetrina | Crea e verifica una mappa di reindirizzamento URL da legacy a nuova. |

## Ricerca Commerce standard

Con la ricerca standard nel catalogo, puoi configurare un termine di ricerca per aprire una pagina di contenuto, una pagina di categoria, una pagina di prodotto o una pagina esterna in cui la distribuzione supporta questa funzionalità. Utilizzarla quando una query inserita dall&#39;acquirente, ad esempio `gift cards` o `returns`, deve aprire una campagna o una pagina informativa.

Per creare o aggiornare questo tipo di reindirizzamento, vedi [Gestire i termini di ricerca](../catalog/search-terms.md). La configurazione del termine di ricerca è separata dallo strumento URL Rewrite, perché il trigger è la query dell’acquirente, non un URL esistente.

>[!NOTE]
>
>Verifica che la vetrina utilizzi la ricerca standard nel catalogo e supporti i reindirizzamenti nativi dei termini di ricerca. Il comportamento e la configurazione disponibile possono essere diversi per [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service] o una vetrina headless.

## L’URL reindirizza e riscrive

Utilizza un URL riscritto quando l’origine è un URL esistente anziché un termine di ricerca immesso dall’acquirente. Alcuni esempi comuni includono il reindirizzamento:

* URL di prodotto precedente a URL di prodotto nuovo.

* Un URL di categoria ritirato in un URL di categoria sostitutivo.

* URL obsoleto di una pagina CMS in un nuovo URL di pagina di contenuto.

Per le distribuzioni che supportano lo strumento di riscrittura URL, vai a **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]** per creare il reindirizzamento. Per istruzioni dettagliate, consulta [Riscritture URL](url-rewrite.md).

>[!NOTE]
>
>L&#39;argomento [URL rewrites](url-rewrite.md) si applica solo a PaaS. Per [!DNL Adobe Commerce as a Cloud Service] o una vetrina [!DNL Edge Delivery Services], utilizzare le istruzioni di routing per la vetrina.

## Live Search

[!DNL Live Search] sostituisce l&#39;esperienza di ricerca predefinita nella vetrina e fornisce funzionalità quali sinonimi, facet e regole di merchandising.

Utilizza [!DNL Live Search] quando devi modificare la rilevanza della ricerca, la classificazione del prodotto o la visibilità del prodotto. Utilizzare i sinonimi quando parole diverse restituiscono prodotti simili. Utilizza le regole di merchandising quando i prodotti devono essere potenziati, seppelliti o classificati in modo diverso.

Il comportamento di ricerca [!DNL Live Search] non deve essere trattato come un sostituto del drop-in per ogni configurazione nativa dei termini di ricerca di Commerce. Quando una query deve passare a una pagina di contenuto o di campagna, implementa il reindirizzamento nel livello storefront o edge-routing che riceve la richiesta. Per ulteriori informazioni, consulta la [[!DNL Live Search] documentazione](https://experienceleague.adobe.com/it/docs/commerce/live-search/overview).

## Servizi di consegna Edge

Per una vetrina con tecnologia [!DNL Edge Delivery Services], gestisci i reindirizzamenti nella vetrina o nel livello di indirizzamento Edge. Non presumere che l&#39;URL amministratore [!DNL Adobe Commerce] riscriva controlli ogni richiesta.

Quando si utilizza l&#39;authoring dei documenti, è necessario mantenere i mapping di reindirizzamento nella configurazione di reindirizzamento del sito. Per i reindirizzamenti che devono essere eseguiti prima che una richiesta raggiunga l’origine, utilizza la configurazione CDN o Edge appropriata. Per le istruzioni SEO correlate, vedere [Linee guida SEO per Commerce Storefront](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=it).

## Migra da Luma

Tratta la migrazione di reindirizzamento come parte della migrazione della vetrina. Mantenere il percorso del cliente e l’intento SEO (Search Engine Optimization), quindi implementare nuovamente il routing per la vetrina di destinazione.

Prima di passare alla nuova vetrina:

1. Esporta e crea un inventario degli URL Luma esistenti e delle pagine di destinazione dei termini di ricerca.

1. Classifica ogni elemento come regola di reindirizzamento dei termini di ricerca, di reindirizzamento URL o di merchandising.

1. Mappa ogni URL legacy al nuovo percorso della vetrina.

1. Implementa ogni reindirizzamento sul livello che riceve la richiesta.

1. Codici di stato del test, parametri di query, URL canonici, percorsi delle impostazioni internazionali e cicli di reindirizzamento.

1. Monitora registri e analisi dopo l’avvio per individuare gli URL legacy non risolti.

## Risolvere i problemi dei reindirizzamenti

Utilizzare i controlli seguenti quando un reindirizzamento non si comporta come previsto nelle viste di ricerca, storefront routing e store di [!DNL Adobe Commerce].

| Problema | Cosa controllare |
| --- | --- |
| Un termine di ricerca non viene reindirizzato | Verifica che la vetrina utilizzi la ricerca standard nel catalogo, che la query di ricerca corrisponda al termine configurato e che il termine di ricerca sia assegnato alla vista archivio corretta. Se [!DNL Live Search] è abilitato, verificare che il reindirizzamento sia implementato nel livello storefront o edge. |
| Un reindirizzamento funziona su Luma ma non su Edge Delivery Services | Verificare che il reindirizzamento sia configurato nel livello di routing della vetrina o della rete CDN [!DNL Edge Delivery Services]. [!DNL Adobe Commerce] Le riscritture dell’URL amministratore potrebbero non ricevere la richiesta. |
| Live Search restituisce i risultati invece di reindirizzare | Utilizza [!DNL Live Search] regole per la classificazione del prodotto e la visibilità. Per la navigazione a una pagina di contenuto o di campagna, configura il reindirizzamento nella vetrina o nel livello Edge. |
| Un reindirizzamento funziona in una vista store ma non in un’altra | Controlla la visualizzazione store assegnata al termine di ricerca o alla regola URL. Verifica il percorso e la query completi delle impostazioni locali in ogni visualizzazione archivio interessata. |

## Ulteriori informazioni su questo argomento

* [Panoramica e best practice per l’ottimizzazione SEO](seo-overview.md)

* [Che cos&#39;è la vetrina?](../getting-started/storefront.md)

* [Gestire i termini di ricerca](../catalog/search-terms.md)

* [Riscritture URL](url-rewrite.md)
