---
title: Configurazione dell’immagine del prodotto
description: Scopri come impostare una dimensione massima in pixel (larghezza e altezza) e ridimensionare automaticamente i file immagine del prodotto durante il caricamento.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Configurazione dell’immagine del prodotto

Se si prevede di caricare immagini di grandi dimensioni per la visualizzazione nella pagina _[!UICONTROL Product Details]_, è consigliabile impostare una dimensione massima in pixel (larghezza e altezza) e ridimensionare automaticamente i file al caricamento. Per supportare questo tipo di caricamento di immagini di prodotto, è disponibile un’opzione per abilitare il ridimensionamento automatico di file di immagine di dimensioni maggiori durante il caricamento. Per i prodotti che desideri aggiungere al catalogo ma per i quali non disponi ancora di una risorsa immagine da visualizzare, puoi configurare un’immagine segnaposto.

## Ridimensionamento immagine prodotto

Durante il caricamento delle immagini di prodotto, è possibile aggiungere immagini di dimensioni maggiori con dimensioni diverse per ottenere zoom dettagliati e di alta qualità sulla pagina _[!UICONTROL Product Details]_. Per garantire che tutte le immagini abbiano dimensioni e aspetto simili, è disponibile un’opzione di ridimensionamento per garantire che tutte le immagini corrispondano a una dimensione pixel specifica. Questa opzione ridimensiona automaticamente tutte le immagini del prodotto utilizzando le impostazioni di configurazione, che possono essere utili con le prestazioni di zoom, un caricamento più rapido delle immagini e un aspetto uniforme delle immagini del prodotto.

>[!NOTE]
>
>Per una migliore compatibilità, si consiglia di caricare tutte le immagini del prodotto con il profilo colore `sRGB`. Tutti gli altri profili colore vengono automaticamente convertiti nel profilo colore `sRGB` durante il caricamento dell&#39;immagine del prodotto, il che potrebbe causare incoerenza di colore nell&#39;immagine caricata.

Impostando la larghezza e l&#39;altezza massime in pixel, l&#39;immagine viene ridimensionata in pixel in base alle dimensioni fisiche. Commerce ridimensiona l’immagine in base alla maggiore quantità di larghezza o altezza mantenendo le proporzioni. La riduzione della quantità di qualità per le immagini JPG-riduce le dimensioni del file.

Ad esempio, un JPG-3000 x 2100 pixel al 100% potrebbe essere un file di immagine di dimensioni pari o superiori a 5 MB. Il ridimensionamento di questa immagine ridurrebbe la larghezza a 1920 pixel, mantenendo proporzioni e qualità all&#39;80% per fornire dimensioni di file molto più piccole con alta qualità.

### Abilita ridimensionamento immagine

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _Configurazione caricamento immagini_.

   Per modificare le impostazioni predefinite, deselezionare la casella di controllo **[!UICONTROL Use system value]**, se necessario.

   ![Configurazione caricamento immagine](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste impostazioni di configurazione, vedi [_Configurazione caricamento immagine_](../configuration-reference/advanced/system.md#image-upload-configuration) nel _Riferimento configurazione_.

1. Per attivare, assicurarsi che **[!UICONTROL Enable Frontend Resize]** sia impostato su `Yes`.

1. Immettere un&#39;impostazione **[!UICONTROL Quality]** compresa tra `1` e `100`%.

   Si consiglia un&#39;impostazione tra 80 e 90% per un file di dimensioni ridotte e di alta qualità.

1. Imposta **[!UICONTROL Maximum Width]** in pixel per l&#39;immagine.

   Quando l&#39;immagine viene ridimensionata, non supera questa larghezza e mantiene le proporzioni.

1. Imposta **[!UICONTROL Maximum Height]** in pixel per l&#39;immagine.

   Quando l&#39;immagine viene ridimensionata, non supera questa altezza e mantiene le proporzioni.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Descrizioni dei campi

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Quality] | Globale | Determina la qualità JPG dell&#39;immagine ridimensionata. Una qualità inferiore riduce le dimensioni del file. Si consiglia l&#39;80-90% per ridurre le dimensioni dei file con un&#39;alta qualità. Predefinito: 80 |
| [!UICONTROL Enable Frontend Resize] | Globale | Consente a Commerce di ridimensionare immagini di grandi dimensioni e di dimensioni eccessive che è possibile caricare per la pagina _[!UICONTROL Product Details]_. Commerce ridimensiona i file immagine utilizzando JavaScript durante il caricamento del file. Quando l&#39;immagine viene ridimensionata, mantiene le proporzioni esatte, per soddisfare e non superare le dimensioni massime per Larghezza massima o Altezza massima. Predefinito: `Yes` |
| [!UICONTROL Maximum Width] | Globale | Determina la larghezza massima in pixel dell&#39;immagine. Quando l&#39;immagine viene ridimensionata, non supera questa larghezza. Predefinito: `1920` |
| [!UICONTROL Maximum Height] | Globale | Determina l&#39;altezza massima in pixel dell&#39;immagine. Quando l&#39;immagine viene ridimensionata, non supera questa altezza. Predefinito: `1200` |

{style="table-layout:auto"}

## Segnaposto immagine

Adobe Commerce e il Magento Open Source utilizzano immagini temporanee come segnaposto fino a quando non saranno disponibili le immagini permanenti del prodotto. È possibile caricare un segnaposto diverso per ogni ruolo. L&#39;immagine segnaposto iniziale è un logo di esempio che è possibile sostituire con l&#39;immagine desiderata.

![Segnaposto immagine](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_Per caricare immagini segnaposto:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Icona di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Product Image Placeholders]**.

   ![Segnaposto Immagine Prodotto](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste impostazioni di configurazione, vedi [_Segnaposto immagine prodotto_](../configuration-reference/catalog/catalog.md#product-image-placeholders) nel _Riferimento configurazione_.

1. Per ogni ruolo immagine, fare clic su **[!UICONTROL Choose File]**, trovare l&#39;immagine nel computer e caricare il file.

   È possibile utilizzare la stessa immagine per tutti e tre i ruoli oppure caricare un&#39;immagine segnaposto diversa per ogni ruolo.

1. Al termine, fare clic su **[!UICONTROL Save]**.

Per informazioni sui ruoli immagine e sulle dimensioni consigliate, vedere [Caricare un&#39;immagine](product-image.md#upload-an-image).
