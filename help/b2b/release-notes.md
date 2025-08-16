---
title: Note sulla versione di [!DNL Adobe Commerce B2B]
description: Consulta le note sulla versione per informazioni sulle modifiche apportate in  [!DNL Adobe Commerce B2B]  versioni.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 298dae1e7ff3ec2af42d70a255075877458eeb4f
workflow-type: tm+mt
source-wordcount: '9030'
ht-degree: 0%

---

# Note sulla versione di [!DNL Adobe Commerce B2B]

Queste note sulla versione dell’estensione B2B acquisiscono aggiunte e correzioni che Adobe ha aggiunto durante un ciclo di rilascio, tra cui:

![Nuove](../assets/new.svg) nuove funzionalità
![Problema risolto](../assets/fix.svg) correzioni e miglioramenti
![Problema noto](../assets/bug.svg) Problemi noti

>[!NOTE]
>
>Consulta [Disponibilità del prodotto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html?lang=it) per informazioni sulle versioni dell&#39;estensione B2B Commerce supportate per le versioni disponibili di Adobe Commerce.

## B2B v1.5.3-alfa2

*12 agosto 2025*

Compatibile con Adobe Commerce versione 2.4.9-alpha2

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-71](https://helpx.adobe.com/it/security/products/magento/apsb25-71.html).

## B2B v1.5.2-p2

*12 agosto 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.8-p2, 2.4.7-p7 e 2.4.6-p12.
Compatibile con Adobe Commerce versioni da 2.4.7 a 2.4.7-p6, da 2.4.6 a 2.4.6-p11.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-71](https://helpx.adobe.com/it/security/products/magento/apsb25-71.html).

## B2B v1.5.2-p1

*10 giugno 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.8-p1, 2.4.7-p6 e 2.4.6-p11.
Compatibile con Adobe Commerce versioni da 2.4.7 a 2.4.7-p5, da 2.4.6 a 2.4.6-p10

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-50](https://helpx.adobe.com/it/security/products/magento/apsb25-50.html).

## B2B 1.5.2

*8 aprile 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.8, 2.4.7-p5 e 2.4.6-p10.
Compatibile con Adobe Commerce versioni da 2.4.7 a 2.4.7-p4, da 2.4.6 a 2.4.6-p9

La versione 1.5.2 di B2B include miglioramenti della qualità e correzioni di bug.

### Gestione società

![Nuovi](../assets/new.svg)<!-- B2B-4123 -->Gli amministratori ora possono gestire più società da un singolo account utilizzando il commutatore società vetrina. I vantaggi principali includono:

- **Gestione semplificata per più società**: gli amministratori possono ora controllare più società da un unico account utente, eliminando la necessità di creare e gestire accessi separati per ogni società.
- **Cambio di azienda efficiente**: un&#39;interfaccia intuitiva consente agli amministratori di passare rapidamente da un&#39;azienda all&#39;altra e di apportare aggiornamenti, migliorando la produttività durante la gestione di più entità.
- **Operazioni semplificate**: i manager regionali e i leader aziendali possono gestire centralmente tutte le loro aziende, consentendo processi decisionali più rapidi e operazioni aziendali più semplici.

Questo miglioramento si basa sulla funzionalità di iscrizione multiaziendale di B2B 1.5.0, che consentiva agli utenti di appartenere a più aziende ma non supportava l’accesso come amministratore tra le aziende. Il commutatore aziendale elimina la necessità di account amministratore separati, mantenendo al contempo controlli di accesso e visualizzazioni specifiche per l’azienda.

### Azienda

![È stato risolto un problema](../assets/fix.svg)<!-- B2B-4480 --> che causava la visualizzazione di un messaggio di errore `No such entity with cartId = ?` da parte dei clienti guest durante l&#39;accesso come utente aziendale con i prodotti nel carrello.

### Offerta negoziabile

![Problema risolto](../assets/fix.svg) La versione di B2B v1.5.2 include le seguenti correzioni per i preventivi negoziabili:

- &#x200B;<!-- B2B-3252 -->Il campo [!UICONTROL Line Item Discount Amount] ora convalida l&#39;input per impedire l&#39;immissione di valori di sconto negativi.
- &#x200B;<!-- B2B-3224 -->È stato risolto un problema di esperienza utente a causa del quale le note sugli elementi di riga lunghi venivano troncate e risultavano di difficile lettura per i clienti B2B.
- &#x200B;<!-- B2B-2865 -->I clienti B2B ora possono specificare le quantità di prodotto utilizzando valori decimali (ad esempio 1,5 o 2,75) durante la creazione dei preventivi.

### Modello di offerta

![Nuovo](../assets/new.svg)<!-- B2B-4104 --> Nuova possibilità per gli acquirenti e i venditori B2B di allegare ai modelli di preventivo i collegamenti ai documenti esterni. Questa funzione consente il collegamento diretto da virgolette a documenti ospitati in servizi come DocuSign e Adobe Sign, a complemento della funzionalità di file allegato esistente. I vantaggi principali includono:

- Collaborazione semplificata grazie all&#39;accesso diretto agli accordi e ai contratti critici
- Maggiore trasparenza con accesso immediato alla documentazione più recente
- Negoziazioni più rapide delle offerte, eliminando la necessità di scaricare e caricare i file
- Gestione flessibile dei documenti tramite servizi di hosting esterni

## B2B 1.5.1

*11 febbraio 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p4+ e 2.4.6-p9+.
Compatibile con Adobe Commerce versioni da 2.4.8-beta1 a 2.4.8-beta2, da 2.4.7 a 2.4.7-p3, da 2.4.6 a 2.4.6-p8

La versione 1.5.1 di B2B include miglioramenti della qualità e correzioni di bug.

### Azienda

![Problema risolto](../assets/fix.svg)<!-- B2B-4422 --> Se un cliente tenta di cambiare società nella pagina Dettagli preventivo, il sistema reindirizza il cliente a una pagina *Accesso negato* per assicurarsi che un preventivo creato per una società non possa essere utilizzato per effettuare un ordine con i prezzi di un&#39;altra società. In precedenza, un utente poteva creare un preventivo con il prezzo di una società e quindi passare a un’altra società per effettuare un ordine con prezzi diversi.

### Sconti riga

![Problema risolto](../assets/fix.svg)<!-- B2B-2938 --> È stata migliorata l&#39;efficienza del sistema risolvendo il degrado delle prestazioni osservato nello scenario di ricalcolo delle offerte. In precedenza, a ogni voce del carrello venivano aggiunte due nuove entità che causavano un notevole aumento delle richieste del database, con conseguente rallentamento delle prestazioni.

### Offerta negoziabile

![Problema risolto](../assets/fix.svg)<!-- B2B-3820 --> Il sistema ora mantiene la posizione degli elementi dell&#39;interfaccia utente quando la convalida JavaScript viene applicata ai campi *[!UICONTROL min/max qty]* nella pagina del modello di offerta Luma Storefront. In precedenza, l’applicazione della convalida JavaScript a questi campi causava lo spostamento di altri elementi dell’interfaccia utente della pagina.

### Carrello

![È stato risolto il problema](../assets/fix.svg)<!-- B2B-4222 -->. È stato introdotto un nuovo sistema di gestione del carrello progettato per semplificare l&#39;esperienza di acquisto per gli utenti che gestiscono più account aziendali. Il nuovo sistema associa i carrelli alle singole aziende, anziché all’account del cliente, per semplificare l’esperienza di acquisto e migliorare il flusso di lavoro supportando le seguenti funzionalità.

- **Carrelli specifici della società:**—I carrelli acquisti sono ora collegati alle singole società per supportare le opzioni di prezzo e prodotto specifiche della società.
- **Commutazione senza problemi**: gli utenti possono passare facilmente da un account aziendale all&#39;altro senza influire sul contenuto del carrello di ogni azienda.
- **Integrità contestuale**: tutti i dettagli del carrello rimangono nel contesto della rispettiva azienda, fornendo un&#39;esperienza di acquisto coerente e affidabile.

## B2B 1.5.0

*30 ottobre 2024*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p3+ e 2.4.6-p8+.
Compatibile con Adobe Commerce versioni 2.4.8-beta1, 2.4.7-2.4.7-p2, 2.4.6-2.4.6-p7.

Adobe Commerce B2B versione 1.5.0 è compatibile anche con PHP 8.3 e supporta [GraphQL Application Server](https://experienceleague.adobe.com/it/docs/commerce-operations/performance-best-practices/concepts/application-server).

La versione 1.5.0 di B2B include nuove funzioni, miglioramenti della qualità e correzioni di bug.

>[!NOTE]
>
> Scopri le modifiche non compatibili con le versioni precedenti (BIC) introdotte nella versione 1.5.0 di B2B esaminando gli elementi di rilievo e le informazioni di riferimento nell’argomento [Modifiche non compatibili con le versioni precedenti](backward-incompatible-changes.md).

### Gestione società

![Nuovo](../assets/new.svg) **Gestione società**<!--B2B-2901-->: gli esercenti possono ora visualizzare e gestire le società Adobe Commerce come organizzazioni gerarchiche assegnando le società alle società padre designate. Dopo che una società è stata assegnata a una società madre, l&#39;amministratore della società madre può gestire l&#39;account della società. Solo gli utenti amministratori autorizzati possono aggiungere e gestire le assegnazioni aziendali. Per ulteriori dettagli, vedere [Gestione gerarchia società](manage-company-hierarchy.md).

- Aggiungi e gestisci le assegnazioni della società dalla nuova sezione *[!UICONTROL Company Hierarchy]* nella pagina *[!UICONTROL Company Account]* dell&#39;amministratore.

- Ordina e filtra le società in base alla nuova impostazione *[!UICONTROL Company Type]*. Nella griglia delle società, la colonna *[!UICONTROL Company Type]* indica se una società è una singola società o parte della gerarchia organizzativa (padre o figlio).

![Nuovo](../assets/new.svg) **Gestisci la configurazione della società alla scala**<!--B2B-2849-->—Modifica rapidamente le impostazioni di configurazione della società per le società selezionate utilizzando l&#39;azione collettiva *[!UICONTROL Change company setting]* ora disponibile per la gestione delle società dalla griglia *[!UICONTROL Companies]* o *[!UICONTROL Company Hierarchy]*. Ad esempio, se crei un nuovo catalogo condiviso per un gruppo di aziende, puoi modificare la configurazione del catalogo condiviso in un’unica azione, anziché modificare singolarmente ogni azienda.

![I nuovi](../assets/new.svg) sviluppatori API possono utilizzare il nuovo endpoint REST API per le relazioni con le società `/V1/company/{parentId}/relations` per creare, visualizzare e rimuovere le assegnazioni aziendali. Consulta [Gestire gli oggetti aziendali](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) nella *Guida per gli sviluppatori API Web*.

### Account società

![Nuovo](../assets/new.svg)<!--B2B-2828--> **Assegnazione di più società**—Semplificare l&#39;accesso degli utenti aziendali assegnando un utente a più società. Ad esempio, se un buyer effettua un ordine da più sedi della società, creare un singolo account e assegnare a tale account tutte le società con cui lavora il buyer. Quindi, l&#39;acquirente può effettuare l&#39;accesso una sola volta e passare da un account aziendale all&#39;altro scegliendo la società dalla vetrina.

>[!NOTE]
>
>Un utente di un’azienda può essere assegnato a più aziende, ma può essere l’amministratore dell’azienda per una sola azienda.

![Nuovo](../assets/new.svg) <!--B2B-2747--> **Selettore ambito società** - Consente agli utenti società assegnati a più società di cambiare società nella vetrina. Quando l’ambito viene cambiato, i dati vengono aggiornati per mostrare le informazioni in base al nuovo contesto aziendale. Ad esempio, se la nuova società utilizza un catalogo condiviso diverso, l’utente della società visualizza prodotti, prezzi e altre informazioni in base al nuovo catalogo condiviso. Anche il contenuto relativo a ordini, preventivi e modelli di preventivo viene aggiornato in base al contesto della società selezionata.

>[!NOTE]
>Il contenuto del carrello riflette gli articoli selezionati dal cliente corrente. Se il cliente dispone di un carrello attivo e seleziona un’altra società, gli viene richiesto di aggiornare il carrello per riflettere l’assortimento del prodotto, i prezzi e gli sconti promozionali in base al nuovo contesto aziendale. I prodotti che non sono disponibili nel catalogo associato alla nuova azienda vengono rimossi dal carrello. Se il prezzo o la disponibilità del prodotto sono diversi, il carrello viene aggiornato in modo da riflettere i dati disponibili nel contesto della società selezionata.<!--B2B-4222-->

![Problema risolto](../assets/fix.svg)<!--ACP2E-1933--> Gli amministratori della società ora possono aggiungere utenti della società dalla vetrina. In precedenza, Commerce registrava un errore quando un utente amministratore tentava di aggiungere un nuovo utente: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Preventivi e modelli di preventivo

I miglioramenti apportati alle funzionalità di preventivo consentono a buyer e venditori di gestire i preventivi e la negoziazione dei preventivi in modo più efficace.

![Nuovi](../assets/new.svg) **Modelli di preventivo**—<!--B2B-3367-->Acquirenti e venditori possono ora semplificare il processo di offerta creando modelli di preventivo riutilizzabili e personalizzabili. Utilizzando i modelli di preventivo, il processo di negoziazione dei preventivi può essere completato una sola volta e gli acquirenti possono generare preventivi collegati preapprovati per ordini ricorrenti anziché passare attraverso il processo di negoziazione dei preventivi per ciascun ordine. I modelli di preventivo estendono la funzionalità di preventivo esistente aggiungendo le seguenti funzionalità avanzate:

- **Le soglie di ordine** consentono ai venditori di impostare impegni di ordine minimi e massimi, garantendo che l&#39;acquirente rispetti i volumi di acquisto concordati.
- **L&#39;impostazione di quantità minime e massime per gli ordini degli articoli** offre al buyer la flessibilità necessaria per adeguare le quantità degli ordini nel preventivo collegato senza richiedere un nuovo modello o ulteriori negoziazioni.
- **Tieni traccia del numero di preventivi collegati generati e degli ordini completati correttamente** per ottenere informazioni sull&#39;esecuzione degli accordi negoziati.
- **I preventivi collegati** sono preventivi preapprovati che il buyer genera da un modello di preventivo attivo per inviare ordini ricorrenti in base alle condizioni negoziate nel modello di preventivo.

![Nuovo](../assets/new.svg) **Miglioramenti alle funzionalità delle virgolette esistenti**

- **Le regole dell&#39;elenco di controllo di accesso (ACL) di Commerce aggiornate** consentono ai responsabili e ai supervisori B2B di gestire preventivi e modelli di preventivo di utenti subordinati. Regole separate supportano la configurazione granulare per l&#39;accesso di visualizzazione, modifica ed eliminazione.

- **Salva preventivo come bozza**<!--B2B-2566--> - Durante la creazione di una [richiesta di preventivo](quote-request.md) dal carrello, gli acquirenti possono salvare il preventivo come bozza in modo da poterlo esaminare e aggiornare prima di avviare il processo di negoziazione del preventivo con il venditore. L&#39;offerta provvisoria non ha una data di scadenza. Gli acquirenti possono esaminare e aggiornare i preventivi provvisori dalla sezione [!UICONTROL My Quotes] del dashboard account.

- **Rinomina preventivo**<!--B2B-2596--> - Gli acquirenti possono modificare il nome di un preventivo dalla pagina [Dettagli preventivo](account-dashboard-my-quotes.md#quote-actions) selezionando l&#39;opzione **[!UICONTROL Rename]**. Questa opzione è disponibile per gli acquirenti autorizzati che modificano il preventivo. Gli eventi di modifica del nome vengono registrati nel registro Cronologia preventivo.

- **Offerta duplicata**<!--B2B-2701--> - Acquirenti e venditori possono creare un nuovo preventivo copiando un preventivo esistente. Viene creata una copia dalla visualizzazione dei dettagli del preventivo selezionando **[!UICONTROL Create Copy]** nella [visualizzazione dei dettagli del preventivo](quote-price-negotiation.md#button-bar) nell&#39;Admin o nello [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Spostare l&#39;articolo del preventivo nell&#39;elenco delle richieste di acquisto**<!--B2B-2755-->. Gli acquirenti dispongono ora della flessibilità necessaria per rimuovere i prodotti da un preventivo e salvarli in un elenco delle richieste di acquisto se decidono di non includerli nel processo di negoziazione del preventivo.

- **Rimuovere più prodotti da un preventivo**<!--B2B-2881-->. Nei preventivi con un numero elevato di prodotti, gli acquirenti possono ora rimuovere più prodotti dal preventivo selezionandoli e utilizzando l&#39;opzione *[!UICONTROL Remove]* dal controllo *[!UICONTROL Actions]* nella pagina Dettagli preventivo. Nelle versioni precedenti, un acquirente doveva eliminare i prodotti uno alla volta.

- **Blocco sconto articolo linea**<!--B2B-2597-->. Durante la negoziazione del preventivo, i venditori possono utilizzare il blocco sconto articolo linea per una maggiore flessibilità quando applicano sconti durante il processo di negoziazione del preventivo. Ad esempio, un venditore può applicare uno sconto speciale su un oggetto e bloccare l&#39;oggetto per evitare ulteriori sconti. Quando un articolo è bloccato, non è possibile aggiornare il prezzo dell&#39;articolo quando viene applicato uno sconto a livello di preventivo. Vedi [Avvia offerta per un acquirente](sales-rep-initiates-quote.md).

![È stato risolto il problema](../assets/fix.svg) **Sono state corrette le funzionalità delle virgolette esistenti**

- Ai commercianti che fanno clic sul pulsante *[!UICONTROL Print]* nella visualizzazione Dettagli preventivo nell&#39;amministratore viene ora richiesto di salvare il preventivo come PDF. In precedenza, i commercianti venivano reindirizzati a una pagina contenente i dettagli delle offerte. <!--ACP2E-1984-->

- In precedenza, quando si inviava un preventivo cliente con `0` percentuale e si modificava la quantità, l&#39;amministratore generava un&#39;eccezione ma salvava la quantità. In seguito a questa correzione, per `0 percentage` verrà generata l&#39;eccezione appropriata con un messaggio. <!--ACP2E-1742-->

- Durante la negoziazione del preventivo, un venditore può ora specificare uno sconto `0%` nel campo Sconto preventivo negoziato e inviare il preventivo all&#39;acquirente. In precedenza, se il venditore inseriva uno sconto dello 0% e inviava nuovamente il preventivo all&#39;acquirente, l&#39;amministratore restituiva un messaggio di errore `Exception occurred during quote sending`. <!--ACP2E-1742-->

- La convalida ReCaptcha ora funziona correttamente durante il processo di pagamento di un preventivo B2B quando ReCaptcha V3 è configurato per il pagamento in vetrina. In precedenza, la convalida non era riuscita con un messaggio di errore `recaptcha validation failed, please try again`.  <!--ACP2E-2097-->

### Ordini di acquisto

![Problema risolto](../assets/fix.svg) <!--ACP2E-1825-->Un utente associato alla società non può più inserire ordini di acquisto dopo il blocco della società. In precedenza, un utente associato alla società poteva effettuare ordini di acquisto quando la società era bloccata.

## B2B v1.4.2-p7

*12 agosto 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p7+ e 2.4.6-p12+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-71](https://helpx.adobe.com/it/security/products/magento/apsb25-71.html).

{{b2b-compatibility}}

## B2B v1.4.2-p6

*10 giugno 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p6+ e 2.4.6-p11+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-50](https://helpx.adobe.com/it/security/products/magento/apsb25-50.html).

{{b2b-compatibility}}

## B2B v1.4.2-p5

*8 aprile 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p5+ e 2.4.6-p10+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.7-p5+ e 2.4.6-p10+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-26](https://helpx.adobe.com/it/security/products/magento/apsb25-26.html).

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11 febbraio 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p4+ e 2.4.6-p9+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.7-p4+ e 2.4.6-p9+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-08](https://helpx.adobe.com/it/security/products/magento/apsb25-08.html).

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8 ottobre 2024*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p3+ e 2.4.6-p8+.

![Nuovo](../assets/new.svg) È stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.7-p3+ e 2.4.6-p8+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB24-73](https://helpx.adobe.com/it/security/products/magento/apsb24-73.html).

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p2+ e 2.4.6-p7+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.7-p2+ e 2.4.6-p7+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate nel Bollettino sulla sicurezza xxxx.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9 agosto 2024*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.7-p1+ e 2.4.6-p6+.

![Nuovo](../assets/new.svg) È stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.7-p1+ e 2.4.6-p6+.

{{b2b-compatibility}}

## B2B v1.4.2

*10 ottobre 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce versione 2.4.7 e versione da 2.4.6 a 2.4.6-p5.

La versione 1.4.2 di B2B include miglioramenti della qualità e correzioni di bug.

![Problema risolto](../assets/fix.svg) <!--B2B-2897-->Se un venditore crea un preventivo dell&#39;acquirente che include uno SKU di prodotto non disponibile nel catalogo condiviso associato alla società dell&#39;acquirente, il sistema visualizza il messaggio di errore `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Il venditore non può salvare il preventivo finché non rimuove il prodotto non disponibile. In precedenza, il preventivo veniva salvato con lo SKU non disponibile incluso e il preventivo non veniva caricato nella vetrina.

>[!IMPORTANT]
>
>Adobe Commerce B2B versione 1.4.2+ è compatibile con PHP 8.2. Se aggiorni l’istanza di Commerce alla versione 2.4.7+, assicurati che l’istanza utilizzi PHP versione 8.2 per mantenere la compatibilità con Adobe Commerce versione B2B. Inoltre, B2B 1.4.2+ non supporta attualmente [GraphQL Application Server](https://experienceleague.adobe.com/it/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7 agosto 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=it). Compatibile con Adobe Commerce 2.4.7-beta1.

La versione 1.4.1 di B2B include miglioramenti della qualità e correzioni di bug.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1825-->Un utente associato alla società non può più inserire ordini di acquisto dopo il blocco della società. In precedenza, un utente associato alla società poteva effettuare ordini di acquisto quando la società era bloccata.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1943-->Lo stato del prodotto in inevaso è ora visualizzato correttamente nella vetrina. In precedenza, i prodotti disponibili per la spedizione venivano erroneamente identificati come prodotti in inevaso.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1862-->Se il modulo di registrazione della società include un attributo del tipo di file del cliente, il file caricato durante il processo di registrazione viene ora incluso nelle informazioni sull&#39;account per l&#39;amministratore della società dopo la creazione della società. In precedenza, l’allegato era mancante.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1793-->Il selettore dei campioni per un prodotto configurabile ora viene visualizzato come previsto nella pagina di configurazione dell&#39;elemento dell&#39;elenco richieste di acquisto. In precedenza, il selettore campioni veniva visualizzato come campo a discesa nella pagina di configurazione dell’elemento dell’elenco richieste di acquisto.

![È stato risolto il problema](../assets/fix.svg) <!--ACP2E-1968-->Quando si utilizza la [query GraphQL società](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) per restituire i dettagli della società, i risultati vengono ora restituiti correttamente senza errori.

## B2B v1.4.0

*13 giugno 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=it). Compatibile con Adobe Commerce 2.4.7-beta1

Questa versione include nuove funzionalità e miglioramenti per i preventivi negoziabili B2B e diverse correzioni di bug.

![Nuovo](../assets/new.svg) Aggiunta compatibilità con Adobe Commerce 2.4.7-beta1.

![Nuovi](../assets/new.svg) **Offerte avviate dal venditore**—I venditori possono ora avviare un preventivo per un acquirente direttamente dalle griglie Preventivo e Cliente dell&#39;amministratore. Questa funzionalità semplifica il processo di offerta e riduce la complessità per i clienti. Se un cliente non ha avviato un ordine, un venditore può creare rapidamente un preventivo per conto del cliente e avviare il processo di negoziazione. In precedenza, i preventivi potevano essere creati solo dalla vetrina dall&#39;acquirente o da un venditore che aveva effettuato l&#39;accesso come cliente.

![Nuovo](../assets/new.svg) **Sconti e negoziazione per elemento riga**—<!--B2B-2440--> In un preventivo, acquirenti e venditori B2B possono ora negoziare a livello di elemento riga, applicando sconti e scambiando note fino al raggiungimento di un accordo. La creazione e gli aggiornamenti delle note sono inclusi nella cronologia dell’elemento riga e dell’offerta per tenere traccia della comunicazione. In precedenza, acquirenti e venditori potevano scambiarsi note e applicare sconti solo a livello di preventivo.

![Problema risolto](../assets/fix.svg) Adobe Commerce visualizza ora i dettagli corretti durante il pagamento quando è abilitata l&#39;opzione Ordini di acquisto e quando è stato selezionato un preventivo virtuale creato con l&#39;opzione di pagamento PayPal. In precedenza, i totali venivano visualizzati come zero in queste condizioni.

![È stato risolto il problema](../assets/fix.svg) <!--ACP2E-1504--> Gli errori di convalida non si verificano più quando si tenta di salvare una società con un limite di credito superiore a 999. In precedenza, per i limiti di credito aziendali superiori a 999, Adobe commerce inseriva un separatore con la virgola, causando un errore di convalida che impediva il salvataggio degli aggiornamenti.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1474--> L&#39;indirizzo di spedizione selezionato rimane invariato quando si effettua un ordine con un preventivo negoziabile. In precedenza, quando si effettuava un ordine, l&#39;indirizzo di spedizione selezionato veniva modificato nell&#39;indirizzo di spedizione predefinito.

![È stato risolto il problema](../assets/fix.svg) <!--ACP2E-1429--> Nelle impostazioni di configurazione dell&#39;archivio per le funzionalità B2B, il campo **[!UICONTROL Enable Shared Catalog direct products price assigning]** è ora disabilitato automaticamente. Nella vetrina, è nascosto quando l&#39;impostazione **[!UICONTROL Enable Company]** o **[!UICONTROL Enable Shared Catalog]** è impostata su **[!UICONTROL No]**.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1683--> Durante la creazione di un account aziendale dalla vetrina, Commerce ora convalida l&#39;indirizzo e-mail prima di elaborare la registrazione della società. Se l’indirizzo e-mail non è valido, l’operazione non riesce e non vengono elaborati aggiornamenti dell’account. In precedenza, veniva creato un account cliente anche se la richiesta di creare un account aziendale non riusciva a causa di un indirizzo e-mail non valido.

![È stato risolto il problema](../assets/fix.svg) <!--ACP2E-1664--> Gli SKU di prodotto che includono virgolette doppie nel catalogo condiviso e nella struttura dei prezzi non causano più errori nell&#39;amministratore.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1498--> È stata aggiornata la configurazione di Vernice per l&#39;applicazione Commerce per impedire agli utenti guest di visualizzare i dati di altri gruppi di clienti.

### Problema noto

Se si installa o si aggiorna B2B 1.4.0 in [Adobe Commerce versione 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=it), si verifica il seguente errore:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

È possibile risolvere il problema aggiungendo dipendenze manuali per il pacchetto di sicurezza B2B aggiungendo dipendenze manuali per il pacchetto di sicurezza B2B con un [tag di stabilità](https://getcomposer.org/doc/04-schema.md#package-links). Per istruzioni, vedere [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html?lang=it).

## B2B v1.3.5-p12

*12 agosto 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.6-p12+.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-71](https://helpx.adobe.com/it/security/products/magento/apsb25-71.html).

## B2B v1.3.5-p10

*8 aprile 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.6-p10+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.6-p10.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-26](https://helpx.adobe.com/it/security/products/magento/apsb25-26.html).

## B2B v1.3.5-p9

*11 febbraio 2025*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.6-p9+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza Adobe Commerce 2.4.6-p9.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-08](https://helpx.adobe.com/it/security/products/magento/apsb25-08.html).

## B2B v1.3.5-p8

*8 ottobre 2024*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.6-p8+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza di Adobe Commerce 2.4.6-p8.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB24-73](https://helpx.adobe.com/it/security/products/magento/apsb24-73.html).

## B2B v1.3.5-p7

*9 agosto 2024*

[!BADGE Supportate]{type=Informative tooltip="Supportato"} versioni delle patch di sicurezza Adobe Commerce 2.4.6-p7+.

![Nuovo](../assets/new.svg) è stata aggiunta la compatibilità con le versioni delle patch di sicurezza di Adobe Commerce 2.4.6-p7.

## B2B v1.3.5

*14 marzo 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 - 2.4.6 e versioni successive

![Nuovo](../assets/new.svg) è stata rilasciata la versione B2B 1.3.5-p2 per supportare la compatibilità con Adobe Commerce 2.4.6-p2.

![Nuovo](../assets/new.svg) È stata rilasciata la versione B2B 1.3.5-p1 per supportare la compatibilità con Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Dopo aver aggiornato Commerce dalla versione 2.4.6 alla [versione più recente](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=it#2.4.6), assicurati di eseguire l’aggiornamento alla versione della patch B2B 1.3.5 supportata. In alternativa, aggiorna l’estensione B2B dalla versione 1.3.5 alla versione 1.4.0 o successiva per ottenere le funzioni più recenti.

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.6.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce visualizza ora i dettagli corretti durante il pagamento quando l&#39;opzione Ordini di acquisto è abilitata e quando è stato selezionato un preventivo virtuale creato con l&#39;opzione di pagamento PayPal. In precedenza, i totali venivano visualizzati come zero in queste condizioni.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-609--> L&#39;elenco dei gruppi di clienti per l&#39;impostazione **Consenti esplorazione categoria** non contiene più gruppi di clienti correlati a cataloghi condivisi.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1244--> L&#39;attributo cliente Partita IVA ora funziona come previsto con gli account amministratore società sia in Admin che in storefront. Per creare un conto aziendale non sono più necessari attributi IVA/imposta personalizzati. In precedenza, quando un esercente creava un account aziendale con un attributo personalizzato Imposta/IVA, Adobe Commerce generava un errore di convalida sia nella vetrina che nell’Amministratore.

![È stato risolto il problema](../assets/fix.svg) <!--- ACP2E-1236--> La disabilitazione della funzione di catalogo condiviso in un ambito specifico ora funziona correttamente. In precedenza, Adobe Commerce impostava un ambito non valido quando un commerciante salvava la configurazione di un catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1203--> Gli utenti amministratori ora possono salvare i valori degli attributi personalizzati del cliente per gli utenti aziendali. In precedenza, non era possibile salvare gli attributi personalizzati del cliente per gli utenti aziendali.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1221--> I problemi di prestazioni vengono risolti con la convalida delle autorizzazioni aziendali fornite tramite GraphQL quando molte autorizzazioni aziendali sono già assegnate.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce non genera più un errore nella pagina del carrello quando si utilizza l&#39;ordine rapido per aggiungere un prodotto in una quantità che supera le scorte disponibili.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1090--> Sono state migliorate le prestazioni di `SELECT` operazioni sulle autorizzazioni aziendali.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-2456--> Le query per categorie ora restituiscono i prezzi dei prodotti in base alle impostazioni di configurazione dello store quando non sono impostate in modo esplicito le autorizzazioni per le categorie nella categoria in cui viene eseguita la query.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-6829--> Il pulsante **[!UICONTROL Place Order]** ora funziona come previsto quando si completa un acquisto con una richiesta di preventivo approvata. Sono stati risolti i problemi relativi al plug-in `negotiableQuoteCheckoutSessionPlugin` dell&#39;offerta negoziabile.

## B2B v1.3.4-p14

*12 agosto 2025*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-71](https://helpx.adobe.com/it/security/products/magento/apsb25-71.html).

## B2B v1.3.4-p13

*10 giugno 2025*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.5-p12.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-50](https://helpx.adobe.com/it/security/products/magento/apsb25-50.html).

## B2B v1.3.4-p12

*8 aprile 2025*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.5-p12.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-26](https://helpx.adobe.com/it/security/products/magento/apsb25-26.html).

## B2B v1.3.4-p11

*11 febbraio 2025*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.5-p11.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-08](https://helpx.adobe.com/it/security/products/magento/apsb25-08.html).

## B2B v1.3.4-p10

*9 ottobre 2024*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.5-p10.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB24-73](https://helpx.adobe.com/it/security/products/magento/apsb24-73.html).

## B2B v1.3.4

*9 agosto 2022*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.5.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce non invia più notifiche e-mail ogni volta che una società esistente viene aggiornata da una chiamata API. Le e-mail ora vengono inviate solo quando viene creata un’azienda.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce ora calcola correttamente un totale complessivo di un preventivo negoziabile quando l&#39;impostazione di calcolo delle imposte **[!UICONTROL Enable Cross Border Trade]** è abilitata.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-322-->I prodotti configurabili ora vengono spostati nell&#39;ultima posizione nell&#39;elenco dei prodotti dopo l&#39;aggiornamento delle scorte quando l&#39;impostazione **[!UICONTROL Move out of stock to the bottom]** è abilitata. Viene implementata una nuova query di database personalizzata per garantire che l’ordinamento dell’indice Elasticsearch rispetti quello abilitato dall’amministratore. In precedenza, i prodotti configurabili e i relativi prodotti secondari non venivano spostati in fondo all’elenco quando questa impostazione era abilitata.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-308-->L&#39;e-mail dell&#39;ordine di acquisto ora rispetta l&#39;impostazione di invio e-mail di ogni sito Web in una distribuzione multisito. Un controllo per l&#39;impostazione **[!UICONTROL Disable Email Communications]** è stato aggiunto alla logica personalizzata per le code e-mail. In precedenza, Adobe Commerce non rispettava l’impostazione di invio dell’e-mail per il sito web secondario.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-302-->Il titolo del campo SKU della pagina Ordine rapido è stato modificato per maggiore chiarezza.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce visualizza ora un messaggio di errore più informativo quando un acquirente immette uno SKU non valido nel campo **Inserisci SKU o nome prodotto**.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1753-->Il campo **[!UICONTROL Account Created in]** per un amministratore società ora mantiene il valore previsto dopo il salvataggio della società.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-722 -->La query `customer` non restituisce più risultati vuoti quando recupera gli elenchi di richieste di acquisto filtrati da `uid`.

![È stato risolto il problema](../assets/fix.svg) <!--- ACP2E-210 -->È stato aggiunto un plug-in prima della chiamata `collectQuoteTotals` per garantire che i crediti dell&#39;archivio vengano applicati una sola volta.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-665 -->I clienti vengono ora reindirizzati alla pagina di accesso quando il loro account viene eliminato da un amministratore dall&#39;amministratore. In precedenza, Adobe Commerce generava un errore. Il blocco di codice del plug-in (`SessionPlugin`) si trova ora nel blocco `try…catch`. In precedenza, questo codice non veniva racchiuso all’interno del blocco generico di gestione delle eccezioni.

![È stato risolto il problema](../assets/fix.svg) <!--- ACP2E-661 --> Nella pagina Ordine rapido in modalità mobile, premendo **Invio** dopo aver immesso un nome di prodotto o uno SKU valido, l&#39;acquirente passa al campo successivo come previsto.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-607 -->Il nome della società è ora visibile come previsto nelle sezioni relative agli indirizzi di fatturazione e spedizione del flusso di lavoro di pagamento.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-375 -->Il credito dello store non è più disponibile quando il metodo di pagamento **[!UICONTROL Zero Subtotal Checkout]** è disabilitato. In precedenza, la casella di controllo Credito store non funzionava durante il posizionamento dell’ordine da parte dell’amministratore. L&#39;applicazione non ha effettuato l&#39;ordine con il credito dell&#39;archivio e ha visualizzato questo errore: `The requested Payment Method is not available`.

## B2B v1.3.3-p15

*12 agosto 2025*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-71](https://helpx.adobe.com/it/security/products/magento/apsb25-71.html).

## B2B v1.3.3-p14

*10 giugno 2025*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.5-p12.

![Problema risolto](../assets/fix.svg) Include le correzioni di sicurezza documentate in [Bollettino sulla sicurezza APSB25-50](https://helpx.adobe.com/it/security/products/magento/apsb25-50.html).

## B2B v1.3.3

*9 agosto 2022*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.4.

![Problema risolto](../assets/fix.svg) <!--- MC-41985--> Il tempo necessario per eseguire l&#39;aggiornamento da Adobe Commerce 2.3.x a Adobe Commerce 2.4.x in implementazioni con più di 100.000 ruoli aziendali è stato notevolmente ridotto.

![Problema risolto](../assets/fix.svg) <!--- MC-42153--> La richiesta POST `V1/order/:orderId/invoice` ora supporta la creazione di fatture parziali quando il metodo di pagamento **[!UICONTROL Payment on Account]** è abilitato. In precedenza, Adobe Commerce ha generato questo errore: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problema risolto](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro ora funziona come previsto con un preventivo B2B negoziabile quando il carrello del cliente contiene altri prodotti. Adobe Commerce ora elabora correttamente l’ordine e invia un’e-mail al cliente come previsto. In precedenza, Adobe Commerce generava un errore irreversibile e inviava al cliente un’e-mail di conferma con valori pari a zero.

![Problema risolto](../assets/fix.svg) La paginazione <!--- MC-41819--> è ora visualizzata correttamente nella pagina dei risultati della ricerca nel catalogo dopo l&#39;esclusione di alcuni prodotti nel catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42886--> Gli attributi personalizzati del cliente vengono ora salvati come previsto durante la creazione o il salvataggio di un utente della società nell&#39;amministratore.

![Problema risolto](../assets/fix.svg) <!--- MC-42927--> Il pulsante **[!UICONTROL Submit]** nel modulo Crea nuova società è ora disattivato dopo un clic per impedire l&#39;invio di più moduli. In precedenza, era possibile inviare il modulo più volte facendo clic ripetutamente su questo pulsante, generando un errore.

![Problema risolto](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce non visualizza più il collegamento di riordino nella vetrina quando un acquirente accede a un negozio per il quale i riordini sono stati disabilitati.

![Problema risolto](../assets/fix.svg) <!--- MC-43115--> La ricerca rapida per ordine per SKU ora non distingue tra maiuscole e minuscole quando è abilitato il catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42203--> È ora possibile aggiornare un file per un attributo del cliente durante la creazione di una società. In precedenza, quando si tentava di creare una società con un allegato di tipo `File`, Adobe Commerce non creava la società e registrava questo errore nel registro eccezioni: `Something went wrong while saving file`.

![Problema risolto](../assets/fix.svg) <!--- MC-42242--> È ora possibile creare un&#39;azienda con un account cliente con un attributo personalizzato con un tipo (`File`) o (`Image`). In precedenza, se l’account disponeva di una di queste opzioni personalizzabili, il caricatore della pagina di modifica dell’azienda non veniva risolto, impedendo la modifica dei dettagli dell’azienda.

![Problema risolto](../assets/fix.svg) <!--- MC-42268--> La query `products` ora restituisce un campo `total_count` preciso quando il catalogo condiviso è abilitato.

![Problema risolto](../assets/fix.svg) <!--- MC-42203--> È ora possibile aggiornare un file per un attributo del cliente durante la creazione di una società. In precedenza, quando si tentava di creare una società con un allegato di tipo `File`, Adobe Commerce non creava la società e registrava questo errore nel registro eccezioni: `Something went wrong while saving file`.

![Problema risolto](../assets/fix.svg) <!--- MC-43178--> Le pagine _Configurazione società_ e _Crea società_ ora funzionano come previsto dopo aver disabilitato un metodo di spedizione online. È stata aggiunta una verifica per impedire il tentativo di elaborazione dei moduli di spedizione disabilitati. In precedenza, Adobe Commerce visualizzava questo errore: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problema risolto](../assets/fix.svg) <!--- MC-42214--> La pagina _Categoria_ visualizza ora dati di prodotto coerenti durante la generazione delle autorizzazioni durante l&#39;indicizzazione parziale. A questo processo è stato aggiunto un nuovo indicizzatore parziale per le autorizzazioni della directory. In precedenza, i dati visualizzati durante l’esecuzione dell’indicizzatore non erano corretti.

![Problema risolto](../assets/fix.svg) <!--- MC-42567--> La query `categoryList` ora restituisce il numero corretto di prodotti quando vengono utilizzate le autorizzazioni del catalogo e i prodotti vengono assegnati a un catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42528--> La query `categoryList` rispetta ora le autorizzazioni delle categorie e restituisce solo le categorie consentite. In precedenza, restituiva tutte le categorie assegnate e non assegnate.

![Problema risolto](../assets/fix.svg) <!--- MC-42399--> La richiesta `rest/V1/company/{id}` ora restituisce `is_purchase_order_enabled` valori di attributo come previsto.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-128--> Gli attributi cliente personalizzati vengono ora visualizzati come previsto nella scheda _Amministratore società_.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-130--> Il blocco Elenco desideri nella pagina Il mio account viene ora visualizzato come previsto per gli amministratori della società e gli utenti della società.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-133--> Gli errori di ordine rapido non vengono più visualizzati nel carrello. In precedenza, Adobe Commerce visualizzava questo errore nel carrello quando lo SKU non veniva trovato nel catalogo: `The SKU was not found in the catalog`.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-194--> Le operazioni di salvataggio del catalogo condiviso sono state ottimizzate per essere eseguite più rapidamente. In precedenza, il salvataggio di un catalogo condiviso con molti gruppi di clienti poteva richiedere alcuni minuti.

![Problema risolto](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce ora elimina tutte le autorizzazioni delle sottocategorie dalla tabella `sharedcatalog_category_permissions` quando la categoria principale viene eliminata. In precedenza, venivano rimossi solo i dati della categoria principale.

## B2B v1.3.2

*29 agosto 2022*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.3.

![Problema risolto](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce ora invia e-mail di aggiornamento sulle offerte negoziabili scadute. In precedenza, alla scadenza di un preventivo negoziabile, Adobe Commerce non inviava e-mail di aggiornamento.

![Problema risolto](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce ora invia e-mail di aggiornamento con scadenza imminente e preventivi negoziabili scaduti quando manca un processo `cron`.

### Azienda

![È stato risolto il problema](../assets/fix.svg) <!--- MC-41542--> Nel campo a discesa Crea nuovo paese per la pagina dell&#39;account della società non sono più elencati valori di opzione vuoti. In precedenza, i primi due valori dell&#39;opzione e il codice paese `AN` erano vuoti.

![Problema risolto](../assets/fix.svg) <!--- MC-41260--> Se si fa clic sul pulsante **[!UICONTROL Return]** per un ordine creato da un utente della società, ora viene reindirizzato un utente amministratore alla pagina Crea reso come previsto. In precedenza, l&#39;amministratore veniva reindirizzato alla pagina Cronologia ordini.

![È stato risolto il problema](../assets/fix.svg) [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} <!--- MC-40798--> Adobe Commerce non ha più esito negativo con un errore di memoria insufficiente durante l&#39;esecuzione del metodo `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` durante `bin/magento setup:upgrade`. In precedenza, Adobe Commerce non utilizzava la dimensione batch per la raccolta durante l’inizializzazione delle autorizzazioni, ma caricava una raccolta di tutti i ruoli aziendali.

![Problema risolto](../assets/fix.svg) <!--- MC-40551--> Gli utenti della società ora possono modificare e aggiornare i valori degli attributi personalizzati del cliente. In precedenza, questi attributi non venivano associati correttamente al modulo utente di creazione e modifica. Un utente della società può immettere valori di attributo diversi, ma Adobe Commerce non li ha salvati correttamente.

![Problema risolto](../assets/fix.svg) <!--- MC-32653--> La struttura delle risorse per le autorizzazioni del ruolo della società ora può essere tradotta come previsto. In precedenza, la struttura delle autorizzazioni non veniva tradotta anche se erano presenti file di traduzione validi.

![Problema risolto](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce ora salva i valori degli attributi cliente personalizzati per gli utenti B2B come previsto. In precedenza, la creazione di un account aziendale contenente attributi cliente personalizzati causava un errore di modello e Adobe Commerce non caricava correttamente il modulo. L&#39;aggiunta di un argomento al layout di `company_create_account` ha risolto questo problema.

![È stato risolto il problema](../assets/fix.svg) <!--- MC-41721--> I filtri degli utenti della società come Mostra tutti gli utenti, Mostra utenti attivi e Mostra utenti inattivi ora funzionano come previsto. In precedenza, il filtraggio delle azioni sulla pagina utente dell’azienda causava un errore JavaScript.

### Credito società

![Problema risolto](../assets/fix.svg) <!--- MC-41551--> Gli amministratori con account con restrizioni che includono solo privilegi a livello di sito Web possono ora creare una società che utilizza una valuta diversa rispetto al sito Web.

![Problema risolto](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce ora invia e-mail aziendali dall&#39;indirizzo e-mail e dall&#39;ambito `from` corretti. In precedenza, Adobe Commerce non considerava l’ambito del sito web durante l’invio dell’assegnazione del credito aziendale o l’aggiornamento dell’e-mail.

### Ordine rapido

![Problema risolto](../assets/fix.svg) <!--- MC-42104--> La creazione di un ordine utilizzando l&#39;ordinamento rapido da un file CSV ora funziona come previsto con SKU inesistenti.

![È stato risolto il problema](../assets/fix.svg) <!--- MC-40268--> L&#39;utilizzo dell&#39;ordine rapido per eseguire ricerche in più SKU ora funziona come previsto. In precedenza, i risultati includevano voci duplicate.

![Problema risolto](../assets/fix.svg) <!--- MC-40261--> La visualizzazione dell&#39;elenco dei prodotti aggiunti ora tratta gli SKU immessi in lettere minuscole e maiuscole allo stesso modo quando si utilizzano gli SKU per selezionare più prodotti durante l&#39;ordine rapido.

![Problema risolto](../assets/fix.svg) <!--- MC-40225--> L&#39;utilizzo dell&#39;ordine rapido consente di aggiungere prodotti nella quantità specificata dall&#39;acquirente. In precedenza, Adobe Commerce aggiungeva un solo prodotto anche quando le quantità specificate dall’acquirente superavano il valore di uno.

![Problema risolto](../assets/fix.svg) <!--- MC-41283--> La funzione di completamento automatico dell&#39;ordine rapido ora funziona con SKU parziali.

![Problema risolto](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce ora visualizza i prodotti configurati come **Non visibili singolarmente** nell&#39;elenco di suggerimenti automatici e nei risultati della ricerca della pagina Ordine rapido.

![Problema risolto](../assets/fix.svg) <!--- MC-42402--> Gli acquirenti ora possono utilizzare il modulo Ordine rapido per aggiungere più prodotti in base agli SKU che includono caratteri maiuscoli. In precedenza, veniva aggiunto solo il primo prodotto.

### Offerta negoziabile

![Problema risolto](../assets/fix.svg) <!--- MC-41232--> Gli acquirenti vengono ora reindirizzati alla pagina delle offerte negoziabili dopo aver incollato il collegamento a un&#39;offerta negoziabile nel campo URL e aver effettuato l&#39;accesso. In precedenza, gli acquirenti venivano reindirizzati alla pagina Il mio account.

![Problema risolto](../assets/fix.svg) <!--- MC-39317--> Il riordinamento ora funziona come previsto per gli ordini che contengono un prodotto con un&#39;opzione di personalizzazione data per un account cliente creato durante l&#39;estrazione. In precedenza, Adobe Commerce non elaborava il riordino e visualizzava questo errore: `The product has required options. Enter the options and try again`.

![Problema risolto](../assets/fix.svg) <!--- MC-39063--> L&#39;indirizzo di spedizione di un preventivo negoziabile non è più modificabile durante l&#39;estrazione quando il modulo Ordine di acquisto è disabilitato. Questo comportamento è il risultato di una correzione precedente in cui `isQuoteAddressLocked` è stato rimosso dal renderer di estrazione preventivo negoziabile.

![Problema risolto](../assets/fix.svg) <!--- MC-38967--> I commercianti possono ora aggiungere prodotti a un preventivo negoziabile dall&#39;amministratore.

### Ordini di acquisto

![Problema risolto](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce visualizza ora un messaggio di errore informativo come previsto quando si inserisce un ordine di acquisto utilizzando PayPal Express Checkout quando l&#39;attributo **[!UICONTROL Name Prefix]** è impostato su `required`. In precedenza, Adobe Commerce non effettuava l’ordine né visualizzava un messaggio di errore.

![Problema risolto](../assets/fix.svg) <!--- MC-39620--> Il componente dell&#39;interfaccia utente per l&#39;indirizzo di fatturazione nel modulo Ordine di acquisto ora utilizza correttamente l&#39;indirizzo del preventivo quando Google Tag Manager è abilitato. In precedenza, si verificava un errore JavaScript nella pagina di pagamento.

### Elenchi richieste

![Problema risolto](../assets/fix.svg) <!--- MC-40426--> I commercianti ora possono utilizzare l&#39;endpoint POST `rest/all/V1/requisition_lists` per creare un elenco di richieste di acquisto per un cliente. In precedenza, Adobe Commerce generava questo errore 400 quando si tentava di creare un elenco di richieste di acquisto: `Could not save Requisition List`.

![Problema risolto](../assets/fix.svg) <!--- MC-41123--> Il pulsante **[!UICONTROL Add to Requisition List]** viene ora visualizzato per i prodotti in magazzino di un carrello quando il carrello contiene anche prodotti esauriti. In precedenza, se un carrello conteneva due prodotti, uno dei quali era esaurito, il pulsante _[!UICONTROL Add to Requisition List]_&#x200B;non veniva visualizzato per nessuno dei due prodotti.

![Problema risolto](../assets/fix.svg) <!--- MC-40877--> Ora puoi utilizzare l&#39;API REST per aggiungere un prodotto a un elenco di richieste.

![Problema risolto](../assets/fix.svg) <!--- MC-40155--> I valori dell&#39;elenco delle richieste di acquisto **[!UICONTROL Latest Activity Date]** ora sono conformi al formato locale.

![Problema risolto](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce non genera più un errore irreversibile quando si modifica un prodotto bundle da un elenco di richieste.

![Problema risolto](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce ora visualizza il prezzo del prodotto corretto quando si aggiunge un prodotto con un&#39;opzione personalizzabile `(File)` a un elenco di desideri da un elenco di richieste. Anche il collegamento al file caricato è visibile come previsto. In precedenza, Adobe Commerce mostrava prezzi del prodotto errati e non mostrava il collegamento al file.

![Problema risolto](../assets/fix.svg) <!--- MC-36383--> I prodotti con un&#39;opzione personalizzabile `(File)` possono ora essere aggiunti a un carrello da un elenco di richieste.

### Catalogo condiviso

![Problema risolto](../assets/fix.svg) <!--- MC-40497--> Un amministratore con un ruolo limitato a un sito Web specifico può ora creare, visualizzare e modificare un catalogo condiviso. In precedenza, Adobe Commerce generava un errore irreversibile quando un amministratore con un ruolo limitato tentava di creare un catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-41337--> I risultati della navigazione a livelli ora includono un conteggio accurato dei prodotti con attributi filtrati e gli acquirenti possono applicare più filtri. In precedenza era possibile applicare un solo filtro e Adobe Commerce mostrava un conteggio di prodotti non accurato nella navigazione a più livelli.

![Problema risolto](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce ora visualizza correttamente i conteggi dei prodotti nei filtri di navigazione a livelli nei risultati di ricerca. In precedenza, un plug-in per la pagina Risultati ricerca non utilizzava Elasticsearch, ma inviava una nuova query al database.

![Problema risolto](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce non elimina più i prezzi dei livelli quando un commerciante elimina tutti i prodotti da un catalogo condiviso predefinito.

![Problema risolto](../assets/fix.svg) <!--- MC-39802--> I filtri sono ora filtrati in base alla categoria corrente e visualizzati correttamente in tutte le pagine quando i cataloghi condivisi sono abilitati. In precedenza, i filtri venivano calcolati in modo errato solo per la pagina corrente e non venivano filtrati per la categoria corrente.

![Problema risolto](../assets/fix.svg) <!--- MC-39522--> La query di GraphQL `products` non restituisce più l&#39;intervallo di prezzo e la categoria di un prodotto per i prodotti non assegnati a un catalogo condiviso quando è abilitato il catalogo condiviso. In precedenza, la query restituiva le aggregazioni del prodotto, anche se il prodotto stesso non veniva restituito nell&#39;array `items`.

## B2B v1.3.1

*9 febbraio 2021*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.2.

![Nuovi](../assets/new.svg) metodi di pagamento online sono ora supportati per gli ordini fornitore.

![Problema risolto](../assets/fix.svg) L&#39;aggiunta di un prodotto configurabile al carrello direttamente da un elenco di richieste di acquisto quando il prodotto è stato utilizzato in un ordine precedente non restituisce più un errore di sistema.

![Problema risolto](../assets/fix.svg) Adobe Commerce ora visualizza correttamente la scheda Richiedi la mia approvazione per gli ordini fornitore quando viene distribuita una configurazione di database divisa.

![Problema risolto](../assets/fix.svg) Adobe Commerce visualizza ora i dettagli sui prodotti in bundle e sulle gift card quando visualizzi gli ordini di acquisto.

![Problema risolto](../assets/fix.svg) Gli acquirenti vengono ora reindirizzati come previsto dopo aver effettuato l&#39;accesso al loro account durante la navigazione in un archivio in cui **[!UICONTROL Website Restriction]** è abilitato e **[!UICONTROL Restriction Mode]** è impostato su `Private Sales: Login Only`. In precedenza, gli acquirenti venivano reindirizzati alla home page del negozio. <!--- MC-38934-->

![Problema risolto](../assets/fix.svg) La cronologia degli ordini ora viene caricata come previsto nella pagina del dashboard account dell&#39;amministratore della società nelle distribuzioni con una gerarchia di società B2B che contiene molti clienti (maggiore di 13000). In precedenza, la cronologia degli ordini veniva caricata lentamente o non veniva caricata affatto e Adobe Commerce mostrava un errore 503. <!--- MC-38830-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più più più messaggi di avviso identici quando si aggiunge un prodotto non configurato con opzioni personalizzabili a un elenco richieste di acquisto da una pagina Categoria. <!--- MC-38342-->

![Problema risolto](../assets/fix.svg) I prodotti nuovi e duplicati sono ora visibili come previsto nella pagina della categoria quando sono abilitati i cataloghi condivisi B2B. <!--- MC-38307-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora mantiene il `store_id` corretto associato a un amministratore della società quando il gruppo di clienti di una società viene aggiornato. In precedenza, `store_id` è stato modificato nell&#39;archivio predefinito al momento dell&#39;aggiornamento del gruppo. <!--- MC-38196-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora salva un prodotto raggruppato in un elenco di richieste di acquisto come elenco di prodotti semplici nello stesso modo in cui aggiunge un prodotto raggruppato a un carrello. In precedenza, a causa del modo in cui Adobe Commerce salvava i prodotti raggruppati, il collegamento per un prodotto raggruppato dall’elenco delle richieste di acquisto veniva sempre reindirizzato ai prodotti semplici e non al prodotto raggruppato. <!--- MC-38049-->

![Problema risolto](../assets/fix.svg) È ora possibile filtrare gli ordini in base al campo **[!UICONTROL Company Name]** durante l&#39;esportazione delle informazioni dell&#39;ordine in formato CSV. In precedenza, Adobe Commerce registrava un errore in `var/export/{file-id}`. <!--- MC-37785-->

![Problema risolto](../assets/fix.svg) Adobe Commerce visualizza ora la finestra a comparsa Crea elenco richieste di acquisto come previsto quando si seleziona la scheda Crea nuovo elenco richieste di acquisto nella vetrina. <!--- MC-37915-->

![Problema risolto](../assets/fix.svg) Gli elenchi delle richieste di acquisto ora includono tutti i prodotti raggruppati e le quantità aggiunte all&#39;elenco. In precedenza, quando un commerciante passava a un elenco di richieste di acquisto dopo avervi aggiunto prodotti da una pagina dei dettagli del prodotto, Adobe Commerce visualizzava questo errore: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problema risolto](../assets/fix.svg) La visualizzazione corretta dell&#39;archivio è ora associata al sito Web rilevante quando si crea una società in una distribuzione multisito. In precedenza non era possibile creare una società e Adobe Commerce ha visualizzato questo errore: `The store view is not in the associated website`. <!--- MC-37488-->

![Problema risolto](../assets/fix.svg) L&#39;ordinamento di prodotti per SKU tramite Ordine rapido non determina più quantità di prodotti duplicate nel file CSV. <!--- MC-37427-->

![Problema risolto](../assets/fix.svg) Il pulsante **[!UICONTROL Add to Cart]** non è più bloccato se la sezione _[!UICONTROL Enter Multiple SKUs]_&#x200B;della pagina Ordine rapido contiene un valore vuoto. Al contrario, Adobe Commerce ora visualizza un messaggio che richiede di immettere SKU validi. <!--- MC-37387-->

![Problema risolto](../assets/fix.svg) Adobe Commerce visualizza ora questo messaggio nella pagina del prodotto quando si invia una revisione del prodotto da un elenco di richieste: `You submitted your review for moderation`. La revisione viene visualizzata anche nella pagina Revisioni in sospeso (Amministratore **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). In precedenza, anche se Adobe Commerce aggiungeva la revisione all’elenco delle revisioni in sospeso, generava un errore 404 nella pagina del prodotto. <!--- MC-37119-->

![Problema risolto](../assets/fix.svg) Le prestazioni del consumer `sharedCatalogUpdateCategoryPermissions` sono state migliorate. Dopo aver creato un catalogo condiviso, l’indicizzatore delle autorizzazioni del catalogo ora utilizza solo l’ID del gruppo di clienti del catalogo condiviso e non tutti i gruppi di clienti. <!--- MC-36770-->

![Problema risolto](../assets/fix.svg) I campi attributo dell&#39;indirizzo del cliente personalizzati associati all&#39;indirizzo non predefinito di un acquirente vengono ora salvati come previsto nel flusso di lavoro di estrazione della vetrina. <!--- MC-36630-->

![Problema risolto](../assets/fix.svg) È ora possibile inserire gli ordini per i prodotti che appartengono al catalogo condiviso predefinito di un archivio tramite l&#39;API REST amministratore (`rest/V1/carts/{<CART_ID>/items`) come previsto. Adobe Commerce ora controlla se il prodotto è stato assegnato a un catalogo pubblico prima della convalida delle autorizzazioni del catalogo condiviso in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. In precedenza, Adobe Commerce non aggiungeva il prodotto al carrello e generava questo errore: `No such shared catalog entity`. <!--- MC-36535-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora invia le e-mail di registrazione utente della nuova società dall&#39;indirizzo dell&#39;archivio Adobe Commerce. In precedenza, questo messaggio e-mail veniva inviato dall’indirizzo dell’amministratore della società. <!--- MC-36480-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora controlla gli attributi personalizzati per verificare la duplicazione dei nomi di attributi aziendali riservati prima di consentire a un commerciante di salvare un nuovo attributo. <!--- MC-36282-->

![Problema risolto](../assets/fix.svg) La query `credit_history` ora restituisce lo storico dei crediti della società specificata sia per l&#39;importo originariamente allocato che per l&#39;importo acquistato. In precedenza, questa query restituiva un errore.

![Problema risolto](../assets/fix.svg) I campi **[!UICONTROL Company]** e **[!UICONTROL Job Title]** nella pagina Modifica informazioni account non sono più modificabili.

### Problemi noti

- Gli acquirenti B2B possono utilizzare metodi di pagamento online per aggirare il flusso abituale degli ordini di acquisto. Questo scenario può verificarsi se l&#39;acquirente può ridurre l&#39;intero totale di pagamento a 0, ad esempio tramite un codice promozionale o una gift card, e quindi rimuovere il codice o la gift card. Anche in queste condizioni, Adobe Commerce continua a effettuare l’ordine per l’importo corretto in base ai prezzi degli articoli nel catalogo assegnato. **_Soluzione_**: disabilitare le carte regalo e i codici coupon quando i metodi di pagamento online sono abilitati per l&#39;approvazione dell&#39;ordine fornitore. <!--- B2B-1603-->

- Gli acquirenti vengono reindirizzati al carrello quando tentano di effettuare un ordine da un ordine di acquisto utilizzando PayPal Express Checkout quando **[!UICONTROL In-Context Mode]** è disabilitato. <!--- B2B-1604-->

- Adobe Commerce talvolta visualizza un errore 404 quando un acquirente crea un ordine di acquisto e poi passa alla pagina di pagamento. Questo errore si verifica quando un acquirente ha creato in precedenza un ordine di acquisto diverso con un metodo di pagamento online prima di passare alla pagina di pagamento senza completare l&#39;acquisto precedente. L&#39;acquirente può comunque effettuare l&#39;ordine di acquisto. **_Operazioni da eseguire_**: nessuna operazione. <!--- B2B-1605-->

- Gli sconti per un metodo di pagamento specifico persistono durante il pagamento di un ordine di acquisto anche quando l&#39;acquirente modifica il metodo di pagamento durante il pagamento finale. Di conseguenza, i clienti possono ricevere uno sconto a cui non hanno diritto. Questo problema si verifica perché una regola del carrello per il metodo di pagamento originale viene ancora applicata nonostante la modifica del metodo di pagamento. **_Operazioni da eseguire_**: nessuna operazione. Consulta il [problema noto B2B di Adobe Commerce 2.4.2: lo sconto rimane per gli ordini di acquisto online dopo la modifica del metodo di pagamento](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html?lang=it) _articolo della Knowledge Base_. <!-- B2B-1012 -->

- La query `deleteRequisitionListOutput` restituisce dettagli sull&#39;elenco di richieste di acquisto eliminato anziché sugli elenchi di richieste rimanenti. <!--- MC-39894-->

## B2B v1.3.0

*15 ottobre 2020*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

Questa versione include miglioramenti alle approvazioni degli ordini, ai metodi di spedizione, al carrello acquisti e alla registrazione delle azioni dell’amministratore.

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.1.

![Nuove](../assets/new.svg) approvazioni di ordini B2B sono state migliorate per migliorare l&#39;usabilità e consentire azioni in blocco sugli ordini fornitore.

![I nuovi](../assets/new.svg) commercianti B2B possono ora controllare i metodi di spedizione offerti a ciascuna società.<!--- BUNDLE-160 161 162 -->

![Nuovo](../assets/new.svg) I commercianti possono ora consentire agli utenti di cancellare il contenuto del carrello in un&#39;unica azione e possono configurare questa funzionalità in modo indipendente su ogni sito Web <!--- BUNDLE-108 -->

![Nuovi](../assets/new.svg) acquirenti B2B possono ora aggiungere singoli articoli o l&#39;intero contenuto del carrello direttamente a un elenco di richieste di acquisto. <!--- BUNDLE-145 144-->

![I nuovi](../assets/new.svg) commercianti B2B possono creare ordini dall&#39;amministratore per conto dei clienti utilizzando Pagamento in conto come metodo di pagamento. <!--- BUNDLE-166 178-->

![Nuovo](../assets/new.svg) I commercianti possono ora visualizzare direttamente tutti i preventivi associati a un utente dalla pagina dei dettagli del cliente. <!--- BUNDLE-139 -->

![New](../assets/new.svg) I commercianti possono ora filtrare la griglia Clienti online per società. <!--- BUNDLE-137 -->

![Nuovi](../assets/new.svg) Gli amministratori ora possono filtrare i clienti nell&#39;amministratore in base al rappresentante commerciale <!--- BUNDLE-110 -->

![Nuovo](../assets/new.svg) Per ridurre la creazione di account fraudolenti o spam, gli esercenti possono ora abilitare Google reCAPTCHA nel modulo di richiesta della nuova azienda nella vetrina. <!--- BUNDLE-154 -->

![Nuove](../assets/new.svg) azioni dell&#39;amministratore eseguite nei moduli aziendali sono ora registrate nel registro delle azioni dell&#39;amministratore. Le azioni sono registrate da tutti i moduli aziendali rilevanti: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più il pulsante **[!UICONTROL Delete customer]** nella pagina **Clienti** quando l&#39;amministratore connesso non dispone dei diritti per eliminare i clienti nelle distribuzioni in cui è installato B2B. <!--- MC-35655-->

![Problema risolto](../assets/fix.svg) Il gruppo di clienti non viene più modificato automaticamente per un cliente assegnato a un&#39;azienda quando si modifica il cliente nella griglia Cliente. <!--- MC-35254-->

![Problema risolto](../assets/fix.svg) Quando un commerciante crea un catalogo condiviso, le autorizzazioni vengono ora impostate automaticamente su `Allow` per le funzionalità **[!UICONTROL Display Product Prices]** e **[!UICONTROL Add to Cart]** nelle categorie quando al gruppo di clienti viene assegnato questo accesso nelle impostazioni delle autorizzazioni del catalogo. In precedenza, queste impostazioni venivano impostate automaticamente su `Deny` anche quando le autorizzazioni del catalogo erano impostate su `Allow`.<!--- MC-34792-->

![Problema risolto](../assets/fix.svg) Le autorizzazioni della categoria del catalogo condiviso non vengono più sovrascritte quando un prodotto viene modificato dalla pagina di modifica del prodotto.<!--- MC-34777-->

![Problema risolto](../assets/fix.svg) Adobe Commerce invia ora una notifica e-mail di conferma che un cliente dispone dell&#39;autorizzazione per superare il limite di credito designato quando un esercente abilita l&#39;impostazione **[!UICONTROL Allow To Exceed Credit Limit]**. In precedenza, l’e-mail di notifica inviata da Adobe Commerce indicava che il cliente non disponeva dell’autorizzazione per superare il limite. <!--- MC-34584-->

![Problema risolto](../assets/fix.svg) Il contenitore HTML che racchiude il prezzo del prodotto negli elenchi delle richieste di acquisto ora viene riprodotto correttamente per i figli dei prodotti inclusi nel pacchetto. <!--- MC-36331-->

![Problema risolto](../assets/fix.svg) I commercianti ora possono indicare la lingua in cui l&#39;e-mail dell&#39;utente della società viene inviata al momento della creazione di una società in implementazioni multilingue. In precedenza, il menu a discesa consentiva ai commercianti di selezionare la vista e la lingua appropriate per il negozio.  <!--- MC-35777-->

![Problema risolto](../assets/fix.svg) I campi degli attributi dell&#39;indirizzo del cliente personalizzati vengono ora visualizzati come previsto nel flusso di lavoro di estrazione della vetrina. <!--- MC-35607-->

![È stato risolto il problema](../assets/fix.svg). La scheda di configurazione delle funzionalità B2B ora si apre correttamente. <!--- MC-35458-->È ora possibile utilizzare QuickOrder per aggiungere prodotti al carrello e rimuovere gli elementi. In precedenza, quando un acquirente utilizzava QuickOrder per aggiungere più prodotti al carrello e poi rimuoveva un prodotto, quest’ultimo non veniva rimosso. <!--- MC-35327-->

![Problema risolto](../assets/fix.svg) È ora possibile aggiornare una società utilizzando la richiesta REST API PUT `/V1/company/:companyId` senza specificare `region_id` quando lo stato è configurato come **non richiesto**. In precedenza, anche se `region_id` non era obbligatorio, Adobe Commerce restituiva un errore se non era specificato. <!--- MC-35304-->

![Problema risolto](../assets/fix.svg) Quando crei o aggiorni una società B2B utilizzando l&#39;API REST (`http://magento.local/rest/V1/company/2`, dove `2` rappresenta l&#39;ID società), la risposta ora include le impostazioni per `applicable_payment_method` o `available_payment_methods` come previsto. <!--- MC-35248-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più una pagina 404 quando un commerciante utilizza il pulsante **Invio** invece di fare clic sul pulsante **[!UICONTROL Save]** durante la creazione di un elenco di richieste di acquisto nella vetrina.<!--- MC-35094-->

![Problema risolto](../assets/fix.svg) Le autorizzazioni della categoria non cambiano più quando un nuovo prodotto viene assegnato a un catalogo condiviso pubblico. In precedenza, le autorizzazioni per le categorie venivano duplicate. <!--- MC-34386-->

![È stato risolto il problema](../assets/fix.svg) L&#39;endpoint REST API PUT `rest/default/V1/company/{id}`, utilizzato per aggiornare l&#39;e-mail aziendale, non fa più distinzione tra maiuscole e minuscole. <!--- MC-34308-->

![Problema risolto](../assets/fix.svg) La disabilitazione dei moduli di premi non influisce più sulle funzionalità B2B negli account cliente. In precedenza, quando i moduli di ricompensa venivano disabilitati, le seguenti schede relative a B2B non venivano visualizzate: Profilo società, Utenti società e Ruoli e autorizzazioni.<!--- MC-34191-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora utilizza il nome del mittente corretto nelle notifiche e-mail quando vengono apportate modifiche agli account aziendali. In precedenza, Adobe Commerce utilizzava il nome del mittente del contatto generale definito nell’ambito predefinito per tutte le e-mail. <!--- MC-33917-->

![Problema risolto](../assets/fix.svg) È ora possibile implementare correttamente il multishipping per gli ordini che contengono prodotti sia fisici che virtuali. <!--- MC-33818-->

![Problema risolto](../assets/fix.svg) I commercianti possono ora creare utenti società dalla sezione _[!UICONTROL Company Users]_&#x200B;nelle pagine Il mio account e la struttura della società quando **[!UICONTROL Access Restriction]**&#x200B;è abilitato e **[!UICONTROL Restriction Mode]**&#x200B;è impostato su `Sales: Login Only`. In precedenza, Adobe Commerce generava questo errore quando un commerciante tentava di creare un utente: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non reimposta più il gruppo clienti di un cliente sul valore predefinito quando un cliente salva le informazioni sul proprio account. <!--- MC-33554-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non genera più un errore irreversibile quando un amministratore assegna un cliente con un carrello attivo a un gruppo di clienti. <!--- MC-33313-->

![Problema risolto](../assets/fix.svg) Adobe Commerce fornisce ora un evento DataLayer `addToCart` per le pagine degli elenchi di ordini rapidi e richieste di acquisto.  <!--- MC-33295-->

![Problema risolto](../assets/fix.svg) Le e-mail di notifica inviate ai rappresentanti commerciali assegnati a un&#39;azienda ora includono il logo aziendale assegnato. In precedenza, l’e-mail di notifica includeva il logo LUMA predefinito e non il logo aziendale caricato. <!--- MC-33232-->

![Problema risolto](../assets/fix.svg) Un elenco di richieste ora include tutti i prodotti e le quantità raggruppati che sono stati aggiunti all&#39;elenco. In precedenza, quando un commerciante passava a un elenco di richieste di acquisto dopo avervi aggiunto prodotti da una pagina dei dettagli del prodotto, Adobe Commerce visualizzava questo errore: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problema risolto](../assets/fix.svg) La query `products` ora restituisce un campo `total_count` preciso quando è abilitato il catalogo condiviso. <!--- MC-42268-->

![Problema risolto](../assets/fix.svg) Le pagine Configurazione società e Crea società ora funzionano come previsto dopo la disattivazione di un metodo di spedizione online. È stata aggiunta una verifica per impedire il tentativo di elaborazione dei moduli di spedizione disabilitati. In precedenza, Adobe Commerce visualizzava questo errore: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![È stato risolto il problema](../assets/fix.svg). Il consumo di memoria per i test di integrazione è stato ridotto, migliorando le prestazioni dei test e riducendo il tempo necessario per il completamento. <!--- AC-266-->

## B2B v1.2.0

*28 luglio 2020*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} Adobe Commerce 2.4.0 e versioni successive

![Nuovo](../assets/new.svg) Aggiunto supporto per Adobe Commerce 2.4.0.

![Nuovo](../assets/new.svg) servizio di ricerca ordini per vetrine, con un ringraziamento per il contributo di Marek Mularczyk di [Divante](https://www.divante.com/) e dei membri della community.

![Nuovi](../assets/new.svg) ordini di acquisto migliorati e riscritti. Ora sono inclusi per impostazione predefinita in Adobe Commerce.

![Nuove](../assets/new.svg) regole di approvazione ordine di acquisto sono state implementate. Queste regole consentono agli utenti di controllare il flusso di lavoro Ordine di acquisto creando regole di acquisto per gli ordini.

![Nuovo](../assets/new.svg) Accesso come cliente è ora incluso per impostazione predefinita in Adobe Commerce. Questa funzione consente ai dipendenti del sito di assistere i clienti effettuando l’accesso come cliente per vedere ciò che vedono.

![Problema risolto](../assets/fix.svg) Le aggregazioni di attributi ora funzionano correttamente per la navigazione a livelli con Elasticsearch

![Problema risolto](../assets/fix.svg) La ricerca di ordini per caratteri speciali ora funziona correttamente.

![È stato risolto il problema](../assets/fix.svg). Se si fa clic sul pulsante **[!UICONTROL Clear All]**, ora tutti i filtri vengono espansi anziché compressi.

![Problema risolto](../assets/fix.svg) Il nome/SKU del prodotto è ora incluso nel riepilogo del filtro di ricerca della cronologia ordini.

![Problema risolto](../assets/fix.svg) L&#39;indicatore di ordinamento è ora visualizzato correttamente nella griglia Ordini di acquisto.

![Problema risolto](../assets/fix.svg) Ora è possibile fare clic sui pulsanti Approva, Annulla, Rifiuta e Ordine di acquisto una sola volta. In precedenza, era possibile fare clic più volte sul pulsante.

![Problema risolto](../assets/fix.svg) I pulsanti Approva, Rifiuta, Annulla e Convalida dell&#39;ordine di acquisto ora vengono riprodotti correttamente sui dispositivi mobili.

![È stato risolto un problema](../assets/fix.svg). In precedenza, l&#39;approvazione di un ordine di acquisto con uno sconto scaduto determinava l&#39;inserimento dell&#39;ordine nell&#39;importo completo e non aggiornava il totale dell&#39;ordine di acquisto. Ora il totale dell’ordine di acquisto viene aggiornato per mostrare il totale corretto.

![Problema risolto](../assets/fix.svg) È stato introdotto un problema in 2.3.4 in cui gli attributi di estensione personalizzati non venivano copiati dall&#39;indirizzo del cliente all&#39;indirizzo del preventivo. Questo problema è stato risolto.

![È stato risolto il problema](../assets/fix.svg) Se è installato B2B, veniva visualizzato un errore SQL durante l&#39;assegnazione di categorie a cataloghi condivisi. Questo problema è stato risolto.

![È stato risolto il problema](../assets/fix.svg) A causa di un valore di tipo di variabile errato, gli amministratori non potevano aggiungere prodotti configurabili a un ordine. I menu a discesa delle opzioni non si popolano. Questa funzione ora funziona correttamente.

![È stato risolto un problema](../assets/fix.svg). In precedenza, quando si modificavano le autorizzazioni per le categorie per il gruppo Non connesso, si verificava un errore durante il salvataggio delle modifiche. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) È stata aggiunta una correzione per consentire agli amministratori degli archivi di aggiungere prodotti a un ordine che non si trova nel catalogo condiviso. In precedenza, veniva visualizzato un messaggio di errore quando si aggiungeva un elemento non presente nel catalogo.

![È stato risolto il problema](../assets/fix.svg) [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}. In precedenza, dopo l&#39;esecuzione del comando `php bin/magento indexer:set-dimensions-mode catalog_product_price website` e il tentativo di creare un catalogo condiviso, si verificava un errore. Questo problema è stato risolto.

![È stato risolto il problema](../assets/fix.svg) Quando si aggiungeva una società e si assegnava l&#39;amministratore della società a un sito Web non predefinito, veniva inviato l&#39;ID sito errato, causando un errore. Questo problema è stato risolto.

![È stato risolto il problema](../assets/fix.svg) In precedenza, dopo lo spostamento di un cliente in un altro gruppo di clienti, l&#39;aggiunta di un prodotto a un ordine tramite _Ordine rapido_ non riusciva e generava un errore. Questo problema è stato risolto.

![È stato risolto un problema](../assets/fix.svg). In precedenza, durante il tentativo di estrazione tramite WebAPI con virgolette B2B, veniva inviato un valore non corretto all&#39;API, causando un errore. Questo problema è stato risolto.

![È stato risolto un problema](../assets/fix.svg). In precedenza, quando si impostava una società su &quot;Attiva&quot; tramite l&#39;API, si verificava un errore. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) A causa di un tag `form` non necessario, la pagina dell&#39;ordine è stata aggiornata automaticamente quando si preme INVIO dopo aver modificato un costo di spedizione proposto. Questo problema è stato risolto.

![È stato risolto un problema](../assets/fix.svg). In precedenza, quando si impostava un limite di visualizzazione dei prodotti in una pagina di catalogo e tale limite era inferiore al numero totale di prodotti, si verificava un errore. Questa funzione ora funziona come previsto.

![È stato risolto il problema](../assets/fix.svg) In precedenza, quando si modificava l&#39;amministratore di una società, l&#39;indirizzo dell&#39;amministratore originale veniva copiato nel nuovo amministratore, assegnando loro due indirizzi. Ora viene aggiunto solo l’indirizzo corretto.

![È stato risolto un problema](../assets/fix.svg). In precedenza, l&#39;utilizzo dell&#39;API per salvare un preventivo quando Git era impostato su &quot;Consentito e notifica al cliente&quot; non riusciva. Questa chiamata API ora funziona come previsto.

![Problema risolto](../assets/fix.svg) L&#39;imposta sul prodotto fissa viene ora visualizzata nella pagina dei dettagli Preventivi.

![È stato risolto il problema](../assets/fix.svg). In precedenza, se si faceva clic su un allegato nella scheda Commenti della pagina Le mie citazioni, il file non veniva scaricato. Questo comportamento ora funziona come previsto.

### Problemi noti

- Adobe Commerce genera un’eccezione durante l’aggiornamento a B2B 1.2.0 in una distribuzione multisito. Quando viene eseguito `setup:upgrade`, l&#39;errore si verifica nel modulo `PurchaseOrder`: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Soluzione**: installare l&#39;interfaccia `B2B-716 Add NonTransactionableInterface` nell&#39;hotfix della patch dati `InitPurchaseOrderSalesSequence`, ora disponibile nella sezione **Il mio account** > **Download** di `magento.com`.
- Se un codice di sconto scade prima dell&#39;approvazione di un ordine di acquisto (OA), l&#39;OA continua a visualizzare l&#39;importo scontato, ma dopo l&#39;approvazione dell&#39;OA l&#39;ordine viene collocato al totale non scontato. **Soluzione**: installare l&#39;hotfix `B2B-709 Purchase Order Discount patch` per questo problema, ora disponibile nella sezione **Account personale** > **Download** di `magento.com`.
- Se gli articoli di un ordine di acquisto sono esauriti o la quantità è insufficiente quando l&#39;ordine di acquisto viene convertito in un ordine effettivo, si verifica un errore. Se gli ordini inevasi sono abilitati, l&#39;ordine viene elaborato normalmente.
