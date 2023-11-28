---
title: Flusso di lavoro ed elaborazione degli ordini
description: Scopri il flusso di lavoro degli ordini, lo stato applicato a ogni passaggio e come spostare gli ordini attraverso questo processo.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1733'
ht-degree: 0%

---

# Flusso di lavoro ed elaborazione degli ordini

Quando un cliente effettua un ordine, viene creato un ordine di vendita come record temporaneo della transazione. Nella griglia Ordini, gli ordini di vendita inizialmente hanno lo stato &quot;In sospeso&quot; e possono essere annullati in qualsiasi momento fino all&#39;elaborazione del pagamento. Dopo la conferma del pagamento, l&#39;ordine può essere fatturato e spedito.

**Passaggio 1: Effettuare un ordine** - Il processo di pagamento inizia quando l&#39;acquirente fa clic su **[!UICONTROL Go to Checkout]** sulla pagina del carrello oppure [riordina](reorders-allow.md) direttamente dal proprio account cliente.

**Passaggio 2: ordine in sospeso** - Lo stato dell&#39;ordine cliente iniziale è `Pending`. In questo stato, il pagamento non è stato elaborato e l’ordine può ancora essere modificato o annullato. Questo stato si verifica quando il metodo di pagamento è configurato per la modalità di autorizzazione.

**Passaggio 3: Ricezione del pagamento** - Lo stato dell’ordine cambia in `Processing` quando il pagamento è ricevuto o autorizzato. A seconda del metodo di pagamento, potresti ricevere una notifica quando la transazione viene autorizzata o elaborata. Questo stato si verifica automaticamente quando il metodo di pagamento è configurato per la modalità acquisizione o vendita intento.

**Passaggio 4: Ordine di fatturazione** - Un ordine viene generalmente fatturato dopo la ricezione del pagamento. Il metodo di pagamento determina le opzioni di fatturazione necessarie per l&#39;ordine. Dopo la generazione e l&#39;invio della fattura, viene inviata una copia al cliente. Se il metodo di pagamento è configurato con `capture` o `intent sale` azione di pagamento, una fattura viene generata automaticamente quando il pagamento viene autorizzato e acquisito.

>[!NOTE]
>
>Le fatture non vengono create automaticamente per gli ordini effettuati utilizzando `Gift Card`, `Store Credit`, `Reward Points`, o altri metodi di pagamento offline.

**Passaggio 5: Registrare una singola spedizione** - Lo stato dell’ordine cambia in `Complete` quando i dettagli della spedizione sono completi, la spedizione viene prenotata e la spedizione impostata. Il requisito di spedizione è soddisfatto con un documento di trasporto stampato e l&#39;etichetta di spedizione o _Notifica pronta per il ritiro_ è selezionato (metodo di consegna in-store). Il cliente riceve la notifica e il pacchetto viene spedito. Se vengono utilizzati numeri di registrazione, la spedizione può essere tracciata dal conto del cliente.

>[!NOTE]
>
>Per informazioni dettagliate sullo stato degli ordini e sulle opzioni di configurazione del metodo di pagamento, consulta [Stato ordine](order-status.md) e [Pagamenti](payments.md).

## Visualizza un ordine

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Trovare l&#39;ordine nella griglia.

1. In _[!UICONTROL Action]_, fare clic su **[!UICONTROL View]**.

1. Verifica stato ordine:

   - A `Pending` l&#39;ordine può essere modificato, sospeso, annullato o fatturato e spedito.

   - A `Processing` l&#39;ordine non può più essere modificato o annullato in modo sostanziale, ma è possibile modificare l&#39;indirizzo di fatturazione e di spedizione.

   - A `Completed` l&#39;ordine può essere riordinato.

L’e-mail del cliente può essere modificata in qualsiasi punto del flusso di lavoro dell’ordine modificando il cliente. Non è possibile modificare l&#39;e-mail se l&#39;ordine è stato effettuato da un ospite.

