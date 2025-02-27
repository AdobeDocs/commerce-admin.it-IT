---
title: Menu [!UICONTROL Sales]
description: L'amministratore di Commerce include il menu [!UICONTROL Sales], che fornisce l'accesso agli strumenti per l'utilizzo degli ordini in base alla posizione all'interno del flusso di lavoro.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Menu [!UICONTROL Sales]

Il menu Vendite elenca le transazioni in base alla posizione in cui si trovano nel flusso di lavoro dell&#39;ordine. Potresti considerare ciascuna opzione come una fase diversa della durata di un ordine.

![Menu Vendite](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Visualizza il menu [!UICONTROL Sales]

Nella barra laterale _Admin_, fai clic su **[!UICONTROL Sales]**.

## Opzioni del menu

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B)

Gli acquirenti autorizzati possono [negoziare il prezzo](../b2b/quotes.md) con il venditore inviando una [richiesta](../b2b/quote-request.md) dal carrello.

### [!UICONTROL Orders]

Quando viene inserito un [ordine](orders.md), viene creato un ordine cliente come record temporaneo della transazione. Il pagamento non è stato elaborato e l&#39;ordine può ancora essere annullato.

### [!UICONTROL Invoices]

Una [fattura](invoices.md) è un record della ricevuta di pagamento di un ordine. È possibile creare più fatture per un singolo ordine, ognuna con un numero uguale o inferiore di prodotti acquistati specificati. A seconda dell&#39;azione di pagamento, il pagamento può essere acquisito automaticamente quando viene generata la fattura.

### [!UICONTROL Shipments]

Una [spedizione](shipments.md) è un record dei prodotti in un ordine spedito. Come per le fatture, è possibile associare più spedizioni a un singolo ordine, fino a quando non vengono spediti tutti i prodotti dell&#39;ordine.

### [!UICONTROL Credit Memos]

Una [nota di credito](credit-memos.md) è un documento che mostra l&#39;importo dovuto dal cliente per un rimborso completo o parziale. L’importo può essere applicato a un acquisto o rimborsato al cliente.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

È possibile concedere un&#39;autorizzazione [restituita](returns.md) (RMA) per il merchandise ai clienti che richiedono la restituzione di un articolo per la sostituzione o il rimborso. Le RMA possono essere rilasciate per tipi di prodotto Semplici, Raggruppati, Configurabili e Bundle. Tuttavia, le RMA non sono disponibili per i prodotti virtuali e scaricabili o per le carte regalo.

### [!UICONTROL Billing Agreements]

Un [contratto di fatturazione](paypal-billing-agreements.md) è simile a un ordine di acquisto, con la differenza che non è limitato a un singolo acquisto. Durante il pagamento, il cliente sceglie Contratto di fatturazione come metodo di pagamento. Un contratto di fatturazione semplifica il processo di pagamento in quanto il cliente non deve inserire informazioni di pagamento per ogni acquisto.

### [!UICONTROL Transactions]

La pagina [Transazioni](transactions.md) elenca tutte le attività di pagamento che hanno avuto luogo tra il tuo Negozio e tutti i sistemi di pagamento e fornisce l&#39;accesso a informazioni più dettagliate.

### [!UICONTROL Braintree Virtual Terminal]

Nella pagina Braintree terminale virtuale, un utente amministratore può accettare il pagamento per l’importo selezionato. Per rendere disponibile la funzionalità del terminale, un commerciante deve configurare [impostazioni di Braintree di base](braintree.md). Braintree offre un’esperienza di pagamento completamente personalizzabile con rilevamento di frodi e integrazione PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

(L&#39;opzione di archiviazione deve essere abilitata) [L&#39;archiviazione degli ordini](order-archive.md) e di altri documenti di vendita migliora regolarmente le prestazioni e consente di mantenere l&#39;area di lavoro libera da informazioni non necessarie.
