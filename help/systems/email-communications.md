---
title: Configurare le comunicazioni e-mail
description: Scopri come configurare le comunicazioni e-mail, incluso il routing delle e-mail restituite o delle risposte a un indirizzo e-mail specifico.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Configurare le comunicazioni e-mail

Il _Impostazioni invio posta_ consente di indirizzare e-mail restituite o risposte a un indirizzo specifico. Se l&#39;archivio è in esecuzione su un server SMTP o Windows, è possibile verificare le impostazioni dell&#39;host e della porta.

>[!IMPORTANT]
>
>**Avviso di protezione** Tutti i commercianti devono impostare immediatamente la propria configurazione di invio della posta per proteggersi da un potenziale exploit di esecuzione del codice remoto identificato di recente. Fino a quando questo problema non viene risolto, si consiglia vivamente di evitare di utilizzare [!DNL Sendmail] per le comunicazioni e-mail. In _[!UICONTROL Mail Sending Settings]_, assicurati che_[!UICONTROL Set Return Path]_ è impostato su `No`.

Per un elenco dettagliato delle impostazioni di configurazione, vedi [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) nel _Riferimento configurazione_.

## Configurare le comunicazioni e-mail

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Mail Sending Settings]** ed effettuare le seguenti operazioni:

   ![Configurazione avanzata - impostazioni di invio posta](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Se necessario, impostare **[!UICONTROL Disable Email Communications]** a `No`.

   - Per **[!UICONTROL Transport]**, scegli il tipo di trasporto per le comunicazioni e-mail dallo store: `Sendmail` o `SMTP`

   - Se l&#39;esecuzione avviene su un server SMTP o Windows, verificare le impostazioni seguenti:

      - **[!UICONTROL Host]** - `localhost` o altro

      - **[!UICONTROL Port (25)]** - `25` o altro

   - Per **[!UICONTROL Set Return Path]**, scegli una delle seguenti opzioni:

      - `No` - (Misura di sicurezza consigliata) Indirizzi che hanno restituito l&#39;e-mail all&#39;indirizzo e-mail predefinito del punto vendita.
      - `Yes` - Indirizzi che hanno restituito l&#39;e-mail all&#39;indirizzo predefinito del punto vendita.
      - `Specified` - Le route hanno restituito l&#39;e-mail all&#39;indirizzo specificato in **[!UICONTROL Return Path Email]**.

   - Se l&#39;esecuzione avviene su un server SMTP, configurare la connessione:

      - **[!UICONTROL Username]** - Immettere il nome utente di accesso per il server SMTP.
      - **[!UICONTROL Password]** - Immettere la password per l&#39;accesso al server SMTP.
      - **[!UICONTROL Auth]** - Scegliere il tipo di autenticazione per la connessione al server SMTP: `NONE` , `PLAIN`, o `LOGIN`
      - **[!UICONTROL SSL]** - Scegliere il tipo di verifica per il certificato di sicurezza del server: `SSL` o `TLS`

     ![Configurazione avanzata - impostazioni di invio posta](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales Emails]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General Settings]** sezione.

1. Imposta **[!UICONTROL Asynchronous sending]** a `Enable`.

   ![Configurazione vendite - Impostazioni generali e-mail](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Per un elenco dettagliato delle impostazioni di configurazione, vedi [_Impostazioni generali_](../configuration-reference/sales/sales-emails.md) nel _Riferimento configurazione_.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
