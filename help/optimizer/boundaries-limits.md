---
title: Limiti e limitazioni dei servizi di merchandising
description: Scopri i limiti di licenza e i limiti del sistema di Adobe Commerce Optimizer. Pianifica la capacità, tieni traccia dell’utilizzo ed evita latenza e limitazione quando superi i limiti.
role: Admin, Developer
hide: true
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo alle istanze Adobe Commerce as a Cloud Service con provisioning CCDM (infrastruttura SaaS gestita da Adobe)."
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# Limiti e limitazioni di Merchandising Services con il modello dati catalogo componibile (CCDM)

Adobe Commerce Merchandising Services con CCDM applica limiti di licenza e limiti di sistema che definiscono la capacità utilizzabile dal progetto:

- **Limiti di licenza**—In base alla capacità acquistata; possono essere estesi acquistando pacchetti aggiuntivi.
- **Limiti di sistema**: sono stati corretti i limiti che proteggono le risorse di sistema e garantiscono prestazioni affidabili per tutti gli utenti.

Il tuo utilizzo deve rimanere entro questi limiti. Il loro superamento può causare un aumento della latenza e la limitazione delle richieste.

## Richiedi capacità aggiuntiva

I limiti di licenza possono essere aumentati acquistando i pacchetti di licenza descritti nella sezione [Limiti di licenza e limiti di sistema](#license-limits-and-system-boundaries) oppure negoziando licenze personalizzate per casi d&#39;uso univoci. Contatta il rappresentante del tuo account Adobe per discutere delle tue esigenze.

Per domande sui limiti del sistema, contatta il [Supporto Adobe](https://experienceleague.adobe.com/home?lang=it#support).

## Impedisci problemi di prestazioni

Segui queste best practice per restare entro i limiti ed evitare problemi operativi:

- **Rivedi i limiti**—Comprendi i [limiti di capacità](#license-limits-and-system-boundaries) prima di avviare nuove storefront o campagne.
- **Tieni traccia dell&#39;utilizzo**. Utilizza dashboard delle metriche o registri CDN incorporati.

## Limiti di licenza e limiti di sistema

Nelle tabelle seguenti vengono riepilogati i limiti di licenza e i limiti di sistema per area capacità e vengono fornite informazioni sull&#39;aggiunta di licenze aggiuntive per espandere la capacità, se applicabile.


### Catalogo

| **Capacità** | **Descrizione** | **Allocazione di base** | **Espandibile?** |
| --- | --- | --- | --- |
| Tasso di acquisizione dei prodotti | Il numero di prodotti creati o aggiornati | Aggiornamenti a 1K al minuto<p>Massimo 100.000 aggiornamenti al giorno</p> | Sì<p>Aggiungi un pacchetto di licenza:</p><ul><li>5.000 aggiornamenti al minuto<br>Massimo 500.000 aggiornamenti al giorno</li> <li>10.000 aggiornamenti al minuto<br>Massimo 1 milione di aggiornamenti al giorno</li></ul><p>La capacità massima per l’acquisizione dei dati è di 1 milione di aggiornamenti al giorno.</p> |
| Dimensione payload del prodotto | La quantità massima di dati consentita durante la creazione, l’aggiornamento o l’acquisizione di informazioni di prodotto tramite l’API | 200 KB | No |
| Varianti catalogo | Il numero di visualizzazioni di un catalogo disponibili per gli utenti della vetrina,<p>conteggiati come (*Numero di visualizzazioni catalogo × Numero di listini prezzi fissi*)</p> | 100 varianti | Sì<p>Aggiungi pacchetto di licenze per 100 varianti di catalogo</p> |
| Prodotti in un&#39;unica origine catalogo | SKU supportate nel catalogo | 250.000 SKU | Sì<p>Aggiungi pacchetto di licenza SKU da 100.000</p> |
| Varianti per prodotto | Il numero di varianti di prodotto (dimensioni, combinazioni di colori) consentite per prodotto | 10K | No |
| Origini del catalogo | Il numero di contesti di dati del catalogo (ad esempio, impostazioni internazionali o origini dati come PIM ed ERP) | 50 | No |

{style="table-layout:auto"}

### Listino prezzi

| **Capacità** | **Descrizione** | **Allocazione di base** | **Espandibile?** |
| --- | --- | --- | --- |
| Listino prezzi | Numero di listini prezzi consentiti per istanza | In base al numero di [varianti catalogo](#catalog) | Sì<br>Aumenta varianti di catalogo |
| Sconti per record di prezzo | Il numero di sconti che è possibile applicare a un prezzo di prodotto all&#39;interno di un singolo listino prezzi dedicato | 10 | No |

{style="table-layout:auto"}

### Visualizzazioni e criteri del catalogo

| **Capacità** | **Descrizione** | **Allocazione di base** | **Espandibile?** |
| --- | --- | --- | --- |
| Visualizzazioni catalogo | Numero di sottoinsiemi configurabili del catalogo principale | In base al numero di [varianti catalogo](#catalog) | Sì<br>Aumenta varianti di catalogo |
| Criteri per visualizzazione catalogo | Numero di filtri dati consentiti | 10 | No |
| Valori degli attributi in un criterio | Numero di caratteristiche del prodotto che possono essere configurate per il filtro | 100 | No |
| [Assegnazione chiave di accesso limitata](setup/private-catalog-view.md) | Numero di chiavi di accesso con restrizioni che possono essere assegnate a una singola vista catalogo | 3 | No |
| Dimensione chiave RSA (chiavi di accesso limitate) | Forza minima e massima della chiave accettata per una chiave ad accesso limitato | minimo 2048 bit, massimo 8192 bit | No |
| Chiavi di accesso con restrizioni | Ritardo propagazione revoca chiave | Fino a 5 minuti, a causa della memorizzazione nella cache. I token firmati da una chiave rimossa vengono negati una volta trascorso il ritardo. | Non applicabile |

{style="table-layout:auto"}

### Vetrina catalogo

L’allocazione di base per le funzionalità di vetrina del catalogo è determinata in base al livello GMV (Gross Merchandise Value). La tabella indica l&#39;allocazione minima per ogni funzionalità.

| **Capacità** | **Descrizione** | **Allocazione di base** | **Espandibile?** |
| --- | --- | --- | --- |
| Percentuale di recupero catalogo | Numero di volte in cui un’API di catalogo viene chiamata al mese da un sistema (vetrina, sistema di transazioni, ERP o altro) per recuperare dati dal catalogo | Basato sul livello GMV<p>Allocazione minima: 10 milioni/mese</p> | Sì<p>Aggiungi 1 milione di richieste al mese pacchetti di licenze</p> |
| Richieste di contenuto | Richieste allo storefront per le visualizzazioni di pagina HTML o per le chiamate API JSON. Conteggiato come 1 visualizzazione pagina o 5 chiamate API. | Basato sul livello GMV<p>Allocazione minima: 2 milioni/mese</p> | Sì<p>Aggiungi pacchetto di licenze di 1 milione al mese</p> |
| Varianti GenAI per vetrina | Tolleranza per la generazione di contenuti basati su testo | Basato sul livello GMV<p>Allocazione minima: 1K variazioni/mese</p> | Sì<p>Acquistare separatamente i crediti IA generativi</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>La generazione dell&#39;immagine richiede una licenza [!DNL Adobe Firefly] fornita alla stessa organizzazione IMS di [!DNL Adobe Commerce Optimizer].


### Individuazione prodotto

I seguenti limiti si applicano alla ricerca di prodotti vetrina, all’elenco e alla configurazione del merchandising.

| **Capacità** | **Descrizione** | **Allocazione di base** | **Espandibile?** |
| --- | --- | --- | --- |
| Recupero del prodotto | Numero massimo di SKU per [!DNL Catalog Service] richiesta GraphQL durante il recupero dei dati prodotto con `products`, `productSearch`, `refineProduct` e `variants`. Suddividere le richieste più grandi in più chiamate. | 100 | No |
| Attributi filtrabili | Il numero di caratteristiche del prodotto (come colore, dimensioni, marchio o materiale) che possono essere abilitate per la navigazione e i facet su più livelli | 200 | No |
| Attributi ricercabili | Numero di caratteristiche del prodotto che possono essere indicizzate per la ricerca nel catalogo | 200 | No |
| Attributi ordinabili | Il numero di caratteristiche del prodotto disponibili come opzioni di ordinamento nelle pagine di ricerca e categoria. | 50 | No |
| Profondità di paginazione della ricerca | Numero massimo di prodotti raggiungibili tramite impaginazione ricerca (ad esempio, pagina 100 × 100 prodotti/pagina) | 10K | No |
| Facet | Il numero di attributi di prodotto filtrabili (come Marchio, Colore, Dimensione, Prezzo) che possono essere configurati per aiutare gli acquirenti a perfezionare i risultati di ricerca e sfogliare le categorie | 100<p>Deve essere un attributo filtrabile</p> | No |
| Opzioni per facet | Il numero di valori di attributi di prodotto filtrabili che gli acquirenti possono selezionare all’interno di un facet (ad esempio, &quot;Rosso&quot;, &quot;Blu&quot; per Colore; &quot;Piccolo&quot;, &quot;Medium&quot; per Dimensione) | 100 | Sì<p>Può aumentare tramite richiesta di supporto</p> |

{style="table-layout:auto"}

### Consigli

Per i consigli sui prodotti sono disponibili le seguenti funzionalità. Alcune funzionalità disponibili in altri prodotti Adobe Commerce non sono supportate in [!DNL Adobe Commerce Optimizer].

| **Capacità** | **Descrizione** | **Allocazione di base** | **Espandibile?** |
| --- | --- | --- | --- |
| Unità di consigli attive | Numero di componenti per consigli live nella vetrina (ad esempio &quot;Hanno visto anche i clienti&quot; o &quot;Potrebbe piacerti anche&quot;) | 50 | No |
| Inclusioni/esclusioni di categorie o attributi | Filtra i prodotti in base a un set specifico idoneo per i consigli | Non supportato | — |

{style="table-layout:auto"}
