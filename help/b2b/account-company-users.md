---
title: Gestire gli account utente aziendali
description: Scopri gli account utente dell’azienda e come funzionano nell’account aziendale associato.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Gestire gli account utente aziendali

Gli utenti della società vengono assegnati dall&#39;amministratore della società e sono visibili dall&#39;amministratore nella griglia _[!UICONTROL Customers]_in base al tipo di cliente,_[!UICONTROL Company User]_. Si tratta in genere di acquirenti con diversi livelli di autorizzazione per accedere ai servizi e alle risorse del punto vendita.

L&#39;amministratore della società configura innanzitutto la [struttura della società](account-company-structure.md) e quindi completa le seguenti attività, in base alle esigenze:

- Creare utenti aziendali e assegnare utenti ai team

- Definire ruoli e autorizzazioni e assegnare utenti ai ruoli

>[!IMPORTANT]
>
>Gli utenti dell’azienda possono essere aggiunti, modificati o rimossi solo dall’amministratore dell’azienda. Impossibile annullare la rimozione perché l&#39;utente viene rimosso dalla struttura dell&#39;azienda.

## Aggiungi utenti società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Users]**.

   ![Utenti società](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Add New User]** ed effettua le seguenti operazioni:

   - Immette **[!UICONTROL Job Title]** del nuovo utente.

   - Seleziona il **[!UICONTROL User Role]** appropriato se sono definiti i ruoli e le autorizzazioni. In caso contrario, possono tornare in un secondo momento per assegnare il ruolo.

     ![Aggiungi nuovo utente](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Completa i campi rimanenti in base alle esigenze dell’utente:

      - **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   Per impostazione predefinita, il **[!UICONTROL Status]** dell&#39;account è `Active`.

1. Al termine, fa clic su **[!UICONTROL Save]**.

1. Ripete il processo per creare tutti gli utenti aziendali necessari.

   I nuovi utenti vengono visualizzati nell&#39;elenco Utenti società insieme all&#39;Amministratore società.

Per risparmiare tempo durante il primo ordine, l&#39;amministratore della società può ricordare a ogni utente della società di aggiungere l&#39;indirizzo predefinito di fatturazione e spedizione della società alla [rubrica](../customers/account-dashboard-address-book.md).

## Modifica utenti società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Users]**.

1. Trova il record utente da aggiornare e fa clic su **[!UICONTROL Edit]**.

1. Apporta le modifiche necessarie.

1. Al termine, fa clic su **[!UICONTROL Save]**.

## Rimuovere un utente della società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Structure]**.

1. Seleziona l&#39;utente della società nella struttura della società.

1. Clic su **[!UICONTROL Delete Selected]**.

   ![Elimina utente](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL Delete]**.

Nell&#39;amministratore, l&#39;utente della società rimane elencato nella griglia [Clienti](../customers/customers-all.md), ma con uno stato `Inactive`.

## Descrizioni dei campi

| Campo | Descrizione |
|--------------|---------------|
| [!UICONTROL Job Title] | Qualifica dell&#39;utente dell&#39;azienda. |
| [!UICONTROL User Role] | Il [ruolo](account-company-roles-permissions.md) assegnato all&#39;utente della società. Opzioni: `Default User` / (altri ruoli) |
| [!UICONTROL First Name] | Il nome dell’utente dell’azienda. |
| [!UICONTROL Last Name] | Cognome dell&#39;utente della società. |
| [!UICONTROL Email] | L’indirizzo e-mail dell’utente dell’azienda. |
| [!UICONTROL Phone Number] | Numero di telefono dell&#39;utente della società. |
| [!UICONTROL Status] | Stato dell&#39;account utente della società. Opzioni: `Active` / `Inactive` |

{style="table-layout:auto"}
