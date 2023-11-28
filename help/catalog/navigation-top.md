---
title: Navigazione superiore
description: Scopri come definire il menu principale di un negozio, che funziona come una directory per i diversi reparti.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Navigazione superiore

Il menu principale del tuo negozio è come un elenco dei diversi reparti del negozio. Ogni opzione rappresenta una categoria diversa di prodotti. La posizione e la presentazione della navigazione superiore possono variare in base al tema, ma il modo in cui funziona è essenzialmente lo stesso.

![Navigazione superiore](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

La struttura delle categorie del catalogo può influenzare l’indicizzazione del sito da parte dei motori di ricerca. Più una categoria è annidata in profondità, meno è probabile che venga indicizzata in modo completo. In genere, l’utilizzo di un numero di livelli visibili compreso tra uno e tre è il più efficace. Il [categoria principale](category-root.md) conta come primo livello, anche se non viene visualizzato nel menu. Il numero massimo di livelli disponibili nella navigazione superiore è determinato dalla configurazione. Inoltre, potrebbe esserci un limite al numero di livelli di menu supportati dal tema del negozio. Ad esempio, il tema Luma di esempio supporta fino a cinque livelli, inclusa la directory principale.

## Livelli del menu di conteggio

| Elemento | Descrizione |
|--- |--- |
| Livello 1 | Il primo livello è la categoria principale, che nei dati di esempio è denominata &quot;Categoria predefinita&quot;. La directory principale è un contenitore per il menu e il suo nome non viene visualizzato come opzione nel menu. |
| Livello 2 | Su uno schermo desktop, la navigazione superiore è il menu principale visualizzato nella parte superiore della pagina. Su un dispositivo mobile, il menu principale viene in genere visualizzato come un menu a comparsa di opzioni. Le opzioni di secondo livello nell’archivio Luma sono _Novità_, _Donne_, _Uomini_, _Ingranaggio_, _Formazione_, e _Vendita_. |
| Livello 3 | Il terzo livello viene visualizzato sotto ogni opzione del menu principale. Ad esempio, in _Donne_, le opzioni di terzo livello sono _In alto_ e _In basso_. |
| Livello 4 | Le opzioni di quarto livello sono sottocategorie che si discostano da un’opzione di terzo livello. Ad esempio, in _In alto_, le opzioni del menu di quarto livello sono _Giacche_, _Felpe e felpe_, _Tees_, e _Reggiseni e serbatoi_. |

{style="table-layout:auto"}

## Impostare la navigazione superiore

La procedura seguente illustra come visualizzare una categoria nella navigazione superiore di un archivio:

### Passaggio 1: creare una categoria

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Imposta un **[!UICONTROL Store View]** per determinare dove sarà disponibile la nuova categoria.

1. Nell&#39;albero delle categorie selezionare la categoria padre della nuova categoria.

   Se inizi dall’inizio senza dati, potrebbero essere presenti solo due categorie nell’elenco: _Categoria predefinita_, che è la radice, e un _Categoria di esempio_.

1. Clic **[!UICONTROL Add Subcategory]**.

1. Completa le informazioni di base con le seguenti impostazioni:

   - **[!UICONTROL Enable Category]** imposta su `Yes`
   - **[!UICONTROL Include in Menu]** imposta su `Yes`

1. In impostazione di visualizzazione **[!UICONTROL Anchor]** a `Yes`.

1. Completa tutte le altre operazioni richieste [impostazioni categoria](category-create.md).

1. Al termine, fai clic su **[!UICONTROL Save]**.

Per un&#39;installazione multistore, è possibile assegnare un menu principale diverso come [categoria principale](category-root.md) per ogni [archiviare](../stores-purchase/stores.md#add-stores).

### Passaggio 2: impostare la profondità della navigazione superiore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi **[!UICONTROL Category Top Navigation]** sezione.

   ![Navigazione superiore categoria](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Perché la profondità della navigazione superiore ha un [ambito di configurazione](../getting-started/websites-stores-views.md#scope-settings), l’impostazione si applica a tutti i siti web, gli store e le visualizzazioni dello store nell’installazione di Commerce. Il _[!UICONTROL Category Top Navigation]_la sezione di configurazione è disponibile solo quando_[!UICONTROL Store View]_ nell’angolo in alto a sinistra è impostato su `Default Config`.

   Per un elenco dettagliato di queste opzioni, vedi [Navigazione superiore categoria](../configuration-reference/catalog/catalog.md#layered-navigation) nel _Riferimento configurazione_.

1. Per limitare il numero di sottocategorie visualizzate nella navigazione superiore, immetti il numero per **[!UICONTROL Maximal Depth]**.

   Il valore predefinito è `0`, che non pone un limite al numero di livelli di sottocategoria.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
