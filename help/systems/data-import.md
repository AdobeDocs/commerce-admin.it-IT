---
title: Importare dati
description: Scopri le linee guida per l’importazione dei dati e come utilizzare le operazioni di importazione dei dati.
exl-id: caae8811-445e-49d4-aa90-226a355732bc
feature: Products, Customers, Data Import/Export
source-git-commit: 1c1327dbda76283ae28f761d1e523e049e0e492f
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%

---

# Importare dati

I dati per tutti i tipi di prodotto possono essere importati nello store. Inoltre, puoi importare prodotti, dati sui prezzi avanzati, dati sui clienti, dati sull’indirizzo del cliente e immagini dei prodotti. L&#39;importazione supporta le operazioni seguenti:

- Aggiungi/aggiorna
- Sostituisci
- Elimina

## Linee guida per l’importazione

### Nuove entità

- Le entità vengono aggiunte con i valori attributo specificati nel file CSV.
- Per un attributo obbligatorio senza valore predefinito impostato, l’entità (la riga o le righe corrispondenti) non può essere importata se non è presente alcun valore o se non è valido.
- Per un attributo obbligatorio con un set di valori predefinito, viene importata l’entità (la riga o le righe corrispondenti) e viene impostato il valore predefinito per l’attributo, se non è presente alcun valore o un valore non valido.
- Se i dati complessi non sono validi, l’entità (la riga o le righe corrispondenti) non può essere importata.

### Entità esistenti

- Per gli attributi che non sono dati complessi, i valori del file di importazione, inclusi i valori vuoti per gli attributi non obbligatori, sostituiscono i valori esistenti.
- Se per un attributo obbligatorio non è presente alcun valore o è presente un valore non valido, il valore esistente non viene sostituito.
- Se i dati complessi per l&#39;entità non sono validi, l&#39;entità (la riga o le righe corrispondenti) non può essere importata, ad eccezione del caso in cui è stata selezionata l&#39;opzione Elimina entità nel menu a discesa Comportamento importazione.

### Dati complessi

Se un attributo specificato nel file di importazione esiste e il relativo valore deriva da un insieme di valori definito, si applica quanto segue:

- Se il valore non è già incluso nel set di valori definito, è possibile importare la riga e impostare un valore predefinito per l&#39;attributo.
- Se il valore è già incluso nel set definito, la riga corrispondente non può essere importata.
- Se il file di importazione specifica un nome di attributo non ancora definito nel sistema, non viene creato e i relativi valori non vengono importati.

### File non validi

- Impossibile importare un file se tutte le righe non sono valide.
- Nel file di importazione è specificato un nome di dati complesso o di dati di servizio non esistenti, ad esempio una colonna con un&#39;intestazione `_<non-existing name>`.

Il processo di importazione di Adobe Commerce potrebbe non riconoscere correttamente i file codificati in UTF-8 che utilizzano un Byte Order Mark (BOM). I file contenenti una distinta base possono causare problemi o errori durante il processo di importazione.

## Operazioni di importazione

| Operazione | Descrizione |
| --------- | ----------- |
| Aggiungi/aggiorna | I nuovi dati di prodotto vengono aggiunti ai dati di prodotto esistenti per le voci esistenti nel database. È possibile aggiornare tutti i campi eccetto `sku`.<br><br>Le nuove classi di imposta specificate nei dati di importazione vengono create automaticamente.<br><br>Le nuove categorie di prodotti specificate nel file di importazione vengono create automaticamente.<br><br>I nuovi SKU specificati nel file di importazione vengono creati automaticamente <br><br>**_Nota:_**Per i prodotti, è possibile aggiornare tutti i campi eccetto SKU tramite l&#39;importazione.<br><br>**_Importante:_** Non è possibile rimuovere più valori di campo, ad esempio siti Web o categorie, utilizzando il comportamento di importazione _Aggiungi/Aggiorna_. Questi campi rimangono nel database dopo l’importazione se non sono elencati nel file CSV. |
| Sostituisci | I dati di prodotto esistenti vengono sostituiti con nuovi dati.<br><br>**_Importante:_**prestare attenzione durante la sostituzione dei dati perché i dati del prodotto esistenti vengono cancellati e tutti i riferimenti nel sistema vengono persi.<br><br>Se uno SKU nei dati di importazione corrisponde allo SKU di un&#39;entità esistente, tutti i campi, incluso lo SKU, vengono eliminati e viene creato un nuovo record utilizzando i dati CSV. Si verifica un errore se il file CSV fa riferimento a uno SKU che non esiste nel database. È possibile controllare i dati per visualizzare l&#39;errore. |
| Elimina | Tutte le entità presenti nel database vengono eliminate dal database.<br><br>L&#39;eliminazione ignora tutte le colonne nei dati di importazione, ad eccezione dello SKU. È possibile ignorare tutti gli altri attributi nei dati.<br><br>Si verifica un errore se il file CSV fa riferimento a uno SKU che non esiste nel database. È possibile controllare i dati per visualizzare l&#39;errore. |

