---
title: Configurare i registri dei regali
description: Scopri come abilitare i registri dei regali e configurare le relative notifiche e-mail.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '356'
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

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Gift Registry]**

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General Options]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - Generale del registro regali](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Il Registro regali è attivato per impostazione predefinita. Se necessario, impostare **[!UICONTROL Enable Gift Registry]** a `Yes`.

   - Per **[!UICONTROL Maximum Registrants]**, immettere il numero massimo di persone che possono essere invitate a partecipare a un evento del registro dei regali.

## Passaggio 2: Configurare le notifiche e-mail

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Owner Notification]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - notifica del proprietario del registro regali](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Scegli la **[!UICONTROL Email Template]** che avvisa i proprietari del registro regali quando vengono creati i registri.

   - Scegli la [contatto store](../getting-started/store-details.md#store-email-addresses) che viene visualizzato come **[!UICONTROL Email Sender]** del messaggio.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Gift Registry Sharing]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti: condivisione del registro regali](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Scegli la **[!UICONTROL Email Template]** che avvisa i destinatari del registro regali quando un registro viene condiviso con loro.

   - Scegli l&#39;identificatore store visualizzato come **[!UICONTROL Email Sender]** del messaggio.

   - Per **[!UICONTROL Maximum Sent Emails Threshold]**, inserisci il numero massimo di e-mail che possono essere inviate contemporaneamente.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Gift Registry Update]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - aggiornamento del registro regali](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Scegli la **[!UICONTROL Email Template]** notifica ai proprietari del registro delle donazioni le modifiche apportate al registro.

   - Scegli l&#39;identificatore store visualizzato come **[!UICONTROL Email Sender]** del messaggio.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna la cache.

   Dopo l&#39;aggiornamento della cache, Registro regali viene visualizzato nel menu Archivi in Altre impostazioni e diventa disponibile negli account dei clienti.
