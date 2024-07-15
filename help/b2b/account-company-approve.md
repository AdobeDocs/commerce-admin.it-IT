---
title: Approvare un account società
description: Scopri come approvare le richieste dell’account aziendale nell’amministratore.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Approvare un account società

Lo stato delle richieste ricevute dalla vetrina per creare una società è `Pending Approval` finché la richiesta non viene esaminata dall&#39;amministratore dello store e approvata o rifiutata. Lo stato di un account società può essere impostato su uno dei seguenti:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

È inoltre possibile utilizzare il controllo [Azioni](account-company-manage.md) per approvare più richieste aziendali.

![Approvazione in sospeso](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Approva un account società in sospeso

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   È possibile utilizzare il selettore _[!UICONTROL Columns]_sopra la griglia per visualizzare la colonna **[!UICONTROL Status]**.

1. Nella colonna _[!UICONTROL Action]_fare clic su **[!UICONTROL Edit]**.

1. Imposta **[!UICONTROL Company Status]** su `Active`.

   ![Imposta lo stato della società](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL Change status]**.

   L’amministratore della società riceve una notifica e-mail che informa che la società è ora attiva.

1. Se applicabile, impostare **[!UICONTROL Sales Representative]** su un account utente amministratore specifico.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Account Information]** e utilizzare il campo **[!UICONTROL Comment]** per immettere note sull&#39;account.

   I commenti non sono visibili dalla vetrina.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   Viene inviata un’e-mail di conferma all’amministratore della società e della stessa che l’account della società è approvato.

## Stato dell’azienda

| Stato | Descrizione |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | La società è approvata e può essere gestita dalla vetrina dall&#39;amministratore della società. |
| [!UICONTROL Pending Approval] | La richiesta di creare un account società è stata inviata dalla vetrina, ma non è ancora stata rivista. |
| [!UICONTROL Rejected] | La richiesta di creazione di un account società è stata rifiutata dall&#39;amministratore dello store. |
| [!UICONTROL Blocked] | L&#39;account aziendale non è più in buono stato. Il cliente può accedere all’account dalla vetrina, ma non può effettuare acquisti. |

{style="table-layout:auto"}
