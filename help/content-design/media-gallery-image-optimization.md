---
title: Ottimizzazione immagine di Media Gallery
description: Scopri come utilizzare l’ottimizzazione delle immagini per [!DNL Commerce] risorse multimediali.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Ottimizzazione immagine di Media Gallery

Il nuovo [Raccolta file multimediali](media-gallery.md) fornisce un _ottimizzazione immagine_ che migliora le prestazioni e riduce le dimensioni dei file multimediali nella vetrina. Questa ottimizzazione è abilitata per impostazione predefinita e può essere modificata nelle impostazioni di configurazione dell’archivio.

## Configura ottimizzazione immagine

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable Image Optimization]** a `Yes`.
   - Inserisci il **[!UICONTROL Maximum Width]** e **[!UICONTROL Maximum Height]** valori (in pixel) in base alle tue esigenze.

## Comportamento

Quando la funzionalità di ottimizzazione immagine di Media Gallery è abilitata, una copia ottimizzata di un’immagine viene inserita automaticamente nel contenuto da [Raccolta file multimediali](media-gallery.md) al posto del file originale.

Quando _Larghezza massima_ e _Altezza massima_ vengono modificati nella configurazione, aggiorna tutte le immagini ottimizzate esistenti che erano state precedentemente inserite.

L’ottimizzazione delle immagini di Media Gallery richiede che il `media.gallery.renditions.update` i consumer di coda sono in esecuzione per la rigenerazione di immagini ottimizzate quando la configurazione viene modificata. Consulta [Gestire le code dei messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) nel _Guida alla configurazione_ per ulteriori dettagli.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
