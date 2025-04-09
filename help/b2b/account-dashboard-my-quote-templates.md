---
title: '[!UICONTROL My Quote Templates]'
description: Scopri l’esperienza del cliente per i modelli di preventivo, disponibili nella dashboard dell’account storefront.
feature: B2B, Companies, Quotes
exl-id: 3d95a44e-b874-442b-af96-0dc6b589d0f7
source-git-commit: 15f85631741859280450ae1b477e2f3859c42773
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# [!UICONTROL My Quote Templates]

Se i preventivi sono abilitati, nella sezione _[!UICONTROL My Quotes Template]_del dashboard dei conti cliente vengono elencati tutti i modelli di preventivo associati al conto cliente. A seconda delle autorizzazioni, solo gli acquirenti che effettuano acquisti per conto di una società possono richiedere un modello di preventivo e negoziare prezzi e condizioni per gli ordini ricorrenti.

![Modelli di offerta personali](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

L&#39;elenco dei modelli di preventivo organizza i modelli per stato.

- **[!UICONTROL Active Quote Templates]** elenca i modelli negoziati e approvati per l&#39;utilizzo. Le informazioni includono il totale minimo del preventivo e gli ordini effettuati se queste opzioni sono state configurate durante il processo di negoziazione. Gli acquirenti possono generare un preventivo collegato dal modello per inviare un ordine in base alle condizioni del preventivo.

- **[!UICONTROL In Review]** elenca i modelli nel processo di negoziazione che mostrano lo stato corrente e forniscono un collegamento per aprire il modello.

- **[!UICONTROL Inactive]** elenca i modelli scaduti, annullati o non più validi perché un acquirente ha esaurito il numero di ordini impegnati consentiti.

Per l&#39;acquirente, la pagina *[!UICONTROL My Quotes Templates]* è il punto focale per tutte le comunicazioni tra l&#39;acquirente e il venditore durante il processo di negoziazione.

Un acquirente che accetta le condizioni negoziate offerte dal venditore può accettare il modello e quindi utilizzarlo per generare preventivi collegati pre-approvati che possono essere utilizzati per effettuare ordini.

- Azioni relative alla gestione del modello di preventivo:

   - Annullare un modello
   - Invia al venditore per la revisione
   - Accetta il modello di preventivo
   - Modificare la data di scadenza del modello di preventivo
   - Aggiungi un indirizzo di spedizione
   - Gestisci collegamenti documenti di riferimento

- Azioni per l&#39;aggiornamento dei dettagli del modello di preventivo durante il processo di negoziazione:

   - Rivedi gli aggiornamenti e i prezzi degli articoli.
   - Se nel modello di preventivo sono state configurate soglie di quantità, regolare i valori minimo e massimo.
   - Tenere traccia del processo di negoziazione dalle sezioni [!UICONTROL Comments] e [!UICONTROL History].
   - Per i modelli ancora in fase di revisione, l&#39;acquirente può modificare il modello di preventivo rimuovendo gli elementi.
   - Comunica e negozia con il venditore aggiungendo note a livello di articolo e preventivo.
   - Aggiungere, modificare o rimuovere collegamenti al documento di riferimento a contratti e accordi esterni.

  Dopo aver apportato le modifiche, l&#39;acquirente restituisce il modello al venditore per la revisione.

- Azioni generali durante la negoziazione:

   - Invia modello di offerta al venditore per la revisione
   - Accetta il modello di preventivo
   - Annulla per terminare la negoziazione e chiudere il preventivo

Nell&#39;esempio seguente viene illustrato un modello di preventivo che è stato aggiornato dall&#39;acquirente e inviato nuovamente al venditore per la revisione.

![Visualizzazione acquirente del modello di preventivo](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

I modelli con lo stato `Submitted` vengono bloccati finché il venditore non rivede e aggiorna il modello e lo restituisce all&#39;acquirente.

## Creare un modello di preventivo

Il buyer può avviare il processo di negoziazione del modello di preventivo utilizzando uno dei metodi seguenti:

- Creare un modello da un preventivo esistente facendo clic sull&#39;azione **[!UICONTROL Create quote template]**.

- Inviare una richiesta di preventivo dallo storefront e aggiungere commenti che richiedano al rappresentante commerciale di creare un modello di preventivo dalla richiesta di preventivo.

## Visualizzare un modello di preventivo

1. L&#39;acquirente effettua l&#39;accesso al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL My Quote Templates]**.

1. Trova il modello di preventivo nell&#39;elenco e fa clic su **[!UICONTROL View]** nella colonna _[!UICONTROL Action]_.

## Aggiungi un indirizzo di spedizione

L&#39;acquirente non può accettare un modello di preventivo finché non dispone di un indirizzo di spedizione.

1. L&#39;acquirente effettua l&#39;accesso al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL My Quote Templates]**.

1. Seleziona il modello di preventivo desiderato.

1. Nella sezione **[!UICONTROL Shipping Information]**, fa clic su **[!UICONTROL Add New Address]**.

1. Compila i dettagli per il nuovo indirizzo.

1. Clic su **[!UICONTROL Save Address]**.

Dopo che l&#39;acquirente ha aggiunto l&#39;indirizzo, invia il modello al venditore per la revisione. Il venditore fornisce le opzioni di spedizione e consegna. Questi aggiornamenti possono influire sui prezzi delle offerte negoziate. Le opzioni di spedizione sono bloccate al momento del pagamento.

## Genera un&#39;offerta collegata

Dopo che l&#39;acquirente ha accettato un modello di preventivo, può utilizzarlo per generare preventivi collegati preapprovati da *[!UICONTROL My Quote Templates dashboard]* o dal modello di preventivo utilizzando l&#39;azione **[!UICONTROL Generate a quote]**.

Il preventivo collegato include una notifica che indica che è approvato e pronto per il pagamento. Fornisce inoltre un collegamento al modello di preventivo nelle informazioni di intestazione.

![Offerte collegate generate da un modello di preventivo](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

Se il modello di preventivo è stato configurato con una soglia dell&#39;ordine, il conteggio viene incrementato quando viene generata l&#39;offerta collegata.

Gli acquirenti possono completare le seguenti azioni da un preventivo collegato:

- Se l&#39;offerta è configurata con soglie di quantità, adeguare la quantità dell&#39;ordine per le voci.
- Procedi al pagamento per inviare un ordine.
- Eliminare o stampare il preventivo.
- Aprire il modello di preventivo utilizzato per generare il preventivo.

## Annullare un modello di preventivo

Dalla pagina del modello di preventivo, fare clic su **[!UICONTROL Cancel Quote Template]**.

Il modello di preventivo è stato annullato e lo stato del preventivo cambia in `Closed`. Le virgolette chiuse rimangono nell&#39;elenco di *[!UICONTROL Inactive]* e rimangono elencate nella griglia _[!UICONTROL Quote Templates]_dell&#39;amministratore.

## Gestisci collegamenti documenti di riferimento

La funzione dei collegamenti ai documenti di riferimento consente a buyer e venditori di aggiungere, modificare e gestire i collegamenti a documenti esterni, ad esempio contratti, accordi o specifiche, durante il processo di creazione del modello di preventivo.

### Aggiungi un collegamento al documento di riferimento

1. Aprire il modello di preventivo.

1. Nella sezione **[!UICONTROL Reference Documents]**, fare clic su **[!UICONTROL Add]**.

1. Nella finestra di dialogo Informazioni documento:
   - Immetti **[!UICONTROL Document Name]** (obbligatorio)
   - Immetti **[!UICONTROL Document Identifier]** (facoltativo)
   - Immetti **[!UICONTROL Reference Document URL]** (obbligatorio)

1. Fare clic su **[!UICONTROL Add to Quote Template]**.

   Il collegamento al documento di riferimento viene aggiunto al modello di preventivo con il seguente formato:
   `Document Name, Document Identifier https://document-url`

### Modificare un collegamento a un documento di riferimento

1. Aprire il modello di preventivo.

1. Nella sezione **[!UICONTROL Reference Documents]**, fare clic su **[!UICONTROL Edit]** accanto al collegamento del documento che si desidera modificare.

1. Aggiorna le informazioni del documento nella finestra di dialogo:
   - Nome documento
   - Identificatore documento
   - URL documento di riferimento

1. Fare clic su **[!UICONTROL Add to Quote Template]**.

### Rimuovere un collegamento a un documento di riferimento

1. Aprire il modello di preventivo.

1. Nella sezione **[!UICONTROL Reference Documents]**, fare clic su **[!UICONTROL Remove]** accanto al collegamento del documento che si desidera eliminare.

### Visualizzare un documento di riferimento

1. Aprire il modello di preventivo.

1. Nella sezione **[!UICONTROL Reference Documents]** fare clic sul collegamento del nome del documento.

   Il documento viene aperto in una nuova finestra del browser.

### Limitazioni dei collegamenti ai documenti di riferimento

- I collegamenti ai documenti di riferimento possono essere aggiunti, modificati o rimossi solo quando il modello di preventivo è in uno stato modificabile.
- Una volta inviato o accettato il modello di preventivo, i collegamenti del documento di riferimento diventano di sola lettura.
- Il campo Nome documento è obbligatorio quando si aggiunge o si modifica un collegamento a un documento di riferimento.
- I collegamenti ai documenti di riferimento rimangono accessibili anche dopo l&#39;accettazione o il completamento del modello di preventivo.
