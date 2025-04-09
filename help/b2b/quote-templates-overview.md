---
title: Casi d’uso e flussi di lavoro per i modelli di preventivo
description: Creare un modello di preventivo da un preventivo esistente per semplificare la negoziazione dei preventivi per gli ordini ricorrenti.
feature: B2B, Quotes
exl-id: 7d1e7a3d-6c50-416a-b490-0a083e1c06b4
source-git-commit: 6fe8a356ab517fc5dd169c4a6f7ef52937f705c4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Caso di utilizzo e flussi di lavoro dei modelli di preventivo

La funzionalità Modello preventivo consente a buyer e venditori di semplificare il processo di creazione dei preventivi creando modelli riutilizzabili e personalizzabili.

- **Preventivi personalizzabili** - Gli acquirenti possono generare preventivi collegati da un modello preapprovato, consentendo la personalizzazione all&#39;interno di parametri specifici quali quantità di voci e selezioni.
- **Soglie ordini**: i venditori possono impostare impegni di ordine minimo e massimo, garantendo che gli acquirenti rispettino i volumi di acquisto concordati. Dopo che il buyer ha accettato il modello di preventivo, il conteggio della soglia dell&#39;ordine viene incrementato ogni volta che viene generato un preventivo collegato. Se l&#39;offerta collegata viene chiusa senza essere convertita in un ordine, l&#39;ordine viene sottratto dal conteggio delle soglie. Quando viene raggiunta la soglia massima dell&#39;ordine, il modello di preventivo scade.
- **Date scadenza** - I modelli possono avere periodi di validità (*[!UICONTROL Valid Until]*), assicurando che i termini siano applicabili solo entro un intervallo di tempo specificato. Alla scadenza, il modello viene chiuso e tutte le virgolette collegate associate vengono chiuse.
- **Sconti e determinazione prezzi**- I venditori possono utilizzare le stesse funzionalità di sconto per articolo di linea, preventivo e prezzo di spedizione disponibili con i preventivi per impostare sconti per ordini ricorrenti, semplificando il processo di negoziazione.
- **Monitoraggio e reporting**: il sistema tiene traccia del numero di preventivi collegati generati dal modello e degli ordini completati con successo per fornire informazioni dettagliate sull&#39;adempimento delle quote di ordini concordate.
- **Collegamenti** ai documenti di riferimento: sia gli acquirenti che i venditori possono aggiungere, modificare e gestire collegamenti a documenti esterni (ad esempio DocuSign, Adobe Sign o altri servizi online) al modello di offerta. Ciò consente una facile accesso a contratti e accordi correlati durante il processo di modello di preventivo.

## Caso d&#39;uso

Un acquirente di un&#39;azienda può utilizzare un modello di offerta per ordinare un set specifico di prodotti per un periodo di tempo. L&#39;acquirente configura le seguenti opzioni del modello di offerta per rendere il processo di offerta più efficiente, coerente e allineato agli accordi di acquisto strategici.

- L&#39;ordine soglia specificare il numero minimo e massimo di ordini idonei per la negoziazione dei prezzi. Può essere utilizzato per applicare e tenere traccia delle quote degli ordini specificate nei contratti.

- Soglie quantità (quantità minime/massime) Il modello specifica una soglia di quantità per impostare la quantità minima e massima che può essere acquistata per ogni ordine, garantendo al venditore la possibilità di gestire in modo efficace i livelli di scorte e al contempo offrendo al buyer la flessibilità necessaria per adeguare le quantità.

- Collegamenti ai documenti di riferimento per mantenere connessioni con contratti e accordi esterni, semplificando l&#39;accesso alla relativa documentazione durante il processo di offerta.

## Flusso di lavoro per modello di preventivo

I modelli di offerta possono essere avviati dall&#39;acquirente o dal venditore.

**Passaggio 1: creazione del modello di citazione (Nuovo)**

- **L&#39;acquirente crea il modello di preventivo**

  Quando rivede un preventivo esistente, l&#39;acquirente decide che l&#39;azienda deve inviare più ordini nel corso del prossimo anno e desidera richiedere ulteriori sconti in base alla ripetizione dell&#39;attività. Creano un modello di preventivo utilizzando l&#39;azione *[!UICONTROL Create quote template]* nel preventivo. L&#39;acquirente può aggiungere collegamenti al documento di riferimento a contratti o accordi esterni utilizzando il controllo *[!UICONTROL Add]* nella sezione dei documenti di riferimento. Quindi avviano la negoziazione inviando il modello di preventivo al venditore per la revisione.

  Gli acquirenti possono anche richiedere un modello di preventivo aggiungendo i prodotti che desiderano acquistare regolarmente al carrello. Quindi, richiedi un preventivo e indica nei commenti la frequenza con cui desiderano ripetere l’acquisto.