{style="table-layout:auto"}

## Processo di importazione

La dimensione del file di importazione è determinata dalle impostazioni nel file `php.ini` sul server. Il messaggio di sistema nella pagina _Importa_ indica il limite di dimensioni corrente. La dimensione predefinita è 2 MB.

I caratteri speciali (come il segno di uguale, i simboli maggiore e minore di, le virgolette singole e doppie, la barra rovesciata, la barra verticale e i simboli della e commerciale) possono causare problemi durante il trasferimento dei dati. Per garantire la corretta interpretazione di tali caratteri speciali, è possibile contrassegnarli come _sequenza di escape_. Se ad esempio i dati includono una stringa di testo come `code="str"`, `code="str2"`, la scelta di racchiudere il testo tra virgolette garantisce che le virgolette doppie originali siano considerate parte dei dati. Quando il sistema rileva una doppia serie di virgolette doppie, è possibile comprendere che il set esterno di virgolette doppie racchiude i dati effettivi.

Durante l’importazione dei dati di prodotto, i nuovi dati di prodotto vengono aggiunti alle voci di dati di prodotto esistenti nel database. Tutti i campi ad eccezione di SKU possono essere aggiornati tramite l’importazione. Tutti i dati di prodotto esistenti vengono sostituiti con i nuovi dati importati. Presta attenzione durante la sostituzione dei dati. Tutti i dati di prodotto esistenti vengono cancellati e tutti i riferimenti nel sistema vengono persi.

![Importazione dati](./assets/import-options.png){width="600" zoomable="yes"}

