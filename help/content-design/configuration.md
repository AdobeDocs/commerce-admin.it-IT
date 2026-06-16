---
title: Configurazione del progetto
description: La configurazione di progettazione consente di modificare facilmente le regole e le impostazioni di configurazione relative alla progettazione visualizzandole in una singola pagina.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
TQID: https://experienceleague.adobe.com/6sccsrSWuaF6BkKqngQq3JH2GerWxfybWd5aXcs0gIc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# Configurazione del progetto

La configurazione Progettazione consente di modificare facilmente le regole e le impostazioni di configurazione relative alla progettazione visualizzandole in una singola pagina.

![Pagina Configurazione progettazione](./assets/configuration.png){width="700" zoomable="yes"}

## Modificare la configurazione del progetto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione archivio da configurare e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

   Nella pagina vengono visualizzate le impostazioni di progettazione correnti per la visualizzazione Store.

1. Per modificare il tema predefinito, impostare **[!UICONTROL Applied Theme]** sul tema che si desidera applicare alla visualizzazione.

   Se non viene specificato alcun tema, viene utilizzato il tema predefinito del sistema. Alcune estensioni di terze parti modificano il tema predefinito del sistema.

1. [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} Se il tema deve essere utilizzato solo per un dispositivo specifico, impostare **[!UICONTROL User Agent Rules]**.

   ![Regole agente utente](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Per ogni tipo di dispositivo in cui si desidera specificare un tema:

   - Fare clic su **[!UICONTROL Add New User Agent Rule]**.

   - Per **[!UICONTROL Search String]**, immettere l&#39;ID del browser per il dispositivo specifico.

     Una stringa di ricerca può essere un&#39;espressione normale o un&#39;espressione regolare compatibile con Perl (PCRE) (per ulteriori informazioni, vedere [Agente utente](https://en.wikipedia.org/wiki/User_agent)). La seguente stringa di ricerca identifica Firefox:

         /^mozilla/i
     
   - Per **[!UICONTROL Theme Name]**, scegliere il tema da utilizzare per il dispositivo specificato.

   >[!NOTE]
   >
   >Puoi aggiungere tutte le regole per i dispositivi che desideri designare. Le stringhe di ricerca vengono confrontate nell&#39;ordine in cui vengono immesse.

1. In _[!UICONTROL Other Settings]_&#x200B;espandere ogni sezione e seguire le istruzioni degli argomenti collegati per modificare le impostazioni in base alle esigenze.

   - [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [[!UICONTROL Header]](page-setup.md#header)
   - [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [[!UICONTROL Footer]](page-setup.md#footer)
   - [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Altre impostazioni da modificare](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.
