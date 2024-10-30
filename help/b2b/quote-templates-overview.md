---
title: Casi d’uso e flussi di lavoro per i modelli di preventivo
description: Creare un modello di preventivo da un preventivo esistente per semplificare la negoziazione dei preventivi per gli ordini ricorrenti.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Caso di utilizzo e flussi di lavoro dei modelli di preventivo

La funzionalità Modello preventivo consente a buyer e venditori di semplificare il processo di creazione dei preventivi creando modelli riutilizzabili e personalizzabili.

- **Preventivi personalizzabili** - Gli acquirenti possono generare preventivi collegati da un modello preapprovato, consentendo la personalizzazione all&#39;interno di parametri specifici quali quantità di voci e selezioni.
- **Soglie ordini**: i venditori possono impostare impegni di ordine minimo e massimo, garantendo che gli acquirenti rispettino i volumi di acquisto concordati.
- **Date scadenza** - I modelli possono avere periodi di validità, assicurando che i termini siano applicabili solo entro un intervallo di tempo specificato.
- **Sconti e determinazione prezzi**- I venditori possono utilizzare le stesse funzionalità di sconto per articolo di linea, preventivo e prezzo di spedizione disponibili con i preventivi per impostare sconti per ordini ricorrenti, semplificando il processo di negoziazione.
- **Tracciamento e reporting** - Il sistema tiene traccia del numero di preventivi collegati generati dal modello e degli ordini completati correttamente per fornire informazioni approfondite sull&#39;evasione delle quote di ordini concordate.

## Caso d’uso

Un acquirente aziendale può utilizzare un modello di preventivo per ordinare un set specifico di prodotti in un periodo di tempo. L&#39;acquirente configura le seguenti opzioni del modello di preventivo per rendere il processo di offerta più efficiente, coerente e allineato con i contratti di acquisto strategici.

- Soglia ordine per specificare il numero minimo e massimo di ordini idonei per la determinazione dei prezzi negoziati. Può essere utilizzato per applicare e tenere traccia delle quote degli ordini specificate nei contratti.

- Soglie quantità (quantità minime/massime) Il modello specifica una soglia di quantità per impostare la quantità minima e massima che può essere acquistata per ogni ordine, garantendo al venditore la possibilità di gestire in modo efficace i livelli di scorte e al contempo offrendo al buyer la flessibilità necessaria per adeguare le quantità.

## Flusso di lavoro per modello di preventivo

I modelli di preventivo possono essere avviati dall&#39;acquirente o dal venditore.

**Passaggio 1: creazione modello di preventivo (nuovo)**

- **L&#39;acquirente crea il modello di preventivo**

  Quando rivede un modello di preventivo esistente, l&#39;acquirente decide che l&#39;azienda deve inviare più ordini nel corso dell&#39;anno successivo e desidera richiedere ulteriori sconti in base alla ripetizione dell&#39;attività. Creano un modello di preventivo utilizzando l&#39;azione *[!UICONTROL Create quote template]* nel preventivo. Quindi, avviano la negoziazione inviando il nuovo modello al venditore per la revisione.

  Gli acquirenti possono anche creare un modello di preventivo direttamente dalla pagina *[!UICONTROL My Quote Templates]** della vetrina.

