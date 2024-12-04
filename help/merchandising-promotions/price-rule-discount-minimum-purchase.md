---
title: 'Esempio di regola prezzo carrello: sconto con prezzo minimo del prodotto'
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire uno sconto con un prezzo del prodotto minimo.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 6bc76c76bc7a17e115696911cc2499075d35c541
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Esempio di regola prezzo carrello: sconto con acquisto minimo

Le regole di prezzo del carrello possono essere utilizzate per offrire uno sconto percentuale basato su un prezzo prodotto minimo nel carrello. Nell’esempio seguente, uno sconto del 10% viene applicato a tutti i prodotti nell’intero carrello quando almeno 1 prodotto con un prezzo superiore a $ 30,00 da una categoria specificata viene aggiunto al carrello. Il formato dello sconto è il seguente:

X% intero carrello spento quando almeno 1 prodotto è dalla categoria Y e il suo prezzo è superiore a $ Z dollari.

## Passaggio 1: Creare una regola del carrello

Segui le [istruzioni](price-rules-cart.md) di base per creare una regola carrello.

## Passaggio 2: Definire le condizioni

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Conditions]**.

1. Fai clic su _Aggiungi_ (![Aggiungi icona](../assets/icon-add-green-circle.png)) e scegli **[!UICONTROL Product Attribute Combination]**.

   ![Condizione regola prezzo carrello - combinazione di attributi prodotto](./assets/condition1.png){width="500" zoomable="yes"}

1. Fare clic su _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) all&#39;inizio della riga successiva e nell&#39;elenco in **[!UICONTROL Product Attribute]** scegliere **[!UICONTROL Category]**.

   - Fai clic sul collegamento (**...**) _altro_ per visualizzare altre opzioni.

     ![Condizione regola prezzo carrello - Opzioni categoria](./assets/condition3.png){width="600" zoomable="yes"}

   - Fai clic sull&#39;icona _Selettore_ (![icona Elenco](../assets/icon-list-chooser.png)) per visualizzare le categorie disponibili. Nell&#39;albero delle categorie selezionare la casella di controllo di ogni categoria che si desidera includere. Fai clic sull’icona di spunta per accettare le selezioni per le categorie.

     ![Condizione regola prezzo carrello - categoria](./assets/condition4.png){width="600" zoomable="yes"}

1. Fai clic su _Aggiungi_ (![Aggiungi icona](../assets/icon-add-green-circle.png)) all&#39;inizio della riga successiva ed effettua le seguenti operazioni:

   - Nell&#39;elenco in **[!UICONTROL Cart Item Attribute]**, scegliere **[!UICONTROL Price in cart]**.

     ![Condizione regola prezzo carrello - attributo articolo carrello](./assets/condition5.png){width="500"}

   - Fai clic su **is** e scegli `equals or greater than`.

   - Fare clic su **...** e immettere l&#39;importo che il prezzo nel carrello deve corrispondere alla condizione. Immettere ad esempio `30`.

     ![Condizione regola prezzo carrello - prezzo nel carrello](./assets/condition6.png){width="500"}

1. Fare clic su **[!UICONTROL Save and Continue Edit]**.

## Passaggio 3: Definire le azioni

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Actions]** ed effettuare le seguenti operazioni:

   ![Azioni regola prezzo carrello](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Apply]** su `Percent of product price discount`.

   - Immettere **[!UICONTROL Discount Amount]**. Ad esempio, immettere `10` per uno sconto del 10%.

   - Per impedire l&#39;applicazione di promozioni aggiuntive all&#39;acquisto, impostare **[!UICONTROL Discard subsequent rules]** su `Yes`.

1. Fare clic su **[!UICONTROL Save and Continue Edit]** e completare la regola in base alle esigenze.

## Passaggio 4: Completa le etichette

Completa il [passaggio 4](price-rules-cart.md) delle istruzioni della regola prezzo carrello per inserire le etichette visualizzate durante l&#39;estrazione.

## Passaggio 5: salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fare clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.
