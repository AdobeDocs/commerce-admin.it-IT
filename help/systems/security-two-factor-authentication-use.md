---
title: Impostazione dell’autenticazione a due fattori per gli account utente
description: Scopri come impostare l’autenticazione a due fattori durante l’accesso iniziale da parte dell’amministratore e autenticare la tua identità utilizzando un’app per dispositivi supportata.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: dc6e5fc7c0996af30bae6374cd7c9879902b9235
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Impostazione dell’autenticazione a due fattori per gli account utente

Queste istruzioni mostrano come impostare l’autenticazione a due fattori durante il primo accesso a Adobe Commerce o Magento Open Source e come autenticare la tua identità utilizzando le app e i dispositivi seguenti.

Per istruzioni complete, vedere [Accesso amministratore](../getting-started/admin-signin.md).

>[!NOTE]
>
>Gli archivi che hanno abilitato l&#39;autenticazione [!DNL Adobe Identity Management Services] (IMS) hanno Adobe Commerce nativo e Magento Open Source 2FA disabilitati. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza di Commerce con le credenziali Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Vedi Panoramica sull&#39;integrazione di [[!DNL Adobe Identity Management Service] (IMS)](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Passaggio 1: configurare [!DNL Google Authenticator]

1. Immetti le credenziali del tuo account e accedi a _Admin_. Viene visualizzata una nuova schermata di autenticazione con un codice QR.

1. Apri l&#39;app **[!UICONTROL Google Authenticator]** sul tuo dispositivo mobile.

1. Fare clic sul segno più ( **+** ) per aggiungere una voce e allineare la casella rossa con il codice QR per eseguire la scansione con la fotocamera sullo smartphone.

1. Quando il telefono riconosce il codice QR e aggiunge una voce, inserisci il codice a 6 cifre nel _campo Amministratore_**[!UICONTROL Authenticator code]**.

1. Al termine, fare clic su **[!UICONTROL Confirm]**.

   ![Codice QR Google Authenticator](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Passaggio 2: accedere con [!DNL Google Authenticator]

1. Immetti le credenziali del tuo account e accedi a Commerce _Admin_.

   ![Autenticatore Google - accesso](./assets/storefront-2fa-google-code.png){width="300"}

1. Apri [!DNL Google Authenticator] sul tuo dispositivo mobile.

1. Quando richiesto, immettere il codice di autenticazione a sei cifre.

1. Per salvare l&#39;autenticazione per gli accessi futuri, selezionare la casella di controllo **[!UICONTROL Trust this device, do not ask again]**.

1. Al termine, fare clic su **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] offre una versione di prova gratuita e addebiti in base al numero di utenti associati all&#39;account. Segui le [istruzioni per configurare il tuo account e scaricare l&#39;app](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Passaggio 1: configurare [!DNL Duo Security]

1. Immetti le credenziali del tuo account e accedi a _Admin_.

1. Quando viene visualizzata la pagina di installazione di [!DNL Duo], fare clic su **[!UICONTROL Get Started]** ed eseguire le operazioni seguenti:

   ![Esempio di vetrina - Configurazione Duo](./assets/storefront-2fa-duo-setup-options.png){width="300"}

1. Seleziona l’opzione. Puoi scegliere Touch ID, Duo Mobile, Security Key o Phone Number (Numero di telefono). Questo esempio mostra l’opzione Duo Mobile o Phone Number (Numero cellulare o telefono Duo).

1. Quando richiesto, immettere il numero di telefono e fare clic su **[!UICONTROL Continue]**.

   Conferma la proprietà inviando e verificando il passcode sul numero di telefono.

1. Quando viene richiesto di eseguire l&#39;installazione [!DNL Duo Mobile] per il tipo di telefono in uso, fare clic su **[!UICONTROL I have Duo Mobile]**.

1. Apri [!DNL Duo Mobile] ed esegui la scansione del codice QR per Sincronizzazione l&#39;autenticatore con Adobe Systems Commerce. Al termine dell&#39;attivazione viene visualizzato un segno di spunta.

1. Puoi aggiungere altri dispositivi (se necessario) o saltare. La configurazione è stata completata ed è possibile accedere con Duo.

   ![Azioni di verifica Duo](./assets/storefront-2fa-duo-setup-complete.png){width="300"}

### Passaggio 2: accedere con [!DNL Duo Security]

Nell&#39;esempio seguente vengono illustrate le opzioni per `Ask me to choose an authenticator method`:

1. Quando richiesto, immetti le credenziali _Admin_ per accedere.

   ![Duo - accesso](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Scegli accedi con Duo per ricevere una notifica push sull&#39;app Duo Mobile, accedi con Touch ID o procedi con un&#39;altra opzione configurata durante l&#39;installazione.

1. Approvate la richiesta dell&#39;app Duo/ID contatto/Messaggio di testo e avrete effettuato l&#39;accesso.

   ![Duo - accesso](./assets/storefront-2fa-duo-success.png){width="300"}

## [!DNL Authy]

[!DNL Authy] offre gratuitamente la propria app e il proprio servizio agli utenti. Segui le istruzioni per scaricare e configurare l’app per il dispositivo o il browser. Per ulteriori informazioni, consulta la [[!DNL Authy] documentazione](https://authy.com/features/setup/).

### Passaggio 1: configurare Authy

1. Immetti le credenziali del tuo account e accedi a _Admin_.

   Registrazione ![[!DNL Authy]](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Quando ti viene richiesto di registrarti su Authy, effettua le seguenti operazioni:

   - Seleziona il tuo paese.

   - Inserisci il tuo numero di telefono.

   - Selezionare **[!UICONTROL Verification method]**: `SMS` o `Call Me`

   Fare clic su **[!UICONTROL Continue]**. Un messaggio viene inviato al telefono tramite SMS o chiamata.

1. Immettere il codice di verifica ricevuto e fare clic su **[!UICONTROL Verify]**.

1. Al termine, fare clic su **[!UICONTROL Confirm]**.

   ![[!DNL Authy] codice di verifica](./assets/storefront-2fa-authy-verify.png){width="300"}

### Passaggio 2: accedere con [!DNL Authy]

1. Immetti le credenziali del tuo account e accedi a _Admin_.

   ![[!DNL Authy] - accesso](./assets/storefront-2fa-authy-access.png){width="300"}

1. Scegliere uno dei metodi seguenti per l&#39;autenticazione:

   - `Use one touch` - Invia un avviso all&#39;app [!DNL Authy]. Nell’app, accetta l’accesso.
   - `Use authy token` - Richiede di immettere un codice dall&#39;app [!DNL Authy].

1. In caso di problemi di accesso, scegliere il metodo da utilizzare per ricevere il codice. Quindi, immetti il codice che ricevi per accedere a _Admin_.

   L’app include questi metodi di emergenza aggiuntivi.

   - `Send me a code via SMS` - SMS inviato al dispositivo mobile configurato.
   - `Send me a code via phone call` - L&#39;utente riceve una telefonata con un codice.

   Il tuo account viene verificato e aperto.

## U2F ([!DNL Yubikey] e altri dispositivi)

Segui le istruzioni del provider di soluzioni per configurare il dispositivo U2F. Per ulteriori informazioni, vedere la documentazione del fornitore, ad esempio [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) di [!UICONTROL Yubico].

1. Immetti le tue credenziali account e accedi all&#39;amministratore __.

   ![accesso chiave U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Premere il tasto.

   L&#39;autenticazione attiva immediatamente e apre _Admin_.

1. Inserire **[!UICONTROL U2F key]** in una porta USB del computer.
