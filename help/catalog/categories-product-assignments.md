---
title: Assegnazioni prodotti categoria
description: Informazioni sull'utilizzo delle impostazioni [!UICONTROL Products in Category] per controllare quali prodotti sono attualmente assegnati alla categoria.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: eb78c90debf31c8e28b3710584e6865dae1cb6a4
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Assegnazioni prodotti categoria

Per una categoria, utilizzare la sezione _[!UICONTROL Products in Category]_per esaminare i prodotti attualmente assegnati alla categoria. I filtri di ricerca nella parte superiore di ogni colonna vengono utilizzati per aggiungere e rimuovere prodotti dalla categoria. Puoi anche utilizzare [regole di categoria](../merchandising-promotions/category-product-rules.md) (![solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce) per modificare dinamicamente la selezione del prodotto quando viene soddisfatta una serie di condizioni. Per ulteriori informazioni, vedere [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Durante la configurazione della regola di categoria, i prodotti sono _ordinati_, _corrispondenti_, _assegnati_ e _non assegnati_ in base a tale regola **_solo_** quando la categoria viene salvata. Per assicurarsi che un nuovo prodotto venga assegnato in base alla regola quando lo si aggiunge al catalogo, è **necessario salvare nuovamente ogni categoria** impostata in modo che corrisponda ai prodotti per regola. Inoltre, se lo stato delle scorte dei prodotti viene modificato in `In Stock` o `Out of Stock` e i prodotti della categoria sono _ordinati_ in base alla regola **Ordinamento automatico**, è necessario fare clic su **[!UICONTROL Save Category]**.

![Prodotti categoria](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Nelle pagine delle categorie, `Out of stock` prodotti sono sempre visualizzati **_dopo_** `In Stock` prodotti nell&#39;elenco dei prodotti con tutti i tipi di ordinamento.

>[!NOTE]
>
>La colonna _Stock_ visualizza la quantità di prodotto disponibile solo per _**ambito categoria selezionato**_. Quando per i prodotti vengono gestite più scorte, è necessario passare dagli ambiti corrispondenti per visualizzare altri valori di colonna _Stock_ nella griglia _Prodotti categoria_.

## Applicare una regola di categoria

{{ee-feature}}

1. Imposta **[!UICONTROL Match products by rule]** su `Yes`.

   Vengono visualizzate le opzioni di ordinamento e condizione automatiche.

   ![Per abbinare i prodotti per regola](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Imposta l&#39;ordine **[!UICONTROL Automatic Sorting]**.

   L’ordinamento automatico si basa sulle condizioni correnti.

   - `Stock level` - Sposta in alto o in basso.
   - `Special price` - Sposta in alto o in basso.
   - `New Products` - Elenca prima i prodotti più recenti.
   - `Color` - Ordina alfabeticamente per colore.
   - `Name` - Ordine crescente o decrescente in base al nome.
   - `SKU` - Ordine crescente o decrescente per SKU
   - `Price` - Ordine crescente o decrescente in base al prezzo.

1. Fare clic su **[!UICONTROL Add Condition]** ed effettuare le seguenti operazioni:

   - Scegliere **[!UICONTROL Attribute]** che è la base della condizione.
   - Scegliere il **[!UICONTROL Operator]** necessario per formare l&#39;espressione.
   - Immettere il **[!UICONTROL Value]** a cui deve corrispondere la corrispondenza.

   ![Aggiungi condizione alla regola di categoria](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Ripetere questo processo per ogni attributo da utilizzare per descrivere le condizioni da soddisfare. Ad esempio, per trovare i prodotti creati da 7 a 30 giorni fa, effettua le seguenti operazioni:

   - Imposta **[!UICONTROL Date Created]** su `Less than 30`.
   - Imposta **[!UICONTROL Logic]** su `AND`.
   - Imposta **[!UICONTROL Date Modified]** su `Greater than 7`.

1. Al termine, fare clic su **[!UICONTROL Save Category]**.

### Opzioni pagina

| Opzione | Descrizione |
|--- |--- |
| [!UICONTROL Match products by rule] | Determina se l’elenco dei prodotti nella categoria viene generato in modo dinamico da una regola di categoria. Opzioni: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | Applica automaticamente un ordinamento all&#39;elenco dei prodotti della categoria. Opzioni: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Aggiunge un&#39;altra condizione alla regola. |

{style="table-layout:auto"}

### Condizioni pagina

| Opzione | Descrizione |
|--- |--- |
| [!UICONTROL Attribute] | Determina l&#39;attributo utilizzato come base della condizione. Opzioni: <br/>**[!UICONTROL Clone Category ID(s)]**- Duplica in modo dinamico i prodotti, senza il relativo ordinamento e ordine, da più categorie in base all&#39;ID categoria.<br/>**[!UICONTROL Color]** - Include prodotti in base al colore. <br/>**[!UICONTROL Date Created (days ago)]**- Include i prodotti in base al numero di giorni dall&#39;aggiunta dei prodotti al catalogo.<br/>**[!UICONTROL Date Modified (days ago)]** - Include i prodotti in base al numero di giorni dall&#39;ultima modifica dei prodotti. <br/>**[!UICONTROL Name]**- Include prodotti basati sul nome del prodotto.<br/>**[!UICONTROL Price]** - Include i prodotti in base al prezzo. <br/>**[!UICONTROL Quantity]**- Include i prodotti in base alla quantità in magazzino.<br/>** SKU **- Include prodotti basati su SKU. |
| [!UICONTROL Operator] | Specifica l&#39;operatore applicato al valore dell&#39;attributo per soddisfare la condizione. A meno che non sia specificato un operatore, viene utilizzato `Equal` come valore predefinito. Opzioni: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Specifica il valore che l&#39;attributo deve soddisfare la condizione. |
| [!UICONTROL Logic] | Utilizzato per definire più condizioni e viene visualizzato solo quando viene aggiunta un’altra condizione. Opzioni: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>La quantità di un prodotto configurabile con opzioni figlio viene calcolata combinando tutte le quantità di prodotto figlio. Prendi in considerazione un esempio di prodotto configurabile _Endurance Fitness Tank_ con opzioni di colore viola, rosso e giallo e diverse quantità di ciascuno. In questo scenario, la quantità del prodotto padre corrisponde alla quantità combinata dei prodotti secondari di colore viola, rosso e giallo.

## Controlli


## Controlli pagina

{{ee-feature}}

| Controllo | Descrizione |
|----------|--------------|
| ![Visualizza come elenco](../assets/icon-view-list.png) | Visualizza come elenco |
| ![Visualizza come sezioni](../assets/icon-view-tiles.png) | Visualizza come riquadri |
| ![Attiva/Disattiva ](../assets/toggle-no.png) | Corrispondenza per regola - No |
| ![Attiva/Disattiva Sì](../assets/toggle-yes.png) | Corrispondenza per regola - Sì |
| ![Sposta controller](../assets/icon-move.png) | Il controllo di trascinamento consente di acquisire un prodotto e spostarlo in un&#39;altra posizione nella pagina corrente della griglia. Per ulteriori informazioni, vedere [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Controller posizione](../assets/control-position.png) | Determina la posizione del prodotto nell&#39;elenco. |

{style="table-layout:auto"}

## Controlli pagina

{{ce-feature}}

| Controllo | Descrizione |
|----------|--------------|
| ![Casella di controllo selezionata](../assets/checkbox-selected.png) | Utilizza la casella di controllo nell’intestazione della prima colonna per selezionare tutti i prodotti o cancellare tutte le selezioni. Il controllo nella prima riga determina il tipo di ricerca e può essere impostato per includere qualsiasi record oppure solo i record assegnati o non assegnati alla categoria. La casella di controllo nella prima colonna di ogni riga identifica i prodotti da aggiungere alla categoria. Opzioni: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | I controlli filtro nella parte superiore di ogni colonna possono essere utilizzati per immettere valori specifici che si desidera includere o omettere dall&#39;elenco, a seconda dell&#39;impostazione Seleziona tutto. |
| [!UICONTROL Reset Filter] | Cancella tutti i filtri di ricerca. |
| [!UICONTROL Search] | Cerca il catalogo in base ai criteri di filtro e visualizza il risultato. |

{style="table-layout:auto"}
