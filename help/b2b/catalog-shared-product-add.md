---
title: Aggiungere prodotti a un catalogo condiviso
description: Scopri come aggiungere prodotti a un catalogo condiviso, singolarmente o in gruppi per categoria.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
TQID: 'https://experienceleague.adobe.com/f-5xQDov-Q3tfYw8MBDQPinimUIUkGe-q2Nfzm8L9ps'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%
---
# Aggiungere prodotti a un catalogo condiviso

I prodotti possono essere aggiunti a un catalogo condiviso singolarmente o in gruppi di più prodotti per categoria.

Affinché un prodotto complesso (ad esempio bundle, raggruppato o configurabile) sia visibile dalla vetrina in un catalogo condiviso, è necessario che siano soddisfatti i seguenti requisiti:

- Tutti i [prodotti associati](../catalog/product-configurations.md) e le opzioni devono essere assegnati allo stesso catalogo condiviso e abilitati nel catalogo principale.
- Per i prodotti [configurable](../catalog/product-create-configurable.md) e [grouped](../catalog/product-create-grouped.md), sono visibili solo i prodotti associati abilitati.
- Per un prodotto [bundle](../catalog/product-create-bundle.md), tutte le opzioni devono essere incluse nel catalogo condiviso.

  ![Seleziona prodotti per il catalogo](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Metodo 1: Aggiungere un singolo prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Per il prodotto nella griglia da aggiungere, passare alla colonna _[!UICONTROL Action]_e fare clic su **[!UICONTROL Edit]**.

1. Scorri verso il basso, espandi ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Product in Shared Catalogs]_ed effettua le seguenti operazioni:

   - Seleziona la casella di controllo di ciascun catalogo condiviso in cui deve essere visualizzato il prodotto. Per scegliere tutti i cataloghi, fare clic su **[!UICONTROL Select all]**.

     ![Prodotto in cataloghi condivisi](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Il nome di ogni catalogo selezionato viene visualizzato nel campo _[!UICONTROL Shared Catalogs]_.

     ![Cataloghi condivisi assegnati](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Fare clic su **[!UICONTROL Done]** per salvare le impostazioni.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Metodo 2: Aggiungere più prodotti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso nella griglia, passare alla colonna _[!UICONTROL Action]_e selezionare **[!UICONTROL Set Pricing and Structure]**.

1. Nell&#39;albero delle categorie eseguire una delle operazioni seguenti:

   - Per includere tutti i prodotti, fare clic su **[!UICONTROL Select all]** o selezionare la casella di controllo della categoria padre.
   - Per includere categorie specifiche di prodotti, seleziona la casella di controllo di ciascuna categoria che desideri includere.
   - Per includere o escludere un singolo prodotto, seleziona o deseleziona la casella di controllo del prodotto.

   La notazione sotto ogni categoria nella struttura mostra il numero di prodotti della categoria attualmente inclusi nel catalogo condiviso. La notazione sotto la [categoria principale](../catalog/category-root.md) mostra il numero totale di prodotti di tutte le categorie attualmente selezionate per il catalogo condiviso.

1. Per visualizzare i prodotti di categoria nella griglia, fare clic sul nome della categoria nella struttura.

   Quando si seleziona una categoria, si verifica quanto segue:

   - L&#39;interruttore nella prima colonna della griglia è impostato su `On` per ciascun prodotto selezionato.
   - Se un prodotto viene assegnato a più categorie e viene omesso in una di esse, rimane disponibile tramite le altre categorie e tramite [ricerca nel catalogo](../catalog/search.md).
   - Il sistema imposta automaticamente [Autorizzazioni categoria](../catalog/category-permissions.md) su `Allow` per i prodotti selezionati.
