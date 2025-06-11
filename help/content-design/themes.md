---
title: Temi
description: Scopri  [!DNL Commerce] i temi, tra cui file di layout, file modello, file di traduzione e interfacce che definiscono l'aspetto del tuo archivio.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Temi

Un tema è una raccolta di file che determina la presentazione visiva dell’archivio. Quando si installa [!DNL Commerce] per la prima volta, gli elementi di progettazione dell&#39;archivio sono basati sul tema _Default_. Oltre al tema predefinito iniziale fornito con l&#39;installazione di [!DNL Commerce], è possibile utilizzare _così com&#39;è_ o modificarlo in base alle proprie esigenze.

Un tema reattivo regola il layout della pagina in base alla porta di visualizzazione del dispositivo. Il tema _Luma_ di esempio ha un layout flessibile e reattivo che può essere visualizzato dal desktop, dal tablet o dal dispositivo mobile.

I temi [!DNL Commerce] includono file di layout, file modello, file di traduzione e interfacce. Uno skin è una raccolta di file CSS, immagini e JavaScript di supporto che insieme creano la presentazione visiva e le interazioni che i clienti sperimentano quando visitano il tuo store. I temi e gli skin possono essere modificati e personalizzati da uno sviluppatore o da un professionista del design che conosce il design dei temi di Commerce e ha accesso al server. Per ulteriori informazioni, vedere la [_Guida per gli sviluppatori di FrontEnd_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Tema Luma](./assets/design-responsive.png){width="600" zoomable="yes"}

## Il tema predefinito

Il tema reattivo `Magento Blank` esegue il rendering della visualizzazione della vetrina per diversi dispositivi e incorpora le best practice per desktop, tabelle e dispositivi mobili. Alcuni temi sono progettati per essere utilizzati solo con dispositivi specifici. Quando [!DNL Commerce] rileva un ID browser specifico o un agente utente, utilizza il tema configurato per il browser specifico. La stringa di ricerca può includere anche espressioni regolari compatibili con Perl (PCRE).

![Temi](./assets/themes.png){width="700" zoomable="yes"}

### Filtrare la griglia del tema

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Fare clic su **[!UICONTROL Filters]**.

1. Immetti un intervallo ID, un nome tema (o titolo), un percorso cartella o un tema principale.

1. Fare clic su **[!UICONTROL Apply Filters]** per aggiornare l&#39;elenco dei temi.

## Visualizza impostazioni tema correnti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Nell&#39;elenco dei temi installati, individuare il tema che si desidera esaminare e fare clic sulla riga per visualizzare le impostazioni.

1. Per visualizzare una pagina di esempio, fare clic su **[!UICONTROL Theme Preview Image]**.

![Anteprima tema](./assets/theme-settings.png){width="600" zoomable="yes"}

## Applicare un tema predefinito

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione archivio da configurare e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. In _[!UICONTROL Default Theme]_, impostare **[!UICONTROL Applied Theme]**&#x200B;su quello che si desidera utilizzare per la visualizzazione corrente.

   ![Tema applicato](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.

## Aggiungere una regola agente utente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. In _[!UICONTROL Design Rule]_, fare clic su **[!UICONTROL Add New User Agent Rule]**.

   ![Regola di progettazione](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Search String]**, immettere l&#39;ID del browser per il dispositivo specifico.

   Le stringhe di ricerca vengono confrontate nell&#39;ordine in cui vengono immesse. Ad esempio, per Firefox immetti:

   `/^mozilla/i`

1. Per inserire altri dispositivi, ripetere la procedura.

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.
