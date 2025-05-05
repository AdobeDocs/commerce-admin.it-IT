---
title: Negoziazione di un preventivo
description: Scopri sui flussi di lavoro di negoziazione dei preventivi e su come collaborare con gli acquirenti per l'acquisto.
exl-id: 93efbc9d-da4d-4ff8-95c1-13848b68bc38
feature: B2B, Quotes
source-git-commit: ec00288f33af2abb785d1b37dd67aaf1ebe35c06
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 0%

---

# Negoziare un preventivo

Se [nella configurazione sono abilitati](configure-quotes.md) B2B preventivi, la negoziazione dei prezzi può essere avviata da un acquirente autorizzato da un&#39;azienda o da un rappresentante di vendita.

Gli acquirenti avviano [il processo di negoziazione dei prezzi richiedendo un preventivo](quote-request.md) dal carrello. I rappresentanti commerciali possono avviare la negoziazione [creando un preventivo provvisorio per un acquirente](sales-rep-initiates-quote.md), aggiornando il preventivo con gli articoli dell&#39;ordine e i prezzi iniziali e inviandolo all&#39;acquirente.

Quando inizia la negoziazione dei prezzi, i preventivi sono elencati nella griglia [Preventivi](quotes.md). Tutte le negoziazioni tra l&#39;acquirente e il venditore si svolgono per e-mail e vengono avviate e tracciate dalla vista dettagliata del preventivo.

Durante il processo di negoziazione, il venditore può effettuare le seguenti operazioni dall&#39;amministratore:

- Aggiungere o rimuovere prodotti
- Modifica la quantità
- Applica uno sconto agli articoli riga o all&#39;intero preventivo
- Aggiungere o modificare il metodo di spedizione
- Aggiungi commenti
- Invia il preventivo aggiornato all&#39;acquirente o salva come bozza

Gli acquirenti gestiscono il processo di negoziazione dei preventivi dalla vetrina utilizzando [[!UICONTROL My Quotes]](account-dashboard-my-quotes.md). Mentre il preventivo è aperto per la revisione, lo stato nel conto dell&#39;acquirente è impostato su `Pending`. L&#39;acquirente può modificare e sottomettere nuovamente il preventivo anche se è stato rifiutato o è scaduto.

## Passaggio 1: Visualizza il richiesta

1. Nella barra laterale Amministratore, vai a **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

   Il nuovo richiesta viene visualizzato nella _[!UICONTROL Quotes]_&#x200B;griglia.

1. Nella colonna _Azioni_ fare clic su **[!UICONTROL View]**.

   ![Nuovo preventivo](./assets/quote-grid-new.png){width="700" zoomable="yes"}

## Passaggio 2: modifica il preventivo

1. In _[!UICONTROL Quote & Account Information]_, fai clic sull&#39;icona Calendario__(![icona](../assets/icon-calendar.png) Calendario).

   ![Informazioni su preventivi e account](./assets/quote-details-account-information.png){width="575" zoomable="yes"}

1. Scegli un **[!UICONTROL Expiration Date]** per il preventivo.

1. Scorri verso il _[!UICONTROL Quote Totals]_&#x200B;basso fino alla sezione e aggiorna la sezione in base alle **[!UICONTROL Negotiated Price]**&#x200B;esigenze.

   ![Aggiorna prezzo negoziato](./assets/quote-change-update-negotiated-price.png){width="600" zoomable="yes"}

   Se il buyer modifica la quantità di articoli nel preventivo, nella parte superiore del preventivo viene visualizzato un avviso che indica che l&#39;elenco degli articoli è stato modificato e che il prezzo negoziato deve essere aggiornato.

   ![Avviso di modifica preventivo](./assets/quote-change-notice.png){width="600" zoomable="yes"}

### Aggiungi nuovi prodotti all&#39;offerta

1. Fare clic su **[!UICONTROL Add Products by SKU]**.

1. Immettere **[!UICONTROL SKU]** e **[!UICONTROL Qty]** da aggiungere.

   ![Aggiungi a preventivo da SKU](./assets/quote-details-add-by-sku.png){width="600" zoomable="yes"}

### Applica aggiornamenti riga

Se necessario, applicare le modifiche all&#39;elemento riga nella sezione _[!UICONTROL Items Quoted]_.

![Applica aggiornamenti elemento riga](./assets/quote-apply-line-item-operations.png){width="600" zoomable="yes"}

- Modifica **[!UICONTROL Quantity]** che deve essere acquistato al prezzo proposto.

