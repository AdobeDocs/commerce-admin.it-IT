---
title: Scenari di messaggi azionari
description: Scopri la combinazione di impostazioni di configurazione che controllano i messaggi sulla disponibilità delle scorte nelle pagine dei prodotti e negli elenchi dei prodotti nelle pagine dei cataloghi.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%

---

# Scenari di messaggi azionari

Puoi utilizzare una combinazione di impostazioni di configurazione per controllare i messaggi sulla disponibilità delle scorte nelle pagine dei prodotti e negli elenchi dei prodotti nelle pagine del catalogo.

![Prodotto raggruppato con messaggio &quot;esaurito&quot;](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## Messaggi stock della pagina prodotto

Sono disponibili diverse varianti di messaggistica per la pagina del prodotto, a seconda della combinazione delle impostazioni Gestisci disponibilità Stock e Stock.

### Esempio 1: mostra messaggio di disponibilità

#### Scenario 1

Questa combinazione di impostazioni fa apparire il messaggio di disponibilità sulla pagina del prodotto, in base alla disponibilità di magazzino di ciascun prodotto.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### Scenario 2

Quando le scorte non sono gestite per un prodotto, questa combinazione di impostazioni può essere utilizzata per visualizzare il messaggio di disponibilità sulla pagina del prodotto.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### Esempio 2: nascondere il messaggio di disponibilità

#### Scenario 1

Questa combinazione di configurazione e impostazioni del prodotto impedisce la visualizzazione del messaggio di disponibilità nella pagina del prodotto.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | Nessuno |
|  | `Out of Stock` | Nessuno |

#### Scenario 2

Quando le scorte non vengono gestite per un prodotto, questa combinazione di configurazione e impostazioni del prodotto impedisce la visualizzazione del messaggio di disponibilità nella pagina del prodotto.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | Nessuno |

## Messaggi stock pagina catalogo

Le seguenti opzioni di visualizzazione sono disponibili per gli elenchi delle categorie e dei risultati di ricerca, a seconda della disponibilità del prodotto e delle impostazioni di configurazione.

![Messaggio esaurito sulla pagina della categoria](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### Esempio 1: mostrare il prodotto con il messaggio &quot;esaurito&quot;

Questa combinazione di impostazioni di configurazione include i prodotti esauriti negli elenchi delle categorie e dei risultati della ricerca e visualizza un messaggio &quot;esaurito&quot;.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | Nessuno |

### Esempio 2: mostrare il prodotto senza il messaggio &quot;esaurito&quot;

Questa combinazione di impostazioni di configurazione include i prodotti esauriti negli elenchi delle categorie e dei risultati della ricerca, ma non visualizza un messaggio.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | Nessuno |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### Esempio 3: nascondere il prodotto finché non è disponibile

Questa impostazione di configurazione omette completamente i prodotti di stock dagli elenchi delle categorie e dei risultati di ricerca fino a quando non sono di nuovo disponibili.

| Opzioni Stock | Impostazione | Messaggio |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | Nessuno |
