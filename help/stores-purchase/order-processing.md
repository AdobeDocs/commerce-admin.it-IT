---
title: Flusso di lavoro ed elaborazione degli ordini
description: Scopri il flusso di lavoro degli ordini, lo stato applicato a ogni passaggio e come spostare gli ordini attraverso questo processo.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 82f040fa34cf96af6f1e9752f8d9f1ddeab9f84c
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# Flusso di lavoro ed elaborazione degli ordini

Quando un cliente effettua un ordine, viene creato un ordine di vendita come record temporaneo della transazione. Nella griglia Ordini, gli ordini di vendita inizialmente hanno lo stato &quot;In sospeso&quot; e possono essere annullati in qualsiasi momento fino all&#39;elaborazione del pagamento. Dopo la conferma del pagamento, l&#39;ordine può essere fatturato e spedito.

**Passaggio 1: Ordina** - Il processo di pagamento inizia quando l&#39;acquirente fa clic su **[!UICONTROL Go to Checkout]** nella pagina del carrello o [riordina](reorders-allow.md) direttamente dal proprio account cliente.

**Passaggio 2: ordine in sospeso**. Lo stato iniziale dell&#39;ordine di vendita è `Pending`. In questo stato, il pagamento non è stato elaborato e l’ordine può ancora essere modificato o annullato. Questo stato si verifica quando il metodo di pagamento è configurato per la modalità di autorizzazione.

**Passaggio 3: ricezione pagamento** - Lo stato dell&#39;ordine diventa `Processing` quando il pagamento viene ricevuto o autorizzato. A seconda del metodo di pagamento, potresti ricevere una notifica quando la transazione viene autorizzata o elaborata. Questo stato si verifica automaticamente quando il metodo di pagamento è configurato per la modalità acquisizione o vendita intento.

**Passaggio 4: ordine di fatturazione** - Un ordine viene generalmente fatturato dopo la ricezione del pagamento. Il metodo di pagamento determina le opzioni di fatturazione necessarie per l&#39;ordine. Dopo la generazione e l&#39;invio della fattura, viene inviata una copia al cliente. Se il metodo di pagamento è configurato con l&#39;azione di pagamento `capture` o `intent sale`, viene generata automaticamente una fattura quando il pagamento viene autorizzato e acquisito.

>[!NOTE]
>
>Le fatture non vengono create automaticamente per gli ordini effettuati utilizzando `Gift Card`, `Store Credit`, `Reward Points` o altri metodi di pagamento offline.

**Passaggio 5: Registra una singola spedizione** - Lo stato dell&#39;ordine diventa `Complete` quando i dettagli della spedizione sono completi, la spedizione è registrata e la spedizione è impostata. Il requisito di spedizione è soddisfatto con un documento di trasporto stampato e l&#39;etichetta di spedizione oppure è selezionato _Notify Ready for Pickup_ (metodo di consegna in-store). Il cliente riceve la notifica e il pacchetto viene spedito. Se vengono utilizzati numeri di registrazione, la spedizione può essere tracciata dal conto del cliente.

>[!NOTE]
>
>Per informazioni dettagliate sullo stato degli ordini e sulle opzioni di configurazione del metodo di pagamento, vedere [Stato ordine](order-status.md) e [Pagamenti](payments.md).

## Visualizza un ordine

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Trovare l&#39;ordine nella griglia.

1. Nella colonna _[!UICONTROL Action]_&#x200B;fare clic su **[!UICONTROL View]**.

1. Verifica stato ordine:

   - Un ordine `Pending` può essere modificato, bloccato, annullato o fatturato e spedito.

   - Un ordine `Processing` non può più essere modificato o annullato in modo sostanziale, ma è possibile modificare l&#39;indirizzo di fatturazione e di spedizione.

   - È possibile riordinare un ordine `Completed`.

L’e-mail del cliente può essere modificata in qualsiasi punto del flusso di lavoro dell’ordine modificando il cliente. Non è possibile modificare l&#39;e-mail se l&#39;ordine è stato effettuato da un ospite.

Il pannello sinistro di un ordine aperto consente di accedere a diversi tipi di informazioni correlate all’ordine.

![Visualizza ordine](./assets/order-view.png){width="700" zoomable="yes"}

## Elabora un ordine

