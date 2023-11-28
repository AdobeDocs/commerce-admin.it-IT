---
title: Gestire gli account utente amministratore
description: Scopri come creare account utente amministratore e assegnare ruoli per concedere autorizzazioni alle funzioni amministratore.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Gestire gli account utente amministratore

Quando il tuo archivio viene installato per la prima volta, viene creato un account Amministratore predefinito con credenziali di accesso che ti forniscono accesso amministrativo completo. Come best practice, è consigliabile creare un altro account utente con accesso completo come amministratore. In questo modo, puoi utilizzare un account per le attività amministrative quotidiane e riservare l’altro come account &quot;Super Admin&quot;. Può essere utile se si dimenticano le credenziali normali o se queste diventano in qualche modo inutilizzabili.

Se altri membri del team o provider di servizi necessitano dell&#39;accesso, è possibile creare un account utente separato per ciascuno di essi e assegnare un accesso limitato in base alle esigenze aziendali da conoscere. Per limitare i siti web o gli store a cui gli utenti possono accedere nell’Admin, devi prima [creare un ruolo](permissions-user-roles.md) con ambito limitato e solo le risorse necessarie selezionate. Quindi, puoi assegnare il ruolo a un account utente specifico. Gli utenti amministratori assegnati a un ruolo con restrizioni possono visualizzare e modificare i dati solo per i siti Web o gli archivi associati al ruolo, ma non possono modificare le impostazioni globali o i dati.

>[!NOTE]
>
>I commercianti di Adobe Commerce che dispongono di un Adobe ID e desiderano un accesso semplificato ai prodotti Adobe Commerce e Adobe Business possono integrare l’autenticazione Commerce con il flusso di lavoro di autenticazione IMS di Adobe. Dopo l’abilitazione di questa integrazione per l’archivio Commerce, per accedere ogni utente amministratore deve utilizzare le proprie credenziali di Adobe, non le credenziali Commerce. Consulta [Panoramica dell’integrazione di Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Per gli utenti o i ruoli temporanei, puoi anche impostare una data di scadenza per l’account utente.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Creare un utente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New User]**.

   Per modificare un utente esistente, fare clic sul nome di un utente nella griglia. È possibile modificare _[!UICONTROL User Info]_e_[!UICONTROL User Role]_ sezioni in base alle esigenze.

