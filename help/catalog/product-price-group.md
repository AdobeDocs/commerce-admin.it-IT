---
title: Prezzi di gruppo
description: Scopri come utilizzare la determinazione prezzi di gruppo per impostare i prezzi per gli articoli scontati in base ai gruppi di clienti nel tuo negozio.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Prezzi di gruppo

Puoi utilizzare le impostazioni di configurazione del prodotto nell’amministratore per impostare i prezzi per gli articoli scontati in base ai gruppi di clienti nel tuo negozio. Questo modello di prezzo strategico è denominato _prezzi di gruppo_.

Il prezzo scontato di qualsiasi prodotto può essere offerto ai membri di un gruppo di clienti specifico quando l&#39;acquirente è connesso al loro account. Il prezzo del gruppo di clienti viene visualizzato nella pagina del prodotto insieme al prezzo regolare, in modo che un acquirente possa confrontare facilmente i prezzi e agire di conseguenza. Dopo aver aggiunto il prodotto al carrello, il prezzo regolare viene sostituito dal prezzo di gruppo in base al gruppo di clienti.

La determinazione dei prezzi per i gruppi di clienti è un componente di [prezzi su più livelli](product-price-tier.md) ed è impostato in modo simile. L&#39;unica differenza è che i prezzi del gruppo di clienti hanno una quantità pari a 1.

![Sconto gruppo clienti](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Vantaggi dell&#39;utilizzo dei prezzi di gruppo

- Adatto per acquirenti all&#39;ingrosso

- Incentivo per i clienti ad aggiornare il proprio gruppo di clienti per trarre vantaggio dagli sconti

- Campagne di marketing mirate

- Creare fiducia e credibilità premiando i clienti fedeli

## Imposta un prezzo di gruppo

1. Apri il prodotto in modalità di modifica.

1. Sotto _[!UICONTROL Price]_, fare clic su **[!UICONTROL Advanced Pricing]**.

1. In _[!UICONTROL Customer Group Price]_, fare clic su **[!UICONTROL Add]**.

   Se il tuo negozio include [B2B per Adobe Commerce](../b2b/introduction.md) e ha [cataloghi condivisi](../b2b/catalog-shared.md) abilitata, questa sezione è etichettata _[!UICONTROL Catalog and Tier Price]_.

   ![Advanced Pricing](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configura il prezzo di gruppo:

   - Per un&#39;installazione multisito, scegliere **[!UICONTROL Website]** se si applica il prezzo del gruppo.

   - Scegli la **[!UICONTROL Customer Group]** cioè ricevere lo sconto.

   - Immetti un **[!UICONTROL Quantity]** di `1`.

   - Per **[!UICONTROL Price]**, impostare il tipo di determinazione prezzi e l&#39;importo:

      - `Fixed` - Inserire il prezzo del prodotto scontato.

      - `Discount` - Inserire il prezzo scontato come percentuale del prezzo del prodotto.

     ![Determinazione prezzi gruppo clienti](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Per aggiungere un altro prezzo di gruppo, fare clic su **[!UICONTROL Add]** e ripetere il passaggio precedente.

1. Al termine, fai clic su **[!UICONTROL Done]** e poi **[!UICONTROL Save]**.

>[!NOTE]
>
>Il **_finale_** il prezzo del prodotto viene calcolato come **_minimo_** prezzo rilevante, utilizzando la formula seguente: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prezzo fisso_** Le opzioni personalizzabili del prodotto sono _non_ sono influenzati dalle regole Prezzo di gruppo, Prezzo livello, Prezzo speciale o Prezzo catalogo.
