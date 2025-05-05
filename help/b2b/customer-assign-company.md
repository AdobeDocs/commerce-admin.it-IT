---
title: Aggiungere utenti a un account società
description: Scopri come aggiungere un cliente esistente a un account aziendale.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Aggiungere utenti a un account società

Quando è abilitato nella configurazione, l’amministratore aziendale aggiunge e gestisce gli utenti aziendali dalla vetrina. Tuttavia, gli account degli utenti aziendali possono anche essere aggiunti e gestiti dall’amministratore.

Se necessario, puoi assegnare un utente a più di un’azienda. Ad esempio, se gli acquirenti B2B supportano più aziende, puoi aggiungere i loro account utente a tutte le aziende con cui lavorano. Nella vetrina, gli acquirenti assegnati a più società possono passare da un account aziendale all&#39;altro scegliendo una delle società disponibili nel menu *[!UICONTROL Company]*.

![Associa alla società](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>Se un individuo ha già un account personale presso il tuo negozio e successivamente va a lavorare per un&#39;azienda, non assegnare l&#39;account individuale della persona all&#39;azienda. Crea invece un account utente aziendale per la persona con un indirizzo e-mail aziendale.

## Aggiungi un utente società

Quando aggiungi un utente della società, la prima società associata all’account utente è quella predefinita.

1. Nella barra laterale di amministrazione, vai a **[!UICONTROL Customers > All Customers]**.

1. Fare clic su **[!UICONTROL Add new customer]**.

1. Configura il nuovo account.

   1. Specificare lo stato iniziale dell&#39;account impostando l&#39;interruttore **[!UICONTROL Customer Active]**.

      Attivalo per attivare immediatamente l’account o disattivalo per creare un account inattivo.

   1. Selezionare l&#39;ambito del sito Web dall&#39;elenco **[!UICONTROL Associate to Website]**.

   1. Fare clic su **[!UICONTROL Associate to Company]** per visualizzare le società disponibili.

      ![Associa alla società](./assets/company-assign-customer-account.png){width="675"}

      Se necessario, filtrare l&#39;elenco digitando le prime lettere del nome della società nella casella di immissione.

   1. Nell&#39;elenco selezionare una o più società a cui si desidera assegnare il cliente e fare clic su **[!UICONTROL Done]**.

      Gli utenti aziendali vengono aggiunti automaticamente al gruppo di clienti (o [catalogo condiviso](catalog-shared.md)) per ogni azienda associata al proprio account.

   1. Immettere le informazioni obbligatorie sull&#39;account utente: **[!UICONTROL First Name]**, **[!UICONTROL Last Name]** e **[!UICONTROL Email]**.

   1. Consenti ai rappresentanti commerciali di accedere alla vetrina per conto del cliente abilitando **[!UICONTROL Allow remote shopping assistance]**.

   1. Applicare le modifiche facendo clic su **[!UICONTROL Save Customer]**.

      ![Griglia clienti con assegnazioni società](./assets/company-assign-user-assignments.png){width="675"}

[!UICONTROL Customers grid] mostra una riga separata per ogni società a cui l&#39;utente è assegnato. Le seguenti colonne vengono aggiornate.

- La colonna _[!UICONTROL Customer Type]_&#x200B;viene aggiornata per mostrare il ruolo assegnato all&#39;utente.

  Se è la prima volta che il cliente viene assegnato a una società, la colonna _[!UICONTROL Customer Type]_&#x200B;viene aggiornata da&#x200B;_[!UICONTROL Individual user]_ a _[!UICONTROL Company User]_.

- La colonna _[!UICONTROL Group]_&#x200B;cambia al nome del gruppo di clienti (o del catalogo condiviso) assegnato alla società.

- Nella colonna _[!UICONTROL Company]_&#x200B;viene visualizzato il nome della società a cui è ora associato il profilo cliente.

## Assegnare un utente a uno o più account società

Quando si assegna un nuovo utente, la prima società associata all&#39;account utente è quella predefinita.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trovare il cliente nella griglia e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. Nel pannello a sinistra, scegli **[!UICONTROL Account Information]**.

1. Dall&#39;elenco **[!UICONTROL Associate to Company]**, selezionare una o più società da assegnare all&#39;utente della società e fare clic su **[!UICONTROL Done]**.

1. Applicare le modifiche facendo clic su **[!UICONTROL Save Customer]**.

## Rimuovere l&#39;assegnazione della società da un account utente

Se si rimuove un’azienda da un profilo utente, viene revocato l’accesso dell’utente a tale azienda. I dati utente rimangono accessibili nell’amministratore. Se si rimuovono tutte le assegnazioni della società, _[!UICONTROL Customer Type]_&#x200B;diventa *[!UICONTROL Individual user]*&#x200B;e le funzionalità B2B vengono disabilitate per l&#39;account.

1. Dalla griglia Cliente nell’amministratore, modifica il profilo cliente da aggiornare.

1. Nella sezione *[!UICONTROL Account Information], rimuovere una società assegnata dal campo **[!UICONTROL Associate to Company]** facendo clic su **[!UICONTROL X]** nell&#39;etichetta del nome della società.

1. Applicare le modifiche facendo clic su **[!UICONTROL Save Customer]**.

>[!NOTE]
>
>Se a un utente della società viene assegnato il ruolo di amministratore società, non sarà possibile assegnare l&#39;associazione società a tale utente finché non si aggiorna l&#39;account Società per assegnare un nuovo amministratore società.
