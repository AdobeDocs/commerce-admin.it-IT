---
title: Esempio di regola prezzo carrello - promozione spedizione gratuita
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire la spedizione gratuita.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# Esempio di regola prezzo carrello - promozione spedizione gratuita

La spedizione gratuita può essere offerta come promozione, con o senza un [coupon](price-rules-cart-coupon.md). È inoltre possibile applicare un buono di spedizione gratuito agli ordini di ritiro del cliente, in modo che l&#39;ordine possa essere fatturato e spedito per completare il [flusso di lavoro](../stores-purchase/order-processing.md#order-workflow-and-processing).

Alcune configurazioni del vettore di spedizione ti consentono di offrire la spedizione gratuita in base a un ordine minimo. Per espandere questa funzionalità di base, puoi utilizzare le regole di prezzo del carrello per creare condizioni complesse in base a più attributi di prodotto, contenuti del carrello e gruppi di clienti.

## Passaggio 1: Abilita spedizione gratuita

1. Abilita [spedizione gratuita](../stores-purchase/shipping-free.md) nella configurazione dell&#39;archivio.

1. Completa le impostazioni di spedizione gratuita per qualsiasi [servizio vettore](../stores-purchase/carriers.md) che desideri utilizzare per la spedizione gratuita.

## Passaggio 2: Creare una regola di prezzo del carrello

Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Segui i passaggi seguenti per impostare il tipo di promozione di spedizione gratuita che desideri offrire.

### Esempio 1: spedizione gratuita per qualsiasi ordine

1. Completa **[!UICONTROL Rule Information]** come segue:

   - Immettere **[!UICONTROL Rule Name]** come riferimento interno.
   - Immettere un breve **[!UICONTROL Description]** per descrivere la regola.
   - Imposta **[!UICONTROL Active]** su `Yes`.
   - Nella casella **[!UICONTROL Websites]** selezionare ogni sito in cui sarà disponibile il buono di spedizione gratuito.
   - Selezionare **[!UICONTROL Customer Groups]** a cui si applica la regola.
   - Imposta **[!UICONTROL Coupon]** su uno dei seguenti:
      - Per offrire una promozione di spedizione gratuita senza un coupon, accettare l&#39;impostazione predefinita (`No Coupon`).
      - Per utilizzare un coupon con la regola del prezzo, selezionare `Specific Coupon`. Se necessario, completare le istruzioni per impostare un [coupon](price-rules-cart-coupon.md).

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Actions]** ed effettua le seguenti operazioni:

   - Imposta **[!UICONTROL Apply]** su `Percent of product price discount`.
   - Imposta **[!UICONTROL Apply to Shipping Amount]** su `Yes`.
   - Imposta **[!UICONTROL Free Shipping]** su `For matching items only`.

   ![Regola prezzo carrello - azioni spedizione gratuita](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Esempio 2: spedizione gratuita per ordini superiori a $

1. Completare le impostazioni di **[!UICONTROL General Information]** come descritto nell&#39;esempio precedente.

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Conditions]**.

1. Fai clic su _Aggiungi_ (![Aggiungi icona](../assets/icon-add-green-circle.png)) per inserire una condizione ed effettuare le seguenti operazioni:

   - Nell&#39;elenco in **[!UICONTROL Cart Attribute]**, scegliere `Subtotal`.
   - Fare clic su **[!UICONTROL is]** e scegliere `equals or greater than`.
   - Fare clic su **...** e immettere un valore di soglia per il subtotale, ad esempio `100`, per completare la condizione.

   ![Regola prezzo carrello - condizione](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Se necessario, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Actions]** ed eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Apply]** su `Percent of product price discount`.
   - Imposta **[!UICONTROL Apply to Shipping Amount]** su `Yes`.
   - Imposta **[!UICONTROL Free Shipping]** su `For matching items only`.

## Passaggio 3: Completa le etichette

Completa il [passaggio 4](price-rules-cart.md) delle istruzioni della regola prezzo carrello per inserire le etichette visualizzate durante l&#39;estrazione.

## Passaggio 4: Salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fare clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.
