---
title: Aggiungi un'attività di magazzino
description: Scopri come aggiungere scorte e mappare le origini ai canali di vendita (siti web), fornendo un collegamento diretto alle quantità vendibili e agli inventari dei prodotti.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Aggiungi un titolo

Le scorte associano le fonti ai canali di vendita (o ai siti Web), fornendo un collegamento diretto alle quantità vendibili e agli inventari dei prodotti.

Quando crei un magazzino personalizzato, assegni siti web e sorgenti. Le origini possono includere origini abilitate e disabilitate. Ad esempio, è possibile aggiungere una warehouse alle scorte, preparando l&#39;apertura dell&#39;ubicazione per la gestione delle scorte e il completamento delle spedizioni.

Dopo aver aggiunto le origini, devi assegnare la priorità all’ordine delle origini, dall’alto (primo) al basso (ultimo). Questo ordine influisce sui consigli durante la spedizione dell&#39;ordine.

![Nuovo Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Aggiungere le scorte di magazzino

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Fare clic su **[!UICONTROL Add New Stock]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General]** e immettere un **[!UICONTROL Name]** univoco per identificare il nuovo titolo.

   ![Opzioni generali sulle azioni](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sales Channels]** e selezionare **[!UICONTROL Websites]** in cui è disponibile questa azione.

   Per eseguire un&#39;installazione multisito, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascun sito Web.

   >[!NOTE]
   >
   >Se si seleziona un sito Web o un canale di vendita assegnato a un altro titolo, l&#39;assegnazione verrà annullata. Tutti i Sales Channel non assegnati a un magazzino personalizzato vengono assegnati al magazzino predefinito.

   Opzioni ![Sales Channel per le scorte](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sources]** ed eseguire le operazioni seguenti per qualsiasi azione diversa da quella predefinita:

   - Fare clic su **[!UICONTROL Assign Sources]**.

   ![Origini assegnate](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Selezionare le caselle di controllo per tutte le origini che si desidera assegnare al materiale.

   >[!IMPORTANT]
   >
   >Se si assegna la stessa origine a più scorte, si potrebbero verificare vendite in eccesso dei prodotti assegnati a tale origine.

   - Fare clic su **[!UICONTROL Done]**.

     Le origini aggiunte vengono visualizzate in Origini assegnate.

     ![Assegna origini al magazzino](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Utilizza ![Icona ordinamento](assets/icon-sort.png) per trascinare e rilasciare le origini in una priorità dall&#39;alto (primo) al basso (ultimo).

   L&#39;ordine di origine è importante per gli ordini di spedizione.

   ![Esempio di origini assegnate](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Scegliere **[!UICONTROL Save & Close]** dal menu _[!UICONTROL Save]_(![freccia menu](../assets/icon-menu-down-arrow-red.png)).

## Descrizioni dei campi

| Campo | Descrizione |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nome del titolo. Esempio: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Definisce l&#39;[ambito](../getting-started/websites-stores-views.md#scope-settings) del titolo assegnando il titolo a siti Web specifici come _canali di vendita_. Selezionare uno o più siti Web per azione. Ogni sito web può essere assegnato a un solo stock. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Assegna le origini magazzino a questo magazzino. Le origini personalizzate non possono essere assegnate al magazzino predefinito. |
| [!UICONTROL Assigned Sources] | Elenco delle origini assegnate. Trascina e rilascia le origini utilizzando ![Icona di ordinamento](assets/icon-sort.png) in un ordine prioritario per l&#39;evasione e la spedizione degli ordini.<br/><br/>**[!UICONTROL Code]**- ID di codice univoco per l&#39;origine.<br/>**[!UICONTROL Name]** - Descrizione del nome per l&#39;origine.<br/>**[!UICONTROL Unassign]**- Rimuovi l&#39;origine assegnata dal titolo utilizzando ![Icona cestino](../assets/icon-delete-trashcan-solid.png). |
