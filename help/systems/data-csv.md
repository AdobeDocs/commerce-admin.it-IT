---
title: File di dati CSV
description: Scopri la struttura utilizzata nel file CSV per supportare l’importazione e l’esportazione dei dati.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# File di dati CSV

Il formato di file con valori separati da virgola (CSV) viene utilizzato come base per le operazioni di trasferimento dei dati ed è supportato da tutte le applicazioni per fogli di calcolo e database. Per l&#39;importazione e l&#39;esportazione sono supportati i seguenti tipi di file:

- Importa: `CSV` e `ZIP` (file CSV compresso)
- Esporta: `CSV`

>[!IMPORTANT]
>
>Per modificare i file CSV, si consiglia di utilizzare un programma che supporti la codifica UTF-8, ad esempio Blocco note++. Microsoft® Excel inserisce caratteri aggiuntivi nell’intestazione di colonna del file CSV, impedendo in tal modo la reimportazione dei dati in Commerce. Se utilizzi Mac, puoi salvare i dati in formato CSV (Windows).

I file CSV hanno una struttura specifica che deve corrispondere al database. Ogni intestazione di colonna corrisponde al codice attributo del campo rappresentato dalla colonna. Per garantire che le intestazioni di colonna possano essere lette da Commerce, esporta innanzitutto i dati dall’archivio come file CSV. Puoi quindi modificare i dati e importarli nuovamente in Commerce.

Se apri un file CSV esportato in un editor di testo, i valori sono separati da virgole e più valori sono racchiusi tra virgolette doppie. Durante l’importazione, puoi specificare un separatore personalizzato, anche se l’impostazione predefinita è la virgola.

## Struttura CSV dei prodotti

Un’esportazione completa del database dei prodotti contiene informazioni su ciascun prodotto presente nel catalogo e sulle relazioni tra di essi. Ogni record dispone di una selezione fissa di colonne che corrispondono agli attributi nel catalogo, anche se l&#39;ordine degli attributi viene ignorato durante il processo di importazione.

La prima riga della tabella contiene i nomi di ogni attributo, utilizzati come intestazioni di colonna. Le righe rimanenti descrivono i singoli record di prodotto. Qualsiasi riga che inizia con un valore nella colonna SKU è l&#39;inizio di un nuovo record di prodotto. Un singolo prodotto può includere diverse righe che contengono informazioni su più immagini o opzioni di prodotto. La riga successiva con un valore nella colonna SKU inizia un nuovo prodotto.

La colonna categoria contiene un percorso per ogni categoria a cui è assegnato il prodotto. Il percorso include la categoria principale, seguita da una barra (`/`) tra ciascun livello. Per impostazione predefinita, la virgola `,` Il carattere viene utilizzato per separare percorsi di categorie diversi. (è possibile specificare un separatore diverso con _[!UICONTROL Multiple value separator]_). Ad esempio:

`Default Category/Gear,Default Category/Gear/Bags`

Per importare i dati, è necessario includere solo lo SKU ed eventuali colonne con modifiche. Eventuali colonne vuote vengono ignorate durante il processo di importazione. Impossibile aggiungere attributi durante il processo di importazione. È possibile includere solo gli attributi esistenti.

Per una descrizione dettagliata di ciascun attributo di prodotto, vedi [Struttura dei file CSV dei prodotti](data-attributes-product.md).

| Nome colonna | Descrizione |
| ----------- | ----------- |
| `_<name>` | Le intestazioni di colonna che iniziano con un carattere di sottolineatura contengono proprietà di entità servizio o dati complessi. Le colonne del servizio non sono attributi del prodotto. |
| `<attribute_name>` | Le intestazioni di colonna con un codice di attributo o un nome di campo identificano la colonna di dati. Una colonna può rappresentare un attributo di sistema o un attributo creato dall&#39;amministratore dell&#39;archivio. |

{style="table-layout:auto"}

## Struttura CSV del cliente

Il file CSV dei clienti contiene le informazioni sui clienti provenienti dal database e presenta la seguente struttura:

La prima riga della tabella contiene i nomi delle colonne di attributi, che corrispondono ai codici di attributo. Esistono due tipi di nomi di colonna, come illustrato nella tabella seguente. Altre righe contengono valori di attributo, dati di servizio e dati complessi. Ogni riga con valori non vuoti nel `email` e `_website` colonne avvia la descrizione del cliente successivo. Ogni riga può rappresentare i dati del cliente con o senza i dati dell’indirizzo oppure solo i dati dell’indirizzo. Se una riga contiene solo i dati dell’indirizzo, i valori nelle colonne, relativi al profilo cliente, vengono ignorati e potrebbero essere vuoti.

Per aggiungere o sostituire più indirizzi per un cliente, aggiungere una riga per ogni nuovo indirizzo con dati cliente vuoti e i dati dell&#39;indirizzo nuovi o aggiornati sotto la riga dati cliente.

Per una descrizione dettagliata di ciascun attributo del cliente, vedi [Struttura dei file CSV dei clienti](data-attributes-customer.md).

| Nome colonna | Descrizione |
| ----------- | ----------- |
| `_<name>` | Le intestazioni di colonna che iniziano con un carattere di sottolineatura contengono proprietà di entità servizio o dati complessi. Le colonne del servizio non sono attributi del cliente. |
| `<attribute name>` | Nomi delle colonne con i valori degli attributi creati dal sistema e degli attributi creati dall&#39;amministratore del punto vendita. |

{style="table-layout:auto"}
