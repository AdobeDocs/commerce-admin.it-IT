---
title: Gestire gli account utente amministratore
description: Scopri come creare account utente amministratore e assegnare ruoli per concedere autorizzazioni alle funzioni amministratore.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: ad75c77ada34c4d66b1a58a666edadd44d054e17
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Gestire gli account utente amministratore

Quando il tuo archivio viene installato per la prima volta, viene creato un account Amministratore predefinito con credenziali di accesso che ti forniscono accesso amministrativo completo. Come best practice, è consigliabile creare un altro account utente con accesso completo come amministratore. In questo modo, puoi utilizzare un account per le attività amministrative quotidiane e riservare l’altro come account &quot;Super Admin&quot;. Può essere utile se si dimenticano le credenziali normali o se queste diventano in qualche modo inutilizzabili.

Se altri membri del team o fornitori di servizi hanno bisogno di accedere, puoi creare singoli account utente per loro e assegnare un accesso limitato in base alle loro esigenze aziendali specifiche. Per limitare i siti Web o gli archivi a cui gli utenti possono accedere in Amministrazione, devi prima [creare un ruolo](permissions-user-roles.md) con ambito limitato e solo le risorse necessarie selezionate. Quindi, puoi assegnare il ruolo a un account utente specifico. Gli utenti amministratori assegnati a un ruolo con restrizioni possono visualizzare e modificare i dati solo per i siti Web o gli archivi associati al ruolo, ma non possono modificare le impostazioni globali o i dati.

>[!NOTE]
>
>I commercianti di Adobe Commerce che dispongono di un Adobe ID e desiderano un accesso semplificato ai prodotti aziendali Adobe Commerce e Adobe possono integrare l’autenticazione Commerce con il flusso di lavoro di autenticazione IMS di Adobe. Una volta abilitata l’integrazione per il tuo archivio Commerce, per accedere ogni utente amministratore deve utilizzare le credenziali Adobe, non le credenziali Commerce. Consulta [Panoramica dell&#39;integrazione del servizio Adobe Identity Management (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=it).

Per gli utenti o i ruoli temporanei, puoi anche impostare una data di scadenza per l’account utente.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Creare un utente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add New User]**.

   Per modificare un utente esistente, fare clic sul nome di un utente nella griglia. È possibile modificare le sezioni _[!UICONTROL User Info]_&#x200B;e&#x200B;_[!UICONTROL User Role]_ in base alle esigenze.

