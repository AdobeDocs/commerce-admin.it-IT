---
title: '[!UICONTROL Security] > [!UICONTROL 2FA]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Security] > [!UICONTROL 2FA] dell'amministratore di Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/-5t8bTj14iB---88TotUNefATWwE80LTswPO3xVWU70
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Per gli archivi che hanno abilitato l’autenticazione IMS (Adobe Identity Management Services), l’autenticazione a due fattori (2FA) nativa di Adobe Commerce e Magento Open Source è disabilitata. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza di Adobe Commerce con le credenziali Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica sull&#39;integrazione di Adobe Commerce con Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Autenticazione a due fattori (2FA)](../../systems/security-two-factor-authentication.md) nella _Guida ai sistemi di amministrazione_.

## [!UICONTROL General]

![Generale](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Globale | Indica i metodi di autenticazione a due fattori richiesti. Se si selezionano più provider, ogni utente dovrà configurare ogni metodo 2FA al successivo accesso. |
| [!UICONTROL Configuration Email URL for Web API] | Globale | Per le implementazioni personalizzate, l&#39;URL di un collegamento di configurazione e-mail alternativo inviato agli utenti _Admin_ al primo accesso. Nel modello e-mail, utilizza il segnaposto `:tfat` per indicare dove viene inserito il token. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Globale | Determina quante volte un amministratore può immettere un [!DNL one-time password (OTP)] prima che il suo account venga temporaneamente disabilitato. Predefinito: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Globale | Determina per quanto tempo (in secondi) un amministratore può attendere di immettere un [!DNL one-time password (OTP)] prima che il suo account venga temporaneamente disabilitato. Predefinito: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Globale | Determina per quanto tempo (in secondi) il sistema accetta [!DNL one-time-password (OTP)] di un amministratore dopo la scadenza. Non può essere superiore alla durata di un singolo OTP (in genere 30 secondi). Predefinito: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Sicurezza Duo](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Client Id] | Globale | ID client dall&#39;account [!DNL Duo Security]. |
| [!UICONTROL Client Secret] | Globale | Il segreto client dall&#39;account [!DNL Duo Security]. |
| [!UICONTROL Integration Key] | Globale | Chiave di integrazione dall&#39;account API [!DNL Duo Security]. |
| [!UICONTROL Secret Key] | Globale | Chiave segreta dell&#39;account API [!DNL Duo Security]. |
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
