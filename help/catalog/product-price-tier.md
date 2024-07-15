---
title: Prezzi a livelli
description: Scopri come utilizzare la determinazione prezzi a livello per offrire uno sconto sulla quantità da un elenco di prodotti o da una pagina di prodotti.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
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
     >Per ottenere il prezzo scontato, la percentuale definita viene calcolata rispetto al valore definito nel campo _[!UICONTROL Price]_, non nel campo_[!UICONTROL Special Price]_.

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
