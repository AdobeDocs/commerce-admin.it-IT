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

Gli utenti dell’azienda vengono assegnati dall’amministratore dell’azienda e sono visibili dall’amministratore in _[!UICONTROL Customers]_griglia per tipo di cliente,_[!UICONTROL Company User]_. Si tratta in genere di acquirenti con diversi livelli di autorizzazione per accedere ai servizi e alle risorse del punto vendita.

L’amministratore della società configura innanzitutto [struttura aziendale](account-company-structure.md), quindi completa le seguenti attività, in base alle esigenze:

- Creare utenti aziendali e assegnare utenti ai team

- Definire ruoli e autorizzazioni e assegnare utenti ai ruoli

>[!IMPORTANT]
>
>Gli utenti dell’azienda possono essere aggiunti, modificati o rimossi solo dall’amministratore dell’azienda. Impossibile annullare la rimozione perché l&#39;utente viene rimosso dalla struttura dell&#39;azienda.

## Aggiungi utenti società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Users]**.

   ![Utenti società](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Clic **[!UICONTROL Add New User]** ed effettua quanto segue:

   - Entra nel **[!UICONTROL Job Title]** del nuovo utente.

   - Scegli la **[!UICONTROL User Role]** se sono definiti i ruoli e le autorizzazioni. In caso contrario, possono tornare in un secondo momento per assegnare il ruolo.

     ![Aggiungi nuovo utente](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Completa i campi rimanenti in base alle esigenze dell’utente:

      - **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   Per impostazione predefinita, il **[!UICONTROL Status]** dell’account è `Active`.

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Ripete il processo per creare tutti gli utenti aziendali necessari.

   I nuovi utenti vengono visualizzati nell&#39;elenco Utenti società insieme all&#39;Amministratore società.

Per risparmiare tempo durante il primo ordine, l&#39;amministratore della società può ricordare a ogni utente della società di aggiungere l&#39;indirizzo di fatturazione e spedizione predefinito della società [rubrica](../customers/account-dashboard-address-book.md).

## Modifica utenti società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Users]**.

1. Trova il record utente da aggiornare e fa clic su **[!UICONTROL Edit]**.

1. Apporta le modifiche necessarie.

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Rimuovere un utente della società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Structure]**.

1. Seleziona l&#39;utente della società nella struttura della società.

1. Clic **[!UICONTROL Delete Selected]**.

   ![Elimina utente](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL Delete]**.

In Admin (Amministratore), l’utente della società rimane elencato in [Clienti](../customers/customers-all.md) ma con una griglia `Inactive` stato.

## Descrizioni dei campi

| Campo | Descrizione |
|--------------|---------------|
| [!UICONTROL Job Title] | Qualifica dell&#39;utente dell&#39;azienda. |
| [!UICONTROL User Role] | Il [ruolo](account-company-roles-permissions.md) assegnato all’utente della società. Opzioni: `Default User` / (altri ruoli) |
| [!UICONTROL First Name] | Il nome dell’utente dell’azienda. |
| [!UICONTROL Last Name] | Cognome dell&#39;utente della società. |
| [!UICONTROL Email] | L’indirizzo e-mail dell’utente dell’azienda. |
| [!UICONTROL Phone Number] | Numero di telefono dell&#39;utente della società. |
| [!UICONTROL Status] | Stato dell&#39;account utente della società. Opzioni: `Active` / `Inactive` |

{style="table-layout:auto"}
