---
title: Acquisto immediato
description: Scopri l’acquisto istantaneo e come può offrire un pagamento rapido per gli account cliente registrati.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
TQID: https://experienceleague.adobe.com/sxfhq1vK7ohJBBli3U05dNoOvV2cdHc3j17nwvf3Le4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Acquisto immediato

_Acquisto immediato_ consente ai clienti di velocizzare il processo di pagamento utilizzando le informazioni salvate nel loro account. Se attivato, il pulsante _Acquisto immediato_ viene visualizzato sotto il pulsante _Aggiungi al carrello_ nella pagina del prodotto per i clienti che soddisfano i requisiti.

![Pagina prodotto con opzione di acquisto immediato visualizzata](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Requisiti del cliente

- Il cliente è [connesso](../customers/customer-sign-in.md) al proprio account.

- L&#39;account cliente ha un [indirizzo predefinito per fatturazione e spedizione](../customers/account-dashboard-address-book.md).

- È disponibile almeno un [metodo di spedizione](delivery.md) per il paese specificato nell&#39;indirizzo di spedizione predefinito.

- L&#39;account cliente ha un metodo di pagamento [memorizzato](../stores-purchase/stored-payment-methods.md) con Vault abilitato.

  I seguenti metodi di pagamento possono essere utilizzati per fornire un accesso sicuro alle informazioni salvate sulla carta di credito:

   - [Carte di credito Braintree](braintree.md) (l&#39;acquisto immediato non può essere utilizzato con le carte di credito Braintree se 3D Secure è abilitato.)
   - [Braintree con PayPal abilitato](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Acquisto immediato sul negozio

1. Nella vetrina, il cliente accede alla pagina del prodotto dell’articolo da acquistare.

1. Seleziona le opzioni richieste e fa clic su **[!UICONTROL Instant Purchase]**.

   ![Finestra di dialogo per confermare l&#39;acquisto immediato](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Esamina le informazioni di **[!UICONTROL Instant Purchase Confirmation]** e fa clic su **[!UICONTROL OK]** per completare la transazione.

   Nella parte superiore della pagina del prodotto vengono visualizzati un messaggio di conferma e un numero di ordine.

## Configurare l’acquisto immediato

### Passaggio 1: aprire la pagina di configurazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Passaggio 2: configurare l&#39;insieme di credenziali del metodo di pagamento

Puoi utilizzare l’acquisto istantaneo con Braintree o Payment Services per Adobe Commerce e Magento Open Source. Il vaulting deve essere attivato prima che un acquirente possa utilizzare la funzione di acquisto istantaneo.

Scopri come configurare il metodo di pagamento e abilitare il vaulting per Braintree o Payment Services:

- [Braintree](braintree.md)
- [Documentazione di Payment Services](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)

### Passaggio 3: abilitare l’acquisto immediato

1. Nel pannello a sinistra sotto la sezione _[!UICONTROL Sales]_, scegli **[!UICONTROL Sales]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Instant Purchase]**.

1. Se la modifica riguarda una visualizzazione archivio specifica, [scegliere la visualizzazione archivio](../configuration-reference/scope-change.md#set-the-scope) in cui applicare la configurazione.

   Quando richiesto, fare clic su **[!UICONTROL OK]** per continuare.

1. Imposta **[!UICONTROL Enabled]** su `Yes`.

1. Immettere **[!UICONTROL Button Text]** che si desidera visualizzare sul pulsante.

   Il testo del pulsante può essere modificato per ogni visualizzazione store o lingua. Per impostazione predefinita, il testo del pulsante è `Instant Purchase`.

   ![Configurazione - Opzioni di acquisto immediato](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedi [Acquisto immediato](../configuration-reference/sales/sales.md#instant-purchase) nella _Guida di riferimento alla configurazione_.

1. Fare clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e seguire le istruzioni per eseguire il flushing della cache.
