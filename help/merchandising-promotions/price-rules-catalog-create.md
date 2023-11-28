---
title: Creare una regola del prezzo di catalogo
description: Scopri come creare una regola del prezzo di catalogo che applica uno sconto a prodotti specifici ogni volta che viene soddisfatta una serie di condizioni.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Creare una regola del prezzo di catalogo

Segui queste istruzioni per applicare uno sconto su prodotti specifici ogni volta che viene soddisfatta una serie di condizioni. Gli sconti della regola del prezzo di catalogo diventano effettivi prima che il prodotto venga inserito nel carrello.

## Passaggio 1: aggiungere una regola

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Rule]**.

   Il _[!UICONTROL Rule Information]_La sezione include sezioni espandibili per **[!UICONTROL Conditions]**e **[!UICONTROL Actions]**.

   ![Regola prezzo catalogo - informazioni](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Completa il **[!UICONTROL Rule Name]** e **[!UICONTROL Description]** campi.

   Questi campi sono solo per riferimento interno.

1. Imposta il **[!UICONTROL Status]** della regola del prezzo, se necessario.

   Per impostazione predefinita, lo stato è `Inactive`.

   >[!NOTE]
   >
   >Dopo la creazione della regola, il relativo stato può essere aggiornato cambiando lo stato in `Active` o `Inactive` secondo necessità.

1. Seleziona la **[!UICONTROL Websites]** dove la regola deve essere disponibile.

1. Seleziona la **[!UICONTROL Customer Groups]** a cui si applica questa regola.

   Per scegliere più gruppi, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   >[!NOTE]
   >
   >Le opzioni in questo elenco dipendono dai gruppi di clienti creati e gestiti in _Clienti_ > _Gruppi di clienti_.

1. ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Inserisci il **[!UICONTROL From]** e **[!UICONTROL To]** date per determinare quando è in vigore la regola prezzo.

   È possibile immettere le date o utilizzare **[!UICONTROL Calendar]** (![Icona Calendario](../assets/icon-calendar.png)) per scegliere le date. Se si lasciano vuote le date, la regola viene attivata quando la regola del prezzo viene salvata.

1. Immetti un numero per stabilire **[!UICONTROL Priority]** della presente regola in relazione ad altre regole.

   >[!NOTE]
   >
   >Il _[!UICONTROL Priority]_L&#39;impostazione è importante quando lo stesso prodotto catalogo soddisfa le condizioni impostate per più di una regola di prezzo. La regola con l’impostazione di priorità più elevata (dove 1 indica la priorità più elevata) diventa attiva per il prodotto.

## Passaggio 2: definire le condizioni

La maggior parte delle condizioni disponibili si basa sui valori di attributo esistenti. Per applicare la regola a tutti i prodotti, lascia vuote le condizioni.

>[!NOTE]
>
>Se almeno un attributo di prodotto condizionale ha un valore vuoto, la regola del prezzo di catalogo non viene applicata al prodotto.

>[!NOTE]
>
>Per applicare una `Category` condizione dell’attributo del prodotto a qualsiasi [fascio](../catalog/product-create-bundle.md) o [raggruppato](../catalog/product-create-grouped.md) prodotto, tutti i prodotti secondari devono essere assegnati alla stessa categoria affinché la regola venga applicata correttamente. In caso contrario, è possibile utilizzare un [Regola prezzo carrello](price-rules-cart-create.md) al suo posto.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Conditions]** sezione.

   La prima condizione viene visualizzata per impostazione predefinita e viene indicata come segue:

   `If **ALL** of these conditions are **TRUE**:`

   ![Regola prezzo catalogo - riga condizione 1](./assets/catalog-condition1.png){width="400"}

   L’istruzione dispone di due collegamenti in grassetto su cui è possibile fare clic per visualizzare la selezione delle opzioni per quella parte dell’istruzione. È possibile creare condizioni diverse modificando la combinazione di questi valori.

1. Modificare l&#39;istruzione in uno dei modi seguenti:

   - Clic **[!UICONTROL ALL]** e seleziona `ALL` o `ANY`.
   - Clic **[!UICONTROL TRUE]** e seleziona `TRUE` o `FALSE`.
   - Lascia invariata la condizione per applicare la regola a tutti i prodotti.

   È possibile creare condizioni diverse modificando la combinazione di questi valori. In questo esempio viene utilizzata la condizione predefinita.

1. Fai clic su _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) all&#39;inizio della riga successiva e seleziona un&#39;opzione per la condizione, ad esempio un attributo o una combinazione di prodotti.

