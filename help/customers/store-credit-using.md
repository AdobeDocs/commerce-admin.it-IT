---
title: Applica credito negozio
description: Gli amministratori del negozio possono applicare il credito del negozio a un acquisto.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
TQID: 'https://experienceleague.adobe.com/O2EJMZscownPnhjPeFROdwikhYmHuDYdCx4N7NpXlho'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b2b09a49ecd0c585d6ea456f0c00e05d813e324d
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%
---
# Applica credito negozio

{{ee-feature}}

Gli amministratori del Negozio possono visualizzare il saldo e la cronologia del credito dal conto cliente e applicare il credito del Negozio a un acquisto.

![Saldo credito cliente e cronologia](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Memorizza risorse ruolo credito

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."}

Le risorse seguenti determinano quali utenti amministratori possono modificare il saldo del credito del negozio di un cliente e quali utenti possono applicare il credito del negozio a un ordine. Per informazioni sull&#39;assegnazione di risorse a un ruolo utente, vedere [Risorse ruolo](../systems/permissions-user-roles.md#role-resources).

- **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** > **[!UICONTROL Manage Store Credit Balances]** consente agli utenti di visualizzare e aggiornare i saldi di credito dello store. Senza di essa, la scheda **[!UICONTROL Store Credit]** e la scheda **[!UICONTROL Store Credit Balance]** della scheda **[!UICONTROL Customer View]** non sono visibili. L’utente può comunque apportare altre modifiche agli account cliente.

- **[!UICONTROL Sales]** > **[!UICONTROL Operations]** > **[!UICONTROL Orders]** > **[!UICONTROL Actions]** > **[!UICONTROL Create]** > **[!UICONTROL Can Spend Store Credit]** consente agli utenti di applicare il credito dello store durante la [creazione di un ordine](../stores-purchase/customer-account-create-order.md). Senza di esso, la casella di controllo **[!UICONTROL Use Store Credit]** non è visibile.

Gli utenti e le integrazioni amministratori che utilizzano l&#39;API REST necessitano della risorsa **[!UICONTROL Can Spend Store Credit]** per applicare il credito dello store a un carrello o per effettuare un ordine per un carrello a cui è già stato applicato il credito dello store. Per ulteriori informazioni, vedere [Memorizza credito](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/store-credit/).

## Visualizza il saldo a credito

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Individuare il cliente nella griglia.

1. Nella colonna _Azione_ fare clic su **[!UICONTROL Edit]**.

1. Scorrere la pagina _[!UICONTROL Customer View]_&#x200B;e visualizzare **[!UICONTROL Store Credit Balance]**&#x200B;nella parte inferiore.

![Memorizza saldo credito](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Aggiorna saldo credito negozio

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Individuare il cliente nella griglia.

1. Nella colonna _Azione_ fare clic su **[!UICONTROL Edit]**.

1. Nel pannello a sinistra, scegli **[!UICONTROL Store Credit]**.

1. Scegliere il sito Web (vetrina) che si desidera associare al saldo.

1. Per **[!UICONTROL Update Balance]**, immettere il nuovo valore.

1. Per notificare al cliente l&#39;aggiornamento del saldo, selezionare la casella di controllo **[!UICONTROL Notify Customer by Email]** e scegliere la visualizzazione dello store da **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Immetti **[!UICONTROL Comment]** sulla modifica.

1. Al termine degli aggiornamenti, fare clic su **[!UICONTROL Save and Continue Edit]** o **[!UICONTROL Save Customer]**.

Il saldo aggiornato dovrebbe essere visualizzato in **[!UICONTROL Balance History]**.

## Applicare un saldo a credito a un ordine come amministratore del negozio

In qualità di amministratore del negozio, puoi eseguire varie operazioni per conto di un cliente, incluso l’invio di ordini. Quando [crei un ordine](../stores-purchase/customer-account-create-order.md), puoi applicare un saldo a credito del negozio dovuto al cliente. Il saldo disponibile viene visualizzato nella sezione _Informazioni su pagamento e spedizione_. Selezionare la casella di controllo **[!UICONTROL Use Store Credit]** per applicare il saldo o una parte del saldo se il totale dell&#39;ordine è inferiore.

![Applica il saldo a credito dell&#39;archivio all&#39;ordine](assets/store-credit-apply.png){width="500" zoomable="yes"}

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."} La casella di controllo **[!UICONTROL Use Store Credit]** viene visualizzata solo quando il ruolo utente include la risorsa **[!UICONTROL Can Spend Store Credit]**. Vedi [Archivia risorse ruolo di credito](#store-credit-role-resources).

## Applica credito del negozio durante l&#39;acquisto

Se è presente un saldo a credito per la sede, il cliente può applicare il credito del negozio al saldo dell&#39;ordine prima di inserire l&#39;ordine nella vetrina.

1. Il cliente visualizza l&#39;importo del credito del negozio disponibile.

   Durante il passaggio _Verifica e pagamenti_, l&#39;importo disponibile viene visualizzato in _[!UICONTROL Store Credit]_.

1. Per applicare l&#39;importo all&#39;ordine, fare clic su **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >Il totale dell&#39;ordine viene ricalcolato e l&#39;importo del credito dell&#39;archivio applicato viene visualizzato in _[!UICONTROL Order Summary]_.

   ![Saldo a credito archiviato applicato all&#39;ordine](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Quando è pronto, fa clic su **[!UICONTROL Place Order]**.
