---
title: Negoziazione di un preventivo
description: Scopri i flussi di lavoro per la negoziazione dei preventivi e come lavorare con gli acquirenti per gli acquisti.
exl-id: 93efbc9d-da4d-4ff8-95c1-13848b68bc38
feature: B2B, Quotes
source-git-commit: 734290b9d609a173186325b418cd92cbf41b0efb
workflow-type: tm+mt
source-wordcount: '2021'
ht-degree: 0%

---

# Negoziazione di un preventivo

Se [Quotazioni B2B abilitate](configure-quotes.md) nella configurazione, la negoziazione dei prezzi può essere avviata da un acquirente autorizzato di una società o di un rappresentante commerciale.

Gli acquirenti avviano il processo di negoziazione dei prezzi [richiesta di un preventivo](quote-request.md) dal carrello. I rappresentanti commerciali possono avviare la negoziazione [creazione di un preventivo provvisorio per un acquirente](sales-rep-initiates-quote.md), aggiornando il preventivo con gli articoli dell&#39;ordine e i prezzi iniziali e inviandolo all&#39;acquirente.

Quando inizia la negoziazione del prezzo, i preventivi sono elencati nella [Virgolette](quotes.md) griglia. Tutte le negoziazioni tra l&#39;acquirente e il venditore si svolgono per e-mail e vengono avviate e tracciate dalla vista dettagliata del preventivo.

Durante il processo di negoziazione, il venditore può effettuare le seguenti operazioni dall&#39;amministratore:

- Aggiungere o rimuovere prodotti
- Modifica la quantità
- Applica uno sconto agli articoli riga o al prezzo totale
- Aggiungere o modificare il metodo di spedizione
- Aggiungi commenti
- Invia il preventivo aggiornato all&#39;acquirente o salva come bozza

Gli acquirenti gestiscono il processo di negoziazione dei preventivi dalla vetrina utilizzando [[!UICONTROL My Quotes]](account-dashboard-my-quotes.md). Mentre il preventivo è aperto per la revisione, lo stato nel conto dell&#39;acquirente è impostato su `Pending`. L&#39;acquirente può modificare e sottomettere nuovamente il preventivo anche se è stato rifiutato o è scaduto.

## Passaggio 1: visualizzare la richiesta

1. Nella barra laterale Amministratore, vai a **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

   La nuova richiesta viene visualizzata nel _[!UICONTROL Quotes]_griglia.

1. In _Azioni_ , fare clic su **[!UICONTROL View]**.

   ![Nuova offerta](./assets/quote-grid-new.png){width="700" zoomable="yes"}

## Passaggio 2: modificare il preventivo

1. Sotto _[!UICONTROL Quote & Account Information]_, fare clic su_ Calendario _(![Icona Calendario](../assets/icon-calendar.png)).

   ![Informazioni su preventivo e account](./assets/quote-details-account-information.png){width="575" zoomable="yes"}

1. Scegli un **[!UICONTROL Expiration Date]** per il preventivo.

1. Scorri verso il basso fino a _[!UICONTROL Quote Totals]_e aggiorna il **[!UICONTROL Negotiated Price]**secondo necessità.

   ![Aggiorna prezzo negoziato](./assets/quote-change-update-negotiated-price.png){width="600" zoomable="yes"}

   Se il buyer modifica la quantità di articoli nel preventivo, nella parte superiore del preventivo viene visualizzato un avviso che indica che l&#39;elenco degli articoli è stato modificato e che il prezzo negoziato deve essere aggiornato.

   ![Avviso di modifica preventivo](./assets/quote-change-notice.png){width="600" zoomable="yes"}

### Aggiungi nuovi prodotti all&#39;offerta

1. Clic **[!UICONTROL Add Products by SKU]**.

1. Inserisci il **[!UICONTROL SKU]** e **[!UICONTROL Qty]** da aggiungere.

   ![Aggiungi a preventivo per SKU](./assets/quote-details-add-by-sku.png){width="600" zoomable="yes"}

