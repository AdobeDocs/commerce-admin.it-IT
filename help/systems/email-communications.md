---
title: Configurare le comunicazioni e-mail
description: Scopri come configurare le comunicazioni e-mail, incluso il routing delle e-mail restituite o delle risposte a un indirizzo e-mail specifico.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
TQID: https://experienceleague.adobe.com/0spSxu59rF2KomOWVI5iR9pcg2r-VLm-GiXvJvatnww
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Configurare le comunicazioni e-mail

Le _impostazioni di invio posta_ consentono di indirizzare le e-mail restituite o le risposte a un indirizzo specifico. Se l&#39;archivio è in esecuzione su un server SMTP o Windows, è possibile verificare le impostazioni dell&#39;host e della porta.

>[!IMPORTANT]
>
>**Avviso di protezione** Tutti i commercianti devono impostare immediatamente la configurazione di invio della posta per proteggersi da un potenziale exploit di esecuzione del codice remoto identificato di recente. Fino alla risoluzione del problema, si consiglia di evitare di utilizzare [!DNL Sendmail] per le comunicazioni e-mail. In _[!UICONTROL Mail Sending Settings]_, assicurarsi che_[!UICONTROL Set Return Path]_ sia impostato su `No`.

Per un elenco dettagliato delle impostazioni di configurazione, vedere [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) in _Riferimento configurazione_.

## Configurare le comunicazioni e-mail

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Mail Sending Settings]** ed effettuare le seguenti operazioni:

   ![Configurazione avanzata - impostazioni invio posta](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Se necessario, impostare **[!UICONTROL Disable Email Communications]** su `No`.

   - Per **[!UICONTROL Transport]**, scegliere il tipo di trasporto per le comunicazioni e-mail dall&#39;archivio: `Sendmail` o `SMTP`

   - Se l&#39;esecuzione avviene su un server SMTP o Windows, verificare le impostazioni seguenti:

      - **[!UICONTROL Host]** - `localhost` o altro/i

      - **[!UICONTROL Port (25)]** - `25` o altro/i

   - Per **[!UICONTROL Set Return Path]**, scegliere una delle opzioni seguenti:

      - `No` - (misura di sicurezza consigliata) Le route hanno restituito l&#39;indirizzo e-mail dell&#39;archivio predefinito.
      - `Yes` - Le route hanno restituito l&#39;e-mail all&#39;indirizzo predefinito dell&#39;archivio.
      - `Specified` - Le route hanno restituito l&#39;indirizzo e-mail specificato in **[!UICONTROL Return Path Email]**.

   - Se l&#39;esecuzione avviene su un server SMTP, configurare la connessione:

      - **[!UICONTROL Username]** - Immettere il nome utente di accesso per il server SMTP.
      - **[!UICONTROL Password]** - Immettere la password di accesso al server SMTP.
      - **[!UICONTROL Auth]** - Scegliere il tipo di autenticazione per la connessione al server SMTP: `NONE`, `PLAIN` o `LOGIN`
      - **[!UICONTROL SSL]** - Scegliere il tipo di verifica per il certificato di sicurezza del server: `SSL` o `TLS`

     ![Configurazione avanzata - impostazioni invio posta](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales Emails]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General Settings]**.

1. Imposta **[!UICONTROL Asynchronous sending]** su `Enable`.

   ![Configurazione vendite - impostazioni generali e-mail](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Per un elenco dettagliato delle impostazioni di configurazione, vedere [_Impostazioni generali_](../configuration-reference/sales/sales-emails.md) nel _Riferimento configurazione_.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
