---
title: Impostazioni prodotto - [!UICONTROL Design]
description: Per un prodotto, le impostazioni [!UICONTROL Design] consentono di applicare un tema diverso a una pagina di prodotto e di modificare il layout.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
TQID: 'https://experienceleague.adobe.com/u6VzZ9TiovuSopBcBjmpQTKl3pzh3DoXXzpr8akWp-8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%
---
# Impostazioni prodotto - [!UICONTROL Design]

Le impostazioni di _[!UICONTROL Design]_&#x200B;consentono di applicare un tema diverso alla pagina del prodotto, modificare il layout delle colonne, determinare la posizione in cui vengono visualizzate le opzioni del prodotto e immettere un codice XML personalizzato.

![Progettazione](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando lo stesso prodotto viene assegnato a più categorie con impostazioni di progettazione diverse per ogni categoria, si consiglia di impostare **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` nelle [opzioni di configurazione Ottimizzazione motore di ricerca](../configuration-reference/catalog/catalog.md#search-engine-optimization). Per accedere a questa impostazione, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, espandi **[!UICONTROL Catalog]**&#x200B;e scegli **[!UICONTROL Catalog]**&#x200B;nel pannello a sinistra, quindi espandi la sezione **[!UICONTROL Search Engine Optimization]**&#x200B;nella pagina.

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|---|---|----|
| [!UICONTROL Theme] | Visualizzazione store | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) consente di applicare un tema diverso al prodotto. Opzioni: (tutti i temi disponibili) |
| [!UICONTROL Layout] | Visualizzazione store | Consente di applicare un [layout](../content-design/page-layout.md) diverso alla pagina del prodotto. Opzioni: <br/>**[!UICONTROL No layout updates]**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per la pagina prodotto.<br/>**[!UICONTROL Empty]** - Consente di definire un layout personalizzato, ad esempio una pagina a 4 colonne. (Richiede la comprensione di XML) <br/>**[!UICONTROL 1 column]**- Applica un layout a una colonna alla pagina del prodotto.<br/>**[!UICONTROL 2 columns with left bar]** - Applica un layout a due colonne con barra laterale a sinistra alla pagina del prodotto. <br/>**[!UICONTROL 2 columns with right bar]**- Applica un layout a due colonne con barra laterale a destra alla pagina del prodotto.<br/>**[!UICONTROL 3 columns]** - Applica un layout a tre colonne alla pagina del prodotto. <br/>**[!UICONTROL Page -- Full Width]**- (Richiede [[!DNL Page Builder]](../page-builder/introduction.md)) Applica il layout a larghezza intera per le pagine CMS alla pagina prodotto.<br/>**[!UICONTROL Category -- Full Width]** - (Richiede [!DNL Page Builder]) Applica il layout a larghezza intera per le pagine delle categorie alla pagina del prodotto. <br/>**[!UICONTROL Product -- Full Width]**- (Richiede [!UICONTROL Page Builder]) Applica il layout a larghezza intera per le pagine di prodotto alla pagina di prodotto. |
| [!UICONTROL Display Product Options In] | Visualizzazione store | Determina dove vengono visualizzate le opzioni prodotto nella pagina prodotto. Opzioni: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Visualizzazione store | Consente di accedere alle opzioni per aggiornare un layout personalizzato nella pagina del prodotto. |

{style="table-layout:auto"}

