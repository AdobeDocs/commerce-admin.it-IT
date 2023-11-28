---
title: Autenticazione a due fattori (2FA)
description: Scopri il supporto dell’autenticazione a due fattori per garantire la sicurezza dello store e dei dati.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Autenticazione a due fattori (2FA)

Il Commerce _Amministratore_ per l&#39;installazione di Adobe Commerce o di Magento Open Source, consente di accedere al negozio, agli ordini e ai dati dei clienti. Per impedire l’accesso non autorizzato ai tuoi dati, tutti gli utenti che tenteranno di accedere a _Amministratore_ deve completare un processo di autenticazione per verificarne l’identità.

>[!NOTE]
>
>Questa implementazione dell’autenticazione a due fattori (2FA) si applica al _Amministratore_ solo, e non è disponibile per gli account cliente. L’autenticazione a due fattori che protegge l’account Commerce dispone di una configurazione separata. Per ulteriori informazioni, consulta [Proteggere l’account Commerce](../getting-started/commerce-account-secure.md).

L’autenticazione a due fattori è ampiamente utilizzata ed è comune generare codici di accesso per siti web diversi sulla stessa app. In questo modo solo l&#39;utente sarà in grado di accedere al proprio account utente. Se si perde la password o se un bot la indovina, l&#39;autenticazione a due fattori aggiunge un livello di protezione. Ad esempio, puoi utilizzare Google Authenticator per generare codici per l’amministratore del negozio, l’account Commerce e l’account Google.

![IPHONE di configurazione della sicurezza - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce supporta metodi 2FA di più provider. Alcune richiedono l’installazione di un’app che genera una password monouso (OTP) immessa dagli utenti all’accesso per verificarne l’identità. I dispositivi universali di secondo fattore (U2F) assomigliano a una chiave fob e generano una chiave univoca per verificare l’identità. Altre periferiche verificano l&#39;identità quando vengono inserite in una porta USB. In qualità di amministratore dello store, puoi richiedere uno o più metodi 2FA disponibili per verificare l’identità dell’utente. La configurazione 2FA si applica a tutti i siti Web e gli archivi associati all&#39;installazione di Adobe Commerce.

La prima volta che un utente accede a _Amministratore_, devono impostare ogni [2FA](../configuration-reference/security/2fa.md) metodo che richiedi e verificane l’identità utilizzando l’app o il dispositivo associato. Dopo questa configurazione iniziale, l’utente deve eseguire l’autenticazione con uno dei metodi configurati ogni volta che accede. Le informazioni 2FA di ogni utente vengono registrate nel _Amministratore_ account e può essere [ripristina](security-two-factor-authentication-manage.md) se necessario. Per ulteriori informazioni sulla procedura di accesso, consulta [_Amministratore_ Accedi](../getting-started/admin-signin.md).

>[!NOTE]
>
>Gli archivi che hanno abilitato l’autenticazione Adobe Identity Management Services (IMS) hanno Adobe Commerce nativo e Magento Open Source 2FA disabilitato. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza Commerce con le credenziali di Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica dell’integrazione di Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Puoi guardare questo [demo video](https://video.tv.adobe.com/v/339104?quality=12&learn=on) per una panoramica dell’autenticazione a due fattori in Admin.

## Configurare i provider 2FA richiesti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Security]** e scegli **[!UICONTROL 2FA]**.

1. In _[!UICONTROL General]_sezione, seleziona ogni **[!UICONTROL Provider to use]**.

   | Provider | Funzione |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Genera una password monouso nell&#39;applicazione per l&#39;autenticazione utente. |
   | [!UICONTROL Duo Security] | Fornisce notifiche SMS e push. |
   | [!UICONTROL Authy] | Genera un codice a sei cifre dipendente dal tempo e fornisce protezione o token SMS o Voice Call 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Utilizza un dispositivo fisico per l’autenticazione, ad esempio [[!DNL YubiKey]](https://www.yubico.com/). |

   Per selezionare più metodi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ogni elemento.

1. Completare le impostazioni per ogni metodo 2FA richiesto.

   ![Configurazione della sicurezza - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

   La prima volta che gli utenti accedono a _Amministratore_, devono impostare ogni metodo 2FA richiesto. Dopo questa configurazione iniziale, ogni volta che effettuano l’accesso devono eseguire l’autenticazione con uno dei metodi configurati.

## Impostazioni provider 2FA

Completare le impostazioni per ogni metodo 2FA richiesto.

### Google

Per modificare il periodo di tempo in cui la password monouso (OTP) è disponibile durante l&#39;accesso, deselezionare **[!UICONTROL Use system value]** casella di controllo. Quindi, inserisci il numero di secondi che desideri **[!UICONTROL OTP Window]** per essere valido.

![Configurazione della sicurezza - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

### [!DNL Duo Security]

Immetti le seguenti credenziali dal tuo account Duo Security:

- Chiave di integrazione
- Chiave segreta
- Nome host API

![Configurazione della sicurezza - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Immetti la chiave API dal tuo [!DNL Authy] account.

1. Per modificare il messaggio predefinito visualizzato durante l&#39;autenticazione, deselezionare **[!UICONTROL Use system value]** casella di controllo. Quindi, immetti il **[!UICONTROL OneTouch Message]** che desideri visualizzare.

   ![Configurazione della sicurezza - Autenticazione](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Dispositivi U2F ([!DNL Yubikey] e altri)

Per impostazione predefinita, il dominio dell&#39;archivio viene utilizzato durante il processo di autenticazione. Per utilizzare un dominio personalizzato per risolvere i problemi di autenticazione, cancella **[!UICONTROL Use system value]** casella di controllo. Quindi, immetti il **[!UICONTROL WebAPi Challenge Domain]**.

![Configurazione della sicurezza - Dispositivi U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
