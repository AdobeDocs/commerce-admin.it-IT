---
title: Configurare la sicurezza dell’amministratore
description: Scopri come configurare la sicurezza per l’amministratore del tuo store.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Configurare la sicurezza dell’amministratore

È consigliabile adottare un approccio multidimensionale per proteggere la sicurezza del negozio. Puoi iniziare utilizzando un [URL amministratore personalizzato](../stores-purchase/store-urls.md#use-a-custom-admin-url) non è facile da indovinare, piuttosto che l’ovvio &quot;Admin&quot; o &quot;Backend&quot;. Per impostazione predefinita, le password utilizzate per [accedi](../getting-started/admin-signin.md) La lunghezza di to the Admin deve essere di sette o più caratteri e deve includere sia lettere che numeri. As a [best practice](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), utilizza solo password amministratore sicure che includono una combinazione di lettere, numeri e simboli. Adobe Commerce e Magento Open Source non consentono il riutilizzo delle ultime quattro password assegnate all’account.

La configurazione della sicurezza Admin consente di:

- Aggiungere una chiave segreta agli URL
- Richiedi distinzione tra maiuscole e minuscole per le password
- Limitare la durata delle sessioni di amministrazione
- Limita la durata delle password
- Limita il numero di tentativi di accesso che possono essere effettuati prima che l’account utente amministratore sia [bloccato](permissions-users-all.md#locked-users).

Per una maggiore sicurezza, è possibile configurare la durata dell&#39;inattività della tastiera prima della scadenza della sessione corrente e richiedere che il nome utente e la password siano sensibili all&#39;uso di maiuscole e minuscole.

Oltre alle impostazioni di protezione in questa sezione, [autenticazione a due fattori](security-two-factor-authentication.md) (2FA) è necessario per verificare l’identità degli utenti con una password monouso generata da un’app o da un dispositivo. La prima volta che accedi all’amministratore, ti viene richiesto di configurare 2FA. Per una maggiore sicurezza, è possibile configurare l’accesso amministratore anche per richiedere un’ [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Archivi che hanno abilitato [!DNL Adobe Identity Management Services] Per l’autenticazione IMS, Adobe Commerce nativo e Magento Open Source 2FA sono disabilitati. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza Commerce con le credenziali di Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [[!DNL Adobe Identity Management Service] Panoramica dell’integrazione di (IMS)](../getting-started/adobe-ims-integration-overview.md).

Per informazioni tecniche, consulta [Panoramica sulla sicurezza](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} nella documentazione per gli sviluppatori.

![Sicurezza di amministrazione](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configurare la sicurezza dell’amministratore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL Advanced]_, scegli **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Security]** sezione.

1. Per impedire agli utenti amministratori di effettuare l’accesso dallo stesso account su dispositivi diversi, imposta **[!UICONTROL Admin Account Sharing]** a `No`.

1. Per determinare il metodo utilizzato per gestire le richieste di reimpostazione della password, impostare **[!UICONTROL Password Reset Protection Type]** a uno dei seguenti elementi:

   - `By IP and Email` — È possibile reimpostare la password online dopo aver ricevuto una risposta dalla notifica inviata all&#39;indirizzo e-mail associato all&#39;account Admin.
   - `By IP` — La password può essere reimpostata online senza ulteriore conferma.
   - `By Email` — La password può essere reimpostata solo rispondendo via e-mail alla notifica inviata all&#39;indirizzo e-mail associato all&#39;account Admin.
   - `None` — La password può essere reimpostata solo dall&#39;amministratore dello store.

1. Impostare le opzioni di protezione di accesso:

   - Per **[!UICONTROL Recovery Link Expiration Period (hours)]**, immettere il numero di ore in cui il collegamento di ripristino della password rimane valido.

   - Per determinare il numero massimo di richieste di password che è possibile inviare all&#39;ora, immettere il numero per **[!UICONTROL Max Number of Password Reset Requests]**.

   - Per **[!UICONTROL Min Time Between Password Reset Requests]**, immetti il numero minimo di minuti che devono trascorrere tra le richieste di reimpostazione della password.

   - Per aggiungere una chiave segreta all’URL dell’amministratore come precauzione contro gli exploit, imposta **[!UICONTROL Add Secret Key to URLs]** a `Yes`. Questa impostazione è attivata per impostazione predefinita.

   - Per richiedere che l&#39;utilizzo di caratteri maiuscoli e minuscoli nelle credenziali di accesso immesse corrisponda a quanto memorizzato nel sistema, impostare **[!UICONTROL Login is Case Sensitive]** a `Yes`.

   - Per determinare la durata di una sessione di amministrazione prima del timeout, immetti la durata della sessione in secondi per **[!UICONTROL Admin Session Lifetime (seconds)]** campo. Il valore deve essere di almeno 60 secondi.

   - Per **[!UICONTROL Maximum Login Failures to Lockout Account]**, immetti quante volte un utente può tentare di accedere all’amministratore prima che l’account venga bloccato. Per impostazione predefinita, sono consentiti sei tentativi. Lascia vuoto il campo per tentativi di accesso illimitati.

   - Per **[!UICONTROL Lockout Time (minutes)]**, immetti il numero di minuti in cui un account Amministratore viene bloccato quando viene raggiunto il numero massimo di tentativi.

1. Impostare le opzioni della password:

   - Per limitare la durata delle password amministratore, immettere il numero di giorni di validità di una password **[!UICONTROL Password Lifetime (days)]**. Per una durata illimitata, lascia vuoto il campo.

   - Imposta **[!UICONTROL Password Change]** a uno dei seguenti elementi:

      - `Forced` — Richiede che gli utenti Admin modifichino le loro password dopo la configurazione dell&#39;account.
      - `Recommended` — consiglia agli utenti amministratori di modificare le password dopo la configurazione dell&#39;account.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Requisiti della password amministratore

Per impostazione predefinita, una password amministratore deve avere una lunghezza di sette o più caratteri e includere sia lettere che numeri.
