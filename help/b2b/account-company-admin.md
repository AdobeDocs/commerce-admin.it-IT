---
title: Assegnare un amministratore società
description: Scopri come assegnare un account utente della società come amministratore della società designato per l’account aziendale.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Assegnare un amministratore società

L’amministratore della società viene inizialmente assegnato al momento della creazione dell’account aziendale e può essere modificato solo da un amministratore dello store dell’amministratore.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Trovare la società nell&#39;elenco e fare clic su **[!UICONTROL Edit]**.

   ![Aziende](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Company Admin]**.

   ![Amministratore società](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Immettere **[!UICONTROL Job Title]** del nuovo amministratore della società e fare clic su **[!UICONTROL Proceed]** per continuare.

   Questa azione cancella il modulo e i campi obbligatori _[!UICONTROL First Name]_e_[!UICONTROL Last Name]_ sono evidenziati.

1. Immettere l&#39;indirizzo **[!UICONTROL Email]** del nuovo amministratore della società.

   Se il sistema non trova l&#39;indirizzo e-mail nel database, viene richiesto di confermare la sostituzione dell&#39;amministratore della società.

   - Se non esiste un account utente per il nuovo amministratore della società, il sistema crea un account di tipo `Company Admin`.

   - Se l&#39;account utente esiste nel sistema, viene spostato nella posizione di amministratore della società nella struttura della società.

1. Immettere **[!UICONTROL First Name]** e **[!UICONTROL Last Name]** ed eventuali altre informazioni applicabili per il nuovo amministratore della società.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   L’account individuale dell’ex amministratore della società rimane nel sistema come account utente individuale attivo nella struttura della società, assegnato al ruolo utente predefinito.

   Il sistema invia una notifica e-mail della modifica agli amministratori della nuova e della società precedente.
