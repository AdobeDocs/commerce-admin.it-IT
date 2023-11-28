---
title: 'Esempio di regola prezzo carrello: sconto con acquisto minimo'
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire uno sconto con un acquisto minimo.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Esempio di regola prezzo carrello: sconto con acquisto minimo

Le regole di prezzo del carrello possono essere utilizzate per offrire uno sconto percentuale in base a un acquisto minimo. Nell&#39;esempio seguente, viene applicato uno sconto del 25% a tutti gli acquisti superiori a $ 200,00 in una categoria specifica. Il formato dello sconto è il seguente:

X% di sconto su tutte le Y (categoria) superiori a $ Z dollari

## Passaggio 1: Creare una regola del carrello

Segui le istruzioni di base [istruzioni](price-rules-cart.md) per creare una regola del carrello.

## Passaggio 2: Definire le condizioni

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Conditions]** sezione.

1. Clic _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) e scegliere **[!UICONTROL Product Attribute Combination]**.

   ![Condizione regola prezzo carrello - combinazione di attributi prodotto](./assets/condition1.png){width="500" zoomable="yes"}

1. Clic _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) all&#39;inizio della riga successiva e nell&#39;elenco in **[!UICONTROL Product Attribute]**, scegli **[!UICONTROL Category]**.

   - Fai clic su (**...**) _altro_ per visualizzare altre opzioni.

     ![Condizione regola prezzo carrello - Opzioni categoria](./assets/condition3.png){width="600" zoomable="yes"}

   - Fai clic su _Selettore_ (![Icona elenco](../assets/icon-list-chooser.png)) per visualizzare le categorie disponibili. Nell&#39;albero delle categorie selezionare la casella di controllo di ogni categoria che si desidera includere. Fai clic sull’icona di spunta per accettare le selezioni per le categorie.

     ![Condizione regola prezzo carrello - categoria](./assets/condition4.png){width="600" zoomable="yes"}

1. Clic _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) all&#39;inizio della riga successiva ed eseguire le operazioni seguenti:

   - Nell’elenco in **[!UICONTROL Cart Item Attribute]**, scegli **[!UICONTROL Price in cart]**.

     ![Condizione regola prezzo carrello - attributo articolo carrello](./assets/condition5.png){width="500"}

   - Clic **è** e scegli `equals or greater than`.

   - Clic **...** e inserire l&#39;importo che il prezzo nel carrello deve essere per soddisfare la condizione. Ad esempio, immetti `30`.

     ![Condizione regola prezzo carrello - prezzo nel carrello](./assets/condition6.png){width="500"}

1. Clic **[!UICONTROL Save and Continue Edit]**.

## Passaggio 3: Definire le azioni

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Actions]** ed effettuare le seguenti operazioni:

   ![Azioni regola prezzi carrello](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Apply]** a `Percent of product price discount`.

   - Inserisci il **[!UICONTROL Discount Amount]**. Ad esempio, immetti `10` per uno sconto del 10%.

   - Per evitare l’applicazione di promozioni aggiuntive all’acquisto, imposta **[!UICONTROL Discard subsequent rules]** a `Yes`.

1. Clic **[!UICONTROL Save and Continue Edit]** e completa la regola come necessario.

## Passaggio 4: Completa le etichette

Completa [Passaggio 4](price-rules-cart.md) delle istruzioni della regola prezzo carrello per inserire le etichette visualizzate durante il pagamento.

## Passaggio 5: salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fai clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.