1. In _[!UICONTROL Account Information]_eseguire le operazioni seguenti:

   ![Informazioni account utente](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Inserisci il **[!UICONTROL User Name]** per conto di.

     Il nome utente deve essere facile da ricordare. Non fa distinzione tra maiuscole e minuscole. Ad esempio, se il nome utente è `John`, possono anche accedere come `john`.

   - Completare le informazioni seguenti:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Ogni account utente deve avere un indirizzo e-mail univoco.

   - Immetti un **[!UICONTROL Password]** per l’account.

     >[!NOTE]
     >
     >Una password amministratore deve avere una lunghezza di sette o più caratteri e includere sia lettere che numeri. Per ulteriori opzioni relative alla password, consulta [Configurazione della sicurezza di amministrazione](security-admin.md).

   - Per **[!UICONTROL Password Confirmation]**, immettere nuovamente la password per accertarsi che sia stata immessa correttamente.

   - Se lo store ha più lingue, imposta **[!UICONTROL Interface Locale]** nella lingua da utilizzare per l’interfaccia di amministrazione.

1. Imposta **[!UICONTROL This Account is]** a `Active`.

1. Fai clic sull’icona del calendario per impostare **[!UICONTROL Expiration Date]** per l’account utente.

   La definizione di una data di scadenza è utile quando un utente o un ruolo è temporaneo. Dopo la data di scadenza, lo stato dell’account utente cambia in `Inactive` e possono essere aggiornati, se necessario.

1. Sotto _[!UICONTROL Current User Identity Verification]_, immettere la password dell&#39;account utente.

>[!IMPORTANT]
>
>Con il _[!UICONTROL Account Information]_sezione completa, puoi salvare l’utente. Il nuovo utente viene visualizzato in_[!UICONTROL Users]_ ma il nome utente non può accedere finché non viene assegnato un ruolo.

## Assegna un ruolo utente

1. Nel pannello a sinistra, fai clic su **[!UICONTROL User Role]**.

   Nella griglia sono elencati tutti i ruoli utente esistenti. Per un nuovo negozio, _[!UICONTROL Administrators]_è l’unico ruolo disponibile.

   ![Amministratore - Aggiungi nuovo ruolo utente](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. In _[!UICONTROL Assigned]_, selezionare un ruolo utente.

   È possibile [visualizzare i ruoli utente esistenti o definire ruoli utente aggiuntivi](permissions-user-roles.md). Dopo aver definito un ruolo, è necessario modificare l&#39;account utente per assegnare il nuovo ruolo.

## Verificare o reimpostare i provider 2FA

1. Apri l’account utente Amministratore.

1. Nel pannello a sinistra, fai clic su **[!UICONTROL 2FA]**.

   ![Amministratore - Aggiungi nuovo ruolo utente](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Verificare le soluzioni 2FA disponibili per _Amministratore_ e consigliano a ogni utente di installare le soluzioni che desidera utilizzare prima di accedere.

   Per accedere a è necessaria l&#39;autenticazione di una sola soluzione 2FA _Amministratore_.

1. Se l&#39;utente deve reinstallare la soluzione 2FA, è possibile reimpostare la configurazione 2FA corrente.

   L&#39;utente deve ripetere il processo di configurazione prima di poter accedere di nuovo. È possibile, ad esempio, che l&#39;utente disponga di un nuovo smartphone e debba reinstallare Google Authenticator. Per cancellare l&#39;impostazione 2FA corrente dell&#39;utente, fare clic su **[!UICONTROL Reset (Provider)]** per ogni soluzione da eliminare. Quando richiesto, fai clic su **[!UICONTROL OK]** per confermare.

   L’utente riceve un’e-mail con un collegamento a [configurare 2FA](security-two-factor-authentication.md). Il collegamento può essere utilizzato una sola volta. Se l’utente tenta di accedere più volte, dopo ogni tentativo viene inviato un nuovo collegamento.

1. Clic **[!UICONTROL Save User]**.

1. Quando richiesto, immettere la password per confermare l&#39;identità e fare di nuovo clic su **[!UICONTROL Save User]**.

   Il _[!UICONTROL Users]_viene visualizzata la griglia con l&#39;elenco di tutti gli utenti.

## Eliminare un utente amministratore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Individua l’account utente utilizzando i filtri sopra la griglia e fai clic sul nome utente.

1. Quando richiesto, immettere la password per confermare l&#39;identità.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Delete User]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

## Password dimenticata e reimpostare le e-mail

La configurazione del modello e-mail amministratore determina le e-mail inviate quando gli utenti dimenticano e reimpostano le password. Questa configurazione specifica il contatto dell&#39;archivio che viene visualizzato come mittente del messaggio e per quanto tempo il collegamento di recupero password rimane valido.

**_Per configurare i modelli e-mail per amministratori:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Nel pannello laterale sinistro, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandi ![interruttore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Admin User Emails]** sezione.

   ![Configurazione avanzata - Impostazioni modello e-mail amministratore](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Forgot Password Email Template]** al modello inviato quando un utente Admin dimentica le proprie password.

1. Imposta **[!UICONTROL Forgot and Reset Email Sender]** al contatto del punto vendita che viene visualizzato come mittente del messaggio.

1. Imposta **[!UICONTROL User Notification Template]** al modello e-mail utilizzato come impostazione predefinita per le notifiche dell’amministratore.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Utenti chiusi

Per la sicurezza della tua azienda, gli account utente vengono bloccati per impostazione predefinita dopo sei tentativi non riusciti di [accedi](../getting-started/admin-signin.md) all’amministratore. Qualsiasi account utente attualmente bloccato viene visualizzato nella griglia Utenti bloccati. Un account può essere sbloccato da qualsiasi altro utente con autorizzazioni di amministratore complete.

È possibile implementare ulteriori misure di sicurezza tramite password in [Amministratore avanzato](../configuration-reference/advanced/admin.md#security) configurazione. Consulta [Admin Security](security-admin.md).

![Avviso schermata di accesso - l’account è temporaneamente disabilitato](./assets/admin-login-locked-out-message.png){width="300"}

**_Per sbloccare un account amministratore:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Nella griglia, seleziona la casella di controllo dell’account bloccato.

   ![Autorizzazioni - Account utente bloccati](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Actions]** a `Unlock`.

1. Clic **[!UICONTROL Submit]** per sbloccare l’account.