1. Nell’elenco in **[!UICONTROL Product Attribute]**, scegli l’attributo che desideri utilizzare come base della condizione.

   In questo esempio, la condizione è `Attribute Set`.

   ![Regola prezzo catalogo - riga condizione 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Affinché un attributo venga visualizzato nell’elenco, deve essere configurato per l’utilizzo in condizioni di regola promozionale. Per ulteriori informazioni, consulta [Attributi del prodotto](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Quando si utilizza `is not one of` condizione con un _SKU_ attributo del prodotto e prodotto configurabile, è necessario selezionare sia gli SKU del prodotto principale che quelli del prodotto secondario. Per evitare di elencare tutti gli SKU secondari nella regola, puoi utilizzare `does not contain` condizione con parti SKU comuni di un prodotto configurabile e dei relativi prodotti secondari.

   La condizione selezionata viene visualizzata nell&#39;istruzione, seguita da altri due collegamenti in grassetto. Le opzioni variano a seconda dell’attributo di condizione selezionato. L&#39;affermazione ora dice:

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Clic **[!UICONTROL is]** e scegli l’operatore di confronto che descrive la condizione da soddisfare.

   Queste opzioni possono includere un’opzione per diversi confronti. In questo esempio, le opzioni sono `is` e `is not`.

1. Seleziona o immetti i valori per la condizione.

   A seconda della condizione, è possibile selezionare i prodotti da una griglia o da un elenco, immettere un valore numerico e così via.

   ![Regola prezzo catalogo - riga condizione 2](./assets/catalog-condition3.png){width="400"}

   L&#39;elemento selezionato viene visualizzato nell&#39;istruzione per completare la condizione.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Per aggiungere un&#39;altra riga di condizione all&#39;istruzione, fare clic sul pulsante _Aggiungi_ (![Icona Aggiungi](../assets/icon-add-green-circle.png)) e scegliere una delle seguenti opzioni:

   - `Conditions Combination`
   - `Product Attribute`

   Ripetere il processo fino al completamento di tutte le condizioni desiderate.

   Se in qualsiasi momento si desidera eliminare parte dell&#39;istruzione di condizione, fare clic sul pulsante **[!UICONTROL Delete]** (![Icona Elimina](../assets/icon-delete-red-circle.png) alla fine della riga.

## Passaggio 3: definire le azioni

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png)il **[!UICONTROL Actions]** ed effettuare le seguenti operazioni:

   ![Regola prezzo catalogo - azioni](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. Sotto **[!UICONTROL Pricing Structure Rules]**, impostato **[!UICONTROL Apply]** a uno dei seguenti elementi:

   - `Apply as percentage of original` - Sconto sull&#39;articolo sottraendo una percentuale del prezzo regolare. Ad esempio: inserire 10 in Importo sconto per un prezzo finale ridotto del 10% rispetto al prezzo normale.
   - `Apply as fixed amount` - Sconto sull&#39;articolo sottraendo un importo fisso dal prezzo regolare. Ad esempio: inserire 10 in Importo sconto per un prezzo finale inferiore di 10 dollari rispetto al prezzo normale.
   - `Adjust final price to this percentage` - Adegua il prezzo finale di una percentuale del prezzo regolare. Ad esempio: inserire 25 in Importo sconto per un prezzo finale che viene ridotto del 75% rispetto al prezzo normale.
   - `Adjust final price to discount value` - Imposta il prezzo finale su un importo fisso e scontato. Ad esempio: inserire 20 in Importo sconto per un prezzo finale di 20,00 $.

   >[!NOTE]
   >
   >_Prezzo normale_ si riferisce al prezzo di base del prodotto senza sconti promozionali o prezzi avanzati (special/tier/group). _Prezzo finale_ si riferisce al prezzo scontato visualizzato nel carrello. <br/>Il **_finale_** il prezzo del prodotto viene calcolato come **_minimo_** prezzo rilevante, utilizzando la formula seguente: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Prezzo fisso_** Le opzioni personalizzabili del prodotto sono _non_ sono influenzati dalle regole Prezzo di gruppo, Prezzo livello, Prezzo speciale o Prezzo catalogo.

1. Inserisci il **[!UICONTROL Discount Amount]**.

1. Per interrompere l&#39;elaborazione di altre regole dopo l&#39;applicazione di questa regola, impostare **[!UICONTROL Discard Subsequent Rules]** a `Yes`.

   >[!NOTE]
   >
   >Imposta su `Yes` è una garanzia per evitare che il sistema applichi più sconti (regole) allo stesso prodotto.

## Passaggio 4: aggiungere blocchi dinamici correlati

{{ee-feature}}

[Blocchi dinamici](../content-design/dynamic-blocks.md) che sono associati a una regola del prezzo di catalogo vengono visualizzati nella vetrina ogni volta che vengono soddisfatte le condizioni. Questo passaggio è facoltativo.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png)il **[!UICONTROL Related Dynamic Blocks]** sezione.

1. Utilizza il [filtri di ricerca](../getting-started/admin-workspace.md) per individuare i blocchi dinamici da associare alla regola.

1. Seleziona la casella di controllo nella prima colonna per associare il blocco dinamico alla regola.

   ![Regola prezzo catalogo - blocchi dinamici correlati](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save and Continue Edit]**.

## Passaggio 5: pianificare la regola

{{ee-feature}}

>[!NOTE]
>
>L&#39;impostazione della regola su attivo deve essere aggiunta come aggiornamento pianificato. Per ulteriori informazioni, consulta [Modifiche pianificate](price-rule-catalog-scheduled-changes.md).

1. In _Modifiche pianificate_ , fare clic su **[!UICONTROL Schedule New Update]** nella parte superiore della confezione).

   Se la regola dispone di un aggiornamento pianificato esistente, puoi fare clic su **[!UICONTROL View/Edit]** a destra della modifica elencata.

   Puoi modificare l’aggiornamento esistente o assegnare la regola del prezzo di catalogo a un’altra campagna. Il **Modifica aggiornamento esistente** è selezionata per impostazione predefinita.