- **Rappresentante commerciale**: un rappresentante commerciale può creare un modello di preventivo dall&#39;amministratore per conto di un acquirente aziendale specifico. Il rappresentante commerciale può creare il modello di preventivo nell&#39;amministratore da un preventivo esistente o dalla griglia [!UICONTROL Quote Templates] e salvarlo come `draft` oppure inviarlo all&#39;acquirente per avviare la negoziazione. In stato di bozza, il preventivo è visibile solo al venditore. Dopo l&#39;invio del preventivo, lo stato è `Submitted`. Non può essere modificato dal venditore finché l&#39;acquirente non lo rispedisce indietro.

  ![Venditore che avvia un preventivo dell&#39;acquirente dalla griglia Preventivi nell&#39;Amministratore](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

  Quando il venditore crea il modello di preventivo, la data di scadenza ([!UICONTROL Valid until] campo data) viene impostata automaticamente su 180 giorni. Se il buyer ha creato il modello, la data di scadenza è vuota.  L&#39;acquirente deve impostare la data di scadenza prima di inviare nuovamente il modello all&#39;acquirente per la revisione.

  Quando il venditore crea il modello di offerta, la data di scadenza (*[!UICONTROL Valid until]* campo data) viene impostata automaticamente su 180 giorni. Se l&#39;acquirente ha creato il modello, la data di scadenza è vuota.  L&#39;acquirente deve impostare la data di scadenza prima di inviare nuovamente il modello all&#39;acquirente per la revisione.

**Passaggio 2: revisione e negoziazione del preventivo (revisione)**

La revisione o la negoziazione di un modello di offerta può includere la modifica delle quantità, la rimozione di articoli, l&#39;aggiunta di commenti riga, l&#39;applicazione di sconti riga o preventivi (venditore), l&#39;aggiunta di un indirizzo di spedizione (acquirente) e la gestione dei collegamenti ai documenti di riferimento.

- **Il venditore visualizza richiesta e invia la risposta** - Nell&#39;amministratore, il venditore visualizza il modello di preventivo dalla *[!UICONTROL Quote Templates]* griglia * o lo apre dal collegare nel notifica email. In vetrina, lo stato dell&#39;offerta cambia in `Pending`, e l&#39;acquirente non può apportare alcuna modifica. Seguendo lo stesso processo per la [negoziazione del preventivo](quote-price-negotiation.md), il venditore risponde offrendo sconti sui prezzi e adeguando le quantità e gli articoli in base alle esigenze, immette un commento e invia nuovamente il modello di preventivo all&#39;acquirente. Il venditore può anche aggiungere, modificare o rimuovere link al documento di riferimento durante questo processo. L&#39;acquirente e il rappresentante commerciale ricevono una notifica via e-mail che informa che il venditore ha risposto.

- **L&#39;acquirente visualizza il modello di offerta dal venditore e invia la risposta** : l&#39;acquirente fa clic sull&#39;collegare nell&#39;notifica e-mail per aprire il modello di offerta o lo apre dalla _pagina I miei modelli_ di preventivo della dashboard di account. L&#39;acquirente può lasciare note al venditore a livello di riga o di preventivo, modificare le quantità, rimuovere articoli e gestire collegamenti a documenti di riferimento.

L&#39;acquirente e il venditore continuano il processo di negoziazione fino al raggiungimento di un accordo o il venditore rifiuta il modello di preventivo. Se l&#39;acquirente apporta modifiche al modello di offerta, ovvero aggiunta o rimozione di prodotti, modifica delle quantità di prodotti o modifica dei collegamenti ai documenti di riferimento, deve essere restituito al venditore per la revisione.

- **L&#39;acquirente aggiunge un indirizzo** di spedizione - L&#39;acquirente deve aggiungere un indirizzo di spedizione al modello di offerta se non ne ha uno. Dopo che l&#39;acquirente ha aggiunto l&#39;indirizzo, il venditore può fornire le opzioni di spedizione e consegna. I metodi di spedizione visualizzati dipendono dalla configurazione Storefront.

Se il buyer aggiunge un indirizzo di spedizione, l&#39;accordo di negoziazione deve essere rivisto e il venditore può continuare il processo di negoziazione fino a quando non viene raggiunto un accordo o il venditore rifiuta il modello di preventivo.

**Passaggio 3: l&#39;acquirente accetta il modello di preventivo**

L&#39;acquirente accetta le condizioni negoziate nel modello. Dopo l&#39;accettazione del modello di preventivo, il buyer può utilizzarlo per [generare preventivi collegati e preapprovati](account-dashboard-my-quote-templates.md#generate-a-linked-quote) che possono essere utilizzati per sottomettere ordini senza richiedere ulteriori negoziazioni.

Le opzioni di spedizione sono bloccate al momento del pagamento.

I modelli di preventivo rimangono attivi fino alla scadenza, all&#39;annullamento o alla chiusura o alla mancata validità dell&#39;acquirente che ha raggiunto il numero massimo d&#39;ordine soglia.

### Visualizza un modello di citazione

1. Nella colonna di **[!UICONTROL Actions]** un record, fare clic su **[!UICONTROL View]**.

1. Per rispondere all&#39;richiesta del cliente, seguire le istruzioni e iniziare lo stesso [processo di negoziazione](quote-price-negotiation.md) dei prezzi utilizzato per negoziare i preventivi.

### Visualizza attività del modello di citazione

Visualizzare la sequenza temporale della negoziazione, la comunicazione e altre attività del modello di preventivo da [!UICONTROL Comments] e [!UICONTROL History Log]. Le informazioni includono le modifiche di stato, gli aggiornamenti alle informazioni sul cliente e sulla spedizione, gli aggiornamenti di articolo e prezzo e altre informazioni importanti.

1. Aprire un modello di preventivo.

1. Visualizzare i commenti e la cronologia delle negoziazioni dei preventivi scorrendo fino a **[!UICONTROL Negotiation]** e selezionando **[!UICONTROL Comments]** e **[!UICONTROL History Log]**.

   ![Visualizza Storia](./assets/quote-view-history.png){width="400" zoomable="yes"}

1. Anche la cronologia viene tracciata a livello riga.

   ![Visualizza Cronologia degli elementi pubblicitari](./assets/quote-view-line-item-history.png){width="400" zoomable="yes"}

### Rifiuta un modello di preventivo

Solo i modelli di preventivo con stato `In Review` possono essere rifiutati.

1. Dalla griglia *[!UICONTROL Quote Templates]*, aprire il modello di preventivo che si desidera rifiutare.

1. Nel modello di preventivo, fare clic su **[!UICONTROL Decline]**.

1. Quando richiesto, immettere il motivo del rifiuto e fare clic su **[!UICONTROL Confirm]**.