- Selezionare **[!UICONTROL Configure]** e modificare le opzioni del prodotto.

  L&#39;opzione [!UICONTROL Configure] è disponibile solo su un elemento di riga per un prodotto configurabile

- Nel menu **[!UICONTROL Action]**, selezionare un&#39;azione per aggiornare l&#39;elemento:
   - **Elemento sconto** per applicare uno sconto come percentuale, importo fisso o prezzo preferito.
Se necessario, è possibile bloccare l&#39;importo dello sconto per evitare ulteriori sconti. Se lo sconto non è bloccato,
sia lo sconto sulla voce che lo sconto a livello di preventivo vengono applicati al prezzo del prodotto.
   - **Lascia una nota all&#39;acquirente** per fornirgli ulteriori informazioni su un oggetto
   - **Rimuovi** per rimuovere un elemento dal preventivo.

### Applica modifiche e aggiornamenti

- Per applicare le modifiche, fare clic su **[!UICONTROL Add to Quote]**.

- Per aggiornare la citazione, fare clic su **[!UICONTROL Recalculate the Quote]**.

- Per applicare le modifiche e aggiornare il preventivo al catalogo condiviso e alle regole di prezzo, fare clic su **[!UICONTROL Update Prices]** e quindi fare clic **[!UICONTROL Proceed]** per confermare l&#39;aggiornamento.

  ![Articoli citati](./assets/quote-detail-items-quoted.png){width="600" zoomable="yes"}

### Aggiorna informazioni di spedizione

1. Se l&#39;acquirente include un indirizzo _Spedisci a_ nel preventivo, fare clic su **[!UICONTROL Get shipping methods and rates]**.

1. Scegli un metodo di spedizione tra le opzioni disponibili.

1. Immetti **[!UICONTROL Proposed Shipping Price]**.

   I _[!UICONTROL Quote Totals]_&#x200B;sono stati aggiornati per riflettere il prezzo di spedizione proposto.

### Allegare un documento di supporto

1. Nella casella _Aggiungi commento_ fare clic su **[!UICONTROL Attach file]**.

   Per impostazione predefinita, [i file allegati](../configuration-reference/sales/quotes.md) possono avere una dimensione massima di 2 MB in uno dei seguenti formati: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG JPEG o PNG.

1. Scegliete il file dalla directory.

## Passaggio 3: aggiornare le informazioni a livello di preventivo e inviare la risposta

1. Nella sezione _[!UICONTROL Negotiation]_&#x200B;della scheda&#x200B;_[!UICONTROL Comments]_, immetti la tua risposta nella sezione **[!UICONTROL Add your comment]**.

1. Per includere un documento di supporto, fare clic su **[!UICONTROL Attach file]** e selezionare il file dalla directory.

   La dimensione massima consentita per gli allegati è 2 MB.

1. Per applicare uno sconto al preventivo:

   - Nella _[!UICONTROL Quote Totals]_&#x200B;sezione scegliere&#x200B;_[!UICONTROL Negotiated Price]_ uno dei seguenti tipi di sconto:

      - `Percentage Discount`: una percentuale di sconto riduce il prezzo originale di una percentuale specifica.
      - `Amount Discount`: uno sconto di importo applica una riduzione del prezzo fisso.
      - `Proposed Price`: uno sconto prezzo proposto imposta il prezzo finale su un importo specifico, indipendentemente dal prezzo originale.

   - Inserire l&#39;importo come percentuale o prezzo fisso.

     ![Commenti di negoziazione](./assets/quote-detail-negotiation-comments.png){width="600" zoomable="yes"}

   - È possibile applicare sconti a ogni voce o preventivo nel suo insieme:

      - **Sconti articoli riga**: gli sconti articoli riga vengono applicati ai singoli articoli nel carrello. Lo sconto può essere un `percentage`, un `amount` specifico o un `proposed price`.
      - **Sconti a livello di carrello**: gli sconti a livello di carrello vengono applicati all&#39;intero carrello. Lo sconto può essere un `percentage` o un `amount` specifico e viene applicato al valore totale del carrello.
      - **Combinazione di sconti per carrello ed elemento riga**: in alcuni casi è possibile applicare sconti sia a livello di carrello che a livello di elemento riga. Lo sconto riga viene applicato per primo, seguito dallo sconto a livello di carrello sul totale rimanente.

1. Invia o salva il preventivo:

   - Se il preventivo è pronto per essere inviato all&#39;acquirente, fare clic su **[!UICONTROL Send]**.

   - Per continuare a lavorare sulla citazione in un secondo momento, fare clic su **[!UICONTROL Save as Draft]**.

