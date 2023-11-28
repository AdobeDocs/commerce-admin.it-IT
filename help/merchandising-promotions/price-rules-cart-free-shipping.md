---
title: Esempio di regola prezzo carrello - promozione spedizione gratuita
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire la spedizione gratuita.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Esempio di regola prezzo carrello - promozione spedizione gratuita

La spedizione gratuita può essere offerta come promozione, con o senza [coupon](price-rules-cart-coupon.md). È inoltre possibile applicare un buono di spedizione gratuito agli ordini di ritiro del cliente, in modo che l&#39;ordine possa essere fatturato e spedito per completare il [workflow](../stores-purchase/order-processing.md#order-workflow-and-processing).

Alcune configurazioni del vettore di spedizione ti consentono di offrire la spedizione gratuita in base a un ordine minimo. Per espandere questa funzionalità di base, puoi utilizzare le regole di prezzo del carrello per creare condizioni complesse in base a più attributi di prodotto, contenuti del carrello e gruppi di clienti.

## Passaggio 1: Abilita spedizione gratuita

1. Abilita [spedizione gratuita](../stores-purchase/shipping-free.md) nella configurazione dell’archivio.

1. Completa le impostazioni di spedizione gratuita per qualsiasi [servizio vettore](../stores-purchase/carriers.md) che si desidera utilizzare per la spedizione gratuita.

## Passaggio 2: Creare una regola di prezzo del carrello

Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Segui i passaggi seguenti per impostare il tipo di promozione di spedizione gratuita che desideri offrire.

### Esempio 1: spedizione gratuita per qualsiasi ordine

1. Completa il **[!UICONTROL Rule Information]** come segue:

   - Immetti un **[!UICONTROL Rule Name]** per riferimento interno.
   - Inserisci una descrizione **[!UICONTROL Description]** per descrivere la regola.
   - Imposta **[!UICONTROL Active]** a `Yes`.
   - In **[!UICONTROL Websites]** selezionare ogni sito in cui sarà disponibile il buono di spedizione gratuito.
   - Seleziona la **[!UICONTROL Customer Groups]** a cui si applica la regola.
   - Imposta **[!UICONTROL Coupon]** a uno dei seguenti elementi:
      - Per offrire una promozione di spedizione gratuita senza un coupon, accettare l&#39;impostazione predefinita (`No Coupon`).
      - Per utilizzare un coupon con la regola del prezzo, selezionare `Specific Coupon`. Se necessario, completare le istruzioni per impostare un [coupon](price-rules-cart-coupon.md).

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Actions]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Apply]** a `Percent of product price discount`.
   - Imposta **[!UICONTROL Apply to Shipping Amount]** a `Yes`.
   - Imposta **[!UICONTROL Free Shipping]** a `For matching items only`.

   ![Regola prezzo carrello - azioni di spedizione gratuite](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Esempio 2: spedizione gratuita per ordini superiori a $

1. Completa il **[!UICONTROL General Information]** come descritto nell&#39;esempio precedente.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Conditions]** sezione.

1. Clic _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) per inserire una condizione ed effettuare le seguenti operazioni:

   - Nell’elenco in **[!UICONTROL Cart Attribute]**, scegli `Subtotal`.
   - Clic **[!UICONTROL is]** e scegli `equals or greater than`.
   - Clic **...** e immettere un valore di soglia per il subtotale, ad esempio `100`, per completare la condizione.

   ![Regola prezzo carrello - Condizione](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Se necessario, espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Actions]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Apply]** a `Percent of product price discount`.
   - Imposta **[!UICONTROL Apply to Shipping Amount]** a `Yes`.
   - Imposta **[!UICONTROL Free Shipping]** a `For matching items only`.

## Passaggio 3: Completa le etichette

Completa [Passaggio 4](price-rules-cart.md) delle istruzioni della regola prezzo carrello per inserire le etichette visualizzate durante il pagamento.

## Passaggio 4: Salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fai clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.
