---
title: '[!DNL Page Builder] setup'
description: Informazioni su [!DNL Page Builder] configurazione delle funzioni in Admin for Adobe Commerce e Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] configurazione

Quando è abilitato nella configurazione, [!DNL Page Builder] è lo strumento predefinito per la creazione di contenuti per pagine CMS, blocchi e blocchi dinamici. Inoltre, la _[!UICONTROL Enable Advanced CMS]_offerte di pulsanti [!DNL Page Builder] come opzione per Categorie e Prodotti. È inoltre possibile scegliere il valore predefinito [layout di pagina](../content-design/page-layout.md) che desideri utilizzare per prodotti, categorie e pagine CMS. [!DNL Page Builder] non è disponibile per il contenuto della newsletter, che utilizza la modalità WYSIWYG [editor](../content-design/editor.md).

>[!NOTE]
>
>Una volta installato, [!DNL Page Builder] sostituisce l&#39;impostazione predefinita per [!UICONTROL Mask for Meta Description] campo di configurazione. Il valore viene modificato da `{{name}} {{description}}` a `{{name}}`.
><br>
>Puoi accedere a questa impostazione quando vai a [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], espandi [!UICONTROL Catalog]e scegli [!UICONTROL Catalog] sotto. Il [!UICONTROL Mask for Meta Description] il campo è nel [!UICONTROL Product Fields Auto-generation] sezione.

>[!NOTE]
>
>Un utente amministratore deve avere [!UICONTROL Content] le autorizzazioni per [ambito del ruolo](../systems/permissions-user-roles.md) da vedere [!UICONTROL Edit with Page Builder] ed essere in grado di utilizzare Page Builder.

Per ulteriori informazioni sulle opzioni di configurazione degli Strumenti avanzati di Content Management, vedere [_Guida di riferimento alla configurazione_](../configuration-reference/general/content-management.md).

## Configura [!DNL Page Builder]

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e verifica che **[!UICONTROL Enable Page Builder]** è impostato su `Yes`.

   ![Strumenti di contenuto avanzati](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Se si è pronti a configurare [!DNL Google Maps], eseguire le operazioni seguenti:

   - Se necessario, seguire le istruzioni [Ottieni chiave API][1] e quindi copiare e incollare le istruzioni **[!UICONTROL Google Maps API Key]**.

   - Per modificare il **[!UICONTROL Google Maps Style]**, incolla il codice JSON generato da [[!DNL Google Maps] Creazione guidata stile API][2].

   >[!NOTE]
   >
   >Consulta [Media - Mappa](map.md) per ulteriori informazioni sull&#39;utilizzo di [!DNL Google Maps] nel tuo [!DNL Page Builder] contenuto.

1. Per configurare il numero di linee guida in [!DNL Page Builder] nella griglia di colonna, effettuare le seguenti operazioni:

   - Per **[!UICONTROL Default Column Grid Size]**, immettere il numero predefinito di colonne che si desidera visualizzare nella griglia.

   - Per **[!UICONTROL Maximum Column Grid Size]**, immettere il numero massimo di colonne che si desidera rendere disponibili nella griglia.

   >[!NOTE]
   >
   >Consulta [Layout - Colonna](column.md) per ulteriori informazioni sull&#39;utilizzo della griglia di colonna quando si lavora con [!DNL Page Builder] contenuto.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configurare i layout predefiniti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** ed effettuare le seguenti operazioni:

   ![Layout predefiniti](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Per ulteriori informazioni sulle opzioni di configurazione Web, vedere [_Guida di riferimento alla configurazione_](../configuration-reference/general/web.md#default-layouts).

   - Scegli la **[!UICONTROL Default Product Layout]** che desideri utilizzare per le pagine di prodotti.

   - Scegli la **[!UICONTROL Default Category Layout]** da utilizzare per le pagine delle categorie.

   - Scegli la **[!UICONTROL Default Page Layout]** che desideri utilizzare per le pagine CMS.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Disattiva [!DNL Page Builder]

>[!NOTE]
>
>Disattivazione [!DNL Page Builder] sostituisce gli strumenti di contenuto avanzati con la modalità WYSIWYG [editor](../content-design/editor.md)e potrebbero causare errori di visualizzazione nella vetrina. Contenuto creato in precedenza con [!DNL Page Builder] potrebbe non essere modificabile dall’amministratore.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e imposta **[!UICONTROL Enable Page Builder]** a `No`.

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL Turn Off]**.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, [aggiorna](../systems/cache-management.md) cache non valida.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
