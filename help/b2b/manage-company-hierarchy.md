---
title: Gestire la gerarchia aziendale
description: Creare e gestire gerarchie aziendali per supportare le organizzazioni B2B con modelli operativi complessi.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Gestisci [!UICONTROL Company Hierarchy]

Gli amministratori possono creare un [!UICONTROL Company Hierarchy] assegnando società correlate a una società padre designata, che è la società nella parte superiore della gerarchia organizzativa.

Dall&#39;amministratore, creare una società padre modificando una singola società (`[!UICONTROL Company Type] = Company`) e assegnando società correlate nella configurazione [!UICONTROL Company Hierarchy].

![Griglia gerarchia società](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>Per informazioni dettagliate sulla griglia [!UICONTROL Company Hierarchy], vedere [Descrizioni del campo Gerarchia società](account-company-create.md#company-hierarchy).

Gestire le assegnazioni di società modificando una società padre e utilizzando la griglia *[!UICONTROL Company Hierarchy]* per aggiungere o rimuovere società. Utilizza il controllo *[!UICONTROL Actions]* per gestire la [configurazione avanzata delle impostazioni](#change-company-settings) per le aziende dell&#39;organizzazione.

## Assegnare società a una società madre

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Griglia Aziende](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dalla griglia [!UICONTROL Companies], aprire la pagina dei dettagli della società per creare le assegnazioni.

   - Per assegnare altre società a una società padre esistente, selezionare l&#39;azione **[!UICONTROL Edit]** per la società padre.
   - Per creare una società padre, selezionare l&#39;azione **[!UICONTROL Edit]** per la società designata come padre.

     Impossibile creare una nuova società padre da una società padre o figlio esistente.

1. Nella pagina Dettagli società espandere **[!UICONTROL Company Hierarchy]** e quindi selezionare **[!UICONTROL Assign Companies]**.

   ![Crea società madre](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. Dall&#39;elenco delle società disponibili, scegliere le società da assegnare, quindi selezionare **[!UICONTROL Assign Selected Companies]**.

   ![Selezionare le società da assegnare](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Quando richiesto, completare l&#39;assegnazione della società selezionando **[!UICONTROL Assign]**.

## Annullamento dell’assegnazione di società a una società madre

1. Nella pagina Società aprire la pagina dei dettagli della società per la società padre selezionando l&#39;azione **[!UICONTROL Edit]**.

   ![Pagina dettagli società padre](./assets/company-update.png){width="700" zoomable="yes"}

1. Visualizzare l&#39;elenco delle società assegnate espandendo **[!UICONTROL Company Hierarchy]**.

1. Rimuovi l’azienda dall’organizzazione.

   - Nella colonna [!UICONTROL Action] per la società da rimuovere, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Rimuovere un&#39;azienda da un&#39;organizzazione](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - Quando richiesto, rimuovere la società assegnata dalla gerarchia selezionando **[!UICONTROL Unassign]**.

## Gestire le impostazioni aziendali per un&#39;organizzazione

Aggiorna la configurazione [Impostazioni avanzate](account-company-create.md#advanced-settings) per un&#39;organizzazione per applicare la configurazione padre a tutte le società figlie o per applicare le stesse impostazioni alle società selezionate nell&#39;organizzazione.

Durante il processo di aggiornamento, i valori di configurazione iniziali vengono impostati per impostazione predefinita sui valori correnti configurati per la società madre. È necessario modificare almeno un&#39;impostazione per aggiornare la configurazione per le società selezionate.

**Modifica la configurazione delle impostazioni avanzate per più società**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Dalla griglia [!UICONTROL Companies], modificare la società padre selezionando **[!UICONTROL Edit]** dalla colonna **[!UICONTROL Action]**.

1. Nella pagina dei dettagli della società padre, espandere la sezione **[!UICONTROL Company Hierarchy]** per visualizzare le società incluse nell&#39;organizzazione.

1. Seleziona le aziende da configurare.

   ![Seleziona società dalla gerarchia società](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Dal controllo **[!UICONTROL Actions]** sopra la griglia, selezionare **[!UICONTROL Change company settings]**.

   ![Modifica impostazioni società per gerarchia società](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Modifica la configurazione delle impostazioni.

   - Nella pagina [!UICONTROL Change company settings], trovare l&#39;impostazione di configurazione da modificare.

   - Selezionare la casella di controllo **[!UICONTROL Change]** per abilitare l&#39;impostazione.

   - Aggiorna il valore in base alle esigenze.

     ![Modifica le impostazioni aziendali per più società](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Dopo aver aggiornato la configurazione, selezionare **[!UICONTROL Apply Changes]**.

1. Quando richiesto, selezionare **[!UICONTROL Change settings]** per aggiornare la configurazione per le società selezionate.

>[!TIP]
>
>Gestisci la configurazione delle impostazioni avanzate per una singola azienda modificando la voce aziendale.
