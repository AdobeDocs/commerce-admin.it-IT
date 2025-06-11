---
title: Risorse tema
description: Scopri come gestire le risorse dei temi, ad esempio CSS, font, immagini e file JavaScript.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: e50b85311f4512fb54c7cb29faf6136eaf07eae6
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Risorse tema

I _file statici_ sono la raccolta di risorse, ad esempio CSS, font, immagini e JavaScript, utilizzate da un tema. Il percorso dei file statici è specificato nella configurazione [URL di base](../stores-purchase/store-urls.md). È possibile aggiungere una firma digitale all&#39;URL di ogni file statico per consentire ai browser di rilevare quando è disponibile una versione più recente. La versione più recente del file viene utilizzata se la firma è diversa da quella memorizzata nella cache del browser.

Per un&#39;installazione standard, le risorse associate a un tema sono organizzate nella cartella `web` nel seguente percorso sotto la directory principale [!DNL Commerce].

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Aggiungere una firma digitale agli URL statici dei file

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Static Files Settings]**.

   ![Impostazioni file statici](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Imposta **[!UICONTROL Sign Static Files]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

| Tipo di file | Descrizione |
|--- |--- |
| CSS | Controlla lo stile visivo associato all&#39;interfaccia. Percorso di esempio sul server: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Font | Specificare i font disponibili per il tema. Percorso sul server: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Immagini | Fornisci le risorse grafiche utilizzate dal tema, inclusi i pulsanti, le texture di sfondo e così via. Percorso di esempio sul server: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Routine JavaScript specifiche per il tema e funzioni richiamabili. Percorso di esempio sul server: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Unisci file CSS

Come parte di uno sforzo per ottimizzare il tuo sito e ridurre il tempo di caricamento delle pagine, puoi ridurre il numero di file CSS separati unendoli in un unico file condensato. Se apri un file CSS unito, viene visualizzato un flusso continuo di testo, con le interruzioni di riga rimosse. Non è possibile modificare il file unito, quindi è meglio attendere che tu non sia fuori dalla modalità di sviluppo e che non apporti più frequenti modifiche al CSS.

>[!NOTE]
>
>I file CSS possono essere uniti dal pannello _Admin_ solo quando si lavora in [modalità sviluppatore](../systems/developer-tools.md#operation-modes).

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL CSS Settings]**.

   ![Impostazioni CSS](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Per le descrizioni dettagliate di queste opzioni di configurazione, vedi [Impostazioni CSS](../configuration-reference/advanced/developer.md#css-settings) nel _Riferimento configurazione_.

1. Imposta **[!UICONTROL Merge CSS Files]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Unisci file JavaScript

È possibile unire più file JavaScript in un unico file condensato per ridurre il tempo di caricamento della pagina. Se si apre un file JavaScript unito, viene visualizzato un flusso continuo di testo, con le interruzioni di riga rimosse. Se il processo di sviluppo è terminato e il codice non contiene errori, è consigliabile unire i file.

>[!NOTE]
>
>I file JavaScript possono essere uniti dal pannello _Admin_ solo quando si lavora in [Modalità sviluppatore](../systems/developer-tools.md#operation-modes).

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL JavaScript Settings]**.

   ![Impostazioni JavaScript](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Per le descrizioni dettagliate di queste opzioni di configurazione, vedere [Impostazioni di JavaScript](../configuration-reference/advanced/developer.md#javascript-settings) nella _Guida di riferimento alla configurazione_.

1. Imposta **[!UICONTROL Merge JavaScript Files]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
