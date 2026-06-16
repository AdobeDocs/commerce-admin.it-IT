---
title: Prezzi speciali
description: Scopri come offrire prezzi speciali per un determinato periodo di tempo.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/j6DspCgn2P4-pHxXuOd-AiJCL0SBezxg-rn6yYmMIk8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 855
ht-degree: 0%

---

# Prezzi speciali

Un prezzo speciale può essere offerto per un determinato periodo di tempo. Durante il periodo di tempo specificato, il prezzo speciale viene visualizzato al posto del prezzo regolare, seguito da una notazione che mostra il prezzo regolare.

![Prezzo speciale su una pagina di prodotto](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Applica prezzo speciale a un singolo prodotto

Puoi facilmente impostare un prezzo speciale per un singolo prodotto nel catalogo.

### Utilizza un aggiornamento pianificato

{{ee-feature}}

Adobe Commerce include il supporto per [aggiornamenti pianificati](../content-design/content-staging-scheduled-update.md). Utilizzare questi strumenti promozionali per applicare un prezzo speciale a un prodotto specifico per un periodo di tempo specificato.

1. Apri il prodotto in modalità di modifica.

1. Fare clic su **[!UICONTROL Scheduled Update]**.

   ![Aggiungi aggiornamento pianificato per il prodotto](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. Per **Aggiorna nome**, immettere un nome per la promozione prezzo speciale.

1. Immettere un breve **[!UICONTROL Description]**.

1. Utilizza l&#39;icona _Calendario_ ( ![icona calendario](../assets/icon-calendar.png) ) per scegliere **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per la promozione prezzo speciale.

   È possibile utilizzare i cursori **[!UICONTROL Hour]** e **[!UICONTROL Minute]** per scegliere anche l&#39;ora di inizio e di fine. Fare clic su **[!UICONTROL Close]** quando sono impostati l&#39;inizio e la fine.

   ![Salva come nuovo aggiornamento](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Scorri verso il basso fino al campo _Prezzo_, fai clic su **[!UICONTROL Advanced Pricing]** e immetti l&#39;importo di **[!UICONTROL Special Price]** da applicare in base all&#39;aggiornamento pianificato.

   ![Impostazioni prezzi speciali](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Done]** e quindi su **[!DNL Save]**.

   Nella vetrina, il prezzo speciale dovrebbe essere visualizzato sia nell’elenco dei cataloghi che nella pagina del prodotto.

   _[!UICONTROL Scheduled Change]_viene visualizzato nella parte superiore della pagina.

   ![Modifica pianificata](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Utilizzare una data di inizio e una data di fine semplici

{{ce-feature}}

Magento Open Source include opzioni di data di inizio e di fine semplici nelle opzioni di Advanced Pricing.

1. Apri il prodotto in modalità di modifica.

1. Scorri verso il basso fino al campo _[!UICONTROL Price]_, fai clic su **[!UICONTROL Advanced Pricing]**e immetti l&#39;importo **[!UICONTROL Special Price]**.

1. Utilizza l&#39;icona _Calendario_ ( ![Icona Calendario](../assets/icon-calendar.png) ) per scegliere **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** per la promozione prezzo speciale.

   Il prezzo speciale entra in vigore immediatamente dopo la mezzanotte all&#39;inizio della data di inizio (00:01) e continua fino a poco prima della mezzanotte (23:59) del giorno prima della data di fine.

   ![Modifica pianificata](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Done]** e quindi su **[!UICONTROL Save]**.

   Nella vetrina, il prezzo speciale dovrebbe essere visualizzato sia nell’elenco dei cataloghi che nella pagina del prodotto.

## Applica un prezzo speciale a più prodotti

È inoltre possibile assegnare un prezzo speciale a più prodotti, ad esempio più varianti di un [prodotto configurabile](product-create-configurable.md).

### Imposta un prezzo speciale per i prodotti selezionati

{{ee-feature}}

L’esempio seguente mostra come assegnare lo stesso prezzo speciale a più varianti di prodotto di un prodotto configurabile in Adobe Commerce.

1. Nella pagina _[!UICONTROL Products]_, fare clic su **[!UICONTROL Filters]**e immettere **[!UICONTROL Name]**del prodotto configurabile.

1. Impostare **[!UICONTROL Type]** su `Configurable Product` e fare clic su **[!UICONTROL Apply Filters]**.

1. Per assegnare lo stesso prezzo speciale a tutti i prodotti, impostare il controllo nell&#39;intestazione della prima colonna su `Select All`.

   In alternativa, puoi selezionare la casella di controllo di ciascun prodotto che desideri includere.

1. Impostare il controllo **[!UICONTROL Actions]** su `Update attributes`.

1. Scorri verso il basso fino al campo _[!UICONTROL Special Price]_, seleziona la casella di controllo **[!UICONTROL Change]**sotto il campo_[!UICONTROL Special Price]_ e immetti il prezzo speciale che desideri offrire.

   ![Campi Prezzo speciale](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

Il prezzo speciale disponibile nel negozio viene visualizzato nelle inserzioni del catalogo e nella pagina del prodotto. Per un prodotto configurabile, il prezzo normale viene visualizzato anche nella pagina del prodotto quando si scelgono le opzioni.

### Imposta un prezzo speciale e un intervallo di date per i prodotti selezionati

{{ce-feature}}

L’esempio seguente mostra come assegnare lo stesso prezzo speciale a più varianti di prodotto di un prodotto configurabile in Magento Open Source.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Fare clic su **[!UICONTROL Filters]**.

1. Immettere **[!UICONTROL Name]** del prodotto configurabile.

1. Imposta **[!UICONTROL Type]** su `Simple Product`.

   ![Filtri](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Apply Filters]**.

   La griglia elenca tutti i prodotti semplici associati come varianti del prodotto configurabile.

1. Per assegnare lo stesso prezzo speciale a tutti i prodotti, impostare il controllo nell&#39;intestazione della prima colonna su `Select All`.

   In alternativa, puoi selezionare la casella di controllo di ciascun prodotto che desideri includere.

1. Impostare il controllo **[!UICONTROL Actions]** su `Update attributes`.

   ![Aggiorna attributi](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Scorri verso il basso fino al campo _[!UICONTROL Special Price]** ed effettua le seguenti operazioni:

   - Selezionare la casella di controllo **[!UICONTROL Change]** sotto il campo _[!UICONTROL Special Price]** e immettere il prezzo speciale che si desidera offrire.

   - Selezionare la casella di controllo **[!UICONTROL Change]** sotto il campo _Prezzo speciale da data_, fare clic sul _Calendario_ (![Icona Calendario](../assets/icon-calendar.png) ) e scegliere la prima data della promozione prezzo speciale.

     Il prezzo speciale entra in vigore immediatamente dopo la mezzanotte all&#39;inizio della data di inizio (00:01) e continua fino a poco prima della mezzanotte (23:59) del giorno prima della data di fine.

   - Selezionare la casella di controllo **[!UICONTROL Change]** sotto il campo _Prezzo speciale fino alla data_, fare clic sul _Calendario_ (![Icona Calendario](../assets/icon-calendar.png) ) e scegliere l&#39;ultima data della promozione prezzo speciale.

   ![Campi prezzo speciale](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

   Un messaggio indica quanti record sono stati aggiornati con il prezzo speciale.

   Il prezzo speciale diventa disponibile nel negozio alla data specificata e viene visualizzato nelle inserzioni del catalogo e nella pagina del prodotto. Per un prodotto configurabile, il prezzo normale viene visualizzato anche nella pagina del prodotto quando si scelgono le opzioni.

   ![Prezzo speciale per il prodotto configurabile](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Test

Se il prezzo speciale non viene visualizzato correttamente nella vetrina sia nella pagina di elenco che in quella dei prodotti, cancella la cache del browser:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Fare clic su **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>Il prezzo del prodotto **_final_** è calcolato come prezzo rilevante **_minimum_**, utilizzando la seguente formula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Le opzioni personalizzabili del prodotto_** a prezzo fisso sono _non_ influenzate dalle regole di prezzo di gruppo, prezzo di livello, prezzo speciale o prezzo di catalogo.