>[!NOTE]
>
> Durante la negoziazione del preventivo, gli sconti possono essere bloccati per evitare ulteriori modifiche. Una volta bloccato un preventivo, né il tipo di sconto né l&#39;importo possono essere modificati senza prima sbloccare il preventivo. Questo meccanismo di bloccaggio garantisce il rispetto delle condizioni concordate tra il rappresentante di vendita e l&#39;acquirente.

## Passaggio 4: completare un preventivo

Quando si invia un preventivo, il sistema invia una notifica sia all&#39;acquirente che al rappresentante commerciale che gestisce l&#39;account della società. L&#39;e-mail include un collegamento al preventivo nel conto dell&#39;acquirente e la data di scadenza del preventivo. In qualsiasi momento della negoziazione, l&#39;acquirente può eseguire una delle seguenti operazioni:

- Accetta il preventivo negoziato e completa l&#39;acquisto.
- Invia una risposta con una controproposta e continua la trattativa.
- Termina la trattativa.

Per monitorare la sua posizione nel workflow, controlla la tua email e lo stato del preventivo nella griglia. È possibile continuare il processo di negoziazione per tutto il tempo necessario.

## Barra dei pulsanti

| Pulsante | Descrizione |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Torna alla pagina _[!UICONTROL Quotes]_&#x200B;senza salvare le modifiche. |
| [!UICONTROL Print] | Invia l&#39;offerta a una stampante o la salva come file PDF. |
| [!UICONTROL Create Copy] | Crea e apre una copia del preventivo corrente con `(copy)` aggiunto al nome originale. Rinominare il nuovo preventivo modificando il campo [!UICONTROL Name]. Elabora il nuovo preventivo salvandolo come bozza o inviandolo al cliente. |
| Crea modello | Crea un modello di preventivo basato sul preventivo corrente. I modelli di preventivo semplificano la negoziazione dei preventivi consentendo a buyer e venditori di concordare condizioni di contratto e di determinazione dei prezzi che possono essere applicate a più preventivi. . In base al contratto, il buyer può generare un preventivo collegato preapprovato dal modello per gli ordini successivi anziché riavviare il processo di richiesta di preventivo. |
| [!UICONTROL Save as Draft] | Salva le modifiche apportate al preventivo, ma non inviarlo nuovamente all&#39;acquirente. |
| [!UICONTROL Decline] | Rifiuta la richiesta di negoziare i prezzi, sia nell&#39;indagine iniziale che durante le negoziazioni in corso. Quando un preventivo viene rifiutato, il venditore deve aggiungere un commento per spiegare la decisione. Quando un preventivo viene rifiutato, tutti i prezzi negoziati vengono ripristinati ai valori originali. Questo pulsante viene disattivato mentre il venditore è in attesa di una risposta da parte dell&#39;acquirente. |
| [!UICONTROL Send] | Invia il preventivo aggiornato come risposta alla richiesta dell&#39;acquirente. Questo pulsante è disabilitato se il venditore è in attesa di una risposta da parte dell&#39;acquirente. |

{style="table-layout:auto"}

## Descrizioni dei campi

Le informazioni e le funzioni relative alle quotazioni nell&#39;amministratore sono organizzate nelle seguenti sezioni.

### [!UICONTROL Quote & Account Information]

