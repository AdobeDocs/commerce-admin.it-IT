---
title: Rimborsi nel pannello di controllo del conto cliente
description: I clienti del Negozio possono visualizzare le informazioni sul rimborso associate all'ordine nel dashboard del proprio account.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 485
ht-degree: 0%

---

# Rimborsi nel pannello di controllo del conto cliente

{{ee-feature}}

Se è stato emesso un rimborso per un ordine, i clienti possono visualizzare le informazioni sul rimborso associate all’ordine nel dashboard del conto. Se hai abilitato l&#39;opzione [!UICONTROL _Mostra cronologia credito store ai clienti_] per [Configurazione credito store](../customers/credit-configure.md), i clienti possono accedere anche alla cronologia del credito [Store](../customers/store-credit.md).

## Visualizza un rimborso sul vetrina

1. Dalla vetrina, il cliente accede al proprio account.

1. Individua l&#39;ordine utilizzando uno dei metodi seguenti:

   * Ricerca dell&#39;ordine nell&#39;elenco di **Ordini recenti** e clic su **[!UICONTROL View]**.
   * Nel pannello a sinistra, scegliere **[!UICONTROL My Orders]**. Trovare quindi l&#39;ordine nell&#39;elenco e fare clic su **[!UICONTROL View]**.

1. Il cliente fa clic sulla scheda **[!UICONTROL Refunds]** per visualizzare i dettagli del rimborso.

   ![Rimborso dettagli in vetrina](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Visualizza il saldo del credito del negozio e la cronologia sul negozio

Metodo 1: **Dalla dashboard dell&#39;account cliente**

1. Dalla vetrina, il cliente accede al proprio account.

1. Se il rimborso è stato applicato al credito del negozio, seleziona **[!UICONTROL Store Credit]** nel pannello a sinistra.

1. L&#39;importo rimborsato al credito del negozio viene visualizzato nell&#39;elenco con la data e l&#39;ora dell&#39;azione.

   ![Importo rimborsato per il credito dell&#39;archivio](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >La pagina Credito negozio fornisce inoltre un collegamento per consentire al cliente di riscattare una [gift card](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Metodo 2: **Dalla pagina _Revisione e pagamenti_**

1. Il cliente aggiunge un prodotto al carrello.

2. Consente di passare alla pagina _Estrai_.

3. Supera il passaggio **[!UICONTROL Shipping]**.

4. Se il credito dello store è disponibile, il cliente fa clic su **[!UICONTROL Use Store Credit]**.

   ![Memorizza credito dalla pagina Revisioni e pagamenti](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Se il cliente cambia idea sull&#39;utilizzo del credito del negozio, fa clic su **[!UICONTROL Remove]** nella sezione _Riepilogo ordine_.

## Azioni di pagamento nell’amministratore

Puoi configurare le azioni di pagamento per il tuo [metodo di pagamento](../configuration-reference/sales/payment-methods.md) specifico. Ogni metodo di pagamento prevede una serie diversa di azioni di pagamento.

| Azione di pagamento | Descrizione |
|--- |---|
| [!UICONTROL Capture Online] | Quando la fattura viene inviata, il sistema acquisisce il pagamento dal gateway di pagamento di terze parti. Un utente amministratore può quindi creare una nota di accredito e annullare la fattura. |
| [!UICONTROL Capture Offline] | Quando la fattura viene inviata, il sistema non acquisisce il pagamento. Si presume che il pagamento venga acquisito direttamente tramite il gateway e che non possa essere acquisito tramite Adobe Commerce. Un utente amministratore può quindi creare una nota di accredito, ma non può annullare la fattura. Anche se l&#39;ordine ha utilizzato un pagamento online, la fattura è essenzialmente una fattura offline. |
| [!UICONTROL Not Capture] | Quando la fattura viene inviata, il sistema non acquisisce il pagamento. Si presume che il pagamento venga acquisito tramite Adobe Commerce in un secondo momento. Nella fattura completata è presente un pulsante [!UICONTROL _Acquisisci_]. Prima dell&#39;acquisizione, è possibile annullare la fattura. Dopo l&#39;acquisizione, è possibile creare una nota di credito e annullare la fattura. |

{style="table-layout:auto"}

>[!WARNING]
>
>Selezionare l&#39;opzione [!UICONTROL _Non acquisire_] a meno che non si sia certi che il pagamento verrà acquisito tramite Adobe Commerce in un secondo momento. Non puoi creare una nota di credito finché il pagamento non viene acquisito utilizzando il pulsante [!UICONTROL _Acquisisci_].
