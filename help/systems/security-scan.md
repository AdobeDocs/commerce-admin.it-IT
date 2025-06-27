---
title: Scansione di sicurezza
description: Scopri come eseguire un’analisi della sicurezza avanzata e monitorare ciascuno dei siti Adobe Commerce e Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 8e634311cd84a9e797a36218c29abb4699d72835
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Scansione di sicurezza

L&#39;analisi avanzata della sicurezza consente di monitorare tutti i siti Adobe Commerce e Magento Open Source, incluso PWA, per individuare rischi noti per la sicurezza e malware, nonché di ricevere aggiornamenti delle patch e notifiche di sicurezza.

- Ottieni da insight lo stato di sicurezza in tempo reale del tuo negozio.
- Ricevi suggerimenti in base alle best practice per aiutare a risolvere i problemi.
- Pianifica l&#39;esecuzione dell&#39;analisi della sicurezza settimanale, giornaliera o su richiesta.
- Esegui oltre 21.000 test di sicurezza per identificare potenziali malware.
- Accedi ai report cronologici di sicurezza che tengono traccia e monitorano l’avanzamento dei siti.
- Accedere al rapporto di scansione che mostra i controlli riusciti e non riusciti, con le azioni consigliate.

Lo strumento di analisi della sicurezza è disponibile gratuitamente nel dashboard dell&#39;[account Commerce/Magento](../getting-started/commerce-account-create.md). Per informazioni tecniche, vedere [Configurare lo strumento di analisi della sicurezza](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) nella _Guida di Commerce sull&#39;infrastruttura cloud_.

![Strumento di analisi protezione](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Esegui un&#39;analisi della sicurezza

1. Accedi al tuo account [Commerce/Magento](../getting-started/commerce-account-create.md).

1. Nel pannello a sinistra, fare clic sulla scheda [!UICONTROL Security Scan]. (Se necessario, rivedere e accettare eventuali termini aggiornati per l&#39;utilizzo dello strumento di analisi della sicurezza).

   - Nel pannello a sinistra, scegli **[!UICONTROL Security Scan]**.
   - Fare clic su **[!UICONTROL Go to Security Scan]**.
   - Leggi **[!UICONTROL Terms and Conditions]**.
   - Fare clic su **[!UICONTROL Agree]** per continuare.

1. Nella pagina _[!UICONTROL Monitored Websites]_, fare clic su **[!UICONTROL +Add Site]**.

   Se disponi di più siti con domini diversi, configura una scansione separata per ciascun dominio.

   ![Siti monitorati](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Per verificare la proprietà del dominio del sito aggiungendo un codice di conferma, eseguire una delle operazioni seguenti:

   **vetrina Commerce**:

   - Immettere **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.
   - Fare clic su **[!UICONTROL Generate Confirmation Code]**.
   - Fai clic su **Copia** per copiare il codice di conferma negli Appunti.

     ![Genera codice di conferma](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Accedi all’amministratore del tuo archivio come utente con privilegi di amministratore completo ed effettua le seguenti operazioni:

      - Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Trovare il sito nell&#39;elenco e fare clic su **[!UICONTROL Edit]**.
      - Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL HTML Head]**.
      - Scorri verso il basso fino a **[!UICONTROL Scripts and Style Sheets]** e fai clic nella casella di testo alla fine di qualsiasi codice esistente, quindi incolla il codice di conferma nella casella di testo.

        ![Script e fogli di stile](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Al termine, fare clic su **[!UICONTROL Save Configuration]**.

   **vetrina PWA**:

   - Immettere **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.

   - Per **[!UICONTROL Confirmation Code]**, scegliere l&#39;opzione `META Tag` e quindi fare clic su **[!UICONTROL Generate Code]**.

   - Fare clic su **[!UICONTROL Copy]** per copiare negli Appunti il tag META del codice di conferma generato.

     ![Genera codice di conferma](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Vai alla directory del progetto PWA Studio storefront ed effettua le seguenti operazioni:

      - Nella directory del progetto PWA Studio, vai a `packages > venia-concept > template.html`.
      - Aggiungi il codice di conferma copiato (il tag META generato) all’intestazione del HTML e salva le modifiche.

        ![Copia Codice Di Conferma](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Torna a PWA Studio CLI e utilizza il filato per installare le dipendenze del progetto ed eseguire il comando project build.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Nel progetto Cloud*, crea una cartella `pwa` e copia il contenuto nella cartella `dist` del progetto storefront.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Utilizza lo strumento Git CLI per posizionare nell’area intermedia, eseguire il commit e inviare queste modifiche al progetto Cloud.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Al termine del processo di generazione, le modifiche verranno distribuite nella parte anteriore dello store di PWA.

1. Torna alla pagina _[!UICONTROL Security Scan]_nel tuo account Commerce e fai clic su **[!UICONTROL Verify Confirmation Code]**per stabilire la proprietà del dominio.

1. Dopo una conferma, configurare le opzioni **[!UICONTROL Set Automatic Security Scan]** per uno dei tipi seguenti:

   **Scansione settimanale (consigliata)**:

   - Scegliere **[!UICONTROL Week Day]**, **[!UICONTROL Time]** e **[!UICONTROL Time Zone]** per eseguire l&#39;analisi ogni settimana.
   - Per impostazione predefinita, la scansione inizia ogni settimana a mezzanotte del sabato (UTC) e continua fino alla prima domenica.

     ![Analisi settimanale](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Scansione giornaliera**:

   - Scegliere **[!UICONTROL Time]** e **[!UICONTROL Time Zone]** che l&#39;analisi deve essere eseguita ogni giorno.
   - Per impostazione predefinita, la scansione inizia ogni giorno a mezzanotte (UTC).

     ![Scansione giornaliera](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Immettere **[!UICONTROL Email Address]** dove si desidera ricevere le notifiche delle scansioni completate e degli aggiornamenti di sicurezza.

   ![Indirizzo e-mail](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Submit]**.

   Dopo aver verificato la proprietà del dominio, il sito viene visualizzato nell&#39;elenco Siti Web monitorati dell&#39;account Commerce.

1. Se disponi di più siti web con domini diversi, ripeti questo processo per impostare un’analisi di sicurezza per ciascuno di essi.

## Eliminare un&#39;analisi della protezione

>[!NOTE]
>
>Solo la persona che ha originariamente configurato la scansione può eliminarla dall&#39;account. Se non hanno effettuato l&#39;accesso al loro account [account](https://account.magento.com) dall&#39;agosto 2022, devono prima assicurarsi di avere [registrato per un Adobe ID](https://account.magento.com).

**Eliminare un&#39;analisi**

1. Accedi all&#39;[account Commerce/Magento](../getting-started/commerce-account-create.md).

1. Nel pannello sinistro fare clic sulla scheda [!UICONTROL Security Scan]. (Se necessario, rivedere e accettare eventuali termini aggiornati per l&#39;utilizzo dello strumento di analisi della sicurezza).

   - Fare clic su **[!UICONTROL Go to Security Scan]**.
   - Leggi **[!UICONTROL Terms and Conditions]**.
   - Fare clic su **[!UICONTROL Agree]** per continuare.

1. Nella pagina _[!UICONTROL Monitored Websites]_, individua il menu a discesa sotto la colonna [!UICONTROL Actions], quindi seleziona **[!UICONTROL Delete]**per i siti Web appropriati.
