---
title: Elenco prodotti
description: Scopri il _[!UICONTROL Products]_ in Admin, dove puoi creare prodotti e modificarne di esistenti.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Elenco prodotti

Tutti i prodotti del catalogo sono accessibili da _[!UICONTROL Products]_in Admin, dove puoi creare prodotti e modificare quelli esistenti. Per un&#39;installazione multisito, ogni sito Web può offrire una selezione diversa di prodotti in vendita dallo stesso catalogo.

Il _[!UICONTROL Products]_L&#39;elenco include tutti i prodotti nel catalogo, indica i siti Web in cui sono disponibili e se sono attualmente abilitati per la vendita. Nelle installazioni B2B di Adobe Commerce con [cataloghi condivisi](../b2b/catalog-shared.md) abilitata, la griglia include una colonna che indica quali prodotti hanno prezzi di sconto alternativi in un catalogo condiviso.

Puoi sfogliare l’elenco pagina per pagina, oppure cercare prodotti specifici. Utilizza lo standard [controlli](../getting-started/admin-grid-controls.md) per ordinare e filtrare l’elenco e applicare [azioni](../getting-started/admin-actions-control.md) ai prodotti selezionati.

![Griglia prodotti](./assets/products-grid.png){width="700" zoomable="yes"}

## Limita visualizzazione prodotto

Per migliorare le prestazioni per i cataloghi di grandi dimensioni, si consiglia di limitare il numero di prodotti visualizzati nella griglia. Puoi limitare le griglie di prodotto visualizzate per:

- Pagina prodotti
- Aggiungi prodotti correlati/up-selling/cross-selling
- Aggiungi prodotti al bundle prodotto
- Aggiungi prodotti al prodotto gruppo
- Crea ordine (amministratore)

Questa impostazione di configurazione per la limitazione di visualizzazione del prodotto è disabilitata per impostazione predefinita. Attivandola, puoi limitare il numero di prodotti nella griglia a un valore specifico. Se è abilitata e il numero di prodotti corrispondenti per la visualizzazione della griglia è maggiore del limite di record, viene restituita una raccolta limitata di record. Al raggiungimento del limite, i record totali trovati, il numero di record selezionati e gli elementi di impaginazione non vengono visualizzati nell&#39;intestazione della griglia.

>[!NOTE]
>
>Se non desideri che la griglia di prodotto sia limitata, utilizza i filtri in modo più preciso per produrre una raccolta con meno elementi rispetto al numero specificato in _[!UICONTROL Records Limit]_campo.

