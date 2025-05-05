---
title: Aggiornamenti pianificati dei prodotti
description: Scopri come pianificare le modifiche agli elenchi dei prodotti per supportare campagne e programmi promozionali.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 2cdf3452f1648dc1ed607d6dfb5ade4be5ed5ce9
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Pianificare gli aggiornamenti dei prodotti

{{ee-feature}}

Gli aggiornamenti dei prodotti possono essere applicati secondo pianificazione e raggruppati con altre modifiche al contenuto. Puoi utilizzare [staging contenuto](../content-design/content-staging.md) per creare una campagna basata su modifiche pianificate al prodotto o applicare le modifiche a una campagna esistente.

Quando configuri le pianificazioni per gli aggiornamenti dei prodotti e le campagne di modifica, tieni presente quanto segue:

- Tutti gli aggiornamenti pianificati vengono applicati consecutivamente, il che significa che qualsiasi entità può avere un solo aggiornamento pianificato alla volta. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere diversi aggiornamenti pianificati per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

- Un&#39;anteprima di gestione temporanea per un aggiornamento pianificato inizia sempre dalla visualizzazione **predefinita** dell&#39;archivio, che emula l&#39;esperienza del cliente di navigare attraverso la campagna di aggiornamento di gestione temporanea.

- Se una campagna è collegata a più di un prodotto, è possibile modificarla solo dal [dashboard di gestione temporanea dei contenuti](../content-design/content-staging-dashboard.md).

- Se inizialmente viene creata una campagna attiva senza una data di fine, non è possibile modificarla in un secondo momento in modo da includere una data di fine. In tal caso, è necessario creare una campagna duplicata e immettere la data di fine necessaria.


>[!NOTE]
>
>I campi [!UICONTROL Set Product as New From] e [!UICONTROL To] e la scheda [!UICONTROL Schedule Design Update] sono stati rimossi da ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e non possono essere modificati direttamente sul prodotto. Devi creare un aggiornamento pianificato per queste attivazioni.

## Crea un aggiornamento pianificato

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selezionare un prodotto esistente e fare clic su **[!UICONTROL Edit]**.

1. Fare clic su **[!UICONTROL Schedule New Update]**.

1. Selezionare **[!UICONTROL Save as a New Update]**.

1. Per **[!UICONTROL Update Name]**, immettere un nome per la nuova campagna di gestione temporanea del contenuto.

1. Immetti una breve **[!UICONTROL Description]** dell&#39;aggiornamento e come deve essere utilizzato.

1. Utilizzare lo strumento Calendario (![icona calendario](../assets/icon-calendar.png)) per scegliere **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per la campagna.

   >[!NOTE]
   >
   >Le campagne **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** devono essere definite utilizzando il fuso orario di amministrazione **_default_**, che viene convertito dal fuso orario locale per ogni sito Web. Ad esempio, con più siti web in fusi orari diversi in cui desideri avviare una campagna basata su un fuso orario USA, devi pianificare un aggiornamento separato per ogni fuso orario locale. Impostare **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per ciascuno di essi e verranno convertiti dal fuso orario del sito Web locale al fuso orario predefinito dell&#39;amministratore.

   ![Pianifica come nuovo aggiornamento](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Scorri verso il basso fino a _[!UICONTROL Price]_&#x200B;e fai clic su **[!UICONTROL Advanced Pricing]**.

1. Immettere **[!UICONTROL Special Price]** per il prodotto durante la campagna pianificata e fare clic su **[!UICONTROL Done]**.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Assegna ad aggiornamento esistente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Selezionare un prodotto esistente e fare clic su **[!UICONTROL Edit]**.

1. Fare clic su **[!UICONTROL Schedule New Update]**.

1. Selezionare **[!UICONTROL Assign to Existing Campaign]**.

1. Nell’elenco, seleziona la campagna da modificare.

   ![Assegnazione a una campagna esistente](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Visualizza la modifica pianificata

La modifica pianificata viene visualizzata nella parte superiore della pagina del prodotto, con le date di inizio e di fine della campagna.

![Modifica pianificata](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## Modifica la modifica pianificata

1. Nella casella _[!UICONTROL Scheduled Changes]_&#x200B;nella parte superiore della pagina, fare clic su **[!UICONTROL View/Edit]**.

1. Apporta le modifiche necessarie all’aggiornamento pianificato.

1. Fare clic su **[!UICONTROL Save]**.

## Rimuovi la modifica pianificata

1. Nella casella _[!UICONTROL Scheduled Changes]_&#x200B;nella parte superiore della pagina, fare clic su **[!UICONTROL View/Edit]**.

1. Nella barra superiore fare clic su **[!UICONTROL Remove from Update]**.

   ![Rimuovi modifica pianificata](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. Nella finestra di dialogo, seleziona **[!UICONTROL Delete the Update]** e fai clic su **[!UICONTROL Done]**.

   Il prodotto viene rimosso dall’aggiornamento e tutte le modifiche pianificate vengono perse.

## Pianificare un aggiornamento della progettazione

{{ce-feature}}

La sezione _[!UICONTROL Schedule Design Update]_&#x200B;consente di apportare modifiche temporanee all&#39;aspetto della pagina del prodotto. È possibile pianificare le modifiche di progettazione per una stagione, una promozione o semplicemente per rinnovare la struttura. Le modifiche della progettazione possono essere pianificate in anticipo, quindi diventano effettive, o_ drip _, nella pianificazione definita.

![Aggiornamento Progettazione Pianificato](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina l’intervallo di date in cui viene applicato un layout personalizzato al prodotto. |
| [!UICONTROL New Theme] | Applica un tema personalizzato al prodotto. |
| [!UICONTROL New Layout] | Applica un layout diverso alla pagina di prodotto. Opzioni: <br/>**[!UICONTROL No layout updates]**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per la pagina prodotto.<br/>**[!UICONTROL Empty]** - Consente di definire un layout personalizzato, ad esempio una pagina a 4 colonne. (richiede una comprensione di XML). <br/>**[!UICONTROL 1 column]**- Applica un layout a una colonna alla pagina del prodotto.<br/>**[!UICONTROL 2 columns with left bar]** - Applica un layout a due colonne con barra laterale a sinistra alla pagina del prodotto. <br/>**[!UICONTROL 2 columns with right bar]**- Applica un layout a due colonne con barra laterale a destra alla pagina del prodotto.<br/>**[!UICONTROL 3 columns]** - Applica un layout a tre colonne alla pagina del prodotto. |

{style="table-layout:auto"}
