---
title: Trasferimento dati
description: Scopri il supporto per il trasferimento di dati, inclusa la convalida dei dati.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Trasferimenti di dati

Utilizzare gli strumenti di importazione ed esportazione per gestire più record in un&#39;unica operazione. Puoi importare nuovi elementi, nonché aggiornare, sostituire ed eliminare i set di prodotti esistenti.

Ad esempio, puoi aggiungere nuovi prodotti al tuo inventario, aggiornare i dati sui prodotti e i dati sui prezzi avanzati e sostituire un set di prodotti esistenti con nuovi prodotti. Gli strumenti di importazione ed esportazione consentono di gestire in modo più efficiente i cataloghi di prodotti di grandi dimensioni, in quanto è possibile esportare i dati, modificarli in un foglio di calcolo e importarli nuovamente nel proprio archivio anziché eseguire più operazioni in Amministrazione.


>[!NOTE]
>
>Adobe Commerce supporta anche l’esportazione di dati SaaS per trasferire i dati di prodotto dal server Commerce ai servizi SaaS. L&#39;esportazione dei dati SaaS è integrata con i servizi SaaS di Commerce, tra cui [Product Recommendations](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=it), [Live Search](https://experienceleague.adobe.com/it/docs/commerce/live-search/overview) e [Catalog Service](https://experienceleague.adobe.com/it/docs/commerce/catalog-service/guide-overview). Per informazioni dettagliate, vedere la [Guida all&#39;esportazione dei dati SaaS](https://experienceleague.adobe.com/it/docs/commerce/saas-data-export/overview).

## Convalida dei dati

Tutti i dati devono superare la convalida per garantire la qualità, l’accuratezza e l’integrità dei valori prima di importarli nell’archivio. La convalida inizia quando si fa clic su **[!UICONTROL Check Data]**. Durante il processo, tutte le entità nel file di importazione vengono verificate per i seguenti elementi:

- **Attributi** - I nomi delle intestazioni di colonna vengono verificati per assicurarsi che corrispondano agli attributi corrispondenti nel database di sistema. Il valore di ogni attributo viene controllato per assicurarsi che soddisfi i requisiti del tipo di dati (decimal, integer, varchar, text e datetime).
- **Dati complessi** - I valori provenienti da un set definito, ad esempio un tipo di input a discesa o a selezione multipla, vengono verificati per verificare che i valori siano presenti nel set definito.
- **Dati del servizio** - I valori nelle colonne dei dati del servizio vengono verificati per garantire che le proprietà o i valori dei dati complessi siano coerenti con quelli già definiti nel database di sistema.
- **Valori richiesti** - Per le nuove entità, viene verificata la presenza dei valori di attributo richiesti nel file. Per le entità esistenti, non è necessario verificare nuovamente l&#39;esistenza dei valori di attributo richiesti.
- **Separatori** - Sebbene i separatori non siano visibili quando vengono visualizzati in un foglio di calcolo, i valori dei dati in un file CSV sono separati da virgole e i valori di testo sono racchiusi tra virgolette doppie. Durante il processo di convalida, viene verificata la formattazione dei separatori e di ogni insieme di virgolette che racchiude le stringhe di caratteri.

I risultati della convalida vengono visualizzati nella sezione Risultati convalida e includono le seguenti informazioni:

- Numero di entità controllate
- Numero di righe non valide
- Numero di errori rilevati

Se i dati sono validi, viene visualizzato un messaggio di _Importazione completata_.

![Messaggio di sistema - file valido](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Se la convalida non riesce, leggi la descrizione di ciascun errore e correggi il problema nel file CSV. Ad esempio, se una riga contiene uno SKU non valido, il processo di importazione si interrompe e tale riga e tutte le righe successive non vengono importate. Dopo aver risolto correttamente il problema, importa di nuovo i dati. Se si verificano molti errori, potrebbero essere necessari diversi tentativi per superare la convalida.

### Messaggi di convalida dei dati

#### Convalida

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Errori

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
