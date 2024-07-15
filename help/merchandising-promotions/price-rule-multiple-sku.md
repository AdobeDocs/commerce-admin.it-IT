---
title: Regola prezzo catalogo con più SKU
description: Scopri come applicare una singola regola del prezzo di catalogo a più SKU.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Regola prezzo catalogo con più SKU

Una singola regola di prezzo di catalogo può essere applicata a più SKU, consentendo di creare varie promozioni in base a un prodotto, un marchio o una categoria. Quando crei questa regola, vuoi impostare condizioni che corrispondano agli SKU selezionati. Durante la creazione della regola, puoi sfogliare e selezionare facilmente gli SKU dalla griglia.

## Passaggio 1: Verificare le proprietà della vetrina dell’attributo del prodotto

Prima di iniziare, verificare che le [proprietà storefront](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) dell&#39;attributo `sku` siano impostate su `Use in Promo Rules`.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Nel filtro di ricerca nella parte superiore della colonna _[!UICONTROL Attribute Code]_, immettere `sku` e fare clic su **[!UICONTROL Search]**.

1. Fare clic per aprire l&#39;attributo `sku` in modalità di modifica.

1. Nel pannello a sinistra, fai clic su **[!UICONTROL Storefront Properties]** e assicurati che **[!UICONTROL Use for Promo Rule Conditions]** sia impostato su `Yes`.

1. Se si è modificato il valore della proprietà, fare clic su **[!UICONTROL Save Attribute]**.

## Passaggio 2: Applicare una regola di prezzo a più SKU

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. Effettuare una delle seguenti operazioni:

   - Segui le istruzioni per creare una [regola prezzo catalogo](price-rules-catalog.md).
   - Apri una regola del prezzo di catalogo esistente.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Conditions]** ed eseguire le operazioni seguenti:

   - Nella prima riga, impostare il primo parametro su `ANY`.

     ![Condizione regola prezzo catalogo - ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - Fare clic su _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) all&#39;inizio della riga successiva e nell&#39;elenco in **[!UICONTROL Product Attribute]** fare clic su `SKU`.

     ![Condizione regola prezzo catalogo - SKU è uno di](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - Per il confronto, sono disponibili diverse opzioni. Se si desidera individuarne almeno uno da un elenco di SKU, `select is one of`. Per individuare un gruppo di SKU che devono essere tutti applicati, selezionare `is`. È consigliabile selezionare `is one of`.

     ![Condizione regola prezzo catalogo - SKU è uno di](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - Per completare la condizione, fare clic sul collegamento altro (**...**) e fare clic sull&#39;icona _Selettore_ (![Icona elenco](../assets/icon-list-chooser.png)) per l&#39;elenco dei prodotti disponibili.

     ![Condizione regola prezzo catalogo - più SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - Sfoglia, filtra o cerca gli SKU da aggiungere. Nell’elenco, seleziona la casella di controllo di ciascun prodotto da includere.

   - Fare clic su **[!UICONTROL Save and Apply]** per aggiungere gli SKU alla condizione.

     ![Condizione regola prezzo catalogo - più SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Completa la regola, incluse [azioni](price-rules-catalog.md) da eseguire quando vengono soddisfatte le condizioni.

1. Al termine della regola, fare clic su **[!UICONTROL Save]**.

{{new-price-rule}}
