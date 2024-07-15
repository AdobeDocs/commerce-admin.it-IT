---
title: Archivio registro azioni
description: Scopri come configurare e visualizzare l’archivio del registro azioni di amministrazione.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Archivio registro azioni

{{ee-feature}}

Nell&#39;archivio delle [azioni](action-log.md) dell&#39;amministratore sono elencati i file di registro CSV archiviati nel server. Nella configurazione, è possibile specificare la durata di memorizzazione delle voci di registro e la frequenza di archiviazione. Per impostazione predefinita, il nome del file include la data corrente in formato ISO:  `yyyyMMddHH`

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
