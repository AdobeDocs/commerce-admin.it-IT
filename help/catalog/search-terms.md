---
title: Gestire i termini di ricerca
description: Scopri come gestire i termini di ricerca per il tuo negozio per reindirizzare i clienti utilizzando termini errati o alternativi.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 3851258543ba829a4bdbfdb5d3d053ec4627184a
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Gestire i termini di ricerca

Il [pagina di destinazione](../content-design/pages.md) Un termine di ricerca può essere una pagina di contenuto, una pagina di categoria, una pagina di dettagli di un prodotto o anche una pagina di un sito diverso.

Utilizza i termini di ricerca per acquisire gli errori ortografici più comuni e reindirizzarli alla pagina appropriata. Per esempio, se vendete mobili da patio in ferro battuto, sapete che molte persone scrivono erroneamente il termine come _ferro da stiro_, o anche _ferro marcio_. È possibile immettere ogni parola errata come termine di ricerca e renderla sinonimo di _ferro battuto_. Anche se la parola è errata, la ricerca viene indirizzata alla pagina per il ferro battuto.

Puoi anche scoprire cosa cercano i clienti esaminando i termini di ricerca utilizzati per trovare i prodotti nel tuo negozio. Se un numero sufficiente di persone cerca un prodotto che non è presente nel catalogo, potrebbe indicare un’opportunità di vendita. Nel frattempo, invece di lasciarli a mani vuote, puoi reindirizzarli a un altro prodotto nel catalogo.

## Aggiungi termini di ricerca

Man mano che si apprendono nuove parole utilizzate dagli utenti per eseguire ricerche nel negozio, è possibile aggiungerle all&#39;elenco dei termini di ricerca per indirizzare gli utenti verso i prodotti più simili del catalogo.

![Griglia termini di ricerca](./assets/search-terms.png){width="700" zoomable="yes"}

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Search Query] | Query utilizzata per eseguire la ricerca. |
| [!UICONTROL Store] | Archivio in cui è stata applicata la query di ricerca. |
| [!UICONTROL Results] | Numero di risultati trovati per query. |
| [!UICONTROL Uses] | Numero di utilizzi. |
| [!UICONTROL Redirect URL] | URL della pagina di destinazione in cui l&#39;utente è stato reindirizzato dopo aver eseguito la ricerca. |
| [!UICONTROL Suggested Terms] | Determina se il risultato della query visualizza i termini suggeriti. |
| [!UICONTROL Actions] | Apre il prodotto in modalità di modifica. |

{style="table-layout:auto"}

>[!NOTE]
>
>Il numero di risultati viene aggiornato ogni volta che un acquirente esegue una ricerca utilizzando questa query di ricerca. Non viene aggiornato se uno qualsiasi dei prodotti viene modificato o rimosso.

### Aggiungi un termine di ricerca

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Clic **[!UICONTROL Add New Search Term]**.

   ![Informazioni generali sui termini di ricerca](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. Sotto _[!UICONTROL General Information]_nel **[!UICONTROL Search Query]**immettere la parola o la frase da aggiungere come nuovo termine di ricerca.

1. Se il tuo negozio è disponibile in più lingue, scegli il **[!UICONTROL Store]** visualizzazione.

1. Per reindirizzare i risultati della ricerca a un&#39;altra pagina del tuo negozio o a un altro sito Web, immetti l&#39;URL completo della pagina di destinazione in **[!UICONTROL Redirect URL]** campo.

1. Se desideri che questo termine sia disponibile come suggerimento ogni volta che una ricerca non restituisce alcun risultato, imposta **[!UICONTROL Display in Suggested Terms]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Search]**.

## Modificare un termine di ricerca

1. In _[!UICONTROL Search Terms]_fare clic sulla riga di un record per aprire il termine di ricerca in modalità di modifica.

1. Apporta le modifiche necessarie.

1. Al termine, fai clic su **[!UICONTROL Save Search]**.

## Eliminare un termine di ricerca

Esistono due metodi per eliminare un termine di ricerca: dalla griglia e nella pagina di modifica.

**Metodo 1:** In _[!UICONTROL Search Terms]_griglia

1. Nell&#39;elenco selezionare la casella di controllo del termine da eliminare.

1. Nell&#39;angolo superiore sinistro dell&#39;elenco, impostare **[!UICONTROL Actions]** a `Delete`.

1. Al termine, fai clic su **[!UICONTROL Submit]**.

**Metodo 2:** Il giorno _[!UICONTROL Edit a Search Term]_pagina

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Trova il termine di ricerca da eliminare e aprilo in modalità di modifica.

1. Clic **[!UICONTROL Delete Search]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

## Termini di ricerca popolari

Il _Termini di ricerca_ nel piè di pagina del negozio vengono visualizzati i termini di ricerca utilizzati dai visitatori del negozio, ordinati in base alla popolarità. I termini di ricerca vengono visualizzati in una _tag cloud_ formato, in cui la dimensione del testo indica la popolarità del termine.

Per impostazione predefinita, i Termini di ricerca popolari sono abilitati come strumento di ottimizzazione del motore di ricerca, ma non dispongono di una connessione diretta al processo di ricerca del catalogo. Poiché la pagina Termini di ricerca è indicizzata dai motori di ricerca, tutti i termini sulla pagina possono contribuire a migliorare la classificazione del motore di ricerca e la visibilità del tuo negozio. L&#39;URL della pagina Termini di ricerca popolari è: `mystore.com/search/term/popular/`

