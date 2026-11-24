---
title: Arricchimento catalogo
description: Utilizza l'arricchimento del catalogo [!DNL Adobe Commerce] per rivedere la copia del prodotto suggerita dall'intelligenza artificiale, creare processi di arricchimento e distribuire aggiornamenti approvati per l'individuazione di LLM e IA.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b2a1abb72839717a7249e9a34b13266b8e384189
workflow-type: tm+mt
source-wordcount: '1976'
ht-degree: 0%
---
# Arricchimento del catalogo

L&#39;arricchimento del catalogo è una funzionalità nativa di [!DNL Adobe Commerce] che consente di migliorare i nomi dei prodotti e le descrizioni lunghe in modo che il catalogo venga rappresentato in modo più accurato quando gli acquirenti utilizzano LLM e assistenti AI per la ricerca e l&#39;individuazione dei prodotti.

## Come funziona {#how-it-works}

Il catalogo prodotti [!DNL Adobe Commerce] è il sistema di registrazione per i dati dei prodotti: nomi, descrizioni, attributi, prezzi e inventario. [!DNL Adobe Commerce] connette i dati del catalogo live alle esperienze Adobe AI. Da lì, l’agente catalogo può identificare le lacune nei nomi dei prodotti e nelle descrizioni lunghe, proporre miglioramenti e riscrivere le modifiche approvate in Commerce in modo da poterle esaminare nell’amministratore Commerce.

Con l’arricchimento del catalogo puoi:

- Identifica le lacune e le incoerenze nei nomi dei prodotti e nelle descrizioni lunghe che influiscono sul modo in cui i moduli LLM interpretano i prodotti.
- Revisione dei miglioramenti suggeriti con contesto di supporto, incluse giustificazioni e confronti prima e dopo.
- Applica gli aggiornamenti approvati direttamente al catalogo Commerce in modo che l’amministratore, la vetrina e altri canali che leggono tali campi rimangano allineati.

Poiché i nomi dei prodotti e le descrizioni lunghe risiedono in Commerce, il miglioramento della copia una sola volta può essere utile per ogni canale che utilizza tali dati di prodotto. Il vantaggio dipende da come e quando i sistemi vengono aggiornati.

| Direzione | Finalità |
| --- | --- |
| Catalogo Commerce -> analisi | I segnali di traffico del catalogo e dell’Agentic rivelano opportunità di suggerimenti di arricchimento. |
| Arricchimento -> Catalogo Commerce | Dopo aver approvato un aggiornamento, le modifiche al nome e alla descrizione del prodotto vengono salvate nel catalogo Commerce in modo che l’amministratore e la vetrina riflettano i valori ottimizzati. |

### Accedere all’arricchimento del catalogo

