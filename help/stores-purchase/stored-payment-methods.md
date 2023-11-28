---
title: Metodi di pagamento memorizzati
description: Scopri come i clienti possono utilizzare i metodi di pagamento memorizzati nella vetrina Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Metodi di pagamento memorizzati

I clienti che hanno accesso a un vaulting sicuro per memorizzare le informazioni di pagamento possono effettuare il pagamento senza inserire ogni volta le informazioni sulla carta di credito. Se [Acquisto immediato](checkout-instant-purchase.md) è abilitato, i clienti possono evitare il processo di pagamento in due fasi e effettuare l’ordine dalla pagina del prodotto.

Un metodo di pagamento che supporta un archivio protetto, ad esempio [Braintree](braintree.md), è obbligatorio. Quando nella configurazione del metodo di pagamento è abilitato un vaulting protetto, i clienti hanno la possibilità, durante il pagamento, di salvare le informazioni sulla carta di credito come metodo di pagamento memorizzato. I clienti possono gestire i metodi di pagamento memorizzati dal dashboard del proprio account.

![Metodi di pagamento memorizzati](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Aggiungi metodo di pagamento memorizzato al pagamento

1. Dalla vetrina, il cliente accede alla pagina dei dettagli del prodotto.

1. Aggiunge il prodotto al carrello.

1. Consente di passare alla pagina di pagamento.

1. Completa il _Spedizione_ passaggio.

1. Seleziona il **[!UICONTROL Braintree Credit Card]** metodo di pagamento.

1. Inserisce i dati della carta di credito.

1. Seleziona il **[!UICONTROL Save for later use]** casella di controllo.

1. Clic **[!UICONTROL Place Order]**.

Il metodo di pagamento salvato viene quindi visualizzato nel _[!UICONTROL Stored Payment Methods]_della dashboard del cliente.

## Elimina un metodo di pagamento memorizzato

Qualsiasi metodo di pagamento precedentemente aggiunto e memorizzato non può essere modificato dal cliente, può solo essere eliminato. Questa azione non può essere annullata.

1. Nella barra laterale del loro account, il cliente seleziona **[!UICONTROL Stored Payment Methods]**.

1. Trova la voce del metodo di pagamento da eliminare.

1. Clic **[!UICONTROL Delete]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.
