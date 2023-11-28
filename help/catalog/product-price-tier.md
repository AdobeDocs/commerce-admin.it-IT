---
title: Prezzi a livelli
description: Scopri come utilizzare la determinazione prezzi a livello per offrire uno sconto sulla quantità da un elenco di prodotti o da una pagina di prodotti.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Prezzi a livelli

I prezzi a livelli consentono di offrire uno sconto sulla quantità da un elenco di prodotti o da una pagina di prodotti nel negozio. Lo sconto può essere applicato a una visualizzazione negozio specifica, a un gruppo di clienti o a un catalogo condiviso.

Se sono presenti molti prodotti da aggiornare, è consigliabile importare le modifiche dei prezzi del livello anziché immetterle singolarmente. Per ulteriori informazioni, consulta [Importa prezzi livello](../systems/data-import-price-tier.md).

![Prezzo di listino su una pagina di prodotto della vetrina](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

La pagina del prodotto calcola lo sconto sulla quantità e visualizza un messaggio di tipo:

`Buy 6 for $5.95 each and save 15%`

I prezzi in vetrina hanno la precedenza dalla quantità più alta a quella più bassa. Se si dispone di un prezzo livello per la quantità `5` e uno per `10`, e un cliente aggiunge cinque, sei, sette, otto o nove articoli al carrello, il cliente riceve il prezzo scontato per la quantità `5` livello. Quando il cliente aggiunge il decimo articolo, il prezzo scontato specificato per la quantità `10` il livello sostituisce il livello per una quantità di `5`, e prezzo scontato per `10` applicabile.

## Aggiungere un livello di prezzo per un prodotto

1. Apri il prodotto in modalità di modifica.

1. Sotto _[!UICONTROL Price]_, fare clic su **[!UICONTROL Advanced Pricing]**.

1. In _[!UICONTROL Tier Price]_, fare clic su **[!UICONTROL Add]**.

   Se si sta creando un livello di più prezzi, fare clic su **[!UICONTROL Add]** per ogni livello aggiuntivo, in modo da poter lavorare tutti i livelli contemporaneamente. Ogni livello del gruppo ha lo stesso sito Web e lo stesso gruppo di clienti o un&#39;assegnazione di catalogo condivisa, ma con quantità e prezzo diversi.

## Configurare il livello del prezzo

1. Se il tuo negozio dispone di più siti web, scegli **[!UICONTROL Website]** per i quali si applica la determinazione dei prezzi secondo un livello.

1. Se necessario, limitare la disponibilità del piano tariffario selezionando **[!UICONTROL Customer Group]** o **[!UICONTROL Shared Catalog]** (![B2B per Adobe Commerce](../assets/b2b.svg) Disponibile con [B2B per Adobe Commerce](./b2b/../introduction.md) solo ).

1. Per **[!UICONTROL Qty]**, inserire la quantità che deve essere ordinata per ricevere lo sconto.

   - **Metodo 1:** Immetti il prezzo come importo fisso

     Imposta **[!UICONTROL Price]** a `Fixed` e inserire il prezzo adeguato per un&#39;unità di quel livello.

     ![Livello Prezzo come importo fisso](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Metodo 2:** Immetti il prezzo come percentuale

     Imposta **[!UICONTROL Price]** a `Discount` e inserire il prezzo scontato come percentuale del prezzo base del prodotto.

     Ad esempio, per uno sconto del 15%, immettere il numero `15`. Il prezzo viene salvato con due posizioni decimali, ad esempio `15.00`.)

     >[!NOTE]
     >
     >Per ottenere il prezzo scontato, la percentuale definita viene calcolata rispetto al valore definito nel _[!UICONTROL Price]_ non il campo _[!UICONTROL Special Price]_ campo.

     ![Livello prezzo in percentuale](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Completa la configurazione del prezzo

1. Per aggiungere un altro set di prezzi per un sito Web o un gruppo di clienti diverso, ripetere i passaggi precedenti.

1. Al termine, fai clic su **[!UICONTROL Done]** e poi **[!UICONTROL Save]**.

>[!NOTE]
>
>Il **_finale_** il prezzo del prodotto viene calcolato come **_minimo_** prezzo rilevante, utilizzando la formula seguente: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prezzo fisso_** Le opzioni personalizzabili del prodotto sono _non_ sono influenzati dalle regole Prezzo di gruppo, Prezzo livello, Prezzo speciale o Prezzo catalogo.
