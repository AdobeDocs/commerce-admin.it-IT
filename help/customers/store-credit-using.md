---
title: Applica credito negozio
description: Gli amministratori del negozio possono applicare il credito del negozio a un acquisto.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Applica credito negozio

{{ee-feature}}

Gli amministratori del Negozio possono visualizzare il saldo e la cronologia del credito dal conto cliente e applicare il credito del Negozio a un acquisto.

![Saldo credito cliente e cronologia](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Visualizza il saldo a credito

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Individuare il cliente nella griglia.

1. In _Azione_ , fare clic su **[!UICONTROL Edit]**.

1. Scorri _[!UICONTROL Customer View]_e visualizzare **[!UICONTROL Store Credit Balance]**in basso.

![Memorizza saldo credito](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Aggiorna saldo credito negozio

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > _Operazioni_ > **[!UICONTROL All Customers]**.

1. Individuare il cliente nella griglia.

1. In _Azione_ , fare clic su **[!UICONTROL Edit]**.

1. Nel pannello a sinistra, scegli **[!UICONTROL Store Credit]**.

1. Scegliere il sito Web (vetrina) che si desidera associare al saldo.

1. Per **[!UICONTROL Update Balance]**, immetti il nuovo valore.

1. Per notificare al cliente l&#39;aggiornamento del saldo, selezionare **[!UICONTROL Notify Customer by Email]** e scegli la visualizzazione store da **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Immetti un **[!UICONTROL Comment]** circa il cambiamento.

1. Al termine degli aggiornamenti, fai clic su **[!UICONTROL Save and Continue Edit]** o **[!UICONTROL Save Customer]**.

Il saldo aggiornato deve essere visualizzato in **[!UICONTROL Balance History]**.

## Applicare un saldo a credito a un ordine come amministratore del negozio

In qualità di amministratore del negozio, puoi eseguire varie operazioni per conto di un cliente, incluso l’invio di ordini. Quando [creare un ordine](../stores-purchase/customer-account-create-order.md), puoi applicare un saldo a credito del Negozio dovuto al cliente. Il saldo disponibile viene visualizzato nel _Informazioni su pagamento e spedizione_ sezione. Seleziona la **[!UICONTROL Use Store Credit]** casella di controllo per applicare il saldo o una parte del saldo se il totale dell&#39;ordine è inferiore.

![Applica il saldo a credito del punto vendita all&#39;ordine](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Applica credito del negozio durante l&#39;acquisto

Se è presente un saldo a credito per la sede, il cliente può applicare il credito del negozio al saldo dell&#39;ordine prima di inserire l&#39;ordine nella vetrina.

1. Il cliente visualizza l&#39;importo del credito del negozio disponibile.

   Durante il _Revisione e pagamenti_ fase, l&#39;importo disponibile viene visualizzato in _[!UICONTROL Store Credit]_.

1. Per applicare l’importo all’ordine, fai clic su **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Il totale dell&#39;ordine viene ricalcolato e l&#39;importo del credito del punto vendita applicato viene visualizzato nel _[!UICONTROL Order Summary]_.

   ![Saldo a credito del punto vendita applicato all&#39;ordine](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Quando è pronto, fa clic su **[!UICONTROL Place Order]**.
