---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Services] > [!UICONTROL Magento Web API] dell'amministratore di Commerce.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![Impostazioni SOAP](./assets/web-api-soap-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Visualizzazione store | Determina il set di caratteri predefinito. Se vuoto, viene utilizzato UTF-8. |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![Limiti di input GraphQl](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Visualizzazione store | Determina se i limiti di input sono abilitati per le chiamate GraphQL. Valore predefinito: `No`. |
| [!UICONTROL Maximum Page Size] | Visualizzazione store | Imposta il numero massimo di elementi consentiti in un risultato di ricerca impaginato nella risposta di GraphQL. Questa opzione non è disponibile quando _Abilita limiti di input_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Limiti Di Input Api Web](./assets/web-api-input-limits.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Visualizzazione store | Determina se i limiti di input sono abilitati per le chiamate API Web. Valore predefinito: `No`. |
| Limite elenco input | Visualizzazione store | Imposta il numero massimo di elementi consentiti in una proprietà di matrice di entità nella richiesta API Web. Questa opzione non è disponibile quando _Abilita limiti di input_ = `No`. |
| [!UICONTROL Maximum Page Size] | Visualizzazione store | Imposta il numero massimo di elementi consentiti in un risultato di ricerca impaginato nella risposta API Web. Questa opzione non è disponibile quando _Abilita limiti di input_ = `No`. |
| [!UICONTROL Default Page Size] | Visualizzazione store | Imposta il numero predefinito di elementi in un risultato di ricerca impaginato nella risposta API Web. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Sicurezza API Web](./assets/web-api-security.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Globale | Determina se gli ospiti possono accedere in modo anonimo a CMS, catalogare e archiviare risorse dalle API SOAP e REST. Per impostazione predefinita, l&#39;accesso come ospite anonimo non è consentito. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![Autenticazione JWT](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Globale | Specifica il tipo di algoritmo JWS o JWE utilizzato per la crittografia JWT (JSON Web Token) |
| [!UICONTROL Content encryption algorithm for JWEs] | Globale | Specifica il tipo di algoritmo di crittografia del contenuto utilizzato per la crittografia JWT quando si seleziona l’algoritmo JWE. Questa opzione viene ignorata per gli algoritmi JWS. |
| [!UICONTROL Customer JWT Expires In] | Globale | Imposta il periodo di tempo (in minuti) prima della scadenza di un token Bearer JWT del cliente. Il token Bearer JWT del cliente scade tra 30 minuti se questo campo è vuoto o ha un valore negativo. Valore predefinito: `60` |
| [!UICONTROL Admin User JWT Expires In] | Globale | Imposta il periodo di tempo (in minuti) prima della scadenza del token Bearer JWT di amministrazione. Il token Bearer JWT dell’amministratore scade tra 30 minuti se questo campo è vuoto o contiene un valore negativo. Valore predefinito: `60` |

{style="table-layout:auto"}
