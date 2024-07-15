---
title: Aggiornare un profilo cliente
description: Accedi alle informazioni sull’attività del cliente, ad esempio quando ha effettuato l’ultimo accesso o uscita dal proprio account, e aggiorna il profilo del cliente.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# Aggiornare un profilo cliente

Il pannello sinistro della pagina _[!UICONTROL Customer Information]_include informazioni sull&#39;attività del cliente, gli indirizzi, le statistiche degli ordini, gli ordini recenti, il contenuto del carrello, le recensioni dei prodotti e gli abbonamenti alle newsletter.

![Profilo cliente](assets/cust-profile.png){width="700" zoomable="yes"}

## Modificare un account cliente

Metodo 1: **_Modifica rapida_**

1. Nella prima colonna selezionare la casella di controllo del conto cliente da modificare.

1. Imposta la colonna **[!UICONTROL Actions]** su `Edit`.

   >[!INFO]
   >
   >Il valore di ogni valore che è possibile aggiornare viene visualizzato in una casella di testo. Dalla griglia è possibile modificare solo alcuni valori del record cliente selezionato.

   ![Modifica rapida](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Se necessario, aggiorna uno dei seguenti valori:

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Fare clic su **[!UICONTROL Save]**.

Metodo 2: **_Modifica completa_**

1. Nella griglia individuare il record cliente da modificare.

1. Nella colonna _Azioni_ all&#39;estrema destra, fare clic su **[!UICONTROL Edit]**.

1. Apportare le modifiche necessarie alle informazioni aziendali.

   >[!INFO]
   >
   >Per ulteriori informazioni, consulta [Aggiornare un profilo cliente](../customers/update-account.md).

1. Al termine, fare clic su **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Se si desidera annullare tutte le modifiche prima di salvare, fare clic su **[!UICONTROL Reset]** nella barra dei pulsanti superiore per ripristinare tutte le modifiche apportate all&#39;ultima versione salvata.

## Informazioni cliente

### [!UICONTROL Customer View]

Nella scheda _Visualizzazione clienti_ sono elencate le informazioni sul cliente, inclusi **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]** e **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

La scheda [Informazioni account](../customers/account-dashboard-account-information.md) fornisce informazioni dettagliate sul cliente, in cui un utente amministratore può modificare informazioni personali, e-mail, assistenza per acquisti remoti, data di nascita e allegare il cliente al sito Web o all&#39;azienda.

### [!UICONTROL Addresses]

La scheda [Indirizzi](../customers/account-dashboard-address-book.md) contiene gli indirizzi di fatturazione e spedizione predefiniti del cliente ed eventuali indirizzi aggiuntivi utilizzati di frequente.

### [!UICONTROL Orders]

La griglia [Ordini](../stores-purchase/orders.md) contiene un elenco di tutti gli ordini dei clienti correnti. L&#39;amministratore può tenere traccia del loro avanzamento.

### [!UICONTROL Returns]

{{ee-feature}}

Nella scheda [Restituisce](../stores-purchase/returns.md) sono elencate le richieste dei clienti restituite correnti.

### [!UICONTROL Shopping cart]

Nella scheda [carrello](../stores-purchase/cart.md) sono visualizzati i prodotti attualmente presenti nel carrello, ma per qualche motivo l&#39;acquisto non è stato completato.

### [!UICONTROL Wish List]

In un [elenco desideri](../stores-purchase/wishlists.md) viene visualizzato un elenco di prodotti che un cliente può trasferire al carrello in un secondo momento.

### [!UICONTROL Gift Registry]

{{ee-feature}}

Nella sezione [Registro regali](../merchandising-promotions/gift-registry-storefront.md) sono elencati i registri regali correnti del cliente e l&#39;evento associato.


### [!UICONTROL Store Credit]

{{ee-feature}}

Nella scheda [Memorizza credito](../customers/store-credit.md) viene visualizzato un importo che viene ripristinato in un account cliente. L&#39;amministratore può gestire questo valore.

### [!UICONTROL Newsletter]

Nella scheda [Newsletter](../merchandising-promotions/newsletters.md) vengono visualizzati tutti i messaggi e-mail inviati al cliente corrente.

### [!UICONTROL Billing Agreements]

Nella scheda [Contratti di fatturazione](../stores-purchase/paypal-billing-agreements.md) sono elencati tutti i contratti di fatturazione PayPal tra il punto vendita e il cliente.

### [!UICONTROL Product Reviews]

Nella scheda [Recensioni prodotto](../catalog/settings-advanced-product-reviews.md) sono visualizzate tutte le revisioni inviate dal cliente.

### [!UICONTROL Reward Points]

{{ee-feature}}

La sezione [Punti premio](../merchandising-promotions/rewards-loyalty.md) mostra il saldo corrente dei punti premio del cliente. Un utente amministratore può gestire questo valore.

## Barra dei pulsanti

| Pulsante | Descrizione |
|----------|--------------|
| **[!UICONTROL Back]** | Torna alla pagina Clienti senza salvare le modifiche. |
| **[!UICONTROL Login as Customer]** | Consente al commerciante di accedere come cliente. |
| **[!UICONTROL Delete Customer]** | Elimina l&#39;account cliente. |
| **[!UICONTROL Reset]** | Ripristina i valori precedenti delle modifiche non salvate nel modulo per il cliente. |
| **[!UICONTROL Create Order]** | [Crea un ordine](../stores-purchase/customer-account-create-order.md) associato al conto cliente. |
| **[!UICONTROL Reset Password]** | Reimposta la password del cliente. |
| **[!UICONTROL Force Sign-In]** | Cancella i token associati alla password del cliente e fornisce all&#39;amministratore l&#39;accesso all&#39;account. |
| **[!UICONTROL Manage Shopping Cart]** | Consente di accedere al carrello di un cliente. |
| **[!UICONTROL Save and Continue Edit]** | Salva le modifiche e mantiene aperto l&#39;account cliente. |
| **[!UICONTROL Save Customer]** | Salva le modifiche e chiude l&#39;account cliente. |

{style="table-layout:auto"}
