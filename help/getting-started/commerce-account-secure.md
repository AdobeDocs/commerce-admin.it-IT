---
title: Proteggi [!DNL Commerce] account
description: Scopri come utilizzare l’autenticazione a due fattori per proteggere [!DNL Commerce] account.
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# Proteggi [!DNL Commerce] account

L&#39;autenticazione a due fattori (TFA o 2FA) è un ulteriore livello di sicurezza per proteggere meglio [!DNL Commerce] account da accessi non autorizzati. Per completare la procedura di accesso, TFA richiede un _secondo fattore_ oltre alle credenziali standard di nome utente e password. Questo secondo fattore assume la forma di codici di verifica temporanei generati in modo continuo da un&#39;applicazione TFA installata sul dispositivo mobile e abbinata al [!DNL Commerce] account.

Con TFA abilitato, il tuo account è più sicuro. Un utente non autorizzato non può effettuare l’accesso a meno che non disponga sia delle credenziali del nome utente e della password (primo fattore) che di un codice di verifica valido dell’applicazione TFA sul tuo dispositivo personale (secondo fattore).

>[!NOTE]
>
>L&#39;autenticazione a due fattori che protegge _Amministratore_ del tuo negozio ha una configurazione separata. Per ulteriori informazioni, consulta [Autenticazione a due fattori](../systems/security-two-factor-authentication.md).

## Prima di iniziare

Per usare TFA, devi avere un’applicazione TFA installata sul tuo dispositivo personale (come smartphone, tablet, computer). Ne sono disponibili molte, ma alcune opzioni popolari e gratuite includono:

- Autenticatore Google (iOS, Android™, BlackBerry®)

- Authy (iOS, Android™)

- Microsoft® Authenticator (iOS, Android™, Windows Phone)

## Abilita autenticazione a due fattori

1. Accedi al tuo [[!DNL Commerce] account][1]{:target=&quot;_blank&quot;}.

