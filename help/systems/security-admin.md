---
title: Configurare la sicurezza dell’amministratore
description: Scopri come configurare la sicurezza per l’amministratore del tuo store.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Configurare la sicurezza dell’amministratore

È consigliabile adottare un approccio multidimensionale per proteggere la sicurezza del negozio. Puoi iniziare utilizzando un [URL amministratore personalizzato](../stores-purchase/store-urls.md#use-a-custom-admin-url) non facile da indovinare, anziché l&#39;ovvio &quot;Amministratore&quot; o &quot;Back-end&quot;. Per impostazione predefinita, le password utilizzate per [accedere](../getting-started/admin-signin.md) all&#39;amministratore devono essere composte da sette o più caratteri e includere sia lettere che numeri. Come [best practice](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=it), utilizza solo password amministratore complesse che includono una combinazione di lettere, numeri e simboli. Adobe Commerce e Magento Open Source non consentono il riutilizzo delle ultime quattro password assegnate all’account.

La configurazione della sicurezza Admin consente di:

- Aggiungere una chiave segreta agli URL
- Richiedi distinzione tra maiuscole e minuscole per le password
- Limitare la durata delle sessioni di amministrazione
- Limita la durata delle password
- Limita il numero di tentativi di accesso che possono essere effettuati prima che l&#39;account utente amministratore sia [bloccato](permissions-users-all.md#locked-users).

Per una maggiore sicurezza, è possibile configurare la durata dell&#39;inattività della tastiera prima della scadenza della sessione corrente e richiedere che il nome utente e la password siano sensibili all&#39;uso di maiuscole e minuscole.

Oltre alle impostazioni di protezione in questa sezione, è necessaria l&#39;autenticazione a [due fattori](security-two-factor-authentication.md) (2FA) per verificare l&#39;identità degli utenti con una password monouso generata da un&#39;app o da un dispositivo. La prima volta che accedi all’amministratore, ti viene richiesto di configurare 2FA. Per ulteriore sicurezza, è possibile configurare l&#39;accesso amministratore anche per richiedere un [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Gli archivi che hanno abilitato l&#39;autenticazione [!DNL Adobe Identity Management Services] (IMS) hanno Adobe Commerce nativo e Magento Open Source 2FA disabilitati. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza di Commerce con le credenziali Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Vedi Panoramica sull&#39;integrazione di [[!DNL Adobe Identity Management Service] (IMS)](../getting-started/adobe-ims-integration-overview.md).

Per informazioni tecniche, consulta [Panoramica sulla sicurezza](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} nella documentazione per gli sviluppatori.

![Sicurezza amministratore](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configurare la sicurezza dell’amministratore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL Advanced]_, scegli **[!UICONTROL Admin]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Security]**.

1. Per impedire agli utenti amministratori di effettuare l&#39;accesso dallo stesso account su dispositivi diversi, impostare **[!UICONTROL Admin Account Sharing]** su `No`.

1. Per determinare il metodo utilizzato per gestire le richieste di reimpostazione della password, impostare **[!UICONTROL Password Reset Protection Type]** su uno dei seguenti valori:

   - `By IP and Email` — È possibile reimpostare la password online dopo aver ricevuto una risposta dalla notifica inviata all&#39;indirizzo di posta elettronica associato all&#39;account Admin.
   - `By IP` — La password può essere reimpostata online senza ulteriori conferme.
   - `By Email` — È possibile reimpostare la password solo rispondendo tramite e-mail alla notifica inviata all&#39;indirizzo e-mail associato all&#39;account Admin.
   - `None` — La password può essere reimpostata solo dall&#39;amministratore dello store.

1. Impostare le opzioni di protezione di accesso:

   - Per **[!UICONTROL Recovery Link Expiration Period (hours)]**, immettere il numero di ore in cui il collegamento di ripristino della password rimane valido.

   - Per determinare il numero massimo di richieste di password che è possibile inviare all&#39;ora, immettere il numero per **[!UICONTROL Max Number of Password Reset Requests]**.

   - Per **[!UICONTROL Min Time Between Password Reset Requests]**, immettere il numero minimo di minuti che devono trascorrere tra le richieste di reimpostazione della password.

   - Per aggiungere una chiave segreta all&#39;URL amministratore come precauzione contro gli exploit, impostare **[!UICONTROL Add Secret Key to URLs]** su `Yes`. Questa impostazione è attivata per impostazione predefinita.

   - Per richiedere che l&#39;utilizzo di caratteri maiuscoli e minuscoli nelle credenziali di accesso immesse corrisponda a quanto archiviato nel sistema, impostare **[!UICONTROL Login is Case Sensitive]** su `Yes`.

   - Per determinare la durata di una sessione di amministrazione prima del timeout, immettere la durata della sessione in secondi per il campo **[!UICONTROL Admin Session Lifetime (seconds)]**. Il valore deve essere di almeno 60 secondi.

   - Per **[!UICONTROL Maximum Login Failures to Lockout Account]**, immettere il numero di volte in cui un utente può tentare di accedere all&#39;amministratore prima che l&#39;account venga bloccato. Per impostazione predefinita, sono consentiti sei tentativi. Lascia vuoto il campo per tentativi di accesso illimitati.

   - Per **[!UICONTROL Lockout Time (minutes)]**, immettere il numero di minuti di blocco di un account amministratore quando viene raggiunto il numero massimo di tentativi.

1. Impostare le opzioni della password:

   - Per limitare la durata delle password amministratore, immettere il numero di giorni di validità di una password per **[!UICONTROL Password Lifetime (days)]**. Per una durata illimitata, lascia vuoto il campo.

   - Imposta **[!UICONTROL Password Change]** su uno dei seguenti:

      - `Forced` - Richiede che gli utenti Admin modifichino le password dopo la configurazione dell&#39;account.
      - `Recommended` — consiglia agli utenti amministratori di modificare le password dopo la configurazione dell&#39;account.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Requisiti della password amministratore

Per impostazione predefinita, una password amministratore deve avere una lunghezza di sette o più caratteri e includere sia lettere che numeri.
