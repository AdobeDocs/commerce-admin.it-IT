---
title: '[!UICONTROL Sales] menu'
description: L’amministratore di Commerce include [!UICONTROL Sales] , che consente di accedere agli strumenti per l'utilizzo degli ordini in base alla loro posizione all'interno del flusso di lavoro.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: a7c6203cf738e3fb9be887d637010ca9c155937a
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# [!UICONTROL Sales] menu

Il menu Vendite elenca le transazioni in base alla posizione in cui si trovano nel flusso di lavoro dell&#39;ordine. Potresti considerare ciascuna opzione come una fase diversa della durata di un ordine.

![Menu Vendite](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Visualizza [!UICONTROL Sales] menu

Il giorno _Amministratore_ barra laterale, fai clic su **[!UICONTROL Sales]**.

## Opzioni del menu

### [!UICONTROL Quotes]

![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile con B2B per Adobe Commerce)

Gli acquirenti autorizzati possono [negoziare il prezzo](../b2b/quotes.md) con il venditore inviando un [richiesta](../b2b/quote-request.md) dal carrello.

### [!UICONTROL Orders]

Quando un [ordine](orders.md) viene inserito, un ordine cliente viene creato come record temporaneo della transazione. Il pagamento non è stato elaborato e l&#39;ordine può ancora essere annullato.

### [!UICONTROL Invoices]

Un [fattura](invoices.md) è la registrazione della ricezione del pagamento di un ordine. È possibile creare più fatture per un singolo ordine, ognuna con un numero uguale o inferiore di prodotti acquistati specificati. A seconda dell&#39;azione di pagamento, il pagamento può essere acquisito automaticamente quando viene generata la fattura.

### [!UICONTROL Shipments]

A [spedizione](shipments.md) è una registrazione dei prodotti in un ordine spedito. Come per le fatture, è possibile associare più spedizioni a un singolo ordine, fino a quando non vengono spediti tutti i prodotti dell&#39;ordine.

### [!UICONTROL Credit Memos]

A [nota di accredito](credit-memos.md) è un documento che mostra l&#39;importo dovuto dal cliente per un rimborso completo o parziale. L’importo può essere applicato a un acquisto o rimborsato al cliente.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

A [autorizzazione merce restituita](returns.md) (RMA) può essere concesso ai clienti che richiedono la restituzione di un articolo per la sostituzione o il rimborso. Le RMA possono essere rilasciate per tipi di prodotto Semplici, Raggruppati, Configurabili e Bundle. Tuttavia, le RMA non sono disponibili per i prodotti virtuali e scaricabili o per le carte regalo.

### [!UICONTROL Billing Agreements]

A [contratto di fatturazione](paypal-billing-agreements.md) è simile a un ordine di acquisto, con la differenza che non è limitato a un singolo acquisto. Durante il pagamento, il cliente sceglie Contratto di fatturazione come metodo di pagamento. Un contratto di fatturazione semplifica il processo di pagamento in quanto il cliente non deve inserire informazioni di pagamento per ogni acquisto.

### [!UICONTROL Transactions]

Il [Transazioni](transactions.md) pagina elenca tutte le attività di pagamento che hanno avuto luogo tra il tuo negozio e tutti i sistemi di pagamento e fornisce l&#39;accesso a informazioni più dettagliate.

### [!UICONTROL Braintree Virtual Terminal]

Nella pagina Braintree terminale virtuale, un utente amministratore può accettare il pagamento per l’importo selezionato. Per rendere disponibile la funzione del terminale, un esercente deve configurare [Braintree impostazioni](braintree.md). Braintree offre un’esperienza di pagamento completamente personalizzabile con rilevamento di frodi e integrazione PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

(L&#39;opzione di archiviazione deve essere abilitata) [Ordini di archiviazione](order-archive.md) e altri documenti di vendita migliorano regolarmente le prestazioni e mantengono il vostro spazio di lavoro libero da informazioni inutili.
