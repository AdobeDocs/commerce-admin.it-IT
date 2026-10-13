---
source-git-commit: bb5da9eea16601303b62ccc06327c6a832062c49
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%
---
# Problemi risolti di Adobe Commerce B2B (v1.5.4-alpha1)

## B2B v1.5.4-alfa1

*13 ottobre 2026*

Sono stati risolti 23 problemi nel codice Adobe Commerce B2B 1.5.4-alpha1. Di seguito è descritto un sottoinsieme dei problemi risolti inclusi in questa versione.

### Interfaccia utente amministratore

#### [B2B] Quantità di prodotti del bundle non mantenute dopo l&#39;aggiornamento dei prezzi nei preventivi di backend

È stato risolto un problema che causava il ripristino del valore precedente della quantità di un articolo bundle in un preventivo negoziabile amministratore dopo la modifica della quantità nella griglia a seguito di una modifica della configurazione tramite la finestra di dialogo Configura.

_ACP2E-5005_

### B2B

#### La pagina Dettagli offerta [B2B] (vetrina e amministratore) perde le informazioni sull&#39;articolo/prodotto quando il prodotto correlato viene eliminato dal catalogo

È stato risolto il problema relativo alla scomparsa dei prodotti non vendibili dai preventivi negoziabili finalizzati

_ACP2E-4680_

#### Quantità prodotto del bundle non aggiornata correttamente dopo l’invio di un preventivo dal back-end

È stato risolto il problema che impediva l&#39;aggiornamento delle quantità delle opzioni di prodotto del bundle durante la riconfigurazione di un preventivo negoziabile dal pannello di amministrazione. In precedenza, le modifiche apportate alle quantità di opzioni bundle tramite il pulsante Configura venivano automaticamente eliminate.

_ACP2E-4801_

#### [La griglia delle società di amministrazione di CLOUD] [B2B] causa un elevato CPU MySQL: query correlata company_type / COUNT

È stato risolto il problema che causava un elevato utilizzo di MySQL CPU da parte della griglia delle società amministratore (clienti → società) e lunghe sessioni di database. In precedenza, per determinare il tipo di società (padre/figlio/società) per ogni riga era necessaria una sottoquery correlata rispetto alla tabella company_relation che veniva attivata una volta per riga aziendale, rendendo le query di inserimento e di conteggio totale O(N²) su scala; la correzione sostituisce questa con un singolo JOIN preaggregato che viene eseguito una volta indipendentemente dalle dimensioni del set di dati.

_ACP2E-4846_

#### Pagamento in conto (B2B) - Il pulsante Modifica ordine non è presente per gli ordini in sospeso, ma è visibile per COD

Il pulsante Modifica ordine è ora disponibile per gli ordini con pagamento in acconto. In precedenza non era possibile modificare un ordine effettuato con Pagamento in acconto mentre l&#39;ordine era in sospeso

_ACP2E-4877_

#### Timeout del PHP per risparmiare l&#39;azienda B2B con un super-utente multi-azienda

Il salvataggio di un’azienda B2B o il caricamento della pagina del super-utente dell’azienda nell’amministratore non supera più il tempo di esecuzione massimo del PHP quando il super-utente dell’azienda viene assegnato a un numero molto elevato di aziende.

_ACP2E-4967_

#### [ON-PREM] offerte negoziabili non aggiornate come previsto

È stato risolto il problema che impediva l&#39;aggiornamento dei preventivi negoziabili quando un prodotto presente in un preventivo negoziabile attivo veniva eliminato.

_ACP2E-5001_

#### Assegni aggiuntivi volatili &quot;Pagamento in conto&quot;

È stato risolto il problema che consentiva ai singoli clienti (B2C) di scegliere il metodo di pagamento Payment on Account (Pagamento in acconto), un metodo di pagamento destinato esclusivamente ai membri dell’azienda B2B durante il pagamento. In precedenza, a tali clienti veniva erroneamente consentito di procedere con il pagamento in acconto invece di ricevere un errore di tipo &quot;metodo di pagamento non disponibile&quot;.

_ACP2E-5013_

#### L&#39;azione di salvataggio della procedura guidata Catalogo condiviso cancella la struttura dei prezzi di un catalogo condiviso

È stato risolto un problema che si verificava quando l&#39;azione di salvataggio della procedura guidata Catalogo condiviso cancellava la struttura dei prezzi di un salvataggio di catalogo condiviso