| Campo | Descrizione |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | Il nome assegnato a una richiesta di preventivo da [buyer](account-company-roles-permissions.md). |
| [!UICONTROL Status] | Indica lo stato corrente dell&#39;offerta. Lo stato di un preventivo può essere modificato solo da un&#39;azione dell&#39;acquirente o del venditore. Consulta anche le [Impostazioni stato](quotes.md) dell&#39;amministratore e dell&#39;account dell&#39;acquirente [&#128279;](account-dashboard-my-quotes.md). |
| [!UICONTROL Created] | La data e l&#39;ora in cui il buyer ha inviato per la prima volta la richiesta di preventivo. |
| [!UICONTROL Created By] | Il nome e il cognome dell&#39;acquirente della società che ha inviato la richiesta di preventivo. |
| [!UICONTROL Expiration Date] | Indica l&#39;ultimo giorno di validità dell&#39;offerta corrente. La data di scadenza predefinita viene impostata nella configurazione come 30 giorni dopo la sottomissione di una richiesta di preventivo da parte di un buyer. <br/><br/>Il venditore può sostituire la data di scadenza predefinita immettendo una data diversa (DD MMM YYYY ) o scegliendo la data dal calendario. Il preventivo non scade mai se il campo viene lasciato vuoto. <br/><br/>Per i preventivi aperti, il venditore riceve una [notifica e-mail](../systems/email-templates.md) 48 ore prima della scadenza pianificata del preventivo. Gli acquirenti vengono informati 24 ore prima della data di scadenza. <br/><br/>Lo stato del preventivo diventa _Scaduto_ e l&#39;acquirente non può apportare ulteriori modifiche al preventivo. I prezzi proposti nell&#39;offerta tornano ai valori originali del catalogo. <br/><br/>Se un preventivo è aperto per la revisione da parte del venditore quando il preventivo è impostato per la scadenza, la data di scadenza viene reimpostata in base all&#39;intervallo impostato nella configurazione. <br/><br/>La data di scadenza è l&#39;unico campo della sezione _Offerta e account_ che può essere modificato durante il processo di revisione. |
| [!UICONTROL Company] | La ragione sociale della [società](account-companies.md) rappresentata dall&#39;acquirente. |
| [!UICONTROL Company Admin Email] | Indirizzo e-mail dell&#39;[amministratore società](account-company-admin.md). |
| [!UICONTROL Sales Rep] | Il [rappresentante commerciale](account-company-manage.md) che lavora per il venditore ed è il contatto principale assegnato all&#39;account aziendale. |
| [!UICONTROL Shared Catalog (or Customer Group)] | [catalogo condiviso](catalog-shared.md) o [gruppo di clienti](account-company-customer-group.md) a cui è assegnata l&#39;azienda. L&#39;offerta potrebbe includere prezzi personalizzati dal catalogo condiviso assegnato alla società. |

{style="table-layout:auto"}

### [!UICONTROL Add to Quote by SKU]

| Campo | Descrizione |
|---------------------------|-----------------------------------------------------------|
| [!UICONTROL Enter SKU] | Il referenza di magazzino del prodotto che deve essere aggiunto al preventivo. |
| [!UICONTROL Qty] | Il numero di articoli di questo referenza di magazzino da aggiungere al preventivo. |
| [!UICONTROL Add to Quote] | Aggiunge al preventivo il quantità del prodotto specificato. |

{style="table-layout:auto"}

### [!UICONTROL Items Quoted]

| Campo | Descrizione |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name & SKU] | Il nome del prodotto collegato e l’unità di gestione delle scorte (SKU). |
| [!UICONTROL Stock] | Il numero di prodotti inclusi in questa SKU attualmente disponibili per la vendita. |
| [!UICONTROL Cost] | Importo pagato dal venditore per acquistare il prodotto. |
| [!UICONTROL Catalog Price] | Il prezzo del prodotto nel catalogo dell&#39;acquirente, in base al gruppo di clienti o al catalogo condiviso assegnato alla società dell&#39;acquirente. |
| [!UICONTROL Cart Price] | Prezzo originale dell&#39;articolo nel carrello, meno eventuali sconti applicati dal carrello. Il prezzo del carrello potrebbe essere diverso dal prezzo del catalogo se sono presenti sconti o regole del carrello applicabili al gruppo di clienti dell&#39;acquirente. |
| [!UICONTROL Discount] | Sconto riga applicato all&#39;articolo. Il valore può essere una percentuale, un importo fisso o un prezzo proposto. |
| [!UICONTROL Qty] | Il numero di unità in questo SKU che è la base per il prezzo quotato. È possibile immettere solo un numero positivo maggiore di zero. Se si desidera azzerare la quantità, eliminare la riga dal preventivo. |
| [!UICONTROL Subtotal] | Il prezzo proposto moltiplicato per il quantità degli articoli ordinati. |
| [!UICONTROL Estimated Tax] | L&#39;importo dell&#39;imposta stimato per questo riga, in base alla configurazione. A seconda delle impostazioni di calcolo dell&#39;imposta, l&#39;imposta stimata può essere basata su uno dei seguenti elementi: Prezzo unitario / Totale riga / Totale |
| [!UICONTROL Subtotal (Incl./Excl. Tax)] | A seconda della configurazione, questa colonna può visualizzare il subtotale con o senza imposte stimate. |
| [!UICONTROL Action] | Menu di selezione delle operazioni che possono essere applicate a una voce di riga:<ul><li>**[!UICONTROL Discount item]**</li><li>**[!UICONTROL Leave a note to Buyer]**</li><li>**[!UICONTROL Remove an item from the quote]**</li></ul>. |
| [!UICONTROL Configure] | Consente di modificare le opzioni prodotto per un prodotto configurabile. |
| [!UICONTROL Update Prices] | Aggiorna il preventivo con le ultime modifiche del catalogo condiviso e delle regole sui prezzi. |
| [!UICONTROL Recalculate Quote] | Ricalcola tutti i prezzi delle offerte, le regole sui prezzi del carrello e le imposte per riflettere le modifiche apportate al preventivo. |

