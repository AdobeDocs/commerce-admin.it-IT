---
title: '[!UICONTROL Services] &gt; [!UICONTROL Magento Web API]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Services] &gt; [!UICONTROL Magento Web API] pagina dell’amministratore di Commerce.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '324'
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

![Limiti di input di GraphQl](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Visualizzazione store | Determina se i limiti di input sono abilitati per le chiamate GraphQL. Valore predefinito: `No`. |
| [!UICONTROL Maximum Page Size] | Visualizzazione store | Imposta il numero massimo di elementi consentiti in un risultato di ricerca impaginato nella risposta di GraphQL. Questa opzione non è disponibile quando _Abilita limiti di input_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Limiti di input API Web](./assets/web-api-input-limits.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Visualizzazione store | Determina se i limiti di input sono abilitati per le chiamate API Web. Valore predefinito: `No`. |
| Limite elenco input | Visualizzazione store | Imposta il numero massimo di elementi consentiti in una proprietà di matrice di entità nella richiesta API Web. Questa opzione non è disponibile quando _Abilita limiti di input_ = `No`. |
| [!UICONTROL Maximum Page Size] | Visualizzazione store | Imposta il numero massimo di elementi consentiti in un risultato di ricerca impaginato nella risposta API Web. Questa opzione non è disponibile quando _Abilita limiti di input_ = `No`. |
| [!UICONTROL Default Page Size] | Visualizzazione store | Imposta il numero predefinito di elementi in un risultato di ricerca impaginato nella risposta API Web. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Sicurezza API web](./assets/web-api-security.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Globale | Determina se gli utenti guest possono accedere in modo anonimo a CMS, catalogare e archiviare risorse dalle API SOAP e REST. Per impostazione predefinita, l&#39;accesso come ospite anonimo non è consentito. Opzioni: `Yes` / `No` |

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