Il pannello sinistro di un ordine aperto consente di accedere a diversi tipi di informazioni correlate all’ordine.

![Visualizza ordine](./assets/order-view.png){width="700" zoomable="yes"}

## Elabora un ordine

Quando un cliente effettua un ordine, viene creato un ordine di vendita come record temporaneo della transazione. Lo stato dell&#39;ordine cliente è `Pending` fino alla ricezione del pagamento. In `Pending` stato, gli ordini possono essere modificati o annullati fino al momento della ricezione del pagamento e della generazione della fattura. Un modo semplice di pensare è che gli ordini diventano fatture, e le fatture diventano spedizioni. La griglia Ordini elenca tutti gli ordini, indipendentemente dalla loro posizione nel flusso di lavoro. Per scoprire come aiutare i clienti con un ordine, consulta [Aggiornare un ordine](order-update.md).

![Ordini](./assets/orders-grid.png){width="700" zoomable="yes"}

Per aprire un `Pending` ordina, fai clic su **[!UICONTROL Edit]** nell’angolo superiore destro.

>[!NOTE]
>
>È possibile modificare gli ordini solo in `Pending` stato. Il pulsante Modifica non è visibile per gli ordini con stato diverso o per gli ordini basati su [offerta negoziata](../b2b/quotes.md).

![Modifica ordine cliente](./assets/order-pending.png){width="600" zoomable="yes"}

Esaminare le sezioni seguenti nell&#39;ordine cliente, utilizzando le descrizioni dei campi come riferimento.

### Descrizioni della vista Ordine

| Linguetta | Descrizione |
|--- |--- |
| [!UICONTROL Information] | Visualizza informazioni dettagliate sull&#39;ordine e sul conto, inclusi gli indirizzi di fatturazione e spedizione, i metodi di pagamento e consegna, gli ordini di articoli, i totali e le note. |
| [!UICONTROL Invoices] | Elenca ogni fattura associata all&#39;ordine. |
| [!UICONTROL Credit Memos] | Elenca ogni nota di accredito associata all&#39;ordine. |
| [!UICONTROL Shipments] | Elenca ogni record di spedizione associato all&#39;ordine. |
| [!UICONTROL Comments History] | Elenca tutte le note correlate all&#39;ordine. |

{style="table-layout:auto"}

>[!NOTE]
>
>Un utente amministratore deve avere **[!UICONTROL Sales / Archive]** [autorizzazioni](../systems/permissions-user-roles.md) affinché il loro ambito di ruolo possa visualizzare _Fatture_, _Note di credito_, e _Spedizioni_ ordinare le schede.

### Barra dei pulsanti

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Back]** | Torna alla pagina Ordini senza salvare le modifiche. |
| **[!UICONTROL Cancel]** | Annulla l&#39;ordine cliente. |
| **[!UICONTROL Send Email]** | Invia un&#39;e-mail relativa all&#39;ordine al cliente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Modifica lo stato dell&#39;ordine cliente in `On Hold`. Per rilasciare il blocco dell&#39;ordine cliente, scegliere **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | Crea una fattura dall&#39;ordine di vendita convertendo l&#39;ordine in una fattura. |
| **[!UICONTROL Ship]** | Crea un record di spedizione per l&#39;ordine. |
| **[!UICONTROL Notify Order is Ready for Pickup]** | Viene visualizzato solo quando un ordine viene effettuato come consegna in-store. Notifica al cliente che l&#39;ordine è pronto per il prelievo. |
| **[!UICONTROL Reorder]** | Crea un ordine cliente in base all&#39;ordine corrente. |
| **[!UICONTROL Edit]** | Apre un ordine in sospeso in modalità di modifica. Il pulsante Modifica non è visibile per gli ordini con stato `Processing`, o ordini basati su preventivi negoziati. |

{style="table-layout:auto"}

### Annullare un ordine

È possibile [annulla](order-update.md) ordini non ancora fatturati. A [nota di accredito](credit-memos.md) deve essere emesso se un cliente desidera annullare un ordine dopo la fatturazione (acquisizione del pagamento).