1. Nella sezione _[!UICONTROL Account Information]_&#x200B;eseguire le operazioni seguenti:

   ![Informazioni account utente](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Immettere **[!UICONTROL User Name]** per l&#39;account.

     Il nome utente deve essere facile da ricordare. Non fa distinzione tra maiuscole e minuscole. Ad esempio, se il nome utente è `John`, è possibile accedere anche come `john`.

   - Completare le informazioni seguenti:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Ogni account utente deve avere un indirizzo e-mail univoco.

   - Immetti **[!UICONTROL Password]** per l&#39;account.

     >[!NOTE]
     >
     >Una password amministratore deve avere una lunghezza di sette o più caratteri e includere sia lettere che numeri. Per ulteriori opzioni relative alla password, vedere [Configurazione della sicurezza amministratore](security-admin.md).

   - Per **[!UICONTROL Password Confirmation]**, immettere nuovamente la password per verificare che sia stata immessa correttamente.

   - Se lo store ha più lingue, impostare **[!UICONTROL Interface Locale]** sulla lingua da utilizzare per l&#39;interfaccia di amministrazione.

1. Imposta **[!UICONTROL This Account is]** su `Active`.

1. Fare clic sull&#39;icona del calendario per impostare **[!UICONTROL Expiration Date]** per l&#39;account utente.

   La definizione di una data di scadenza è utile quando un utente o un ruolo è temporaneo. Dopo la data di scadenza, lo stato dell&#39;account utente cambia in `Inactive` e può essere aggiornato, se necessario.

1. In _[!UICONTROL Current User Identity Verification]_&#x200B;immettere la password dell&#39;account utente.

>[!IMPORTANT]
>
>Dopo aver completato la sezione _[!UICONTROL Account Information]_, puoi salvare l&#39;utente. Il nuovo utente viene visualizzato nella griglia&#x200B;_[!UICONTROL Users]_, ma il nome utente non può accedere finché non viene assegnato un ruolo.

## Assegna un ruolo utente

1. Nel pannello a sinistra, fai clic su **[!UICONTROL User Role]**.

   Nella griglia sono elencati tutti i ruoli utente esistenti. Per un nuovo archivio, _[!UICONTROL Administrators]_&#x200B;è l&#39;unico ruolo disponibile.

   ![Amministratore - Aggiungi nuovo ruolo utente](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Nella colonna _[!UICONTROL Assigned]_&#x200B;selezionare un ruolo utente.

   Puoi [visualizzare ruoli utente esistenti o definire ruoli utente aggiuntivi](permissions-user-roles.md). Dopo aver definito un ruolo, è necessario modificare l&#39;account utente per assegnare il nuovo ruolo.

## Verificare o reimpostare i provider 2FA

1. Apri l’account utente Amministratore.

1. Nel pannello a sinistra, fai clic su **[!UICONTROL 2FA]**.

   ![Amministratore - Aggiungi nuovo ruolo utente](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Verificare le soluzioni 2FA disponibili per gli utenti _Admin_ e consigliare a ogni utente di installare le soluzioni che desidera utilizzare prima dell&#39;accesso.

   Per accedere a _Admin_ è necessaria l&#39;autenticazione di una sola soluzione 2FA.

1. Se l&#39;utente deve reinstallare la soluzione 2FA, è possibile reimpostare la configurazione 2FA corrente.

   L&#39;utente deve ripetere il processo di configurazione prima di poter accedere di nuovo. È possibile, ad esempio, che l&#39;utente disponga di un nuovo smartphone e debba reinstallare Google Authenticator. Per cancellare la configurazione 2FA corrente dell&#39;utente, fare clic su **[!UICONTROL Reset (Provider)]** per ogni soluzione da cancellare. Quando richiesto, fare clic su **[!UICONTROL OK]** per confermare.

   L&#39;utente riceve un&#39;e-mail con un collegamento a [configura 2FA](security-two-factor-authentication.md). Il collegamento può essere utilizzato una sola volta. Se l’utente tenta di accedere più volte, dopo ogni tentativo viene inviato un nuovo collegamento.

1. Fare clic su **[!UICONTROL Save User]**.

1. Quando richiesto, immettere la password per confermare l&#39;identità e fare di nuovo clic su **[!UICONTROL Save User]**.

   La griglia _[!UICONTROL Users]_&#x200B;si apre ed elenca tutti gli utenti.

## Eliminare un utente amministratore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Individua l’account utente utilizzando i filtri sopra la griglia e fai clic sul nome utente.

1. Quando richiesto, immettere la password per confermare l&#39;identità.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Delete User]**.

1. Per confermare l&#39;azione, fare clic su **[!UICONTROL OK]**.

## Password dimenticata e reimpostare le e-mail

La configurazione del modello e-mail amministratore determina le e-mail inviate quando gli utenti dimenticano e reimpostano le password. Questa configurazione specifica il contatto dell&#39;archivio che viene visualizzato come mittente del messaggio e per quanto tempo il collegamento di recupero password rimane valido.

**_Per configurare i modelli e-mail dell&#39;amministratore:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandere ![l&#39;interruttore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Admin User Emails]**.

   ![Configurazione avanzata - Impostazioni modello e-mail amministratore](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Forgot Password Email Template]** sul modello inviato quando un utente amministratore dimentica le password.

1. Impostare **[!UICONTROL Forgot and Reset Email Sender]** sul contatto dell&#39;archivio che viene visualizzato come mittente del messaggio.

1. Imposta **[!UICONTROL User Notification Template]** sul modello di e-mail utilizzato come predefinito per le notifiche dell&#39;amministratore.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Utenti chiusi

Per la sicurezza della tua azienda, gli account utente sono bloccati per impostazione predefinita dopo sei tentativi non riusciti di [accesso](../getting-started/admin-signin.md) all&#39;amministratore. Qualsiasi account utente attualmente bloccato viene visualizzato nella griglia Utenti bloccati. Un account può essere sbloccato da qualsiasi altro utente con autorizzazioni di amministratore complete.

Nella configurazione [Advanced Admin](../configuration-reference/advanced/admin.md#security) è possibile implementare ulteriori misure di sicurezza della password. Vedi [Sicurezza amministratore](security-admin.md).

![Avviso schermata di accesso - l&#39;account è temporaneamente disabilitato](./assets/admin-login-locked-out-message.png){width="300"}

**_Per sbloccare un account amministratore:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Nella griglia, seleziona la casella di controllo dell’account bloccato.

   ![Autorizzazioni - account utente bloccati](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore sinistro impostare **[!UICONTROL Actions]** su `Unlock`.

1. Fare clic su **[!UICONTROL Submit]** per sbloccare l&#39;account.
