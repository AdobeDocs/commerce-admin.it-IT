---
title: Elenco prodotti
description: Scopri come modificare la configurazione dell’elenco dei prodotti, che determina quanti prodotti vengono visualizzati per pagina e quale attributo viene utilizzato per ordinare l’elenco.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Elenco prodotti

Gli elenchi di prodotti possono essere impostati in modo da essere visualizzati per impostazione predefinita come elenco o griglia. Puoi anche determinare quanti prodotti vengono visualizzati per pagina e quale attributo viene utilizzato per ordinare l’elenco. L&#39;elenco dei prodotti include un set di controlli che è possibile utilizzare per ordinare i prodotti, modificare il formato dell&#39;elenco, ordinare per attributo e passare da una pagina all&#39;altra.

>[!NOTE]
>
>Quando si ordina una categoria in base a un attributo di prodotto, anche i prodotti con gli stessi valori di attributo vengono ordinati in base al rispettivo _[!UICONTROL Product ID]_&#x200B;in ordine crescente.

![Prodotti visualizzati come griglia](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Configurare gli elenchi di prodotti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Storefront]**.

   ![Opzioni di configurazione vetrina](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Storefront](../configuration-reference/catalog/catalog.md#storefront) nel _Riferimento configurazione_.

   >[!NOTE]
   >
   >Per visualizzare correttamente i prodotti e i relativi prezzi in base a _ordinamento dei prodotti in base al prezzo_, assicurarsi che le impostazioni per la visualizzazione del prezzo nella [configurazione IVA](../configuration-reference/sales/tax.md) abbiano lo stesso valore (`Excluding Tax` **o** `Including Tax`). Per _[!UICONTROL Calculation Settings]_, controlla il valore **[!UICONTROL Catalog Prices]**. E per&#x200B;_[!UICONTROL Price Display Settings]_, controlla il valore **[!UICONTROL Display Product Prices in Catalog]**. Se questi hanno valori diversi, i filtri dei prezzi nella navigazione a livelli potrebbero non filtrare e ordinare correttamente i prodotti in base al prezzo.

1. Impostare **[!UICONTROL List Mode]** predefinito su uno dei seguenti valori:

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. Per **[!UICONTROL Products per Page on Grid Allowed Values]**, immettere il numero di prodotti che si desidera visualizzare per pagina quando viene visualizzato in formato griglia.

   Per immettere una selezione di valori, separa ogni numero con una virgola.

1. Per **[!UICONTROL Products per Page on Grid Default Value]**, immettere il numero predefinito di prodotti da visualizzare nella griglia per pagina.

1. Per **[!UICONTROL Products per Page on List Allowed Values]**, immettere il numero di prodotti che si desidera visualizzare per pagina quando viene visualizzato in formato elenco.

   Per immettere una selezione di valori, separa ogni numero con una virgola.

1. Per **[!UICONTROL Products per page on List Default Value]**, immettere il numero predefinito di prodotti visualizzati nell&#39;elenco, per pagina.

1. Impostare **[!UICONTROL Product Listing Sorted by]** sull&#39;attributo predefinito utilizzato inizialmente per ordinare l&#39;elenco.

1. Per consentire ai clienti di elencare tutti i prodotti, impostare **[!UICONTROL Allow All Products on Page]** su `Yes`.

1. Se si desidera mantenere tutte le impostazioni di impaginazione mentre i clienti sfogliano le voci di catalogo, impostare **[!UICONTROL Remember Category Pagination]** su `Yes`.

   L’abilitazione di questa impostazione garantisce che il numero di prodotti visualizzati in un elenco o in una griglia venga mantenuto durante la navigazione da una categoria all’altra. Per impostazione predefinita, questo campo è impostato su `No` perché utilizza più spazio di archiviazione nella cache e può influire sul modo in cui le pagine vengono indicizzate dai motori di ricerca.

1. Se si utilizza un [catalogo flat](catalog-flat.md) (**non consigliato**), eseguire le operazioni seguenti:

   - Per visualizzare un elenco di categorie piatte di prodotti, impostare **[!UICONTROL Use Flat Catalog Category]** su `Yes`.

   - Per visualizzare un elenco di prodotti flat, impostare **[!UICONTROL Use Flat Catalog Product]** su `Yes`.

1. Per consentire riferimenti dinamici per le risorse multimediali negli URL di categorie e prodotti, impostare **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Controlli pagina

| Controllo | Descrizione |
|--- |--- |
| [!UICONTROL View As] | Visualizza i prodotti in formato griglia o elenco. |
| [!UICONTROL Sort By] | Modifica l&#39;ordinamento dell&#39;elenco. |
| [!UICONTROL Show Per Page] | Determina quanti prodotti vengono visualizzati per pagina. |
| Collegamenti di impaginazione | Collegamenti ad altre pagine. |

{style="table-layout:auto"}

## Controlli di impaginazione

Le impostazioni di impaginazione vengono visualizzate nella parte superiore e inferiore dell’elenco e controllano il formato dei collegamenti di impaginazione per gli elenchi di prodotti. È possibile impostare il numero di collegamenti visualizzati nel controllo e configurare i collegamenti Successivo e Precedente. Affinché i collegamenti di impaginazione vengano visualizzati, l’elenco deve contenere più prodotti di quanto consentito per pagina nella configurazione dell’elenco dei prodotti.

![Controlli di impaginazione](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Controlli di paginazione della vetrina

| Controllo | Descrizione |
|--- |--- |
| ![Visualizza griglia](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Visualizza l&#39;elenco in formato Griglia o Elenco. |
| ![Ordina per](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Modifica l&#39;ordinamento dell&#39;elenco. La proprietà vetrina _[!UICONTROL Used for Sorting in Product Listing]_&#x200B;determina quali [attributi di prodotto](../catalog/product-attributes.md) possono essere utilizzati per ordinare l&#39;elenco. |
| ![Mostra per pagina](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - Determina quanti prodotti vengono visualizzati per pagina. |
| ![Collegamenti di paginazione](./assets/control-pagination.png) | Collegamenti di impaginazione - Collegamenti di navigazione ad altre pagine. |

{style="table-layout:auto"}

### Configurare i controlli di impaginazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione archivio che si desidera configurare e nella colonna **[!UICONTROL Action]** fare clic su **[!UICONTROL Edit]**.

1. In **[!UICONTROL Other Settings]**, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Pagination]**.

   ![Paginazione](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su queste impostazioni, vedere [Configurazione progettazione](../content-design/configuration.md).

1. Per **[!UICONTROL Pagination Frame]**, immettere il numero di collegamenti che si desidera visualizzare nel controllo di impaginazione.

1. Per **[!UICONTROL Pagination Frame Skip]**, immettere il numero di collegamenti che si desidera ignorare prima di visualizzare il successivo gruppo di collegamenti nel controllo di impaginazione.

   Ad esempio, se la cornice di impaginazione contiene cinque collegamenti e desiderate passare ai cinque collegamenti successivi, quanti collegamenti desiderate ignorare? Se si imposta il valore su quattro (`4`), l&#39;ultimo collegamento del set precedente sarà il primo del set successivo.

1. Per **[!UICONTROL Anchor Text for Previous]**, immettere il testo che si desidera visualizzare per il collegamento Precedente.

   Lasciate vuoto per usare la freccia di default.

1. Per **[!UICONTROL Anchor Text for Next]**, immettere il testo che si desidera visualizzare per il collegamento Successivo. Lasciate vuoto per usare la freccia di default.

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.
