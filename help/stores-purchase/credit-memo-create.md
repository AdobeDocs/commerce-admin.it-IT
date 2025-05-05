---
title: Emetti una nota di credito
description: Scopri come generare e stampare una nota di credito per un ordine fatturato.
exl-id: 84ec72ba-7f72-4fa1-a9bf-91c17f43a3a7
feature: Orders, Invoices
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2132'
ht-degree: 0%

---

# Emetti una nota di credito

Prima di poter stampare una nota di accredito, è necessario generarla per un [ordine fatturato](invoices.md#create-an-invoice). Puoi emettere rimborsi online e offline (parziali o completi) da una nota di credito aperta, a seconda del metodo di pagamento.

- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) I rimborsi possono essere applicati al credito dell&#39;archivio.
- ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) I rimborsi possono essere applicati al credito aziendale.
- Gli acquisti effettuati con carta di credito possono essere rimborsati online o offline.
- Gli acquisti effettuati tramite assegno o vaglia postale devono essere rimborsati offline.

Qualsiasi nota di accredito con [stato aperto](order-status.md) ha un rimborso in sospeso in scadenza.

Con le note di credito è possibile:

- Rimborsare l&#39;intero importo di una fattura.
- Rimborsare una parte della fattura.
- Rimborsare più importi parziali di una fattura.
- Rimborsare più fatture per ordine, senza superare l&#39;importo totale dell&#39;ordine.
- Rimborsare una parte della quantità per una riga, ad esempio tre delle cinque magliette di un ordine.

