---
title: '''[!DNL AR Viewer] per la configurazione di Adobe Commerce'
description: Scopri come gestire le risorse dei modelli 3D utilizzando [!DNL AR Viewer] estensione per gli elenchi di prodotti.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Gestire i modelli 3D di prodotto con [!DNL AR Viewer] per Adobe Commerce

Per ogni prodotto, puoi caricare una `.USDZ` file che consente l&#39;utilizzo di modelli AR e 3D nell&#39;elenco dei prodotti.

Il [!DNL AR Viewer] supporta solo `.USDZ` file.

## Installare l’estensione

[!DNL AR Viewer] è installato come estensione da [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Consulta la [_Guida all’installazione_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) per ulteriori informazioni sul processo di installazione dell’estensione.

Dopo il [!DNL AR Viewer] Se l&#39;estensione è installata e configurata, gli utenti amministratori possono impostare, personalizzare e gestire gli elenchi di prodotti per includere modelli 3D.

## Aggiungere un modello 3D

1. Apri il prodotto in modalità di modifica.

1. Per utilizzare una visualizzazione specifica dello store, impostare **[!UICONTROL Store View]** selezionare la vista applicabile.

   >[!NOTE]
   >
   >I nuovi modelli 3D di prodotto sono _sempre_ caricato e visibile in _tutto_ archiviare le visualizzazioni, anche se `All Store Views` ambito non utilizzato per il caricamento. <br/><br/>Per nascondere qualsiasi modello 3D di prodotto da una visualizzazione di negozio specifica, è necessario passare a tale visualizzazione di negozio, selezionare **[!UICONTROL Hide from Product Page]** selezionare la casella di controllo per il modello 3D e fare clic su **[!UICONTROL Save]**.

1. Scorri verso il basso ed espandi _[!UICONTROL Product 3D Model]_sezione.

   ![Menu a comparsa](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Aggiungere il modello 3D (`.USDZ` del prodotto.

1. Clic **[!UICONTROL Save]**.

### Eliminare un modello 3D

Per rimuovere un modello 3D dai dettagli del prodotto:

1. Clic **[!UICONTROL Delete]**.

1. Clic **[!UICONTROL Save]**.

## Visualizza modelli 3D del prodotto

Quando i dettagli del prodotto vengono aggiornati con il modello 3D:

1. Il [!DNL AR Viewer] genera un codice QR nella descrizione del prodotto che codifica il file AR.

1. Un cliente può visualizzare questo codice QR nella pagina del prodotto.

1. Quando i clienti digitalizzano il codice QR con i propri dispositivi mobili, viene riprodotta un’esperienza AR sul dispositivo mobile.

>[!NOTE]
>
> Per una serie di video dimostrativi su un utente che aggiunge un modello 3d a un prodotto, vedi [Visualizzatore AR per Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) pagina in _Video e Tutorials di Commerce_.
