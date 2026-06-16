---
title: Importa prezzi livello
description: Scopri come esportare i dati dei prezzi a livello e importare i dati aggiornati.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/8eyWhVu-RtuzEYG81xOyqsEFdbz0s7evB-UGepUGCNw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 0%

---

# Importa prezzi livello

Anziché immettere manualmente [i prezzi di livello](../catalog/product-price-tier.md) per ciascun prodotto, può essere più efficiente [importare](data-import.md) i dati relativi ai prezzi. Prima di iniziare, creare un file di esempio dei dati dei prezzi dei livelli esportati che è possibile utilizzare come modello.

![Esempio di vetrina - prezzi su più livelli](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Passaggio 1: esportare i dati dei prezzi del livello

Nell&#39;esempio seguente vengono esportati i dati relativi ai prezzi dei livelli per un singolo prodotto. Quindi, puoi utilizzare i dati esportati come modello per le importazioni in blocco di dati relativi ai prezzi dei livelli. Per ulteriori informazioni sull&#39;esportazione dei dati di determinazione prezzi avanzata, vedere [Dati di determinazione prezzi avanzata](data-attributes-product.md#advanced-pricing-attributes).

![Prezzo su più livelli del prodotto](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. Nella barra laterale _Admin_, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. In _[!UICONTROL Export Settings]_, impostare **[!UICONTROL Entity Type]**su `Advanced Pricing`.

1. Nella griglia **[!UICONTROL Entity Attributes]**, scorrere verso il basso fino agli attributi SKU ed effettuare le seguenti operazioni:

   - Per i prezzi dei livelli basati su una percentuale di sconto, inserisci lo SKU di ciascun prodotto da esportare, separato da una virgola.

     ![Esportazione dati - SKU prodotto](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Per i prezzi dei livelli basati su un importo fisso, immettere lo SKU di ciascun prodotto.

   - Scorrere verso il basso e fare clic su **[!UICONTROL Continue]**.

1. Individua il file di esportazione nel percorso di download per il browser Web e apri il file.

   ![Esempio - dati prezzo livello sconto gruppo clienti esportati](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Dati prezzo livello esportati_**

Nei dati esportati sono incluse le seguenti colonne:

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

I dati esportati vengono utilizzati come modello per l&#39;importazione dei dati relativi ai prezzi dei livelli.

## Passaggio 2: aggiornare i dati

1. Aggiornare i dati relativi al prezzo del livello per ciascun prodotto, in base alle esigenze.

   Tutti i prodotti senza aggiornamenti di prezzo di livello possono essere eliminati dal file CSV. Non è necessario reimportare i prodotti che non sono stati modificati.

1. **[!UICONTROL Save]** il file CSV aggiornato.

>[!NOTE]
>
>Le dimensioni di un file di importazione non possono superare i 2 MB.

## Passaggio 3: importare i dati aggiornati

1. Nella barra laterale _Admin_, vai a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. In _Impostazioni importazione_, impostare **[!UICONTROL Entity Type]** su `Advanced Pricing`.

1. Imposta **[!UICONTROL Import Behavior]** su `Add/Update`.

1. In **[!UICONTROL File to Import]**, fare clic su **[!UICONTROL Choose File]** e selezionare il file che si è preparati a importare dalla directory.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Check Data]**.

1. Se il file è valido, scegliere **[!UICONTROL Import]**.

   In caso contrario, correggere ogni problema relativo ai dati elencati nel messaggio e riprovare a importare il file.
