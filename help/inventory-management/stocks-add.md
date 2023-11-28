---
title: Aggiungi un'attività di magazzino
description: Scopri come aggiungere scorte e mappare le origini ai canali di vendita (siti web), fornendo un collegamento diretto alle quantità vendibili e agli inventari dei prodotti.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# Aggiungi un titolo

Le scorte associano le fonti ai canali di vendita (o ai siti Web), fornendo un collegamento diretto alle quantità vendibili e agli inventari dei prodotti.

Quando crei un magazzino personalizzato, assegni siti web e sorgenti. Le origini possono includere origini abilitate e disabilitate. Ad esempio, è possibile aggiungere una warehouse alle scorte, preparando l&#39;apertura dell&#39;ubicazione per la gestione delle scorte e il completamento delle spedizioni.

Dopo aver aggiunto le origini, devi assegnare la priorità all’ordine delle origini, dall’alto (primo) al basso (ultimo). Questo ordine influisce sui consigli durante la spedizione dell&#39;ordine.

![Nuovo Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Aggiungere le scorte di magazzino

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Clic **[!UICONTROL Add New Stock]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General]** e immettere un valore univoco **[!UICONTROL Name]** per identificare il nuovo stock.

   ![Opzioni generali sulle azioni](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Sales Channels]** e seleziona la **[!UICONTROL Websites]** dove questa scorta è disponibile.

   Per eseguire un&#39;installazione multisito, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascun sito Web.

   >[!NOTE]
   >
   >Se si seleziona un sito Web o un canale di vendita assegnato a un altro titolo, l&#39;assegnazione verrà annullata. Tutti i Sales Channel non assegnati a un magazzino personalizzato vengono assegnati al magazzino predefinito.

   ![Opzioni Sales Channel per le scorte](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Sources]** ed effettuate le seguenti operazioni per qualsiasi materiale diverso da quello di default:

   - Clic **[!UICONTROL Assign Sources]**.

   ![Origini assegnate](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Selezionare le caselle di controllo per tutte le origini che si desidera assegnare al materiale.

   >[!IMPORTANT]
   >
   >Se si assegna la stessa origine a più scorte, si potrebbero verificare vendite in eccesso dei prodotti assegnati a tale origine.

   - Clic **[!UICONTROL Done]**.

     Le origini aggiunte vengono visualizzate in Origini assegnate.

     ![Assegna origini al magazzino](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Utilizzare ![Icona Ordina](assets/icon-sort.png) per trascinare e rilasciare le origini in una priorità dall&#39;alto (primo) al basso (ultimo).

   L&#39;ordine di origine è importante per gli ordini di spedizione.

   ![Esempio di origini assegnate](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Il giorno _[!UICONTROL Save]_(![Freccia del menu](../assets/icon-menu-down-arrow-red.png)), scegliere **[!UICONTROL Save & Close]**.

## Descrizioni dei campi

| Campo | Descrizione |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nome del titolo. Ad esempio: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Definisce il [ambito](../getting-started/websites-stores-views.md#scope-settings) del titolo assegnando il titolo a siti web specifici come _canali di vendita_. Selezionare uno o più siti Web per azione. Ogni sito web può essere assegnato a un solo stock. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Assegna le origini magazzino a questo magazzino. Le origini personalizzate non possono essere assegnate al magazzino predefinito. |
| [!UICONTROL Assigned Sources] | Elenco delle origini assegnate. Trascina e rilascia le sorgenti utilizzando ![Icona Ordina](assets/icon-sort.png) in un ordine prioritario per l&#39;evasione e la spedizione degli ordini.<br/><br/>**[!UICONTROL Code]**- ID di codice univoco per la sorgente.<br/>**[!UICONTROL Name]** - Nome e descrizione dell&#39;origine.<br/>**[!UICONTROL Unassign]**- Rimuove l&#39;origine assegnata dal materiale mediante ![Icona Elimina](../assets/icon-delete-trashcan-solid.png). |
