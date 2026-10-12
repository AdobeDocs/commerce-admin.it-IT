---
title: Editor WYSIWYG
description: Scopri come utilizzare l’editor e lavorare con i contenuti in una vista _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# Editor WYSIWYG

L&#39;editor consente di immettere e formattare il contenuto mentre si lavora in una visualizzazione _What You See Is What You Get_ (WYSIWYG). Se preferisci lavorare direttamente con il codice HTML sottostante, puoi facilmente cambiare modalità. L&#39;editor può essere utilizzato per creare contenuti per [pagine](pages.md), [blocchi](blocks.md) e [descrizioni prodotto](../catalog/product-content.md). Quando si lavora sui dettagli del prodotto, accedere all&#39;editor facendo clic su **[!UICONTROL Show / Hide Editor]**.

![Barra degli strumenti dell&#39;editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Gli argomenti seguenti forniscono informazioni dettagliate sull’utilizzo dell’editor:

- [Inserimento di un collegamento](editor-insert-link.md)
- [Inserimento di un’immagine](editor-insert-image.md)
- [Inserimento di un widget](editor-widget.md)
- [Inserimento di una variabile](editor-insert-variable.md)

## Configurare l’editor

L’editor di WYSIWYG è abilitato per impostazione predefinita e può essere utilizzato per modificare il contenuto su pagine e blocchi CMS, nonché in prodotti e categorie. Dalla configurazione, puoi attivare o disattivare l&#39;editor e scegliere di utilizzare URL statici, anziché [dinamici](../catalog/catalog-urls.md#dynamic-url), per i contenuti multimediali nelle descrizioni di prodotti e categorie.

![Opzioni WYSIWYG](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>TinyMCE è stato sostituito con Hugerte come editor WYSIWYG predefinito in Magento 2.4.6 e versioni successive.

Per una descrizione dettagliata di tutte le opzioni di WYSIWYG, vedere [Gestione contenuto](../configuration-reference/general/content-management.md) nella _Guida di riferimento configurazione_.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Imposta **[!UICONTROL Enable WYSIWYG Editor]** sulla tua preferenza.

   L’editor è attivato per impostazione predefinita.

1. Imposta **[!UICONTROL Static URLs for Media Content in WYSIWYG]** sulle tue preferenze per tutti i [contenuti multimediali](../catalog/catalog-urls.md#static-url) immessi con l&#39;editor di WYSIWYG.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
