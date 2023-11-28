---
title: Riferimento attributi dati prodotto
description: Utilizza questo riferimento degli attributi dei dati del prodotto quando utilizzi importazioni ed esportazioni di dati del prodotto.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2469'
ht-degree: 2%

---

# Riferimento attributi dati prodotto

Nella tabella seguente sono elencati gli attributi di un&#39;esportazione di prodotti tipica, nell&#39;ordine predefinito in cui vengono visualizzati. Ogni attributo è rappresentato nel file CSV come una colonna e i record dei prodotti sono rappresentati da righe. Le colonne che iniziano con un carattere di sottolineatura contengono dati del servizio quali proprietà o valori di opzione per dati complessi. È possibile [esportare](data-export.md) un prodotto del catalogo, per vedere come ogni attributo è rappresentato nei dati.

Nell’installazione utilizzata per esportare questi dati sono installati i dati di esempio, oltre a due siti web e diverse visualizzazioni dello store. Anche se questo elenco include tutte le colonne che vengono in genere esportate, il `sku` è l’unico valore richiesto. Per importare i dati, è possibile includere solo le colonne con le modifiche. Il `sku` deve essere la prima colonna, ma l’ordine degli altri attributi non ha importanza.

## Struttura semplice dei file CSV dei prodotti

| Attributo | Descrizione |
|--- |--- |
| `sku` | (Obbligatorio) L’unità di gestione delle scorte è un identificatore alfanumerico univoco utilizzato per tenere traccia delle scorte. Una SKU può contenere fino a 64 caratteri. Ad esempio: `sku123`<br/>**_Nota:_**Se lo SKU supera i 64 caratteri, l’importazione non riesce. |
| `store_view_code` | Identifica le visualizzazioni specifiche dello store in cui il prodotto è disponibile. Se questo campo viene lasciato vuoto, il prodotto sarà disponibile nella visualizzazione predefinita del Negozio. Ad esempio: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Assegna il prodotto a una serie di attributi o a un modello di prodotto specifici, in base al tipo di prodotto. Una volta creato il prodotto, il set di attributi non può essere modificato. Ad esempio: `default` |
| `product_type` | Indica il tipo di prodotto. Valori:<br/>`simple` — Oggetti materiali di solito venduti in unità singole o in quantità fisse.<br/>`grouped` — Gruppo di prodotti distinti venduti come set.<br/>`configurable` — un prodotto con più opzioni che il cliente deve selezionare prima di effettuare un acquisto. L&#39;inventario può essere gestito per ogni set di varianti perché rappresenta un prodotto separato con una SKU distinta. Ad esempio, una combinazione di colore e dimensioni per un prodotto configurabile è associata a una SKU specifica nel catalogo.<br/>`virtual` — Un prodotto non tangibile che non richiede spedizione e non è conservato in magazzino. Alcuni esempi includono servizi, appartenenze e abbonamenti.<br/>`bundle` — Un set di prodotti personalizzabili di prodotti semplici venduti insieme. |
| `categories` | Indica ogni categoria assegnata al prodotto. Separa le categorie e le sottocategorie con una barra. Per indicare più percorsi di categoria, separare ogni percorso con una barra verticale | simbolo. Ad esempio: `Default Category/Gear&#124;Default Category/Gear/Bags` |
| `product_websites` | Il codice del sito web di ciascun sito web in cui il prodotto è disponibile. Un singolo prodotto può essere assegnato a più siti web o limitato a uno solo. Se si specificano più siti Web, separarli con una virgola e senza spazi. Ad esempio: `base` o `base,website2` |
| `name` | Il nome del prodotto viene visualizzato in tutti gli elenchi di prodotti e corrisponde al nome utilizzato dai clienti per identificare il prodotto. |
| `description` | La descrizione del prodotto fornisce informazioni dettagliate sul prodotto e potrebbe includere semplici tag HTML. |
| `short_description` | L’utilizzo della breve descrizione del prodotto dipende dal tema. Può apparire negli elenchi dei prodotti e a volte viene utilizzato negli elenchi dei feed RSS inviati ai siti di acquisto. |
| `weight` | Peso del singolo prodotto. Il peso effettivo del prodotto è determinato dal vettore al momento della spedizione. |
| product_online | Determina se il prodotto è disponibile per la vendita nel negozio. Valori:<br/>`1` — (Sì) Il prodotto è abilitato e disponibile per la vendita.<br/>`2` — (No) Il prodotto è disabilitato e non è disponibile per la vendita. |
| `tax_class_name` | Nome della classe fiscale associata al prodotto. |
| `visibility` | Determina se il prodotto è visibile nel catalogo e reso disponibile per la ricerca. Valori:<br/>`Not Visible Individually` — Il prodotto non è incluso negli elenchi di prodotti, anche se potrebbe essere disponibile come variante di un altro prodotto.<br/>`Catalog` — Il prodotto viene visualizzato in tutte le voci del catalogo.<br/>`Search` - Il prodotto è disponibile per le operazioni di ricerca.<br/>`Catalog, Search` — Il prodotto è incluso nelle inserzioni del catalogo ed è disponibile anche per la ricerca. |
| `price` | Il prezzo al quale il prodotto è offerto in vendita nel tuo negozio. |
| `special_price` | Il prezzo scontato del prodotto durante l’intervallo di date specificato. |
| `special_price_from_date` | Data di inizio del periodo di tempo in cui è in vigore il prezzo speciale. |
| `special_price_to_date` | L&#39;ultima data del periodo di tempo in cui è in vigore il prezzo speciale. |
| `url_key` | La parte dell’URL che identifica il prodotto. Il valore predefinito è basato sul nome del prodotto. Ad esempio: `product-name` |
| save_rewrites_history | Se fornito con valore `1` con un nuovo `url_key`, viene generato un nuovo URL 301 riscritto in modo che il vecchio URL venga reindirizzato al nuovo URL. |
| `meta_title` | Il metatitolo viene visualizzato nella barra del titolo e nella scheda del browser e degli elenchi dei risultati della ricerca. Il metatitolo deve essere univoco per il prodotto, contenere parole chiave di alto valore e contenere meno di 70 caratteri. |
| `meta_keywords` | Le parole chiave meta sono visibili solo ai motori di ricerca e vengono ignorate da alcuni motori di ricerca. Scegli parole chiave di valore elevato, separate da una virgola. Ad esempio: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | Le metadescrizioni forniscono una breve panoramica del prodotto per l’elenco dei risultati di ricerca. Idealmente, una metadescrizione dovrebbe avere una lunghezza compresa tra 150 e 160 caratteri, anche se il campo accetta fino a 255 caratteri. |
| `base_image` | Percorso relativo per l’immagine principale nella pagina del prodotto. I file vengono archiviati internamente in una struttura di cartelle alfabetiche. Puoi visualizzare la posizione esatta di ogni immagine nei dati esportati. Ad esempio: `/sample_data/m/b/mb01-blue-0.jpg`<br/>Per caricare una nuova immagine o sovrascrivere un&#39;immagine esistente, immettere il nome del file preceduto da una barra. Ad esempio: `/image.jpg` |
| `base_image_label` | Etichetta associata all&#39;immagine di base. |
| `small_image` | Il nome file della piccola immagine utilizzata nelle pagine del catalogo, preceduto da una barra. Ad esempio: `/image.jpg` |
| `small_image_label` | Etichetta associata all&#39;immagine piccola. Ad esempio: `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | Nomi dei file di qualsiasi miniatura da visualizzare nella raccolta nella pagina del prodotto, preceduti da una barra. Ad esempio: `/image.jpg` |
| `thumbnail_image_label` | Etichetta associata alle miniature. Ad esempio: `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | Indica la data di creazione del prodotto. La data viene generata automaticamente al momento della creazione del prodotto, ma può essere modificata in un secondo momento. |
| `updated_at` | Indica la data dell’ultimo aggiornamento del prodotto. |
| `new_from_date` | Specifica la data di inizio per i nuovi elenchi di prodotti e determina se il prodotto viene presentato come un nuovo prodotto. |
| `new_to_date` | Specifica la data &quot;a&quot; per i nuovi elenchi di prodotti e determina se il prodotto viene presentato come un nuovo prodotto. |
| `display_product_options_in` | Se il prodotto dispone di più opzioni, determina dove vengono visualizzate nella pagina del prodotto. Valori: Colonna informazioni prodotto/Blocca dopo Colonna informazioni |
| `map_price` | Il prezzo minimo pubblicizzato del prodotto. (Viene visualizzato solo se MAP è abilitato.) |
| `msrp_price` | Il prezzo al dettaglio consigliato dal produttore per il prodotto. (Viene visualizzato solo se MAP è abilitato.) |
| `map_enabled` | Determina se il prezzo minimo annunciato è abilitato nella configurazione. Valori:<br/>`1` — (Sì) MAP è abilitato.<br/>`0` (o vuoto) - (No) MAP non è abilitato. |
| `gift_message_available` | Determina se un messaggio regalo può essere incluso nell&#39;acquisto del prodotto. Valori:<br/>`1` — (Sì) L&#39;opzione di includere un messaggio regalo viene presentata al cliente.<br/>`0` (o vuoto) - (No) L&#39;opzione per includere un messaggio regalo non viene presentata al cliente. |
| `custom_design` | Elenca i temi disponibili che possono essere applicati alla pagina del prodotto. |
| `custom_design_from` | Specifica la data di inizio in cui il tema selezionato viene applicato alla pagina prodotto. |
| `custom_design_to` | Specifica la data di fine in cui il tema selezionato viene applicato alla pagina prodotto. |
| `custom_layout_update` | Codice XML aggiuntivo applicato come aggiornamento del layout alla pagina di prodotto. |
| `page_layout` | Determina il layout di pagina della pagina prodotto. Valori:<br/>`No layout updates` — Non viene apportata alcuna modifica al layout della pagina.<br/>`1 column` — Applica un layout a una colonna alla pagina di prodotto.<br/>`2 columns with left bar` — Applica un layout a due colonne con barra laterale a sinistra alla pagina del prodotto.<br/>`2 columns with right bar` — Applica un layout a due colonne con barra laterale a destra alla pagina del prodotto.<br/>`3 columns` — Applica un layout a tre colonne alla pagina di prodotto.<br/>`empty` — Applica un layout vuoto alla pagina del prodotto. |
| `product_options_container` | Se il prodotto dispone di più opzioni, determina dove vengono visualizzate nella pagina del prodotto. Valori: Colonna informazioni prodotto/Blocca dopo Colonna informazioni |
| `msrp_display_actual_price_type` | Determina dove il prezzo effettivo di un prodotto è visibile al cliente. Valori:<br/>`In Cart` — visualizza il prezzo effettivo del prodotto nel carrello.<br/>`Before Order Confirmation` — visualizza il prezzo effettivo del prodotto al termine del processo di pagamento, immediatamente prima della conferma dell&#39;ordine.<br/>`On Gesture` — visualizza il prezzo effettivo del prodotto in un popup quando il cliente fa clic sul _Fare clic per visualizzare il prezzo_ o _Cos&#39;è questo?_ collegamento. |
| `country_of_manufacture` | Identifica il paese in cui il prodotto è stato fabbricato. |
| `additional_attributes` | Attributi aggiuntivi creati per il prodotto. Ad esempio: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | Quantità del prodotto attualmente in magazzino. |
| `out_of_stock_qty` | Livello di stock che determina l&#39;esaurimento del prodotto. |
| `use_config_min_qty` | Determina se viene utilizzato il valore predefinito della configurazione e corrisponde alla casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì) Per il valore di questo attributo viene utilizzata l&#39;impostazione di configurazione predefinita.<br/>`0` (o vuoto) — (No) La configurazione predefinita può essere ignorata per il valore di questo attributo. |
| `is_qty_decimal` | Determina se l&#39;attributo qty ha un valore decimale. Valori:<br/>`1` — (Sì) Il valore dell&#39;attributo qty è un valore decimale.<br/>`0` (o vuoto) - (No) Il valore dell&#39;attributo qty è un numero intero (numero intero). |
| `allow_backorders` | Determina se lo store consente gli ordini inevasi e come vengono gestiti. |
| `use_config_backorders` | Determina se viene utilizzata l&#39;impostazione di configurazione predefinita per gli ordini inevasi e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì) Il valore dell&#39;attributo qty è un valore decimale.<br/>`0` (o vuoto) - (No) Il valore dell&#39;attributo qty è un numero intero (numero intero). |
| `min_cart_qty` | Specifica la quantità minima dell&#39;articolo che può essere acquistato in un singolo ordine. |
| `use_config_min_sale_qty` | Determina se viene utilizzata l&#39;impostazione di configurazione predefinita per la quantità minima e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì)<br/>`0` (o in bianco) — (No) |
| `max_cart_qty` | Specifica la quantità massima del prodotto che può essere acquistata in un singolo ordine. |
| `use_config_max_sale_qty` | Determina se viene utilizzata l&#39;impostazione di configurazione predefinita per la quantità massima e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì)<br/>`0` (o in bianco) — (No) |
| `is_in_stock` | Indica se il prodotto è in magazzino. |
| `notify_on_stock_below` | Specifica il livello di stock che attiva un _esaurito_ notifica. |
| `use_config_notify_stock_qty` | Determina se l&#39;impostazione di configurazione predefinita viene utilizzata per attivare la notifica a livello di stock e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì)<br/>`0` (o in bianco) — (No) |
| `manage_stock` | Determina se il controllo dell&#39;inventario viene utilizzato per gestire il prodotto. Valori:<br/>`1` — (Sì) Attiva il controllo completo dell&#39;inventario per gestire i livelli delle scorte del prodotto.<br/>`0` (o vuoto) — (No) Il sistema non tiene traccia del numero di articoli attualmente in magazzino. |
| `use_config_manage_stock` | Determina se viene utilizzata l&#39;impostazione di configurazione predefinita per la gestione del materiale e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì)<br/>`0` (o in bianco) — (No) |
| `use_config_qty_increments` | Determina se viene utilizzata l&#39;impostazione di configurazione predefinita per gli incrementi di quantità e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì)<br/>`0` (o in bianco) — (No) |
| `qty_increments` | Stabilisce il numero di prodotti che compongono un incremento di quantità. |
| `use_config_enable_qty_inc` | Determina se viene utilizzata l&#39;impostazione di configurazione predefinita per abilitare gli incrementi di quantità e corrisponde allo stato della casella di controllo Usa impostazioni di configurazione. Valori:<br/>`1` — (Sì)<br/>`0` (o in bianco) — (No) |
| `enable_qty_increments` | Determina se gli incrementi di quantità sono abilitati per il prodotto. |
| `is_decimal_divided` | Determina se le parti del prodotto possono essere spedite separatamente. Opzioni: `Yes` / `No` |
| `website_id` | Per le installazioni con più siti web, identifica un sito web specifico in cui il prodotto è disponibile. Se vuoto, il prodotto è disponibile in tutti i siti web. |
| `related_skus` | Elenca lo SKU di ciascun prodotto identificato come prodotto correlato. Ad esempio: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Determina la posizione (ordinamento) degli SKU elencati come Prodotti correlati nella colonna related_skus. Ad esempio: `1,2,3,4` |
| `crosssell_skus` | Elenca lo SKU di ciascun prodotto identificato come cross-selling. |
| `crosssell_position` | Determina la posizione (ordinamento) degli SKU elencati come Prodotti di cross-selling in `crosssell_skus` colonna. |
| `upsell_skus` | Elenca lo SKU di ciascun prodotto identificato come upselling. |
| `upsell_position` | Determina la posizione (ordinamento) degli SKU elencati come prodotti di upselling in `upsell_skus` colonna. |
| `additional_images` | I nomi dei file di qualsiasi immagine aggiuntiva da associare al prodotto, preceduti da una barra. Ad esempio: `/image.jpg` |
| `additional_image_labels` | Etichette associate a eventuali immagini aggiuntive. Ad esempio: `Label 1`, `Label 2` |
| `custom_options` | Specifica le proprietà e i valori assegnati a ciascuna opzione personalizzata. Ad esempio: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Dati del servizio per le varianti di prodotto

| Attributo | Descrizione | Applicabile a |
|--- |--- | --- |
| `_super_products_sku` | SKU generata per una variante di prodotto configurabile. Ad esempio: WB03-XS-Green | Prodotti configurabili |
| `_super_attribute_code` | Il codice attributo di una variante di prodotto configurabile. Ad esempio: color | Prodotti configurabili |
| `_super_attribute_option` | Valore di una variante di prodotto configurabile. Ad esempio: verde | Prodotti configurabili |
| `_super_attribute_price_corr` | Adeguamento di prezzo associato a una variante di prodotto configurabile. | Prodotti configurabili |
| `_associated_sku` | SKU di un prodotto associato a un prodotto raggruppato. | Prodotti Raggruppati <br/>Prodotti del bundle |
| `_associated_default_qty` | Determina la quantità del prodotto associato incluso. | Prodotti configurabili<br/>Prodotti Raggruppati<br/>Prodotti del bundle |
| `_associated_position` | Determina la posizione del prodotto associato quando viene elencato con altri prodotti associati. | Prodotti configurabili<br/>Prodotti Raggruppati<br/>Prodotti del bundle |

{style="table-layout:auto"}

## Attributi complessi dei dati del prodotto

Il termine dati complessi si riferisce ai dati associati a più opzioni di prodotto. I seguenti tipi di prodotto utilizzano dati provenienti da prodotti separati per creare varianti di prodotto e più opzioni.

- [Configurabile](../catalog/product-create-configurable.md)
- [Raggruppato](../catalog/product-create-grouped.md)
- [Bundle](../catalog/product-create-bundle.md)

Se esportate un prodotto configurabile, troverete gli attributi standard che compongono un prodotto semplice, oltre agli attributi aggiuntivi necessari per gestire dati complessi.

![Prodotto configurabile: dati esportati](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Prodotti configurabili

| Attributo | Descrizione |
|--- |--- |
| `configurable_variation_labels` | Etichette che identificano le varianti di prodotto. Ad esempio: `Choose Color:` o `Choose Size:` |
| `configurable_variations` | Descrive i valori associati a una variante di prodotto. Ad esempio: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Prodotti raggruppati

| Attributo | Descrizione |
|--- |--- |
| `associated_skus` | Identifica gli SKU dei singoli prodotti che compongono il gruppo. |

{style="table-layout:auto"}

### Prodotti bundle

| Attributo | Descrizione |
|--- |--- |
| `bundle_price_type` | Determina se il prezzo di un articolo bundle è fisso o dinamico. |
| `bundle_sku_type` | Determina se a ogni elemento viene assegnato uno SKU dinamico, variabile o se per il bundle viene utilizzato uno SKU fisso. Opzioni: Fisso / Dinamico |
| `bundle_weight_type` | Determina se il peso di un elemento bundle è variabile o fisso. |
| `bundle_values` | Descrive il valore di apprendimento associato a un’opzione bundle. Ad esempio: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Attributi di determinazione prezzi avanzati

Advanced Price Import/Export consente di aggiornare rapidamente le informazioni sui prezzi per gruppi di prodotti e prezzi di livello. Il processo per [importa](data-import.md) e [esportare](data-export.md) i dati di prezzo avanzati sono identici a quelli di qualsiasi altro tipo di entità. Il file CSV di esempio contiene i prezzi di livello e gruppo per ciascun tipo di prodotto che supporta prezzi avanzati. La modifica del prezzo avanzato non influisce sul resto del record del prodotto.

![Esempio di dati di esportazione - prezzi avanzati](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Attributo | Descrizione |
|--- |--- |
| `sku` | (Obbligatorio) L’unità di gestione delle scorte è un identificatore alfanumerico univoco utilizzato per tenere traccia delle scorte. Una SKU può contenere fino a 64 caratteri. Ad esempio: `sku123`<br/>**_Nota:_**Se lo SKU supera i 64 caratteri, l’importazione non riesce. |
| `tier_price_website` | Il [codice del sito web](../stores-purchase/stores.md#add-websites) identifica ogni sito Web in cui è disponibile il piano tariffario. Ad esempio: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Identifica il [gruppi di clienti](../customers/customer-groups.md) dove è disponibile il piano tariffario. Ad esempio: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Identifica i gruppi di clienti in cui è disponibile la determinazione dei prezzi per livello. Ad esempio: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | Quantità del prodotto che deve essere ordinata per ricevere lo sconto sul prezzo del livello. |
| `tier_price` | Prezzo di livello scontato del prodotto. Per [prodotti bundle](../catalog/product-create-bundle.md), il prezzo livello viene calcolato come percentuale. |
| `group_price_website` | Il [codice del sito web](../stores-purchase/stores.md#add-websites) di ciascun sito web in cui è disponibile la determinazione dei prezzi di gruppo. Se si specificano più siti Web, separarli con una virgola e senza spazi. Ad esempio: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Identifica i gruppi dei clienti in cui è disponibile il prezzo di gruppo. Ad esempio: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | Il prezzo di gruppo scontato del prodotto. Per [prodotti bundle](../catalog/product-create-bundle.md), il prezzo di gruppo è calcolato come percentuale. |

{style="table-layout:auto"}
