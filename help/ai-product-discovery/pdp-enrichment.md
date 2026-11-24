---
title: Arricchimento della pagina dettagli prodotto
description: Utilizza l'arricchimento della pagina dei dettagli del prodotto [!DNL Adobe Commerce] per rivedere la copia del prodotto suggerita dall'intelligenza artificiale, creare processi di arricchimento e distribuire aggiornamenti approvati per l'individuazione di LLM e AI.
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
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# Arricchimento pagina dettagli prodotto

L’arricchimento della pagina dei dettagli del prodotto (PDP) massimizza la crawlability di LLM su ogni PDP con dati di prodotto strutturati senza apportare alcuna modifica all’esperienza visibile per l’uomo. Questa funzionalità legge il catalogo dei prodotti per creare un payload di dati strutturati per ogni PDP, facilmente leggibile e analizzabile dai moduli LLM.

## Come funziona {#how-it-works}

Il catalogo Adobe Commerce contiene informazioni sui prodotti come attributi, varianti, categorie, prezzi e disponibilità. In un processo di arricchimento PDP, seleziona le pagine di prodotto e i gruppi di dati di catalogo da rendere disponibili agli agenti di intelligenza artificiale. Le informazioni sono organizzate per gli agenti senza modificare l’esperienza della vetrina.

Con l’arricchimento di PDP, puoi:

- Scegli prodotti abilitati specifici con pagine di prodotti live.
- Rivedi un riepilogo delle pagine e dei fatti selezionati prima di salvare o eseguire il processo.
- Visualizza in anteprima le informazioni sul prodotto incluse nell’arricchimento.

| Direzione | Finalità |
| --- | --- |
| Catalogo Commerce -> processo di arricchimento | Seleziona le pagine di prodotti live e i dati di catalogo da includere. |
| Processo di arricchimento -> Agenti di IA | Rendi disponibili le informazioni di prodotto esistenti selezionate in un modulo strutturato. La vetrina visibile umana non cambia. |

## Accedere all’arricchimento di PDP

