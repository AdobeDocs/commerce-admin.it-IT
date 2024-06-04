---
title: Note di credito
description: Scopri le note di credito e come vengono utilizzate per emettere un rimborso parziale o completo.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Note di credito

A _nota di accredito_ è un documento che mostra l&#39;importo dovuto dal cliente per un rimborso completo o parziale. L’importo può essere applicato a un acquisto o rimborsato al cliente. È possibile stampare una nota di credito per un singolo ordine o per più ordini come batch. Prima di poter stampare una nota di accredito, è necessario generarla per l&#39;ordine. Il _Note di credito_ pagina elenca le note di credito emesse ai clienti.

![Note di credito](./assets/credit-memos.png){width="700" zoomable="yes"}

## Metodo di rimborso

Il [metodo di pagamento](payments.md) per l&#39;ordine determina, in una certa misura, il metodo con cui si rimborsa un ordine.

È possibile rimborsare gli ordini in tre modi:

- Credito conto: gli ordini pagati utilizzando un conto di credito possono essere rimborsati come credito conto:
   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) [Credito store](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponibile con Adobe Commerce B2B) [Pagamento in acconto](../b2b/enable-basic-features.md#configure-payment-on-account) (metodo offline)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponibile con Adobe Commerce B2B) [Credito società](../b2b/credit-company.md)
- [Rimborso online](payments.md#online-payment-methods)- Gli ordini pagati con carta di credito tramite un gateway di pagamento, come PayPal o Braintree, vengono rimborsati online tramite il processore di pagamento.
- [Rimborso offline](payments.md#offline-payment-methods)- Ordini pagati in contrassegno ([COD](cash-on-delivery.md)) o da [assegno o vaglia postale](check-money-order.md) vengono rimborsati offline.

Puoi emettere un rimborso o un accredito conto offline (se abilitato) per qualsiasi metodo di pagamento.

Un ordine che è stato pagato da Cash on Delivery ([COD](cash-on-delivery.md)) o da [assegno o vaglia postale](check-money-order.md) viene rimborsato offline.

## Flusso di lavoro di rimborso

1. **Azione di pagamento** - Se il [Azione di pagamento](credit-memo-create.md#payment-action-setting) configurazione impostata su `Authorize`, è necessario generare una fattura prima di creare una nota di accredito. procedere al passo 2. Se impostato su `Authorize and Capture`, è già stata generata una fattura. Passare al passaggio 3.

1. **Genera fattura** - [Crea una fattura](invoices.md#create-an-invoice) per l&#39;ordine, in modo da poter inviare un rimborso al cliente tramite nota di credito.

1. **Crea nota di accredito** - [Emetti una nota di credito](credit-memo-create.md) in Admin for a [acquisto di credito](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)o un [assegno o vaglia postale](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Descrizioni delle colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Select] | Selezionare le caselle di controllo per gli elementi della nota di accredito da sottoporre a un&#39;azione oppure utilizzare il controllo di selezione nell&#39;intestazione di colonna. Opzioni: `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Identificatore numerico univoco assegnato quando viene inviata una richiesta di una nota di credito. |
| [!UICONTROL Created] | La data e l&#39;ora in cui il buyer ha presentato per la prima volta la richiesta di una nota di credito. |
| [!UICONTROL Order#] | ID ordine dell’ordine di cui vengono restituiti i prodotti. |
| [!UICONTROL Order Date] | La data e l&#39;ora in cui l&#39;acquirente ha effettuato un ordine. |
| [!UICONTROL Bill-to Name] | Il nome della persona responsabile del pagamento dell’ordine. |
| [!UICONTROL Status] | Indica lo stato corrente di una richiesta di nota di accredito. |
| [!UICONTROL Refunded] | Importo totale rimborsato dall&#39;ordine. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Apre la richiesta di una nota di accredito e conserva una registrazione della negoziazione tra l&#39;acquirente e il venditore. |
| [!UICONTROL Order Status] | Indica lo stato dell’ordine. |
| [!UICONTROL Purchased From] | Indica la visualizzazione del sito Web, del punto vendita e del punto vendita in cui è stato effettuato l&#39;ordine. |
| [!UICONTROL Billing Address] | L’indirizzo di fatturazione del cliente che ha effettuato l’ordine. |
| [!UICONTROL Shipping Address] | L’indirizzo dove deve essere spedito l’ordine. |
| [!UICONTROL Customer Name] | Il nome e il cognome del cliente che ha effettuato l’ordine. |
| [!UICONTROL Email] | L’indirizzo e-mail della persona che ha effettuato l’ordine. |
| [!UICONTROL Customer Group] | Il gruppo di clienti a cui è assegnato il cliente. |
| [!UICONTROL Payment Method] | Il metodo di pagamento da utilizzare per il pagamento. |
| [!UICONTROL Shipping Information] | Il metodo da utilizzare per spedire l’ordine. |
| [!UICONTROL Subtotal] | Il subtotale dell&#39;ordine, senza spedizione e movimentazione, e le imposte. |
| [!UICONTROL Shipping & Handling] | Importo addebitato per la spedizione e la movimentazione. |
| [!UICONTROL Adjustment Refund] | L&#39;importo che viene aggiunto all&#39;importo totale rimborsato come rimborso aggiuntivo. |
| [!UICONTROL Adjustment Fee] | Importo sottratto dall&#39;importo totale rimborsato. |
| [!UICONTROL Grand Total] | Totale ordine. |

{style="table-layout:auto"}