Quando un cliente effettua un ordine, viene creato un ordine di vendita come record temporaneo della transazione. Lo stato dell&#39;ordine cliente è `Pending` fino alla ricezione del pagamento. Quando si trova nello stato `Pending`, gli ordini possono essere modificati o annullati fino al momento della ricezione del pagamento e della generazione della fattura. Un modo semplice di pensare è che gli ordini diventano fatture, e le fatture diventano spedizioni. La griglia Ordini elenca tutti gli ordini, indipendentemente dalla loro posizione nel flusso di lavoro. Per informazioni su come aiutare i clienti con un ordine, consulta [Aggiornare un ordine](order-update.md).

![Ordini](./assets/orders-grid.png){width="700" zoomable="yes"}

Per aprire un ordine `Pending`, fare clic su **[!UICONTROL Edit]** nell&#39;angolo superiore destro.

>[!NOTE]
>
>È possibile modificare gli ordini solo se si trova nello stato `Pending`. Il pulsante Modifica non è visibile per gli ordini con stato diverso o per gli ordini basati su [offerte negoziate](../b2b/quotes.md).

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
>Un utente amministratore deve disporre di **[!UICONTROL Sales / Archive]** [autorizzazioni](../systems/permissions-user-roles.md) per l&#39;ambito del proprio ruolo per visualizzare le _fatture_, _note di credito_ e _spedizioni_ schede ordine.

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
| **[!UICONTROL Edit]** | Apre un ordine in sospeso in modalità di modifica. Il pulsante Modifica non è visibile per gli ordini con stato `Processing` o basati su preventivi negoziati. |

{style="table-layout:auto"}

### Annullare un ordine

È possibile [annullare](order-update.md) ordini non ancora fatturati. È necessario emettere una [nota di credito](credit-memos.md) se un cliente desidera annullare un ordine dopo che è stato fatturato (il pagamento viene acquisito).

