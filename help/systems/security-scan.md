---
title: Scansione di sicurezza
description: Scopri come eseguire un’analisi della sicurezza avanzata e monitorare ciascuno dei siti Adobe Commerce e di Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Scansione di sicurezza

L&#39;analisi avanzata della sicurezza consente di monitorare tutti i siti Adobe Commerce e di Magento Open Source, inclusi PWA, per individuare eventuali rischi noti per la sicurezza e malware, nonché di ricevere aggiornamenti delle patch e notifiche di sicurezza.

- Ottieni informazioni sullo stato di sicurezza in tempo reale del tuo negozio.
- Ricevi suggerimenti in base alle best practice per aiutare a risolvere i problemi.
- Pianifica l&#39;esecuzione dell&#39;analisi della sicurezza settimanale, giornaliera o su richiesta.
- Esegui oltre 21.000 test di sicurezza per identificare potenziali malware.
- Accedi ai report cronologici di sicurezza che tengono traccia e monitorano l’avanzamento dei siti.
- Accedere al rapporto di scansione che mostra i controlli riusciti e non riusciti, con le azioni consigliate.

Lo strumento di analisi della sicurezza è disponibile gratuitamente nel dashboard [Account Commerce/Magento](../getting-started/commerce-account-create.md). Per informazioni tecniche, consulta [Configurare lo strumento Security Scan](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) nel _Guida di Commerce sull’infrastruttura cloud_.

![Strumento di analisi della sicurezza](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Esegui un&#39;analisi della sicurezza

1. Dalla pagina Home di Commerce, accedi al tuo [Account Commerce/Magento](../getting-started/commerce-account-create.md).

1. Rivedere e accettare i termini per l&#39;utilizzo dello strumento Security scan.

   - Nel pannello a sinistra, scegli **[!UICONTROL Security Scan]**.
   - Clic **[!UICONTROL Go to Security Scan]**.
   - Leggi le **[!UICONTROL Terms and Conditions]**.
   - Clic **[!UICONTROL Agree]** per continuare.

1. Il giorno _[!UICONTROL Monitored Websites]_pagina, fai clic su **[!UICONTROL +Add Site]**.

   Se disponi di più siti con domini diversi, configura una scansione separata per ciascun dominio.

   ![Siti monitorati](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Per verificare la proprietà del dominio del sito aggiungendo un codice di conferma, eseguire una delle operazioni seguenti:

   **vetrina Commerce**:

   - Inserisci il **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.
   - Clic **[!UICONTROL Generate Confirmation Code]**.
   - Clic **Copia** per copiare il codice di conferma negli Appunti.

     ![Genera codice di conferma](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Accedi all’amministratore del tuo archivio come utente con privilegi di amministratore completo ed effettua le seguenti operazioni:

      - In _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Individuare il sito nell&#39;elenco e fare clic su **[!UICONTROL Edit]**.
      - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL HTML Head]** sezione.
      - Scorri verso il basso fino a **[!UICONTROL Scripts and Style Sheets]** e fai clic nella casella di testo alla fine di qualsiasi codice esistente e incolla il codice di conferma nella casella di testo.

        ![Script e fogli di stile](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Al termine, fai clic su **[!UICONTROL Save Configuration]**.

   **vetrina PWA**:

   - Inserisci il **[!UICONTROL Site URL]** e **[!UICONTROL Site Name]**.

   - Per **[!UICONTROL Confirmation Code]**, scegli il `META Tag` e quindi fare clic su **[!UICONTROL Generate Code]**.

   - Clic **[!UICONTROL Copy]** per copiare negli Appunti il codice di conferma generato META Tag.

     ![Genera codice di conferma](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Vai alla directory del progetto PWA Studi storefront ed effettua le seguenti operazioni:

      - Nella directory del progetto PWA Studi, vai a `packages > venia-concept > template.html`.
      - Aggiungi il codice di conferma copiato (il tag META generato) all’intestazione del HTML e salva le modifiche.

        ![Copia codice di conferma](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Torna alla CLI di PWA Studi e utilizza il filato per installare le dipendenze del progetto ed eseguire il comando project build.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Nel progetto Cloud*, crea un `pwa` e copiare il contenuto nel file del progetto storefront `dist` cartella.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Utilizza lo strumento Git CLI per posizionare nell’area intermedia, eseguire il commit e inviare queste modifiche al progetto Cloud.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Al termine del processo di compilazione, le modifiche verranno distribuite nella parte anteriore dell’archivio PWA.

1. Torna a _[!UICONTROL Security Scan]_nel tuo account Commerce, quindi fai clic su **[!UICONTROL Verify Confirmation Code]**stabilire la proprietà del dominio.

1. Dopo una conferma, configura il **[!UICONTROL Set Automatic Security Scan]** opzioni per uno dei tipi seguenti:

   **Scansione settimanale (consigliato)**:

   - Scegli la **[!UICONTROL Week Day]**, **[!UICONTROL Time]**, e **[!UICONTROL Time Zone]** che la scansione avvenga ogni settimana.
   - Per impostazione predefinita, la scansione inizia ogni settimana a mezzanotte del sabato (UTC) e continua fino alla prima domenica.

     ![Scansione settimanale](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Scansiona ogni giorno**:

   - Scegli la **[!UICONTROL Time]**, e **[!UICONTROL Time Zone]** che la scansione avvenga ogni giorno.
   - Per impostazione predefinita, la scansione inizia ogni giorno a mezzanotte (UTC).

     ![Scansiona ogni giorno](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Inserisci il **[!UICONTROL Email Address]** dove desideri ricevere notifiche di scansioni completate e aggiornamenti di sicurezza.

   ![Indirizzo e-mail](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Submit]**.

   Dopo aver verificato la proprietà del dominio, il sito viene visualizzato nell&#39;elenco Siti Web monitorati dell&#39;account Commerce.

1. Se disponi di più siti web con domini diversi, ripeti questo processo per impostare un’analisi di sicurezza per ciascuno di essi.
