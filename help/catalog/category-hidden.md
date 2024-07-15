---
title: Categorie nascoste
description: Scopri come utilizzare le categorie nascoste per scopi interni o per creare un collegamento a una categoria non inclusa nel menu di navigazione.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
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