_ACP2E-5015_

#### GraphQL customer.role restituisce &quot;Internal server error&quot; per i clienti B2C senza azienda

È stato risolto il problema per cui l&#39;esecuzione di una query sul cliente { role {...} } tramite GraphQL restituiva un &quot;Errore interno del server&quot; per i clienti B2C non assegnati ad alcuna società. In precedenza, questa query attivava un errore di tipo PHP perché un ID società nullo veniva passato a un metodo con un hint di tipo integer rigoroso.

_ACP2E-5017_

#### [B2B] Lo sconto dell&#39;articolo prodotto del bundle non viene applicato quando le quantità delle opzioni vengono aggiornate nei preventivi back-end

È stato risolto il problema che impediva di applicare uno sconto a livello di articolo a un prodotto Dynamic Price Bundle nell&#39;amministratore del preventivo back-end nel subtotale o nel subtotale (escl. imposte) quando le quantità di opzioni del bundle sono state aggiornate tramite la finestra di dialogo Configura. In precedenza, lo sconto veniva visualizzato nella colonna Sconto ma non riduceva il subtotale citato.

_ACP2E-5034_

#### La sezione Richiesta di acquisto viene ricaricata in ogni navigazione della pagina

È stato risolto il problema che causava l&#39;attivazione da parte della sezione della richiesta di acquisto di un ricaricamento di AJAX non necessario su ogni navigazione della pagina di prodotti e categorie. In precedenza, la sezione veniva ricaricata a ogni caricamento di pagina per qualsiasi cliente con dati dell’elenco di richieste di acquisto non vuoti, anche quando non erano state apportate modifiche.

_ACP2E-5037_

#### [B2B] Errore quando nell&#39;indirizzo della società mancano i dati dell&#39;area geografica

È stato risolto un problema che causava la visualizzazione di un errore nelle pagine Profilo società e Modifica cliente amministratore se a un indirizzo della società era stata aggiunta un’area nel paese in seguito al salvataggio dell’indirizzo senza un’area geografica. Ora, invece di causare un errore, l’indirizzo torna correttamente al testo dell’area memorizzata.

_ACP2E-5092_

#### L’aggiornamento aziendale per l’amministratore con impostazioni locali non inglesi reimposta il limite di credito

È stato risolto un problema a causa del quale la modifica dei dettagli di una società B2B poteva reimpostare involontariamente il Limite di credito configurato su 0 quando le impostazioni locali dell’amministratore differivano da quelle predefinite. Il limite di credito ora viene mantenuto correttamente a meno che non venga esplicitamente modificato.

_ACP2E-5127_

#### L&#39;amministratore con restrizioni del sito Web di [CLOUD] non può eliminare i clienti quando il relativo user_id si scontra con un entity_id cliente inaccessibile

In precedenza, quando un amministratore con restrizioni del sito web tentava di eliminare un cliente, il plug-in di controllo delle autorizzazioni del sistema confrontava l’ID utente dell’amministratore con
ID entità cliente per applicare restrizioni della gerarchia aziendale, senza verificare che l’utente che agisce sia effettivamente un cliente; se l’ID utente dell’amministratore è stato assegnato
per coincidere con l’ID entità di un cliente non correlato su un sito web a cui l’amministratore non poteva accedere, il plug-in ha tentato di caricare quel record cliente inaccessibile
e l’eliminazione non è riuscita con un errore &quot;sono necessarie più autorizzazioni&quot;, anche se l’amministratore disponeva di diritti validi per il cliente da eliminare. Questo problema è stato risolto
aggiungendo una condizione in modo che il confronto dell’ID cliente venga eseguito solo quando l’utente che agisce è effettivamente un cliente, il che significa che le eliminazioni avviate dall’amministratore ignorano completamente tale controllo; gli amministratori con restrizioni possono eliminare nuovamente i clienti all’interno dei siti web assegnati senza essere bloccati da record di clienti non correlati e inaccessibili

_ACP2E-5146_

#### L’ordine B2B mostra un nome società errato negli ordini cliente amministratori

È stato risolto un problema che causava la visualizzazione di un nome società errato per gli ordini di acquisto B2B in Ordini di vendita amministratori quando un utente veniva assegnato a più società.
Il nome della società viene ora visualizzato correttamente in base alla società associata all’ordine.

