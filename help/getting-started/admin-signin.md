---
title: Account utente amministratore
description: Scopri il tuo account amministratore e come utilizzare l’autenticazione a due fattori per accedere all’amministratore.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# Account amministratore

L&#39;account Admin primario è stato inizialmente configurato durante l&#39;installazione e potrebbe contenere informazioni iniziali sui segnaposto o dati di esempio. Il proprietario designato di questo account può personalizzare il nome utente e la password e aggiornare il nome, il cognome e l’indirizzo e-mail in qualsiasi momento. Questo account, un _utente privilegiato_ Con tutte le autorizzazioni per impostazione predefinita, in genere crea gli account utente Amministratore necessari per l’azienda.

- Consulta [Creare un utente](../systems/permissions-users-all.md#create-a-user) per informazioni sull&#39;aggiunta o la modifica di utenti.

- Consulta [Autorizzazioni](../systems/permissions.md) e [Ruoli utente](../systems/permissions-user-roles.md) per informazioni sull’amministratore e sui ruoli utente.

{{ims-admin-note}}

## Accesso amministratore

Il [!DNL Commerce] _Amministratore_ è protetto da più livelli di misure di sicurezza per impedire l&#39;accesso non autorizzato ai dati di archivio, ordine e cliente. La prima volta che accedi a _Amministratore_, è necessario immettere il nome utente e la password e configurare [autenticazione a due fattori](../systems/security-two-factor-authentication.md) (2 BIS).

A seconda della configurazione dell’archivio, potrebbe essere [CAPTCHA](../systems/security-google-recaptcha.md) difficoltà di risoluzione, ad esempio inserimento di una serie di caratteri di tastiera, risoluzione di un rompicapo o clic su una serie di immagini con un tema comune. Questi test sono progettati per identificare l’utente come utente umano, anziché come bot automatizzati.

Per una maggiore sicurezza, è possibile determinare quali parti del _Amministratore_ ogni utente ha [autorizzazione](../systems/permissions.md) per accedere a e limitare il numero di [tentativi di accesso](../configuration-reference/advanced/admin.md). Per impostazione predefinita, dopo sei tentativi l’account viene bloccato e l’utente deve attendere alcuni minuti prima di riprovare. [Account bloccati](../systems/permissions-users-all.md#locked-users) può essere reimpostato anche dalla _Amministratore_.

>[!NOTE]
>
>La prima volta che accedi a _Amministratore_, viene richiesto di _Consenti raccolta dati di utilizzo amministratore_. Consulta [Raccolta dati di utilizzo](admin.md#usage-data-collection) per ulteriori informazioni.

![Accesso amministratore](./assets/admin-login.png){width="400"}

### Passaggio 1: configurare l’autenticazione a due fattori

Prima di accedere a _Amministratore_ del tuo archivio, devi disporre di una soluzione di autenticazione a due fattori configurata e pronta per l’uso. Per ulteriori informazioni sul processo di autenticazione utilizzato da ciascuna soluzione, consulta [Utilizzo dell’autenticazione a due fattori](../systems/security-two-factor-authentication-use.md). Per impostazione predefinita, [!DNL Commerce] supporta [Autenticatore Google][1].

Chiedi [!DNL Commerce] amministratore di sistema quali soluzioni 2FA sono supportate per lo store. Quindi, completare la configurazione della soluzione 2FA preferita seguendo le istruzioni del provider.

### Passaggio 2: accedere all’amministratore

1. Inserisci il _Amministratore_ URL specificato durante il [!DNL Commerce] installazione.

   Il valore predefinito _Amministratore_ L’URL ha un aspetto simile a `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >Anche se questa documentazione utilizza `admin` come URL di base nella maggior parte degli esempi, si consiglia di scegliere un URL univoco e difficile da indovinare [URL personalizzato](../stores-purchase/store-urls.md) per _Amministratore_ del tuo negozio.

   È possibile aggiungere un segnalibro alla pagina o salvare un collegamento sul desktop per accedervi facilmente.

1. Immetti il _Amministratore_ **[!UICONTROL Username]** e **[!UICONTROL Password]**.

1. (Facoltativo) Se per il tuo negozio è abilitato un CAPTCHA, segui le istruzioni visualizzate per risolvere il problema.

   Per ulteriori informazioni, consulta [CAPTCHA](../systems/security-captcha.md) e [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Clic **[!UICONTROL Sign in]**.

   Se è la prima volta che accedi a _Amministratore_ dall’account, dovresti ricevere un’e-mail con un collegamento alle istruzioni di configurazione.

### Passaggio 3: completare la configurazione 2FA

L’esempio seguente mostra come accoppiare il _Amministratore_ account con Google Authenticator.

1. Quando viene visualizzato il codice QR, utilizza uno dei metodi seguenti per acquisire il codice e associare Google Authenticator a _Amministratore_ account.

   ![Configurare Google Authenticator](./assets/admin-login-google-auth-setup.png){width="400"}

   - Acquisire codice QR con uno smartphone

     Sul tuo smartphone, avvia Google Authenticator. Tocca il _segno più_ (+) nell’angolo superiore destro dell’app. Quindi, nella parte inferiore dello schermo, tocca **[!UICONTROL Scan Barcode]** e scatta una foto del codice QR.

   - Acquisisci codice QR dal browser

     Se Google Authenticator è installato come estensione nel browser, fare clic sul pulsante **Autenticatore** nella barra degli strumenti e acquisisce la pagina.

   - Immetti manualmente il codice QR

     Copia la stringa di testo sotto il codice QR. Avvia Google Authenticator con lo smart phone o il browser in uso e fai clic sul segno più (+). Quindi, scegli **[!UICONTROL Manual Entry]**. Sotto **[!UICONTROL Account]**, immetti l&#39;indirizzo e-mail associato al tuo _Amministratore_ e incolla la stringa del codice QR nel **[!UICONTROL Key]** campo.

1. Per accedere a _Amministratore_ con l&#39;autenticazione a due fattori, immettere il codice a sei cifre generato da Google Authenticator in **[!UICONTROL Authenticator code]** e quindi fare clic su **[!UICONTROL Confirm]**.

   ![Immetti il codice di autenticazione](./assets/admin-login-2fa-google.png){width="400"}

## Reimposta la password

Non è consentito riutilizzare le ultime quattro password assegnate all’account.

1. Inserisci il **[!UICONTROL Email Address]** associato al _Amministratore_ account.

   ![Password dimenticata](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Clic **[!UICONTROL Retrieve Password]**.

   Se all’indirizzo e-mail è associato un account, viene inviata un’e-mail per reimpostare la password.

   >[!NOTE]
   >
   >Un _Amministratore_ la password deve contenere almeno sette caratteri e includere sia lettere che numeri. Consulta [Configurazione _Amministratore_ Sicurezza](../systems/security-admin.md) per informazioni sulle opzioni relative alla password.

## Esci dall’amministratore

1. Nell’angolo in alto a destra, fai clic su _Account_ (![Account](../assets/icon-admin-user.png)).

1. Clic **[!UICONTROL Sign Out]**.

   ![Esci](./assets/admin-sign-out.png){width="700" zoomable="yes"}

Il _[!UICONTROL Sign In]_visualizza un messaggio di disconnessione. Esci da_ Amministratore _quando si lascia il computer incustodito.

## Modifica informazioni account

1. Fai clic su _Account_ (![Icona account](../assets/icon-admin-user.png)).

1. Clic **[!UICONTROL Account Setting]**.

   ![Informazioni account](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Apporta le modifiche necessarie alle informazioni del tuo account.

   Se modifichi le credenziali di accesso, assicurati di memorizzarle in un percorso sicuro.

1. Immettere la password dell&#39;account corrente.

1. Clic **[!UICONTROL Save Account]**.

## Consenti più accessi amministratore

L’amministratore consente di gestire gli ordini, i clienti, i prodotti, le funzionalità di spedizione e di pagamento. Come best practice per la sicurezza, la configurazione predefinita prevede di non consentire più accessi per un account utente amministratore. Tuttavia, puoi modificare questa impostazione per consentire agli utenti amministratori di accedere da più dispositivi per adattarsi ai flussi di lavoro aziendali.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Security]** sezione.

1. Per **Condivisione account amministratore**, seleziona `Yes`.

   ![Consenti condivisione account amministratore](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

## Imposta i nomi di accesso degli utenti amministratori con distinzione tra maiuscole e minuscole

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Security]** sezione.

1. Imposta il **[!UICONTROL Login is Case Sensitive]** campo a `Yes`.

1. Clic **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
