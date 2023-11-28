---
title: Importa prodotti bundle
description: Rivedi un esempio di importazione di dati di prodotto per un prodotto bundle.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Importa prodotti bundle

Un prodotto bundle presenta una selezione di articoli e consente ai clienti di scegliere quelli che desiderano acquistare. Tutti gli elementi che compongono un bundle esistono nel catalogo come [Prodotti semplici](../catalog/product-create-simple.md) o [Prodotti virtuali](../catalog/product-create-virtual.md). In genere, i prodotti bundle vengono creati e aggiornati dall’amministratore. Tuttavia, puoi anche importare i dati per creare un prodotto bundle oppure esportare i prodotti bundle esistenti, modificare i dati e importarli nuovamente nel catalogo. Lo Sprite Yoga Companion Kit è un pacchetto di dati di esempio utilizzato nei seguenti esempi.

![Prodotto bundle](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Modificare l&#39;ordine degli elementi del bundle

Esistono due modi per modificare l’ordine degli elementi in un prodotto bundle.

### Metodo 1: trascinamento della selezione

Quando si lavora con un [Bundle](../catalog/product-create-bundle.md) dall’amministratore, puoi trascinare elementi e sezioni nella posizione desiderata.

![Elementi bundle](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Metodo 2: modificare i dati del prodotto

Il modo migliore per comprendere la struttura di un prodotto bundle è esportare il prodotto ed esaminare i dati in un foglio di calcolo. Per modificare l’ordine degli elementi del bundle, esporta il prodotto e aggiungi un parametro di posizione ai dati di ciascun elemento. I dati dell&#39;elemento sono nel `bundle_values` del prodotto esportato. Quando vengono aperti in un foglio di calcolo, tutti gli elementi associati al prodotto si trovano in un&#39;unica cella come una lunga stringa di testo. Il `bundle_values` La colonna contiene i seguenti elementi per ciascun elemento:

- Nome della sezione dell&#39;elemento
- Controllo input
- Indicatore voce richiesto
- SKU
- Colore
- Prezzo
- Indicatore di opzione predefinito
- Quantità predefinita
- Tipo di prezzo
- Indicatore quantità modificabile

#### Passaggio 1: esportare il prodotto del bundle

In questo passaggio, lo Sprite Yoga Companion Kit viene esportato come ([CSV](data-csv.md) file. Puoi utilizzare qualsiasi altro prodotto bundle presente nel catalogo.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Sotto _Impostazioni di esportazione_, impostato **[!UICONTROL Entity Type]** a `Products`.

1. Nell’elenco degli attributi del prodotto, scorri verso il basso fino a **[!UICONTROL SKU]** e inserisci lo SKU del prodotto bundle da esportare.

   Lo SKU è `24-WG080` per il prodotto in questo esempio.

1. Scorri verso il basso fino alla parte inferiore della sezione e fai clic su **[!UICONTROL Continue]**.

1. In _[!UICONTROL Action]_colonna del_[!UICONTROL File name]_ griglia, fare clic su **[!UICONTROL Select]** e scegli `Download`.

   Il file viene visualizzato nel percorso di download utilizzato dal browser.

#### Passaggio 2: modificare i dati

1. Apri il file CSV scaricato in un foglio di calcolo.

1. Scorri verso l’estrema destra, fino a visualizzare `bundle_values` colonna.

   In `bundle_values` , ogni elemento è separato da una virgola e ogni elemento del bundle è separato dal successivo da una barra verticale. L&#39;ultimo elemento non termina con una barra verticale. I dati del bundle esportato dovrebbero essere simili a quelli del seguente esempio:

   ![Valori bundle](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Per semplificare la modifica, è possibile copiare `bundle_values` e incollarlo in un editor di testo. Quindi, aggiungere un&#39;interruzione di riga dopo ogni elemento, in modo che ogni elemento si trovi su una riga separata.

1. Dopo aver modificato i dati, rimuovi con attenzione le interruzioni di riga e incolla di nuovo i dati modificati in `bundle_values` colonna.

   Nell&#39;illustrazione seguente, un `position=[number]` Il parametro viene aggiunto a ogni cinghia di yoga per modificare l&#39;ordine degli elementi nell&#39;elenco del punto vendita.

   ![Parametro di posizione](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. Dopo aver modificato i dati, **[!UICONTROL Save]** il file CSV.

#### Passaggio 3: importare il prodotto aggiornato

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sotto _[!UICONTROL Import Settings]_, impostato **[!UICONTROL Entity Type]**a `Products`.

1. Imposta **[!UICONTROL Import Behavior]** a `Replace`.

   Invece di aggiungere le modifiche come elementi aggiuntivi, questa opzione sovrascrive i dati precedenti per il prodotto bundle.

1. Scorri verso il basso fino a _File da importare_ e fai clic su **[!UICONTROL Choose File]**.

1. Seleziona il file CSV modificato.

1. Clic **[!UICONTROL Check Data]** e attendi alcuni istanti per il controllo dei dati.

1. Se il file è valido, fare clic su **[!UICONTROL Import]**.

1. Al termine del processo, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**e fai clic su **[!UICONTROL Flush Cache Storage]**.

   In questo modo il prodotto aggiornato sarà immediatamente disponibile nella vetrina.
