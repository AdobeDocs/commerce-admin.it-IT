---
title: Documenti di vendita
description: Scopri come configurare i documenti di vendita per supportare gli ordini dei clienti e l’evasione per il tuo negozio Commerce.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Documenti di vendita

Per supportare il flusso di lavoro dell&#39;ordine e fornire ai clienti la documentazione relativa agli ordini inviati, configurare i documenti di vendita correlati in modo che riflettano il marchio del negozio e includere informazioni di riferimento.

## Configura fatture e documenti di trasporto

A differenza delle immagini del logo utilizzate nelle pagine di vetrina, il logo per le fatture dei PDF e altri documenti di vendita può essere un&#39;immagine ad alta risoluzione di 300 dpi. Prestare attenzione a mantenere le proporzioni quando si ridimensiona il logo. Ridimensionare il logo in modo che si adatti all&#39;altezza e non preoccuparsi di eventuali spazi inutilizzati a destra.

![Logo di esempio](./assets/logo-pdf.png){width="200"}

Un modo per ridimensionare il logo per adattarlo alle dimensioni richieste consiste nel creare una nuova immagine vuota con le dimensioni corrette. Quindi, incolla l’immagine del logo e ridimensionala per adattarla all’altezza. Nella maggior parte dei programmi di modifica delle immagini, è possibile ridimensionarla in base a una percentuale per mantenere le proporzioni oppure tenere premuto il tasto Maiusc e ridimensionare manualmente l&#39;immagine.

**_Per aggiornare il logo:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Invoice and Packing Slip Design]** ed effettuare le seguenti operazioni:

   ![Configurazione vendite - fattura di vendita e documento di trasporto](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Per caricare **[!UICONTROL Logo for PDF Print-outs]**, fare clic su **[!UICONTROL Choose File]**, trovare il logo preparato e fare clic su **[!UICONTROL Open]**.

   - Per caricare **[!UICONTROL Logo for HTML Print View]**, fare clic su **[!UICONTROL Choose File]**, trovare il logo preparato e fare clic su **[!UICONTROL Open]**.

   - Inserire l&#39;indirizzo desiderato nelle fatture e nei documenti di trasporto.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

   Per riferimento, prima di ogni campo viene visualizzata una miniatura dell’immagine caricata. Non preoccuparti se la miniatura appare distorta. La proporzione del logo è corretta sulla fattura.

### Sostituire un&#39;immagine

1. Fare clic su **[!UICONTROL Choose File]** e scegliere un altro file del logo.

1. Selezionare la casella di controllo **[!UICONTROL Delete Image]** per l&#39;immagine da sostituire.

1. Fare clic su **[!UICONTROL Save Config]**.

### Formati immagine

| Formato | Requisiti |
|--- |------------------------------------------|
| **_PDF_** |  |
| Formato file | JPG-JPEG, PNG, TIF (TIFF) |
| Dimensioni immagine | Fino a 1080 pixel di larghezza x 270 pixel di altezza |
| Risoluzione | 300 DPI consigliati |
| **_HTML_** |  |
| Formato file | JPG-JPEG, PNG, GIF |
| Dimensioni immagine | Determinato dal tema. |
| Risoluzione | 72 o 96 DPI |

{style="table-layout:auto"}

## Aggiungi ID di riferimento

L&#39;ID ordine e l&#39;indirizzo IP del cliente possono essere inclusi nell&#39;intestazione dei documenti di vendita che accompagnano un ordine. Per impostazione predefinita, sia l&#39;ID ordine che l&#39;indirizzo IP del cliente vengono visualizzati nell&#39;intestazione delle fatture, dei documenti di trasporto della spedizione e delle note di accredito.

![Configurazione vendite - Stampati PDF](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_Per modificare l&#39;impostazione dell&#39;ID ordine:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL PDF Print-outs]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **Fattura**.

1. Imposta **[!UICONTROL Display Order ID in Header]** in base alle tue preferenze.

1. Ripetere per le sezioni **[!UICONTROL Shipment]** e **[!UICONTROL Credit Memo]**.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

**_Per modificare l&#39;impostazione dell&#39;indirizzo IP del cliente:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General]**.

   ![Configurazione vendite - Impostazioni generali vendite](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Hide Customer IP]** sulla tua preferenza.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
