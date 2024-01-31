---
title: Gestire la gerarchia aziendale
description: Scopri come gestire le organizzazioni B2B con modelli operativi complessi creando gerarchie aziendali
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Gestire [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti ai programmi beta"}

Gli amministratori possono creare un [!UICONTROL Company Hierarchy] assegnando società collegate a una società madre designata, che è la società in cima all&#39;organizzazione. Se il [!UICONTROL Company Type] è `Company`, la società non fa parte di un&#39;organizzazione ed è idonea a diventare una società madre o a essere assegnata a una società madre esistente.

In Amministratore, puoi gestire le assegnazioni aziendali modificando una società e quindi aggiornando la [!UICONTROL Company Hierarchy] configurazione per assegnare o annullare l’assegnazione delle società.

![Griglia gerarchia società](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Per ulteriori informazioni su [!UICONTROL Company Hierarchy] griglia, vedere [Gerarchia società](account-company-create.md#company-hierarchy) descrizioni dei campi.

## Assegnare società a un&#39;organizzazione

1. Dalla sezione _Amministratore_ barra laterale, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Griglia Aziende](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. In [!UICONTROL Companies] griglia, aprire la pagina dettagli società per creare le assegnazioni.

   - Per assegnare altre società a una società padre esistente, selezionare **[!UICONTROL Edit]** azione per la società madre.
   - Per creare una società padre, selezionare **[!UICONTROL Edit]** azione per la società da designare come padre.

     Impossibile creare una società padre da una società padre o figlio esistente.

1. Nella pagina dei dettagli della società, espandi **[!UICONTROL Company Hierarchy]**.

   ![Griglia gerarchia società](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   La griglia mostra le assegnazioni esistenti della società, se presenti. La società madre è sempre posizionata al di sopra del [!UICONTROL Company Hierarchy] griglia. Il `[!UICONTROL Current]` Il flag indica la società in fase di modifica.

1. Aggiungere società all&#39;organizzazione padre.

   - Scegli da un elenco di società disponibili selezionando **[!UICONTROL Assign Companies]**.

   - **Seleziona tutto su questa pagina**, oppure seleziona una o più voci aziendali specifiche.

   - Seleziona **[!UICONTROL Assign Selected Companies]**.

   - Completa l&#39;assegnazione della società selezionando **[!UICONTROL Assign]**.

     ![Assegna società all&#39;organizzazione](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Annullamento dell’assegnazione di società a una società madre

1. Il giorno _Amministratore_ barra laterale, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Griglia Aziende](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. In [!UICONTROL Companies] griglia, aprire la pagina dei dettagli della società per la società padre selezionando **[!UICONTROL Edit]**.

1. Visualizzare l&#39;elenco delle società assegnate espandendo **[!UICONTROL Company Hierarchy]**.

1. Dalla sezione [!UICONTROL Company Hierarchy] griglia, annullare l&#39;assegnazione di una società utilizzando **[!UICONTROL Select]** controllo azione da scegliere **[!UICONTROL Unassign from parent]**.

   ![Annullare l’assegnazione di società a un’organizzazione principale](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Quando richiesto, rimuovere la società assegnata dalla gerarchia selezionando **[!UICONTROL Unassign]**.
