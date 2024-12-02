---
title: '[!DNL AR Viewer] per la configurazione di Adobe Commerce'
description: Scopri come gestire le risorse dei modelli 3D utilizzando l’estensione  [!DNL AR Viewer]  per gli elenchi dei prodotti.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Gestisci modelli 3D di prodotto con [!DNL AR Viewer] per Adobe Commerce

Per ogni prodotto, puoi caricare un file `.USDZ` che consente l&#39;utilizzo di modelli AR e 3D nell&#39;elenco dei prodotti.

[!DNL AR Viewer] supporta solo `.USDZ` file.

## Installare l’estensione

[!DNL AR Viewer] è installato come estensione da [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Per ulteriori informazioni sul processo di installazione dell&#39;estensione, vedere la [_Guida all&#39;installazione_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Dopo l&#39;installazione e la configurazione dell&#39;estensione [!DNL AR Viewer], gli utenti amministratori possono impostare, personalizzare e gestire gli elenchi di prodotti per includere modelli 3D.

## Aggiungere un modello 3D

1. Apri il prodotto in modalità di modifica.

1. Per utilizzare una visualizzazione archivio specifica, impostare il selettore **[!UICONTROL Store View]** sulla visualizzazione applicabile.

   >[!NOTE]
   >
   >I nuovi modelli 3D del prodotto sono _sempre_ caricati e visibili in _tutte_ le visualizzazioni archivio, anche se l&#39;ambito `All Store Views` non è utilizzato per il caricamento. <br/><br/>Per nascondere qualsiasi modello 3D di prodotto da una visualizzazione di archivio specifica, è necessario passare a tale visualizzazione, selezionare la casella di controllo **[!UICONTROL Hide from Product Page]** per il modello 3D e fare clic su **[!UICONTROL Save]**.

1. Scorri verso il basso ed espandi la sezione _[!UICONTROL Product 3D Model]_.

   ![Menu a comparsa](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Aggiungere il modello 3D (`.USDZ` file) del prodotto.

1. Fare clic su **[!UICONTROL Save]**.

### Eliminare un modello 3D

Per rimuovere un modello 3D dai dettagli del prodotto:

1. Fare clic su **[!UICONTROL Delete]**.

1. Fare clic su **[!UICONTROL Save]**.

## Visualizza modelli 3D del prodotto

Quando i dettagli del prodotto vengono aggiornati con il modello 3D:

1. [!DNL AR Viewer] genera un codice QR nella descrizione del prodotto che codifica il file AR.

1. Un cliente può visualizzare questo codice QR nella pagina del prodotto.

1. Quando i clienti digitalizzano il codice QR con i propri dispositivi mobili, viene riprodotta un’esperienza AR sul dispositivo mobile.

>[!NOTE]
>
> Per una serie di video dimostrativi di un utente che aggiunge un modello 3d a un prodotto, vedere la pagina [AR Viewer per Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) in _Video e Tutorials di Commerce_.
