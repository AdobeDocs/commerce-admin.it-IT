---
title: Aggiornare un ordine
description: Scopri come aggiornare l’ordine di un cliente nell’Admin.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Aggiornare un ordine

Quando si aiuta un cliente che ha effettuato un ordine, è necessario determinare lo stato dell&#39;ordine. Le opzioni disponibili per un `Pending` sono diverse dalle opzioni per un `Processing` ordine. Per ulteriori informazioni, consulta [Elabora un ordine](order-processing.md).

## Ordini in sospeso

Dopo che un cliente ha effettuato un ordine, ma prima che il pagamento venga ricevuto, l&#39;ordine è in `Pending` stato. È possibile modificare l&#39;ordine, bloccarlo o annullarlo completamente. Nella barra dei pulsanti di un ordine in sospeso sono elencate le azioni disponibili per un ordine.

![Opzioni ordine in sospeso](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Se si modificano parti sostanziali di un ordine, l&#39;ordine originale viene annullato e viene generato un nuovo ordine. È tuttavia possibile modificare l&#39;indirizzo di fatturazione o di spedizione senza generare un nuovo ordine.

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Back]** | Torna alla pagina Ordini senza salvare le modifiche. |
| **[!UICONTROL Login as Customer]** | Consente a un utente amministratore di assistere i clienti con i loro ordini. |
| **[!UICONTROL Cancel]** | Annulla l&#39;ordine in sospeso. |
| **[!UICONTROL Send Email]** | Invia al cliente un&#39;e-mail relativa all&#39;ordine in sospeso. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Modifica lo stato dell&#39;ordine in sospeso in `On Hold`. Per rilasciare il blocco, scegliere _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Crea un [fattura](invoices.md#create-an-invoice) dall&#39;ordine in sospeso convertendo l&#39;ordine in una fattura e modifica lo stato dell&#39;ordine in `processing`. |
| **[!UICONTROL Ship]** | Crea un [spedizione](shipments.md#create-a-shipment) registrazione dell&#39;ordine. |
| **[!UICONTROL Reorder]** | Crea un nuovo ordine in sospeso duplicato dell&#39;ordine in sospeso corrente. |
| **[!UICONTROL Edit]** | Apre un ordine in sospeso in modalità di modifica. Il pulsante Modifica è disponibile solo per gli ordini in sospeso o per gli ordini basati su negoziati [virgolette](../b2b/quotes.md). |

{style="table-layout:auto"}

## Ordini di elaborazione

Un ordine inserisce un `Processing` indicare quando:

* Il pagamento di un ordine viene ricevuto/acquisito e la fattura viene generata quando l&#39;azione di pagamento è impostata su `Authorize and Capture`.
* Una transazione ordine è autorizzata, ma il pagamento non viene ancora acquisito, quando l&#39;azione di pagamento è impostata su `Authorize`.

Il [configurazione azione di pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) determina le azioni dell’ordine disponibili dopo la creazione di un ordine.

Non è possibile modificare sostanzialmente un `Processing` ma puoi modificare l&#39;indirizzo di fatturazione e di spedizione.

![Opzioni ordine di elaborazione](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando l&#39;azione di pagamento del metodo di pagamento è impostata su `Authorize and Capture`, una fattura viene creata automaticamente quando il cliente effettua un ordine. In questo caso, è possibile rimborsare i fondi utilizzando un [nota di accredito](credit-memo-create.md), ma non può [annulla](#cancel-a-pending-order) o [void](#void-a-processing-order) l&#39;ordine.

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Back]** | Torna alla pagina Ordini senza salvare le modifiche. |
| **[!UICONTROL Send Email]** | Invia un&#39;e-mail relativa all&#39;ordine al cliente. |
| **[!UICONTROL Void]** | [Vuoti](#void-a-processing-order) una transazione ordine o una transazione ordine parziale. |
| **[!UICONTROL Credit Memo]** | Avvia il processo di creazione di un [nota di accredito](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Modifica lo stato dell&#39;ordine cliente in `On Hold`. Per rilasciare il blocco dell&#39;ordine cliente, scegliere _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Crea un nuovo ordine in sospeso basato sull&#39;ordine corrente. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Avvia il processo per [return](returns.md) uno o più elementi dell’ordine. |

{style="table-layout:auto"}

## Annullare un ordine di elaborazione

Quando un ordine è ancora in un `Processing` e l’integrazione del pagamento è impostata su `Authorize` (non `Authorize and Capture`), è possibile solo annullare una transazione o annullare un ordine. [Annullamento di un ordine](#cancel-a-pending-order) annulla anche l’autorizzazione.

Quando un ordine viene effettuato utilizzando un metodo di pagamento con l’azione di pagamento impostata su `Authorize and Capture` è possibile rimborsare i fondi tramite nota di accredito, ma non annullarla perché è fatturata e il pagamento viene acquisito.

Il metodo di pagamento determina le azioni di pagamento disponibili. Consulta [Azioni di pagamento](../configuration-reference/sales/payment-methods.md#payment-actions) per ulteriori informazioni.

**_Per annullare un ordine:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. In **[!UICONTROL Action]** per l&#39;ordine da modificare, fare clic su **[!UICONTROL View]**.

1. Clic **[!UICONTROL Void]** per annullare l’ordine.

1. Al prompt, fai clic su **[!UICONTROL OK]** per annullare l’ordine.

Puoi emettere i rimborsi necessari utilizzando una [nota di accredito](credit-memo-create.md) dopo la cattura dei fondi. Puoi anche creare una [autorizzazione restituzione merce (RMA)](returns.md) rilasciati per restituzioni di prodotti. Per ulteriori informazioni, consulta [Elaborazione di un ordine](order-processing.md).

## Modificare un ordine in sospeso

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. In **[!UICONTROL Action]** per l&#39;ordine da modificare, fare clic su **[!UICONTROL View]**.

1. Clic **[!UICONTROL Edit]**.

   ![Modifica ordine](./assets/order-edit.png){width="600" zoomable="yes"}

1. Al prompt, fai clic su **[!UICONTROL OK]** per continuare la modifica.

1. Aggiorna l’ordine in base alle esigenze.

1. Applica le modifiche:
   * Per salvare le modifiche apportate all&#39;indirizzo di fatturazione o di spedizione, fare clic su **[!UICONTROL Save]**.
   * Per salvare le modifiche apportate agli elementi riga e rielaborare l&#39;ordine, fare clic su **[!UICONTROL Submit Order]**.

## Blocca un ordine

Se il metodo di pagamento preferito dal cliente non è disponibile o se l&#39;articolo è temporaneamente esaurito, è possibile bloccare l&#39;ordine.

1. In _Ordini_ griglia, trova la `Pending` dell&#39;ordine che si desidera bloccare.

1. In _Azione_ , fare clic su **[!UICONTROL View]**.

1. Clic **[!UICONTROL Hold]** per bloccare l&#39;ordine.

Per rimuovere il blocco di un ordine, modificarlo di nuovo e fare clic su **[!UICONTROL Unhold]**.

## Annullare un ordine in sospeso

L’annullamento di un ordine ne modifica lo stato da `Pending` a `Canceled`.

1. In _[!UICONTROL Orders]_trovare l&#39;ordine in sospeso da annullare.

1. In _[!UICONTROL Action]_, fare clic su **[!UICONTROL View]**.

1. Clic **[!UICONTROL Cancel]** per annullare l&#39;ordine.

Lo stato dell’ordine è ora `Canceled`.
