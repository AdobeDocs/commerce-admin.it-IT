---
title: 'Esempio di regola prezzo carrello: sconto con primo acquisto'
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire uno sconto ai clienti nuovi.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Esempio di regola prezzo carrello: sconto con primo acquisto

{{ee-feature}}

Le regole di prezzo del carrello possono essere utilizzate per offrire automaticamente uno sconto ai clienti al primo acquisto, senza alcun coupon necessario.

Per offrire uno sconto mirato ai nuovi clienti, puoi:

- Creare un segmento di cliente definito come _acquirenti senza ordini_, e quindi
- Crea una regola di prezzo del carrello per eseguire il targeting del nuovo segmento di clienti.

>[!NOTE]
>
>Assicurati che la funzione Segmenti cliente sia abilitata. Fai riferimento a [Creare un segmento di cliente](../customers/customer-segment-create.md).

## Passaggio 1: Creare un segmento di cliente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Segment]**.

1. Definisci il **[!UICONTROL General Properties]**.

   - Immetti un **[!UICONTROL Segment Name]** per identificare il segmento del cliente (Esempio: _Cliente alle prime esperienze_).

   - Per **[!UICONTROL Assigned to Website]**, seleziona il sito web in cui può essere utilizzato il segmento di clienti.

   - Per **[!UICONTROL Status]**, seleziona `Active`.

   - Per **[!UICONTROL Apply to]**, seleziona `Visitors and Registered Customers`.

   - Al termine, fai clic su **[!UICONTROL Save and Continue Edit]**.

     Ulteriori opzioni sono disponibili nel pannello a sinistra.

   ![Proprietà segmento cliente](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Definisci il **[!UICONTROL Conditions]**.

   Per questo esempio, la condizione è destinata ai clienti per i quali _Il numero totale di ordini è inferiore a 1_ è True.

   - Nel pannello a sinistra, scegli **[!UICONTROL Conditions]**.

     La condizione predefinita inizia con &quot;Se TUTTE queste condizioni sono TRUE:&quot;

   - Clic _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) e seleziona `Number of Orders`.

   - Clic **[!UICONTROL is]** e seleziona `less than`.

   - Clic **...** e immetti `1` nel campo.

   - Fai clic sul segno di spunta verde ( ![Segno di spunta verde](../assets/icon-checkmark-green-circle.png) ) per salvare l&#39;impostazione della condizione.

   ![Condizione del segmento del cliente](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.

Il segmento del cliente viene creato e visualizzato nel _[!UICONTROL Customer Segments]_griglia.

>[!TIP]
>
>Prendi nota dell’ID del segmento. Utilizza questo numero ID per creare la regola del prezzo del carrello.

## Passaggio 2: Crea la regola prezzo carrello

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Rule]**.

   Il **[!UICONTROL Rule Information]** viene visualizzata per impostazione predefinita, con sezioni espandibili per **[!UICONTROL Conditions]** e **[!UICONTROL Conditions]**.

1. Definisci il **[!UICONTROL Rule Information]**.

   - Completa il **[!UICONTROL Rule Name]** e **[!UICONTROL Description]** campi. Questi campi sono solo per riferimento interno.

   - Per **[!UICONTROL Websites]**, seleziona il sito web in cui la regola deve essere disponibile.

   - Per **[!UICONTROL Customer Groups]**, seleziona il gruppo di clienti a cui si applica questa regola.

     Per selezionare più gruppi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

     >[!NOTE]
     >
     >Le opzioni in questo elenco dipendono dai gruppi di clienti creati e gestiti in **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - Per **[!UICONTROL Coupon]**, seleziona `No Coupon`.

   - Per **[!UICONTROL Uses per Customer]**, immetti `1`.

   - Per **[!UICONTROL Priority]**, immettere un numero per stabilire la priorità di questa regola rispetto ad altre regole.

     >[!NOTE]
     >
     >L&#39;impostazione Priorità è importante quando lo stesso prodotto catalogo soddisfa le condizioni impostate per più regole di prezzo. La regola con priorità più alta diventa attiva per il cliente. La priorità più alta è 1. Per questo esempio, immettere `1` significa che questa regola viene applicata prima di qualsiasi altra regola di prezzo. Questo valore viene utilizzato da **[!UICONTROL Discard Subsequent Rules]** impostazione in **[!UICONTROL Action]** sezione.

   - Al termine, fai clic su **[!UICONTROL Save and Continue Edit]**.

     Ulteriori opzioni sono disponibili nel pannello a sinistra.

   ![Informazioni regola prezzo carrello](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Definisci il **[!UICONTROL Conditions]**.

   - Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Conditions]** sezione.

     La regola predefinita inizia con &quot;Se TUTTE queste condizioni sono TRUE:&quot;.

   - Clic _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) e seleziona `Customer Segment`.

     Il campo qualificatore viene impostato automaticamente su `matches`.

   - Clic **...** e inserisci l’ID segmento del segmento cliente di cui desideri eseguire il targeting.

     Per questo esempio, l’ID segmento per il nuovo segmento creato nel passaggio 1 è `2`.

     >[!NOTE]
     >
     >Se non conosci l’ID segmento, fai clic sull’icona del selettore ( ![Icona elenco](../assets/icon-list-chooser.png) ) per visualizzare l&#39;elenco dei segmenti cliente. Puoi immettere manualmente l’ID nel campo o selezionare la casella di controllo del segmento desiderato per compilare automaticamente il campo.

   - Fai clic sul segno di spunta verde ( ![Segno di spunta verde](../assets/icon-checkmark-green-circle.png) ) per salvare l&#39;impostazione della condizione.

   - Al termine, fai clic su **[!UICONTROL Save and Continue Edit]**.

     Questa riga della regola si applica a tutti i clienti che corrispondono all’ID segmento cliente 2.

   ![Condizione del segmento del cliente](./assets/customer-segment-matches.png){width="400"}

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png)il **[!UICONTROL Conditions]** e definiscono le azioni per la regola.

   In questa sezione vengono definiti il tipo di sconto e il valore/importo dello sconto che si desidera applicare ai clienti nuovi. Questo esempio definisce uno sconto del 10% per tutti i clienti che soddisfano la condizione definita. Per informazioni sulle altre opzioni disponibili, vedi [Creazione di una regola prezzo carrello](price-rules-cart-create.md).

   - Per **[!UICONTROL Apply]**, selezionare Percentuale di sconto prezzo prodotto.

   - Per **[!UICONTROL Discount Amount]**, immetti `10`.

   - Per applicare questa regola di prezzo solo agli importi dei prodotti, impostare **[!UICONTROL Apply to Shipping Amount]** a `No`.

   - Per evitare che il sistema applichi più regole di prezzo allo stesso prodotto, impostare **[!UICONTROL Discard Subsequent Rules]** a `Yes`.

   - Al termine, fai clic su **[!UICONTROL Save]**.

   ![Azioni regola prezzi carrello](./assets/actions-first-time.png){width="600" zoomable="yes"}

La nuova regola è normalmente disponibile entro un’ora. Verifica la regola per assicurarti che funzioni come l’hai definita.

## Passaggio 3: salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fai clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.
