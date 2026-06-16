---
title: Categorie nascoste
description: Scopri come utilizzare le categorie nascoste per scopi interni o per creare un collegamento a una categoria non inclusa nel menu di navigazione.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# Categorie nascoste

Esistono molti modi per utilizzare le categorie nascoste. È possibile creare ulteriori livelli di categoria per scopi interni, ma mostrare solo le categorie di livello superiore ai clienti. In alternativa, potrebbe essere necessario creare un collegamento a una categoria non inclusa nel menu di navigazione.

## Creare categorie nascoste

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la categoria che si desidera nascondere ed eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Is Active]** su `Yes`.
   - Imposta **[!UICONTROL Include in Menu]** su `No`.

1. Nella sezione **[!UICONTROL Display Settings]**, impostare **[!UICONTROL Anchor]** su `No`.

   ![Categoria nascosta](./assets/hidden-categories.png){width="600" zoomable="yes"}

   La categoria nascosta è attiva, ma non viene visualizzata nel menu superiore o nella navigazione a livelli.

1. Per creare sottocategorie, completa le seguenti impostazioni per ogni sottocategoria nascosta:

   >[!NOTE]
   >
   >Anche se la categoria è nascosta, puoi creare sottocategorie al di sotto di essa e renderle attive.

   - Imposta **[!UICONTROL Enable Category]** su `Yes`.
   - Nella sezione **[!UICONTROL Display Settings]**, impostare **[!UICONTROL Anchor]** su `Yes`.

   Come categorie attive, ora è possibile collegarsi ad esse da altre posizioni nel negozio, ma non vengono visualizzate nel menu.

1. Al termine, fare clic su **[!UICONTROL Save]**.
