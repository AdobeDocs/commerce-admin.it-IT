---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Security] &gt; [!UICONTROL 2FA] pagina dell’amministratore di Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Gli archivi che hanno abilitato l’autenticazione Adobe Identity Management Services (IMS) hanno Adobe Commerce nativo e l’autenticazione a due fattori (2FA) di Magento Open Source disabilitata. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza di Adobe Commerce con le relative credenziali di Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica sull’integrazione di Adobe Commerce con Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Autenticazione a due fattori (2FA)](../../systems/security-two-factor-authentication.md) nel _Guida ai sistemi di amministrazione_.

## [!UICONTROL General]

![Generale](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Globale | Indica i metodi di autenticazione a due fattori richiesti. Se si selezionano più provider, ogni utente dovrà configurare ogni metodo 2FA al successivo accesso. |
| [!UICONTROL Configuration Email URL for Web API] | Globale | Per le implementazioni personalizzate, l’URL di un collegamento di configurazione e-mail alternativo inviato a _Amministratore_ utenti al primo accesso. Nel modello e-mail, utilizza il segnaposto `:tfat` per indicare dove viene iniettato il token. |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Globale | Durata in secondi di ciascuna password monouso (OTP) generata da Google Authenticator. Predefinito: `30` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Security](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Globale | La chiave di integrazione dal tuo [!DNL Duo Security] account. |
| [!UICONTROL Secret Key] | Globale | La chiave segreta dal tuo [!DNL Duo Security] account. |
| [!UICONTROL API Hostname] | Globale | Il nome host API dal tuo [!DNL Duo Security] account. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL API Key] | Globale | La chiave API dal tuo [!DNL Authy] account. |
| [!UICONTROL OneTouch Message] | Globale | Il messaggio visualizzato nel [!DNL Authy] autenticatore all’accesso. Predefinito: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Chiave U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Globale | Dominio utilizzato per emettere ed elaborare [!DNL WebAuthn] problemi relativi alle implementazioni WebAPI personalizzate. |

{style="table-layout:auto"}
