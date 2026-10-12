---
title: Assegnare un amministratore società
description: Scopri come assegnare un account utente della società come amministratore della società designato per l’account aziendale.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: 'https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
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
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%
---
# Assegnare un amministratore società

L’amministratore della società viene inizialmente assegnato al momento della creazione dell’account aziendale e può essere modificato solo da un amministratore dello store dell’amministratore.

- A ogni società può essere assegnato un solo amministratore.
- Un utente della società può essere l’amministratore di una sola società.
- Le modifiche all’amministratore della società assegnato devono essere completate da un amministratore del negozio dell’amministratore.

## Modifica amministratore società assegnato

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Aziende](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Trovare la società nell&#39;elenco e quindi fare clic su **[!UICONTROL Edit]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Company Admin]**.

   ![Amministratore società](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Immettere **[!UICONTROL Job Title]** del nuovo amministratore società.

   Questa azione cancella il modulo e i campi obbligatori _[!UICONTROL First Name]_&#x200B;e_[!UICONTROL Last Name]_ sono evidenziati.

1. Immettere l&#39;indirizzo **[!UICONTROL Email]** del nuovo amministratore della società.

   Se il sistema non trova l&#39;indirizzo e-mail nel database, viene richiesto di confermare la sostituzione dell&#39;amministratore della società.

   - Se non esiste un account utente per il nuovo amministratore della società, il sistema crea un account di tipo `Company Admin`.

   - Se l&#39;account utente esiste nel sistema, viene spostato nella posizione di amministratore della società nella struttura della società.

1. Immettere **[!UICONTROL First Name]** e **[!UICONTROL Last Name]** ed eventuali altre informazioni applicabili per il nuovo amministratore della società.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   L’account individuale dell’amministratore della società precedente rimane nel sistema come account utente attivo, assegnato al ruolo utente predefinito. Se si tratta dell&#39;unica società associata all&#39;account utente, il tipo di account cambia da *[!UICONTROL Company user]* a *[!UICONTROL Individual user]*.

   Il sistema invia una notifica e-mail della modifica agli amministratori della nuova e della società precedente.