{style="table-layout:auto"}

### [!UICONTROL Shipping Information]

| Campo | Descrizione |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Shipping Address] | Visualizza l&#39;indirizzo di spedizione specificato nell&#39;account dell&#39;acquirente. L&#39;indirizzo di spedizione è vuoto se l&#39;acquirente non ha specificato un indirizzo prima di inviare la richiesta. |
| [!UICONTROL Shipping Method & Price] | Se l&#39;acquirente include un indirizzo _Spedisci a_ nel preventivo, viene visualizzato il collegamento Ottieni tariffe e metodi di spedizione. |

{style="table-layout:auto"}

### [!UICONTROL Negotiation]

| Campo | Descrizione |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Comments] | La scheda Commenti della sezione Negoziazione viene utilizzata per immettere un messaggio all&#39;acquirente relativo al preventivo. <br/>**[!UICONTROL Add your comment]**- I commenti vengono utilizzati per comunicare con l&#39;acquirente durante il processo di negoziazione. Utilizzare i commenti per spiegare eventuali sconti offerti nel preventivo o il motivo per cui una richiesta di preventivo viene rifiutata.<br/>**[!UICONTROL Attach file]** - Le dimensioni massime dei file e i tipi di file supportati per [file allegati](configure-quotes.md) sono determinati dalla configurazione. Per impostazione predefinita, un file allegato può avere una dimensione massima di 2 MB e di uno qualsiasi dei seguenti tipi di file: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG o JPEG, PNG. |
| [!UICONTROL History Log] | In questa scheda viene visualizzata una cronologia completa del preventivo con date, stato del preventivo e commenti. |

{style="table-layout:auto"}

### [!UICONTROL Quote Totals]

| Campo | Descrizione |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Total Cost] | Il costo totale per il venditore degli articoli inclusi nel preventivo. |
| [!UICONTROL Catalog Total Price  (Incl./Excl. Tax)] | Il prezzo totale degli articoli del preventivo senza imposte, in base ai prezzi nel catalogo condiviso o nel catalogo principale utilizzato come base del preventivo. Espandere la sezione per visualizzare i valori utilizzati nel calcolo, a seconda dell&#39;impostazione [Visualizza subtotale](../configuration-reference/sales/tax.md) nella configurazione. Opzioni: <br/>**[!UICONTROL Subtotal (Excl. Tax)]**- Il Prezzo Totale del Catalogo senza imposte stimate.<br/>**[!UICONTROL Subtotal (Incl. Tax)]** - Il Prezzo Totale del Catalogo senza imposte stimate. <br/>**[!UICONTROL Estimated Tax]**- L&#39;importo dell&#39;imposta che si stima si applichi al Prezzo totale del catalogo. |
| Prezzo negoziato | Lo sconto offerto all&#39;acquirente può essere basato su uno dei seguenti elementi: <br/>**[!UICONTROL Percentage Discount]**- Lo sconto in percentuale.<br/>**[!UICONTROL Amount Discount]** - Lo sconto come importo fisso. <br/>**[!UICONTROL Proposed Price]**- Prezzo proposto dal venditore.<p>Se tutti gli articoli del preventivo hanno uno sconto articolo bloccato, la sezione [!UICONTROL Negotiated Price] è disabilitata perché non è possibile applicare ulteriori sconti.</p><p>Se un prodotto ha uno sconto articolo linea non bloccato, sia lo sconto articolo linea che lo sconto a livello di preventivo vengono applicati al prezzo del prodotto.</p> |
| [!UICONTROL Quote Subtotal (Incl./Excl. Tax)] | Il prezzo totale proposto di ogni voce del preventivo, con o senza imposta, a seconda delle impostazioni del [calcolo imposta](../configuration-reference/sales/tax.md) nella configurazione. |
| [!UICONTROL Shipping & Handling] | Importo inserito dal venditore nel campo Prezzo di spedizione proposto nella sezione Informazioni spedizione del preventivo. Se il campo è vuoto, l&#39;importo si basa sul metodo di spedizione selezionato. |
| [!UICONTROL Estimated Tax] | Importo stimato dell&#39;imposta da pagare, come specificato nella configurazione [impostazioni di visualizzazione](../configuration-reference/sales/tax.md). |
| [!UICONTROL Quote Grand Total (Incl. Tax)] | Il totale finale nella parte inferiore del preventivo che include il prezzo negoziato, l&#39;imposta stimata e la spedizione e la movimentazione proposte. |

{style="table-layout:auto"}
