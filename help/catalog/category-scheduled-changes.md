---
title: Modifiche pianificate per le categorie
description: Scopri come pianificare le modifiche di categoria per supportare campagne di marketing e promozioni su store.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 714904d6d81bde6374a5ce644262de252c70a391
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Modifiche pianificate per le categorie

{{ee-feature}}

Gli aggiornamenti per categoria possono essere applicati secondo programma e raggruppati con altre modifiche al contenuto. Puoi creare una campagna in base alle modifiche pianificate per la categoria o applicare le modifiche a una campagna esistente. Per ulteriori informazioni, consulta [Gestione temporanea dei contenuti](../content-design/content-staging.md).

Quando si pianificano modifiche per le categorie, tenere presente quanto segue:

- Tutti gli aggiornamenti pianificati vengono applicati consecutivamente, il che significa che qualsiasi entità può avere un solo aggiornamento pianificato alla volta. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere più aggiornamenti pianificati per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

- Se una campagna è collegata a più categorie, è possibile modificarla solo dal [dashboard di gestione temporanea dei contenuti](../content-design/content-staging-dashboard.md).

- Se una campagna è collegata a più categorie, è possibile modificarla solo dal [dashboard di gestione temporanea dei contenuti](../content-design/content-staging-dashboard.md).

>[!NOTE]
>
>La scheda [!UICONTROL Schedule Design Update] è stata rimossa in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e non può essere modificata direttamente nella categoria. Devi creare un aggiornamento pianificato per queste attivazioni.

## Pianificare un aggiornamento per una categoria

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie a sinistra, scegliere la categoria da modificare.

1. Nella casella _Modifiche pianificate_ nella parte superiore della pagina, fare clic su **[!UICONTROL Schedule New Update]**.

   ![Modifiche pianificate](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Con l&#39;opzione **[!UICONTROL Save as a New Update]** selezionata, impostare i parametri di base per l&#39;aggiornamento:

   - Per **[!UICONTROL Update Name]**, immettere un nome per la nuova campagna di gestione temporanea del contenuto.

   - Immetti una breve **[!UICONTROL Description]** dell&#39;aggiornamento e come deve essere utilizzato.

   - Utilizzare lo strumento Calendario ( ![icona Calendario](../assets/icon-calendar.png) ) per scegliere **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per la campagna.

   >[!IMPORTANT]
   >
   >Le campagne **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** devono essere definite utilizzando il fuso orario di amministrazione **_default_**, che viene convertito dal fuso orario locale di ciascun sito Web. Ad esempio, con più siti web in fusi orari diversi in cui desideri avviare una campagna basata su un fuso orario USA, devi pianificare un aggiornamento separato per ogni fuso orario locale. È possibile impostare **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per ciascuno di essi, che viene convertito dal fuso orario del sito Web locale al fuso orario predefinito dell&#39;amministratore.

   ![Modifiche pianificate](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Apporta le modifiche necessarie all’aggiornamento pianificato.

1. Per visualizzare l&#39;anteprima delle modifiche, fare clic su **[!UICONTROL Preview]** nella barra dei pulsanti in alto a destra.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Assegna a un aggiornamento esistente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie a sinistra, scegliere la categoria da modificare.

1. Nella casella _Modifiche pianificate_ nella parte superiore della pagina, fare clic su **[!UICONTROL Schedule New Update]**.

1. Selezionare **[!UICONTROL Assign to Existing Campaign]**.

1. Nell&#39;elenco trovare la campagna necessaria e fare clic su **[!UICONTROL Select]**.

1. Apporta le modifiche necessarie all’aggiornamento pianificato.

1. Al termine, fare clic su **[!UICONTROL Save]**.