- **Rappresentante commerciale**: un rappresentante commerciale può creare un modello di preventivo dall&#39;amministratore per conto di un acquirente aziendale specifico. Il rappresentante commerciale può creare il modello di preventivo nell&#39;amministratore da un preventivo esistente o dalla griglia [!UICONTROL Quote Templates] e salvarlo come `draft` oppure inviarlo all&#39;acquirente per avviare la negoziazione. In stato di bozza, il preventivo è visibile solo al venditore. Dopo l&#39;invio del preventivo, lo stato è `Submitted`. Non può essere modificato dal venditore finché l&#39;acquirente non lo rispedisce indietro.

  ![Venditore che avvia un preventivo dell&#39;acquirente dalla griglia Preventivi nell&#39;Amministratore](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**Passaggio 2: revisione e negoziazione preventivo (revisione)**

La revisione o la negoziazione di un modello di preventivo può includere la modifica delle quantità, la rimozione di articoli, l&#39;aggiunta di commenti alle voci, l&#39;applicazione di sconti alle voci o ai preventivi (venditore) e l&#39;aggiunta di un indirizzo di spedizione (buyer).

- **Il venditore visualizza la richiesta e invia la risposta**. In Amministratore, il venditore visualizza il modello di preventivo dalla griglia *[!UICONTROL Quote Templates]** o lo apre dal collegamento nella notifica e-mail. Nella vetrina, lo stato del preventivo cambia in `Pending` e l&#39;acquirente non può apportare alcuna modifica. Seguendo lo stesso processo per la [negoziazione del preventivo](quote-price-negotiation.md), il venditore risponde offrendo sconti sui prezzi e adeguando le quantità e gli articoli in base alle esigenze, immette un commento e invia nuovamente il preventivo all&#39;acquirente. L&#39;acquirente e il rappresentante commerciale ricevono una notifica via e-mail che informa che il venditore ha risposto.

- **L&#39;acquirente visualizza il modello di preventivo dal venditore e invia una risposta**. L&#39;acquirente fa clic sul collegamento nella notifica e-mail per aprire il modello di preventivo oppure apre il preventivo dalla pagina _Modelli di preventivo_ del dashboard dell&#39;account. Il buyer può lasciare note al venditore a livello di articolo linea o preventivo, modificare le quantità e rimuovere gli articoli.

Il buyer e il venditore continuano il processo di negoziazione fino al raggiungimento di un accordo o fino al rifiuto del modello di preventivo da parte del venditore. Se l&#39;acquirente apporta modifiche al preventivo, ovvero aggiungendo o rimuovendo prodotti o modificando quantità di prodotti, il preventivo deve essere restituito al venditore per la revisione.

- **L&#39;acquirente aggiunge un indirizzo di spedizione**. L&#39;acquirente deve aggiungere un indirizzo di spedizione al modello di preventivo se non ne dispone. Dopo che l&#39;acquirente ha aggiunto l&#39;indirizzo, il venditore può fornire le opzioni di spedizione e consegna. I metodi di spedizione visualizzati dipendono dalla configurazione Storefront.

Se il buyer aggiunge un indirizzo di spedizione, l&#39;accordo di negoziazione deve essere rivisto e il venditore può continuare il processo di negoziazione fino a quando non viene raggiunto un accordo o il venditore rifiuta il modello di preventivo.

**Passaggio 3: l&#39;acquirente accetta il modello di preventivo**

L&#39;acquirente accetta le condizioni negoziate nel modello. Dopo l&#39;accettazione del modello di preventivo, il buyer può utilizzarlo per generare preventivi collegati preapprovati che possono essere utilizzati per sottomettere ordini senza richiedere ulteriori negoziazioni.

Le opzioni di spedizione sono bloccate al momento del pagamento.

### Visualizzare un modello di preventivo

1. Nella colonna **[!UICONTROL Actions]** per un record, fare clic su **[!UICONTROL View]**.

1. Per rispondere alla richiesta del cliente, seguire le istruzioni e avviare lo stesso processo di [negoziazione dei prezzi](quote-price-negotiation.md) utilizzato per la negoziazione dei preventivi.

### Visualizza attività modello di preventivo

Visualizzare la sequenza temporale della negoziazione, la comunicazione e altre attività del preventivo da [!UICONTROL Comments] e [!UICONTROL History Log]. Le informazioni includono le modifiche di stato, gli aggiornamenti alle informazioni sul cliente e sulla spedizione, gli aggiornamenti su articolo e prezzo e altre informazioni importanti.

1. Aprire un modello di preventivo.

1. Visualizzare i commenti e la cronologia delle negoziazioni dei preventivi scorrendo fino a **[!UICONTROL Negotiation]** e selezionando **[!UICONTROL Comments]** e **[!UICONTROL History Log]**.

   ![Visualizza cronologia](./assets/quote-view-history.png){width="400"}

1. La cronologia viene anche tracciata a livello di elemento riga.

   ![Visualizza cronologia elemento riga](./assets/quote-view-line-item-history.png){width="400"}


### Rifiuta un modello di preventivo

Solo i modelli di preventivo con stato `In Review` possono essere rifiutati.

1. Dalla griglia *[!UICONTROL Quote Templates]*, aprire il modello di preventivo che si desidera rifiutare.

1. Nel modello di preventivo, fare clic su **[!UICONTROL Decline]**.

1. Quando richiesto, immettere il motivo del rifiuto e fare clic su **[!UICONTROL Confirm]**.
