---
title: Rilevamento funzionalità browser
description: Scopri come configurare il rilevamento delle funzionalità del browser e visualizzare un avviso nel caso in cui sia necessario modificare le impostazioni del browser del cliente.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# Rilevamento funzionalità browser

Come la maggior parte dei siti web e delle applicazioni su Internet, Adobe Commerce e Magento Open Source richiedono che il browser del visitatore consenta sia i cookie che JavaScript per il funzionamento completo. Tuttavia, a volte il browser di un utente è impostato sull’impostazione di privacy più alta che impedisce sia i cookie che JavaScript. Il tuo store può essere configurato per testare le funzionalità del browser di ogni visitatore e visualizzare un avviso se le impostazioni devono essere modificate.

- Se le impostazioni di privacy del browser non consentono i cookie, è possibile configurare il sistema per reindirizzarli automaticamente alla pagina [Abilita cookie](../content-design/pages.md#enable-cookies), che spiega come creare le impostazioni consigliate con la maggior parte dei browser.
- Se le impostazioni di privacy del browser non consentono JavaScript, è possibile configurare il sistema in modo che visualizzi il seguente messaggio sopra l&#39;intestazione di ogni pagina.

Per informazioni tecniche, consultare [Browser supportati](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=it#supported-browsers) nella _Guida all&#39;installazione_.

## Configurare il rilevamento delle funzionalità del browser

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Browser Capabilities Detection]** ed effettuare le seguenti operazioni:

   - Per visualizzare istruzioni che spiegano come configurare il browser per l&#39;autorizzazione dei cookie, impostare **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** su `Yes`.

   - Per visualizzare un banner sopra l&#39;intestazione quando JavaScript è disabilitato nel browser dell&#39;utente, impostare **[!UICONTROL Show Notice if JavaScript is Disabled]** su `Yes`.

   - Per visualizzare un banner sopra l&#39;intestazione quando Local Storage è disabilitato nel browser dell&#39;utente, impostare **[!UICONTROL Show Notice if Local Storage is Disabled]** su `Yes`.

   ![Configurazione generale - Rilevamento funzionalità browser Web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
