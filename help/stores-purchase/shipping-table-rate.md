---
title: Tariffa tabella spedizione
description: Scopri come impostare un’opzione di spedizione con tariffa di tavolo per il tuo negozio.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 3%

---

# Tariffa tabella spedizione

Il _tariffa tabella_ il metodo di spedizione fa riferimento a una tabella di dati per calcolare le tariffe di spedizione in base a una combinazione di condizioni, tra cui:

- Peso rispetto alla destinazione
- Prezzo v. destinazione
- Numero di elementi rispetto alla destinazione

Ad esempio, se il tuo magazzino è a Los Angeles, spedire a San Diego costa meno che in Vermont. Puoi utilizzare le tariffe di spedizione per trasferire i risparmi ai tuoi clienti.

I dati utilizzati per calcolare le tariffe delle tabelle vengono preparati in un foglio di calcolo e importati nell&#39;archivio. Quando il cliente richiede un preventivo, i risultati vengono visualizzati nella sezione delle stime di spedizione del carrello.

>[!NOTE]
>
>È possibile attivare un solo set di dati sulla velocità della tabella alla volta.

![Tabella Tariffa spedizione opzione nel riepilogo ordine del carrello](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## Passaggio 1: completare le impostazioni predefinite

Il primo passo è quello di completare le impostazioni predefinite per le tariffe della tabella. Puoi completare questo passaggio senza modificare l’ambito della configurazione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In _[!UICONTROL Sales]_del pannello sinistro, scegliete **[!UICONTROL Delivery Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Table Rates]** sezione.

   >[!NOTE]
   >
   >Se necessario, cancellare prima **[!UICONTROL Use system value]** per modificare le seguenti impostazioni come descritto.

   ![Tariffe tabella](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enabled]** a `Yes`.

1. Inserisci il **[!UICONTROL Title]** che desideri visualizzare per la sezione tariffe tabella durante il pagamento.

   Il titolo predefinito è `Best Way`.

1. Inserisci il **[!UICONTROL Method Name]** che desideri visualizzare come etichetta accanto alla tariffa calcolata nel carrello.

1. Imposta **[!UICONTROL Condition]** a uno dei seguenti metodi di calcolo:

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Per gli ordini che includono prodotti virtuali, impostare **[!UICONTROL Include Virtual Products in Price Calculation]** a `Yes` se si desidera includere i prodotti virtuali nel calcolo.

   >[!NOTE]
   >
   >Poiché i prodotti virtuali, ad esempio i servizi, non hanno peso, non possono modificare il risultato di un calcolo basato sulla condizione Peso rispetto alla destinazione. Tuttavia, i prodotti virtuali possono modificare il risultato di un calcolo basato sulla condizione Prezzo v. Destinazione o Numero di articoli vs. Destinazione.

1. Configura le opzioni relative alle commissioni di gestione in base alle tue esigenze.

   La tariffa di imballaggio è facoltativa e viene visualizzata come un costo aggiuntivo che viene aggiunto alle spese di spedizione. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed`
      - `Percent`

   - Inserisci il **[!UICONTROL Handling Fee]** tasso secondo il metodo utilizzato per calcolare la tassa.

     Ad esempio, se l&#39;addebito è basato su un addebito fisso, immettere l&#39;importo come decimale, ad esempio `4.90`. Tuttavia, se la commissione di gestione si basa su una percentuale dell&#39;ordine, immettere l&#39;importo come percentuale. Ad esempio, se si sta addebitando il 6% dell&#39;ordine, immettere il valore come `.06`.

1. Se necessario, modificare il **[!UICONTROL Displayed Error Message]**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se questo metodo di consegna non è più disponibile.

1. Imposta **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione dell’archivio può utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, il _[!UICONTROL Ship to Specific Countries]_viene visualizzato. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

1. Imposta **[!UICONTROL Show Method if Not Applicable]** a `Yes` se si desidera visualizzare sempre le tariffe delle tabelle

1. Per **[!UICONTROL Sort Order]** Inserire un numero per determinare la sequenza di visualizzazione della funzione Tasso tabella per la spedizione, se elencata con altri metodi di consegna durante il pagamento.

   `0` = innanzitutto, `1` = secondo, `2` = terzo e così via.

1. Clic **[!UICONTROL Save Config]**.

## Passaggio 2: preparare i dati della velocità della tabella

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** a `Main Website`, o a qualsiasi altro sito web in cui si applica la configurazione.

   >[!NOTE]
   >
   >Se necessario, deselezionare **[!UICONTROL Use system value]** per modificare le seguenti impostazioni come descritto.

1. Modificare il **[!UICONTROL Condition]** secondo necessità.

1. Clic **[!UICONTROL Export CSV]**.

   ![Esporta CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Salva il `tablerates.csv` nel sistema.

1. Aprire il file in un&#39;applicazione per fogli di calcolo.

1. Completare la tabella con i valori appropriati per la condizione di calcolo della spedizione.

   - Utilizzare un asterisco (*) come carattere jolly che rappresenta tutti i valori possibili in qualsiasi categoria.
   - Il _[!UICONTROL Country]_deve contenere un [codice di tre caratteri valido][1] per ogni riga.
   - Ordina i dati per _[!UICONTROL Region/State]_in questo modo le posizioni specifiche si trovano nella parte superiore dell’elenco e le posizioni dei caratteri jolly nella parte inferiore. Questo metodo elabora le regole prima con i valori assoluti e successivamente con i valori jolly.
   - Valori in _[!UICONTROL Weight (and above)]_può contenere un massimo di quattro cifre decimali (ad esempio `2.5075`). L’utilizzo di più posizioni decimali nei dati causa un errore di importazione.

   ![Peso rispetto alla destinazione (Australia)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Salva il `tablerates.csv` file.

## Passaggio 3: importare i dati dei tassi della tabella

1. Torna a **[!UICONTROL Table Rates]** sezione della configurazione dello store.

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** al sito web in cui viene utilizzato questo metodo.

1. Per **[!UICONTROL Import]**, fai clic su **[!UICONTROL Choose File]** e seleziona la `tablerates.csv` file per importare le tariffe.

   ![Importa tassi tabella](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

## Passaggio 4: verificare le tariffe

Per verificare che i dati della tariffa della tabella siano corretti, eseguire il processo di pagamento con diversi indirizzi diversi per assicurarsi che le tariffe di spedizione e imballaggio siano calcolate correttamente.

### Esempio 1: prezzo e destinazione

In questo esempio viene utilizzata la condizione Prezzo v. Destinazione per creare una serie di tre diverse tariffe di spedizione in base all&#39;importo del subtotale dell&#39;ordine per gli Stati Uniti continentali, l&#39;Alaska e le Hawaii. L&#39;asterisco (*) è un carattere jolly che rappresenta tutti i valori.

| PAESE | REGIONE/STATO | CAP | SUBTOTALE ORDINE (e versioni successive) | PREZZO DI SPEDIZIONE |
|--- |--- |--- |--- |--- |
| Stati Uniti | CIAO | * | 100 | 10 |
| Stati Uniti | CIAO | * | 50 | 15 |
| Stati Uniti | CIAO | * | 0 | 20 |
| Stati Uniti | AK | * | 100 | 10 |
| Stati Uniti | AK | * | 50 | 15 |
| Stati Uniti | AK | * | 0 | 20 |
| Stati Uniti | * | * | 100 | 5 |
| Stati Uniti | * | * | 50 | 10 |
| Stati Uniti | * | * | 0 | 15 |

{style="table-layout:auto"}

### Esempio 2: peso e destinazione

In questo esempio viene utilizzata la condizione Peso rispetto alla destinazione per creare tariffe di spedizione diverse in base al peso dell&#39;ordine.

| PAESE | REGIONE/STATO | CAP | PESO (e superiore) | PREZZO DI SPEDIZIONE |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | WA | * | 9 | 39.95 |
| AUS | WA | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### Esempio 3: limitare la spedizione gratuita agli Stati Uniti continentali

1. Creare un `tablerates.csv` file che include tutte le destinazioni dello stato in cui sei disposto a fornire la spedizione gratuita.

1. Completa la configurazione della velocità della tabella con le seguenti impostazioni:

   | Impostazione | Valore |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** a `Main Website`, o a qualsiasi altro sito web in cui si applica la configurazione.

1. Per **[!UICONTROL Import]**, fai clic su **[!UICONTROL Choose File]** e seleziona la `tablerates.csv` file per importare le tariffe.


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
