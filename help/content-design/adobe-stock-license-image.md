---
title: Ottenere la licenza di un’immagine Adobe Stock
description: Per assicurarti di avere accesso legale e per eliminare la filigrana di Adobe Stock, acquisisci licenza per le immagini Adobe Stock.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: 0d072ecdba696383bd33b88b64d751736429f2f6
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Ottenere la licenza di un’immagine Adobe Stock

Le risorse Adobe Stock che desideri utilizzare per la produzione Adobe Commerce e gli archivi di Magento Open Source devono essere concessi in licenza. Questa licenza ti garantisce l&#39;accesso legale all&#39;immagine e l&#39;eliminazione della filigrana di Adobe Stock presente in tutte le [anteprime di immagini](./adobe-stock-save-preview.md). Per concedere in licenza immagini o salvare immagini già concesse in licenza, devi aver effettuato l’accesso al tuo account di Adobe.

Il nuovo [[!DNL Media Gallery]](media-gallery.md) offre un&#39;integrazione diretta con Adobe Stock, semplificando la concessione di licenze per le immagini direttamente dalla pagina della galleria.

>[!BEGINSHADEBOX]

**Prerequisiti**

La funzionalità di gestione licenze di Adobe Stock è disponibile solo se è installata e configurata l&#39;[integrazione Adobe Stock](./adobe-stock.md). Per concedere in licenza [immagini Adobe Stock][adobe-stock] è necessario un piano Adobe Stock a pagamento e un account [Adobe][adobe-signin].

>[!ENDSHADEBOX]

## Ottieni licenza per un&#39;immagine dal nuovo [!DNL Media Gallery]

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Segui i passaggi su [Utilizzo di immagini Adobe Stock](./adobe-stock-manage.md) per accedere e salvare le immagini di anteprima nell&#39;[archivio multimediale](./media-storage.md).

   ![Immagine di anteprima salvata](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Fare clic sui tre punti sotto l&#39;immagine (![icona menu risorse](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), quindi fare clic su **[!UICONTROL License]**.

   ![Azioni immagine Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se non hai effettuato l’accesso, viene visualizzato il modulo di accesso. Per ulteriori informazioni sull&#39;accesso, vedere [Utilizzo di immagini Adobe Stock](./adobe-stock-manage.md).

1. Nella finestra di dialogo di conferma della licenza, fare clic su **[!UICONTROL Confirm]** per concedere la licenza all&#39;immagine.

   ![Conferma licenza](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Devi disporre di [crediti Adobe Stock][stock-credits] nel tuo account per concedere in licenza l&#39;immagine.

## Ottenere la licenza di un&#39;immagine dal supporto di archiviazione standard

1. [Accedere alla griglia di ricerca di Adobe Stock][access-search].

1. Per [visualizzare i dettagli dell&#39;immagine][view-details], fare clic su un&#39;immagine nella griglia di ricerca nell&#39;ordine desiderato.

1. A seconda dello stato di licenza corrente dell&#39;immagine, effettuare una delle seguenti operazioni:

   - Se l&#39;immagine è già concessa in licenza, fare clic su **[!UICONTROL Save]**.

   - Se l&#39;immagine è _not_ concessa in licenza, fare clic su **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Devi disporre di [crediti Adobe Stock][stock-credits] nel tuo account per concedere in licenza l&#39;immagine.

   Questa azione richiede di specificare un nome di file utilizzato per salvare l&#39;immagine nell&#39;[archivio multimediale](./media-storage.md). Viene fornito un nome di file predefinito, ma puoi personalizzarlo in base alle tue preferenze.

   ![Salva immagine con licenza Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Fare clic su **[!UICONTROL Confirm]**.

   La pagina viene reindirizzata all&#39;archivio multimediale e viene visualizzata l&#39;anteprima salvata.

[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/it/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/it/manage-account/using/access-adobe-id-account.html
