---
title: Temi
description: Informazioni su [!DNL Commerce] i temi, che includono file di layout, file modello, file di traduzione e interfacce, che definiscono l'aspetto del tuo archivio.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Temi

Un tema è una raccolta di file che determina la presentazione visiva dell’archivio. La prima volta che installi [!DNL Commerce], gli elementi di progettazione del negozio sono basati sulla _Predefinito_ tema. Oltre al tema predefinito iniziale fornito con il [!DNL Commerce] dell&#39;installazione, è possibile utilizzare un&#39;ampia gamma di temi _così com’è_ o modificarli in base alle proprie esigenze.

Un tema reattivo regola il layout della pagina in base alla porta di visualizzazione del dispositivo. Il campione _Luma_ il tema ha un layout flessibile e reattivo che può essere visualizzato dal desktop, dal tablet o dal dispositivo mobile.

[!DNL Commerce] i temi includono file di layout, file modello, file di traduzione e interfacce. Uno skin è una raccolta di file CSS, immagini e JavaScript di supporto che insieme creano la presentazione visiva e le interazioni che i clienti sperimentano quando visitano il tuo store. I temi e gli skin possono essere modificati e personalizzati da uno sviluppatore o da un professionista del design che comprende la progettazione dei temi Commerce e ha accesso al server. Per ulteriori informazioni, consulta [_Guida per gli sviluppatori di front-end_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Tema Luma](./assets/design-responsive.png){width="600" zoomable="yes"}

## Il tema predefinito

Il `Magento Blank` responsive theme esegue il rendering della vetrina per diversi dispositivi e incorpora best practice per desktop, tabelle e dispositivi mobili. Alcuni temi sono progettati per essere utilizzati solo con dispositivi specifici. Quando [!DNL Commerce] rileva un ID browser specifico, o agente utente, e utilizza il tema configurato per il browser specifico. La stringa di ricerca può includere anche espressioni regolari compatibili con Perl (PCRE).

![Temi](./assets/themes.png){width="700" zoomable="yes"}

### Filtrare la griglia del tema

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Clic **[!UICONTROL Filters]**.

1. Immetti un intervallo ID, un nome tema (o titolo), un percorso cartella o un tema principale.

1. Clic **[!UICONTROL Apply Filters]** per aggiornare l&#39;elenco dei temi.

## Visualizza impostazioni tema correnti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Nell&#39;elenco dei temi installati, individuare il tema che si desidera esaminare e fare clic sulla riga per visualizzare le impostazioni.

1. Per visualizzare una pagina di esempio, fare clic su **[!UICONTROL Theme Preview Image]**.

![Anteprima tema](./assets/theme-settings.png){width="600" zoomable="yes"}

## Applicare un tema predefinito

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione dello store che si desidera configurare e fare clic su **[!UICONTROL Edit]** nel _[!UICONTROL Action]_colonna.

1. Sotto _[!UICONTROL Default Theme]_, impostato **[!UICONTROL Applied Theme]**a quello che si desidera utilizzare per la visualizzazione corrente.

   ![Tema applicato](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Configuration]**.

## Aggiungere una regola agente utente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Sotto _[!UICONTROL Design Rule]_, fai clic su **[!UICONTROL Add New User Agent Rule]**.

   ![Regola di progettazione](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Search String]**, immetti l’ID del browser per il dispositivo specifico.

   Le stringhe di ricerca vengono confrontate nell&#39;ordine in cui vengono immesse. Ad esempio, per Firefox immetti:

   `/^mozilla/i`

1. Per inserire altri dispositivi, ripetere la procedura.

1. Al termine, fai clic su **[!UICONTROL Save Configuration]**.
