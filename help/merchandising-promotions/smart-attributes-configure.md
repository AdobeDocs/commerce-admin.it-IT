---
title: Configurare gli attributi avanzati per Visual Merchandiser
description: Scopri come configurare gli attributi avanzati utilizzati da Visual Merchandiser.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: 'https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 76cfaac4-e563-56dd-8938-708bf8b84956
    internal-label: Attributes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%
---
# Configurare gli attributi avanzati per Visual Merchandiser

{{ee-feature}}

La configurazione di Visual Merchandiser determina gli attributi che possono essere utilizzati nella finestra di merchandising e la soglia minima per le scorte. La configurazione identifica anche l’attributo utilizzato per il colore e l’ordine dei valori di colore.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Visual Merchandiser]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General Options]**.

   ![Configurazione catalogo - merchandiser visivo](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. Nell&#39;elenco **[!UICONTROL Attributes for Category Rules]** selezionare ogni attributo che si desidera rendere disponibile per il merchandising visivo.

   Per selezionare più attributi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ogni elemento.

1. Immettere **[!UICONTROL Minimum Stock Threshold]** per visualizzare un prodotto nella finestra di Visual Merchandiser.

1. Immettere **[!UICONTROL Color Attribute Code]**.

   Il valore predefinito è `color`. Se il catalogo utilizza un attributo diverso, immettere il nome dell&#39;attributo in minuscolo.

1. Per **[!UICONTROL Color Order]**, immettere ogni valore di colore su una riga e in sequenza separate per determinare la priorità di ogni colore.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
