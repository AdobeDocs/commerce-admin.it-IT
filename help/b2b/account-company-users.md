---
title: Gestire gli account utente aziendali
description: Scopri gli account utente dell’azienda e come funzionano nell’account aziendale associato.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 9c16d7a3909598328cc42bbcbf39fc14ae6a9eb9
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Gestire gli account utente aziendali

Nella vetrina, gli utenti aziendali vengono assegnati dall&#39;amministratore della società e sono visibili dalla pagina _[!UICONTROL Company Users]_. Si tratta in genere di acquirenti con diversi livelli di autorizzazione per accedere ai servizi e alle risorse del punto vendita.

L&#39;amministratore della società configura innanzitutto la [struttura della società](account-company-structure.md) e quindi completa le seguenti attività, in base alle esigenze:

- Creare utenti aziendali e assegnare utenti ai team

- Definire ruoli e autorizzazioni e assegnare utenti ai ruoli

Solo l’amministratore dell’azienda può aggiungere, modificare, disattivare o eliminare utenti dell’azienda.

- Quando un utente viene rimosso, lo stato dell&#39;account cambia in *inattivo* e il cliente non può più accedere alla società. Gli amministratori possono comunque accedere a tutto il contenuto associato all’utente. L&#39;amministratore dell&#39;account può ripristinare l&#39;accesso modificando lo stato dell&#39;account in *[!UICONTROL Active]* dalla pagina [!UICONTROL Company Users].

- Quando un account utente viene eliminato, l’account e l’eventuale contenuto associato vengono eliminati dalla vetrina. Questa azione non può essere ripristinata.

## Aggiungi utenti società

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Users]**.

   ![Utenti società](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Fai clic su **[!UICONTROL Add New User]** ed effettua le seguenti operazioni:

   - Immette **[!UICONTROL Job Title]** del nuovo utente.

   - Seleziona il **[!UICONTROL User Role]** appropriato se sono definiti i ruoli e le autorizzazioni. In caso contrario, possono tornare in un secondo momento per assegnare il ruolo.

     ![Aggiungi nuovo utente](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Aggiunge le informazioni utente nei campi rimanenti:
      - **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Work Phone Number]**

   Per impostazione predefinita, il **[!UICONTROL Status]** dell&#39;account è `Active`.

1. Al termine, fa clic su **[!UICONTROL Save]**.

1. Ripete il processo per creare tutti gli utenti aziendali necessari.

   I nuovi utenti vengono visualizzati nell&#39;elenco Utenti società insieme all&#39;Amministratore società.

Per risparmiare tempo durante il primo ordine, l&#39;amministratore della società può ricordare a ogni utente della società di aggiungere l&#39;indirizzo predefinito di fatturazione e spedizione della società alla [rubrica](../customers/account-dashboard-address-book.md).

## Rimuovi un utente da [!UICONTROL Company structure]

Gli amministratori della società possono rimuovere un utente da [!UICONTROL Company Structure].

Dopo la rimozione di un account, lo stato dell&#39;account utente diventa *inattivo* e l&#39;utente non può più accedere alla vetrina.
L’amministratore può riattivare un account modificando le informazioni sull’account utente dalla pagina Utenti società.

1. Dalla vetrina, l’amministratore della società accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Structure]**.

1. Seleziona l&#39;utente della società nella struttura della società.

1. Clic su **[!UICONTROL Remove from Structure]**.

   ![Elimina utente](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL Remove]**.

   Nell&#39;amministratore, l&#39;utente della società rimane elencato nella griglia [Clienti](../customers/customers-all.md), ma con uno stato `Inactive`.

## Visualizzare e gestire gli account utente aziendali

Gli amministratori della società possono visualizzare e gestire gli account utente della società utilizzando i filtri di visualizzazione nella pagina [!UICONTROL Company Users].

![Utenti società](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- Visualizzare solo gli utenti inattivi selezionando **[!UICONTROL Show Inactive Users]**.
- Visualizzare solo gli utenti attivi selezionando **[!UICONTROL Show Active Users]**.
- Visualizza tutti gli utenti selezionando **[!UICONTROL Show All Users]**.

L&#39;amministratore della società può gestire un singolo account utilizzando la riga *[!UICONTROL Actions]* per modificare le informazioni sull&#39;account, gestire lo stato dell&#39;account o eliminare un account.

### Modifica informazioni account utente società

Gli amministratori aziendali possono aggiornare le informazioni sul profilo dell’account utente e modificare lo stato dell’account.

1. Nella pagina [!UICONTROL Company Users], trovare l&#39;account utente da aggiornare. Fare clic su **[!UICONTROL Edit]**.

1. Apportare le modifiche necessarie alle informazioni sull&#39;account utente, inclusa la modifica dello stato dell&#39;account.

1. Applicare le modifiche facendo clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Se si modifica un account utente della società e si nota che nel profilo mancano le informazioni obbligatorie relative all&#39;account, ad esempio il titolo della mansione e il numero di telefono dell&#39;ufficio, ciò indica che l&#39;account è stato aggiunto da un amministratore del sito Commerce. Questi account non possono essere modificati dalla vetrina. Per aggiornare le informazioni o modificare lo stato dell&#39;account, contattare l&#39;amministratore del sito.

### Disattivare o eliminare un account attivo

1. Nella pagina [!UICONTROL Company Users], trovare l&#39;account utente da aggiornare. Fare clic su **[!UICONTROL Manage]**.

   ![Gestisci utente dalla pagina Utenti società](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. Quando richiesto, disattiva o elimina l’account utente in base alle esigenze.

>[!IMPORTANT]
>
>Quando si elimina un account utente della società, vengono rimossi dal sistema l’account e tutto il contenuto associato. Questa azione non può essere ripristinata.

## Descrizioni dei campi del profilo dell’account utente della società

| Campo | Descrizione |
|--------------------------------|---------------|
| [!UICONTROL Job Title] | Qualifica dell&#39;utente dell&#39;azienda. |
| [!UICONTROL User Role] | Il [ruolo](account-company-roles-permissions.md) assegnato all&#39;utente della società. Opzioni: `Default User` / (altri ruoli) |
| [!UICONTROL First Name] | Il nome dell’utente dell’azienda. |
| [!UICONTROL Last Name] | Cognome dell&#39;utente della società. |
| [!UICONTROL Email] | L’indirizzo e-mail dell’utente dell’azienda. |
| [!UICONTROL Work Phone Number] | Numero di telefono aziendale dell&#39;utente. |
| [!UICONTROL Status] | Stato dell&#39;account utente della società. Opzioni: `Active` / `Inactive` |

{style="table-layout:auto"}
