---
title: Prezzo minimo pubblicizzato
description: Scopri come utilizzare la funzione MAP (Minimum Advertised Price) per restare conformi ai requisiti del produttore con prezzi speciali.
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---

# Prezzo minimo pubblicizzato

Ai commercianti è talvolta vietato visualizzare un prezzo inferiore al prezzo al dettaglio consigliato dal produttore (MSRP). Il prezzo minimo annunciato (MAP) consente di rimanere in conformità con i requisiti del produttore offrendo al contempo ai clienti un prezzo migliore. Poiché i requisiti variano da un produttore all&#39;altro, è possibile configurare il negozio per impedire la visualizzazione del prezzo effettivo su pagine in cui non è consentito.

La funzione MAP aggiunge un link dedicato _Fai clic per il prezzo_ invece del prezzo normale del prodotto. Se il prezzo nel tuo negozio è inferiore al prezzo minimo impostato per quel prodotto, ci sono due modi in cui le informazioni sui prezzi possono essere gestite sul negozio. Il primo è che il prezzo non viene visualizzato. Se l&#39;acquirente fa clic sul pulsante _Fai clic per il prezzo_, solo il prezzo effettivo al quale stai vendendo il prodotto diventa visibile. Il secondo modo è che il prezzo di listino/di mercato viene visualizzato con una barratura per sottolineare che il prezzo è più basso.

Inoltre, la funzione MAPPA consente di suggerire alcuni miglioramenti. Ad esempio, quando un cliente aggiunge un prodotto di questo tipo al carrello, non viene reindirizzato al carrello e vengono invece visualizzate delle offerte che consentono all’acquirente di:

- Rimuovere un articolo dal carrello (può essere fatto se l&#39;acquirente vuole solo chiarire il prezzo e non ha ancora preso una decisione di acquisto)

- Lascialo nel carrello e continua a fare acquisti

- Procedi con il pagamento

## Logica MAP

Alcuni prodotti hanno prezzi che dipendono da un’opzione selezionata, ad esempio opzioni personalizzate o prodotti semplici con SKU e gestione delle scorte. Per questi prodotti, viene applicata la logica seguente, in base al tipo di prodotto e all’impostazione del prezzo. Il prezzo effettivo viene utilizzato dalla gestione degli ordini, dagli strumenti di gestione dei clienti e dai rapporti.

## Utilizzo di MAP con i tipi di prodotto

| Tipo di prodotto | Descrizione |
|--- |--- |
| [Semplice](product-create-simple.md), [Virtuale](product-create-virtual.md) | Il prezzo effettivo non viene visualizzato automaticamente nelle pagine elenco catalogo e prodotto, ma viene incluso solo in base all&#39;impostazione [!UICONTROL Display Actual Price]. I prezzi delle opzioni personalizzati vengono visualizzati normalmente. |
| [Raggruppato](product-create-grouped.md) | I prezzi dei prodotti semplici associati non vengono visualizzati automaticamente nell&#39;elenco dei cataloghi e nelle pagine dei prodotti, ma vengono inclusi solo in base all&#39;impostazione [!UICONTROL Display Actual Price]. |
| [Configurabile](product-create-configurable.md) | Il prezzo effettivo non viene visualizzato automaticamente nelle pagine elenco catalogo e prodotto, ma viene incluso solo in base all&#39;impostazione [!UICONTROL Display Actual Price]. I prezzi delle opzioni vengono visualizzati normalmente. |
| [Bundle](product-create-bundle.md) (a prezzo fisso) | Il prezzo effettivo non viene visualizzato automaticamente nelle pagine del catalogo, ma viene incluso solo in base all&#39;impostazione [!UICONTROL Display Actual Price]. I prezzi degli elementi del bundle vengono visualizzati normalmente. MAP non è disponibile per i prodotti in bundle con prezzo dinamico. |
| [Scaricabile](product-create-downloadable.md) | Il prezzo effettivo non viene visualizzato automaticamente nelle pagine elenco catalogo e prodotto, ma viene incluso solo in base all&#39;impostazione [!UICONTROL Display Actual Price]. Il prezzo associato a ciascun collegamento di download viene visualizzato normalmente. |

{style="table-layout:auto"}

## Utilizzo di MAP con le impostazioni dei prezzi

| Fissazione del prezzo | Descrizione |
|--- |--- |
| Prezzo principale | Quando MAP viene applicato al prezzo principale, i prezzi delle opzioni, degli articoli del bundle e dei prodotti associati (che aggiungono o sottraggono dal prezzo principale) appaiono normalmente. |
| Prezzo prodotto associato | Se un prodotto non ha un prezzo principale e il suo prezzo è derivato dai prezzi del prodotto associati (ad esempio in un prodotto raggruppato), vengono applicate le impostazioni MAP dei prodotti associati. |
| [MSRP](product-price-minimum-advertised.md) | Se per un prodotto nel carrello è specificato il prezzo di vendita consigliato (MSRP) del produttore, il prezzo non viene barrato. |
| [Prezzo livello](product-price-tier.md) | Se è stata impostata la determinazione prezzi per il livello, il messaggio relativo non viene visualizzato nel catalogo. Nella pagina del prodotto, viene visualizzata una notifica che indica che il prezzo può essere inferiore quando si ordina più di una determinata quantità, ma che lo sconto viene visualizzato solo in percentuale. Per i prodotti associati di un prodotto raggruppato, gli sconti non vengono visualizzati nella pagina del prodotto. Il prezzo del livello viene visualizzato in base all&#39;impostazione Visualizza prezzo effettivo. |
| [Prezzo speciale](product-price-special.md) | Se è specificato il prezzo speciale, il prezzo speciale viene visualizzato in base all&#39;impostazione Visualizza prezzo effettivo. |

## Configurazione MAP

Per impostazione predefinita, la funzione MAP (Minimum Advertised Price) non è abilitata. Se desideri aggiungere questa funzionalità al negozio, devi abilitarla e configurare le impostazioni MAP per i tuoi prodotti. Le impostazioni MAP possono essere applicate a tutti i prodotti nel catalogo o configurate per prodotti specifici. Quando MAP è abilitato a livello globale, tutti i prezzi dei prodotti nella vetrina sono nascosti. Sono disponibili varie opzioni di configurazione che è possibile utilizzare per mantenere la conformità con i termini del contratto stipulato con il produttore, pur offrendo ai clienti un prezzo migliore.

![Il Prezzo Effettivo Viene Visualizzato Come &quot;Su Gesto&quot;](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"}

A livello globale, puoi abilitare o disabilitare MAP, applicarlo a tutti i prodotti, definire come viene visualizzato il prezzo effettivo. È inoltre possibile modificare il testo dei messaggi correlati e delle descrizioni delle informazioni visualizzate nell&#39;archivio.

Quando MAP è abilitato, le impostazioni MAP a livello di prodotto diventano disponibili. È possibile applicare MAP a un singolo prodotto inserendo il piano MSRP e scegliendo come si desidera che il prezzo effettivo venga visualizzato nel negozio. Le impostazioni MAP a livello di prodotto sovrascrivono le impostazioni MAP globali.

![Fare clic per il prezzo](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### Passaggio 1: abilitare MAP per la visualizzazione punto vendita

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Se applicabile, impostare **[!UICONTROL Store View]** nell&#39;angolo superiore destro della visualizzazione in cui si applica la configurazione.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Minimum Advertised Price]_.

1. Se necessario, impostare **Abilita MAP** su `Yes`.

   ![Configurazione MAPPA](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni di configurazione, vedi [_Prezzo minimo annunciato_](../configuration-reference/sales/sales.md#minimum-advertised-price) nella _Guida di riferimento alla configurazione_.

### Passaggio 2: configurare le impostazioni MAP

Per configurare le impostazioni MAP, utilizzare uno dei metodi seguenti:

#### Metodo 1: configurare MAP per tutti i prodotti

1. Per determinare quando e dove il prezzo effettivo deve essere visibile ai clienti, eseguire le operazioni seguenti:

   - Per modificare il valore predefinito, deselezionare la casella di controllo **[!UICONTROL Use system value]**.

   - Impostare **Visualizza prezzo effettivo** su uno dei valori seguenti:
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. Immettere il testo da visualizzare in **[!UICONTROL Default Popup Text Message]**.

1. Immettere una spiegazione aggiuntiva da visualizzare in **[!UICONTROL Default "What's This" Text Message]**.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

#### Metodo 2: configurare MAP per un singolo prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. Aprire il prodotto in modalità **[!UICONTROL Edit]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced Settings]** e scegli **[!UICONTROL Advanced Pricing]**.

   >[!NOTE]
   >
   >I campi [!UICONTROL Manufacturer's Suggested Retail Price] e [!UICONTROL Display Actual Price] vengono visualizzati solo quando [Prezzo minimo annunciato](../configuration-reference/sales/sales.md#minimum-advertised-price) è abilitato nella configurazione.

1. Immettere **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP).

   In questo esempio, il prezzo del prodotto è pari a 54,00 $ e il prezzo consigliato è 59,95.

   ![Prezzo di vendita consigliato dal produttore](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Display Actual Price]** su uno dei seguenti:

   - `Use config` - (predefinito) Applica le impostazioni di visualizzazione come [configurato](../configuration-reference/sales/sales.md#minimum-advertised-price) per l&#39;archivio. |
   - `On Gesture` - Visualizza il prezzo effettivo del prodotto in un popup quando il cliente fa clic su _Fai clic per il prezzo_ o _Cos&#39;è questo?Collegamento_.
   - `In Cart` - Visualizza il prezzo effettivo del prodotto nel carrello.
   - `Before Order Confirmation` - Visualizza il prezzo effettivo del prodotto al termine del processo di pagamento, immediatamente prima della conferma dell&#39;ordine.

1. Al termine, fare clic su **[!UICONTROL Done]** e quindi su **[!UICONTROL Save]**.
