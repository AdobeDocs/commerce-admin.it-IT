---
title: Assegnare un gruppo di clienti a una società
description: Scopri come assegnare un gruppo di clienti a un account aziendale nel tuo store di Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Assegnare un gruppo di clienti a una società

L’assegnazione di un gruppo di clienti a un’azienda equivale essenzialmente all’assegnazione di un catalogo condiviso. Se il Catalogo condiviso non è abilitato [nella configurazione](enable-basic-features.md), a una società viene assegnato un gruppo di clienti anziché un Catalogo condiviso.

- È possibile assegnare un solo gruppo di clienti o un catalogo condiviso alla volta a una società. Impossibile eliminare un gruppo di clienti associato a un catalogo condiviso.
- La modifica del gruppo di clienti assegnato alla società aggiorna i profili di tutti i membri della società.
- Se l&#39;assegnazione del gruppo di clienti viene cambiata da un catalogo condiviso a un gruppo di clienti normale, i membri della società perdono l&#39;accesso al catalogo condiviso e il catalogo principale diventa disponibile dalla vetrina.
- Dopo aver modificato il gruppo della società, un utente della società deve disconnettersi e accedere allo Storefront per visualizzare i nuovi prezzi nel catalogo.

## Modificare il gruppo di clienti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Trovare la società nella griglia e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

   ![Modifica società](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Nella pagina dell&#39;azienda, scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advanced Settings]**.

1. Imposta il **[!UICONTROL Customer Group]** appropriato.

   L&#39;elenco [!UICONTROL Customer Group] include tutti i cataloghi condivisi esistenti, anche se Cataloghi condivisi è disabilitato nella configurazione.

   ![Cambia gruppo clienti o catalogo condiviso](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL Proceed]**.

1. Fare clic su **[!UICONTROL Save]**.
