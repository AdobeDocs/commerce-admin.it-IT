---
title: Metodi di pagamento memorizzati
description: Scopri come i clienti possono utilizzare i metodi di pagamento memorizzati nella vetrina Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Metodi di pagamento memorizzati

I clienti che hanno accesso a un vaulting sicuro per memorizzare le informazioni di pagamento possono effettuare il pagamento senza inserire ogni volta le informazioni sulla carta di credito. Se [Acquisto immediato](checkout-instant-purchase.md) è abilitato, i clienti possono ignorare il processo di pagamento in due fasi e inoltrare l&#39;ordine dalla pagina del prodotto.

È necessario un metodo di pagamento che supporti un insieme di credenziali protetto, ad esempio [Braintree](braintree.md). Quando nella configurazione del metodo di pagamento è abilitato un vaulting protetto, i clienti hanno la possibilità, durante il pagamento, di salvare le informazioni sulla carta di credito come metodo di pagamento memorizzato. I clienti possono gestire i metodi di pagamento memorizzati dal dashboard del proprio account.

![Metodi di pagamento memorizzati](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Aggiungi metodo di pagamento memorizzato al pagamento

1. Dalla vetrina, il cliente accede alla pagina dei dettagli del prodotto.

1. Aggiunge il prodotto al carrello.

1. Consente di passare alla pagina di pagamento.

1. Completa il passaggio _Spedizione_.

1. Seleziona il metodo di pagamento **[!UICONTROL Braintree Credit Card]**.

1. Inserisce i dati della carta di credito.

1. Seleziona la casella di controllo **[!UICONTROL Save for later use]**.

1. Clic su **[!UICONTROL Place Order]**.

Il metodo di pagamento salvato viene quindi visualizzato nella scheda _[!UICONTROL Stored Payment Methods]_del dashboard cliente.

## Elimina un metodo di pagamento memorizzato

Qualsiasi metodo di pagamento precedentemente aggiunto e memorizzato non può essere modificato dal cliente, può solo essere eliminato. Questa azione non può essere annullata.

1. Nella barra laterale del proprio account, il cliente seleziona **[!UICONTROL Stored Payment Methods]**.

1. Trova la voce del metodo di pagamento da eliminare.

1. Clic su **[!UICONTROL Delete]**.

1. Per confermare l&#39;azione, fa clic su **[!UICONTROL OK]**.