![Esempio di vetrina: termini di ricerca più comuni](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_Per configurare i termini di ricerca più comuni:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** sezione.

   ![Configurazione del catalogo - Ottimizzazione del motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Ottimizzazione motore di ricerca](../configuration-reference/catalog/catalog.md#search-engine-optimization) nel _Riferimento configurazione_.

1. Imposta **[!UICONTROL Popular Search Terms]** secondo necessità.

   Se necessario, cancellare il **[!UICONTROL Use system value]** per modificare questa impostazione.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Puoi configurare ulteriormente la memorizzazione in cache di popolari [ricerche nel catalogo](search-configuration.md).

## Sinonimi di ricerca

Un modo per migliorare l&#39;efficacia di [ricerca nel catalogo](search-configuration.md) : per includere termini diversi che gli utenti possono utilizzare per descrivere lo stesso elemento. Non vuoi perdere una vendita solo perché qualcuno sta cercando un _divano_ e il tuo prodotto è elencato come _divano_. È possibile acquisire un intervallo più ampio di termini di ricerca immettendo _divano_, _davenport_, e _loveseat_ come sinonimi per _divano_ e li indirizza alla stessa pagina di destinazione.

Adobe Commerce supporta due diverse soluzioni per la gestione dei sinonimi:

- Live Search [Sinonimi](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) Questa funzione è disponibile per le installazioni di Adobe Commerce con Live Search installato.
- La funzione standard Sinonimi di ricerca (descritta in questa pagina) è disponibile come strumento predefinito per tutte le installazioni di Adobe Commerce.

>[!NOTE]
>
>La funzione standard dei sinonimi di ricerca supporta `name` e `sku` attributi prodotto **_solo_**.

>[!IMPORTANT]
>
>La funzione di ricerca dei sinonimi utilizza solo un metodo di ricerca di corrispondenza full-text.

![Esempio di vetrina - risultati di ricerca con sinonimi](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Creare un gruppo di sinonimi

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   Il _[!UICONTROL Search Synonyms]_viene visualizzata la griglia. Se è la prima volta che si utilizzano i sinonimi di ricerca, la griglia è vuota.

   ![Cerca griglia sinonimi](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Clic **[!UICONTROL New Synonym Group]**.

   ![Nuovo gruppo di sinonimi di ricerca](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Imposta **[!UICONTROL Scope]** alle visualizzazioni dello store in cui si applicano i sinonimi.

1. Immetti ogni sinonimo nel gruppo, separato da virgole. Scegliere le parole che gli utenti potrebbero utilizzare come criteri di ricerca. Ad esempio:

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Per unire questi sinonimi in un gruppo con altri che hanno lo stesso ambito, selezionare **[!UICONTROL Merge existing synonyms]** casella di controllo.

1. Al termine, fai clic su **[!UICONTROL Save Synonym Group]**.

### Modificare un gruppo di sinonimi

1. In _[!UICONTROL Search Synonyms]_fare clic sulla riga di un record per aprire il gruppo di sinonimi in modalità di modifica.

1. Apporta le modifiche necessarie.

1. Al termine, fai clic su **[!UICONTROL Save Synonym Group]**.

### Eliminare un gruppo di sinonimi

Esistono due metodi per eliminare un gruppo di sinonimi: dalla griglia e nella pagina di modifica.

**Metodo 1:** Nella griglia Sinonimi di ricerca

1. In _[!UICONTROL Search Synonyms]_nella griglia, selezionare la casella di controllo del gruppo da eliminare.

1. Nell&#39;angolo superiore sinistro dell&#39;elenco, impostare **[!UICONTROL Actions]** a `Delete`.

1. Al termine, fai clic su **[!UICONTROL Submit]**.

**Metodo 2:** Nella pagina Modifica gruppo di sinonimi

1. Nella griglia Sinonimi di ricerca fare clic sulla riga di un record per aprire il gruppo di sinonimi in modalità di modifica.

1. Clic **[!UICONTROL Delete Synonym Group]**.

1. Quando richiesto, confermare la rimozione del gruppo.

## Rapporto Termini di ricerca

Il rapporto Termini di ricerca mostra il numero di risultati per ciascun termine e il numero di volte (hit) in cui il termine è stato utilizzato. I dati del rapporto possono essere filtrati per termine, archivio, risultati e hit ed esportati per ulteriori analisi.

### Visualizzare il rapporto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Utilizza i controlli per filtrare il report in base alle esigenze.

   ![Rapporto termini di ricerca](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Esportare il rapporto

1. Per **[!UICONTROL Export to]**, scegli un formato di esportazione:

   - `CSV` - File di valori separati da virgole contenente dati di testo normale
   - `Excel XML` - Formato di dati di fogli di calcolo basato su XML

1. Clic **[!UICONTROL Export]**.

   Il file generato viene salvato automaticamente nella cartella specificata per i download.

### Colonne report

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL ID] | ID numerico univoco generato per la voce del termine di ricerca |
| [!UICONTROL Search Query] | Query utilizzata per eseguire la ricerca |
| [!UICONTROL Store] | Archivio in cui è stata applicata la query di ricerca |
| [!UICONTROL Results] | Numero di risultati |
| [!UICONTROL Hits] | Numero di utilizzi |

{style="table-layout:auto"}