### Applica aggiornamenti riga

Applicare le modifiche alle voci in _[!UICONTROL Items Quoted]_se necessario.

![Applica aggiornamenti riga](./assets/quote-apply-line-item-operations.png){width="600" zoomable="yes"}

- Modificare il **[!UICONTROL Quantity]** che devono essere acquistati al Prezzo Proposto.

- Seleziona **[!UICONTROL Configure]** e modificare le opzioni del prodotto.

  Il [!UICONTROL Configure] L’opzione è disponibile solo su una riga per un prodotto configurabile

- In **[!UICONTROL Action]** selezionare un&#39;azione per aggiornare l&#39;elemento:
   - **Elemento sconto** per applicare uno sconto come percentuale, importo fisso o prezzo preferito.
Se necessario, è possibile bloccare l&#39;importo dello sconto per evitare ulteriori sconti. Se lo sconto non è bloccato, vengono applicati al prezzo del prodotto sia lo sconto per l&#39;articolo riga che quello a livello di preventivo.
   - **Lascia una nota all&#39;acquirente** per fornire all&#39;acquirente ulteriori informazioni su un oggetto
   - **Rimuovi** per rimuovere un elemento dal preventivo.

### Applica modifiche e aggiorna

- Per applicare le modifiche, fai clic su **[!UICONTROL Add to Quote]**.

- Per aggiornare il preventivo, fare clic su **[!UICONTROL Recalculate the Quote]**.

- Per applicare le modifiche e aggiornare il preventivo al catalogo condiviso e alle regole di prezzo, fare clic su **[!UICONTROL Update Prices]** e quindi fare clic su **[!UICONTROL Proceed]** per confermare l’aggiornamento.

  ![Elementi citati](./assets/quote-detail-items-quoted.png){width="600" zoomable="yes"}

### Aggiorna informazioni di spedizione

1. Se l&#39;acquirente include _Spedisci a_ nell&#39;offerta, fare clic su **[!UICONTROL Get shipping methods and rates]**.

1. Scegli un metodo di spedizione tra le opzioni disponibili.

1. Immetti un **[!UICONTROL Proposed Shipping Price]**.

   Il _[!UICONTROL Quote Totals]_vengono aggiornati per riflettere il prezzo di spedizione proposto.

### Allegare un documento di supporto

1. Sotto _Aggiungi il commento_ , fare clic su **[!UICONTROL Attach file]**.

   Per impostazione predefinita, [file allegati](../configuration-reference/sales/quotes.md) può essere fino a 2 MB in uno qualsiasi dei seguenti formati di file: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG o JPEG, PNG.

1. Scegliete il file dalla directory.

## Passaggio 3: aggiornare le informazioni a livello di preventivo e inviare la risposta

1. In _[!UICONTROL Negotiation]_sezione sul_[!UICONTROL Comments]_ , immettere la risposta nella scheda **[!UICONTROL Add your comment]** sezione.

1. Per includere un documento di supporto, fare clic su **[!UICONTROL Attach file]** e seleziona il file dalla directory.

   La dimensione massima consentita per gli allegati è 2 MB.

1. Per applicare uno sconto all&#39;intero preventivo:

   - Sotto _[!UICONTROL Quote Totals]_nel_[!UICONTROL Negotiated Price]_ sezione, scegliere uno dei tipi di sconto seguenti:

      - `Percentage Discount`
      - `Amount Discount`
      - `Proposed Price`

   - Inserire l&#39;importo come percentuale o prezzo fisso.

     ![Commenti negoziazione](./assets/quote-detail-negotiation-comments.png){width="600" zoomable="yes"}

1. Invia o salva il preventivo:

   - Se il preventivo è pronto per essere inviato all&#39;acquirente, fare clic su **[!UICONTROL Send]**.

   - Per continuare a lavorare sull&#39;offerta in un secondo momento, fare clic su **[!UICONTROL Save as Draft]**.

