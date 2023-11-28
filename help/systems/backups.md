---
title: Backup del sistema
description: Scopri come creare e pianificare i backup di sistema, inclusi file system, database e file multimediali.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Backup del sistema

Adobe Commerce e Magento Open Source consentono di eseguire il backup di diverse parti del sistema, ad esempio file system, database e file multimediali, e di eseguire il rollback automaticamente. Un record per ogni backup viene visualizzato nella griglia del _Backup_ pagina. Se si elimina un record dall&#39;elenco, viene eliminato anche il file archiviato. I file di backup del database vengono compressi utilizzando il formato GZ. Per i backup di sistema e i backup di database e supporti, viene utilizzato il formato TGZ. Come best practice, è consigliabile limitare l’accesso agli strumenti di backup ed eseguire il backup prima di installare estensioni e aggiornamenti.

- **Limitare l&#39;accesso agli strumenti di backup.** L&#39;accesso allo strumento di gestione dei backup e del rollback può essere limitato tramite la configurazione [ruoli utente](permissions-user-roles.md) per le risorse di backup e rollback. Per limitare l’accesso, lascia deselezionata la casella di controllo corrispondente. Per consentire l&#39;accesso alle risorse di rollback, è necessario concedere anche l&#39;accesso alle risorse di backup.

- **Esegui il backup prima di installare estensioni e aggiornamenti.** Esegui sempre un backup prima di installare un&#39;estensione o un aggiornamento.

{{$include /help/_includes/backups-note.md}}

## Abilitare e pianificare i backup

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Backup Settings]**.

1. Imposta **[!UICONTROL Enabled Schedule Backup]** a `Yes`.

1. Per pianificare i backup automatici, impostare le opzioni di pianificazione:

   - Imposta **[!UICONTROL Enabled Schedule Backup]** a `Yes`.
   - Imposta **[!UICONTROL Scheduled Backup Type]** al tipo di backup da eseguire all&#39;intervallo pianificato.
   - Imposta **[!UICONTROL Start Time]** all&#39;ora del giorno in cui eseguire l&#39;operazione di backup.
   - Imposta **[!UICONTROL Frequency]** a `Daily`, `Weekly`, o `Monthly`.
   - Imposta **[!UICONTROL Maintenance Mode]** a `Yes`.

   ![Configurazione avanzata - backup](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Creare un backup

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Nell&#39;angolo superiore destro fare clic sul tipo di backup che si desidera creare:

   - **[!UICONTROL System Backup]** - Crea un backup completo del database e del file system. Durante il processo, è possibile scegliere di includere la cartella dei supporti nel backup.

   - **[!UICONTROL Database and Media Backup]** - Crea un backup del database e della cartella dei supporti.

   - **[!UICONTROL Database Backup]** - Crea un backup del database.

   ![Strumenti di sistema - backup](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Per attivare la modalità di manutenzione dell&#39;archivio durante il backup, selezionare la casella di controllo.

   Al termine del backup, la modalità di manutenzione viene disattivata automaticamente.

1. Per un backup del sistema, selezionare **[!UICONTROL Include Media folder to System Backup]** per includere la cartella multimediale.

1. Quando richiesto, conferma l’azione.


