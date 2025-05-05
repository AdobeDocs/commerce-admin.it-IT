---
title: Autenticazione a due fattori (2FA)
description: Scopri il supporto per l’autenticazione a due fattori per garantire la sicurezza del sistema e dei dati.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 4997c4c01f11d6e0355eb8e02f8f099db685b400
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---

# Autenticazione a due fattori (2FA)

L&#39;_Amministratore_ di Commerce per l&#39;installazione di Adobe Commerce o Magento Open Source consente di accedere al tuo archivio, agli ordini e ai dati dei clienti. Per impedire l&#39;accesso non autorizzato ai tuoi dati, tutti gli utenti che tenteranno di accedere a _Admin_ dovranno completare un processo di autenticazione per verificarne l&#39;identità.

>[!NOTE]
>
>Questa implementazione dell&#39;autenticazione a due fattori (2FA) si applica solo all&#39;amministratore _1&rbrace; e non è disponibile per gli account cliente._ L’autenticazione a due fattori che protegge l’account Commerce dispone di una configurazione separata. Per ulteriori informazioni, vai a [Proteggi il tuo account Commerce](../getting-started/commerce-account-secure.md).

L’autenticazione a due fattori è ampiamente utilizzata ed è comune generare codici di accesso per siti web diversi sulla stessa app. Questa autenticazione aggiuntiva garantisce che solo l’utente sia in grado di accedere al proprio account utente. Se si perde la password o se un bot la indovina, l&#39;autenticazione a due fattori aggiunge un livello di protezione. Ad esempio, puoi utilizzare Google Authenticator per generare codici per l’amministratore del negozio, l’account Commerce e l’account Google.

![Configurazione di sicurezza iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Systems Commerce supporta i metodi 2FA di più fornitori. Alcuni richiedono l&#39;installazione di un&#39;app che genera un password una tantum (OTP) che gli utenti immettono all&#39;accesso per verificare la propria identità. I dispositivi universali del secondo fattore (U2F) assomigliano a un portachiavi e generano una chiave univoca per verificare l&#39;identità. Altri dispositivi verificano l&#39;identità quando vengono inseriti in una porta USB. L&#39;amministratore store può richiedere uno o più metodi 2FA disponibili per verificare la utente identità. La configurazione 2FA si applica a tutti i siti Web e i negozi associati all&#39;installazione di Adobe Systems Commerce.

La prima volta che un utente accede all&#39;account _Admin_, deve configurare ogni metodo [2FA](../configuration-reference/security/2fa.md) richiesto e verificare la propria identità utilizzando l&#39;app o il dispositivo associato. Dopo questa configurazione iniziale, l’utente deve eseguire l’autenticazione con uno dei metodi configurati ogni volta che accede. Le informazioni 2FA di ogni utente vengono registrate nel suo account _Admin_ e possono essere [reset](security-two-factor-authentication-manage.md) se necessario. Per ulteriori informazioni sul processo di accesso, vai a [_Amministratore_ Accedi](../getting-started/admin-signin.md).

>[!NOTE]
>
>Per gli archivi che hanno abilitato l’autenticazione Adobe Identity Management Services (IMS), Adobe Commerce nativo e Magento Open Source 2FA sono disabilitati. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza di Commerce con le credenziali Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica dell&#39;integrazione del servizio Adobe Identity Management (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=it).

Guarda questa [demo video](https://video.tv.adobe.com/v/339104?quality=12&learn=on) per una panoramica dell&#39;autenticazione a due fattori in Admin.

## Configurare i provider 2FA richiesti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Security]** e scegli **[!UICONTROL 2FA]**.

1. _[!UICONTROL General]_&#x200B;Nella sezione selezionare i provider da utilizzare.

   | Provider | Funzione |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Genera una password monouso nell&#39;applicazione per l&#39;autenticazione utente. |
   | [!UICONTROL Duo Security] | Fornisce notifiche SMS e push. |
   | [!UICONTROL Authy] | Genera un codice a sei cifre dipendente dal tempo e fornisce protezione o token SMS o Voice Call 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Utilizza un dispositivo fisico per l&#39;autenticazione, ad esempio [[!DNL YubiKey]](https://www.yubico.com/). |

   Per selezionare più metodi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ogni elemento.

1. Completa le [impostazioni](../configuration-reference/security/2fa.md) per ogni metodo 2FA richiesto.

   ![Configurazione protezione - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

   La prima volta che gli utenti accedono all&#39;amministratore __, devono configurare ogni metodo 2FA richiesto. Dopo questa configurazione iniziale, devono eseguire l&#39;autenticazione con uno dei metodi configurati ogni volta che accedono.

## Provider 2FA Impostazioni

Completare le impostazioni per ogni metodo 2FA richiesto.

### Google

Per modificare la durata della disponibilità della password monouso (OTP) durante l&#39;accesso, deselezionare la casella di controllo **[!UICONTROL Use system value]**. Immettere quindi il numero di secondi di validità di **[!UICONTROL OTP Window]**.

![Configurazione protezione - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>In Adobe Commerce 2.4.7 e versioni successive, l’impostazione di configurazione della finestra OTP controlla per quanto tempo (in secondi) il sistema accetta la password monouso (OTP) di un amministratore dopo la scadenza. Questo valore deve essere inferiore a 30 secondi. L&#39;impostazione predefinita del sistema è `29`.<br><br> Nella versione 2.4.6, l&#39;impostazione della finestra OTP determina il numero di codici OTP passati e futuri che rimangono validi. Il valore `1` indica che il codice OTP corrente più un codice nel passato e un codice nel futuro rimangono validi in un determinato momento.

### [!DNL Duo Security]

Immetti le seguenti credenziali dal tuo account Duo Security:

- Client ID
- Segreto client
- Chiave di integrazione
- Chiave segreta
- Nome host API

![Configurazione di sicurezza - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Immetti la chiave API dal tuo [!DNL Authy] account.

1. Per modificare il messaggio predefinito visualizzato durante l&#39;autenticazione, deselezionare la casella di **[!UICONTROL Use system value]** controllo. Immettere quindi **[!UICONTROL OneTouch Message]** che si desidera visualizzare.

   ![Configurazione protezione - Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Dispositivi U2F ([!DNL Yubikey] e altri)

Per impostazione predefinita, il dominio dell&#39;archivio viene utilizzato durante il processo di autenticazione. Per utilizzare un dominio personalizzato per problemi di autenticazione, deselezionare la casella di controllo **[!UICONTROL Use system value]**. Quindi, immettere **[!UICONTROL WebAPi Challenge Domain]**.

![Configurazione protezione - Dispositivi U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
