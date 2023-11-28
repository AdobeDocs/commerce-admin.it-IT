---
title: Ottenere la licenza di un’immagine Adobe Stock
description: Per assicurarti di avere accesso legale e per eliminare la filigrana di Adobe Stock, acquisisci licenza per le immagini Adobe Stock.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Ottenere la licenza di un’immagine Adobe Stock

Le risorse Adobe Stock che desideri utilizzare per la produzione Adobe Commerce e gli archivi di Magento Open Source devono essere concessi in licenza. Questa licenza garantisce l’accesso legale all’immagine e l’eliminazione della filigrana Adobe Stock presente su tutte le [anteprime immagini][save-preview]. Per concedere in licenza immagini o salvare immagini già concesse in licenza, devi aver effettuato l’accesso al tuo account di Adobe.

Il nuovo [[!DNL Media Gallery]](media-gallery.md) fornisce un’integrazione diretta con Adobe Stock, semplificando la concessione di licenze per le immagini direttamente dalla pagina della galleria.

## Prerequisiti

Questa funzione richiede [Integrazione di Adobe Stock][adobe-stock-integration] modulo e configurazione. Licenze [Adobe Stock][adobe-stock] immagini richiede un piano Adobe Stock a pagamento e un [account Adobe][adobe-signin].

## Ottieni licenza per un&#39;immagine dal nuovo [!DNL Media Gallery]

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Segui i passaggi per [Utilizzo delle immagini di Adobe Stock][using-adobe-stock] per accedere e salvare le immagini di anteprima in [archiviazione dei supporti][media-storage].

   ![Immagine anteprima salvata](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Fai clic sui tre punti sotto l’immagine (![Icona del menu Risorsa](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), quindi fare clic su **[!UICONTROL License]**.

   ![Azioni immagine Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se non hai effettuato l’accesso, viene visualizzato il modulo di accesso. Per ulteriori informazioni sull&#39;accesso, vedere [Utilizzo delle immagini di Adobe Stock][using-adobe-stock].

1. Nella finestra di dialogo di conferma della licenza, fai clic su **[!UICONTROL Confirm]** per ottenere la licenza per l&#39;immagine.

   ![Conferma licenza](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >È necessario disporre di [Crediti Adobe Stock][stock-credits] nel tuo account per concedere in licenza l’immagine.

## Ottenere la licenza di un&#39;immagine dal supporto di archiviazione standard

1. [Accedere alla griglia di ricerca di Adobe Stock][access-search].

1. A [visualizzare i dettagli dell&#39;immagine][view-details], fare clic su un&#39;immagine nella griglia di ricerca nell&#39;ordine desiderato.

1. A seconda dello stato di licenza corrente dell&#39;immagine, effettuare una delle seguenti operazioni:

   - Se l&#39;immagine è già concessa in licenza, fare clic su **[!UICONTROL Save]**.

   - Se l’immagine è _non_ license, click **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >È necessario disporre di [Crediti Adobe Stock][stock-credits] nel tuo account per concedere in licenza l’immagine.

   Questa azione richiede di specificare un nome di file utilizzato per salvare l&#39;immagine nel [archiviazione dei supporti][media-storage]. Viene fornito un nome di file predefinito, ma puoi personalizzarlo in base alle tue preferenze.

   ![Salva immagine con licenza Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Clic **[!UICONTROL Confirm]**.

   La pagina viene reindirizzata all&#39;archivio multimediale e viene visualizzata l&#39;anteprima salvata.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
