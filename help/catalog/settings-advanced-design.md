---
title: Impostazioni prodotto - [!UICONTROL Design]
description: Per un prodotto, il [!UICONTROL Design] Le impostazioni consentono di applicare un tema diverso a una pagina di prodotto e di modificare il layout.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Impostazioni prodotto - [!UICONTROL Design]

Il _[!UICONTROL Design]_Le impostazioni consentono di applicare un tema diverso alla pagina del prodotto, modificare il layout delle colonne, determinare dove vengono visualizzate le opzioni del prodotto e immettere codice XML personalizzato.

![Progettazione](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando lo stesso prodotto viene assegnato a più categorie con impostazioni di progettazione diverse per ciascuna categoria, si consiglia di impostare **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` nel [Opzioni di configurazione dell’ottimizzazione per i motori di ricerca](../configuration-reference/catalog/catalog.md#search-engine-optimization). Per accedere a questa impostazione, vai a  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, espandi **[!UICONTROL Catalog]**e scegli **[!UICONTROL Catalog]**nel pannello a sinistra, quindi espandi il **[!UICONTROL Search Engine Optimization]**sulla pagina.

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|---|---|----|
| [!UICONTROL Theme] | Visualizzazione store | ![Adobe Commerce](../assets/adobe-logo.svg) Solo per Adobe Commerce consente di applicare un tema diverso al prodotto. Opzioni: (tutti i temi disponibili) |
| [!UICONTROL Layout] | Visualizzazione store | Consente di applicare un [layout](../content-design/page-layout.md) alla pagina del prodotto. Opzioni: <br/>**[!UICONTROL No layout updates]**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per la pagina prodotto.<br/>**[!UICONTROL Empty]** - Consente di definire un layout personalizzato, ad esempio una pagina a 4 colonne. (richiede una comprensione di XML). <br/>**[!UICONTROL 1 column]**- Applica un layout a una colonna alla pagina del prodotto.<br/>**[!UICONTROL 2 columns with left bar]** - Applica un layout a due colonne con barra laterale a sinistra alla pagina del prodotto. <br/>**[!UICONTROL 2 columns with right bar]**- Applica un layout a due colonne con barra laterale a destra alla pagina del prodotto.<br/>**[!UICONTROL 3 columns]** - Applica un layout a tre colonne alla pagina del prodotto. <br/>**[!UICONTROL Page -- Full Width]**- (Richiede [[!DNL Page Builder]](../page-builder/introduction.md)) Applica il layout a larghezza intera per le pagine CMS alla pagina del prodotto.<br/>**[!UICONTROL Category -- Full Width]** - (Richiede [!DNL Page Builder]) Applica il layout a larghezza intera per le pagine delle categorie alla pagina del prodotto. <br/>**[!UICONTROL Product -- Full Width]**- (Richiede [!UICONTROL Page Builder]) Applica il layout a larghezza intera per le pagine di prodotto alla pagina di prodotto. |
| [!UICONTROL Display Product Options In] | Visualizzazione store | Determina dove vengono visualizzate le opzioni prodotto nella pagina prodotto. Opzioni: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Visualizzazione store | Consente di accedere alle opzioni per aggiornare un layout personalizzato nella pagina del prodotto. |

{style="table-layout:auto"}
