---
title: Gestisci origini inventario
description: Scopri le origini e come definiscono le ubicazioni fisiche in cui viene gestito e spedito l’inventario dei prodotti per l’evasione degli ordini o dove sono disponibili i servizi.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Gestire le origini

Le origini sono le ubicazioni fisiche in cui l&#39;inventario dei prodotti viene gestito e spedito per l&#39;evasione degli ordini o in cui sono disponibili i servizi. Tali ubicazioni possono includere magazzini, magazzini fisici, centri di distribuzione, punti di prelievo e corrieri. Le quantità di magazzino vengono allocate a queste origini e [!DNL Commerce] aggrega automaticamente il totale dei prodotti vendibili per le scorte. Per le grandi aziende, aggiungi più origini per tutte le posizioni: in diverse posizioni geografiche per paese e continente, posizioni in una città, in base al tipo di inventario, anche in base ai servizi.

Durante la creazione di un’origine, si consiglia di fornire posizioni geografiche fisiche specifiche. Ciò consente _Algoritmo di priorità della distanza_ confrontare l&#39;ubicazione dell&#39;indirizzo di destinazione della spedizione con le ubicazioni di origine disponibili per determinare l&#39;origine più vicina per evadere le spedizioni. È possibile utilizzare Mappe Google o calcoli offline, che utilizzano i geocodici. Per ulteriori informazioni _Algoritmo di priorità della distanza_, vedi [Configura algoritmo di priorità della distanza](distance-priority-algorithm.md).

Inizia con _Origine predefinita_ che puoi aggiornare ma non disabilitare. Questa origine viene utilizzata dai commercianti single-source e per la migrazione dei prodotti. È sempre necessaria un&#39;origine predefinita.

- **Informazioni sulla posizione** - Ciascuna fonte include il nome, il paese, l&#39;indirizzo fisico della località e un punto di contatto.
- **Abilitazione delle risorse** - Se necessario, è possibile abilitare e disabilitare le origini. Abilitare un&#39;origine solo se accetta ed evade ordini e ordini inevasi.
- **Magazzino disponibile** - Assegna e aggiorna le quantità di magazzino per ogni origine tramite la pagina del prodotto. Le quantità di magazzino vengono calcolate, fornite e impegnate tramite il mapping di origine e di scorte.

Il diagramma seguente illustra le fonti per un commerciante di biciclette che vende una mountain bike, disponibili per le scorte e accessibili da SSA per le spedizioni.

![Esempio di diagramma delle sorgenti](assets/diagram-sources.png){width="600" zoomable="yes"}

Tutti gli archivi iniziano con un&#39;origine predefinita che deve rimanere abilitata:

- Tutti i nuovi prodotti importati in [!DNL Commerce] richiedono un&#39;origine e un magazzino, assegnati automaticamente per l&#39;accesso immediato a [!DNL Inventory Management].
- I commercianti con una sola origine utilizzano l&#39;origine predefinita come unico punto di ubicazione del magazzino e di spedizione.

## Modifica origini

È possibile aggiornare il nome, l&#39;indirizzo, la posizione GPS e le informazioni di contatto. Il codice sorgente è un valore protetto che funge da ID univoco associando la sorgente alle quantità e alle scorte dei tuoi prodotti.

Se si modifica Origine predefinita, è possibile modificare tutte le configurazioni ad eccezione del nome e del codice. È consigliabile che i commercianti single-source aggiungano informazioni corrispondenti alla loro posizione.

Il _[!UICONTROL Manage Sources]_nella pagina sono elencate tutte le ubicazioni di magazzino e le strutture di evasione disponibili. È possibile aggiungere nuove origini di magazzino e modificare le ubicazioni esistenti.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Per aggiungere un&#39;ubicazione di magazzino, vedere [Aggiunta di una nuova origine](sources-add.md).

1. Individuare l&#39;origine inventario e aprirla in _Modifica_ modalità.

1. Aggiorna le informazioni e salva le modifiche.

   ![Gestisci origini](assets/inventory-sources.png){width="600" zoomable="yes"}

## Barra dei pulsanti

| Pulsante | Descrizione |
|--|--|
| [!UICONTROL Add New Source] | Apre il modulo Nuova origine utilizzato per inserire una nuova origine magazzino, una struttura di evasione o una nuova ubicazione. |

## Gestire le descrizioni delle colonne delle origini

| Colonna | Descrizione |
|--|--|
| [!UICONTROL Code] | Codice alfanumerico univoco utilizzato dal sistema per identificare l&#39;origine dell&#39;inventario. |
| [!UICONTROL Name] | Un nome univoco che identifica l’origine dell’inventario per gli utenti amministratori. |
| [!UICONTROL Is Enabled] | Indica se l&#39;origine inventario è attiva e disponibile per l&#39;uso. |
| [!UICONTROL Pickup Location] | Indica se l&#39;origine è attiva come ubicazione di prelievo per [consegna in-store](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Clic **[!UICONTROL Edit]** apre il record origine inventario in modalità di modifica. |

## Altre colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Latitude] | Specifica la coordinata di latitudine dell&#39;origine inventario per GPS. Immetti il valore come numero, preceduto dal segno più o meno, a seconda delle necessità. Il simbolo di grado e le lettere non sono consentiti. Ad esempio: `32.7555` |
| [!UICONTROL State/Province] | Stato o provincia in cui si trova l&#39;origine. |
| [!UICONTROL Postcode] | Il codice postale o ZIP dell’origine. |
| [!UICONTROL Email] | Indirizzo e-mail del contatto principale. |
| [!UICONTROL Longitude] | Specifica la coordinata della longitudine dell&#39;origine di inventario per il GPS. Immetti il valore come numero, preceduto dal segno più o meno, a seconda delle necessità. Il simbolo di grado e le lettere non sono consentiti. Ad esempio: Longitudine -97,3308 |
| [!UICONTROL City] | La città in cui si trova la sorgente. |
| [!UICONTROL Phone] | Numero di telefono del contatto primario. |
| [!UICONTROL Country] | Il paese in cui si trova la sorgente. |
| [!UICONTROL Street] | Indirizzo della sorgente. |
| [!UICONTROL Fax] | L&#39;indicativo di località e il numero di fax del contatto principale. |