1. Per pianificare la regola, immettere **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** che la regola del prezzo deve essere attiva.

   È possibile immettere le date o sceglierne una tra le _Calendario_ (![Icona Calendario](../assets/icon-calendar.png)).

   ![Regola prezzo catalogo - programma di aggiornamento](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.

1. In _Informazioni sulle regole_ , impostare **[!UICONTROL Status]** a `active`.

## Passaggio 6: salvare e verificare la regola

1. Al termine, salva la regola.

   - ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Fai clic su **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Fai clic su **[!UICONTROL Save]**.

     Nella pagina Informazioni regola viene visualizzata una sequenza temporale aggiornata nella sezione Modifiche pianificate per la regola.

     ![Regole prezzo catalogo - modifiche pianificate](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Aggiorna proprietà per una regola:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Fai clic su **[!UICONTROL Edit]** per visualizzare _[!UICONTROL Rule Information]_pagina.

   - ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Fai clic sulla regola nell’elenco per visualizzare _[!UICONTROL Rule Information]_pagina.

1. Verifica la regola per assicurarti che funzioni correttamente.

   Le regole di prezzo vengono elaborate automaticamente ogni notte con altre regole di sistema. Quando crei una regola del prezzo, attendi abbastanza tempo affinché entri nel sistema prima di testarla per assicurarti che funzioni correttamente. Con l’aggiunta di nuove regole, Commerce ricalcola di conseguenza i prezzi e le priorità.

## Demo regola prezzo catalogo

Guarda questo video per scoprire come creare le regole del prezzo di catalogo:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## Descrizioni dei campi

### [!UICONTROL Rule Information]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Rule name] | (Obbligatorio) Il nome della regola serve come riferimento interno. |
| [!UICONTROL Description] | Una descrizione della regola deve includere lo scopo della regola e spiegare come viene utilizzata. |
| [!UICONTROL Websites] | (Obbligatorio) Identifica i siti web in cui è possibile utilizzare la regola. |
| [!UICONTROL Customer Groups] | (Obbligatorio) Identifica i gruppi di clienti a cui si applica la regola. |
| [!UICONTROL Priority] | Numero che indica la priorità di questa regola rispetto ad altre. La priorità più alta è il numero 1. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Determina se la regola è attiva nell&#39;archivio. Opzioni: `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Specifica il primo giorno in cui la regola prezzo è in vigore. Se non specificata, la regola del prezzo entra in vigore al momento del salvataggio. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Specifica l&#39;ultimo giorno di validità della regola prezzo. Se non specificata, la regola del prezzo continua a tempo indefinito. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Specifica le condizioni che devono essere soddisfatte prima che la regola del prezzo di catalogo entri in azione. Se non specificato, la regola viene applicata a tutti i prodotti.

### [!UICONTROL Actions]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Apply] | Determina il tipo di calcolo applicato all’acquisto. Opzioni: <br/>**[!UICONTROL Apply as percentage of original]**- Sconto sull&#39;articolo sottraendo una percentuale del prezzo regolare.<br/>**[!UICONTROL Apply as fixed amount]** - Sconto sull&#39;articolo sottraendo un importo fisso dal prezzo regolare. <br/>**[!UICONTROL Adjust final price to this percentage]**- Adegua il prezzo finale di una percentuale del prezzo regolare.<br/>**[!UICONTROL Adjust final price to discount value]** - Imposta il prezzo finale su un importo fisso e scontato. <br/><br/>**_Nota:_**Il prezzo normale si riferisce al prezzo base del prodotto senza prezzi avanzati (special/tier/group) o sconti promozionali. Il prezzo finale si riferisce al prezzo scontato visualizzato nel carrello. <br/>Il**_finale _**il prezzo del prodotto viene calcolato come**_minimo _**prezzo rilevante, utilizzando la formula seguente: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Obbligatorio) L’importo dello sconto offerto. |
| [!UICONTROL Discard Subsequent Rules] | Determina se è possibile applicare regole aggiuntive a questo acquisto. Per evitare l’applicazione di più sconti allo stesso acquisto, seleziona `Yes`. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifica qualsiasi [blocchi dinamici](../content-design/dynamic-blocks.md) associati alla regola.
