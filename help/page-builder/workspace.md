---
title: '[!DNL Page Builder] Workspace'
description: Scopri gli strumenti disponibili nell'area di lavoro  [!DNL Page Builder]  quando crei pagine di base, pagine di prodotti e cataloghi, blocchi e blocchi dinamici.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

Quando [[!DNL Page Builder] è abilitato](setup.md), la sezione _[!UICONTROL Content]_e il processo di creazione dei contenuti vengono modificati per sfruttare gli strumenti avanzati [!DNL Page Builder] per le [pagine](../content-design/page-add.md), [prodotto](../catalog/product-content.md) e [categoria](../catalog/categories-content-settings.md) pagine, [blocchi](../content-design/block-add.md) e [blocchi dinamici](../content-design/dynamic-blocks.md) di CMS. Questa sezione include un campo_ Intestazione contenuto _, un&#39;anteprima del contenuto e un accesso semplificato all&#39;area di lavoro [!DNL Page Builder] a schermo intero.

![Sezione contenuto con [!DNL Page Builder] anteprima](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Intestazione contenuto

Poiché i motori di ricerca cercano le intestazioni di livello 1 (H1), l’aggiunta di un’intestazione di livello 1 rappresenta un modo semplice per garantire che la pagina venga indicizzata correttamente.

>[!NOTE]
>
>Il campo _[!UICONTROL Content Heading]_visualizzato nella parte superiore della pagina è un campo legacy che supporta il contenuto creato con le versioni precedenti di [!DNL Commerce]. Non fa tuttavia parte di [!DNL Page Builder]. [!UICONTROL Content Heading] è formattato come intestazione H1 in base al foglio di stile associato al tema corrente. È posizionato appena sopra l&#39;area del contenuto attivo definita dalla fase [!DNL Page Builder].

Per un controllo ottimale del posizionamento e del formato delle intestazioni di tutti i livelli, è consigliabile lasciare vuoto il campo _[!UICONTROL Content Heading]_e utilizzare il tipo di contenuto [!DNL Page Builder] [Intestazione](heading.md).

![Intestazione contenuto e altri titoli](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Anteprima

Quando si espande la sezione _[!UICONTROL Content]_ed è presente contenuto creato con [!DNL Page Builder], viene visualizzata un&#39;anteprima del contenuto come apparirebbe in una pagina. Fare clic su **[!UICONTROL Edit with Page Builder]**o all&#39;interno dell&#39;area di anteprima del contenuto per aprire l&#39;area di lavoro [!DNL Page Builder], in cui è possibile apportare gli aggiornamenti necessari.

![Anteprima descrizione prodotto](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Per i moduli prodotto e categoria, questa anteprima del contenuto è abilitata per impostazione predefinita, ma può essere disabilitata. Se le prestazioni risultano ridotte a causa del caricamento dell&#39;anteprima, è possibile disabilitare l&#39;anteprima nelle impostazioni della [configurazione di gestione dei contenuti](../configuration-reference/general/content-management.md#advanced-content-tools).

## Fase

Quando si apre l&#39;area di lavoro [!DNL Page Builder] dall&#39;anteprima, la fase è l&#39;area di lavoro principale in cui è possibile creare e formattare il contenuto e anche apportare modifiche rapide al contenuto live. L&#39;area di visualizzazione è inizialmente vuota e consente di trascinare righe, colonne e schede dal pannello di sinistra.

>[!NOTE]
>
>A partire dalla versione 2.4.1, la modifica del contenuto ora avviene a schermo intero solo per tutte le aree controllate da [!DNL Page Builder]: pagine CMS, pagine di prodotti e categorie, blocchi e blocchi dinamici. La modifica a schermo intero consente di mettere a fuoco i contenuti e offre una visualizzazione che corrisponde meglio all&#39;esperienza utente nella vetrina.

![Fase con contenuto pagina](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Riquadri di visualizzazione

Un _riquadro di visualizzazione_ è l&#39;area visibile di una pagina Web visualizzata dall&#39;utente. In modalità progettazione a schermo intero, i pulsanti del riquadro di visualizzazione vengono visualizzati sopra la fase [!DNL Page Builder] per mostrare il contenuto così come viene visualizzato dall&#39;utente del sito nella vetrina.

![Pulsanti del riquadro di visualizzazione](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] definisce anche i punti di interruzione per i riquadri di visualizzazione. I punti di interruzione definiscono le larghezze minima e massima entro le quali vengono applicati determinati stili. I riquadri di visualizzazione [!DNL Page Builder] forniscono i seguenti punti di interruzione di contenuto:

- **Punto di interruzione desktop**—`min-width: 1024px`. Questo punto di interruzione applica gli stili definiti per le larghezze dei riquadri di visualizzazione che misurano 1024 pixel e più.
- **Punti di interruzione mobile**—`max-width: 768px, min-width: 640px`. Questi punti di interruzione applicano gli stili definiti per larghezze del riquadro di visualizzazione comprese tra 768 e 640 pixel.

I riquadri di visualizzazione [!DNL Page Builder] offrono due funzionalità: **_anteprime contenuto_** e **_impostazioni punto di interruzione_**.

### Anteprime contenuto

Per impostazione predefinita, [!DNL Page Builder] fornisce due anteprime dei riquadri di visualizzazione:

- **Desktop** - Visualizza l&#39;anteprima del contenuto senza una larghezza predefinita. Gli stili definiti dal desktop (che utilizzano una larghezza minima del punto di interruzione di 1024 pixel) vengono ancora applicati alla pagina. Tuttavia, la larghezza del riquadro di visualizzazione Desktop è definita dalle impostazioni per i tipi di contenuto del contenitore, come Righe. Selezionando il riquadro di visualizzazione Desktop viene visualizzato lo stile del contenuto nella vetrina quando la larghezza della pagina del browser è pari o superiore a 1024 pixel.

  ![Anteprima riquadro di visualizzazione desktop con larghezza minima di 1024 pixel](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Dispositivo mobile**: visualizza l&#39;anteprima del contenuto con una larghezza predefinita di 768 pixel. A differenza del riquadro di visualizzazione Desktop, il riquadro di visualizzazione Mobile mostra il contenuto della pagina con una larghezza di 768 pixel, insieme agli stili definiti per le larghezze dei punti di interruzione di 768 pixel (massimo) e 640 pixel (minimo).

  ![Anteprima riquadro di visualizzazione mobile con larghezza minima di 768 pixel](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Impostazioni punto di interruzione

I pulsanti del riquadro di visualizzazione consentono inoltre di applicare stili di punto di interruzione diversi ai tipi di contenuto in base al riquadro di visualizzazione selezionato. Per impostazione predefinita, [!DNL Page Builder] fornisce le impostazioni dei punti di interruzione per i campi _[!UICONTROL Minimum Height]_di Rows, Columns, Tabs, Tab Items, Banners, Sliders e Slides. Quando selezioni il riquadro di visualizzazione mobile e apri l’editor per uno di questi tipi di contenuto, puoi immettere valori di campo specifici per i punti di interruzione del riquadro di visualizzazione mobile. I campi del tipo di contenuto che consentono impostazioni specifiche dei punti di interruzione visualizzano un&#39;icona a destra del campo, simile all&#39;esempio seguente per una riga:

![Indicatore icona per impostazione punto di interruzione](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Pannello

Il pannello [!DNL Page Builder] si trova a sinistra dell&#39;area di visualizzazione e contiene tipi di contenuto che è possibile trascinare nell&#39;area di visualizzazione. Viene quindi visualizzato un contenitore specifico per il tipo di contenuto con una casella strumenti di opzioni. I tipi di contenuto sono organizzati nel pannello come segue:

### Layout

La sezione _[!UICONTROL Layout]_del pannello [!DNL Page Builder] viene utilizzata per aggiungere righe, colonne o schede all&#39;area di visualizzazione. Quando trascini un tipo di contenuto dal pannello all’area di visualizzazione, viene visualizzato un contenitore con una casella degli strumenti contenente le opzioni specifiche per il tipo di contenuto.

Per impostazione predefinita, la fase [!DNL Page Builder] è vuota. Mentre trascini i tipi di contenuto layout dal pannello all’area di visualizzazione, puoi posizionarli sopra, sotto o all’interno di altri contenitori layout sulla pagina. Le righe possono essere aggiunte solo direttamente all&#39;area di visualizzazione.

Pannello ![[!DNL Page Builder] con tipi di contenuto layout e fase](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Tipo di contenuto layout | Descrizione |
| ------------------- |------------ |
| [Riga](row.md) | Una nuova riga può essere trascinata solo dal pannello all’area di visualizzazione e posizionata sopra o sotto un’altra riga, scheda o gruppo di colonne. È inoltre possibile utilizzare l&#39;opzione Duplica per creare una copia di una riga esistente. |
| [Colonna](column.md) | Una colonna può essere trascinata dal pannello all’area di visualizzazione, oppure a righe e schede. Il numero massimo di colonne che è possibile aggiungere è determinato dal numero di divisioni della griglia specificato nella [configurazione](setup.md). |
| [Schede](tabs.md) | Una singola scheda può essere trascinata dal pannello allo stage o a righe e colonne. È possibile aggiungere altre schede dalla casella degli strumenti. |

{style="table-layout:auto"}

### Elementi

Utilizzare la sezione _[!UICONTROL Elements]_del pannello [!DNL Page Builder] per aggiungere testo, intestazioni, pulsanti, divisori e codice HTML a qualsiasi contenitore di layout nella [[!DNL Page Builder] fase](workspace.md#stage). Quando trascini un tipo di contenuto dal pannello a una riga o colonna o a un set di schede sullo stage, viene visualizzato un contenitore. Utilizzare la casella degli strumenti tipo di contenuto per accedere alle impostazioni specifiche del tipo.

Pannello ![[!DNL Page Builder] con tipi di contenuto elemento](./assets/pb-elements.png){width="600" zoomable="yes"}

| Tipo di contenuto elemento | Descrizione |
| -------------------- | ----------- |
| [Testo](text.md) | Aggiunge un contenitore di testo e un editor all&#39;area di visualizzazione. |
| [Intestazione](heading.md) | Aggiunge un contenitore di intestazione all&#39;area di visualizzazione. |
| [Pulsanti](buttons.md) | Aggiunge all&#39;area di visualizzazione un contenitore per un singolo pulsante o un insieme di pulsanti. |
| [Divisore](divider.md) | Aggiunge all&#39;area di visualizzazione un contenitore per un divisore. |
| [Codice HTML](html-code.md) | Aggiunge all&#39;area di visualizzazione un contenitore per il codice HTML. |

{style="table-layout:auto"}

### Media

Utilizzare la sezione _[!UICONTROL Media]_del pannello [!DNL Page Builder] per aggiungere immagini, video, banner, cursori e [!DNL Google Maps] a qualsiasi contenitore di layout sulla [[!DNL Page Builder] fase](workspace.md#stage). Quando un tipo di contenuto multimediale viene trascinato dal pannello all’area di visualizzazione, viene visualizzato un contenitore con una casella degli strumenti contenente le opzioni specifiche per il tipo di contenuto.

Pannello ![[!DNL Page Builder] con tipi di contenuto multimediale](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Tipo di contenuto multimediale | Descrizione |
| ------------------- | ------------------------------------------ |
| [Immagine](image.md) | Aggiunge un contenitore di immagini all&#39;area di visualizzazione. |
| [Video](video.md) | Aggiunge un contenitore video all&#39;area di visualizzazione. |
| [Banner](banner.md) | Aggiunge un contenitore di banner all&#39;area di visualizzazione. |
| [Cursore](slider.md) | Aggiunge un contenitore cursore allo stage. |
| [Mappa](map.md) | Aggiunge un contenitore [!DNL Google Maps] alla fase. |

{style="table-layout:auto"}

### Aggiungi contenuto

Utilizzare la sezione _[!UICONTROL Add Content]_del pannello [!DNL Page Builder] per aggiungere contenuto esistente alla [[!DNL Page Builder] fase](workspace.md#stage). Quando trascini un tipo di contenuto multimediale dal pannello all’area di visualizzazione, viene visualizzato un contenitore. Utilizza la casella degli strumenti del tipo di contenuto per accedere alle_ Impostazioni _specifiche per il tipo.

Pannello ![[!DNL Page Builder] con Aggiungi tipi di contenuto](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Tipo di contenuto | Descrizione |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Blocca](block.md) | Aggiunge un blocco esistente alla fase. |
| [Blocco dinamico](dynamic-block.md) | Aggiunge un blocco dinamico esistente allo stage. |
| [Prodotti](products.md) | Aggiunge un elenco di prodotti alla fase. |
| ![Solo Adobe Commerce](../assets/adobe-logo.svg) [Consigli di prodotto](recommendations.md) | Aggiunge un&#39;unità di consigli alla fase. |

{style="table-layout:auto"}

## Casella strumenti

Ogni contenitore di contenuto sullo stage dispone di una casella strumenti di opzioni. Le opzioni variano in base al tipo di contenuto, ma in genere includono Sposta, Impostazioni, Nascondi/Mostra, Duplica e Rimuovi.

### Mostra casella strumenti

Passa il cursore del mouse sul contenitore per visualizzare la casella degli strumenti e scegli un’opzione.

![Opzioni casella strumenti riga](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Opzioni della Casella degli strumenti

| Opzione | Icona | Descrizione |
| --------- | ---------------------------------------- | ------------ |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il contenitore di contenuto corrente in un&#39;altra posizione sullo stage. |
| Aggiungi | ![Icona Aggiungi](./assets/pb-icon-add.png){width="25"} | Aggiunge elementi figlio come pulsanti, diapositive o tabulazioni. |
| (etichetta) |           | Identifica il tipo di contenuto del contenitore. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre le proprietà del contenitore di contenuto in modalità di modifica. |
| Nascondi | ![Icona Nascondi](./assets/pb-icon-hide.png){width="25"} | Nasconde il contenitore di contenuto corrente. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il contenitore di contenuto corrente. |
| Duplica | ![Icona duplicata](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia del contenitore di contenuto corrente. |
| Rimuovi | ![Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina il contenitore di contenuto corrente dall&#39;area di visualizzazione. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
