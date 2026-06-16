---
title: Configurare i registri dei regali
description: Scopri come abilitare i registri dei regali e configurare le relative notifiche e-mail.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 0%

---

# Configurare i registri dei regali

{{ee-feature}}

Prima di poter offrire registri regali ai clienti, devi abilitare i registri regali e configurare le relative notifiche e-mail. Adobe Commerce invia le seguenti notifiche e-mail in risposta agli eventi nel flusso di lavoro del registro dei regali.

- Quando viene creato un nuovo registro regali, viene inviata un&#39;e-mail al proprietario con un collegamento al registro che può essere condiviso.
- Facoltativamente, il negozio può inviare una notifica con un collegamento al registro regali agli amici e ai familiari del proprietario del registro regali.
- Il proprietario riceve una notifica quando gli articoli vengono acquistati dal registro regali, ma non indica l&#39;acquirente.

Adobe Commerce dispone di modelli predefiniti per ciascuno di questi messaggi e-mail che possono essere personalizzati per il tuo marchio.

## Passaggio 1: Abilita registri regali

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Gift Registry]**

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General Options]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - Registro generale regali](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Il Registro regali è attivato per impostazione predefinita. Se necessario, impostare **[!UICONTROL Enable Gift Registry]** su `Yes`.

   - Per **[!UICONTROL Maximum Registrants]**, immettere il numero massimo di persone che possono essere invitate a partecipare a un evento del Registro di sistema relativo ai doni.

## Passaggio 2: Configurare le notifiche e-mail

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Owner Notification]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - notifica proprietario del registro regali](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Scegliere il **[!UICONTROL Email Template]** che invia una notifica ai proprietari del registro regali quando vengono creati i registri.

   - Scegliere il [contatto archivio](../getting-started/store-details.md#store-email-addresses) che verrà visualizzato come **[!UICONTROL Email Sender]** del messaggio.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Gift Registry Sharing]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - condivisione registro regali](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Scegliere il **[!UICONTROL Email Template]** che invia una notifica ai destinatari del Registro di sistema quando un Registro di sistema viene condiviso con loro.

   - Scegliere l&#39;identificatore dell&#39;archivio visualizzato come **[!UICONTROL Email Sender]** del messaggio.

   - Per **[!UICONTROL Maximum Sent Emails Threshold]**, immettere il numero massimo di e-mail che è possibile inviare contemporaneamente.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Gift Registry Update]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - aggiornamento del registro regali](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Scegliere **[!UICONTROL Email Template]** per notificare ai proprietari del Registro di sistema le modifiche apportate al Registro di sistema.

   - Scegliere l&#39;identificatore dell&#39;archivio visualizzato come **[!UICONTROL Email Sender]** del messaggio.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna la cache.

   Dopo l&#39;aggiornamento della cache, Registro regali viene visualizzato nel menu Archivi in Altre impostazioni e diventa disponibile negli account dei clienti.
