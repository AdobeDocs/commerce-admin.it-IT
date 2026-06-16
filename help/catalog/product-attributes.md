---
title: Panoramica degli attributi del prodotto
description: Scopri gli attributi del prodotto e come vengono utilizzati per descrivere le caratteristiche specifiche di un prodotto.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/reh5hq2WF3rmbKEKZiV8U18hfyLxXeUHHfJcUgWDcJ0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 547
ht-degree: 0%

---

# Panoramica degli attributi del prodotto

Gli attributi sono gli elementi costitutivi del catalogo dei prodotti e descrivono caratteristiche specifiche di un prodotto. Gli attributi del prodotto possono essere organizzati in [set di attributi](attribute-sets.md), che vengono quindi utilizzati come modelli per la creazione di prodotti.

Gli attributi determinano il tipo di controllo di input utilizzato per le opzioni prodotto e forniscono informazioni aggiuntive per le pagine prodotto. Vengono inoltre utilizzati come parametri e criteri di ricerca per la navigazione su più livelli, i rapporti di confronto dei prodotti e le promozioni. Puoi creare tutti gli attributi e le serie di attributi necessari per descrivere i prodotti nel catalogo. Oltre agli attributi che è possibile creare, gli attributi di sistema, ad esempio prezzo, sono incorporati nella piattaforma Commerce di base e non possono essere modificati.

![Creazione di un nuovo attributo durante la modifica di un prodotto](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Quando pianifichi e crei attributi di prodotto, utilizza le best practice descritte nelle sezioni seguenti.

## Nomi di attributo

Stabilisci convenzioni coerenti per la denominazione degli attributi, incluse lettere maiuscole e minuscole e punteggiatura. Ad esempio, `Color:Green` e `Color:green` potrebbero essere considerati come due valori di attributo diversi da sistemi diversi. Tali disturbi nei dati possono influenzare le regole aziendali, i risultati di ricerca e i filtri di dati per le applicazioni che associano i prodotti alle regole.

## Uso attributo

Considera come utilizzare gli attributi durante l’assegnazione di proprietà e valori. Identifica gli attributi utilizzati come etichette per la presentazione, ad esempio il nome di un prodotto, l’immagine, il prezzo e la descrizione, e quali attributi vengono utilizzati per l’immissione dei dati. Considera come gli attributi vengono rappresentati in pagine diverse in tutto il sito e come appaiono sulle pagine delle categorie, sulle pagine dei dettagli del prodotto, sulle griglie delle categorie e sui cursori delle miniature.

## Colore

Le descrizioni a colori ad hoc possono rappresentare una sfida dal punto di vista delle operazioni del database. I nomi dei colori, ad esempio &quot;Azure Skies&quot; o &quot;Robin Egg Blue&quot;, sono molto interessanti, ma potrebbero non restituire i risultati migliori se utilizzati come criteri di ricerca o se il merchandising richiede di specificare `Color_Family:Blue`. Rifletti su come i colori vengono rappresentati nei risultati della ricerca e nella navigazione a più livelli, e stabilisci alcune linee guida per le tue esigenze aziendali. Quindi, cerca di essere coerente quando assegni i valori degli attributi colore in tutto il catalogo.

## Gestione delle varianti

Utilizza le [opzioni di configurazione](product-configurations.md) e [prodotti configurabili](product-create-configurable.md) per gestire le varianti nelle offerte di prodotti. Queste funzioni semplificano la categorizzazione dei prodotti, la creazione di regole di prezzo del carrello e di regole di categorie dinamiche e l’offerta di una selezione di opzioni con vari tipi di input di testo, selezione e data.

## Ricerca ponderata

Agli attributi di prodotto abilitati per la [ricerca nel catalogo](search.md) può essere assegnato un valore più elevato nei risultati di ricerca. Gli attributi con un peso maggiore vengono restituiti prima di quelli con un peso inferiore. Consideriamo ad esempio due attributi nel sistema, _color_ con un peso di ricerca di 3 e _description_ con un peso di ricerca di 1. La ricerca della parola _red_ restituisce un elenco di prodotti con un attributo di colore `red`, ma non restituisce prodotti con descrizioni contenenti la parola _red_. In questo esempio, l&#39;attributo `color` ha un peso definito maggiore dell&#39;attributo `description`.

## Proprietà non utilizzate

Rimuovi le proprietà del prodotto non utilizzate per una migliore strutturazione e un’indicizzazione più rapida.


>[!NOTE]
>
>Per informazioni sull&#39;ottimizzazione della configurazione dell&#39;attributo del prodotto per le prestazioni, consulta [Best practice per la gestione del catalogo](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) nella _playbook di implementazione_.
