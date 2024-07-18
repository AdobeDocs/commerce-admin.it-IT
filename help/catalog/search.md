---
title: Panoramica sulla ricerca nel catalogo
description: Scopri gli strumenti di ricerca rapida e avanzata che i clienti possono utilizzare per individuare i prodotti nella vetrina.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 65d295694e13be2e0a0de29b8b396faa9f2c9cd4
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Panoramica sulla ricerca nel catalogo

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) offre un&#39;esperienza di ricerca rapida, super rilevante e intuitiva ed è disponibile gratuitamente per Adobe Commerce. Questa sezione descrive la funzionalità di ricerca standard che potrebbe essere diversa da [!DNL Live Search].

Le ricerche mostrano che le persone che utilizzano la ricerca hanno più probabilità di effettuare un acquisto rispetto ai clienti che si affidano esclusivamente alla navigazione. Infatti, secondo alcuni studi, le persone che utilizzano la ricerca hanno quasi il doppio delle probabilità di effettuare un acquisto.

Le sezioni seguenti descrivono le funzionalità di base di ricerca nel catalogo. Per informazioni su come configurare e personalizzare le funzionalità native di ricerca nel catalogo, consulta:

- [Configura ricerca catalogo](search-configuration.md)
- [Risultati di ricerca](search-results.md)
- [Gestire i termini di ricerca](search-terms.md)

>[!NOTE]
>
>La funzionalità di ricerca nativa di Commerce fornisce risultati di ricerca con corrispondenza esatta. Mentre [!DNL Live Search], un modulo opzionale disponibile per l&#39;installazione e l&#39;abilitazione in Adobe Commerce, viene implementato in modo diverso e il risultato non è limitato alla stringa di ricerca esatta. Ad esempio, in cui sono presenti dieci prodotti etichettati numericamente per _Omega_: una ricerca per `Omega 1` genera una singola corrispondenza per _Omega 1_ con la funzionalità di ricerca nativa. Ma la stessa stringa di ricerca fornita da Live Search genera una corrispondenza per più elementi, _Omega 1_ e _Omega 10_.

## Ricerca rapida

>[!NOTE]
>
>Quando [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) è installato e il widget [[!DNL Storefront Popover]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/storefront-popover) è abilitato, la casella di ricerca restituisce &quot;cerca durante la digitazione&quot; e restituisce un pop-over.

La casella di ricerca nell’intestazione del negozio aiuta i visitatori a trovare i prodotti nel catalogo. Il testo da cercare può essere il nome completo o parziale del prodotto o qualsiasi altra parola o frase che descriva il prodotto. I termini di ricerca utilizzati dagli utenti per trovare i prodotti possono essere gestiti dall’amministratore.

1. Per **[!UICONTROL Search]**, il cliente immette le prime lettere di ciò che desidera trovare.

   Le corrispondenze nel catalogo vengono visualizzate di seguito, con il numero di risultati trovati.

1. Il cliente preme il tasto Invio o fa clic su un risultato nell’elenco dei prodotti corrispondenti.

   ![Ricerca](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Ricerca avanzata

>[!NOTE]
>
>La funzionalità di ricerca avanzata dei moduli qui descritta non è applicabile a [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La funzione Ricerca avanzata consente agli acquirenti di cercare il catalogo in base ai valori immessi in un modulo. Poiché il modulo contiene più campi, una singola ricerca può includere diversi parametri. Il risultato è un elenco di tutti i prodotti del catalogo che corrispondono ai criteri. Un collegamento a Ricerca avanzata si trova nel piè di pagina del negozio.

![Ricerca avanzata](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Ogni campo nel modulo corrisponde a un attributo del catalogo prodotti. Per aggiungere un campo, impostare le proprietà front-end dell&#39;attributo su `Include in Advanced Search`. Come best practice, includi solo i campi che i clienti molto probabilmente utilizzeranno per trovare un prodotto, perché la presenza di troppi elementi rallenta la ricerca.

1. Nel piè di pagina dell&#39;archivio, il cliente fa clic su **[!UICONTROL Advanced Search]**.

1. Nel modulo _Ricerca avanzata_, aggiunge valori completi o parziali in tutti i campi necessari.

1. Fai clic su **[!UICONTROL Search]** per visualizzare i risultati.

   ![Risultati ricerca](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Se il cliente non visualizza i risultati della ricerca, fa clic su **[!UICONTROL Modify your search]** e prova con un&#39;altra combinazione di criteri.
