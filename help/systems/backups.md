---
title: Backup del sistema
description: Scopri come creare e pianificare i backup di sistema, inclusi file system, database e file multimediali.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/kx2acbOSrWMJGv3ST6qKAXjLPgL2Lsh16wWvOxNO7FE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 0%

---

# Backup del sistema

Adobe Commerce e Magento Open Source consentono di eseguire il backup di diverse parti del sistema, ad esempio file system, database e file multimediali, e di eseguire il rollback automaticamente. Nella griglia della pagina _Backup_ viene visualizzato un record per ogni backup. Se si elimina un record dall&#39;elenco, viene eliminato anche il file archiviato. I file di backup del database vengono compressi utilizzando il formato GZ. Per i backup di sistema e i backup di database e supporti, viene utilizzato il formato TGZ. Come best practice, è consigliabile limitare l’accesso agli strumenti di backup ed eseguire il backup prima di installare estensioni e aggiornamenti.

- **Limita l&#39;accesso agli strumenti di backup.** L&#39;accesso allo strumento di gestione dei backup e del rollback può essere limitato configurando [ruoli utente](permissions-user-roles.md) per le risorse di backup e rollback. Per limitare l’accesso, lascia deselezionata la casella di controllo corrispondente. Per consentire l&#39;accesso alle risorse di rollback, è necessario concedere anche l&#39;accesso alle risorse di backup.

- **Eseguire il backup prima di installare estensioni e aggiornamenti.** Esegui sempre un backup prima di installare un&#39;estensione o un aggiornamento.

{{$include /help/_includes/backups-note.md}}

## Abilitare e pianificare i backup

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Backup Settings]**.

1. Imposta **[!UICONTROL Enabled Schedule Backup]** su `Yes`.

1. Per pianificare i backup automatici, impostare le opzioni di pianificazione:

   - Imposta **[!UICONTROL Enabled Schedule Backup]** su `Yes`.
   - Impostare **[!UICONTROL Scheduled Backup Type]** sul tipo di backup da eseguire all&#39;intervallo pianificato.
   - Impostare **[!UICONTROL Start Time]** sull&#39;ora del giorno per eseguire l&#39;operazione di backup.
   - Imposta **[!UICONTROL Frequency]** su `Daily`, `Weekly` o `Monthly`.
   - Imposta **[!UICONTROL Maintenance Mode]** su `Yes`.

   ![Configurazione avanzata - backup](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Creare un backup

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Nell&#39;angolo superiore destro fare clic sul tipo di backup che si desidera creare:

   - **[!UICONTROL System Backup]** - Crea un backup completo del database e del file system. Durante il processo, è possibile scegliere di includere la cartella dei supporti nel backup.

   - **[!UICONTROL Database and Media Backup]** - Crea un backup del database e della cartella dei supporti.

   - **[!UICONTROL Database Backup]** - Crea un backup del database.

   ![Strumenti di sistema - backup](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Per attivare la modalità di manutenzione dell&#39;archivio durante il backup, selezionare la casella di controllo.

   Al termine del backup, la modalità di manutenzione viene disattivata automaticamente.

1. Per un backup di sistema, selezionare la casella di controllo **[!UICONTROL Include Media folder to System Backup]** per includere la cartella dei supporti.

1. Quando richiesto, conferma l’azione.



<!-- Last updated from includes: 2023-02-22 09:59:54 -->