Prima di iniziare, esaminare i [prerequisiti per l&#39;individuazione dei prodotti AI specifici della distribuzione](prerequisites.md). Dopo aver completato la configurazione per la piattaforma Commerce, apri **[!UICONTROL AI Product Discovery]** nell&#39;amministratore e seleziona **[!UICONTROL Product Details Page Enrichment]**.

## Due percorsi di arricchimento PDP

Esistono due percorsi per ricevere gli arricchimenti PDP:

- **Traffico agente** - Questo tipo di arricchimento viene avviato automaticamente 24-48 ore dopo la configurazione dell&#39;istanza di Commerce e visualizza i risultati nella scheda **Ottimizzazioni**.
- **Gestione arricchimenti** - Questi arricchimenti vengono configurati dal commerciante quando fa clic sul pulsante **[!UICONTROL Create enrichment]** e seleziona manualmente gli SKU da arricchire. Ulteriori informazioni su [Gestione arricchimenti](#create-an-enrichment-job).

## Rivedi attività di arricchimento PDP

La pagina di arricchimento PDP si apre nella scheda **[!UICONTROL Optimizations]**. Utilizza la dashboard per rivedere la copertura dell’arricchimento, l’attività lavorativa e i processi che richiedono attenzione. Utilizza la scheda **[!UICONTROL Settings]** per [collegare](settings.md) l&#39;istanza di Commerce all&#39;individuazione di prodotti AI.

### Trova i lavori che richiedono attenzione

Nella sezione **[!UICONTROL Needs your attention]** sono evidenziati i processi che richiedono un&#39;azione. Una scheda può mostrare il nome del processo, la modalità di selezione dei prodotti, il numero di pagine di prodotto, lo stato del processo e l’avanzamento. Utilizza l’azione disponibile su una scheda per continuare con il processo.

### Cerca tutti i processi

Utilizzare la tabella per cercare e tenere traccia dei processi. Effettua la ricerca per dettagli processo o filtra per stato, inclusi **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]** o **[!UICONTROL Failed]**. Nella tabella sono elencati l&#39;ID, il nome, l&#39;origine, il conteggio delle pagine dei prodotti, la data di inizio, lo stato e le azioni disponibili di ogni processo.

## Creare un processo di arricchimento

In questa sezione imparerai a creare un arricchimento della pagina dei dettagli di un prodotto.

![Crea arricchimento PDP](./assets/create-cat-enrich.png)

1. In **[!UICONTROL Optimizations]**, fare clic su **[!UICONTROL Create enrichment]**.
1. Immetti un nome di **arricchimento**, ad esempio &quot;Black Friday 2026&quot;.
1. Selezionare la **categoria**, ad esempio &quot;Caffè&quot;.
1. Selezionare il **set di attributi**, ad esempio &quot;Accessori&quot;.
1. Selezionare il **tipo di prodotto**, ad esempio &quot;Prodotto semplice&quot;.
1. Selezionare la **fascia di prezzo**.
1. Fare clic su **[!UICONTROL Apply filters]**.

   Puoi visualizzare in anteprima i prodotti che corrispondono ai tuoi criteri di arricchimento e fare clic su **Personalizza** per definire ulteriormente l&#39;ambito dei prodotti che desideri arricchire.

1. Fare clic su **[!DNL Next]** per confermare i prodotti specifici che si desidera arricchire.
1. Fare clic su **[!DNL Run enrichment]**.

   Il processo di arricchimento viene eseguito e visualizzato nella tabella **Ottimizzazioni**. Al termine dell&#39;esecuzione, sarà possibile [rivedere e distribuire](#review-and-deploy-an-enrichment-job) le ottimizzazioni.

### Rivedere un processo di arricchimento {#review-and-deploy-an-enrichment-job}

Aprire un processo di arricchimento.

![Elenco degli URL di arricchimento PDP](./assets/pdp-enrich-urls.png)

Nella tabella **URL con suggerimenti** sono elencati tutti i prodotti con opportunità di arricchimento. Per ogni prodotto è possibile:

- **Espandere la riga** per visualizzare l&#39;analisi di IA e l&#39;arricchimento proposto.
- **Modifica** il nome o la descrizione del prodotto proposto prima di fare domanda, per allinearli alle linee guida per la voce e il merchandising del tuo marchio.
- **Distribuisci l&#39;ottimizzazione** per i prodotti che desideri arricchire e pubblicarla direttamente nella vetrina Adobe Commerce.
- **Contrassegna come Fisso** dopo aver rivisto e applicato l&#39;arricchimento.
- **Ignora** suggerimenti non rilevanti per la strategia del catalogo.

I suggerimenti sono organizzati in tre visualizzazioni: **Suggerimenti correnti**, **Suggerimenti corretti** e **Suggerimenti ignorati**. Una volta applicato un arricchimento, si passa a **Fixed Suggestions** con uno stato di **Applied**. Gli arricchimenti applicati possono essere ripristinati in qualsiasi momento.

### Distribuire l’ottimizzazione

Dopo aver rivisto i suggerimenti e selezionato le pagine dei prodotti da ottimizzare, fai clic su **Distribuisci ottimizzazioni** per pubblicare l&#39;arricchimento utilizzando Ottimizza in Edge. Una finestra di dialogo di conferma della **Distribuzione ad Edge** mostra gli URL del prodotto selezionati, il tipo di ottimizzazione e l&#39;arricchimento applicati. Dopo la distribuzione, una schermata di conferma conferma conferma quali pagine di prodotto sono state ottimizzate correttamente.

L&#39;ottimizzazione viene distribuita esclusivamente agli agenti utente di IA tramite [Ottimizza in Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). I visitatori continuano a vedere la tua esperienza nella vetrina esistente esattamente come prima, senza modifiche alla progettazione PDP, alle prestazioni della pagina o all&#39;esperienza del marchio.

## Limiti e considerazioni {#limits}

- È possibile selezionare solo i prodotti abilitati con una pagina di prodotto live.
- L’arricchimento organizza i fatti già presenti nel catalogo e non aggiunge nuove informazioni sui prodotti.
- Il flusso di lavoro di arricchimento PDP non modifica la vetrina.
- I processi di arricchimento PDP e i processi di arricchimento catalogo hanno scopi e flussi di lavoro diversi.
- L&#39;ottimizzazione PDP utilizza [Ottimizza in Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn).

## Best practice {#best-practices}

- Utilizza nomi di processo chiari che identificano il gruppo di prodotti o la campagna.
- Visualizza in anteprima i fatti inclusi nel processo e conferma che sono accurati e appropriati per gli agenti di intelligenza artificiale.
- Controlla se i prodotti sono già stati arricchiti prima di decidere di saltarli o sovrascriverli.
- Coordinare la sincronizzazione del catalogo e la proprietà dei dati di prodotto con i team responsabili di tali record.

## Esempio: arricchire un prodotto con varianti e specifiche

Una pagina di prodotto contiene spesso più informazioni sul catalogo di quante gli agenti di IA possano leggere. Ad esempio, un commerciante vende uno scarpone da trekking impermeabile. Le opzioni di dimensione, larghezza e colore si trovano in un selettore di varianti che viene caricato con JavaScript. I materiali, gli impermeabilizzatori e le istruzioni di manutenzione si trovano in una scheda Dettagli compressa e la guida di adattamento si apre in un pop-up. Un acquirente può aprire tutti questi elementi, ma un crawler di IA che legge la pagina durante il primo caricamento può visualizzare solo il nome del prodotto, il prezzo e una breve descrizione.

Quando il processo di arricchimento viene eseguito su questo prodotto, prende tutti i dati del catalogo del prodotto, inclusi gli attributi e ogni variante, e li racchiude in un formato strutturato che gli agenti di intelligenza artificiale possono leggere. Un assistente AI può quindi rispondere a domande come &quot;Questo boot è disponibile in un wide fit in dimensione 11?&quot; o &quot;È completamente impermeabile?&quot; dai dati del catalogo del commerciante.

Il processo di arricchimento utilizza solo informazioni già esistenti nel catalogo. Non crea nuovi dati di prodotto e non modifica la pagina di prodotto visualizzata dagli acquirenti.
