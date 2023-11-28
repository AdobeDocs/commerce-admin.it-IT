---
title: Gestisci scorte
description: Scopri come le scorte vengono utilizzate per rappresentare un inventario virtuale e aggregato dei prodotti per le origini dei canali di vendita.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Gestisci azioni

Le scorte rappresentano un inventario virtuale e aggregato dei prodotti per le origini dei canali di vendita (siti Web). A seconda della configurazione del sito, le scorte possono essere assegnate a uno o più canali di vendita. A ciascun canale di vendita può essere assegnato un solo magazzino e un singolo magazzino può essere assegnato a più canali di vendita. Attraverso le scorte, è possibile modificare la definizione delle priorità delle origini utilizzate quando gli ordini vengono inoltrati tramite un canale di vendita.

Si inizia con un Stock predefinito che non può essere rimosso o disabilitato. È possibile aggiungere ulteriori canali di vendita solo alle scorte. L&#39;unica origine assegnata è Origine predefinita. Questo stock viene utilizzato da commercianti single-source, integrazioni di terze parti e prodotti importati.

I Sales Channel rappresentano le entità che vendono il proprio inventario. Per impostazione predefinita, [!DNL Commerce] fornisce i siti Web dei punti vendita come canali di vendita. I canali di vendita possono essere estesi per supportare canali aggiuntivi, come gruppi di clienti B2B e visualizzazioni dei punti vendita. Ogni canale di vendita può essere associato a un solo Stock.

- **Supporto Sales Channel** - Attualmente i canali di vendita includono siti web preconfigurati. Puoi estendere i canali di vendita per includere opzioni personalizzate, come gruppi di clienti B2B e visualizzazioni del negozio. A ciascun canale di vendita può essere assegnato un solo stock. Un singolo stock può essere assegnato a più canali di vendita.
- **Mappa su origini** - A ogni stock possono essere assegnate una o più origini attivate o disattivate, calcolando l&#39;inventario aggregato virtuale per prodotto.
- **Evasione ordine prioritario** - L&#39;algoritmo di priorità predefinito per l&#39;algoritmo di selezione della sorgente utilizza l&#39;elenco di origini delle scorte dall&#39;alto verso il basso per l&#39;esecuzione degli ordini.

Il diagramma seguente consente di definire il funzionamento di un magazzino in relazione a origini e Sales Channel per un commerciante di un negozio di biciclette.

![Diagramma ad esempio scorte per un negozio](assets/diagram-stock.png){width="600" zoomable="yes"}

## Esempi di scorte per mountain bike e store

Tutti i negozi iniziano con un Magazzino predefinito. Deve rimanere `Enabled` per i seguenti motivi:

- Viene utilizzato quando si importano nuovi prodotti, assegnando automaticamente i prodotti all&#39;origine e al magazzino predefiniti per l&#39;accesso immediato a [!DNL Inventory Management].
- Non è possibile aggiungere altre origini oltre l&#39;origine di default a questo stock.
- È richiesto e utilizzato da commercianti single-source, prodotti bundle e prodotti raggruppati.

Per i commercianti multi-sorgente, crea e configura le scorte in modo che si adattino al meglio ai tuoi negozi e all’evasione degli ordini. Quando si assegnano nuove scorte a un canale di vendita, tutte le scorte preesistenti in tale canale di vendita vengono annullate.

Per un&#39;installazione multi-store, il magazzino predefinito viene inizialmente assegnato al [Sito Web principale](../stores-purchase/stores.md#add-websites){target="_blank"} e lo store predefinito. Le scorte e le quantità corrette vengono visualizzate per i prodotti abilitati e disabilitati in **[!UICONTROL Products]** vista griglia.

![Gestisci Stock](assets/inventory-stock.png){width="600" zoomable="yes"}

## Barra dei pulsanti

| Pulsante | Descrizione |
|--|--|
| [!UICONTROL Add New Stock] | Apre il _[!UICONTROL New Stock]_modulo utilizzato per inserire nuove scorte di magazzino per il mapping delle scorte al canale di vendita. |

## Descrizioni delle colonne Gestisci scorte

| Colonna | Descrizione |
|--|--|
| [!UICONTROL ID] | ID numerico univoco generato per l&#39;entrata di magazzino. |
| [!UICONTROL Name] | Nome univoco che identifica le scorte di magazzino. |
| [!UICONTROL Sales Channels] | Definisce l’ambito del titolo assegnando il titolo a siti web specifici come _canali di vendita_. |
| [!UICONTROL Assigned sources] | Origini assegnate alle scorte che forniscono tutte le quantità di prodotto. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Apre il record delle scorte di magazzino in modalità di modifica. |