## Passaggio 4: completare un preventivo

Quando si invia un preventivo, il sistema invia una notifica sia all&#39;acquirente che al rappresentante commerciale che gestisce l&#39;account della società. L&#39;e-mail include un collegamento al preventivo nel conto dell&#39;acquirente e la data di scadenza del preventivo. In qualsiasi momento della negoziazione, l&#39;acquirente può eseguire una delle operazioni seguenti:

- Accettare il preventivo negoziato e completare l&#39;acquisto.
- Inviare una risposta con una controproposta e continuare la negoziazione.
- Terminare la negoziazione.

Per monitorarne la posizione nel flusso di lavoro, controlla l’e-mail e lo stato dell’offerta nella griglia. È possibile continuare il processo di negoziazione per tutto il tempo necessario.

## Barra dei pulsanti

| Pulsante | Descrizione |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Torna a _[!UICONTROL Quotes]_senza salvare le modifiche. |
| [!UICONTROL Print] | Invia l&#39;offerta a una stampante o la salva come file PDF. |
| [!UICONTROL Create Copy] | [!BADGE Funzionalità 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti ai programmi beta"}`(copy)` aggiunta al nome originale. Rinominare la nuova virgoletta modificando [!UICONTROL Name] campo. Elabora il nuovo preventivo salvandolo come bozza o inviandolo al cliente. |
| [!UICONTROL Save as Draft] | Salva le modifiche apportate al preventivo, ma non inviarlo nuovamente all&#39;acquirente. |
| [!UICONTROL Decline] | Rifiuta la richiesta di negoziare i prezzi, sia nell&#39;indagine iniziale che durante le negoziazioni in corso. Quando un preventivo viene rifiutato, il venditore deve aggiungere un commento per spiegare la decisione. Quando un preventivo viene rifiutato, tutti i prezzi negoziati vengono reimpostati sui valori originali. Questo pulsante è disabilitato mentre il venditore è in attesa di una risposta dall&#39;acquirente. |
| [!UICONTROL Send] | Invia il preventivo aggiornato come risposta alla richiesta di informazioni dell&#39;acquirente. Questo pulsante è disattivato se il venditore è in attesa di una risposta da parte dell&#39;acquirente. |

{style="table-layout:auto"}

## Descrizioni dei campi

Le informazioni sui preventivi e le funzioni dell&#39;amministratore sono organizzate nelle sezioni seguenti.

### [!UICONTROL Quote & Account Information]

| Campo | Descrizione |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | Nome assegnato a una richiesta di preventivo da [acquirente](account-company-roles-permissions.md). |
| [!UICONTROL Status] | Indica lo stato corrente dell&#39;offerta. Lo stato di un preventivo può essere modificato solo da un&#39;azione dell&#39;acquirente o del venditore. Consulta anche [Impostazioni di stato](quotes.md) dall’amministratore e dal [account dell&#39;acquirente](account-dashboard-my-quotes.md). |
| [!UICONTROL Created] | La data e l&#39;ora in cui il buyer ha inviato per la prima volta la richiesta di preventivo. |
| [!UICONTROL Created By] | Il nome e il cognome dell&#39;acquirente della società che ha inviato la richiesta di preventivo. |
| [!UICONTROL Expiration Date] | Indica l&#39;ultimo giorno di validità dell&#39;offerta corrente. La data di scadenza predefinita viene impostata nella configurazione come 30 giorni dopo la sottomissione di una richiesta di preventivo da parte di un buyer. <br/><br/>Il venditore può sostituire la data di scadenza predefinita inserendo una data diversa (MMM GG AAAA ) o scegliendo la data dal calendario. Il preventivo non scade mai se il campo viene lasciato vuoto. <br/><br/>Per le quotazioni aperte, il venditore riceve un [notifica e-mail](../systems/email-templates.md) 48 ore prima della scadenza programmata del preventivo. Gli acquirenti vengono informati 24 ore prima della data di scadenza. <br/><br/>Lo stato dell&#39;offerta cambia in _Scaduto_ e l&#39;acquirente non può apportare ulteriori modifiche all&#39;offerta. I prezzi proposti nell&#39;offerta tornano ai valori originali del catalogo. <br/><br/>Se un preventivo è aperto per la revisione da parte del venditore quando il preventivo è impostato per la scadenza, la data di scadenza viene reimpostata in base all&#39;intervallo impostato nella configurazione. <br/><br/>La Data di scadenza è l’unico campo nel _Preventivo e account_ che possono essere modificate durante il processo di revisione. |
| [!UICONTROL Company] | Denominazione sociale del [azienda](account-companies.md) che l&#39;acquirente rappresenta. |
| [!UICONTROL Company Admin Email] | L’indirizzo e-mail del [amministratore società](account-company-admin.md). |
| [!UICONTROL Sales Rep] | Il [rappresentante commerciale](account-company-manage.md) che lavora per il venditore ed è il contatto principale assegnato all&#39;account aziendale. |
| [!UICONTROL Shared Catalog (or Customer Group)] | Il [catalogo condiviso](catalog-shared.md) o [gruppo di clienti](account-company-customer-group.md) a cui è assegnata l’azienda. L&#39;offerta potrebbe includere prezzi personalizzati dal catalogo condiviso assegnato alla società. |

{style="table-layout:auto"}

### [!UICONTROL Add to Quote by SKU]

| Campo | Descrizione |
|---------------------------|-----------------------------------------------------------|
| [!UICONTROL Enter SKU] | SKU del prodotto da aggiungere all&#39;offerta. |
| [!UICONTROL Qty] | Il numero di elementi di questo SKU da aggiungere all&#39;offerta. |
| [!UICONTROL Add to Quote] | Aggiunge all&#39;offerta la quantità del prodotto specificato. |

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
| [!UICONTROL Subtotal] | Il prezzo proposto moltiplicato per la quantità di articoli ordinati. |
| [!UICONTROL Estimated Tax] | L&#39;importo dell&#39;imposta stimato per questa riga, in base alla configurazione. A seconda delle impostazioni di calcolo dell&#39;imposta, l&#39;imposta stimata può essere basata su uno dei seguenti elementi: Prezzo unitario / Totale riga / Totale |
| [!UICONTROL Subtotal (Incl./Excl. Tax)] | A seconda della configurazione, questa colonna può visualizzare il subtotale con o senza imposte stimate. |
| [!UICONTROL Action] | Menu di selezione delle operazioni che possono essere applicate a una voce di riga:<ul><li>**[!UICONTROL Discount item]**</li><li>**[!UICONTROL Leave a note to Buyer]**</li><li>**[!UICONTROL Remove an item from the quote]**</li></ul>. |
| [!UICONTROL Configure] | Consente di modificare le opzioni prodotto per un prodotto configurabile. |
| [!UICONTROL Update Prices] | Aggiorna il preventivo con le ultime modifiche apportate al catalogo condiviso e alle regole di prezzo. |
| [!UICONTROL Recalculate Quote] | Ricalcola tutti i prezzi dei preventivi, le regole del prezzo del carrello e l&#39;imposta per riflettere le modifiche apportate al preventivo. |

{style="table-layout:auto"}

### [!UICONTROL Shipping Information]

| Campo | Descrizione |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Shipping Address] | Visualizza l&#39;indirizzo di spedizione specificato nell&#39;account dell&#39;acquirente. L&#39;indirizzo di spedizione è vuoto se l&#39;acquirente non ha specificato un indirizzo prima di inviare la richiesta. |
| [!UICONTROL Shipping Method & Price] | Se l&#39;acquirente include un&#39;opzione, viene visualizzato il collegamento Ottieni tariffe e metodi di spedizione _Spedisci a_ indirizzo nell&#39;offerta. |

