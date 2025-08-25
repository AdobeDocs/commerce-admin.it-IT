---
title: Gestire le gerarchie aziendali
description: Creare e gestire gerarchie aziendali per supportare le organizzazioni B2B con modelli operativi complessi.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Gestire le gerarchie aziendali

La funzionalità [!UICONTROL Company Hierarchy] consente di organizzare più società correlate in un&#39;unica struttura di società padre. Questa soluzione è ideale per le aziende con filiali, franchising, sedi multiple o strutture organizzative complesse che richiedono una gestione centralizzata mantenendo al contempo le identità delle singole aziende.

## Casi d’uso

* **Gestione centralizzata**: applicazione di impostazioni e configurazioni a più società da un&#39;unica società madre
* **Gestisci struttura**: organizza le aziende in una gerarchia logica che rifletta l&#39;organizzazione aziendale
* **Operazioni semplificate**: gestione di preventivi, ordini di acquisto, metodi di pagamento e impostazioni di spedizione per l&#39;intera organizzazione
* **Mantenere l&#39;autonomia**: le singole aziende mantengono la propria identità beneficiando delle configurazioni condivise

## Prerequisiti

Prima di creare una gerarchia aziendale, assicurati che:

* Le funzioni B2B sono abilitate nell’installazione di Commerce
* Accesso amministratore per gestire le società
* Le società madri e figlie sono già state create come singole società
* L&#39;applicazione delle impostazioni padre sovrascriverà le configurazioni aziendali figlio esistenti

## Come funziona

Gli amministratori possono creare una gerarchia di società assegnando società correlate a una società padre designata, che è la società al vertice della gerarchia organizzativa.

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

   * Per assegnare altre società a una società padre esistente, selezionare l&#39;azione **[!UICONTROL Edit]** per la società padre.
   * Per creare una società padre, selezionare l&#39;azione **[!UICONTROL Edit]** per la società designata come padre.

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

   * Nella colonna [!UICONTROL Action] per la società da rimuovere, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Rimuovere un&#39;azienda da un&#39;organizzazione](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * Quando richiesto, rimuovere la società assegnata dalla gerarchia selezionando **[!UICONTROL Unassign]**.

## Gestire le impostazioni aziendali per un&#39;organizzazione

Aggiorna la configurazione [Impostazioni avanzate](account-company-create.md#advanced-settings) per un&#39;organizzazione. È possibile:

* Applica le impostazioni di configurazione padre a tutte le società figlie
* Applica le stesse impostazioni alle società selezionate nell’organizzazione

È possibile applicare una delle seguenti impostazioni:

* **Gestione preventivi**—Consente o meno alle aziende di richiedere e gestire preventivi
* **Ordini di acquisto**—Controlla se le aziende possono creare e gestire gli ordini di acquisto
* **Configurazione metodo di pagamento**—Definire i metodi di pagamento disponibili per le società
* **Impostazioni metodo di pagamento**—Configura parametri e limiti specifici del metodo di pagamento
* **Disponibilità metodo di spedizione**—Impostare i metodi di spedizione utilizzabili dalle società
* **Configurazione metodo di spedizione**—Definire le impostazioni e le restrizioni del metodo di spedizione

Durante il processo di aggiornamento, i valori di configurazione iniziali vengono impostati per impostazione predefinita sui valori correnti configurati per la società madre. È necessario selezionare la casella di controllo Modifica per almeno un&#39;impostazione per applicare le impostazioni alle società selezionate. Puoi anche aggiornare il valore predefinito per ogni impostazione prima di applicare le modifiche.

>[!WARNING]
>
>L&#39;applicazione delle impostazioni della società padre sostituisce le configurazioni esistenti della società figlio, inclusi i limiti di credito, i metodi di pagamento, le impostazioni di spedizione e le restrizioni personalizzate. Dopo aver applicato le impostazioni, puoi comunque gestire e personalizzare le impostazioni avanzate per le singole società principali e secondarie modificando l’elemento riga della società.

### Best practice

Quando applichi le impostazioni della società madre alle società figlie, prendi in considerazione le seguenti best practice:

* Rivedi le impostazioni aziendali figlio esistenti prima di applicare le configurazioni padre
* Verifica prima le modifiche alle impostazioni per una singola società figlia
* Comunicare le modifiche agli amministratori della società che potrebbero essere interessati

### Applicare le impostazioni di configurazione padre alle società figlie

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Dalla griglia [!UICONTROL Companies], modificare la società padre selezionando **[!UICONTROL Edit]** dalla colonna **[!UICONTROL Action]**.

1. Nella pagina dei dettagli della società padre, espandere la sezione **[!UICONTROL Company Hierarchy]** per visualizzare le società incluse nell&#39;organizzazione.

1. Seleziona le aziende da configurare.

   ![Seleziona società dalla gerarchia società](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Dal controllo **[!UICONTROL Actions]** sopra la griglia, selezionare **[!UICONTROL Change company settings]**.

   ![Modifica impostazioni società per gerarchia società](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Modifica la configurazione delle impostazioni.

   * Nella pagina [!UICONTROL Change company settings], trovare l&#39;impostazione di configurazione da modificare.

   * Selezionare la casella di controllo **[!UICONTROL Change]** per abilitare l&#39;impostazione.

   * Se necessario, aggiorna il valore.

     ![Modifica le impostazioni aziendali per più società](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Dopo aver aggiornato la configurazione, selezionare **[!UICONTROL Apply Changes]**.

1. Quando richiesto, selezionare **[!UICONTROL Change settings]** per aggiornare la configurazione per le società selezionate.

>[!MORELIKETHIS]
>
>* [Crea un account società](account-company-create.md) - Scopri come creare singole società prima di creare gerarchie
>* [Ruoli e autorizzazioni aziendali](account-company-roles-permissions.md) - Comprendere l&#39;accesso degli utenti nelle strutture aziendali
>* [Gestione del credito aziendale](credit-company.md) - Configura i limiti di credito e le condizioni di pagamento per le società
>* [Gestione società](manage-companies.md) - Panoramica delle funzionalità di gestione società
>* [Abilita funzionalità B2B](enable-basic-features.md) - Abilita e configura funzionalità B2B
