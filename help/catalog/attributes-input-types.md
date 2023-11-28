---
title: Tipi di input degli attributi
description: Scopri i tipi di input disponibili per gli attributi del prodotto, che determinano il tipo di dati che possono essere immessi e il formato del campo o del controllo di input.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Tipi di input degli attributi

Quando vengono visualizzati dall’amministratore, gli attributi sono i campi che completi quando crei un prodotto. Il tipo di input assegnato a un attributo determina il tipo di dati che è possibile immettere e il formato del campo o del controllo di input. Dal punto di vista del cliente, gli attributi forniscono informazioni sul prodotto e sono le opzioni e i campi di immissione dati che devono essere completati per acquistare un prodotto.

## Tipi di input

| Proprietà | Descrizione |
|--- |--- |
| [!UICONTROL Text Field] | Campo di input a riga singola per il testo. |
| [!UICONTROL Text Area] | Campo di input a più righe per l&#39;immissione di paragrafi di testo, ad esempio la descrizione di un prodotto. È possibile utilizzare l&#39;editor WYSIWYG per formattare il testo con tag HTML o immettere i tag direttamente nel testo. |
| [!UICONTROL Text Editor] | Un editor di testo perfettamente funzionante nella posizione dell’attributo. |
| [!UICONTROL Date] | Visualizza un valore di data nel [formato preferito](#date-and-time-options) e [fuso orario](../getting-started/store-details.md#locale-options). I valori di data possono essere selezionati da un elenco o da un calendario ( ![Icona Calendario](../assets/icon-calendar.png) ). <br/><br/>**_Nota:_**A seconda della configurazione del sistema,_Amministratore _gli utenti possono immettere le date direttamente in un campo o selezionare una data dal calendario o dall’elenco. Per informazioni su come specificare i valori di data e ora, vedere [Opzioni data e ora](#date-and-time-options). |
| [!UICONTROL Date and Time] | Visualizza un valore di data e ora in [formato preferito](#date-and-time-options) e [fuso orario](../getting-started/store-details.md#locale-options). La data e l’ora possono essere immesse manualmente o selezionate da un calendario. Esempio di formato: MM/GG/AAAA HH:MM |
| [!UICONTROL Yes/No] | Visualizza un elenco a discesa con opzioni predefinite di `Yes` e `No`. |
| A discesa | Visualizza un elenco a discesa di valori che accetta una sola selezione. Il tipo di input a discesa è un componente chiave di [prodotti configurabili](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Visualizza un elenco a discesa di valori che accetta selezioni multiple. |
| [!UICONTROL Price] | Questo tipo di input viene utilizzato per creare campi prezzo che si aggiungono agli attributi predefiniti: `Price`, `Special Price`, `Tier Price`, e `Cost`. La valuta utilizzata è determinata dalla configurazione del sistema. |
| [!UICONTROL Media Image] | Associa un&#39;immagine aggiuntiva a un prodotto, ad esempio il logo di un prodotto, le istruzioni per la cura o gli ingredienti di un&#39;etichetta di cibo. Quando aggiungi un attributo di immagine multimediale al set di attributi di un prodotto, questo diventa un tipo di immagine aggiuntivo, insieme a Base, Piccola e Miniatura. L’attributo dell’immagine multimediale può essere escluso dal [browser multimediale storefront](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Consente di definire [Percentuali FPT](../stores-purchase/fixed-product-tax.md) in base ai requisiti della lingua. |
| [!UICONTROL Visual Swatch] | Visualizza un campione che rappresenta il colore, la trama o il motivo di un prodotto configurabile. A [campione visivo](swatches.md) può essere riempita con un valore di colore esadecimale, oppure può visualizzare un’immagine caricata che rappresenta il colore, il materiale, la trama o il pattern dell’opzione. |
| [!UICONTROL Text Swatch] | Rappresentazione testuale di un’opzione di prodotto configurabile utilizzata di frequente per le dimensioni. [Campioni di testo](swatches.md) può includere anche valori esadecimali dei colori. |
| [!UICONTROL Page Builder] | A [[!DNL Page Builder]](../page-builder/workspace.md) nella posizione dell’attributo, per aggiungere facilmente contenuti coinvolgenti alla pagina del prodotto. |

{style="table-layout:auto"}

## Opzioni data e ora

È possibile personalizzare il formato dei campi di data e ora e selezionare il controllo di input utilizzato per l&#39;immissione dei dati. I valori delle date possono essere selezionati da un elenco a discesa o da un calendario popup.

![Esempio: calendario popup storefront](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_Per formattare i campi data/ora:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e fai clic su **[!UICONTROL Catalog]** elemento secondario.

1. Espandi **[!UICONTROL Date & Time Custom Options]** sezione.

   ![Configurazione del catalogo - Opzioni data e ora](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [_Opzioni personalizzate data e ora_](../configuration-reference/catalog/catalog.md) nel _Riferimento configurazione_.

1. Per utilizzare un calendario popup come controllo di input per i campi data, impostare **[!UICONTROL Use JavaScript Calendar]** a `Yes`.

1. Per stabilire **[!UICONTROL Date Fields Order]**, impostare l&#39;ordine di ogni parte del campo data in base alle esigenze:

   - Mese
   - Giorno
   - Anno

1. Per impostare il formato di ora desiderato, impostare **Formato ora** a uno dei seguenti elementi:

   - `12h AM/PM`
   - `24h`

1. Per stabilire **[!UICONTROL Year Range]** per i valori dell&#39;elenco a discesa, immettere l&#39;anno (AAAA) per impostare **[!UICONTROL from]** e **[!UICONTROL to]** date.

   Se questo campo viene lasciato vuoto, verrà utilizzato automaticamente l&#39;anno corrente.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
