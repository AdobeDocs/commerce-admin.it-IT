---
title: '[!UICONTROL Services] > [!UICONTROL Commerce Services Connector]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Services] > [!UICONTROL Commerce Services Connector] dell'amministratore di Commerce.
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: 'https://experienceleague.adobe.com/50XCqY8JMjvf9G-wcHLxvlskSd5noIAB0LIX6xMarL0'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

Per informazioni su come connettere il tuo archivio ai servizi Adobe Commerce, consulta [Servizi Commerce](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas).

{{config}}

## [!UICONTROL Sandbox API Keys]

![Chiave API sandbox](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | Globale | Chiave API che identifica l’autore e i relativi diritti, se presenti. |
| [!UICONTROL Sandbox private API key] | Globale | Una chiave privata associata alla chiave API. |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![Chiave API di produzione](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Production public API key] | Globale | Chiave API che identifica l’autore e i relativi diritti, se presenti. |
| [!UICONTROL Production private API key] | Globale | Una chiave privata associata alla chiave API. |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![Identificatore SaaS](./assets/saas-identifier.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Project] | Globale | Nome del progetto SaaS che raggruppa tutti gli spazi di dati SaaS. Se non esistono progetti SaaS, viene visualizzato il pulsante _Crea progetto_. |
| [!UICONTROL Data Space] | Globale | Elenca gli spazi di dati SaaS nel progetto SaaS specificato. Il numero di spazi dati SaaS dipende dalla [licenza Commerce](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas):<br />Adobe Commerce - Uno spazio dati di produzione; due spazi dati di test;<br />Magento Open Source - Uno spazio dati di produzione; nessuno spazio dati di test |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![Organizzazione IMS](./assets/ims-organization.png)<!-- zoom -->

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Il tuo Adobe ID è in genere l’indirizzo e-mail utilizzato per la prima volta quando hai iniziato a iscriverti o acquistato un’applicazione o un servizio Adobe. Il tuo Adobe ID è la chiave di cui hai bisogno per accedere al tuo account Adobe. |

{style="table-layout:auto"}
