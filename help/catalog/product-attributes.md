---
title: Panoramica degli attributi del prodotto
description: Scopri gli attributi del prodotto e come vengono utilizzati per descrivere le caratteristiche specifiche di un prodotto.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Panoramica degli attributi del prodotto

Gli attributi sono gli elementi costitutivi del catalogo dei prodotti e descrivono caratteristiche specifiche di un prodotto. Gli attributi del prodotto possono essere organizzati in [set di attributi](attribute-sets.md), che vengono quindi utilizzati come modelli per la creazione di prodotti.

Gli attributi determinano il tipo di controllo di input utilizzato per le opzioni prodotto e forniscono informazioni aggiuntive per le pagine prodotto. Vengono inoltre utilizzati come parametri e criteri di ricerca per la navigazione su più livelli, i rapporti di confronto dei prodotti e le promozioni. Puoi creare tutti gli attributi e le serie di attributi necessari per descrivere i prodotti nel catalogo. Oltre agli attributi che puoi creare, gli attributi di sistema, ad esempio prezzo, sono incorporati nella piattaforma Commerce di base e non possono essere modificati.

![Creazione di un nuovo attributo durante la modifica di un prodotto](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Quando pianifichi e crei attributi di prodotto, utilizza le best practice descritte nelle sezioni seguenti.

## Nomi di attributo

Stabilisci convenzioni coerenti per la denominazione degli attributi, incluse lettere maiuscole e minuscole e punteggiatura. Ad esempio: `Color:Green` e `Color:green` possono essere considerati come due diversi valori di attributo da parte di sistemi diversi. Tali disturbi nei dati possono influenzare le regole aziendali, i risultati di ricerca e i filtri di dati per le applicazioni che associano i prodotti alle regole.

## Uso attributo

Considera come utilizzare gli attributi durante l’assegnazione di proprietà e valori. Identifica gli attributi utilizzati come etichette per la presentazione, ad esempio il nome di un prodotto, l’immagine, il prezzo e la descrizione, e quali attributi vengono utilizzati per l’immissione dei dati. Considera come gli attributi vengono rappresentati in pagine diverse in tutto il sito e come appaiono sulle pagine delle categorie, sulle pagine dei dettagli del prodotto, sulle griglie delle categorie e sui cursori delle miniature.

## Colore

Le descrizioni a colori ad hoc possono rappresentare una sfida dal punto di vista delle operazioni del database. I nomi dei colori come &quot;Azure Skies&quot; o &quot;Robin Egg Blue&quot; sono molto interessanti, ma potrebbero non restituire i risultati migliori se utilizzati come criteri di ricerca o se il merchandising richiede di specificare `Color_Family:Blue`. Rifletti su come i colori vengono rappresentati nei risultati della ricerca e nella navigazione a più livelli, e stabilisci alcune linee guida per le tue esigenze aziendali. Quindi, cerca di essere coerente quando assegni i valori degli attributi colore in tutto il catalogo.

## Gestione delle varianti

Usa prodotto [opzioni di configurazione](product-configurations.md) e [prodotti configurabili](product-create-configurable.md) per gestire le varianti nelle offerte di prodotti. Queste funzioni semplificano la categorizzazione dei prodotti, la creazione di regole di prezzo del carrello e di regole di categorie dinamiche e l’offerta di una selezione di opzioni con vari tipi di input di testo, selezione e data.

## Ricerca ponderata

Attributi del prodotto abilitati per [ricerca nel catalogo](search.md) può essere assegnato un peso per dare loro un valore più alto nei risultati di ricerca. Gli attributi con un peso maggiore vengono restituiti prima di quelli con un peso inferiore. Ad esempio, considera due attributi nel sistema: _colore_ con un peso di ricerca di 3 e _descrizione_ con un peso di ricerca pari a 1. Ricerca della parola _rosso_ restituisce un elenco di prodotti con un attributo di colore impostato su `red`, ma non restituisce prodotti con descrizioni che contengono la parola _rosso_. In questo esempio, la proprietà `color` l&#39;attributo ha un peso definito maggiore del `description` attributo.

## Proprietà non utilizzate

Rimuovi le proprietà del prodotto non utilizzate per una migliore strutturazione e un’indicizzazione più rapida.
