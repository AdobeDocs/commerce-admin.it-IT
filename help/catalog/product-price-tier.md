---
title: Prezzi a livelli
description: Scopri come utilizzare la determinazione prezzi a livello per offrire uno sconto sulla quantità da un elenco di prodotti o da una pagina di prodotti.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Prezzi a livelli

I prezzi a livelli consentono di offrire uno sconto sulla quantità da un elenco di prodotti o da una pagina di prodotti nel negozio. Lo sconto può essere applicato a una visualizzazione negozio specifica, a un gruppo di clienti o a un catalogo condiviso.

Se sono presenti molti prodotti da aggiornare, è consigliabile importare le modifiche dei prezzi del livello anziché immetterle singolarmente. Per ulteriori informazioni, vedere [Importa prezzi livello](../systems/data-import-price-tier.md).

![Prezzo di livello in una pagina di prodotto della vetrina](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

La pagina del prodotto calcola lo sconto sulla quantità e visualizza un messaggio di tipo:

`Buy 6 for $5.95 each and save 15%`

I prezzi in vetrina hanno la precedenza dalla quantità più alta a quella più bassa. Se si dispone di un prezzo livello per la quantità `5` e uno per `10` e un cliente aggiunge cinque, sei, sette, otto o nove articoli al carrello, il cliente riceve il prezzo scontato per il livello quantità `5`. Quando il cliente aggiunge il decimo articolo, il prezzo scontato specificato per il livello quantità `10` sostituisce il livello per una quantità di `5` e viene applicato il prezzo scontato per `10`.

## Aggiungere un livello di prezzo per un prodotto

1. Apri il prodotto in modalità di modifica.

1. Sotto il campo _[!UICONTROL Price]_, fare clic su **[!UICONTROL Advanced Pricing]**.

1. Nella sezione _[!UICONTROL Tier Price]_, fare clic su **[!UICONTROL Add]**.

   Se si sta creando un livello di più prezzi, fare clic su **[!UICONTROL Add]** per ogni livello aggiuntivo, in modo da poter lavorare tutti i livelli contemporaneamente. Ogni livello del gruppo ha lo stesso sito Web e lo stesso gruppo di clienti o un&#39;assegnazione di catalogo condivisa, ma con quantità e prezzo diversi.

## Configurare il livello del prezzo

1. Se lo store dispone di più siti Web, scegliere **[!UICONTROL Website]** a cui si applica il prezzo del livello.

1. Se necessario, limitare la disponibilità del piano tariffario selezionando **[!UICONTROL Customer Group]** o **[!UICONTROL Shared Catalog]** (![Adobe Commerce B2B](../assets/b2b.svg) Disponibile solo con [Adobe Commerce B2B](./b2b/../introduction.md)).

1. Per **[!UICONTROL Qty]**, immettere la quantità che deve essere ordinata per ricevere lo sconto.

   - **Metodo 1:** Immettere il prezzo come importo fisso

     Impostare **[!UICONTROL Price]** su `Fixed` e immettere il prezzo adeguato per un&#39;unità in quel livello.

     ![Livello prezzo come importo fisso](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Metodo 2:** Immettere il prezzo come percentuale

     Impostare **[!UICONTROL Price]** su `Discount` e immettere il prezzo scontato come percentuale del prezzo di base del prodotto.

     Ad esempio, per uno sconto del 15%, immettere il numero `15`. Il prezzo viene salvato con due posizioni decimali, ad esempio `15.00`.

     >[!NOTE]
     >
     >Per ottenere il prezzo scontato, la percentuale definita viene calcolata rispetto al valore definito nel campo _[!UICONTROL Price]_, non nel campo&#x200B;_[!UICONTROL Special Price]_.

     ![Tier Price as a Percentage](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Completa la configurazione del prezzo

1. Per aggiungere un altro set di prezzi per un sito Web o un gruppo di clienti diverso, ripetere i passaggi precedenti.

1. Al termine, fare clic su **[!UICONTROL Done]** e quindi su **[!UICONTROL Save]**.

>[!NOTE]
>
>Il prezzo del prodotto **_final_** è calcolato come prezzo rilevante **_minimum_**, utilizzando la seguente formula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Le opzioni personalizzabili del prodotto_** a prezzo fisso sono _non_ influenzate dalle regole di prezzo di gruppo, prezzo di livello, prezzo speciale o prezzo di catalogo.

## Abilita determinazione prezzi livello per le regole prezzi catalogo

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."}

[!BADGE Sandbox]{type=Caution tooltip="Gli elementi elencati sono attualmente disponibili solo negli ambienti Sandbox. Adobe rende disponibili le nuove versioni negli ambienti Sandbox per consentire di testare le modifiche imminenti prima che siano disponibili negli ambienti di produzione."}

Nelle versioni precedenti di Commerce, non era possibile utilizzare i prezzi dei livelli insieme alle regole dei prezzi di catalogo. Le regole del catalogo ignorano la configurazione del prezzo livello e calcolano gli sconti solo dal prezzo base originale. Utilizzando Adobe Commerce as a Cloud Service, è ora possibile scegliere di includere la determinazione dei prezzi dei livelli nel calcolo delle regole dei prezzi di catalogo.

Per abilitare questa funzionalità:

1. Passare a **[!UICONTROL Stores]** > *[!UICONTROL Settings]* > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Promotions]** e impostare il campo **[!UICONTROL Apply Catalog Price Rule on Grouped Price]** su **[!UICONTROL Yes]**.

   ![Abilita determinazione prezzi livello per le regole prezzi catalogo](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. Definire un prezzo di livello con una quantità di `1` per ogni gruppo di clienti specifico o catalogo condiviso (ad esempio `Wholesale`, `Retail` o gruppo definito dall&#39;esercente) di cui si desidera eseguire il targeting con le regole del prezzo di catalogo. Impossibile utilizzare il gruppo clienti `ALL GROUPS` e il catalogo condiviso `Default` per questo scopo. La determinazione prezzi a livello non è abilitata per alcun gruppo per il quale non è stato definito un prezzo a livello con una quantità di `1`.

1. Definire prezzi di livello aggiuntivi con quantità maggiori di `1` in base alle esigenze. Questi prezzi di livello aggiuntivi verranno applicati come di consueto quando il cliente aggiunge quantità aggiuntive del prodotto al carrello. Le regole del prezzo del catalogo non verranno applicate a questi prezzi di livello aggiuntivi.

Per illustrare il funzionamento della determinazione dei prezzi per livello con le regole dei prezzi di catalogo durante l&#39;acquisto di un singolo prodotto, considerare l&#39;esempio seguente:

- Il prezzo base standard di un prodotto è di 100 USD.
- È stato definito un prezzo di livello per il gruppo di clienti `Wholesale` con una quantità di `1` e un prezzo fisso di 90 USD.
- Una regola del prezzo di catalogo fornisce uno sconto del 10% per il gruppo di clienti `Wholesale`.

Quando è abilitata la determinazione prezzi per il livello per le regole dei prezzi di catalogo, il sistema utilizza il flusso seguente per calcolare il prezzo finale:

1. Prima che il cliente effettui l’accesso, il prezzo del prodotto viene visualizzato come 100 USD (il prezzo base standard).

1. Dopo che il cliente ha effettuato l&#39;accesso come membro del gruppo `Wholesale`, il prezzo del prodotto viene adeguato a 90 USD (il prezzo di livello per il gruppo `Wholesale`).

1. Viene applicata la regola del prezzo di catalogo, che fornisce uno sconto del 10% sul prezzo di livello di 90 USD, risultante in un prezzo finale di 81 USD.

Nella tabella seguente vengono riepilogati i calcoli dei prezzi quando è abilitata la determinazione dei prezzi del livello per le regole dei prezzi di catalogo e una regola dei prezzi di catalogo fornisce uno sconto del 10% per tutti i gruppi di clienti:

Prodotto: prezzo standard $100 (acquisto singolo articolo)

| Gruppo di clienti | Prezzo livello (Qtà=1) | Nuovo prezzo base | Prezzo finale |
|---|---|---|---|
| TUTTI I GRUPPI | Non configurato | $ 100 | $100 - 10% = $90 |
| Commercio all&#39;ingrosso | Fisso: $ 85 | $ 85 | $85 - 10% = $76,50 |
| Retailer | 20% di sconto | $ 80 | $80 - 10% = $72,00 |
| VIP | Sconto del 15% | $ 85 | $85 - 10% = $76,50 |
