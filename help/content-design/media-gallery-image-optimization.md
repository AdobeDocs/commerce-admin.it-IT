---
title: Ottimizzazione immagine di Media Gallery
description: Scopri come utilizzare l'ottimizzazione delle immagini per le  [!DNL Commerce] risorse multimediali.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
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

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