### Passaggio 1: preparare i dati

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. In _Impostazioni importazione_, impostare **[!UICONTROL Entity Type]** su una delle opzioni seguenti:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers and Addresses`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

1. Fare clic su **[!UICONTROL Download Sample File]**.

1. Individua il file di esportazione nel percorso di download per il browser Web e apri il file.

   Il file di esempio include intestazioni di colonna con dati segnaposto per i tipi di prodotto.

   ![Importa file di esempio dei dati](./assets/data-export-sample-data.png){width="600" zoomable="yes"}

1. Esamina la struttura del file di esempio e utilizzala per preparare il file di importazione CSV, assicurandoti che le intestazioni delle colonne siano digitate correttamente.

1. Verifica che la dimensione del file di importazione non superi il limite mostrato nel messaggio.

   ![Notifica dimensioni importazione dati](./assets/data-import-size-notification.png){width="600"}

1. Se i dati di importazione includono percorsi di immagini di prodotto, accertati che i file di immagine siano stati caricati nella posizione appropriata.

   Il percorso predefinito nel server Commerce è: `pub/media/import`.

   Se le immagini risiedono su un server esterno, assicurati di disporre dell’URL completo della directory che le contiene.

### Passaggio 2: scegliere il comportamento di importazione

![Comportamento importazione dati](./assets/data-import-import-behavior.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Import Behavior]** su uno dei seguenti:

   - `Add/Update` (per i prodotti, è possibile aggiornare tutti i campi eccetto SKU tramite l&#39;importazione).
   - `Replace`
   - `Delete`

1. Per determinare cosa accade quando si verifica un errore durante l&#39;importazione dei dati, scegliere una delle opzioni seguenti:

   - `Stop on Error`
   - `Skip error entries`

1. Per **[!UICONTROL Allowed Errors Count]**, immettere il numero di errori che possono verificarsi prima dell&#39;annullamento dell&#39;importazione.

   Il valore predefinito è 10.

1. Accettare il valore predefinito di una virgola (`,`) per **[!UICONTROL Field separator]**.

1. Accettare il valore predefinito di una virgola (`,`) per **[!UICONTROL Multiple value separator]**.

   In un file CSV, il separatore predefinito è una virgola. Per utilizzare un carattere diverso, accertati che i dati nel file CSV corrispondano al carattere specificato.

1. Accettare il valore predefinito `_EMPTY_VALUE_` per **[!UICONTROL Empty attribute value constant]**.

1. Se si desidera racchiudere i caratteri speciali eventualmente presenti nei dati come _sequenza di escape_, selezionare la casella di controllo **[!UICONTROL Fields Enclosure]**.

### Passaggio 3: identificare il file di importazione

![File di importazione dati](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Choose File]** per selezionare il file da importare.

1. Trovare il file CSV che si è preparati a importare e fare clic su **[!UICONTROL Open]**.

1. Per **[!UICONTROL Images File Directory]**, immettere il percorso relativo della posizione sul server Commerce in cui sono archiviate le immagini caricate.

   Esempio: `product_images`.

   >[!NOTE]
   >
   >A partire dalla versione di Adobe Commerce e dal Magento Open Source `2.3.2`, il percorso specificato in _[!UICONTROL Images File Directory]_concatena l&#39;importazione nella directory base delle immagini: `<Magento-root-folder>/var/import/images`. Inserire ad esempio i file `product_images` nella cartella `<Magento-root-directory>/var/import/images/product_images`. La directory base delle immagini di importazione può essere configurata nel file `\Magento\ImportExport\etc\config.xml`. Se il modulo di archiviazione remota è abilitato, importare i file nella cartella `<remote-storage-root-directory>/var/import/images/product_images`.

   Per ulteriori informazioni sull&#39;importazione di immagini prodotto, vedere [Importare immagini prodotto](data-import-product-images.md).

### Passaggio 4: controllare i dati di importazione

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Check Data]**.

1. Attendere alcuni istanti per il completamento del processo di convalida.

   Se i dati di importazione sono validi, viene visualizzato il seguente messaggio:

   ![Messaggio di successo - file valido](./assets/data-import-validation-message.png){width="600"}

1. Se il file è valido, scegliere **[!UICONTROL Import]**.

   In caso contrario, correggere ogni problema relativo ai dati elencati nel messaggio e riprovare a importare il file.

1. Il processo di importazione continua fino alla fine dei dati, a meno che non si verifichi un errore.

   Se nei risultati della convalida viene visualizzato un messaggio di errore, correggere il problema nei dati e importare nuovamente il file.

   ![Messaggio di errore - La chiave URL esiste già](./assets/data-import-validation-error-url-key-exists.png){width="600"}

   Al termine dell’importazione viene visualizzato un messaggio.

## Cronologia importazione

Commerce mantiene un record dei dati importati nell’archivio, inclusi la data e l’ora di inizio, l’utente, l’ora di esecuzione e un collegamento al file importato. Il _Tempo di esecuzione_ è la durata del processo di importazione.

**_Per visualizzare la cronologia di importazione:_**

Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import History]**.

![Cronologia importazione dati](./assets/data-import-history.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Per impostazione predefinita, i file della cronologia di importazione si trovano nella cartella `<Magento-root-directory>/var/import_history`. Se il modulo di archiviazione remota è abilitato, i file di cronologia di importazione si trovano nella cartella `<remote-storage-root-directory>/import_export/import_history`.

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Numero interno utilizzato per designare un trasferimento. |
| [!UICONTROL Start Date & Time] | Una data e un’ora specifiche in cui è avvenuto il trasferimento. |
| [!UICONTROL User] | Il cliente che ha effettuato il trasferimento. |
| [!UICONTROL Imported file] | Collegamento per il download del file importato. |
| [!UICONTROL Error file] | Il file di errore corrispondente. |
| [!UICONTROL Execution Time] | Intervallo di tempo del processo di importazione. |
| [!UICONTROL Summary] | Il numero di elementi creati, aggiornati ed eliminati o il messaggio di errore. |

{style="table-layout:auto"}

Per scaricare il file _Imported/Error_, scegliere **[!UICONTROL Download]**.