Per ulteriori informazioni, vedere [Creare una fattura](invoices.md#create-an-invoice).

## Impostazione azione di pagamento

Il flusso di lavoro di rimborso per gli ordini pagati con carta di credito è determinato dall&#39;impostazione [Azione di pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) nella configurazione per ogni metodo di pagamento disponibile. I rimborsi non possono essere emessi fino al regolamento della transazione.

![Impostazione azione di pagamento](./assets/payment-action-setting.png){width="600" zoomable="yes"}

- Se l&#39;azione di pagamento per il metodo di pagamento configurato è impostata su `Authorize`, è necessario generare la fattura dall&#39;amministratore prima di poter creare una nota di credito.
- Se l&#39;azione di pagamento per il metodo di pagamento configurato è impostata su `Authorize and Capture`, la fattura è già stata generata dall&#39;elaboratore pagamenti, ma i fondi non sono disponibili finché la transazione non viene liquidata. Questo breve periodo di attesa è consigliato da molti processori di pagamento come misura di sicurezza, e può di solito essere gestito automaticamente. Le transazioni possono anche essere regolate manualmente dal tuo account esercente con il processore dei pagamenti.
- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Se crei una nota di credito per un ordine che include opzioni regalo, il rimborso per la confezione regalo e/o la carta stampata viene visualizzato nella sezione Totali rimborso della nota di credito. Per escludere questi costi dall&#39;importo da rimborsare, inserire l&#39;importo come commissione di adeguamento. Se vengono emesse più note di credito per lo stesso ordine, il rimborso per le opzioni regalo viene visualizzato solo nella prima nota di credito.

## Creare una nota di credito

Determinare il tipo di rimborso che si desidera emettere, per un [acquisto di credito](#issue-a-refund-for-a-credit-purchase) o per [assegno o vaglia postale](#issue-an-offline-refund-for-check-or-money-order), e generare la nota di credito ed emettere un rimborso.

### Emetti un rimborso per un acquisto di credito

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

   ![Griglia ordini](./assets/orders-grid.png){width="700" zoomable="yes"}

1. Trovare l&#39;ordine nella griglia e fare clic su **[!UICONTROL View]**.

1. Se il pulsante _[!UICONTROL Credit Memo]_&#x200B;è visibile nella barra dei pulsanti, eseguire una delle operazioni seguenti:

   - Per emettere un rimborso `offline`, andare al passaggio #6.
   - Per emettere un rimborso `online`, continuare con il passaggio #4.

   Per ulteriori informazioni sui rimborsi offline e online, vedere [Note di credito](credit-memos.md).

1. Fai clic su **[!UICONTROL Invoices]** nel pannello a sinistra.

1. Trovare la fattura nella griglia e fare clic su **[!UICONTROL View]**.

   ![Griglia fatture](./assets/order-invoices-grid.png){width="700" zoomable="yes"}

1. Scorrere verso il basso fino alla sezione **[!UICONTROL Invoice Totals]** della fattura, verificare che la fattura sia impostata su `Capture Online` e fare clic su **[!UICONTROL Submit Invoice]**.

   ![Acquisizione online](./assets/order-invoice-capture-online.png){width="600" zoomable="yes"}

   Se tale opzione non è disponibile, la fattura è già stata creata. Procedi al passaggio successivo.

1. Nella barra dei pulsanti nella parte superiore della fattura, fare clic su **[!UICONTROL Credit Memo]**.

1. Verificare le informazioni nella sezione **[!UICONTROL Items to Refund]** ed eseguire le operazioni seguenti, se applicabili:

   - Per restituire il prodotto all&#39;inventario, selezionare la casella di controllo **[!UICONTROL Return to Stock]**.

     Il prodotto torna automaticamente allo stock se _Opzioni Stock di prodotto_ è impostato su `Automatically Return Credit Memo Item to Stock`. Con [Inventory management abilitato](../inventory-management/enable.md), l&#39;elemento torna all&#39;origine che ha inviato la spedizione.

   - Aggiornare **[!UICONTROL Qty to Refund]** e fare clic su **[!UICONTROL Update Qty's]**.

     ![Elementi da rimborsare](./assets/invoice-credit-memo-items-to-refund.png){width="600" zoomable="yes"}

1. Aggiornare la sezione **[!UICONTROL Refunds Totals]** come segue:

   - Per **[!UICONTROL Refund Shipping]**, immettere l&#39;importo da rimborsare dalla tariffa di spedizione.

     Questo campo mostra inizialmente l&#39;importo totale della spedizione dell&#39;ordine disponibile per il rimborso. È uguale all&#39;importo di spedizione totale dell&#39;ordine, meno qualsiasi importo di spedizione già rimborsato. Come la quantità, l&#39;importo può essere ridotto, ma non aumentato.

   - Per **[!UICONTROL Adjustment Refund]**, immettere un valore da aggiungere all&#39;importo totale rimborsato come rimborso aggiuntivo che non si applica ad alcuna parte specifica dell&#39;ordine (spedizione, articoli o imposta). Può essere utilizzato anche per il rimborso parziale con denaro virtuale, ad esempio una gift card, quando un amministratore desidera rimborsare prima un metodo di pagamento non virtuale.

     L&#39;importo inserito non può aumentare il rimborso totale superiore all&#39;importo pagato.

   - Per **[!UICONTROL Adjustment Fee]**, immettere un valore da sottrarre dall&#39;importo totale rimborsato.

     Questo importo non viene sottratto da una sezione specifica dell&#39;ordine, ad esempio spedizione, articoli o imposte.

1. Per aggiungere un commento, immettere il testo nella casella **[!UICONTROL Credit Memo Comments]**.

   - Per inviare una notifica e-mail al cliente, selezionare la casella di controllo **[!UICONTROL Email Copy of Credit Memo]**.

1. Fare clic su **[!UICONTROL Update Totals]**.

1. Effettua le seguenti operazioni, a seconda dei casi:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per rimborsare l&#39;importo al credito del punto vendita del cliente, selezionare la casella di controllo **[!UICONTROL Refund to Store Credit]**.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Per rimborsare l&#39;importo al credito della società del cliente, selezionare la casella di controllo **[!UICONTROL Refund to Company Credit]**.

   - Per emettere un rimborso offline, fare clic su **[!UICONTROL Refund Offline]**.

   - Per emettere un rimborso online, fare clic su **[!UICONTROL Refund]**.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Se l&#39;acquisto è stato pagato con il credito aziendale, fare clic su **[!UICONTROL Refund to Company Credit]**.

   Per ulteriori informazioni sui rimborsi offline e online, vedere [Note di credito](credit-memos.md).

   ![Rimborso totale ordine](./assets/credit-memo-order-total-refund.png){width="600" zoomable="yes"}

### Emetti un rimborso offline per assegno o vaglia postale

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Trovare l&#39;ordine completato nella griglia e aprirlo facendo clic sul collegamento **[!UICONTROL View]**.

1. Nella barra dei pulsanti nella parte superiore della pagina, fare clic su **[!UICONTROL Invoice]**.

1. Scorri verso il basso fino alla parte inferiore della pagina e fai clic su **[!UICONTROL Submit Invoice]**.

1. Nella barra dei pulsanti nella parte superiore della fattura, fare clic su **[!UICONTROL Credit Memo]**.

   ![Crea nota di credito](./assets/order-invoice-info-company.png){width="600" zoomable="yes"}

1. Verificare le informazioni nella sezione **[!UICONTROL Items to Refund]** ed eseguire le operazioni seguenti, se applicabili:

   ![Elementi da rimborsare](./assets/credit-memo-items-to-refund.png){width="600" zoomable="yes"}

   - Selezionare la casella di controllo **[!UICONTROL Return to Stock]** se si desidera restituire il prodotto restituito all&#39;inventario.

     Se Inventory management è abilitato, la quantità di magazzino viene restituita all&#39;origine che ha inviato la spedizione. Il prodotto torna automaticamente allo stock se [Opzioni Stock di prodotto](../inventory-management/enable.md) è impostato su `Automatically Return Credit Memo Item to Stock`.

   - Aggiornare **[!UICONTROL Qty to Refund]** e fare clic su **[!UICONTROL Update Qty's]**.

     L&#39;importo da accreditare non può superare l&#39;importo massimo disponibile per il rimborso.

1. Aggiornare la sezione **[!UICONTROL Refunds Totals]** come applicabile:

   - Per **[!UICONTROL Refund Shipping]**, immettere l&#39;importo da rimborsare dalla tariffa di spedizione.

     Questo campo visualizza inizialmente l&#39;importo totale della spedizione dell&#39;ordine disponibile per il rimborso. È uguale all&#39;importo di spedizione totale dell&#39;ordine, meno qualsiasi importo di spedizione già rimborsato. Come la quantità, l&#39;importo può essere ridotto, ma non aumentato.

   - Per **[!UICONTROL Adjustment Refund]**, immettere un valore da aggiungere all&#39;importo totale rimborsato come rimborso aggiuntivo che non si applica ad alcuna parte specifica dell&#39;ordine (spedizione, articoli o imposta). Può essere utilizzato anche per il rimborso parziale con denaro virtuale, ad esempio una gift card, quando un amministratore desidera rimborsare prima un metodo di pagamento non virtuale.

     L&#39;importo inserito non può aumentare il rimborso totale superiore all&#39;importo pagato.

   - Per **[!UICONTROL Adjustment Fee]**, immettere un valore da sottrarre dall&#39;importo totale rimborsato.

     Questo importo non viene sottratto da una sezione specifica dell&#39;ordine, ad esempio spedizione, articoli o imposte.

   - Se l&#39;acquisto è stato pagato con il credito del negozio, selezionare la casella di controllo **[!UICONTROL Refund to Store Credit]** per accreditare l&#39;importo al saldo del conto cliente.

1. Per aggiungere un commento, immettere il testo nella casella **[!UICONTROL Credit Memo Comments]** ed eseguire le operazioni seguenti:

   - Per inviare una notifica e-mail al cliente, selezionare la casella di controllo **[!UICONTROL Email Copy of Credit Memo]**.

   - Per includere i commenti immessi nell&#39;e-mail, selezionare la casella di controllo **[!UICONTROL Append Comments]**.

     Lo stato di una notifica di nota di credito viene visualizzato nella nota di credito completata accanto al numero della nota di credito.

     ![Totali rimborso](./assets/credit-memo-order-totals.png){width="600" zoomable="yes"}

1. Per completare il processo ed emettere il rimborso, fare clic su **[!UICONTROL Refund Offline]**.

## Descrizioni dei campi

### [!UICONTROL Order & Account Information]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Order Number] | Il numero di ordine viene visualizzato in _Informazioni su ordine e account_, seguito da una nota che indica se l&#39;e-mail di conferma è stata inviata. |
| [!UICONTROL Order Date] | La data e l’ora in cui è stato effettuato l’ordine. |
| [!UICONTROL Order Status] | Indica lo stato dell&#39;ordine come `Complete`. |
| [!UICONTROL Purchased From] | Indica la visualizzazione del sito Web, del punto vendita e del punto vendita in cui è stato effettuato l&#39;ordine. |
| [!UICONTROL Placed from IP] | Indica l&#39;indirizzo IP del computer da cui è stato effettuato l&#39;ordine. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Customer Name] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine. Il nome del cliente è collegato al suo profilo. |
| [!UICONTROL Email] | L’indirizzo e-mail del cliente o dell’acquirente. L’indirizzo e-mail è collegato per aprire un nuovo messaggio e-mail. |
| [!UICONTROL Customer Group] | Il nome del gruppo di clienti o del catalogo condiviso a cui è assegnato il cliente. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Il nome dell&#39;azienda associata all&#39;acquirente e per conto della quale è stato effettuato l&#39;ordine. Il nome dell’azienda è collegato al profilo dell’azienda. |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Billing Address] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine, seguito dall&#39;indirizzo di fatturazione, dal numero di telefono e da [IVA](vat.md), se applicabile. Il numero di telefono è collegato alla composizione automatica su un dispositivo mobile. |
| [!UICONTROL Shipping Address] | Il nome della persona alla cui attenzione deve essere spedito l&#39;ordine, seguito dall&#39;indirizzo di spedizione e dal numero di telefono. Il numero di telefono è collegato alla composizione automatica su un dispositivo mobile. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Payment Information] | Il metodo di pagamento da utilizzare per l’ordine e il numero dell’ordine di acquisto, se applicabile, seguito dalla valuta utilizzata per effettuare l’ordine. Se l&#39;ordine viene addebitato al credito della società utilizzando [Pagamento sul conto](../b2b/enable-basic-features.md#configure-payment-on-account), viene indicato l&#39;importo addebitato sul conto. |
| [!UICONTROL Shipping & Handling Information] | Il metodo di spedizione da utilizzare e le eventuali spese di imballaggio applicabili. |

{style="table-layout:auto"}

### [!UICONTROL Items to Refund]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Product] | Nome del prodotto, SKU e opzioni (se applicabile). |
| [!UICONTROL Price] | Prezzo di acquisto dell&#39;articolo. Per Adobe Commerce B2B, questo valore riflette eventuali sconti applicati all’elemento dal catalogo condiviso, se applicabili. |
| [!UICONTROL Qty] | La quantità ordinata. |
| [!UICONTROL Return to Stock] | Casella di controllo che indica se l&#39;articolo restituito deve essere restituito al magazzino. |
| [!UICONTROL Qty to Refund] | Indica il numero di unità restituite del prodotto. |
| [!UICONTROL Subtotal] | Il subtotale è il prezzo di acquisto moltiplicato per la quantità di unità di prodotto restituite. |
| [!UICONTROL Tax Amount] | Importo dell&#39;imposta che si applica all&#39;articolo restituito come valore decimale. |
| [!UICONTROL Tax Percent] | Percentuale di imposta applicata all&#39;articolo restituito come percentuale. |
| [!UICONTROL Discount Amount] | Qualsiasi sconto applicato all&#39;articolo restituito. |
| [!UICONTROL Row Total] | Totale della voce, incluse le imposte applicabili dovute per il livello di prodotto restituito, meno gli sconti. |
| _totale ordine_ |  |

{style="table-layout:auto"}

### [!UICONTROL Credit Memo Comments]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Comment Text] | Casella di testo utilizzata per immettere un commento al cliente sulla nota di accredito. |

{style="table-layout:auto"}

### [!UICONTROL Refund Totals]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Refund Shipping] | Importo della spedizione da rimborsare. |
| [!UICONTROL Adjustment Refund] | Importo che viene aggiunto all&#39;importo totale rimborsato come rimborso aggiuntivo che non si applica a nessuna parte specifica dell&#39;ordine, ad esempio spedizione, articoli o imposte. L&#39;importo inserito non può aumentare il rimborso totale superiore all&#39;importo pagato. |
| [!UICONTROL Adjustment Fee] | Un importo che viene sottratto dall&#39;importo totale rimborsato, ad esempio una tariffa di ricostituzione delle scorte o un importo correlato alla confezione di regali o alle opzioni regalo. |
| [!UICONTROL Grand Total] | Importo totale da rimborsare |
| [!UICONTROL Append Comments] | Casella di controllo che determina se i commenti sono inclusi nella nota di accredito. |
| [!UICONTROL Email Copy of Credit Memo] | Casella di controllo che determina se viene inviata un&#39;e-mail a una copia della nota di credito. |
| [!UICONTROL Refund to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Casella di controllo che determina se il totale deve essere rimborsato al [credito archivio](../customers/store-credit-using.md). |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Il totale di tutti gli elementi riga da rimborsare. |

{style="table-layout:auto"}

### Pulsanti Rimborso

Il metodo di pagamento utilizzato per l&#39;ordine determina i pulsanti di rimborso disponibili per una nota di accredito.

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Refund]** | Se l&#39;acquisto originale è stato pagato con carta di credito tramite un gateway di pagamento, l&#39;importo del rimborso viene gestito dal processore dei pagamenti. Per gestire i rimborsi, consulta la documentazione fornita dal tuo provider di servizi di pagamento. |
| **[!UICONTROL Refund Offline]** | Se l&#39;acquisto originale è stato pagato con assegno o vaglia postale, il rimborso viene pagato direttamente al cliente, emettendo un assegno, una gift card o contanti se si dispone di una vetrina in mattoni e malta. La nota di credito funge da record della transazione offline. |
| **[!UICONTROL Refund to Company Credit]** | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B) Se l&#39;acquisto è stato addebitato al credito della società, il rimborso viene restituito al [account società](../b2b/credit-company.md). |

{style="table-layout:auto"}

## Stampa una nota di credito

Per stampare o visualizzare la nota di credito completata, è necessario che sia installato un lettore di PDF. Puoi scaricare [Adobe Reader][1] gratuitamente.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Credit Memos]**.

1. Per stampare la nota di accredito, utilizzare uno dei seguenti metodi:

### Metodo 1: Stampa nota di credito corrente

1. Nella griglia aprire la nota di accredito.

1. Fare clic su **[!UICONTROL Print]**.

   ![Stampa la nota di credito](./assets/credit-memo-print.png){width="600" zoomable="yes"}

### Metodo 2: Stampa più note di credito

1. Nell&#39;elenco selezionare la casella di controllo di ogni nota di credito che si desidera stampare.

1. Impostare il controllo **[!UICONTROL Actions]** su `PDF Credit Memos` e fare clic su **[!UICONTROL Submit]**.

   ![Stampa note di credito selezionate](./assets/credit-memos-print.png){width="600" zoomable="yes"}

1. Quando richiesto, effettuare una delle seguenti operazioni:

   - Per salvare il documento, fare clic su **[!UICONTROL Save]** e seguire le istruzioni per salvare il file nel computer. Al termine del download, apri il PDF in Adobe Reader e stampa il documento.

   - Per visualizzare il documento, scegliere **[!UICONTROL Open]**. In Adobe Reader viene aperta la nota di credito PDF pronta per la stampa. Da qui è possibile stampare la nota di credito o salvarla nel computer.


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Scarica Adobe Reader"
