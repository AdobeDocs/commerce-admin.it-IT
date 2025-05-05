---
title: Configurazione di [!DNL Page Builder]
description: Scopri la configurazione della funzione  [!DNL Page Builder]  in Admin for Adobe Commerce and Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Configurazione di [!DNL Page Builder]

Se attivato nella configurazione, [!DNL Page Builder] è lo strumento predefinito per la creazione di contenuti per pagine, blocchi e blocchi dinamici di CMS. Inoltre, il pulsante _[!UICONTROL Enable Advanced CMS]_&#x200B;offre [!DNL Page Builder] come opzione per Categorie e Prodotti. Puoi anche scegliere il [layout di pagina](../content-design/page-layout.md) predefinito che desideri utilizzare per prodotti, categorie e pagine CMS. [!DNL Page Builder] non è disponibile per il contenuto della newsletter, che utilizza l&#39;[editor](../content-design/editor.md) di WYSIWYG.

>[!NOTE]
>
>Una volta installato, [!DNL Page Builder] sostituisce l&#39;impostazione predefinita per il campo di configurazione [!UICONTROL Mask for Meta Description]. Il valore è cambiato da `{{name}} {{description}}` a `{{name}}`.
><br>
>Puoi accedere a questa impostazione quando scegli [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], espandi [!UICONTROL Catalog] e scegli [!UICONTROL Catalog] di seguito. Il campo [!UICONTROL Mask for Meta Description] si trova nella sezione [!UICONTROL Product Fields Auto-generation].

>[!NOTE]
>
>Per visualizzare i pulsanti [!UICONTROL Edit with Page Builder] e utilizzare Page Builder, un utente amministratore deve disporre delle autorizzazioni [!UICONTROL Content] per il proprio ambito [ruolo](../systems/permissions-user-roles.md).

Per ulteriori informazioni sulle opzioni di configurazione degli strumenti avanzati di Content Management, vedere la [_Guida di riferimento alla configurazione_](../configuration-reference/general/content-management.md).

## Configura [!DNL Page Builder]

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e verificare che **[!UICONTROL Enable Page Builder]** sia impostato su `Yes`.

   ![Strumenti di contenuto avanzati](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Se si è pronti a configurare [!DNL Google Maps], eseguire le operazioni seguenti:

   - Se necessario, seguire le istruzioni [Ottieni chiave API][1], quindi copiare e incollare **[!UICONTROL Google Maps API Key]**.

   - Per modificare **[!UICONTROL Google Maps Style]**, incollare il codice JSON generato dalla [[!DNL Google Maps] Creazione guidata stili API][2].

   >[!NOTE]
   >
   >Per ulteriori informazioni sull&#39;utilizzo di [!DNL Google Maps] nel contenuto di [!DNL Page Builder], vedere [Media - Map](map.md).

1. Per configurare il numero di linee guida nella griglia di colonna [!DNL Page Builder], eseguire le operazioni seguenti:

   - Per **[!UICONTROL Default Column Grid Size]**, immettere il numero predefinito di colonne che si desidera visualizzare nella griglia.

   - Per **[!UICONTROL Maximum Column Grid Size]**, immettere il numero massimo di colonne che si desidera rendere disponibili nella griglia.

   >[!NOTE]
   >
   >Per ulteriori informazioni sull&#39;utilizzo della griglia delle colonne durante l&#39;utilizzo del contenuto di [!DNL Page Builder], vedere [Layout - Colonna](column.md).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Configurare i layout predefiniti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** ed effettuare le seguenti operazioni:

   ![Layout predefiniti](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Per ulteriori informazioni sulle opzioni di configurazione Web, vedere la [_Guida di riferimento alla configurazione_](../configuration-reference/general/web.md#default-layouts).

   - Scegliere **[!UICONTROL Default Product Layout]** da utilizzare per le pagine di prodotti.

   - Scegliere **[!UICONTROL Default Category Layout]** da utilizzare per le pagine delle categorie.

   - Scegliere **[!UICONTROL Default Page Layout]** da utilizzare per le pagine CMS.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Disabilita [!DNL Page Builder]

>[!NOTE]
>
>La disabilitazione di [!DNL Page Builder] sostituisce gli strumenti di contenuto avanzato con l&#39;editor [&#128279;](../content-design/editor.md) di WYSIWYG e potrebbe causare errori di visualizzazione nella vetrina.  Il contenuto creato in precedenza con [!DNL Page Builder] potrebbe non essere modificabile dall&#39;amministratore.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** e impostare **[!UICONTROL Enable Page Builder]** su `No`.

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL Turn Off]**.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, [aggiorna](../systems/cache-management.md) la cache non valida.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
