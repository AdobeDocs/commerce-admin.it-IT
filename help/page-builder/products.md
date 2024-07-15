---
title: Aggiungi contenuto - Prodotti
description: Scopri il tipo di contenuto Prodotti, utilizzato per aggiungere un elenco di prodotti alla fase  [!DNL Page Builder] .
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 0%

---

# Aggiungi contenuto - Prodotti

Utilizza il tipo di contenuto _Prodotti_ per aggiungere un elenco di prodotti alla [[!DNL Page Builder] fase](workspace.md#stage), utilizzando un layout griglia o carosello. Utilizzare lo strumento [Aggiungi contenuto - Blocco](block.md) per posizionare il blocco nella fase [!DNL Page Builder] e quindi inserire un elenco di prodotti all&#39;interno del blocco. In alternativa, puoi aggiungere l’elenco dei prodotti direttamente in una riga di una pagina.

## Linee guida per l’utilizzo del carosello del prodotto

Il carosello di prodotti offre un modo potente e coinvolgente per mostrare i tuoi prodotti. Per ottenere il massimo da esso, si raccomandano le seguenti linee guida:

- Aggiungi i caroselli di prodotti direttamente ai contenitori con larghezza di pagina, come righe, schede o layout a una colonna. L’utilizzo di layout a larghezza di pagina garantisce una visualizzazione reattiva dei prodotti. [!DNL Page Builder] riduce il numero di prodotti visualizzati in base alla larghezza della pagina, non alla larghezza del contenitore.

- Non aggiungere un carosello di prodotti a una colonna stretta. Come indicato, [!DNL Page Builder] determina per impostazione predefinita il numero di prodotti da visualizzare in base alla larghezza della pagina, non alla larghezza della colonna.

- Se si desidera che il carosello di prodotti scorra automaticamente in modo continuo, impostare **[!UICONTROL Autoplay]** e **[!UICONTROL Infinite Loop]** su `Yes`. Se Riproduzione automatica è impostato su `Yes` ma Ciclo infinito è impostato su `No`, lo scorrimento automatico si interrompe alla fine dell&#39;elenco dei prodotti.

- Impostare **[!UICONTROL Carousel Mode]** su `Continuous` per evidenziare, centrare e scorrere un prodotto alla volta all&#39;interno del carosello. Gli altri prodotti sono visibili nell’elenco, ma trasparenti per evidenziare il prodotto centrato.

  ![Elenco prodotti in modalità carosello continuo](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- Per visualizzare e scorrere fino a cinque prodotti alla volta all&#39;interno del carosello, mantenere **[!UICONTROL Carousel Mode]** impostato su `Default`.

  ![Elenco prodotti in modalità carosello predefinita](./assets/pb-products-settings-carousel-default.png){width="600"}

Le istruzioni seguenti mostrano come aggiungere un elenco di prodotti a un blocco. Puoi quindi utilizzare un [widget](../content-design/widgets.md) per posizionare il blocco in una posizione specifica in qualsiasi pagina dell&#39;archivio.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Prodotti

| Strumento | Icona | Descrizione |
| --------- | ------------- | ----------------- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il contenitore prodotti e il relativo contenuto in un&#39;altra posizione sullo stage. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre la pagina _Modifica prodotti_, in cui è possibile scegliere l&#39;elenco dei prodotti e modificare le proprietà del contenitore. |
| Nascondi | ![Icona Nascondi](./assets/pb-icon-hide.png){width="25"} | Nasconde il contenitore prodotti corrente e il relativo contenuto. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il contenitore prodotti nascosto e il relativo contenuto. |
| Duplica | ![Icona duplicata](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia del contenitore dei prodotti e del relativo contenuto. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina dall’area di visualizzazione il contenitore prodotti e il relativo contenuto. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Creare un blocco per l’elenco dei prodotti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Fare clic su **[!UICONTROL Add New Block]**.

1. Immettere **[!UICONTROL Block Title]** e **[!UICONTROL Identifier]**.

1. Scegli **[!UICONTROL Store View]** dove il blocco deve essere disponibile.

1. Scorrere verso il basso e fare clic su **[!UICONTROL Edit with Page Builder]** o nell&#39;area di anteprima del contenuto per aprire l&#39;area di lavoro [!DNL Page Builder].

1. Nel pannello [!DNL Page Builder], espandere **[!UICONTROL Add Content]** e trascinare un segnaposto **[!UICONTROL Products]** nell&#39;area di visualizzazione.

   ![Aggiungi tipo di contenuto prodotti](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## Configurare il contenitore dell’elenco dei prodotti

Passa il puntatore del mouse sul contenitore _Products_ vuoto per visualizzare la casella degli strumenti e fai clic sull&#39;icona _Settings_ (![Settings](./assets/pb-icon-settings.png){width="20"} ).

![Casella degli strumenti prodotti](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

Completa le _Impostazioni_ in base alle sezioni seguenti:

### Aspetto

1. Per determinare la modalità di visualizzazione dell&#39;elenco dei prodotti nella pagina, scegliere uno dei tipi di aspetto riportati di seguito.

   | Tipo | Descrizione |
   | ---- | ----------- |
   | Griglia prodotti | Visualizza i prodotti all&#39;interno di una griglia che mostra cinque prodotti per riga (per impostazione predefinita), con tutte le righe necessarie per visualizzare il numero immesso nell&#39;impostazione **[!UICONTROL Number of Products to Display]**. |
   | Carosello prodotto | Visualizza i prodotti all’interno di un carosello (noto anche come dispositivo di scorrimento). Il carosello mostra fino a cinque prodotti per diapositiva. <br/><br/>**Avviso reattività**: quando selezioni questo aspetto, è consigliabile aggiungere il tipo di contenuto Prodotti direttamente a un layout di riga, scheda o colonna in cui è reattivo, mostrando un numero inferiore di prodotti per lato su schermi più piccoli. Se lo aggiungi a tipi di contenuto più stretti della larghezza della pagina (ad esempio, una colonna stretta), il carosello visualizza più prodotti per diapositiva di quanto consentito dal contenitore, indipendentemente dalle dimensioni dello schermo. |

   {style="table-layout:auto"}

   ![Aspetto del prodotto](./assets/pb-products-appearances.png){width="300"}

   Se scegli il carosello del prodotto, devi anche configurare le [impostazioni carosello](#carousel-settings).

1. Per **[!UICONTROL Select Products By]**, scegliere il metodo per la selezione del prodotto:

   Puoi selezionare i prodotti per categoria, SKU o condizione. Queste opzioni si escludono a vicenda. Ad esempio, non è possibile selezionare l’opzione Categoria, utilizzare il selettore Categoria, quindi passare all’opzione Condizione per aggiungere alcune condizioni. I prodotti vengono selezionati solo in base a quanto impostato per _una_ di queste tre opzioni.

   - **[!UICONTROL Category]** - Scegliere questa opzione per visualizzare i prodotti utilizzando una categoria selezionata.

     ![Selezione prodotti per categoria](./assets/pb-products-settings_category.png){width="500"}

     Se selezionata, questa opzione fornisce un selettore **[!UICONTROL Category]**. Fare clic sulla freccia ed eseguire il drill-down per scegliere la categoria di prodotti da visualizzare. Ad esempio, nei dati di esempio di [!DNL Commerce], l&#39;espansione e la selezione di _Donne > Punte > Tette_ consentono di visualizzare tutti i prodotti per tale categoria.

     ![Selezione di una categoria di catalogo](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - Scegliere questa opzione per visualizzare i prodotti utilizzando uno o più SKU

     Se selezionata, questa opzione fornisce una casella di testo **[!UICONTROL Product SKUs]** in cui è necessario immettere un elenco separato da virgole di SKU da visualizzare.

     ![Selezione prodotto per SKU](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - Scegliere questa opzione per visualizzare i prodotti in base a una o più condizioni definite.

     Quando è selezionata, sono disponibili strumenti per aggiungere condizioni alla selezione dei prodotti. Ad esempio, puoi selezionare solo i prodotti con un Genere impostato su Unisex.

     ![Selezione prodotto per condizione](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >Se si seleziona l&#39;opzione Categoria o SKU, verrà visualizzata l&#39;opzione **[!UICONTROL Sort By]** di `Position`. Con questa opzione di ordinamento, i prodotti vengono visualizzati nello stesso ordine in cui sono visualizzati nel catalogo.</br>
     >
     >Per l&#39;opzione Categoria, l&#39;ordinamento per posizione consente di visualizzare i prodotti nello stesso ordine in cui sono visualizzati nel catalogo. Per l&#39;opzione SKU, l&#39;ordinamento in base alla posizione consente di visualizzare i prodotti nell&#39;ordine in cui sono stati immessi nella casella di testo **[!UICONTROL Product SKUs]**.

1. Per **[!UICONTROL Sort By]**, scegliere l&#39;ordinamento per i prodotti nell&#39;elenco:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Position` (solo per le opzioni Categoria e SKU) | Quando si seleziona l&#39;opzione Categoria, la posizione visualizza i prodotti nello stesso ordine della loro posizione nel catalogo. Quando selezionate l&#39;opzione SKU, la posizione visualizza i prodotti nello stesso ordine degli SKU all&#39;interno della casella di testo SKU prodotto (Product SKUs). |
   | `Newest products first` | Ordina i prodotti in base alla data in cui sono stati aggiunti al catalogo, visualizzando per primi i prodotti con le date di immissione più recenti. |
   | `Oldest products first` | Ordina i prodotti in base alla data in cui sono stati aggiunti al catalogo, visualizzando prima i prodotti con le date di immissione meno recenti. |
   | `Name: A - Z` | Ordina i prodotti in ordine alfabetico. |
   | `Name: Z - A` | Ordina i prodotti in ordine alfabetico inverso. |
   | `SKU: ascending` | Ordina i prodotti per SKU in ordine alfanumerico. |
   | `SKU: descending` | Ordina i prodotti per SKU in ordine alfanumerico inverso. |
   | `Stock: low stock first` | Ordina i prodotti dal magazzino più basso a quello più alto disponibile. |
   | `Stock: high stock first` | Ordina i prodotti dal magazzino più alto a quello più basso disponibile. |
   | `Price: high to low` | Ordina i prodotti dal prezzo più alto a quello più basso. |
   | `Price: low to high` | Ordina i prodotti dal prezzo più basso a quello più alto. |

   {style="table-layout:auto"}

   ![Opzioni di ordinamento dei prodotti](./assets/pb-products-sortby.png){width="300"}

1. Immettere **[!UICONTROL Number of Products to Display]** nel carosello o nella griglia.

   I valori possono essere compresi tra `1` e `999`. Il valore predefinito è `5` per una griglia e `20` per un carosello.

   >[!NOTE]
   >
   >Alcuni prodotti nelle impostazioni Categoria, SKU o Condizione potrebbero non essere visualizzati nella griglia o nel carosello dei prodotti. Ad esempio, i prodotti disabilitati, i prodotti contrassegnati come non visibili, i prodotti esauriti e i prodotti assegnati a un altro sito Web non vengono visualizzati.

   >[!IMPORTANT]
   >
   >I prezzi per i prodotti configurabili, raggruppati e raggruppati (prezzo dinamico) non sono definiti nell’amministratore. Pertanto, questi prodotti non vengono visualizzati in **[!UICONTROL Preview]** se sono filtrati in base al prezzo. Questi prodotti non possono essere ordinati correttamente in **[!UICONTROL Preview]** se ordinati per prezzo.

### Impostazioni carosello

1. Per determinare la modalità di visualizzazione dei prodotti all&#39;interno del carosello, scegliere **[!UICONTROL Carousel Mode]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Il carosello visualizza cinque prodotti per diapositiva per impostazione predefinita e riduce responsively tale numero in base alle esigenze. |
   | `Continuous` | Per impostazione predefinita, il carosello visualizza cinque prodotti per diapositiva (con metà di un prodotto a destra e a sinistra), ma centra e scorre un prodotto alla volta in un ciclo infinito. I prodotti a destra e a sinistra del prodotto centrato vengono oscurati in modo da evidenziare il prodotto centrale. |

   {style="table-layout:auto"}

   Se passi da una modalità all&#39;altra, le altre impostazioni del carosello vengono mantenute, ad eccezione dell&#39;impostazione **[!UICONTROL Infinite Loop]**, che è sempre impostata su `Yes` in modalità Continua e il campo è disabilitato.

   ![Impostazioni carosello](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. Se necessario, impostare **[!UICONTROL Autoplay]** su `Yes`.

   Quando la riproduzione automatica è abilitata, il carosello inizia a scorrere automaticamente al caricamento della pagina. Se si lascia l&#39;impostazione predefinita (`No`), il cliente deve fare clic sulla navigazione della diapositiva (punti o frecce) per visualizzare ogni diapositiva in sequenza.

   Se si abilita questa funzione, immettere **[!UICONTROL Autoplay Speed]** per specificare il ritardo in millisecondi tra ciascuna diapositiva. Il valore predefinito è `4000` (4 secondi).

1. Se necessario, impostare **[!UICONTROL Infinite Loop]** su `Yes`.

   Quando è attivato il ciclo infinito, la presentazione viene ripetuta indefinitamente mentre la pagina è aperta. Se si lascia l&#39;impostazione predefinita (`No`), la presentazione verrà riprodotta una sola volta.

   >[!NOTE]
   >
   >Se si imposta **[!UICONTROL Infinite Loop]** su `No` e **[!UICONTROL Autoplay]** su `Yes`, la riproduzione automatica si interrompe alla fine del numero di prodotti da visualizzare.

1. Se necessario, impostare **[!UICONTROL Show Arrows]** su `Yes`.

   Quando questa opzione è abilitata, ogni diapositiva include _avanti_ e _precedente_ frecce di navigazione a sinistra e a destra. Se si lascia l&#39;impostazione predefinita (`No`), le diapositive non visualizzano le frecce di spostamento.

1. Se necessario, impostare **[!UICONTROL Show Dots]** su `No`.

   Se è impostata l&#39;impostazione predefinita (`Yes`), nella parte inferiore del dispositivo di scorrimento del carosello vengono visualizzati dei punti di navigazione. Se disattivi questa impostazione, il cursore del carosello non mostra i punti di navigazione.

### Avanzate

1. Per controllare il posizionamento dell&#39;elenco Prodotti all&#39;interno del contenitore padre, scegliere **[!UICONTROL Alignment]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
   | `Left` | Allinea l&#39;elenco lungo il bordo sinistro del contenitore principale, tenendo conto di eventuali spaziature specificate. |
   | `Center` | Allinea l&#39;elenco al centro del contenitore padre, tenendo conto di eventuali spaziature specificate. |
   | `Right` | Allinea l&#39;elenco lungo il bordo destro del contenitore principale, tenendo conto di qualsiasi spaziatura specificata. |

   {style="table-layout:auto"}

1. Imposta lo stile **[!UICONTROL Border]** applicato a tutti e quattro i lati del contenitore Prodotti:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica lo stile di bordo predefinito specificato dal foglio di stile associato. |
   | `None` | Non fornisce alcuna indicazione visibile dei bordi del contenitore. |
   | `Dotted` | Il bordo del contenitore viene visualizzato come una linea tratteggiata. |
   | `Dashed` | Il bordo del contenitore viene visualizzato come una linea tratteggiata. |
   | `Solid` | Il bordo del contenitore viene visualizzato come linea continua. |
   | `Double` | Il bordo del contenitore viene visualizzato come una doppia riga. |
   | `Groove` | Il bordo del contenitore viene visualizzato come una linea scanalata. |
   | `Ridge` | Il bordo del contenitore viene visualizzato come una linea scanalata. |
   | `Inset` | Il bordo del contenitore viene visualizzato come una linea interna. |
   | `Outset` | Il bordo del contenitore viene visualizzato come una linea di contorno. |

   {style="table-layout:auto"}

1. Se si imposta uno stile di bordo diverso da `None`, completare le opzioni di visualizzazione del bordo:

   | Opzione | Descrizione |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Specificate il colore scegliendo un campione, facendo clic sul selettore del colore oppure immettendo un nome di colore valido o un valore esadecimale equivalente. |
   | [!UICONTROL Border Width] | Immettere il numero di pixel per lo spessore della linea del bordo. |
   | [!UICONTROL Border Radius] | Immettere il numero di pixel per definire la dimensione del raggio utilizzato per arrotondare ogni angolo del bordo. |

   {style="table-layout:auto"}

1. (Facoltativo) Specificare i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore.

   Separare più nomi di classe con uno spazio.

1. Immettere i valori, in pixel, per **[!UICONTROL Margins and Padding]** per determinare i margini esterni e la spaziatura interna del contenitore Prodotti.

   Immettere i valori corrispondenti nel diagramma.

   | Area contenitore | Descrizione |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |


## Salva e visualizza l&#39;anteprima sullo stage

Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

Se hai configurato un carosello di prodotto, questo dovrebbe essere simile al seguente esempio:

![Carosello prodotti sullo stage](./assets/pb-products-admin-carousel.png){width="600"}

È ora possibile utilizzare un [widget](../content-design/widgets.md) per posizionare il blocco in qualsiasi punto dell&#39;archivio. In alternativa, è possibile utilizzare [Aggiungi contenuto - Blocco](block.md) per aggiungere il blocco a una pagina, una scheda o un blocco esistente.
