---
title: Impostazione dell’autenticazione a due fattori per gli account utente
description: Scopri come impostare l’autenticazione a due fattori durante l’accesso iniziale da parte dell’amministratore e autenticare la tua identità utilizzando un’app per dispositivi supportata.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Impostazione dell’autenticazione a due fattori per gli account utente

Queste istruzioni mostrano come impostare l’autenticazione a due fattori durante il primo accesso a Adobe Commerce o al Magento Open Source e come autenticare la tua identità utilizzando le app e i dispositivi seguenti.

Per istruzioni complete, consulta [Accesso amministratore](../getting-started/admin-signin.md).

>[!NOTE]
>
>Archivi che hanno abilitato [!DNL Adobe Identity Management Services] Per l’autenticazione IMS, Adobe Commerce nativo e Magento Open Source 2FA sono disabilitati. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza Commerce con le credenziali di Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [[!DNL Adobe Identity Management Service] Panoramica dell’integrazione di (IMS)](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Passaggio 1: configurazione [!DNL Google Authenticator]

1. Immetti le credenziali del tuo account e accedi a _Amministratore_. Viene visualizzata una nuova schermata di autenticazione con un codice QR.

1. Apri **[!UICONTROL Google Authenticator]** sul tuo dispositivo mobile.

1. Fare clic sul segno più ( **+** ) per aggiungere una voce e allineare la casella rossa con il codice QR da scansionare con la fotocamera sullo smartphone.

1. Quando il telefono riconosce il codice QR e aggiunge una voce, inserisci tale codice di 6 cifre nel _Amministratore_ **[!UICONTROL Authenticator code]** campo.

1. Al termine, fai clic su **[!UICONTROL Confirm]**.

   ![Codice QR Google Authenticator](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Passaggio 2: Accedi con [!DNL Google Authenticator]

1. Immetti le credenziali del tuo account e accedi a Commerce _Amministratore_.

   ![Autenticatore Google - accesso](./assets/storefront-2fa-google-code.png){width="300"}

1. Apri [!DNL Google Authenticator] sul dispositivo mobile.

1. Quando richiesto, immettere il codice di autenticazione a sei cifre.

1. Per salvare l’autenticazione per gli accessi futuri, seleziona la **[!UICONTROL Trust this device, do not ask again]** casella di controllo.

1. Al termine, fai clic su **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] offre una versione di prova gratuita e addebiti in base al numero di utenti associati all’account. Segui le loro [istruzioni per configurare l’account e scaricare l’app](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Passaggio 1: configurazione [!DNL Duo Security]

1. Immetti le credenziali del tuo account e accedi a _Amministratore_.

1. Quando [!DNL Duo] Viene visualizzata la pagina di configurazione, fare clic su **[!UICONTROL Start setup]** ed effettuare le seguenti operazioni:

   ![Esempio di vetrina - Configurazione Duo](./assets/storefront-2fa-duo-user1.png){width="300"}

1. Seleziona il dispositivo.

1. Quando richiesto, immetti il numero di telefono e fai clic su **[!UICONTROL Continue]**.

   In questo esempio viene richiesto il numero di telefono perché si sta utilizzando un dispositivo mobile.

1. Quando viene richiesto di installare [!DNL Duo Mobile] per il tipo di telefono, fai clic su **[!UICONTROL I have Duo Mobile]**.

1. Apri [!DNL Duo Mobile] e scansiona il codice QR per sincronizzare l’autenticatore con Adobe Commerce. Al termine dell’attivazione viene visualizzato un segno di spunta.

1. Per configurare le impostazioni per il dispositivo, scegliere l&#39;azione da eseguire all&#39;accesso.

   - `Ask me to choose an authenticator method` — consente all&#39;utente di selezionare quando effettua l&#39;accesso e l&#39;autenticazione in _Amministratore_.
   - `Automatically send this device a Duo Push` - Invia un messaggio al dispositivo per accettare o negare l&#39;accesso.
   - `Automatically call this device` — chiama e fornisce un passcode da immettere per l&#39;accesso.

   ![Azioni di verifica Duo](./assets/storefront-2fa-duo-user7.png){width="300"}

### Passaggio 2: Accedi con [!DNL Duo Security]

L&#39;esempio seguente mostra le opzioni per `Ask me to choose an authenticator method`:

1. Quando richiesto, immetti _Amministratore_ credenziali per accedere.

   ![Duo - accesso](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Scegliere il metodo da utilizzare per l&#39;autenticazione:

   - `Send Me a Push` — Fai clic per ricevere un avviso push per [!DNL Duo Mobile]. Accetta per autenticare.
   - `Call Me` — Fare clic su questa opzione, ricevere una chiamata con un codice e immettere il codice di accesso.
   - `Enter a Passcode` — Fare clic su questa opzione per ricevere e immettere un codice d&#39;accesso.

1. Completa il push o il codice per accedere completamente a _Amministratore_.

## [!DNL Authy]

[!DNL Authy] offre gratuitamente la propria app e il proprio servizio agli utenti. Segui le istruzioni per scaricare e configurare l’app per il dispositivo o il browser. Per ulteriori informazioni, consulta [[!DNL Authy] documentazione](https://authy.com/features/setup/).

### Passaggio 1: configurare Authy

1. Immetti le credenziali del tuo account e accedi a _Amministratore_.

   ![[!DNL Authy] registrazione](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Quando ti viene richiesto di registrarti su Authy, effettua le seguenti operazioni:

   - Seleziona il tuo paese.

   - Immetti il numero di telefono.

   - Seleziona la **[!UICONTROL Verification method]**: `SMS` o `Call Me`

   Clic **[!UICONTROL Continue]**. Un messaggio viene inviato al telefono tramite SMS o chiamata.

1. Immettere il codice di verifica ricevuto e fare clic su **[!UICONTROL Verify]**.

1. Al termine, fai clic su **[!UICONTROL Confirm]**.

   ![[!DNL Authy] codice di verifica](./assets/storefront-2fa-authy-verify.png){width="300"}

### Passaggio 2: Accedi con [!DNL Authy]

1. Immetti le credenziali del tuo account e accedi a _Amministratore_.

   ![[!DNL Authy] - accesso](./assets/storefront-2fa-authy-access.png){width="300"}

1. Scegliere uno dei metodi seguenti per l&#39;autenticazione:

   - `Use one touch` - Invia un avviso al tuo [!DNL Authy] app. Nell’app, accetta l’accesso.
   - `Use authy token` — Richiede di immettere un codice dal [!DNL Authy] app.

1. In caso di problemi di accesso, scegliere il metodo da utilizzare per ricevere il codice. Quindi, inserisci il codice che ricevi per accedere al _Amministratore_.

   L’app include questi metodi di emergenza aggiuntivi.

   - `Send me a code via SMS` — Viene inviato un SMS al dispositivo mobile configurato.
   - `Send me a code via phone call` — L&#39;utente riceve una telefonata con un codice.

   Il tuo account viene verificato e aperto.

## U2F ([!DNL Yubikey] e altri dispositivi)

Segui le istruzioni del provider di soluzioni per configurare il dispositivo U2F. Per ulteriori informazioni, consulta la documentazione del fornitore, ad esempio [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) da [!UICONTROL Yubico].

1. Immetti le credenziali del tuo account e accedi a _Amministratore_.

   ![Accesso chiave U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Premere il tasto.

   L’autenticazione si attiva immediatamente e apre il _Amministratore_.

1. Inserisci il **[!UICONTROL U2F key]** su una porta USB del computer.
