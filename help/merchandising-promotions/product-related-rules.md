---
title: Regole prodotto correlate
description: Scopri le regole di prodotto correlate e come vengono utilizzate per presentare in modo dinamico ai clienti prodotti correlati, up-sell e cross-selling.
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Regole prodotto correlate (regole target)

{{ee-feature}}

Le regole di prodotto correlate consentono di eseguire il targeting della selezione di prodotti presentati ai clienti come prodotti correlati, up-sell e cross-selling. Ogni regola di prodotto può essere associata a un [segmento di clienti](../customers/customer-segments.md) per produrre una visualizzazione dinamica del merchandising mirato.

Poiché è possibile attivare più regole attive contemporaneamente, è possibile impostare una priorità per ogni regola. Definisce l’ordine in cui le regole vengono applicate e i prodotti vengono visualizzati nella pagina.

Per accedere alle regole prodotto correlate, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![Elenco regole prodotto correlate](./assets/related-products-rules.png){width="700" zoomable="yes"}

## Descrizioni delle colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Un identificatore numerico univoco assegnato a ogni regola di prodotto correlata |
| [!UICONTROL Rule] | Nome della regola prodotto correlata |
| [!UICONTROL Start] | Utilizzare i campi del calendario dinamico (_[!UICONTROL To:]_&#x200B;e&#x200B;_[!UICONTROL From:]_) per filtrare l&#39;elenco in base alla data di inizio della regola definita al momento della creazione della regola. |
| [!UICONTROL End] | Utilizzare i campi del calendario dinamico (_[!UICONTROL To:]_&#x200B;e&#x200B;_[!UICONTROL From:]_) per filtrare l&#39;elenco in base alla data di fine della regola definita al momento della creazione della regola. |
| [!UICONTROL Priority] | Immetti il testo in questo campo per filtrare l’elenco in base alla priorità definita per una regola. |
| [!UICONTROL Applies To] | Questa opzione filtra l&#39;elenco di regole applicabili a `Related Products`, `Up-sells` e `Cross-sells`. |
| [!UICONTROL Status] | Utilizzare questa opzione per filtrare l&#39;elenco in base allo stato della regola (`Active` o `Inactive`). |

{style="table-layout:auto"}

## Priorità delle regole

In qualsiasi momento, potrebbero essere presenti diverse regole attive che possono essere attivate per visualizzare prodotti correlati, up-sell e cross-selling. La priorità di ogni regola determina l’ordine in cui i prodotti vengono visualizzati nella pagina. Il valore può essere impostato su qualsiasi numero intero, con `1` che ha la priorità più alta.

Il numero di ID prodotto che possono essere inclusi in una regola di relazioni prodotto è determinato dal valore `Result Limit`, che ha un massimo di 20. Il valore `Result Limit`, combinato con `Configurable Maximum` per la promozione del prodotto basata su regole specifica, diventa `Real Limit` e determina il numero effettivo di prodotti corrispondenti che possono essere visualizzati nell&#39;elenco.

[Limite risultati] + [Massimo configurabile] = [Limite reale]

Si supponga ad esempio di disporre di tre regole con priorità `1`, `2` e `3`.

- Sono stati restituiti due prodotti corrispondenti per _Regola 1_, sei prodotti corrispondenti per _Regola 2_ e 20 prodotti corrispondenti per _Regola 3_.
- Nella configurazione, _[!UICONTROL Maximum Number of Products for Related Products List]_&#x200B;è impostato su `6`.

  | Regole | Priorità | Prodotti corrispondenti |
  |---|---|-----|
  | Regola 1 | `1` | `2` |
  | Articolo 2 | `2` | `6` |
  | Articolo 3 | `3` | `20` |

Se la prima regola restituisce più prodotti corrispondenti di quanto consentito dal _limite massimo configurabile_, ma inferiore al _limite reale_, i prodotti corrispondenti delle altre regole vengono utilizzati (in ordine di priorità) fino al raggiungimento del _limite reale_.

Per priorità, i prodotti corrispondenti restituiti da _Regola 1_ possono essere utilizzati prima per riempire tutti i 26 slot disponibili. Poiché la regola 1 ha restituito solo due prodotti corrispondenti, c&#39;è ancora spazio per altri 24. _La regola 2_ ha la priorità più alta e restituisce altri sei prodotti corrispondenti. Sono ora disponibili 18 slot da riempire. _La regola 3_ ha il livello di priorità successivo, con un numero sufficiente di prodotti corrispondenti per riempire i restanti 18 slot. Quando tutti gli slot disponibili sono riempiti e a seconda della modalità di rotazione impostata, i prodotti possono essere mischiati o ordinati per ID all&#39;interno di ogni priorità e quindi ridotti al limite massimo configurabile. In questo caso, i rimanenti sei prodotti vengono messi in vendita.

>[!NOTE]
>
>I prodotti selezionati vengono sempre visualizzati prima dei prodotti basati su regole, indipendentemente dalla modalità di rotazione.

## Configurare relazioni di prodotto basate su regole

Il comportamento delle regole di relazione del prodotto e la visualizzazione dei prodotti corrispondenti sono determinati dalle impostazioni di configurazione. Queste impostazioni determinano quanti dei prodotti che corrispondono alla regola possono essere visualizzati e l’ordine in cui compaiono.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Espansione](../assets/icon-display-expand.png) della sezione **[!UICONTROL Rules-Based Product Relations]**.

   ![Configurazione catalogo - relazioni prodotto basate su regole](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. Immettere **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. Imposta **[!UICONTROL Show Related Products]** su uno dei seguenti:

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. Imposta **[!UICONTROL Rotation Mode for Products in Related Product List]** su uno dei seguenti:

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. Per completare le impostazioni del prodotto di cross-selling, effettua le seguenti operazioni:

   - Immettere **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - Imposta **[!UICONTROL Show Cross-Sell Products]** su uno dei seguenti:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Imposta **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** su uno dei seguenti:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Per completare le impostazioni del prodotto di upselling, effettuare le seguenti operazioni:

   - Immettere **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - Imposta **[!UICONTROL Show Upsell Products]** su uno dei seguenti:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Imposta **[!UICONTROL Rotation Mode for Products in Upsell Product List]** su uno dei seguenti:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Modalità di rotazione

| Modalità | Descrizione |
|---|---|
| [!UICONTROL By Priority, Then by ID] | I prodotti vengono ordinati per priorità e quindi riordinati per ID all’interno di ogni priorità. I prodotti della regola di priorità inferiore vengono visualizzati solo quando non sono rimasti prodotti della regola di priorità superiore per riempire gli slot disponibili. |
| [!UICONTROL By Priority, Then Random] | I prodotti sono ordinati per priorità e quindi randomizzati all’interno di ogni priorità. I prodotti della regola di priorità inferiore vengono visualizzati solo quando non sono rimasti prodotti della regola di priorità superiore per riempire gli slot disponibili. |
| [!UICONTROL Weighted Random] | I prodotti vengono randomizzati in modo che i prodotti appartenenti a una regola con priorità maggiore abbiano una probabilità di apparire più elevata rispetto a quelli appartenenti a una regola con priorità inferiore. I prodotti vengono quindi ridotti al limite massimo configurabile e raggruppati per priorità. Questa modalità offre la possibilità ai prodotti con priorità inferiore di apparire a volte anche se gli slot rimanenti potrebbero essere riempiti con prodotti della regola con priorità più elevata |

{style="table-layout:auto"}

## Utilizzare i tipi di pubblico di Real-Time CDP per informare le regole di prodotto correlate

>[!NOTE]
>
>Questa funzione è in versione beta. Se desideri partecipare al programma beta, invia una richiesta a [dataconnection@adobe.com](mailto:dataconnection@adobe.com).


Scopri come [attivare](../customers/audience-activation.md) tipi di pubblico di Real-Time CDP nell&#39;istanza di Adobe Commerce per informare le regole di prodotto correlate.
