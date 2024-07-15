---
title: 'Esempio di regola prezzo carrello: sconto con primo acquisto'
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire uno sconto ai clienti nuovi.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Esempio di regola prezzo carrello: sconto con primo acquisto

{{ee-feature}}

Le regole di prezzo del carrello possono essere utilizzate per offrire automaticamente uno sconto ai clienti al primo acquisto, senza alcun coupon necessario.

Per offrire uno sconto mirato ai nuovi clienti, puoi:

- Crea un segmento di clienti definito come _acquirenti senza ordini_, quindi
- Crea una regola di prezzo del carrello per eseguire il targeting del nuovo segmento di clienti.

>[!NOTE]
>
>Assicurati che la funzione Segmenti cliente sia abilitata. Consulta [Creare un segmento di clienti](../customers/customer-segment-create.md).

## Passaggio 1: Creare un segmento di cliente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Segment]**.

1. Definisci **[!UICONTROL General Properties]**.

   - Immetti un **[!UICONTROL Segment Name]** per identificare il segmento del cliente (esempio: _Primo cliente_).

   - Per **[!UICONTROL Assigned to Website]**, selezionare il sito Web in cui è possibile utilizzare il segmento del cliente.

   - Per **[!UICONTROL Status]**, selezionare `Active`.

   - Per **[!UICONTROL Apply to]**, selezionare `Visitors and Registered Customers`.

   - Al termine, fare clic su **[!UICONTROL Save and Continue Edit]**.

     Ulteriori opzioni sono disponibili nel pannello a sinistra.

   ![Proprietà segmento cliente](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Definisci **[!UICONTROL Conditions]**.

   In questo esempio, la condizione è destinata ai clienti per i quali _il numero totale di ordini è inferiore a 1_ è True.

   - Nel pannello a sinistra, scegli **[!UICONTROL Conditions]**.

     La condizione predefinita inizia con &quot;Se TUTTE queste condizioni sono TRUE:&quot;

   - Fai clic su _Aggiungi_ (![Aggiungi icona](../assets/icon-add-green-circle.png)) e seleziona `Number of Orders`.

   - Fare clic su **[!UICONTROL is]** e selezionare `less than`.

   - Fare clic su **...** e immettere `1` nel campo.

   - Fai clic sul segno di spunta verde ( ![Segno di spunta verde](../assets/icon-checkmark-green-circle.png) ) per salvare l&#39;impostazione della condizione.

   ![Condizione segmento cliente](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save]**.

Il segmento del cliente viene creato e visualizzato nella griglia _[!UICONTROL Customer Segments]_.

>[!TIP]
>
>Prendi nota dell’ID del segmento. Utilizza questo numero ID per creare la regola del prezzo del carrello.

## Passaggio 2: Crea la regola prezzo carrello

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add New Rule]**.

   La sezione **[!UICONTROL Rule Information]** viene visualizzata per impostazione predefinita, con sezioni espandibili per **[!UICONTROL Conditions]** e **[!UICONTROL Conditions]**.

1. Definisci **[!UICONTROL Rule Information]**.

   - Completare i campi **[!UICONTROL Rule Name]** e **[!UICONTROL Description]**. Questi campi sono solo per riferimento interno.

   - Per **[!UICONTROL Websites]**, selezionare il sito Web in cui la regola deve essere disponibile.

   - Per **[!UICONTROL Customer Groups]**, selezionare il gruppo di clienti a cui si applica questa regola.

     Per selezionare più gruppi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

     >[!NOTE]
     >
     >Le opzioni in questo elenco dipendono dai gruppi di clienti creati e gestiti in **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - Per **[!UICONTROL Coupon]**, selezionare `No Coupon`.

   - Per **[!UICONTROL Uses per Customer]**, immettere `1`.

   - Per **[!UICONTROL Priority]**, immettere un numero per stabilire la priorità di questa regola in relazione ad altre regole.

     >[!NOTE]
     >
     >L&#39;impostazione Priorità è importante quando lo stesso prodotto catalogo soddisfa le condizioni impostate per più regole di prezzo. La regola con priorità più alta diventa attiva per il cliente. La priorità più alta è 1. In questo esempio, l&#39;immissione di `1` indica che questa regola viene applicata prima di qualsiasi altra regola di prezzo. Questo valore viene utilizzato dall&#39;impostazione **[!UICONTROL Discard Subsequent Rules]** nella sezione **[!UICONTROL Action]**.

   - Al termine, fare clic su **[!UICONTROL Save and Continue Edit]**.

     Ulteriori opzioni sono disponibili nel pannello a sinistra.

   ![Informazioni regola prezzi carrello](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Definisci **[!UICONTROL Conditions]**.

   - Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Conditions]**.

     La regola predefinita inizia con &quot;Se TUTTE queste condizioni sono TRUE:&quot;.

   - Fai clic su _Aggiungi_ (![Aggiungi icona](../assets/icon-add-green-circle.png)) e seleziona `Customer Segment`.

     Il campo qualificatore predefinito è `matches`.

   - Fare clic su **...** e immettere l&#39;ID segmento del segmento cliente di destinazione.

     Per questo esempio, l&#39;ID segmento per il nuovo segmento creato nel passaggio 1 è `2`.

     >[!NOTE]
     >
     >Se non conosci l&#39;ID segmento, fai clic sull&#39;icona del selettore ( ![icona Elenco](../assets/icon-list-chooser.png) ) per visualizzare l&#39;elenco dei segmenti cliente. Puoi immettere manualmente l’ID nel campo o selezionare la casella di controllo del segmento desiderato per compilare automaticamente il campo.

   - Fai clic sul segno di spunta verde ( ![Segno di spunta verde](../assets/icon-checkmark-green-circle.png) ) per salvare l&#39;impostazione della condizione.

   - Al termine, fare clic su **[!UICONTROL Save and Continue Edit]**.

     Questa riga della regola si applica a tutti i clienti che corrispondono all’ID segmento cliente 2.

   ![Condizione segmento cliente](./assets/customer-segment-matches.png){width="400"}

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png)sezione **[!UICONTROL Conditions]** e definisci le azioni per la regola.

   In questa sezione vengono definiti il tipo di sconto e il valore/importo dello sconto che si desidera applicare ai clienti nuovi. Questo esempio definisce uno sconto del 10% per tutti i clienti che soddisfano la condizione definita. Per informazioni sulle altre opzioni disponibili, vedere [Creazione di una regola prezzo carrello](price-rules-cart-create.md).

   - Per **[!UICONTROL Apply]**, selezionare Percentuale di sconto prezzo prodotto.

   - Per **[!UICONTROL Discount Amount]**, immettere `10`.

   - Per applicare questa regola di prezzo solo agli importi dei prodotti, impostare **[!UICONTROL Apply to Shipping Amount]** su `No`.

   - Per evitare che il sistema applichi più regole di prezzo allo stesso prodotto, impostare **[!UICONTROL Discard Subsequent Rules]** su `Yes`.

   - Al termine, fare clic su **[!UICONTROL Save]**.

   ![Azioni regola prezzo carrello](./assets/actions-first-time.png){width="600" zoomable="yes"}

La nuova regola è normalmente disponibile entro un’ora. Verifica la regola per assicurarti che funzioni come l’hai definita.

## Passaggio 3: salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fare clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.
