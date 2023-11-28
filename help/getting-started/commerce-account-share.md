---
title: Condividi un [!DNL Commerce] account
description: Scopri come concedere un accesso limitato al tuo [!DNL Commerce] account per altro [!DNL Commerce] titolari del conto.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 11b2f3f9558bf5a36199015247fb96d559bb5fdc
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# Condividi un [!DNL Commerce] account

Il tuo [!DNL Commerce] L&#39;account contiene informazioni che è possibile rendere disponibili a dipendenti e provider di servizi attendibili che aiutano a gestire il sito. In qualità di titolare dell&#39;account principale, hai l&#39;autorità di concedere un accesso limitato ad altri [!DNL Commerce] titolari del conto. L&#39;accesso condiviso può essere revocato, ma non può essere trasferito da un utente all&#39;altro.

Il [!DNL Commerce] Il team di supporto non ha accesso all’account e non può impostare l’accesso condiviso per te. Solo il titolare dell’account principale con le autorizzazioni appropriate può impostare l’accesso condiviso. Quando il tuo account viene condiviso, tutte le informazioni riservate, ad esempio la cronologia di fatturazione o le informazioni sulla carta di credito, rimangono protette e non vengono mai condivise con altri utenti.

>[!NOTE]
>
>Tutte le azioni intraprese dagli utenti con accesso condiviso sono di esclusiva responsabilità del titolare del conto principale. Adobe non è responsabile di alcuna azione eseguita dagli utenti che hanno accesso condiviso al tuo account.

![Impostazioni di accesso condiviso](./assets/shared-access.png){width="600" zoomable="yes"}

## Configurare un account condiviso

1. Prima di iniziare, è necessario ottenere le seguenti informazioni dal [!DNL Commerce] conto del **nuovo beneficiario dell&#39;accesso condiviso**:

   - L&#39;utente deve essersi già registrato per un account all&#39;indirizzo account.adobe.com e aver effettuato l&#39;accesso tramite account.magento.com.
   - Il `Account ID` visualizzato nell&#39;angolo superiore sinistro del _[!UICONTROL Magento]_, appena sopra la **Disconnetti**collegamento.
   - Il `Email` indirizzo associato all’account.

1. Accedi al tuo [[!DNL Commerce] account](commerce-account-create.md).

1. Nel pannello di navigazione a sinistra, fai clic su **[!UICONTROL Shared Access]**.

1. Clic **[!UICONTROL Add New User]**.

   ![Aggiungi un nuovo utente](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Sotto [!UICONTROL _New User Information]_, eseguire le operazioni seguenti:

   - Inserisci il **[!UICONTROL Account ID]** dal nuovo utente [!DNL Commerce] account.
   - Inserisci il **[!UICONTROL Email]** indirizzo associato al nuovo utente [!DNL Commerce] account.

   ![Informazioni nuovo utente](./assets/shared-new-user.png){width="600"}

1. Sotto _[!UICONTROL Shared Information]_, eseguire le operazioni seguenti:

   - Per identificare l&#39;account condiviso, immettere un **[!UICONTROL Share Name]**. Questo nome è un riferimento interno ed è visibile solo a te e alla persona con cui condividi l’account.
   - Se si desidera condividere le informazioni personali sul contatto con il nuovo utente, immettere: **[!UICONTROL Your Email]** e **[!UICONTROL Your Phone]**.

1. Sotto _[!UICONTROL Grant Account Permissions]_, seleziona la casella di controllo di ciascun [!DNL Commerce] prodotto e servizio che desideri condividere.

   ![Concedere le autorizzazioni dell’account](./assets/shared-permissions.png){width="600"}

1. Al termine, fai clic su **[!UICONTROL Create Shared Access]**.

   Le informazioni sul nuovo utente vengono visualizzate nel _[!UICONTROL Manage Permissions]_nella pagina Accesso condiviso e un invito e-mail con istruzioni per l&#39;accesso all&#39;account condiviso viene inviato al nuovo utente.

   ![Gestire le autorizzazioni per l’accesso condiviso](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

## Accedere a un account condiviso

Le seguenti istruzioni sono scritte dal punto di vista di un utente condiviso che riceve un invito a un account condiviso.

1. Quando ricevi un invito a un account condiviso, segui le istruzioni riportate nell’e-mail per accedere a [!DNL Commerce] account.

   Il pannello di navigazione sinistro dell’account presenta una nuova _[!UICONTROL Shared with me]_scheda. Il_[!UICONTROL Switch Accounts]_ nell&#39;angolo in alto a destra sono disponibili opzioni per `My Account` e il nome dell’account condiviso.

   ![Condiviso con me](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. Per accedere all’account condiviso, imposta **[!UICONTROL Switch Accounts]** al nome dell’account condiviso.

   ![Passa all’account condiviso](./assets/shared-switch.png){width="600" zoomable="yes"}

   L&#39;account condiviso visualizza un messaggio di benvenuto e informazioni di contatto. Il pannello di navigazione a sinistra include solo gli elementi per i quali disponi dell’autorizzazione all’uso.

1. Per collegare l&#39;account condiviso all&#39;Help Center, fare clic su **[!UICONTROL Support]** nel pannello di navigazione a sinistra dell’account condiviso.

   ![Supporto](./assets/shared-support.png){width="600" zoomable="yes"}

   È possibile utilizzare [Centro assistenza Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) dall’account condiviso per cercare articoli e informazioni sulla risoluzione dei problemi, trovare patch per i problemi noti e creare ticket di supporto.

   >[!NOTE]
   >
   >Dopo aver ricevuto l’accesso condiviso, l’utente deve accedere al proprio [[!DNL Commerce] account](https://account.magento.com/customer/account/login), passa a _Accesso condiviso_, quindi fare clic su **[!UICONTROL Support]** scheda. Questa azione è necessaria solo la prima volta, per garantire che [Knowledge Base di supporto Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) è configurato correttamente tramite `SSO` chiamare.

1. Per tornare al tuo account, fai clic su **Indietro** nei controlli del browser e impostare **[!UICONTROL Switch Accounts]** a `My Account`.

## Revoca dell&#39;accesso condiviso

1. Accedi al tuo account Commerce.

1. Nel pannello di navigazione a sinistra, fai clic su **[!UICONTROL Shared Access]**.

1. Trova l’account da revocare in _[!UICONTROL Managing Users & Permissions]_e fai clic su **[!UICONTROL Delete]**.

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Impossibile eliminare utenti con il nome di condivisione _Accesso condiviso cloud da MAG[XYZ]_ in questa interfaccia. Per ulteriori informazioni, consulta [Come si eliminano gli utenti a cui è stato concesso l’accesso condiviso tramite un progetto Cloud?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
