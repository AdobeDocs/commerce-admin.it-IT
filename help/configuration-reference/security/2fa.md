---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Security] &gt; [!UICONTROL 2FA] dell'amministratore di Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: d6f9c5186276b28cada318cbe765e2271d34bb58
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Gli archivi che hanno abilitato l’autenticazione Adobe Identity Management Services (IMS) hanno Adobe Commerce nativo e l’autenticazione a due fattori (2FA) di Magento Open Source disabilitata. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza di Adobe Commerce con le relative credenziali di Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica sull&#39;integrazione di Adobe Commerce con Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Autenticazione a due fattori (2FA)](../../systems/security-two-factor-authentication.md) nella _Guida ai sistemi di amministrazione_.

## [!UICONTROL General]

![Generale](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Globale | Indica i metodi di autenticazione a due fattori richiesti. Se si selezionano più provider, ogni utente dovrà configurare ogni metodo 2FA al successivo accesso. |
| [!UICONTROL Configuration Email URL for Web API] | Globale | Per le implementazioni personalizzate, l&#39;URL di un collegamento di configurazione e-mail alternativo inviato agli utenti _Admin_ al primo accesso. Nel modello e-mail, utilizza il segnaposto `:tfat` per indicare dove viene inserito il token. |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Globale | Determina per quanto tempo (in secondi) il sistema accetta la password monouso (OTP) di un amministratore dopo la scadenza. Non può essere superiore alla durata di un singolo OTP (in genere 30 secondi). Predefinito: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Sicurezza Duo](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Globale | La chiave di integrazione dal tuo account [!DNL Duo Security]. |
| [!UICONTROL Secret Key] | Globale | La chiave segreta del tuo account [!DNL Duo Security]. |
| [!UICONTROL API Hostname] | Globale | Il nome host API dall&#39;account [!DNL Duo Security]. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL API Key] | Globale | Chiave API dell&#39;account [!DNL Authy]. |
| [!UICONTROL OneTouch Message] | Globale | Messaggio visualizzato nell&#39;autenticatore [!DNL Authy] all&#39;accesso. Predefinito: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Chiave U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Globale | Il dominio utilizzato per emettere ed elaborare [!DNL WebAuthn] problemi per le implementazioni WebAPI personalizzate. |

{style="table-layout:auto"}