Se un ordine è `Pending` o `Processing` e il pagamento non viene acquisito o non acquisito completamente, puoi [annullare l’ordine](#void-an-order) invece di annullarla.

Per ripristinare un ordine annullato, fare clic su **[!UICONTROL Reorder]** e viene creato un nuovo ordine con lo stato `Pending`.

>[!NOTE]
>
>L’annullamento di un ordine genera anche un annullamento, ma l’annullamento di un ordine non attiva l’annullamento.

### Annullare un ordine

Solo gli ordini cliente non fatturati con stato `Processing`, e un [impostazione di integrazione dei pagamenti di `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions), può essere [annullato](order-update.md#void-a-processing-order). Dopo aver annullato un ordine, puoi annullarlo.

### [!UICONTROL Order and Account Information]

![Informazioni su ordini e account](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Informazioni ordine

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Order Number] | Il numero dell’ordine viene visualizzato nella parte superiore dell’ordine di vendita, seguito da una nota che indica se l’e-mail di conferma è stata inviata. |
| [!UICONTROL Order Date] | La data e l’ora in cui è stato effettuato l’ordine. |
| [!UICONTROL Purchased From] | Indica la visualizzazione del sito Web, del punto vendita e del punto vendita in cui è stato effettuato l&#39;ordine. |
| [!UICONTROL Placed from IP] | Indica l&#39;indirizzo IP del computer da cui è stato effettuato l&#39;ordine. |
| [!UICONTROL Order Placed from Quote] | ![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile con B2B per Adobe Commerce) Indica [preventivo](../b2b/quotes.md) da cui è stato generato l’ordine, se applicabile. Il nome dell&#39;offerta è collegato all&#39;offerta. |

{style="table-layout:auto"}

#### Informazioni account

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Customer Name] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine. Il Nome cliente è collegato al profilo cliente. |
| [!UICONTROL Email] | L’indirizzo e-mail del cliente o dell’acquirente. L’indirizzo e-mail è collegato per aprire un nuovo messaggio e-mail. |
| [!UICONTROL Customer Group] | Il nome del gruppo di clienti o del catalogo condiviso a cui è assegnato il cliente. |
| [!UICONTROL Company Name] | ![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile con B2B per Adobe Commerce) Il nome dell’azienda a cui è associato l’acquirente e per conto della quale viene effettuato l’ordine. Il nome dell’azienda è collegato al [profilo società](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Informazioni indirizzo](./assets/order-address-information.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Billing Address] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine, seguito dall&#39;indirizzo di fatturazione, dal numero di telefono e [IVA](vat.md), se applicabile. Il numero di telefono è collegato alla composizione automatica su un dispositivo mobile. |
| [!UICONTROL Shipping Address] | Il nome della persona alla cui attenzione deve essere spedito l&#39;ordine, seguito dall&#39;indirizzo di spedizione e dal numero di telefono. Il numero di telefono è collegato alla composizione automatica su un dispositivo mobile. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Metodo di pagamento e spedizione](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Payment Information] | Il metodo di pagamento da utilizzare per l’ordine e il numero dell’ordine di acquisto, se applicabile, seguito dalla valuta utilizzata per effettuare l’ordine. Se l&#39;ordine viene addebitato al credito della società utilizzando [Pagamento in acconto](../b2b/enable-basic-features.md#configure-payment-on-account), viene indicato l&#39;importo addebitato sul conto. |
| [!UICONTROL Shipping & Handling Information] | Il metodo di spedizione da utilizzare e le eventuali spese di imballaggio applicabili. |

{style="table-layout:auto"}

### Rivedi articoli ordinati

![Elementi ordinati](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

In **[!UICONTROL Order Total]** eseguire le operazioni seguenti:

1. Immetti un **[!UICONTROL Comment]** da includere nell’ordine.

1. Se desideri inviare il commento via e-mail al cliente, seleziona la **[!UICONTROL Notify Customer by Email]** casella di controllo.

1. Se desideri che il commento sia visibile nel conto del cliente, seleziona la **[!UICONTROL Visible on Storefront]** casella di controllo.

   ![Totale ordine](./assets/order-total.png){width="600" zoomable="yes"}

1. Se si è pronti a fatturare l&#39;ordine, fare clic su **[!UICONTROL Invoice]** e seguire le istruzioni per [creare una fattura](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Product] | Nome del prodotto, SKU e opzioni, se applicabile. |
| [!UICONTROL Item Status] | Indica lo stato dell&#39;elemento. Valore: `Ordered` |
| [!UICONTROL Original Price] | Prezzo di catalogo originale dell&#39;articolo prima degli sconti. |
| [!UICONTROL Price] | Prezzo di acquisto dell&#39;articolo. Questo valore riflette eventuali sconti applicati all’elemento dal catalogo condiviso, se applicabili. |
| [!UICONTROL Qty] | La quantità ordinata. |
| [!UICONTROL Subtotal] | Il subtotale è il prezzo di acquisto moltiplicato per la quantità. |
| [!UICONTROL Tax Amount] | Importo dell&#39;imposta applicata all&#39;articolo come valore decimale. |
| [!UICONTROL Tax Percent] | Percentuale dell&#39;imposta applicata all&#39;articolo espressa in percentuale. |
| [!UICONTROL Discount Amount] | Sconto applicato all&#39;articolo. Il valore dello sconto è zero se l&#39;ordine è basato su un preventivo. |
| [!UICONTROL Row Total] | Totale della voce, incluse le imposte applicabili dovute a livello di prodotto, meno gli sconti. |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Status] | Visualizza lo stato dell&#39;ordine cliente. |
| [!UICONTROL Comment] | Casella di testo utilizzata per immettere un commento per il cliente che accompagna l&#39;ordine. <br/>**[!UICONTROL Notify Customer by Email]**: seleziona la casella di controllo se desideri inviare il commento al cliente come e-mail separata.<br/>**[!UICONTROL Visible on Storefront]** : seleziona la casella di controllo se desideri che il commento sia visibile dall’account del cliente. <br/>**[!UICONTROL Submit Comment]**- Invia il commento e invia per e-mail, se applicabile. |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Shipping & Handling] | Importo addebitato per le spese di spedizione e imballaggio. |
| [!UICONTROL Tax] | Importo dell’imposta applicata all’ordine, se applicabile. |
| [!UICONTROL Grand Total] | Totale ordine. |
| [!UICONTROL Total Paid] | Importo totale pagato per l’ordine, se applicabile. |
| [!UICONTROL Total Refunded] | Importo totale rimborsato dall&#39;ordine, se applicabile. |
| [!UICONTROL Total Due] | Importo totale dovuto. |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) L’importo del credito del negozio disponibile applicato all’ordine, se applicabile. |
| [!UICONTROL Catalog Total Price] | ![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile con B2B per Adobe Commerce) Il prezzo totale degli articoli nel preventivo senza imposte, in base ai prezzi nel catalogo condiviso o nel catalogo standard utilizzato come base del preventivo. Se la valuta di visualizzazione della vetrina è diversa da quella di base, il valore viene visualizzato in entrambe le valute, con la visualizzazione della vetrina tra parentesi quadre. |
| [!UICONTROL Negotiated Discount] | ![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile con B2B per Adobe Commerce) Lo sconto che è il risultato di un preventivo negoziato tra l&#39;acquirente e il venditore. Se la valuta di visualizzazione della vetrina è diversa da quella di base, il valore viene visualizzato in entrambe le valute, con la visualizzazione della vetrina tra parentesi quadre. |
| [!UICONTROL Subtotal] | ![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile con B2B per Adobe Commerce) Il prezzo totale del catalogo meno lo sconto negoziato. |

{style="table-layout:auto"}

## Demo sull’elaborazione degli ordini

Guarda questo video e scopri di più sull’elaborazione e lo stato degli ordini:

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12)