_B2B-4656_

### B2B, carrello e pagamento

#### [ON PREM] [B2B] Lo strumento di caricamento Quick Order si blocca quando si tenta di caricare un file binario con estensione .CSV

È stato risolto il problema per cui lo strumento di caricamento dei file Quick Order accettava qualsiasi file rinominato con estensione .csv, inclusi i file binari. In precedenza, non veniva eseguita alcuna convalida del tipo MIME o del contenuto, pertanto i file non CSV (ad esempio i file eseguibili) potevano essere caricati ed elaborati come se fossero elenchi SKU/QTY validi.

_ACP2E-5212_

### B2B, GraphQL

#### Inesattezza conteggio totale GQL elenco richieste di acquisto

È stato risolto il problema che si verificava quando la query di GraphQL richieste di acquisto_elenchi restituiva un valore total_count errato che rifletteva solo il numero di articoli nella pagina corrente invece del numero totale di entità dell&#39;elenco richieste di acquisto che corrispondevano ai criteri della query.

_ACP2E-4799_

### B2B, Ordine

#### Guida sulla pulizia delle tabelle di preventivo di 59M+ (sales_clean_quotes non è in grado di eseguire)

È stato risolto il problema relativo al timeout del processo cron `sales_clean_quotes` nelle istanze con tabelle di virgolette grandi. In precedenza, la query di pulizia selezionava inutilmente tutte le colonne dalla tabella `negotiable_quote`, facendo in modo che MySQL eseguisse un file completo su milioni di righe; ogni preventivo veniva eliminato singolarmente tramite il livello del modello PHP, aggiungendo il costo delle prestazioni.

_ACP2E-4891 - [Contributo codice GitHub](https://github.com/magento/magento2/commit/b63925d9)_

### B2B, Prestazioni

#### [CLOUD] Follow-up di ACSD-70033: Deadlock sulla tabella magento_catalogpermissions_index_product. continuazione

In precedenza, la reindicizzazione delle autorizzazioni del catalogo con Catalogo condiviso abilitato poteva causare un errore di deadlock, causando un errore di reindicizzazione. Ora la reindicizzazione viene completata anche quando più processi di indicizzazione vengono eseguiti contemporaneamente.

_ACP2E-4844_

### Contenuto

#### Le pagine CMS create per siti web diversi presentano pagine errate nel front-end

In precedenza, nelle configurazioni multisito in cui la chiave della cache della pagina di destinazione Restrizione sito web non era inclusa nell’ambito per sito web, causando la visualizzazione della pagina CMS errata nella vetrina secondaria del sito web. La chiave cache in WebsiteRestriction/Controller/Index/Stub.php ora include correttamente l&#39;ID sito Web corrente risolto tramite lo Store Manager.

_ACP2E-4593_

### Framework

#### [B2B] Gli ordini fornitore non vengono convertiti automaticamente in ordini cliente con ActiveMQ

È stato risolto un problema a causa del quale i consumatori avviati da cron non elaboravano i messaggi quando ActiveMQ veniva utilizzato con il protocollo STOMP. Di conseguenza, gli ordini di acquisto approvati automaticamente non sono stati convertiti in ordini di vendita. L’elaborazione dei messaggi per le code STOMP è ora più affidabile e coerente con le implementazioni delle code DB e AMQP.

_ACP2E-4349 - [Contributo codice GitHub](https://github.com/magento/magento2/commit/08b91f1a) - [Contributo codice GitHub](https://github.com/magento/inventory/commit/239464da)_

### Installazione e amministrazione

#### [Cloud] Correzione dei codici di suddivisione ISO esistenti obsoleti

Sono stati aggiornati i codici regionali per 13 paesi, in conformità allo standard ISO 3166-2. In precedenza, alcuni codici di area non corrispondevano allo standard, il che poteva causare problemi con le integrazioni di terze parti e la conformità internazionale. Sono state aggiunte nuove regioni per Belgio, Colombia, Spagna, Francia, Italia e Lettonia. Codici di regione aggiornati per Austria, Colombia, Costa Rica, Germania, Estonia, Spagna, Finlandia, Francia, India, Islanda e Lettonia.

_ACP2E-4495 - [Contributo codice GitHub](https://github.com/magento/magento2/commit/9b6a8bd9)_
