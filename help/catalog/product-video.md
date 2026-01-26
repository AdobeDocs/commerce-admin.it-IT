---
title: Aggiungi video di prodotto
description: Scopri come configurare i video dei prodotti per il tuo store, che richiede una chiave API dati di YouTube da un account Google, e aggiungere un collegamento video per un prodotto.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# Aggiungi video di prodotto

Per aggiungere un video di prodotto, devi prima ottenere una chiave API dal tuo account Google e immetterla nella configurazione dello store. Quindi puoi collegare il prodotto al video.

## Passaggio 1: ottenere la chiave API di YouTube

1. Accedi al tuo account Google e visita la [console per sviluppatori di Google](https://console.developers.google.com/).

1. Nel campo di ricerca nella parte superiore, immettere `YouTube Data API v3` e fare clic sull&#39;icona di ricerca.

1. Quando viene visualizzata la pagina API, accertati che sia abilitata.

1. Nel pannello a sinistra, scegli **[!UICONTROL Credentials]**.

1. A seconda che si disponga di credenziali o meno, eseguire una delle operazioni seguenti:

   - Se disponi già delle credenziali necessarie, copia la chiave nella tabella _Chiavi API_.

   - Se non si dispone già delle credenziali per questa API, fare clic su **[!UICONTROL Create Credentials]** nella parte superiore e seguire le istruzioni per creare le credenziali necessarie. In _Ottieni le tue credenziali_, copia la chiave API e fai clic su **[!UICONTROL Done]**.

1. Copia la chiave API negli Appunti.

1. Fai clic sull’icona Modifica a destra e imposta le restrizioni per assicurarti che la chiave API sia limitata ai referenti corretti.

1. Attendi alcuni istanti mentre viene generata la chiave, quindi copiala negli Appunti.

   Nel passaggio successivo, incollerai la chiave nella configurazione del tuo archivio.

## Passaggio 2: configurare la chiave in Commerce

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Product Video]_&#x200B;e incolla **[!UICONTROL YouTube API key]**.

   ![Configurazione video prodotto](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna la cache.

## Passaggio 3: collegamento al video

1. Apri un prodotto in modalità di modifica.

1. Scorri fino alla sezione _[!UICONTROL Images and Videos]_&#x200B;ed espandila.

   ![Immagini e video](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. fare clic su **[!UICONTROL Add Video]**.

   Se non hai ancora configurato la chiave API di YouTube, fai clic su **[!UICONTROL OK]** per continuare. Non puoi effettuare il collegamento a un video YouTube, ma puoi seguire la procedura.

1. Per **[!UICONTROL Url]**, immetti l&#39;URL del video YouTube o Vimeo.

   ![Nuovo video per il prodotto](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Fai clic all’esterno del campo e attendi il feedback sulla chiave API o sul video.

   Se tutto viene estratto, YouTube fornisce le informazioni di base del video

1. Immetti **[!UICONTROL Title]** e **[!UICONTROL Description]** del video.

1. Per caricare un **[!UICONTROL Preview Image]**, individuare l&#39;immagine e selezionare il file.

   >[!NOTE]
   >
   >Dopo il caricamento, l’immagine di anteprima visualizzata viene generata automaticamente da un provider di servizi video esterno. Non è possibile modificare l’immagine dall’amministratore di Adobe Commerce.

1. Se si preferisce utilizzare i metadati video, fare clic su **[!UICONTROL Get Video Information]**.

1. Per determinare la modalità di utilizzo del video nell&#39;archivio, selezionare la casella di controllo di ogni **[!UICONTROL Role]** applicabile:

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. Al termine, fare clic su **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Se l&#39;opzione di configurazione _[!UICONTROL Autostart base video]_&#x200B;è impostata su `Yes` ma il video non inizia a essere riprodotto automaticamente, ciò potrebbe essere dovuto ai criteri di riproduzione automatica applicati dal browser e non controllabili da Adobe Commerce. Ogni browser supportato dispone di criteri di riproduzione automatica che possono cambiare nel tempo e il video potrebbe non essere riprodotto automaticamente in futuro. Come best practice consigliata, non affidarti alla riproduzione automatica per le funzionalità business critical e verifica il comportamento di riproduzione automatica del video nel tuo store con ogni browser supportato.

## Gestisci accesso API

In base ai [Termini e condizioni](https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services) per gli sviluppatori di Google, YouTube potrebbe disabilitare l&#39;accesso API per gli account inattivi da più di 90 giorni. Questa occorrenza potrebbe impedire la visualizzazione dei video. Per mantenere aggiornato l’accesso API, utilizza un processo cron per eseguire il ping dell’API a intervalli regolari:

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## Riferimento campo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL URL] | URL del video associato. |
| [!UICONTROL Title] | Titolo del video. |
| [!UICONTROL Description] | Descrizione del video. |
| [!UICONTROL Preview Image] | Un’immagine caricata che viene utilizzata come anteprima del video nel tuo store. |
| [!UICONTROL Get Video Information] | Recupera i metadati video memorizzati sul server host. Puoi utilizzare i dati originali o aggiornarli in base alle esigenze. |
| [!UICONTROL Role] | Determina il modo in cui l&#39;immagine di anteprima viene utilizzata nell&#39;archivio. È possibile scegliere qualsiasi combinazione di opzioni: `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}