**_Per configurare la limitazione di visualizzazione del prodotto:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Admin Grids]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Limit Number of Products in Grid]** a `Yes`.

   - (Facoltativo) Immetti un valore in **[!UICONTROL Records Limit]** per limitare il numero di prodotti nella griglia a un valore specifico. Il valore minimo predefinito è `20000`.

   ![Impostazioni di configurazione di Admin Grids](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Controlli pagina

| Controllo | Descrizione |
|--- |--- |
| [!UICONTROL Add Product] | Avvia il processo di creazione di un nuovo prodotto semplice. Per scegliere un tipo di prodotto specifico, fare clic sulla freccia giù. Opzioni: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Elenca tutte le azioni che possono essere applicate ai prodotti selezionati nell&#39;elenco. Per applicare un’azione a un prodotto o a un gruppo di prodotti, seleziona la casella di controllo nella prima colonna di ciascun prodotto. Opzioni: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Avvia una ricerca nel catalogo in base ai filtri correnti. |
| [!UICONTROL Default View] | Indica il layout corrente delle colonne della griglia. Se sono presenti viste colonne griglia salvate, è possibile sceglierne un&#39;altra. |
| [!UICONTROL Columns] | Elenca tutte le azioni che possono essere applicate ai prodotti selezionati nell&#39;elenco. Per applicare un’azione a un prodotto o a un gruppo di prodotti, seleziona la casella di controllo nella prima colonna di ciascun prodotto. |
| [!UICONTROL Search by keyword] | La casella di ricerca, nell’angolo in alto a sinistra, viene utilizzata per trovare i prodotti per parola chiave. |
| [!UICONTROL Edit] | Apre il prodotto in modalità di modifica. È possibile eseguire la stessa operazione facendo clic in un punto qualsiasi della riga. |

{style="table-layout:auto"}

## Colonne predefinite

| Colonna | Descrizione |
|--- |--- |
| (Casella di controllo) | Seleziona più record da sottoporre a un&#39;azione. La casella di controllo nella prima colonna di ogni record selezionato è contrassegnata. Opzioni: <br/>**[!UICONTROL Select All]**- Seleziona tutti i record trovati che corrispondono alle impostazioni correnti del filtro.<br/>**[!UICONTROL Select All on This Page]** - Seleziona solo i record trovati nella pagina corrente che corrispondono alle impostazioni del filtro. |
| [!UICONTROL ID] | Numero sequenziale univoco assegnato la prima volta che viene salvato un nuovo prodotto. |
| [!UICONTROL Thumbnail] | Visualizza una miniatura dell&#39;immagine principale del prodotto. |
| [!UICONTROL Name] | Il nome del prodotto. |
| [!UICONTROL Type] | Il tipo di prodotto. |
| [!UICONTROL Attribute Set] | Nome del set di attributi utilizzato come modello per il prodotto. |
| [!UICONTROL SKU] | Unità di stoccaggio univoca assegnata al prodotto. |
| [!UICONTROL Price] | Il prezzo unitario del prodotto. |
| [!UICONTROL Quantity] | Quantità in magazzino. |
| [!UICONTROL Salable Quantity] | La somma di tutte le unità disponibili di questo prodotto. |
| [!UICONTROL Visibility] | Indica dove il prodotto è visibile nel catalogo. Opzioni: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Indica lo stato del prodotto. Opzioni: `Enabled` e `Disabled` |
| [!UICONTROL Websites] | Indica i siti Web in cui il prodotto è disponibile. |
| [!UICONTROL Action] | Apre il prodotto in modalità Modifica. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con [Adobe Commerce B2B](./b2b/../introduction.md) Solo per ) Indica i cataloghi condivisi che contengono prezzi personalizzati per il prodotto. |

{style="table-layout:auto"}

## Altre colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Short Description] | Breve descrizione del prodotto. |
| [!UICONTROL Special Price From Date] | La prima data della promozione speciale del prezzo. |
| [!UICONTROL Special Price To Date] | L&#39;ultima data della promozione speciale. |
| [!UICONTROL Cost] | Il costo effettivo dell&#39;articolo. |
| [!UICONTROL Manufacturer] | Il produttore del prodotto. |
| [!UICONTROL Meta Keywords] | Meta parole chiave per il prodotto. |
| [!UICONTROL Color] | Il colore del prodotto. |
| [!UICONTROL Set Product as New from Date] | La prima data del prodotto impostato come nuova promozione. |
| [!UICONTROL Set Product as New to Date] | L&#39;ultima data del prodotto impostato come nuova promozione. |
| [!UICONTROL Active From / To] | Le date di inizio e fine del prodotto. |
| [!UICONTROL Layout] | Il layout del prodotto. |
| [!UICONTROL Minimum Advertised Price] | Il prezzo minimo pubblicizzato del prodotto. |
| [!UICONTROL Allow Gift Message] | Il messaggio regalo per i clienti che acquistano una gift card. |
| [!UICONTROL Special Price] | Prezzo speciale del prodotto. |
| [!UICONTROL Weight] | Il peso del prodotto. |
| [!UICONTROL Meta Title] | Titolo metadati del prodotto. |
| [!UICONTROL Meta Description] | Descrizione dei metadati del prodotto. |
| [!UICONTROL Country of Manufacture] | Il paese di fabbricazione. |
| [!UICONTROL New Theme] | Tema personalizzato applicato al prodotto. |
| [!UICONTROL URL Key] | Chiave URL del prodotto. |
| [!UICONTROL Tax Class] | La classe fiscale del prodotto. |
| [!UICONTROL Allow Gift Message] | Visualizza la disponibilità del messaggio regalo per il prodotto. |

{style="table-layout:auto"}
