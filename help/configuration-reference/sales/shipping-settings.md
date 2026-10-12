---
title: '[!UICONTROL Sales] > [!UICONTROL Shipping Settings]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] > [!UICONTROL Shipping Settings] dell'amministratore di Commerce.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
TQID: 'https://experienceleague.adobe.com/4-Kmcd3F8pQyMgxp-NmkBFVNuEXWuYn-BOzpvxuFMhU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 04d3134c-2afb-5bd7-ac14-e19fa935e848
    internal-label: Shipping/Delivery
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
source-wordcount: '209'
ht-degree: 4%
---
# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Impostazioni di spedizione](../../stores-purchase/shipping-settings.md) nella _Guida agli store e all&#39;acquisto_.

## [!UICONTROL Origin]

![Origine](./assets/shipping-settings-origin.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Country] | Sito Web | Il paese del punto di origine. |
| [!UICONTROL Region/State] | Sito Web | Regione o stato del punto di origine. |
| [!UICONTROL ZIP/Postal Code] | Sito Web | Il codice postale o ZIP del punto di origine. |
| [!UICONTROL City] | Sito Web | La città del punto di origine. |
| [!UICONTROL Street Address] | Sito Web | Indirizzo del punto di origine. |
| [!UICONTROL Street Address Line 2] | Sito Web | Una riga aggiuntiva per l’indirizzo stradale del punto di origine, se necessario. |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![Parametri criteri di spedizione](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | Sito Web | Determina se la politica di spedizione viene visualizzata durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Shipping Policy] | Visualizzazione store | Contiene la politica di spedizione come testo. |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."}

![Parametri criteri di spedizione](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | Visualizzazione store | Determina se i numeri di registrazione delle spedizioni inviati nelle e-mail dei clienti sono collegamenti o testo normale. Il valore predefinito `No` indica che i numeri sono testo normale. Opzioni: `Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | Visualizzazione store | Il modello URL per le spedizioni del servizio postale degli Stati Uniti. |
| [!UICONTROL UPS Tracking URL] | Visualizzazione store | Modello URL per spedizioni United Parcel Service. |
| [!UICONTROL FedEx Tracking URL] | Visualizzazione store | Modello URL per spedizioni Federal Express. |
| [!UICONTROL DHL Tracking URL] | Visualizzazione store | Modello URL per spedizioni DHL Express. |

{style="table-layout:auto"}
