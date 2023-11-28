---
title: Risultati di ricerca
description: Scopri come configurare in che modo i prodotti corrispondono ai criteri di ricerca immessi nella casella Ricerca rapida o nel modulo Ricerca avanzata.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# Risultati di ricerca

>[!NOTE]
>
>Questa pagina descrive le funzionalità di ricerca standard che potrebbero essere diverse da [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Il _Risultati di ricerca_ L&#39;elenco include tutti i prodotti che corrispondono ai criteri di ricerca immessi nella casella Ricerca rapida o nel modulo Ricerca avanzata. Ogni elenco di prodotti del catalogo ha essenzialmente gli stessi controlli. L’unica differenza è che uno è il risultato di una query di ricerca e l’altra è il risultato di [navigazione](navigation.md).

I risultati possono essere formattati come griglia o elenco e ordinati in base a una selezione di attributi. I controlli di impaginazione vengono visualizzati se nella pagina sono presenti più prodotti di quanti ne possano contenere. Utilizzare questi controlli per passare da una pagina all&#39;altra. Il numero di record per pagina è determinato dalla configurazione di Catalog Frontend. Per ulteriori informazioni, consulta [Elenco prodotti](navigation-product-listings.md).

Con **Elasticsearch**:

- Non è disponibile il supporto predefinito per la ricerca in base al suffisso. Ad esempio, la ricerca per SKU potrebbe non restituire il risultato previsto se la parola chiave contiene solo la parte finale dello SKU.
- È disponibile il supporto predefinito per la ricerca per prefisso (ricerca parziale per parole chiave) per `name` e `sku` solo attributi del prodotto. La ricerca di tutti gli altri attributi del prodotto viene eseguita in base alla parola chiave intera, con l’esatta corrispondenza.
- Risultati di ricerca per `name` e `sku` gli attributi del prodotto si basano sulla rilevanza, non sulla corrispondenza esatta. Le corrispondenze più rilevanti, ad esempio una corrispondenza esatta _Nome prodotto_ o _SKU_, vengono elencati per primi. Per cercare una corrispondenza esatta, il cliente può utilizzare le virgolette nella query di ricerca. Ad esempio, un `WSH12-32-Red` la query di ricerca può restituire diversi prodotti, ordinati in base alla rilevanza. Ma un `"WSH12-32-Red"` la query di ricerca restituisce un solo prodotto con **_esattamente_** corrisponde `sku`.

![Risultati di ricerca con controlli di impaginazione](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>A causa dell’annuncio di fine del supporto di Elasticsearch 7 relativo ad agosto 2023, si consiglia a tutti i clienti di Adobe Commerce di migrare al motore di ricerca OpenSearch 2.x. Per informazioni sulla migrazione del motore di ricerca durante l’aggiornamento del prodotto, consulta [Migrazione a OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) nel _Guida all’aggiornamento_.

## Mappatura delle parole chiave per estendere i risultati della ricerca

Questa tecnica utilizza un attributo per creare un’associazione basata su parole chiave tra due prodotti in modo che la ricerca di uno dei due prodotti restituisca i risultati per entrambi i prodotti. È possibile utilizzare la mappatura delle parole chiave per promuovere un prodotto nei risultati di ricerca in cui altrimenti non verrebbe visualizzato.

![Risultati di ricerca con mappatura parole chiave](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

Nell&#39;esempio seguente viene utilizzata la mappatura delle parole chiave basata su SKU. Quando si immette uno SKU nella casella di ricerca, entrambi i prodotti vengono visualizzati nei risultati. Vengono mappati gli SKU dei seguenti prodotti configurabili, anziché gli SKU delle varianti di prodotto:

- Giubbotto Antivento Montana (MJ03)
- Cappuccio di canguro Chaz (MH01)

### Passaggio 1: creare un attributo

1. In _[!UICONTROL Products]_, aprire la `Montana Wind Jacket` (MJ03) in modalità di modifica.
1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Attribute]**.
1. Il giorno _Seleziona attributo_ pagina, fai clic su **[!UICONTROL Create New Attribute]**.
1. Completa le proprietà dell’attributo come segue:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label]  - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (impostazione predefinita)
   - [!UICONTROL Use in Filter Options] - `Yes` (impostazione predefinita)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Al termine, fai clic su **[!UICONTROL Save Attribute]**.

   L’attributo viene aggiunto al set di attributi del prodotto.

### Passaggio 2: mappare il primo prodotto

1. Nella pagina delle impostazioni del prodotto, scorri verso il basso ed espandi il _[!UICONTROL Attributes]_sezione.
1. In **[!UICONTROL Search Keywords]** , immettere lo SKU `MH01` da mappare a questo prodotto.

   È possibile immettere più SKU separati da uno spazio nel campo Parole chiave di ricerca. In questo esempio ne viene immesso solo uno.

   ![Sezione Attributi con parola chiave di ricerca](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]**.
1. Vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**e aggiorna **[!UICONTROL Page Cache]**.

### Passaggio 3: mappare il secondo prodotto

1. In _[!UICONTROL Products]_, aprire la `Chaz Kangaroo Hoodie` (MH01) in modalità di modifica.
1. Scorri verso il basso ed espandi **[!UICONTROL Attributes]** sezione.
1. In **[!UICONTROL Search Keywords]** , immettere lo SKU per l&#39;altro prodotto, `MJ03`.
1. Clic **[!UICONTROL Save]**.
1. Vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**e aggiorna **[!UICONTROL Page Cache]**.

### Passaggio 4: testarlo nella vetrina

1. Vai alla vetrina e immetti `MJ03` nel _Ricerca rapida_ casella.
1. Verifica che entrambi i prodotti siano restituiti nell’elenco dei risultati della ricerca.

## Ricerca ponderata

Agli attributi dei prodotti abilitati per la ricerca nel catalogo può essere assegnato un valore più elevato nei risultati di ricerca. Gli attributi con un peso maggiore vengono restituiti prima degli attributi con un peso inferiore. Ad esempio, se nel sistema sono presenti due attributi, _colore_ con un peso di ricerca di 3 e _descrizione_ con un peso di ricerca pari a 1. Ricerca della parola _rosso_ restituisce un elenco di prodotti con un attributo di colore impostato su `red` nella parte superiore dei risultati di ricerca e restituisce prodotti con descrizioni che contengono la parola _rosso_ nella parte inferiore dei risultati della ricerca. In questo esempio, la proprietà `color` l&#39;attributo ha un peso definito maggiore del `description` attributo.

**_Per impostare le proprietà di ponderazione della ricerca di un attributo:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Trova l’attributo nell’elenco e aprilo in modalità di modifica.

1. Nel pannello a sinistra, scegli **[!UICONTROL Storefront Properties]** ed effettuare le seguenti operazioni:

   - Per includere l&#39;attributo nelle query di ricerca, impostare **[!UICONTROL Use in Search]** a `Yes`.

   - Per stabilire il valore di ricerca dell&#39;attributo, impostare **[!UICONTROL Search Weight]** a un numero compreso tra 1 e 10, dove `10` ha la priorità più alta. Se non viene immesso alcun valore, per impostazione predefinita tutti gli attributi hanno lo spessore di ricerca `1`.

   ![Spessore ricerca](./assets/search-weight.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Attribute]**.
