---
title: Credito store
description: Il credito del Negozio è un importo che viene ripristinato in un conto cliente e può essere utilizzato per pagare gli acquisti o per i rimborsi in contanti.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Credito store

{{ee-feature}}

Il credito del Negozio è un importo che viene ripristinato in un conto cliente. I clienti possono utilizzare il credito del negozio per pagare gli acquisti e gli amministratori possono utilizzare il credito del negozio per i rimborsi in contanti. I saldi della gift card possono essere accreditati sul conto del cliente, invece di utilizzare il codice gift card per acquisti futuri.

Dopo il pagamento e la fatturazione di un ordine, è possibile rimborsare l&#39;ordine o parte di esso emettendo una nota di credito [](../stores-purchase/credit-memo-create.md). Una nota di credito differisce da un rimborso perché l&#39;importo del credito viene ripristinato sul conto del cliente in cui può essere utilizzato per acquisti futuri. A volte, un rimborso può essere dato contemporaneamente all&#39;emissione di una nota di credito e applicato al saldo del credito del negozio del cliente. L&#39;importo del credito del punto vendita disponibile nel conto del cliente è specificato nella configurazione.

>[!NOTE]
>
>Il metodo di pagamento [_Estrazione subtotale zero_](../stores-purchase/zero-subtotal-checkout.md) deve essere abilitato nel caso in cui il credito dell&#39;archivio copra il totale dell&#39;ordine.

## Flusso di lavoro per crediti store

1. **Accesso cliente** - Il cliente accede all&#39;account prima di iniziare il processo di pagamento.

1. **Usa store** - Accredito Durante il passaggio [!UICONTROL _Verifica e pagamenti_] del processo di pagamento, il cliente seleziona [!UICONTROL _Usa credito store_] come opzione di pagamento. Il saldo disponibile viene visualizzato tra parentesi. Se il saldo disponibile è maggiore del totale complessivo, gli altri metodi di pagamento non vengono più visualizzati.

1. **Credito applicato all&#39;ordine** - L&#39;importo del credito dell&#39;archivio applicato all&#39;ordine viene visualizzato con i totali dell&#39;ordine e viene sottratto dal totale complessivo.

1. **Saldo cliente adeguato** - Il saldo disponibile del cliente viene adeguato al momento dell&#39;ordine.
