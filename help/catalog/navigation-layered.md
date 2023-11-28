---
title: Navigazione a livelli
description: Scopri come la navigazione a livelli consente agli acquirenti di trovare facilmente i prodotti in base alla categoria, alla fascia di prezzo o a qualsiasi altro attributo disponibile.
exl-id: 5f17528a-3593-449c-a044-98736a4ae913
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 1%

---

# Navigazione a livelli

>[!NOTE]
>
>La navigazione a livelli standard descritta in questa sezione differisce dalla navigazione filtrata Live Search con [facet](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

La navigazione a livelli consente di trovare facilmente i prodotti in base alla categoria, alla fascia di prezzo o a qualsiasi altro attributo disponibile. La navigazione a livelli viene in genere visualizzata nella colonna sinistra dei risultati di ricerca e delle pagine delle categorie e talvolta nella home page. La navigazione standard include _Acquista per_ elenco di categorie e fascia di prezzo. Puoi configurare la visualizzazione della navigazione su più livelli, compreso il conteggio dei prodotti e la gamma dei prezzi.

![Navigazione a livelli per categoria e prezzo](./assets/navigation-layered-basic.png){width="700" zoomable="yes"}

## Attributi filtrabili

>[!NOTE]
>
>I requisiti degli attributi filtrabili descritti in questo argomento differiscono per [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Per ulteriori informazioni, consulta [Facet](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

La navigazione a livelli può essere utilizzata per cercare i prodotti per categoria o per attributo. Ad esempio, quando un acquirente sceglie la categoria Mens/Short dalla navigazione superiore, i risultati iniziali includono tutti i prodotti della categoria. L&#39;elenco può essere filtrato ulteriormente scegliendo uno stile, un clima, un colore, un materiale, un motivo o un prezzo specifico oppure una combinazione di valori. Gli attributi filtrabili vengono visualizzati in una sezione espansa che elenca ogni valore di attributo. Come opzione, l’elenco dei prodotti con risultati corrispondenti può essere configurato per includere prodotti con o senza corrispondenza.

Le proprietà dell’attributo, combinate con il tipo di input del prodotto, determinano gli attributi che possono essere utilizzati per la navigazione su più livelli. La navigazione a livelli è disponibile solo per [_ancoraggio_](categories-display-settings.md) , ma possono anche essere aggiunte alle pagine dei risultati di ricerca. Il **Tipo di input del catalogo per il proprietario del negozio** la proprietà di ciascun attributo deve essere impostata su `Yes/No`, `Dropdown`, `Multiple Select`, o `Price`. Per rendere gli attributi filtrabili, la **Uso in navigazione a livelli** proprietà di ogni deve essere impostata su `Filterable (with results)` o `Filterable (no results)`.

_Esempio: attributi filtrabili con risultati_

![Attributi filtrabili nella navigazione a livelli](./assets/storefront-layered-navigation-filtered.png){width="700" zoomable="yes"}

_Esempio: i valori dei campioni filtrabili vengono visualizzati senza risultato_

![Valore campione filtrabile senza risultati](./assets/storefront-product-attribute-filter-no-results.png){width="700" zoomable="yes"}

Le istruzioni seguenti mostrano come impostare una navigazione a livelli di base con attributi filtrabili. Per una navigazione avanzata su più livelli con fasce di prezzo, consulta [Navigazione prezzi](navigation-layered.md#configure-price-navigation).

## Passaggio 1: impostare le proprietà dell’attributo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Sfoglia o utilizza la ricerca filtrata per trovare un attributo nell’elenco e aprirlo in modalità di modifica.

   ![Immetti i termini di ricerca per colonna da utilizzare per la ricerca filtrata](./assets/attribute-search.png){width="700" zoomable="yes"}

1. Nel pannello a sinistra, scegli **[!UICONTROL Storefront Properties]** e imposta **[!UICONTROL Use In Layered Navigation]** a uno dei seguenti elementi:

   - `Filterable (with results)` - La navigazione a livelli include solo i filtri per i quali è possibile trovare prodotti corrispondenti. Qualsiasi valore di attributo già applicato a tutti i prodotti visualizzati nell’elenco deve comunque essere visualizzato come filtro disponibile. I valori degli attributi con un conteggio di zero (0) corrispondenze con i prodotti vengono omessi dall’elenco dei filtri disponibili. L’elenco filtrato include solo i prodotti che corrispondono al filtro. L’elenco dei prodotti viene aggiornato solo se i filtri selezionati modificano ciò che viene visualizzato.

   - `Filterable (no results)` - La navigazione a livelli include filtri per tutti i valori di attributo disponibili e i relativi conteggi di prodotti, inclusi i prodotti con zero (0) corrispondenze di prodotto. Se il valore dell’attributo è un campione, viene visualizzato come filtro ma viene barrato. Il filtro a livelli di prezzo non è supportato da questa opzione e non influisce sui filtri di prezzo.

1. Imposta **[!UICONTROL Use In Search Results Layered Navigation]** a `Yes`.

   ![Proprietà vetrina](./assets/attribute-storefront-properties.png){width="600" zoomable="yes"}

1. Ripetere questi passaggi per ogni attributo che si desidera includere nella navigazione a livelli.

>[!NOTE]
>
>Il [!UICONTROL Position] Il campo è disattivato per impostazione predefinita, pertanto è necessario salvare l&#39;attributo prima di poter modificare questa impostazione.

## Passaggio 2: rendere la categoria un ancoraggio

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nella struttura delle categorie selezionare la categoria in cui si desidera utilizzare la navigazione a livelli.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Display Settings]** sezione e set **[!UICONTROL Anchor]** a `Yes`.

   ![Impostazioni di visualizzazione categoria](./assets/category-layered-navigation-anchor.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.

## Passaggio 3: verificare i risultati

Per verificare l’impostazione, visita il negozio e passa alla categoria dal menu principale. La selezione degli attributi filtrabili viene visualizzata nella navigazione a livelli della pagina della categoria.

Cerca, filtra e controlla i prodotti visualizzati.

## Rimuovere i valori degli attributi filtrabili dalla navigazione a livelli

La navigazione a livelli include filtri per tutti i valori di attributo disponibili e i relativi conteggi di prodotti, inclusi i prodotti con zero (0) corrispondenze di prodotti (come mostrato nell’immagine seguente).

![Visualizzazione dei filtri zero](./assets/filterable-attributes-on-plp.png){width="700" zoomable="yes"}

Questo risultato può rendere difficile per i clienti selezionare un prodotto preferito e non è necessario visualizzare i valori degli attributi &#x200B;&#x200B;con 0 prodotti nel front-end.

Per rimuovere i valori degli attributi filtrabili con 0 prodotti dalla navigazione a livelli, attenersi alla procedura descritta di seguito.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Sfoglia o utilizza la ricerca filtrata per trovare un attributo nell’elenco e aprirlo in modalità di modifica.

1. Sotto _[!UICONTROL Attribute Information]_, fai clic su **[!UICONTROL Storefront Properties]**.

1. Per **[!UICONTROL Layered Navigation]**, scegli `Filterable (with results)`.

   ![Sezione Informazioni attributo](./assets/storefront-properties-tab.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Attribute]**.

## Navigazione prezzi

>[!NOTE]
>
>La configurazione della navigazione del prezzo descritta in questo argomento è diversa per [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La navigazione dei prezzi può essere utilizzata per distribuire i prodotti in base alla fascia di prezzo in una navigazione a più livelli. È inoltre possibile suddividere ogni intervallo in intervalli. Esistono alcuni modi per calcolare la navigazione dei prezzi:

- Automatico (equalizza intervalli prezzi)
- Automatico (Equalizza conteggi prodotti)
- Manuale

Con i primi due metodi, i passaggi di navigazione vengono calcolati automaticamente. Il metodo manuale consente di specificare un limite di divisione per gli intervalli di prezzo. L’esempio seguente mostra la differenza tra i passaggi di navigazione del prezzo 10 e 100.

La suddivisione iterativa fornisce la migliore distribuzione dei prodotti tra le fasce di prezzo. Con la suddivisione iterativa, dopo aver scelto l&#39;intervallo tra 0,00 e 99 dollari, il cliente può analizzare in profondità diversi sottogruppi di prezzi. La suddivisione dell&#39;intervallo di prezzi si interrompe quando il numero di prodotti raggiunge la soglia impostata dal limite di divisione intervallo.

## Esempio: Passaggi di navigazione del prezzo

| Prezzo Incrementato di 10 | Prezzo Incrementato di 100 |
|----------|--------|
| $20.00 - $29.99 (1) | $0.00 - $99.99 (4) |
| $30.00 - $39.99 (2) | $100 - $199.99 (5) |
| $70.00 - $79.99 (1) | $400.00 - $499.99 (2) |
| $100.00 - $109.99 (1) | $700,00 e versioni successive (1) |
| $120.00 - $129.99 (2) |   |
| $150.00 - $159.99 (1) |   |
| $180.00 - $189.99 (1) |   |
| $420.00 - $429.99 (1) |   |
| $440.00 - $449.99 (1) |   |
| $710,00 e versioni successive (1) |   |

{style="table-layout:auto"}

## Configurare la navigazione del prezzo

>[!IMPORTANT]
>
>Per visualizzare correttamente i prodotti e i relativi prezzi in base a _filtri di prezzo_ nella navigazione a livelli, accertati che le impostazioni per il prezzo siano visualizzate nella sezione [Configurazione IVA](../configuration-reference/sales/tax.md) hanno lo stesso valore (`Excluding Tax` **o** `Including Tax`). Per _[!UICONTROL Calculation Settings]_, controlla **[!UICONTROL Catalog Prices]**valore. E per_[!UICONTROL Price Display Settings]_, controlla **[!UICONTROL Display Product Prices in Catalog]** valore. Se questi hanno valori diversi, i filtri dei prezzi nella navigazione a livelli potrebbero non filtrare e ordinare correttamente i prodotti in base al prezzo.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _Navigazione a livelli_ sezione.

   Per impostazione predefinita, **[!UICONTROL Display Product Count]** è impostato su `Yes`. Se necessario, deselezionare la **[!UICONTROL Use system value]** per modificare questa impostazione.

   ![Navigazione a livelli](../configuration-reference/catalog/assets/layered-navigation.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni di configurazione, vedi [Navigazione a livelli](../configuration-reference/catalog/catalog.md#layered-navigation) nel _Riferimento configurazione_.

1. Imposta **[!UICONTROL Price Navigation Steps Calculation]** per uno dei metodi descritti nelle sezioni seguenti.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Metodo 1: Automatico (equalizza intervalli di prezzi)

Esci **[!UICONTROL Price Navigation Steps Calculation]** imposta su `Automatic (Equalize Price Ranges)` (impostazione predefinita). Questa impostazione utilizza l’algoritmo standard per la navigazione del prezzo.

### Metodo 2: Automatico (equalizza conteggi prodotti)

>[!TIP]
>
>Se necessario, deselezionare **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Imposta **[!UICONTROL Price Navigation Steps Calculation]** a `Automatic (equalize product counts)`.

1. Per visualizzare un solo prezzo quando più prodotti hanno lo stesso prezzo, impostare **[!UICONTROL Display Price Interval as One Price]** a `Yes`.

1. Per **[!UICONTROL Interval Division Limit]**, immettere la soglia per il numero di prodotti compresi in una fascia di prezzo.

   L’intervallo non può essere ulteriormente suddiviso oltre questo limite. Il valore predefinito è `9`.

   ![Automatico (equalizza conteggi prodotti)](../configuration-reference/catalog/assets/layered-navigation-equalize-product-counts.png){width="600" zoomable="yes"}

### Metodo 3: manuale

>[!NOTE]
>
>Se necessario, deselezionare **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Imposta **[!UICONTROL Price Navigation Steps Calculation]** a `Manual`.

1. Immetti un valore che determina **[!UICONTROL Default Price Navigation Step]**.

1. Inserisci il **[!UICONTROL Maximum Number of Price Intervals]** consentito, fino a `100`.

   ![Manuale](../configuration-reference/catalog/assets/layered-navigation-manual.png){width="600" zoomable="yes"}

## Configurare la navigazione su più livelli

>[!NOTE]
>
>La configurazione standard descritta in questa pagina è diversa per [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La configurazione della navigazione a livelli determina se un conteggio dei prodotti viene visualizzato tra parentesi dopo ogni attributo e la dimensione del calcolo del passaggio utilizzato nella navigazione dei prezzi.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi _[!UICONTROL Catalog]_e scegliere **[!UICONTROL Catalog]**sotto.

1. Espandi _[!UICONTROL Layered Navigation]_sezione.

   >[!NOTE]
   >
   >Se necessario, deselezionare **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Per visualizzare il numero di prodotti trovati per ogni attributo, impostare **[!UICONTROL Display Product Count]** a `Yes`.

1. Imposta **[!UICONTROL Price Navigation Step Calculation]** a `Automatic (equalize price ranges)`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
