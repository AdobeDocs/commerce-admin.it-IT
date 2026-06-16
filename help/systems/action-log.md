---
title: Registri delle azioni
description: Scopri i registri delle azioni e come configurare le azioni registrate per tenere traccia di tutte le modifiche apportate al tuo archivio.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/UtJhP452hJXDyEyjxrknuF4WPoLza-UcnuWxP6ILtq8
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
source-wordcount: 289
ht-degree: 0%

---

# Registri delle azioni

{{ee-feature}}

La funzione Registri azioni registra (registra) ogni modifica apportata da un utente amministratore che lavora nel tuo archivio. Questo ti consente di tenere traccia di tutte le modifiche apportate al tuo archivio. Il tracciamento di queste modifiche, insieme all&#39;impostazione delle [autorizzazioni di amministratore](permissions.md) per un utente, può aiutare a proteggere l&#39;archivio dalle modifiche indesiderate.

Per la maggior parte delle azioni amministratore, le informazioni registrate includono l’azione, il nome dell’utente, l’esito positivo o negativo dell’azione e l’ID dell’oggetto interessato dall’azione. Vengono registrati anche l’indirizzo IP e la data.

Per impostazione predefinita, tutte le azioni amministratore sono abilitate e registrate. Per configurare la registrazione delle azioni amministratore, controlla le opzioni e seleziona o deseleziona la casella di controllo per ogni tipo di azione. Adobe Commerce registra solo i tipi selezionati.

Visualizza il [Report log azioni](action-log-report.md) per esaminare le azioni e i dettagli di amministrazione registrati.

![Configurazione avanzata - registrazione azioni amministratore](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Per un elenco dettagliato delle impostazioni di configurazione, vedere [Archiviazione log azioni amministratore](../configuration-reference/advanced/system.md) nel _Riferimento configurazione_.

## Configurare le azioni amministratore per la registrazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Admin Actions Logging]** ed eseguire le operazioni seguenti per ogni azione:

   - Per abilitare la registrazione amministratore per l’azione, seleziona la casella di controllo.
   - Per disabilitare la registrazione amministratore per l’azione, deseleziona la casella di controllo.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Archivia registro azioni amministratore

I registri delle azioni dell’amministratore possono essere archiviati per un numero qualsiasi di giorni. Gli archivi possono essere eliminati anche dopo una durata specifica.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere **[!UICONTROL Admin Action Log Archiving]** e impostare le opzioni:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Imposta il numero di giorni per la conservazione del registro archiviato.
   - **[!UICONTROL Log Archiving Frequency]** - Impostare la frequenza per la creazione degli archivi.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