Prima di iniziare, esaminare i [prerequisiti per l&#39;individuazione dei prodotti AI specifici della distribuzione](prerequisites.md). Dopo aver completato la configurazione per la piattaforma Commerce, vai a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** nell&#39;amministratore.

![Dashboard di arricchimento del catalogo](assets/catalog-enrich-dashboard.png){zoomable="yes"}

L&#39;area di lavoro di arricchimento del catalogo include le schede **[!UICONTROL Optimizations]**, **[!UICONTROL Brand governance]** e **[!UICONTROL Settings]**.

- Utilizzare la scheda **[!UICONTROL Optimizations]** per esaminare i segnali di rilevamento basati sul traffico agente e gestire i processi di arricchimento.
- Utilizzare la scheda **[!UICONTROL Brand Governance]** per [definire i requisiti](brand-governance.md) per i nomi e le descrizioni dei prodotti generati da [!DNL Commerce Catalog Agent].
- Utilizza la scheda **[!UICONTROL Settings]** per [connettere la tua istanza di Commerce](settings.md) all&#39;individuazione di prodotti AI.

L’estensione condivisa abilita anche l’arricchimento di PDP, che dispone di un flusso di lavoro separato per esporre fatti di prodotto strutturati agli agenti di intelligenza artificiale. Consulta [arricchimento della pagina dei dettagli del prodotto](pdp-enrichment.md).

## Due percorsi di arricchimento del catalogo

Esistono due percorsi per ricevere gli arricchimenti del catalogo:

- **Traffico agente** - Questo tipo di arricchimento viene avviato automaticamente 24-48 ore dopo la configurazione dell&#39;istanza di Commerce e visualizza i risultati nella scheda **Ottimizzazioni**.
- **Gestione arricchimenti** - I commercianti configurano questi arricchimenti quando fanno clic sul pulsante **[!UICONTROL Create enrichment]** e selezionano manualmente gli SKU da arricchire. Ulteriori informazioni su [Gestione arricchimenti](#create-an-enrichment-job).

### Rivedere e applicare l’arricchimento del catalogo {#review-and-apply}

Dopo aver abilitato e configurato l&#39;arricchimento del catalogo, utilizzare la scheda **[!UICONTROL Optimizations]** per esaminare le informazioni sul traffico di ricerca e agenti e gestire i processi di arricchimento.

### Verifica il traffico agente mensile

Ogni controllo del traffico agenziale mensile identifica SKU a traffico elevato e rende disponibile un batch consigliato. Le ottimizzazioni per la revisione vengono generate automaticamente per gli SKU con traffico agente elevato. Queste ottimizzazioni vengono generate automaticamente in base alla regola di governance &quot;Predefinita&quot;. Le schede mensili mostrano il conteggio dei prodotti, le visite dell’agente di intelligenza artificiale e lo stato del processo. I batch con traffico agente e autoselezionati utilizzano lo stesso flusso di lavoro di selezione, conferma, esecuzione, revisione e distribuzione delle regole.

### Esamina i processi che richiedono attenzione

Nella sezione **[!UICONTROL Needs your attention]** sono evidenziati i processi che richiedono un&#39;azione, inclusi quelli completati e pronti per la revisione. Apri un processo completato per esaminare le modifiche proposte al prodotto prima della distribuzione.

### Trova processi

Nella tabella **[!UICONTROL All jobs]** sono elencati l&#39;ID di ogni processo, il nome, l&#39;origine, il conteggio SKU, la regola utilizzata, l&#39;ora di inizio e lo stato. Le origini identificano se un batch è stato autoselezionato o è stato consigliato dal traffico agente. Tenere traccia dello stato di elaborazione come **[!UICONTROL Queued]**, **[!UICONTROL Running]**, **[!UICONTROL Completed]** o **[!UICONTROL Failed]**. Nell&#39;area di lavoro Ottimizzazioni, questi processi possono anche essere visualizzati come **[!UICONTROL Generating]** durante l&#39;esecuzione, **[!UICONTROL Ready to review]** al termine della generazione e **[!UICONTROL Deployed]** dopo la distribuzione delle modifiche approvate. È possibile eseguire più processi contemporaneamente. Riprovare un processo non riuscito con **[!UICONTROL Retry]**.

### Creare un processo di arricchimento

**Per creare un arricchimento del catalogo:**

![Crea arricchimento catalogo](./assets/create-cat-enrich.png){zoomable="yes"}

1. In **[!UICONTROL Optimizations]**, fare clic su **[!UICONTROL Create enrichment]**.
1. Immetti un nome di **arricchimento**, ad esempio &quot;Black Friday 2026&quot;.
1. Selezionare la **categoria**, ad esempio &quot;Caffè&quot;.
1. Selezionare il **set di attributi**, ad esempio &quot;Accessori&quot;.
1. Selezionare il **tipo di prodotto**, ad esempio &quot;Prodotto semplice&quot;.
1. Selezionare la **fascia di prezzo**.
1. Fare clic su **[!UICONTROL Apply filters]**.

   Puoi visualizzare in anteprima i prodotti che corrispondono ai tuoi criteri di arricchimento e fare clic su **Personalizza** per definire ulteriormente l&#39;ambito dei prodotti che desideri arricchire.

1. Fai clic su **[!DNL Next]** e visualizza in anteprima la [regola di governance](brand-governance.md) applicata all&#39;arricchimento.
1. Fare clic su **[!DNL Next]** per confermare i prodotti specifici che si desidera arricchire.
1. Fare clic su **[!DNL Run enrichment]**.

   Il processo di arricchimento viene eseguito e visualizzato nella tabella Ottimizzazioni. Al termine dell&#39;esecuzione, sarà possibile [rivedere e distribuire](#review-deploy-catalog) le ottimizzazioni.

### Rivedere e distribuire un processo di arricchimento {#review-deploy-catalog}

Aprire un processo di arricchimento.

![Elenco URL di arricchimento catalogo](./assets/catalog-enrich-urls.png){zoomable="yes"}

Nella tabella **URL con suggerimenti** sono elencati tutti i prodotti con opportunità di arricchimento. Per ogni prodotto è possibile:

- **Espandere la riga** per visualizzare l&#39;analisi di IA e l&#39;arricchimento proposto.
- **Modifica** il nome o la descrizione del prodotto proposto prima di fare domanda, per allinearli alle linee guida per la voce e il merchandising del tuo marchio.
- **Distribuisci l&#39;ottimizzazione** per i prodotti che desideri arricchire e pubblicarla direttamente nel tuo catalogo Adobe Commerce.
- **Contrassegna come Fisso** dopo aver rivisto e applicato l&#39;arricchimento.
- **Ignora** suggerimenti non rilevanti per la strategia del catalogo.

I suggerimenti sono organizzati in tre visualizzazioni: **Suggerimenti correnti**, **Suggerimenti corretti** e **Suggerimenti ignorati**. Dopo aver applicato un arricchimento, questo viene spostato su Fixed Suggestions con uno stato di **Applied** e un&#39;azione **View in Catalog** per verificare l&#39;aggiornamento in Adobe Commerce. Gli arricchimenti applicati possono essere ripristinati in qualsiasi momento, ripristinando il nome e la descrizione del prodotto originali.

## Verificare l’arricchimento nell’amministratore {#verify-in-admin}

**Per verificare l&#39;arricchimento del catalogo applicato:**

1. Vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]** nell&#39;amministratore di Commerce.
1. Utilizza i filtri e il selettore **[!UICONTROL Store View]** come necessario (ad esempio, **[!UICONTROL Default Store View]**).
1. Cerca lo SKU.
1. Apri il prodotto in modalità di modifica.

   Il modulo del prodotto riporta il nome e/o la descrizione del prodotto arricchito.

   ![Nome prodotto arricchito](./assets/enriched-product-name.png){zoomable="yes"}

1. Facoltativo: selezionare **[!UICONTROL Override Catalog Agent provided Product Name]** se si desidera mantenere un nome immesso manualmente.

   Le sostituzioni manuali influiscono sul modo in cui i suggerimenti rimangono sincronizzati con il catalogo. Per ulteriori informazioni, vedere [Sostituzione manuale in Admin](#manual-override-in-the-admin).

1. Espandere la sezione **[!UICONTROL Content]** e individuare il campo di descrizione.

   La descrizione arricchita viene visualizzata quando si applicano le modifiche alla descrizione.

   ![Arricchisci descrizione prodotto](./assets/enrich-product-description.png){zoomable="yes"}

1. Facoltativo: selezionare **[!UICONTROL Override Catalog Agent provided Description]** se si desidera conservare una descrizione immessa manualmente.

Le sostituzioni manuali influiscono sul modo in cui i suggerimenti rimangono sincronizzati con il catalogo. Per ulteriori informazioni, vedere [Sostituzione manuale in Admin](#manual-override-in-the-admin).

## Verificare l’arricchimento nella vetrina {#verify-storefront}

**Per verificare l&#39;arricchimento nella vetrina:**

1. Cerca lo SKU nella vetrina.
1. Apri la pagina del prodotto.
1. Verifica che il nome e la descrizione del prodotto corrispondano a quelli approvati.

   Potrebbero volerci un po&#39; di tempo prima che l&#39;arricchimento appaia sul vetrina.

1. Verifica che le aree che mostrano la descrizione estesa corrispondano a quelle approvate.
1. Facoltativo: conferma i canali a valle che utilizzano gli stessi attributi del catalogo, se pertinente per il rollout.

## Override, acquisizione e suggerimenti obsoleti {#overrides-ingestion}

Dopo che l’arricchimento del catalogo ha aggiornato il nome o la descrizione di un prodotto, gli stessi campi possono essere modificati da altri sistemi di acquisizione. Alcuni esempi includono chiamate REST API, importazioni CSV e feed PIM.

### Valore originale riacquisito {#original-value-reingested}

Se un processo esterno scrive il nome o la descrizione originale (il valore esistente prima dell’applicazione dell’arricchimento), Commerce continua a rispettare il valore arricchito per quel campo in base alle regole di arricchimento del catalogo. Il suggerimento potrebbe non essere ripristinato automaticamente in base a quella sola acquisizione.

### Nuovo valore riacquisito {#new-value-reingested}

Se il processo esterno invia un nuovo valore che non è una ripetizione del testo di prearricchimento, Commerce rispetta il nuovo valore di catalogo. Ad esempio, il valore arricchito viene sostituito con un nuovo nome da &quot;Scarpe rosse&quot; a &quot;Scarpe rosse iconiche&quot;. Il suggerimento di arricchimento correlato è in genere contrassegnato come *Obsoleto* perché il catalogo live non corrisponde più al contesto del suggerimento.

### Sostituzione manuale in Admin {#manual-override-in-the-admin}

Se si modifica manualmente il nome o la descrizione del prodotto nell&#39;amministratore [!DNL Adobe Commerce]:

- Il valore Admin vince come sistema di registrazione per quella modifica manuale.
- Il suggerimento di arricchimento è contrassegnato come *Obsoleto*.
- Il flusso di lavoro dei suggerimenti torna allo stato originale per l&#39;elemento in modo da poter ridefinire la linea di base o accettare un nuovo suggerimento se l&#39;analisi viene eseguita nuovamente.

Queste regole ti aiutano a capire se l’arricchimento del catalogo, i feed di acquisizione o le modifiche dell’amministratore sono autorevoli quando più canali toccano la stessa SKU.

## Limiti e considerazioni {#limits}

- L’arricchimento si applica solo ai nomi dei prodotti e alle descrizioni lunghe. Non modifica il layout della pagina dei dettagli del prodotto, i widget o altri contenuti della vetrina a livello di pagina.
- Cataloghi di grandi dimensioni e conteggi URL elevati possono influenzare la rapidità con cui viene completata l’analisi e il numero di suggerimenti visualizzati contemporaneamente.
- Suggerimenti significativi presuppongono che i bot rilevanti per LLM possano accedere agli URL del prodotto a cui tieni. Regole robot, autenticazione, blocco geografico e personalizzazione intensiva possono ridurre la copertura.

## Best practice {#best-practices}

- Documentare la proprietà del sistema per il nome e la descrizione del prodotto in modo che i processi PIM o di feed non entrino involontariamente in conflitto con l’arricchimento del catalogo.
- Coordina con i team SEO e brand prima di applicare titoli o descrizioni in blocco.
- Risincronizza o analizza dopo le principali importazioni del catalogo in modo che i suggerimenti riflettano lo stato corrente del catalogo.

## Esempi

Gli esempi seguenti mostrano come l’arricchimento del catalogo trasforma gli attributi tecnici grezzi in copie di prodotto narrative incentrate sull’acquirente che i moduli LLM possono utilizzare per rispondere alle domande di acquisto.

### Esempio: prodotto a base di caffè con attributi tecnici

Un catalogo di Coffee retailer memorizza solo le specifiche tecniche per un prodotto di chicchi di caffè arrosto medio: varietà di chicchi, regione di origine, metodo di elaborazione, livello di arrosto e gamma di altitudine. Questi campi descrivono il prodotto ma non ne comunicano il valore a un acquirente, quindi un assistente AI ha poco da lavorare quando risponde a una domanda come &quot;quale caffè ha un sapore liscio e a basso contenuto acido?&quot;

L’arricchimento del catalogo legge gli attributi tecnici e i motivi attraverso il modo in cui interagiscono per dedurre le caratteristiche rilevanti per l’acquirente:

| Attributo tecnico | Caratteristica dedotta | Ragionamento |
| --- | --- | --- |
| Miele processo, Medium arrosto | Bassa acidità | La mucillagine di frutta lasciata sul fagiolo durante la lavorazione del miele sopprime l&#39;acidità, e la torrefazione media scompone i composti acidi residui. |
| processo del miele, Arabica, arrosto Medium | Aroma di nocciola | Gli zuccheri di frutta della mucillagine si combinano con le note naturali di Arabica, amplificate a media arrostimento. |
| processo del miele, Arabica | Bocca ricca e cremosa | Gli oli assorbiti dalla mucillagine durante l&#39;essiccazione aggiungono viscosità e corpo. |
| Processo del miele, altitudine 900-1200m | Sottotoni in caramello | I fagioli più densi e ad alta quota sviluppano zuccheri più complessi, resi più profondi dalla lavorazione del miele. |

L’arricchimento del catalogo applica le seguenti caratteristiche dedotte alla copia del prodotto:

- **Prima**: &quot;Medium chicchi di caffè arrosto - Arabica, Brasile Minas Gerais, processo del miele, 900-1200m&quot;
- **Dopo**: &quot;I fagioli Arabica coltivati a 900-1200m nel Minas Gerais brasiliano, miele lavorato e medio torrefatto, sviluppano un sapore dolce naturale, cremoso con un carattere di nocciola distinto, sottotoni di caramello, e bassa acidità. Un caffè speciale coerente e avvicinabile, meglio sperimentato attraverso versare sopra.&quot;

Il nome e la descrizione aggiornati vengono salvati direttamente nel catalogo Commerce, pertanto la vetrina, i feed LLM e altri canali che leggono tali campi riflettono tutti la stessa copia arricchita.

### Esempio: configurazione di mobili modulari

Un retailer per mobili vende un divano modulare in cui la descrizione del prodotto elenca solo i codici di configurazione e il nome del fabric, ad esempio `6 Standard Seats + 6 Standard Sides in Sapphire Navy Corded Velvet`. Questa scorciatoia è comprensibile per un cliente di ritorno, ma offre all’assistente di intelligenza artificiale un piccolo contesto sul funzionamento del prodotto o su cosa lo rende resistente o confortevole.

L’arricchimento del catalogo espande gli attributi di configurazione e struttura in una descrizione narrativa che spiega cosa fa ogni componente e perché è importante per l’acquirente:

- **Prima**: &quot;6 Posti Standard + 6 Lati Standard in Velluto Cordato Sapphire Navy&quot;
- **Dopo**: &quot;Questa configurazione include 6 set di inserimento posti standard e 6 inserti laterali standard che funzionano in modo intercambiabile come braccia o schienali, formando gli elementi modulari del layout. Ogni sedile è dotato di Schiuma standard con tre strati ad alta densità progettati per preservare l&#39;sollevamento e resistere alle cadute. La copertina Sapphire Navy Corded Velvet è durevole come è lussuosa, con corde testurizzate che creano un sottile lucentezza e una sensazione morbida e peluche. Le coperture sono cucite a mano per un aspetto preciso e personalizzato e sono lavabili in lavatrice e modificabili, in modo che la sezione possa evolvere con il tuo spazio.&quot;

Poiché la descrizione arricchita viene scritta nuovamente nel catalogo Commerce, è disponibile per i bot AI che scansionano la pagina dei dettagli del prodotto e per qualsiasi canale o feed a valle che consuma i dati del catalogo del prodotto, senza modificare il layout o la progettazione visualizzati dagli acquirenti sulla pagina.