Se un ordine è `Pending` o `Processing` e il pagamento non viene acquisito o non viene acquisito completamente, è possibile [annullare l&#39;ordine](#void-an-order) invece di annullarlo.

Per ripristinare un ordine annullato, fare clic sul pulsante **[!UICONTROL Reorder]** e creare un nuovo ordine con lo stato `Pending`.

>[!NOTE]
>
>L’annullamento di un ordine genera anche un annullamento, ma l’annullamento di un ordine non attiva l’annullamento.

### Annullare un ordine

Solo gli ordini cliente non fatturati con stato `Processing` e impostazione di integrazione del pagamento [di `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions) possono essere [annullati](order-update.md#void-a-processing-order). Dopo aver annullato un ordine, puoi annullarlo.

### [!UICONTROL Order and Account Information]

![Informazioni su ordini e account](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Informazioni ordine

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Order Number] | Il numero dell’ordine viene visualizzato nella parte superiore dell’ordine di vendita, seguito da una nota che indica se l’e-mail di conferma è stata inviata. |
| [!UICONTROL Order Date] | La data e l’ora in cui è stato effettuato l’ordine. |
| [!UICONTROL Purchased From] | Indica la visualizzazione del sito Web, del punto vendita e del punto vendita in cui è stato effettuato l&#39;ordine. |
| [!UICONTROL Placed from IP] | Indica l&#39;indirizzo IP del computer da cui è stato effettuato l&#39;ordine. |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) indica il [preventivo](../b2b/quotes.md) da cui è stato generato l&#39;ordine, se applicabile. Il nome dell&#39;offerta è collegato all&#39;offerta. |

{style="table-layout:auto"}

#### Informazioni account

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Customer Name] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine. Il Nome cliente è collegato al profilo cliente. |
| [!UICONTROL Email] | L’indirizzo e-mail del cliente o dell’acquirente. L’indirizzo e-mail è collegato per aprire un nuovo messaggio e-mail. |
| [!UICONTROL Customer Group] | Il nome del gruppo di clienti o del catalogo condiviso a cui è assegnato il cliente. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Il nome dell&#39;azienda a cui è associato l&#39;acquirente e per conto della quale è stato effettuato l&#39;ordine. Il nome della società è collegato al [profilo società](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Informazioni indirizzo](./assets/order-address-information.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Billing Address] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine, seguito dall&#39;indirizzo di fatturazione, dal numero di telefono e da [IVA](vat.md), se applicabile. Il numero di telefono è collegato alla composizione automatica su un dispositivo mobile. |
| [!UICONTROL Shipping Address] | Il nome della persona alla cui attenzione deve essere spedito l&#39;ordine, seguito dall&#39;indirizzo di spedizione e dal numero di telefono. Il numero di telefono è collegato alla composizione automatica su un dispositivo mobile. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Metodo di pagamento e spedizione](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Payment Information] | Il metodo di pagamento da utilizzare per l’ordine e il numero dell’ordine di acquisto, se applicabile, seguito dalla valuta utilizzata per effettuare l’ordine. Se l&#39;ordine viene addebitato al credito della società utilizzando [Pagamento sul conto](../b2b/enable-basic-features.md#configure-payment-on-account), viene indicato l&#39;importo addebitato sul conto. |
| [!UICONTROL Shipping & Handling Information] | Il metodo di spedizione da utilizzare e le eventuali spese di imballaggio applicabili. |

{style="table-layout:auto"}

### Attributi ordine personalizzati

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."}

Gli attributi personalizzati dell&#39;ordine consentono di associare all&#39;ordine ulteriori informazioni specifiche alle esigenze aziendali.

![Attributi ordine personalizzati](./assets/custom-order-attributes.png){width="600" zoomable="yes"}

Nella sezione **[!UICONTROL Custom Order Attributes]** vengono visualizzati tutti gli attributi dell&#39;ordine personalizzati e i relativi valori correnti.

Per creare un nuovo attributo ordine personalizzato, immettere **[!UICONTROL Attribute Code]** e **[!UICONTROL Value]**

Per creare attributi di ordine personalizzati aggiuntivi, fare clic su **[!UICONTROL Add Attribute]**.

Per rimuovere un attributo ordine personalizzato, fare clic sull&#39;icona **[!UICONTROL X]**.

>[!NOTE]
>
>Gli attributi dell&#39;ordine personalizzati possono essere modificati solo quando l&#39;ordine è nello stato `Pending`. Per gli ordini con altri stati, è possibile visualizzare i valori degli attributi ma non modificarli.

### Rivedi articoli ordinati

![Elementi ordinati](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

Nella sezione **[!UICONTROL Order Total]** eseguire le operazioni seguenti:

1. Immettere un **[!UICONTROL Comment]** da includere nell&#39;ordine.

1. Per inviare il commento al cliente tramite posta elettronica, selezionare la casella di controllo **[!UICONTROL Notify Customer by Email]**.

1. Se si desidera che il commento sia visibile nell&#39;account cliente, selezionare la casella di controllo **[!UICONTROL Visible on Storefront]**.

   ![Totale ordini](./assets/order-total.png){width="600" zoomable="yes"}

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
| [!UICONTROL Comment] | Casella di testo utilizzata per immettere un commento per il cliente che accompagna l&#39;ordine. <br/>**[!UICONTROL Notify Customer by Email]**- Selezionare la casella di controllo se si desidera inviare il commento al cliente come e-mail separata.<br/>**[!UICONTROL Visible on Storefront]** - Selezionare la casella di controllo se si desidera che il commento sia visibile dall&#39;account del cliente. <br/>**[!UICONTROL Update]**- Aggiunge il commento e invia un&#39;e-mail, se applicabile. |

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
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) l&#39;importo del credito del negozio disponibile applicato all&#39;ordine, se applicabile. |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Il prezzo totale degli articoli nel preventivo senza imposte, in base ai prezzi nel catalogo condiviso o nel catalogo standard utilizzato come base del preventivo. Se la valuta di visualizzazione della vetrina è diversa da quella di base, il valore viene visualizzato in entrambe le valute, con la visualizzazione della vetrina tra parentesi quadre. |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Sconto risultante da un preventivo negoziato tra l&#39;acquirente e il venditore. Se la valuta di visualizzazione della vetrina è diversa da quella di base, il valore viene visualizzato in entrambe le valute, con la visualizzazione della vetrina tra parentesi quadre. |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Il prezzo totale del catalogo meno lo sconto negoziato. |

{style="table-layout:auto"}

## Demo sull’elaborazione degli ordini

Guarda questo video e scopri di più sull’elaborazione e lo stato degli ordini:

>[!VIDEO](https://video.tv.adobe.com/v/3410798/?quality=12&learn=on&captions=ita)
