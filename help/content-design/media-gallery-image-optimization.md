---
title: Ottimizzazione immagine di Media Gallery
description: Scopri come utilizzare l'ottimizzazione delle immagini per le  [!DNL Commerce] risorse multimediali.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Ottimizzazione immagine di Media Gallery

La nuova [Galleria file multimediali](media-gallery.md) fornisce una funzionalità di _ottimizzazione immagine_ che migliora le prestazioni e riduce le dimensioni dei file multimediali nella vetrina. Questa ottimizzazione è abilitata per impostazione predefinita e può essere modificata nelle impostazioni di configurazione dell’archivio.

## Configura ottimizzazione immagine

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable Image Optimization]** su `Yes`.
   - Immetti i valori **[!UICONTROL Maximum Width]** e **[!UICONTROL Maximum Height]** (in pixel) in base alle tue esigenze.

## Comportamento

Quando la funzionalità di ottimizzazione immagine di Raccolta multimediale è abilitata, una copia ottimizzata di un&#39;immagine viene inserita automaticamente nel contenuto dalla [Raccolta multimediale](media-gallery.md) al posto del file originale.

Quando i valori _Larghezza massima_ e _Altezza massima_ vengono modificati nella configurazione, vengono aggiornate tutte le immagini ottimizzate esistenti precedentemente inserite.

L&#39;ottimizzazione delle immagini di Media Gallery richiede che i consumer della coda `media.gallery.renditions.update` siano in esecuzione per la rigenerazione delle immagini ottimizzate quando la configurazione viene modificata. Per ulteriori dettagli, vedere [Gestione delle code di messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) nella _Guida alla configurazione_.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