{style="table-layout:auto"}

### [!UICONTROL Negotiation]

| Campo | Descrizione |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Comments] | La scheda Commenti della sezione Negoziazione viene utilizzata per immettere un messaggio all&#39;acquirente relativo al preventivo. <br/>**[!UICONTROL Add your comment]**- I commenti vengono utilizzati per comunicare con l&#39;acquirente durante il processo di negoziazione. Utilizzare i commenti per spiegare eventuali sconti offerti nel preventivo o il motivo per cui una richiesta di preventivo viene rifiutata.<br/>**[!UICONTROL Attach file]** - Dimensione massima del file e tipi di file supportati per [file allegati](configure-quotes.md) sono determinati dalla configurazione. Per impostazione predefinita, un file allegato può avere una dimensione massima di 2 MB e può essere di uno qualsiasi dei seguenti tipi di file: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG o JPEG, PNG. |
| [!UICONTROL History Log] | In questa scheda viene visualizzata una cronologia completa del preventivo con date, stato del preventivo e commenti. |

{style="table-layout:auto"}

### [!UICONTROL Quote Totals]

| Campo | Descrizione |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Total Cost] | Il costo totale per il venditore degli articoli inclusi nel preventivo. |
| [!UICONTROL Catalog Total Price  (Incl./Excl. Tax)] | Il prezzo totale degli articoli del preventivo senza imposte, in base ai prezzi nel catalogo condiviso o nel catalogo principale utilizzato come base del preventivo. Espandere la sezione per visualizzare i valori utilizzati nel calcolo, a seconda della [Visualizza subtotale](../configuration-reference/sales/tax.md) nella configurazione. Opzioni: <br/>**[!UICONTROL Subtotal (Excl. Tax)]**- Il prezzo totale del catalogo senza imposta stimata.<br/>**[!UICONTROL Subtotal (Incl. Tax)]** - Il prezzo totale del catalogo senza imposta stimata. <br/>**[!UICONTROL Estimated Tax]**- L&#39;importo dell&#39;imposta che si prevede di applicare al prezzo totale del catalogo. |
| Prezzo negoziato | Lo sconto offerto all&#39;acquirente può essere basato su uno dei seguenti elementi: <br/>**[!UICONTROL Percentage Discount]**- Sconto espresso in percentuale.<br/>**[!UICONTROL Amount Discount]** - Lo sconto come importo fisso. <br/>**[!UICONTROL Proposed Price]**- Il prezzo proposto dal venditore.<p>Se tutti gli articoli del preventivo hanno uno sconto articolo bloccato, il [!UICONTROL Negotiated Price] La sezione è disabilitata perché non è possibile applicare ulteriori sconti.</p><p>Se un prodotto ha uno sconto articolo linea non bloccato, sia lo sconto articolo linea che lo sconto a livello di preventivo vengono applicati al prezzo del prodotto.</p> |
| [!UICONTROL Quote Subtotal (Incl./Excl. Tax)] | Il prezzo totale proposto di ogni voce del preventivo, con o senza imposta, a seconda della [calcolo delle imposte](../configuration-reference/sales/tax.md) nella configurazione. |
| [!UICONTROL Shipping & Handling] | Importo inserito dal venditore nel campo Prezzo di spedizione proposto nella sezione Informazioni spedizione del preventivo. Se il campo è vuoto, l&#39;importo si basa sul metodo di spedizione selezionato. |
| [!UICONTROL Estimated Tax] | L&#39;importo dell&#39;imposta che si stima sia dovuto, come specificato nella configurazione [impostazioni di visualizzazione](../configuration-reference/sales/tax.md). |
| [!UICONTROL Quote Grand Total (Incl. Tax)] | Il totale finale nella parte inferiore del preventivo che include il prezzo negoziato, l&#39;imposta stimata e la spedizione e la movimentazione proposte. |

{style="table-layout:auto"}
