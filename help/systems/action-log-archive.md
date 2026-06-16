---
title: Archivio registro azioni
description: Scopri come configurare e visualizzare l’archivio del registro azioni di amministrazione.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
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
source-wordcount: 160
ht-degree: 0%

---

# Archivio registro azioni

{{ee-feature}}

Nell&#39;archivio delle [azioni](action-log.md) dell&#39;amministratore sono elencati i file di registro CSV archiviati nel server. Nella configurazione, è possibile specificare la durata di memorizzazione delle voci di registro e la frequenza di archiviazione. Per impostazione predefinita, il nome del file include la data corrente in formato ISO: `yyyyMMddHH`

>[!NOTE]
>
>L&#39;archiviazione dei registri richiede la configurazione di un [processo cron](cron.md).

## Configurare l’archivio dei registri

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Admin Actions Log Archiving]** e impostare le seguenti opzioni:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Immettere il numero di giorni in cui si desidera mantenere le voci di registro nel database prima che vengano rimosse.
   - **[!UICONTROL Log Archiving Frequency]** — Impostato su `Daily`, `Weekly` o `Monthly`.

   ![Configurazione avanzata - archiviazione registro azioni amministratore](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Per un elenco dettagliato delle impostazioni di configurazione, vedere [Archiviazione log azioni amministratore](../configuration-reference/advanced/system.md) nel _Riferimento configurazione_.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Visualizzare l’archivio

Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archivio log azioni](./assets/action-log-archive.png){width="600" zoomable="yes"}
