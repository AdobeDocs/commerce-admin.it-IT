---
title: Prezzi di gruppo
description: Scopri come utilizzare la determinazione prezzi di gruppo per impostare i prezzi per gli articoli scontati in base ai gruppi di clienti nel tuo negozio.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
TQID: https://experienceleague.adobe.com/OCeX5pLtUzWdwOW5W8qpI4DCeab2PTAVi5xF8HUr91A
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 0%

---

# Prezzi di gruppo

Puoi utilizzare le impostazioni di configurazione del prodotto nell’amministratore per impostare i prezzi per gli articoli scontati in base ai gruppi di clienti nel tuo negozio. Questo modello di determinazione dei prezzi strategico è denominato _prezzo di gruppo_.

Il prezzo scontato di qualsiasi prodotto può essere offerto ai membri di un gruppo di clienti specifico quando l&#39;acquirente è connesso al loro account. Il prezzo del gruppo di clienti viene visualizzato nella pagina del prodotto insieme al prezzo regolare, in modo che un acquirente possa confrontare facilmente i prezzi e agire di conseguenza. Dopo aver aggiunto il prodotto al carrello, il prezzo regolare viene sostituito dal prezzo di gruppo in base al gruppo di clienti.

La determinazione dei prezzi per i gruppi di clienti è un componente di [determinazione prezzi su più livelli](product-price-tier.md) ed è impostata in modo simile. L&#39;unica differenza è che i prezzi del gruppo di clienti hanno una quantità pari a 1.

![Sconto gruppo clienti](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Vantaggi dell&#39;utilizzo dei prezzi di gruppo

- Adatto per acquirenti all&#39;ingrosso

- Incentivo per i clienti ad aggiornare il proprio gruppo di clienti per trarre vantaggio dagli sconti

- Campagne di marketing mirate

- Creare fiducia e credibilità premiando i clienti fedeli

## Imposta un prezzo di gruppo

1. Apri il prodotto in modalità di modifica.

1. Sotto il campo _[!UICONTROL Price]_, fare clic su **[!UICONTROL Advanced Pricing]**.

1. Nella sezione _[!UICONTROL Customer Group Price]_, fare clic su **[!UICONTROL Add]**.

   Se il tuo archivio include [Adobe Commerce B2B](../b2b/introduction.md) e dispone di [cataloghi condivisi](../b2b/catalog-shared.md) abilitati, questa sezione è etichettata _[!UICONTROL Catalog and Tier Price]_.

   ![Determinazione prezzi avanzata](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configura il prezzo di gruppo:

   - Per un&#39;installazione multisito, scegliere **[!UICONTROL Website]** in cui si applica il prezzo di gruppo.

   - Scegliere **[!UICONTROL Customer Group]** per ricevere lo sconto.

   - Immettere **[!UICONTROL Quantity]** di `1`.

   - Per **[!UICONTROL Price]**, impostare il tipo di prezzo e l&#39;importo:

      - `Fixed` - Inserire il prezzo del prodotto scontato.

      - `Discount` - Inserire il prezzo scontato come percentuale del prezzo del prodotto.

     ![Determinazione prezzi gruppo clienti](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Per aggiungere un altro prezzo di gruppo, fare clic su **[!UICONTROL Add]** e ripetere il passaggio precedente.

1. Al termine, fare clic su **[!UICONTROL Done]** e quindi su **[!UICONTROL Save]**.

>[!NOTE]
>
>Il prezzo del prodotto **_final_** è calcolato come prezzo rilevante **_minimum_**, utilizzando la seguente formula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Le opzioni personalizzabili del prodotto_** a prezzo fisso sono _non_ influenzate dalle regole di prezzo di gruppo, prezzo di livello, prezzo speciale o prezzo di catalogo.