1. Nel riquadro di navigazione a sinistra, seleziona **[!UICONTROL Account Settings]** e quindi selezionare **[!UICONTROL Two-factor Authentication]**.

   ![Abilita TFA](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. Seleziona **[!UICONTROL Enable]** per avviare il processo di configurazione dell&#39;autenticazione a due fattori.

1. Inserisci il **[!UICONTROL Verification Code]** inviato all’e-mail e seleziona **[!UICONTROL Verify Code]** per continuare.

   ![Immetti il codice di verifica](./assets/2fA-verification-code-prompt.png){width="400"}

1. Aprire l&#39;applicazione di autenticazione a due fattori scaricata e installata sul dispositivo personale.

1. Il giorno [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION] modulo, utilizza **[!UICONTROL Setup Code]** per aggiungere Adobe Commerce all’applicazione TFA.

   ![Aggiungere Adobe Commerce all’app TFA](./assets/commerce-account-2fa-setup-app.png){width="400"}

   Puoi aggiungere il codice scansionando il codice QR utilizzando l’applicazione TFA o immettendolo manualmente. Questo codice associa l’applicazione TFA al tuo [!DNL Commerce] e abilita le autorizzazioni per generare l’app TFA e generare i codici di verifica per l’accesso sicuro all’account.

1. Completa la configurazione.

   - Il giorno [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION] immettere il codice di verifica dell&#39;applicazione di autenticazione a due fattori.

   - Seleziona **[!UICONTROL Verify Code]**.

   >[!NOTE]
   >
   >Per motivi di sicurezza, i codici di verifica nell&#39;applicazione TFA scadono e vengono rigenerati continuamente. **_Sempre_** utilizza il codice attualmente visualizzato.

1. Salva il **[!UICONTROL Recovery Codes]** presentato in un luogo sicuro e accessibile.

   ![Archivia codici di recupero](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   Se non riesci a fornire un codice di verifica quando accedi al tuo [!DNL Commerce] account, è necessario utilizzare un codice di recupero per recuperare l&#39;accesso all&#39;account.

   Ogni codice di ripristino può essere utilizzato una sola volta, ma è possibile [generare](#generate-new-recovery-codes) nuovi. I codici di ripristino fanno distinzione tra maiuscole e minuscole.

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per continuare.

1. Per garantire di poter recuperare l’accesso al tuo account, immetti un **[!UICONTROL Recovery Email]**.

   Questo indirizzo e-mail è necessario se non è possibile generare un codice di verifica dall&#39;applicazione di autenticazione a due fattori e non si dispone dell&#39;accesso a un codice di ripristino pregenerato inutilizzato.

   Una volta ogni 24 ore, è possibile generare e inviare un codice di ripristino temporaneo all&#39;indirizzo e-mail di ripristino designato. Utilizzare questo codice per recuperare l&#39;accesso all&#39;account.

   >[!IMPORTANT]
   >
   >Mantenere l&#39;accesso all&#39;account di posta elettronica di ripristino. In caso contrario, non è possibile utilizzare codici di recupero temporanei inviati a tale account.

   ![Imposta e-mail di ripristino](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per completare il processo di configurazione dell&#39;autenticazione a due fattori.

   - Viene inviata una notifica all’indirizzo e-mail associato al tuo [!DNL Commerce] per verificare di aver abilitato correttamente l’autenticazione a due fattori.

   - Viene inviata una notifica all’account e-mail di ripristino per confermare la configurazione.

>[!TIP]
>
>Se perdi il tuo dispositivo personale o ne ottieni uno nuovo, puoi [modificare l’app di autenticazione a due fattori](#change-your-two-factor-authentication-application) e generare nuovi codici di ripristino.

## Accedi utilizzando un codice di verifica

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Inserisci il **[!UICONTROL Verification Code]** visualizzato nell&#39;applicazione di autenticazione a due fattori quando richiesto.

   ![Immetti il codice di verifica](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. Seleziona **[!UICONTROL Submit]** per completare la procedura di accesso.

## Accedi utilizzando un codice di ripristino

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Seleziona **[!UICONTROL Use recovery code]** per ignorare il prompt del codice di verifica.

1. Inserisci un valore non utilizzato **[!UICONTROL Recovery Code]** quando richiesto.

   ![Immetti il codice di recupero](./assets/2fa-recovery-code.png){width="600"}

1. Seleziona **[!UICONTROL Submit]** per completare la procedura di accesso.

## Accedi utilizzando l’e-mail di ripristino

1. Accedi al tuo [[!DNL Commerce] account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Seleziona **[!UICONTROL Use recovery code]** per ignorare il prompt del codice di verifica.

1. Per ottenere un codice di ripristino temporaneo tramite e-mail, selezionare **[!UICONTROL recovery email]** collegamento.

   ![Utilizzare l’e-mail di ripristino](./assets/2fa-recovery-email.png){width="600"}

1. Aprire l&#39;account di posta elettronica di recupero per ottenere il codice temporaneo, quindi immettere il codice nei campi designati.

1. Seleziona **[!UICONTROL Submit]** per completare la procedura di accesso.

Dopo aver utilizzato un codice di ripristino temporaneo per accedere all&#39;account, [genera nuovi codici di ripristino](#generate-new-recovery-codes) e salvarli per evitare ulteriori problemi di accesso all’account.

## Visualizza i codici di ripristino

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Completa il processo di accesso utilizzando uno dei metodi di autenticazione a due fattori descritti in precedenza.

1. Nel riquadro di navigazione a sinistra, seleziona **[!UICONTROL Account Settings]** e quindi selezionare **[!UICONTROL Two-factor Authentication]**.

   ![Impostazioni 2FA](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. Per visualizzare i codici di ripristino pregenerati, selezionare **Visualizza codici di ripristino**.

1. Inserisci il **[!UICONTROL Verification Code]** inviato all’e-mail e seleziona **[!UICONTROL Verify Code]** per continuare.

   ![Immetti il codice di verifica](./assets/2fA-verification-code-prompt.png){width="400"}

1. Salva il **Codici di ripristino** presentato in un luogo sicuro e accessibile.

   Se non riesci a fornire un codice di verifica per accedere al [!DNL Commerce] account, l&#39;utilizzo di un codice di recupero è l&#39;unico modo per recuperare l&#39;accesso all&#39;account.

   Ogni codice di ripristino è monouso, ma è sempre possibile [generare](#generate-new-recovery-codes) nuovi. I codici di ripristino fanno distinzione tra maiuscole e minuscole.

   ![Visualizza codici di recupero](./assets/2fa-view-recovery.png){width="400"}

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per chiudere la finestra di dialogo

## Genera nuovi codici di ripristino

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Completa il processo di accesso utilizzando uno dei metodi di autenticazione a due fattori descritti in precedenza.

1. Nel riquadro di navigazione a sinistra, seleziona **[!UICONTROL Account Settings]** e quindi selezionare **[!UICONTROL Two-factor Authentication]**.

1. Per generare nuovi codici di ripristino pregenerati, selezionare **Genera nuovi codici di ripristino**.

1. Inserisci il **[!UICONTROL Verification Code]** inviato all’e-mail e seleziona **[!UICONTROL Verify Code]** per continuare.

1. Salva il **Codici di ripristino** presentato in un luogo sicuro e accessibile.

   Se non riesci a fornire un codice di verifica quando accedi al tuo [!DNL Commerce] account, l&#39;utilizzo di un codice di recupero è l&#39;unico modo per recuperare l&#39;accesso all&#39;account.

   Tutti i codici di ripristino generati in precedenza vengono ora resi non validi e devono essere eliminati (solo il set corrente di codici di ripristino generati è funzionante). I codici di ripristino fanno distinzione tra maiuscole e minuscole.

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per chiudere la finestra di dialogo

## Cambia l’e-mail di ripristino

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Completa il processo di accesso utilizzando uno dei metodi di autenticazione a due fattori descritti in precedenza.

1. Nel riquadro di navigazione a sinistra, seleziona **[!UICONTROL Account Settings]** e quindi selezionare **[!UICONTROL Two-factor Authentication]**.

1. Seleziona **Modifica e-mail di ripristino** per modificare l&#39;e-mail di ripristino su file per il tuo account.

1. Inserisci il **[!UICONTROL Verification Code]** inviato all’e-mail e seleziona **[!UICONTROL Verify Code]** per continuare.

1. Per essere certi di poter recuperare l’accesso al tuo account, immetti un **E-mail di ripristino**.

   Questo indirizzo e-mail è necessario se non è possibile generare un codice di verifica dall&#39;applicazione di autenticazione a due fattori e non si dispone dell&#39;accesso a un codice di ripristino pregenerato inutilizzato.

   Una volta ogni 24 ore, è possibile generare e inviare un codice di ripristino temporaneo all&#39;indirizzo e-mail di ripristino designato. Puoi utilizzare questo codice per recuperare l’accesso all’account.

   >[!IMPORTANT]
   >
   >Mantenere l&#39;accesso all&#39;account di posta elettronica di ripristino. In caso contrario, non è possibile utilizzare codici di recupero temporanei inviati a tale account.

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per chiudere la finestra di dialogo

   Il sistema invia una notifica e-mail all’e-mail di ripristino designata per confermare che un particolare indirizzo e-mail è in archivio come e-mail di ripristino per la ricezione di codici di ripristino temporanei.

## Modificare l&#39;applicazione di autenticazione a due fattori

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Completa il processo di accesso utilizzando uno dei metodi di autenticazione a due fattori descritti in precedenza.

1. Nel riquadro di navigazione a sinistra, seleziona **[!UICONTROL Account Settings]** e quindi selezionare **[!UICONTROL Two-factor Authentication]**.

1. Seleziona **Cambia applicazione TFA** per utilizzare un’applicazione TFA diversa con il tuo account magento.com.

1. Inserisci il **[!UICONTROL Verification Code]** inviato all’e-mail e seleziona **[!UICONTROL Verify Code]** per continuare.

1. Apri l’applicazione di autenticazione a due fattori sul tuo dispositivo personale.

1. Inserisci il **Codice di configurazione** nell&#39;applicazione di autenticazione a due fattori.

   Puoi aggiungere il codice scansionando il codice QR utilizzando l’applicazione TFA o immettendolo manualmente. Questo codice associa l’applicazione TFA al tuo [!DNL Commerce] e abilita le autorizzazioni dell’app TFA per generare codici di verifica per l’accesso sicuro all’account.

   >[!NOTE]
   >
   >Per motivi di sicurezza, i codici di verifica nell&#39;applicazione TFA scadono e vengono rigenerati continuamente. **_Sempre_** utilizza il codice attualmente visualizzato.

1. Con la tua applicazione TFA ora associata al tuo [!DNL Commerce] account, immetti il **[!UICONTROL Verification Code]** visualizzato nell’applicazione TFA e seleziona **[!UICONTROL Verify Code]** per continuare.

1. Salva il **Codici di ripristino** presentato in un luogo sicuro e accessibile.

   Se non riesci a fornire un codice di verifica quando accedi al tuo [!DNL Commerce] account, l&#39;unico modo per recuperare l&#39;accesso all&#39;account è utilizzare un codice di recupero.

   Ogni codice di ripristino è monouso, ma è sempre possibile [generare](#generate-new-recovery-codes) nuovi. I codici di ripristino fanno distinzione tra maiuscole e minuscole. I codici di ripristino fanno distinzione tra maiuscole e minuscole.

1. Seleziona la casella di controllo per confermare e selezionare **[!UICONTROL Submit]** per continuare.

1. Per essere certi di poter recuperare l’accesso al tuo account, immetti un **E-mail di ripristino**.

   Questo indirizzo e-mail è necessario se non è possibile generare un codice di verifica dall&#39;applicazione di autenticazione a due fattori e non si dispone dell&#39;accesso a un codice di ripristino pregenerato inutilizzato.

   Una volta ogni 24 ore, è possibile generare e inviare un codice di ripristino temporaneo all&#39;indirizzo e-mail di ripristino designato. Utilizzare questo codice per recuperare l&#39;accesso all&#39;account.

   >[!IMPORTANT]
   >
   >Mantenere l&#39;accesso all&#39;account di posta elettronica di ripristino. In caso contrario, non è possibile utilizzare codici di recupero temporanei inviati a tale account.

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per completare il processo di configurazione dell&#39;autenticazione a due fattori.

   Viene inviata una notifica e-mail all’e-mail di recupero designata per confermare che un particolare indirizzo e-mail sia in archivio come e-mail di recupero per la ricezione di un codice di recupero temporaneo.

## Disattiva l&#39;autenticazione a due fattori

>[!IMPORTANT]
>
>Se i criteri di sicurezza organizzativi richiedono l’autenticazione a più fattori sugli account Adobe Commerce, non è possibile disabilitare l’autenticazione a due fattori.

1. Vai a [!DNL Commerce] [accesso account][1]{:target=&quot;_blank&quot;}.

1. Immetti le credenziali del nome utente e della password, quindi seleziona **[!UICONTROL Login]**.

1. Completa il processo di accesso utilizzando uno dei metodi di autenticazione a due fattori descritti in precedenza.

1. Nel riquadro di navigazione a sinistra, seleziona **[!UICONTROL Account Settings]** e seleziona **[!UICONTROL Two-factor Authentication]** sotto.

1. Seleziona **[!UICONTROL Disable]** per avviare il processo di disattivazione TFA.

1. Inserisci il **[!UICONTROL Verification Code]** inviato all’e-mail e seleziona **[!UICONTROL Verify Code]** per continuare.

1. Seleziona la casella di controllo di conferma e seleziona **[!UICONTROL Submit]** per completare la disattivazione dell&#39;autenticazione a due fattori.

   Il sistema invia una conferma e-mail che indica che TFA è stato disabilitato sul tuo [!DNL Commerce] account.

   ![Disattiva TFA](./assets/2fa-disable.png){width="400"}

[1]: https://account.magento.com/customer/account/login
