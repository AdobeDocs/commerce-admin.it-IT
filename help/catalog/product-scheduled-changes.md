---
title: Aggiornamenti pianificati dei prodotti
description: Scopri come pianificare le modifiche agli elenchi dei prodotti per supportare campagne e programmi promozionali.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 1e809696ee6d623d162226628329ed53e8f71511
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Pianificare gli aggiornamenti dei prodotti

{{ee-feature}}

Gli aggiornamenti dei prodotti possono essere applicati secondo pianificazione e raggruppati con altre modifiche al contenuto. È possibile utilizzare [staging dei contenuti](../content-design/content-staging.md) per creare una campagna in base alle modifiche pianificate al prodotto o applicarle a una campagna esistente.

>[!NOTE]
>
>Tutti gli aggiornamenti pianificati vengono applicati consecutivamente, il che significa che qualsiasi entità può avere un solo aggiornamento pianificato alla volta. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere diversi aggiornamenti pianificati per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

>[!NOTE]
>
>Un’anteprima di staging per un aggiornamento pianificato inizia sempre dal **predefinito** la vista store, che emula l’esperienza del cliente durante la navigazione nella campagna di aggiornamento dell’area di gestione temporanea.

## Crea un aggiornamento pianificato

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleziona un prodotto esistente e fai clic su **[!UICONTROL Edit]**.

1. Clic **[!UICONTROL Schedule New Update]**.

1. Seleziona **[!UICONTROL Save as a New Update]**.

1. Per **[!UICONTROL Update Name]**, immetti un nome per la nuova campagna di staging dei contenuti.

1. Inserisci una descrizione **[!UICONTROL Description]** dell’aggiornamento e come deve essere utilizzato.

1. Utilizza il calendario (![icona calendario](../assets/icon-calendar.png)) per scegliere il **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per la campagna.

   >[!NOTE]
   >
   >Campagna **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** deve essere definito utilizzando **_predefinito_** Fuso orario amministratore, convertito dal fuso orario locale per ogni sito Web. Ad esempio, con più siti web in fusi orari diversi in cui desideri avviare una campagna basata su un fuso orario USA, devi pianificare un aggiornamento separato per ogni fuso orario locale. Imposta **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per ogni e viene convertito dal fuso orario del sito web locale al fuso orario predefinito dell’amministratore.

   ![Pianifica come nuovo aggiornamento](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Scorri verso il basso fino a _[!UICONTROL Price]_e fai clic su **[!UICONTROL Advanced Pricing]**.

1. Immetti un **[!UICONTROL Special Price]** per il prodotto durante la campagna pianificata e fai clic su **[!UICONTROL Done]**.

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Assegna ad aggiornamento esistente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleziona un prodotto esistente e fai clic su **[!UICONTROL Edit]**.

1. Clic **[!UICONTROL Schedule New Update]**.

1. Seleziona **[!UICONTROL Assign to Existing Campaign]**.

1. Nell’elenco, seleziona la campagna da modificare.

   ![Assegnazione a una campagna esistente](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Visualizza la modifica pianificata

La modifica pianificata viene visualizzata nella parte superiore della pagina del prodotto, con le date di inizio e di fine della campagna.

![Modifica pianificata](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## Modifica la modifica pianificata

1. In _[!UICONTROL Scheduled Changes]_nella parte superiore della pagina, fai clic su **[!UICONTROL View/Edit]**.

1. Apporta le modifiche necessarie all’aggiornamento pianificato.

1. Clic **[!UICONTROL Save]**.

## Rimuovi la modifica pianificata

1. In _[!UICONTROL Scheduled Changes]_nella parte superiore della pagina, fai clic su **[!UICONTROL View/Edit]**.

1. Nella barra superiore, fai clic su **[!UICONTROL Remove from Update]**.

   ![Rimuovi modifica pianificata](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. Nella finestra di dialogo, seleziona **[!UICONTROL Delete the Update]** e fai clic su **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >Il prodotto viene rimosso dall’aggiornamento e tutte le modifiche pianificate vengono perse.

## Pianificare un aggiornamento della progettazione

{{ce-feature}}

Il _[!UICONTROL Schedule Design Update]_consente di apportare modifiche temporanee all&#39;aspetto della pagina di prodotto. È possibile pianificare le modifiche di progettazione per una stagione, una promozione o semplicemente per rinnovare la struttura. Le modifiche di progettazione possono essere pianificate in anticipo, quindi diventano effettive, oppure_ gocciolamento _, nella pianificazione definita.

![Design Update Programmato](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina l’intervallo di date in cui viene applicato un layout personalizzato al prodotto. |
| [!UICONTROL New Theme] | Applica un tema personalizzato al prodotto. |
| [!UICONTROL New Layout] | Applica un layout diverso alla pagina di prodotto. Opzioni: <br/>**[!UICONTROL No layout updates]**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per la pagina prodotto.<br/>**[!UICONTROL Empty]** - Consente di definire un layout personalizzato, ad esempio una pagina a 4 colonne. (richiede una comprensione di XML). <br/>**[!UICONTROL 1 column]**- Applica un layout a una colonna alla pagina del prodotto.<br/>**[!UICONTROL 2 columns with left bar]** - Applica un layout a due colonne con barra laterale a sinistra alla pagina del prodotto. <br/>**[!UICONTROL 2 columns with right bar]**- Applica un layout a due colonne con barra laterale a destra alla pagina del prodotto.<br/>**[!UICONTROL 3 columns]** - Applica un layout a tre colonne alla pagina del prodotto. |

{style="table-layout:auto"}
