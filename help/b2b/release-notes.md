---
title: '''[!DNL Adobe Commerce B2B] note sulla versione'
description: Consulta le note sulla versione per informazioni sulle modifiche apportate in [!DNL Adobe Commerce B2B] versioni.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: e837dded8569cf917be8c36277362f5df77fb708
workflow-type: tm+mt
source-wordcount: '6851'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] note sulla versione

Queste note sulla versione per l’estensione B2B acquisiscono aggiunte e correzioni che Adobe ha aggiunto durante un ciclo di rilascio, tra cui:

![Nuovo](../assets/new.svg) Nuove funzioni
![Problema risolto](../assets/fix.svg) Correzioni e miglioramenti
![Problema noto](../assets/bug.svg) Problemi noti

>[!NOTE]
>
>Consulta [Disponibilità del prodotto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) per informazioni sulle versioni dell’estensione B2B Commerce supportate per le versioni disponibili di Adobe Commerce.

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*13 novembre 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

La versione B2B v1.5.0-beta include nuove funzioni, miglioramenti della qualità e correzioni di bug.

![Nuovo](../assets/new.svg) I miglioramenti apportati alle funzionalità di preventivo consentono a buyer e venditori di gestire i preventivi e la negoziazione dei preventivi in modo più efficace.

- **Salva preventivo come bozza**<!--B2B-2566-->- Durante la creazione di un [richiesta di offerta](quote-request.md) dal carrello, gli acquirenti possono salvare il preventivo come bozza selezionando **[!UICONTROL Save as Draft]** il [!UICONTROL Request a Quote] modulo.

  L&#39;offerta provvisoria non ha una data di scadenza. Gli acquirenti possono esaminare e aggiornare le bozze dei preventivi [!UICONTROL My Quotes] sezione del dashboard dell’account.

- **Rinomina offerta**<!--B2B-2596-->- Gli acquirenti possono ora modificare il nome di un preventivo dalla [Dettagli offerta](account-dashboard-my-quotes.md#quote-actions) selezionando la **[!UICONTROL Rename]** opzione. Questa opzione è disponibile per gli acquirenti autorizzati che modificano il preventivo. Gli eventi di modifica del nome vengono registrati nel registro Cronologia preventivo.

- **Virgolette duplicate**<!--B2B-2701-->- Acquirenti e venditori possono ora creare un nuovo preventivo copiando un preventivo esistente. Viene creata una copia dalla vista Dettaglio preventivo selezionando  **[!UICONTROL Create Copy]** il [Visualizzazione dettagli offerta](quote-price-negotiation.md#button-bar) in Admin o [Vetrina](account-dashboard-my-quotes.md#quote-actions).

- **Blocco sconto voce**<!--B2B-2597-->- Durante la negoziazione dei preventivi, i venditori possono utilizzare il blocco degli sconti della voce per una maggiore flessibilità durante l&#39;applicazione degli sconti. Ad esempio, un venditore può applicare uno sconto speciale su un oggetto e bloccare l&#39;oggetto per evitare ulteriori sconti. Quando un articolo è bloccato, non è possibile aggiornare il prezzo dell&#39;articolo quando viene applicato uno sconto a livello di preventivo. Consulta [Avvia offerta per un acquirente](sales-rep-initiates-quote.md).

![Nuovo ](../assets/new.svg)**Gestione società**<!--B2B-2901-->—Gli esercenti possono ora visualizzare e gestire le società Adobe Commerce come organizzazioni gerarchiche assegnando le società alle società madri designate. Dopo che una società è stata assegnata a una società madre, l&#39;amministratore della società madre può gestire l&#39;account della società. Solo gli utenti amministratori autorizzati possono aggiungere e gestire le assegnazioni aziendali. Per ulteriori informazioni, consulta [Gestisci gerarchia società](assign-companies.md).

- Nella pagina Società, è disponibile una nuova **[!UICONTROL Company Type]** questo campo identifica le aziende padre e figlio. Gli esercenti possono filtrare la visualizzazione aziendale per tipo di società e gestire le società utilizzando elementi riga o azioni in blocco.

- Gli esercenti possono aggiungere e gestire le assegnazioni aziendali dal nuovo **[!UICONTROL Company Hierarchy]** sezione sul [!UICONTROL Company Account] pagina.

- Gli sviluppatori API possono utilizzare il nuovo endpoint REST API per le relazioni con la società `/V1/company/{parentId}/relations` per creare, visualizzare e rimuovere le assegnazioni aziendali. Consulta [Gestire gli oggetti aziendali](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) nel *Guida per gli sviluppatori di API Web*.

![Problema risolto](../assets/fix.svg)<!--ACP2E-1984-->Commercianti che fanno clic su **[!UICONTROL Print]** nella visualizzazione Dettagli preventivo dell&#39;amministratore viene ora richiesto di salvare il preventivo come PDF. In precedenza, i commercianti venivano reindirizzati a una pagina contenente i dettagli delle offerte.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1742-->In precedenza, quando si inviava un preventivo cliente con 0 percentuale e si modificava la quantità, l’amministratore generava un’eccezione ma salvava la quantità. In seguito a questa correzione, per `0 percentage` verrà generata un&#39;eccezione appropriata con un messaggio.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1742-->Durante la negoziazione del preventivo, un venditore può ora specificare un `0%` sconto nel campo Sconto preventivo negoziato e inviare nuovamente il preventivo all&#39;acquirente. In precedenza, se il venditore inseriva uno sconto dello 0% e inviava nuovamente il preventivo all&#39;acquirente, l&#39;Amministratore restituiva un `Exception occurred during quote sending` messaggio di errore.

![Problema risolto](../assets/fix.svg) <!--ACP2E-2097-->La convalida ReCaptcha ora funziona correttamente durante il processo di pagamento di un preventivo B2B quando ReCaptcha V3 è configurato per il pagamento in vetrina. In precedenza, la convalida non riusciva per un motivo `recaptcha validation failed, please try again` messaggio di errore.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1825-->Gli ordini fornitore non possono più essere inoltrati da un utente associato alla società dopo che questa è stata bloccata. In precedenza, un utente associato alla società poteva effettuare ordini di acquisto quando la società era bloccata.

![Problema risolto](../assets/fix.svg)<!--ACP2E-1933-->Gli amministratori aziendali possono ora aggiungere utenti aziendali dalla vetrina. In precedenza, Commerce registrava un errore quando un utente amministratore tentava di aggiungere un nuovo utente: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2

*10 ottobre 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

La versione 1.4.2 di B2B include miglioramenti della qualità e correzioni di bug

![Problema risolto](../assets/fix.svg) <!--B2B-2897-->Se un venditore crea un&#39;offerta di acquisto che include uno SKU di prodotto non disponibile nel catalogo condiviso associato alla società acquirente, il sistema visualizza il messaggio di errore `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Il venditore non può salvare il preventivo finché non rimuove il prodotto non disponibile. In precedenza, il preventivo veniva salvato con lo SKU non disponibile incluso e il preventivo non veniva caricato nella vetrina.

## B2B v1.4.1

*7 agosto 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibile con Adobe Commerce 2.4.7-beta1.

La versione 1.4.1 di B2B include miglioramenti della qualità e correzioni di bug.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1825-->Gli ordini fornitore non possono più essere inoltrati da un utente associato alla società dopo che questa è stata bloccata. In precedenza, un utente associato alla società poteva effettuare ordini di acquisto quando la società era bloccata.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1943-->Lo stato del prodotto ordinato in inevaso viene ora visualizzato correttamente nella vetrina. In precedenza, i prodotti disponibili per la spedizione venivano erroneamente identificati come prodotti in inevaso.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1862-->Se il modulo di registrazione della società include un attributo del tipo di file del cliente, il file caricato durante il processo di registrazione viene ora incluso nelle informazioni sull’account per l’amministratore della società dopo la creazione della società. In precedenza, l’allegato era mancante.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1793-->Il selettore campioni per un prodotto configurabile ora viene visualizzato come previsto nella pagina di configurazione dell’articolo dell’elenco richieste di acquisto. In precedenza, il selettore campioni veniva visualizzato come campo a discesa nella pagina di configurazione dell’elemento dell’elenco richieste di acquisto.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1968-->Quando si utilizza [Query GraphQL società](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) per restituire i dettagli della società, i risultati vengono ora restituiti correttamente senza errori.

## B2B v1.4.0

*13 giugno 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatibile con Adobe Commerce 2.4.7-beta1

Questa versione include nuove funzionalità e miglioramenti per i preventivi negoziabili B2B e diverse correzioni di bug.

![Nuovo](../assets/new.svg) È stata aggiunta la compatibilità con Adobe Commerce 2.4.7-beta1.

![Nuovo](../assets/new.svg) **Offerte avviate dal venditore**- I venditori possono ora avviare un preventivo per un acquirente direttamente dalle griglie Preventivo e Cliente nell&#39;Admin. Questa funzionalità semplifica il processo di offerta e riduce la complessità per i clienti. Se un cliente non ha avviato un ordine, un venditore può creare rapidamente un preventivo per conto del cliente e avviare il processo di negoziazione. In precedenza, i preventivi potevano essere creati solo dalla vetrina dall&#39;acquirente o da un venditore che aveva effettuato l&#39;accesso come cliente.

![Nuovo](../assets/new.svg) **Sconti e negoziazione articoli linea**—<!--B2B-2440--> All&#39;interno di un preventivo, acquirenti e venditori B2B possono ora negoziare a livello di voce, applicando sconti e scambiando note fino a quando non viene raggiunto un accordo. La creazione e gli aggiornamenti delle note sono inclusi nella cronologia dell’elemento riga e dell’offerta per tenere traccia della comunicazione. In precedenza, acquirenti e venditori potevano scambiarsi note e applicare sconti solo a livello di preventivo.

![Problema risolto](../assets/fix.svg) Adobe Commerce visualizza ora i dettagli corretti durante il pagamento quando l&#39;opzione Ordini di acquisto è abilitata e quando è stato selezionato un preventivo virtuale creato con l&#39;opzione di pagamento PayPal. In precedenza, i totali venivano visualizzati come zero in queste condizioni.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1504--> Gli errori di convalida non si verificano più quando si tenta di salvare un&#39;azienda con un limite di credito superiore a 999. In precedenza, per i limiti di credito della società superiori a 999, Adobe commerce inseriva un separatore con la virgola, causando un errore di convalida che impediva il salvataggio degli aggiornamenti.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1474-->  L&#39;indirizzo di spedizione selezionato rimane invariato quando si effettua un ordine con un preventivo negoziabile. In precedenza, quando si effettuava un ordine, l&#39;indirizzo di spedizione selezionato veniva modificato nell&#39;indirizzo di spedizione predefinito.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1429--> Nelle impostazioni di configurazione dello store per le funzionalità B2B, **[!UICONTROL Enable Shared Catalog direct products price assigning]** Il campo è ora disattivato automaticamente. Nella vetrina, è nascosto quando il **[!UICONTROL Enable Company]** impostazione o **[!UICONTROL Enable Shared Catalog]** è impostato su **[!UICONTROL No]**.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1683--> Durante la creazione di un account aziendale dalla vetrina, Commerce ora convalida l’indirizzo e-mail prima di elaborare la registrazione dell’azienda. Se l’indirizzo e-mail non è valido, l’operazione non riesce e non vengono elaborati aggiornamenti dell’account. In precedenza, veniva creato un account cliente anche se la richiesta di creare un account aziendale non riusciva a causa di un indirizzo e-mail non valido.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1664--> Gli SKU di prodotto che includono virgolette doppie nel catalogo condiviso e nella struttura dei prezzi non causano più errori nell’amministratore.

![Problema risolto](../assets/fix.svg) <!--ACP2E-1498--> È stata aggiornata la configurazione Vernice per l&#39;applicazione Commerce per impedire agli utenti guest di visualizzare i dati di altri gruppi di clienti.

### Problema noto

Se installi o aggiorni B2B 1.4.0 su [Adobe Commerce versione 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), si verifica il seguente errore:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

È possibile risolvere questo problema aggiungendo dipendenze manuali per il pacchetto di sicurezza B2B aggiungendo dipendenze manuali per il pacchetto di sicurezza B2B con un [tag di stabilità](https://getcomposer.org/doc/04-schema.md#package-links). Per istruzioni, vedere [Knowledge Base di Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14 marzo 2023*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](../assets/new.svg) È stata rilasciata la versione 1.3.5-p2 di B2B per supportare la compatibilità con Adobe Commerce 2.4.6-p2.

![Nuovo](../assets/new.svg) È stata rilasciata la versione 1.3.5-p1 di B2B per supportare la compatibilità con Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Dopo aver aggiornato Commerce dalla versione 2.4.6 alla [versione più recente](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), assicurati di eseguire l’aggiornamento alla versione della patch B2B 1.3.5 supportata. In alternativa, aggiorna l’estensione B2B dalla versione 1.3.5 alla versione 1.4.0 o successiva per ottenere le funzioni più recenti.

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.6.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce visualizza ora i dettagli corretti durante il pagamento quando l&#39;opzione Ordini di acquisto è abilitata e quando è stato selezionato un preventivo virtuale creato con l&#39;opzione di pagamento PayPal. In precedenza, i totali venivano visualizzati come zero in queste condizioni.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-609--> L’elenco dei gruppi di clienti per il **Consenti esplorazione categoria** l&#39;impostazione non contiene più gruppi di clienti correlati a cataloghi condivisi.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1244--> L&#39;attributo cliente Partita IVA ora funziona come previsto con i conti di amministrazione società sia in Admin che in vetrina. Per creare un conto aziendale non sono più necessari attributi IVA/imposta personalizzati. In precedenza, quando un esercente creava un account aziendale con un attributo personalizzato Imposta/IVA, Adobe Commerce generava un errore di convalida sia nella vetrina che nell’Amministratore.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1236--> La disattivazione della funzione di catalogo condiviso in un ambito specifico ora funziona correttamente. In precedenza, Adobe Commerce impostava un ambito non valido quando un commerciante salvava la configurazione di un catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1203--> Gli utenti amministratori possono ora salvare i valori degli attributi personalizzati del cliente per gli utenti aziendali. In precedenza, non era possibile salvare gli attributi personalizzati del cliente per gli utenti aziendali.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1221--> I problemi di prestazioni vengono risolti con la convalida delle autorizzazioni aziendali fornite tramite GraphQL quando molte autorizzazioni aziendali sono già assegnate.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce non genera più un errore nella pagina del carrello quando si utilizza l’ordine rapido per aggiungere un prodotto in una quantità che supera le scorte disponibili.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1090--> Le prestazioni di `SELECT` sono state migliorate le operazioni relative alle autorizzazioni aziendali.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-2456--> Le query per categorie ora restituiscono i prezzi dei prodotti in base alle impostazioni di configurazione del negozio quando non sono impostate in modo esplicito autorizzazioni per la categoria in questione.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-6829--> Il **[!UICONTROL Place Order]** Il pulsante ora funziona come previsto quando si completa un acquisto con una richiesta di preventivo approvata. Problemi relativi al preventivo negoziabile `negotiableQuoteCheckoutSessionPlugin` Il plug-in è stato risolto.

## B2B v1.3.4

*9 agosto 2022*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.5.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce non invia più notifiche e-mail ogni volta che un’azienda esistente viene aggiornata da una chiamata API. Le e-mail ora vengono inviate solo quando viene creata un’azienda.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce ora calcola correttamente un totale complessivo di un preventivo negoziabile quando **[!UICONTROL Enable Cross Border Trade]** impostazione di calcolo delle imposte abilitata.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-322-->I prodotti configurabili vengono ora spostati all’ultima posizione nell’elenco dei prodotti dopo l’aggiornamento delle scorte quando **[!UICONTROL Move out of stock to the bottom]** è attivata. Viene implementata una nuova query di database personalizzata per garantire che il criterio di ordinamento dell’indice Elasticsearch rispetti quello abilitato dall’amministratore. In precedenza, i prodotti configurabili e i relativi prodotti secondari non venivano spostati in fondo all’elenco quando questa impostazione era abilitata.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-308-->L’e-mail dell’ordine di acquisto ora rispetta l’impostazione di invio delle e-mail di ciascun sito web in una distribuzione multisito. Un assegno per il **[!UICONTROL Disable Email Communications]** viene aggiunta alla logica personalizzata per le code e-mail. In precedenza, Adobe Commerce non rispettava l’impostazione di invio dell’e-mail per il sito web secondario.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-302-->Il titolo del campo SKU della pagina Ordine rapido viene modificato per maggiore chiarezza.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce ora visualizza un messaggio di errore più informativo quando un acquirente inserisce una SKU non valida in **Inserisci SKU o nome prodotto** campo.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-1753-->Il **[!UICONTROL Account Created in]** ora il valore di un campo per l’amministratore della società viene mantenuto come previsto dopo il salvataggio della società.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-722 -->Il `customer` query non restituisce più risultati vuoti quando recupera gli elenchi di richieste di acquisto filtrati per `uid`.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-210 -->È stato aggiunto un plug-in prima del `collectQuoteTotals` effettua una chiamata per garantire che i crediti del negozio vengano applicati una sola volta.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-665 -->I clienti vengono ora reindirizzati alla pagina di accesso quando il loro account viene eliminato da un amministratore dell’amministratore. In precedenza, Adobe Commerce generava un errore. Il plug-in (`SessionPlugin`) il blocco di codice si trova ora all&#39;interno del `try…catch` blocco. In precedenza, questo codice non veniva racchiuso all’interno del blocco generico di gestione delle eccezioni.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-661 --> Nella pagina Ordine rapido in modalità mobile, premere **Invio** dopo aver inserito un nome di prodotto o uno SKU valido, porta l’acquirente al campo successivo, come previsto.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-607 -->Il nome della società è ora visibile come previsto nelle sezioni degli indirizzi di fatturazione e spedizione del flusso di lavoro di pagamento.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-375 -->Il credito del Negozio non è più disponibile quando **[!UICONTROL Zero Subtotal Checkout]** metodo di pagamento disabilitato. In precedenza, la casella di controllo Credito store non funzionava durante il posizionamento dell’ordine da parte dell’amministratore. L’applicazione non ha inserito l’ordine con il credito dello store e ha visualizzato questo errore: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 agosto 2022*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.4.

![Problema risolto](../assets/fix.svg) <!--- MC-41985--> Il tempo necessario per eseguire l’aggiornamento da Adobe Commerce 2.3.x a Adobe Commerce 2.4.x in implementazioni con più di 100.000 ruoli aziendali è stato notevolmente ridotto.

![Problema risolto](../assets/fix.svg) <!--- MC-42153--> Il POST `V1/order/:orderId/invoice` ora supporta la creazione di fatture parziali quando **[!UICONTROL Payment on Account]** metodo di pagamento abilitato. In precedenza, Adobe Commerce generava questo errore: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problema risolto](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro ora funziona come previsto con il preventivo B2B negoziabile quando il carrello del cliente contiene altri prodotti. Adobe Commerce ora elabora correttamente l’ordine e invia un’e-mail al cliente come previsto. In precedenza, Adobe Commerce generava un errore irreversibile e inviava al cliente un’e-mail di conferma con valori pari a zero.

![Problema risolto](../assets/fix.svg) <!--- MC-41819--> La paginazione ora viene visualizzata correttamente nella pagina dei risultati della ricerca nel catalogo dopo l’esclusione di alcuni prodotti nel catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42886--> Gli attributi personalizzati del cliente vengono ora salvati come previsto durante la creazione o il salvataggio di un utente aziendale nell’amministratore.

![Problema risolto](../assets/fix.svg) <!--- MC-42927--> Il **[!UICONTROL Submit]** Il pulsante Crea nuova società è ora disattivato dopo un clic per impedire l’invio di più moduli. In precedenza, era possibile inviare il modulo più volte facendo clic ripetutamente su questo pulsante, generando un errore.

![Problema risolto](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce non visualizza più il collegamento di riordino nella vetrina quando un acquirente accede a un negozio per il quale i riordini sono stati disabilitati.

![Problema risolto](../assets/fix.svg) <!--- MC-43115--> La ricerca rapida per SKU non fa più distinzione tra maiuscole e minuscole quando è abilitato il catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42203--> È ora possibile aggiornare un file per un attributo del cliente al momento della creazione di un’azienda. In precedenza, quando si tentava di creare un’azienda con un allegato di tipo `File`, Adobe Commerce non ha creato la società e ha registrato questo errore nel registro eccezioni: `Something went wrong while saving file`.

![Problema risolto](../assets/fix.svg) <!--- MC-42242--> È ora possibile creare una società con un account cliente con un attributo personalizzato con (`File`) o (`Image`). In precedenza, se l’account disponeva di una di queste opzioni personalizzabili, il caricatore della pagina di modifica dell’azienda non veniva risolto, impedendo la modifica dei dettagli dell’azienda.

![Problema risolto](../assets/fix.svg) <!--- MC-42268--> Il `products` query ora restituisce un valore preciso `total_count` quando è abilitato il catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42203-->  È ora possibile aggiornare un file per un attributo del cliente al momento della creazione di un’azienda. In precedenza, quando si tentava di creare un’azienda con un allegato di tipo `File`, Adobe Commerce non ha creato la società e ha registrato questo errore nel registro eccezioni: `Something went wrong while saving file`.

![Problema risolto](../assets/fix.svg) <!--- MC-43178--> Il _Configurazione società_ e _Crea società_ Le pagine ora funzionano come previsto dopo aver disabilitato un metodo di spedizione online. È stata aggiunta una verifica per impedire il tentativo di elaborazione dei moduli di spedizione disabilitati. In precedenza, Adobe Commerce visualizzava questo errore: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Problema risolto](../assets/fix.svg) <!--- MC-42214--> Il _Categoria_ Durante la generazione delle autorizzazioni durante l’indicizzazione parziale, ora nella pagina vengono visualizzati dati di prodotto coerenti. A questo processo è stato aggiunto un nuovo indicizzatore parziale per le autorizzazioni della directory. In precedenza, i dati visualizzati durante l’esecuzione dell’indicizzatore non erano corretti.

![Problema risolto](../assets/fix.svg) <!--- MC-42567--> Il `categoryList` query ora restituisce il numero corretto di prodotti quando si utilizzano le autorizzazioni del catalogo e i prodotti vengono assegnati a un catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-42528--> Il `categoryList` query ora rispetta le autorizzazioni per le categorie e restituisce solo le categorie consentite. In precedenza, restituiva tutte le categorie assegnate e non assegnate.

![Problema risolto](../assets/fix.svg) <!--- MC-42399--> Il `rest/V1/company/{id}` request now restituisce `is_purchase_order_enabled` valori attributo come previsto.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-128--> Gli attributi cliente personalizzati vengono ora visualizzati come previsto nella _Amministratore società_ scheda.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-130--> Il blocco Elenco desideri nella pagina Account personale ora viene visualizzato come previsto per gli amministratori e gli utenti aziendali.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-133--> Gli errori di ordine rapido non vengono più visualizzati nel carrello. In precedenza, Adobe Commerce visualizzava questo errore nel carrello quando lo SKU non veniva trovato nel catalogo:  `The SKU was not found in the catalog`.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-194--> Le operazioni di salvataggio del catalogo condiviso sono state ottimizzate per velocizzare l’esecuzione. In precedenza, il salvataggio di un catalogo condiviso con molti gruppi di clienti poteva richiedere alcuni minuti.

![Problema risolto](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce ora elimina tutte le autorizzazioni delle sottocategorie dal `sharedcatalog_category_permissions` quando la categoria padre viene eliminata. In precedenza, venivano rimossi solo i dati della categoria principale.

## B2B v1.3.2

*29 agosto 2022*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.3.

![Problema risolto](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce ora invia correttamente e-mail di aggiornamento sui preventivi negoziabili scaduti. In precedenza, alla scadenza di un preventivo negoziabile, Adobe Commerce non inviava e-mail di aggiornamento.

![Problema risolto](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce ora invia correttamente e-mail di aggiornamento relative a quotazioni negoziabili in scadenza e scadute quando un `cron` processo mancante.

### Azienda

![Problema risolto](../assets/fix.svg) <!--- MC-41542--> Nel campo a discesa del paese della pagina Crea nuovo account società non sono più elencati valori di opzione vuoti. In precedenza, i primi due valori dell’opzione e il codice del paese `AN` erano vuoti.

![Problema risolto](../assets/fix.svg) <!--- MC-41260--> Facendo clic su **[!UICONTROL Return]** per un ordine creato da un utente della società ora reindirizza un utente amministrativo alla pagina Crea reso come previsto. In precedenza, l&#39;amministratore veniva reindirizzato alla pagina Cronologia ordini.

![Problema risolto](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce non ha più esito negativo con un errore di memoria insufficiente durante l’esecuzione del comando `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` metodo durante `bin/magento setup:upgrade`. In precedenza, Adobe Commerce non utilizzava la dimensione batch per la raccolta durante l’inizializzazione delle autorizzazioni, ma caricava una raccolta di tutti i ruoli aziendali.

![Problema risolto](../assets/fix.svg) <!--- MC-40551--> Gli utenti aziendali possono ora modificare e aggiornare i valori degli attributi personalizzati del cliente. In precedenza, questi attributi non venivano associati correttamente al modulo utente di creazione e modifica. Un utente della società può immettere valori di attributo diversi, ma Adobe Commerce non li ha salvati correttamente.

![Problema risolto](../assets/fix.svg) <!--- MC-32653--> La struttura delle risorse per le autorizzazioni del ruolo aziendale ora può essere tradotta come previsto. In precedenza, la struttura delle autorizzazioni non veniva tradotta anche se erano presenti file di traduzione validi.

![Problema risolto](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce ora salva i valori degli attributi cliente personalizzati per gli utenti B2B come previsto. In precedenza, la creazione di un account aziendale contenente attributi cliente personalizzati causava un errore di modello e Adobe Commerce non caricava correttamente il modulo. Aggiunta di un argomento al layout di `company_create_account` ha risolto questo problema.

![Problema risolto](../assets/fix.svg) <!--- MC-41721--> I filtri utente aziendali, ad esempio Mostra tutti gli utenti, Mostra utenti attivi e Mostra utenti inattivi, ora funzionano come previsto. In precedenza, il filtraggio delle azioni sulla pagina utente della società causava un errore JavaScript.

### Credito società

![Problema risolto](../assets/fix.svg) <!--- MC-41551--> Gli amministratori con account limitati che includono solo privilegi a livello di sito Web possono ora creare una società che utilizza una valuta diversa rispetto al sito Web.

![Problema risolto](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce ora invia e-mail aziendali dalla giusta `from` indirizzo e-mail e ambito. In precedenza, Adobe Commerce non considerava l’ambito del sito web durante l’invio dell’assegnazione del credito aziendale o l’aggiornamento dell’e-mail.

### Ordine rapido

![Problema risolto](../assets/fix.svg) <!--- MC-42104--> La creazione di un ordine utilizzando Ordine rapido da un file CSV ora funziona come previsto con SKU inesistenti.

![Problema risolto](../assets/fix.svg) <!--- MC-40268--> L’utilizzo di Ordine rapido per eseguire ricerche su più SKU ora funziona come previsto. In precedenza, i risultati includevano voci duplicate.

![Problema risolto](../assets/fix.svg) <!--- MC-40261--> La visualizzazione dell&#39;elenco dei prodotti aggiunti ora considera gli SKU immessi in minuscolo e in maiuscolo allo stesso modo quando si utilizzano gli SKU per selezionare più prodotti durante l&#39;ordine rapido.

![Problema risolto](../assets/fix.svg) <!--- MC-40225--> L’utilizzo dell’ordine rapido ora aggiunge i prodotti nella quantità specificata dall’acquirente. In precedenza, Adobe Commerce aggiungeva un solo prodotto anche quando le quantità specificate dall’acquirente superavano il valore di uno.

![Problema risolto](../assets/fix.svg) <!--- MC-41283--> La funzione di completamento automatico ordine rapido ora funziona con SKU parziali.

![Problema risolto](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce ora mostra i prodotti configurati come **Non visibile singolarmente** nell&#39;elenco di suggerimenti automatici e nei risultati della ricerca della pagina Ordine rapido.

![Problema risolto](../assets/fix.svg) <!--- MC-42402--> Gli acquirenti possono ora utilizzare il modulo Ordine rapido per aggiungere più prodotti in base agli SKU che includono caratteri maiuscoli. In precedenza, veniva aggiunto solo il primo prodotto.

### Offerta negoziabile

![Problema risolto](../assets/fix.svg) <!--- MC-41232--> Gli acquirenti vengono ora reindirizzati alla pagina delle offerte negoziabili dopo aver incollato il collegamento a un&#39;offerta negoziabile nel campo URL e aver effettuato correttamente l&#39;accesso. In precedenza, gli acquirenti venivano reindirizzati alla pagina Il mio account.

![Problema risolto](../assets/fix.svg) <!--- MC-39317--> Il riordinamento ora funziona come previsto per gli ordini che contengono un prodotto con un&#39;opzione di personalizzazione data per un account cliente creato durante il pagamento. In precedenza, Adobe Commerce non elaborava il riordine e visualizzava questo errore: `The product has required options. Enter the options and try again`.

![Problema risolto](../assets/fix.svg) <!--- MC-39063--> L&#39;indirizzo di spedizione per un preventivo negoziabile non è più modificabile durante il pagamento quando il modulo Ordine di acquisto è disabilitato. Questo comportamento è risultato da una correzione precedente in cui `isQuoteAddressLocked` è stato rimosso dal modulo di rendering estrazione preventivo negoziabile.

![Problema risolto](../assets/fix.svg) <!--- MC-38967--> Gli esercenti possono ora aggiungere prodotti a un preventivo negoziabile dell’amministratore.

### Ordini di acquisto

![Problema risolto](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce visualizza ora un messaggio di errore informativo come previsto quando inserisci un ordine di acquisto utilizzando PayPal Express Checkout quando **[!UICONTROL Name Prefix]** attributo impostato su `required`. In precedenza, Adobe Commerce non effettuava l’ordine né visualizzava un messaggio di errore.

![Problema risolto](../assets/fix.svg) <!--- MC-39620--> Il componente dell’interfaccia utente per l’indirizzo di fatturazione nel modulo Ordine di acquisto ora utilizza correttamente l’indirizzo del preventivo quando Google Tag Manager è abilitato. In precedenza, si verificava un errore JavaScript nella pagina di pagamento.

### Elenchi richieste

![Problema risolto](../assets/fix.svg) <!--- MC-40426--> I commercianti possono ora utilizzare il POST `rest/all/V1/requisition_lists` endpoint per creare un elenco di richieste per un cliente. In precedenza, Adobe Commerce generava questo errore 400 quando si tentava di creare un elenco di richieste di acquisto: `Could not save Requisition List`.

![Problema risolto](../assets/fix.svg) <!--- MC-41123--> Il **[!UICONTROL Add to Requisition List]** ora viene visualizzato il pulsante per i prodotti in magazzino di un carrello quando il carrello contiene anche prodotti esauriti. In precedenza, se un carrello conteneva due prodotti, uno dei quali era esaurito, il _[!UICONTROL Add to Requisition List]_non è stato visualizzato per nessuno dei prodotti.

![Problema risolto](../assets/fix.svg) <!--- MC-40877--> È ora possibile utilizzare l’API REST per aggiungere un prodotto a un elenco di richieste di acquisto.

![Problema risolto](../assets/fix.svg) <!--- MC-40155--> Elenco richieste **[!UICONTROL Latest Activity Date]** i valori ora rispettano il formato locale.

![Problema risolto](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce non genera più un errore irreversibile quando si modifica un prodotto bundle da un elenco di richieste di acquisto.

![Problema risolto](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce ora visualizza il prezzo di prodotto corretto quando aggiungi un prodotto con un’opzione personalizzabile `(File)` a un elenco di desideri da un elenco di richieste. Anche il collegamento al file caricato è visibile come previsto. In precedenza, Adobe Commerce mostrava prezzi del prodotto errati e non mostrava il collegamento al file.

![Problema risolto](../assets/fix.svg) <!--- MC-36383--> Prodotti con opzione personalizzabile `(File)` ora può essere aggiunto a un carrello da un elenco di richieste di acquisto.

### Catalogo condiviso

![Problema risolto](../assets/fix.svg) <!--- MC-40497--> Ora un amministratore con un ruolo limitato a un sito web specifico può creare, visualizzare e modificare un catalogo condiviso. In precedenza, Adobe Commerce generava un errore irreversibile quando un amministratore con un ruolo limitato tentava di creare un catalogo condiviso.

![Problema risolto](../assets/fix.svg) <!--- MC-41337--> I risultati della navigazione a livelli ora includono un conteggio accurato dei prodotti con attributi filtrati e gli acquirenti possono applicare più filtri. In precedenza era possibile applicare un solo filtro e Adobe Commerce mostrava un conteggio di prodotti non accurato nella navigazione a più livelli.

![Problema risolto](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce ora visualizza correttamente i conteggi dei prodotti nei filtri di navigazione a più livelli nei risultati della ricerca. In precedenza, un plug-in per la pagina Risultati ricerca non utilizzava Elasticsearch, ma inviava una nuova query al database.

![Problema risolto](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce non elimina più i prezzi livello quando un commerciante elimina tutti i prodotti da un catalogo condiviso predefinito.

![Problema risolto](../assets/fix.svg) <!--- MC-39802--> I filtri vengono ora filtrati in base alla categoria corrente e visualizzati correttamente in tutte le pagine quando sono abilitati i cataloghi condivisi. In precedenza, i filtri venivano calcolati in modo errato solo per la pagina corrente e non venivano filtrati per la categoria corrente.

![Problema risolto](../assets/fix.svg) <!--- MC-39522--> GraphQL `products` query non restituisce più l&#39;intervallo di prezzo e la categoria di un prodotto per i prodotti non assegnati a un catalogo condiviso quando quest&#39;ultimo è abilitato. In precedenza, la query restituiva le aggregazioni del prodotto, anche se il prodotto stesso non veniva restituito in `items` array.

## B2B v1.3.1

*9 febbraio 2021*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.2.

![Nuovo](../assets/new.svg) I metodi di pagamento online sono ora supportati per gli ordini di acquisto.

![Problema risolto](../assets/fix.svg) L’aggiunta di un prodotto configurabile al carrello direttamente da un elenco di richieste di acquisto quando il prodotto è stato utilizzato in un ordine precedente non restituisce più un errore di sistema.

![Problema risolto](../assets/fix.svg) Adobe Commerce ora visualizza correttamente la scheda Richiedi la mia approvazione per gli ordini di acquisto quando viene distribuita una configurazione di database divisa.

![Problema risolto](../assets/fix.svg) Adobe Commerce ora visualizza i dettagli sui prodotti in bundle e sulle gift card quando vengono visualizzati gli ordini di acquisto.

![Problema risolto](../assets/fix.svg) Gli acquirenti vengono ora reindirizzati come previsto dopo aver effettuato l’accesso al loro account durante la navigazione in un negozio in cui **[!UICONTROL Website Restriction]** è abilitato e **[!UICONTROL Restriction Mode]** è impostato su `Private Sales: Login Only`. In precedenza, gli acquirenti venivano reindirizzati alla home page del negozio. <!--- MC-38934-->

![Problema risolto](../assets/fix.svg) La cronologia degli ordini ora viene caricata come previsto nella pagina del dashboard account dell’amministratore della società nelle distribuzioni con una gerarchia aziendale B2B che contiene molti clienti (maggiore di 13000). In precedenza, la cronologia degli ordini veniva caricata lentamente o non veniva caricata affatto e Adobe Commerce mostrava un errore 503. <!--- MC-38830-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più più più messaggi di avviso identici quando si aggiunge un prodotto non configurato con opzioni personalizzabili a un elenco richieste di acquisto da una pagina Categoria. <!--- MC-38342-->

![Problema risolto](../assets/fix.svg) I prodotti nuovi e duplicati sono ora visibili come previsto nella pagina della categoria quando sono abilitati i cataloghi condivisi B2B. <!--- MC-38307-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora mantiene il corretto `store_id` associato a un amministratore della società quando il gruppo di clienti di una società viene aggiornato. Precedentemente, il `store_id` è stato modificato nell’archivio predefinito quando il gruppo è stato aggiornato. <!--- MC-38196-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora salva un prodotto raggruppato in un elenco di richieste di acquisto come elenco di prodotti semplici nello stesso modo in cui aggiunge un prodotto raggruppato a un carrello. In precedenza, a causa del modo in cui Adobe Commerce salvava i prodotti raggruppati, il collegamento per un prodotto raggruppato dall’elenco delle richieste di acquisto veniva sempre reindirizzato ai prodotti semplici e non al prodotto raggruppato. <!--- MC-38049-->

![Problema risolto](../assets/fix.svg) Ora puoi filtrare gli ordini per **[!UICONTROL Company Name]** durante l’esportazione delle informazioni dell’ordine in formato CSV. In precedenza, Adobe Commerce registrava un errore in `var/export/{file-id}`. <!--- MC-37785-->

![Problema risolto](../assets/fix.svg) Quando si seleziona la scheda Crea nuovo elenco richieste nella vetrina, Adobe Commerce ora visualizza la finestra a comparsa Crea elenco richieste come previsto. <!--- MC-37915-->

![Problema risolto](../assets/fix.svg) Gli elenchi delle richieste di acquisto ora includono tutti i prodotti raggruppati e le quantità che sono state aggiunte all’elenco. In precedenza, quando un commerciante passava a un elenco di richieste di acquisto dopo avervi aggiunto prodotti da una pagina dei dettagli del prodotto, Adobe Commerce visualizzava questo errore: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problema risolto](../assets/fix.svg) Quando crei una società in una distribuzione multisito, ora al sito web pertinente viene associata la visualizzazione corretta dello store. In precedenza, non era possibile creare una società e Adobe Commerce visualizzava questo errore: `The store view is not in the associated website`. <!--- MC-37488-->

![Problema risolto](../assets/fix.svg) Ordinando i prodotti in base allo SKU mediante l&#39;opzione Ordinamento rapido non si otterranno più quantità di prodotti duplicate nel file CSV. <!--- MC-37427-->

![Problema risolto](../assets/fix.svg) Il **[!UICONTROL Add to Cart]** non è più bloccato quando il _[!UICONTROL Enter Multiple SKUs]_nella pagina Ordine rapido contiene un valore vuoto. Al contrario, Adobe Commerce ora visualizza un messaggio che richiede di immettere SKU validi. <!--- MC-37387-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora visualizza questo messaggio nella pagina del prodotto quando si invia una revisione del prodotto da un elenco di richieste di acquisto: `You submitted your review for moderation`. La revisione viene visualizzata anche nella pagina Revisioni in sospeso (Amministratore **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). In precedenza, anche se Adobe Commerce aggiungeva la revisione all’elenco delle revisioni in sospeso, generava un errore 404 nella pagina del prodotto. <!--- MC-37119-->

![Problema risolto](../assets/fix.svg) L&#39;esecuzione del `sharedCatalogUpdateCategoryPermissions` è stato migliorato. Dopo aver creato un catalogo condiviso, l’indicizzatore delle autorizzazioni del catalogo ora utilizza solo l’ID del gruppo di clienti del catalogo condiviso e non tutti i gruppi di clienti. <!--- MC-36770-->

![Problema risolto](../assets/fix.svg) I campi attributo dell’indirizzo del cliente personalizzati associati all’indirizzo non predefinito di un acquirente vengono ora salvati come previsto nel flusso di lavoro di pagamento della vetrina. <!--- MC-36630-->

![Problema risolto](../assets/fix.svg) Ora è possibile effettuare gli ordini per gli acquirenti tramite l’API REST di amministrazione (`rest/V1/carts/{<CART_ID>/items`) come previsto. Adobe Commerce ora controlla se il prodotto è stato assegnato a un catalogo pubblico prima della convalida delle autorizzazioni del catalogo condiviso in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. In precedenza, Adobe Commerce non aggiungeva il prodotto al carrello dell’acquirente e generava questo errore: `No such shared catalog entity`. <!--- MC-36535-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora invia e-mail di registrazione utente della nuova azienda dall’indirizzo del negozio Adobe Commerce. In precedenza, questo messaggio e-mail veniva inviato dall’indirizzo dell’amministratore della società. <!--- MC-36480-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora controlla gli attributi personalizzati per verificare la duplicazione dei nomi di attributi riservati dell’azienda prima di consentire a un commerciante di salvare un nuovo attributo. <!--- MC-36282-->

![Problema risolto](../assets/fix.svg) Il `credit_history` query restituisce ora la cronologia dei crediti della società specificata sia per l&#39;importo allocato originariamente che per l&#39;importo acquistato. In precedenza, questa query restituiva un errore.

![Problema risolto](../assets/fix.svg) Il **[!UICONTROL Company]** e  **[!UICONTROL Job Title]** I campi della pagina Modifica informazioni account non sono più modificabili.

### Problemi noti

- Gli acquirenti B2B possono utilizzare metodi di pagamento online per aggirare il flusso abituale degli ordini di acquisto. Questo scenario può verificarsi se l&#39;acquirente può ridurre l&#39;intero totale di pagamento a 0, ad esempio tramite un codice promozionale o una gift card, e quindi rimuovere il codice o la gift card. Anche in queste condizioni, Adobe Commerce continua a effettuare l’ordine per l’importo corretto in base ai prezzi degli articoli nel catalogo assegnato. **_Soluzione alternativa_**: disabilita le carte regalo e i codici coupon quando i metodi di pagamento online sono abilitati per l’approvazione dell’ordine fornitore. <!--- B2B-1603-->

- Gli acquirenti vengono reindirizzati al carrello quando tentano di effettuare un ordine da un ordine di acquisto utilizzando PayPal Express Checkout quando **[!UICONTROL In-Context Mode]** è disabilitato. <!--- B2B-1604-->

- Adobe Commerce talvolta visualizza un errore 404 quando un acquirente crea un ordine di acquisto e poi passa alla pagina di pagamento. Questo errore si verifica quando un acquirente ha creato in precedenza un ordine di acquisto diverso con un metodo di pagamento online prima di passare alla pagina di pagamento senza completare l&#39;acquisto precedente. L&#39;acquirente può comunque effettuare l&#39;ordine di acquisto. **_Lavora in giro_**: nessuna. <!--- B2B-1605-->

- Gli sconti per un metodo di pagamento specifico persistono durante il pagamento di un ordine di acquisto anche quando l&#39;acquirente modifica il metodo di pagamento durante il pagamento finale. Di conseguenza, i clienti possono ricevere uno sconto a cui non hanno diritto. Questo problema si verifica perché una regola del carrello per il metodo di pagamento originale viene ancora applicata nonostante la modifica del metodo di pagamento. **_Lavora in giro_**: nessuna. Consulta la [Adobe Commerce 2.4.2 Problema noto B2B: rimane lo sconto per gli ordini di acquisto online dopo la modifica del metodo di pagamento](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Knowledge Base_ articolo. <!-- B2B-1012 -->

- Il `deleteRequisitionListOutput` query restituisce i dettagli dell&#39;elenco di richieste di acquisto eliminato anziché i restanti elenchi. <!--- MC-39894-->

## B2B v1.3.0

*15 ottobre 2020*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

Questa versione include miglioramenti alle approvazioni degli ordini, ai metodi di spedizione, al carrello acquisti e alla registrazione delle azioni dell’amministratore.

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.1.

![Nuovo](../assets/new.svg) Le approvazioni degli ordini B2B sono state migliorate per migliorarne l’usabilità e consentire azioni in blocco sugli ordini di acquisto.

![Nuovo](../assets/new.svg) I commercianti B2B possono ora controllare i metodi di spedizione offerti a ciascuna Azienda.<!--- BUNDLE-160 161 162 -->

![Nuovo](../assets/new.svg) I commercianti possono ora consentire agli utenti di cancellare il contenuto del carrello in un’unica azione e possono configurare questa funzionalità in modo indipendente su ogni sito web <!--- BUNDLE-108 -->

![Nuovo](../assets/new.svg) Gli acquirenti B2B possono ora aggiungere singoli articoli o l&#39;intero contenuto del carrello direttamente a un elenco di richieste di acquisto. <!--- BUNDLE-145 144-->

![Nuovo](../assets/new.svg) Gli esercenti B2B possono creare ordini dall’Amministratore per conto dei clienti utilizzando Payment on Account come metodo di pagamento. <!--- BUNDLE-166 178-->

![Nuovo](../assets/new.svg) Gli esercenti possono ora visualizzare direttamente tutti i preventivi associati a un utente dalla pagina dei dettagli del cliente. <!--- BUNDLE-139 -->

![Nuovo](../assets/new.svg) Gli esercenti possono ora filtrare la griglia Clienti online in base alla società. <!--- BUNDLE-137 -->

![Nuovo](../assets/new.svg) Gli amministratori ora possono filtrare i clienti nell’amministratore in base al rappresentante commerciale. <!--- BUNDLE-110 -->

![Nuovo](../assets/new.svg) Per ridurre la creazione di account fraudolenti o spam, gli esercenti possono ora abilitare Google reCAPTCHA nel modulo di richiesta della nuova azienda sulla vetrina. <!--- BUNDLE-154 -->

![Nuovo](../assets/new.svg) Le azioni di amministrazione eseguite nei moduli aziendali vengono ora registrate nel registro delle azioni di amministrazione. Le azioni vengono registrate da tutti i moduli aziendali pertinenti: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più il **[!UICONTROL Delete customer]** pulsante sulla **Clienti** quando l’amministratore connesso non dispone dei diritti per eliminare i clienti nelle implementazioni in cui è installato B2B. <!--- MC-35655-->

![Problema risolto](../assets/fix.svg) Il gruppo di clienti non viene più modificato automaticamente per un cliente assegnato a un&#39;azienda quando si modifica il cliente nella griglia Cliente. <!--- MC-35254-->

![Problema risolto](../assets/fix.svg) Quando un commerciante crea un catalogo condiviso, le autorizzazioni vengono ora impostate automaticamente su `Allow` per **[!UICONTROL Display Product Prices]** e **[!UICONTROL Add to Cart]** funzioni nelle categorie quando al gruppo di clienti viene assegnato questo accesso nelle impostazioni delle autorizzazioni del catalogo. In precedenza, queste impostazioni venivano impostate automaticamente su `Deny` anche quando le autorizzazioni del catalogo sono state impostate su `Allow`.<!--- MC-34792-->

![Problema risolto](../assets/fix.svg) Le autorizzazioni della categoria di catalogo condiviso non vengono più sovrascritte quando un prodotto viene modificato dalla pagina di modifica del prodotto.<!--- MC-34777-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora invia una notifica e-mail che conferma che un cliente è autorizzato a superare il limite di credito designato quando un esercente abilita **[!UICONTROL Allow To Exceed Credit Limit]** impostazione. In precedenza, l’e-mail di notifica inviata da Adobe Commerce indicava che il cliente non disponeva dell’autorizzazione per superare il limite. <!--- MC-34584-->

![Problema risolto](../assets/fix.svg) Il contenitore HTML che racchiude il prezzo del prodotto negli elenchi delle richieste di acquisto ora viene riprodotto correttamente per i figli dei prodotti raggruppati. <!--- MC-36331-->

![Problema risolto](../assets/fix.svg) I commercianti possono ora designare la lingua in cui viene inviata l’e-mail dell’utente dell’azienda durante la creazione di un’azienda in implementazioni multilingue. In precedenza, il menu a discesa consentiva ai commercianti di selezionare la vista e la lingua appropriate per il negozio.  <!--- MC-35777-->

![Problema risolto](../assets/fix.svg) I campi degli attributi dell’indirizzo del cliente personalizzati ora vengono visualizzati come previsto nel flusso di lavoro di pagamento della vetrina. <!--- MC-35607-->

![Problema risolto](../assets/fix.svg) La scheda di configurazione delle funzioni B2B ora si apre correttamente. <!--- MC-35458-->Gli ospiti possono ora utilizzare QuickOrder per aggiungere prodotti al carrello e rimuovere gli articoli. In precedenza, quando un acquirente utilizzava QuickOrder per aggiungere più prodotti al carrello e poi rimuoveva un prodotto, quest’ultimo non veniva rimosso. <!--- MC-35327-->

![Problema risolto](../assets/fix.svg) È ora possibile aggiornare un’azienda utilizzando REST API PUT `/V1/company/:companyId` richiesta senza specificare `region_id` quando lo stato è configurato come **non obbligatorio**. Precedentemente, anche se `region_id` non era obbligatorio, Adobe Commerce ha restituito un errore se non specificato. <!--- MC-35304-->

![Problema risolto](../assets/fix.svg) Quando crei o aggiorni una società B2B utilizzando l’API REST (`http://magento.local/rest/V1/company/2`, dove `2` rappresenta l’ID società), la risposta ora include le impostazioni per `applicable_payment_method` o `available_payment_methods` come previsto. <!--- MC-35248-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più una pagina 404 quando un commerciante utilizza **Invio** invece di fare clic sul pulsante **[!UICONTROL Save]** durante la creazione di un elenco di richieste di acquisto nella vetrina.<!--- MC-35094-->

![Problema risolto](../assets/fix.svg) Le autorizzazioni della categoria non cambiano più quando un nuovo prodotto viene assegnato a un catalogo condiviso pubblico. In precedenza, le autorizzazioni per le categorie venivano duplicate. <!--- MC-34386-->

![Problema risolto](../assets/fix.svg) Il PUT dell’endpoint REST API `rest/default/V1/company/{id}`, utilizzato per aggiornare l’e-mail aziendale, non distingue più tra maiuscole e minuscole. <!--- MC-34308-->

![Problema risolto](../assets/fix.svg) La disabilitazione dei moduli di ricompensa non influisce più sulle funzioni B2B negli account dei clienti. In precedenza, quando i moduli di ricompensa venivano disabilitati, le seguenti schede relative a B2B non venivano visualizzate: Profilo società, Utenti società e Ruoli e autorizzazioni.<!--- MC-34191-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora utilizza il nome del mittente corretto nelle notifiche e-mail quando vengono apportate modifiche agli account aziendali. In precedenza, Adobe Commerce utilizzava il nome del mittente del contatto generale definito nell’ambito predefinito per tutte le e-mail. <!--- MC-33917-->

![Problema risolto](../assets/fix.svg) È ora possibile implementare correttamente il multishipping per gli ordini che contengono prodotti sia fisici che virtuali. <!--- MC-33818-->

![Problema risolto](../assets/fix.svg) Gli esercenti possono ora creare utenti aziendali dalla _[!UICONTROL Company Users]_nelle pagine Il mio account e la struttura della società quando **[!UICONTROL Access Restriction]**è abilitato e **[!UICONTROL Restriction Mode]**è impostato su `Sales: Login Only`. In precedenza, Adobe Commerce generava questo errore quando un commerciante tentava di creare un utente: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non ripristina più il gruppo di clienti predefinito di un cliente quando quest’ultimo salva le informazioni sul proprio account. <!--- MC-33554-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non genera più un errore irreversibile quando un amministratore assegna un cliente con un carrello attivo a un gruppo di clienti. <!--- MC-33313-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora fornisce un’ `addToCart` Evento DataLayer per le pagine degli elenchi Ordine rapido e Richiesta di acquisto.  <!--- MC-33295-->

![Problema risolto](../assets/fix.svg) Le e-mail di notifica inviate ai rappresentanti commerciali assegnati a un&#39;azienda ora includono il logo aziendale assegnato. In precedenza, l’e-mail di notifica includeva il logo LUMA predefinito e non il logo aziendale caricato. <!--- MC-33232-->

![Problema risolto](../assets/fix.svg) Un elenco di richieste ora include tutti i prodotti raggruppati e le quantità aggiunte all&#39;elenco. In precedenza, quando un commerciante passava a un elenco di richieste di acquisto dopo avervi aggiunto prodotti da una pagina dei dettagli del prodotto, Adobe Commerce visualizzava questo errore: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problema risolto](../assets/fix.svg) Il `products` query ora restituisce un valore preciso `total_count` quando è abilitato il catalogo condiviso. <!--- MC-42268-->

![Problema risolto](../assets/fix.svg) Le pagine Configurazione società e Crea società ora funzionano come previsto dopo la disattivazione di un metodo di spedizione online. È stata aggiunta una verifica per impedire il tentativo di elaborazione dei moduli di spedizione disabilitati. In precedenza, Adobe Commerce visualizzava questo errore: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problema risolto](../assets/fix.svg) Il consumo di memoria per i test di integrazione è stato ridotto, il che migliora le prestazioni dei test e riduce il tempo necessario per il loro completamento. <!--- AC-266-->

## B2B v1.2.0

*28 luglio 2020*

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](../assets/new.svg) È stato aggiunto il supporto per Adobe Commerce 2.4.0.

![Nuovo](../assets/new.svg) Storefront Order Search, con i ringraziamenti per il contributo di Marek Mularczyk da [Divante](https://www.divante.com/) e i membri della community.

![Nuovo](../assets/new.svg) Gli ordini di acquisto vengono migliorati e riscritti. Ora sono inclusi per impostazione predefinita in Adobe Commerce.

![Nuovo](../assets/new.svg) Le regole di approvazione dell&#39;ordine di acquisto sono state implementate. Queste regole consentono agli utenti di controllare il flusso di lavoro Ordine di acquisto creando regole di acquisto per gli ordini.

![Nuovo](../assets/new.svg) L’accesso Accedi come cliente è ora incluso per impostazione predefinita in Adobe Commerce. Questa funzione consente ai dipendenti del sito di assistere i clienti effettuando l’accesso come cliente per vedere ciò che vedono.

![Problema risolto](../assets/fix.svg) Le aggregazioni di attributi ora funzionano correttamente per la navigazione a livelli con Elasticsearch

![Problema risolto](../assets/fix.svg) La ricerca di ordini per caratteri speciali ora funziona correttamente.

![Problema risolto](../assets/fix.svg) Facendo clic su **[!UICONTROL Clear All]** Button ora espande tutti i filtri, anziché comprimerli.

![Problema risolto](../assets/fix.svg) Il nome/SKU prodotto è ora incluso nel riepilogo del filtro di ricerca della cronologia ordini.

![Problema risolto](../assets/fix.svg) L&#39;indicatore di ordinamento viene ora visualizzato correttamente nella griglia Ordini di acquisto personali.

![Problema risolto](../assets/fix.svg) Ora è possibile fare clic una sola volta sui pulsanti Approva, Annulla, Rifiuta e Ordine di acquisto. In precedenza, era possibile fare clic più volte sul pulsante.

![Problema risolto](../assets/fix.svg) I pulsanti Approva, Rifiuta, Annulla e Convalida dell’ordine di acquisto ora vengono riprodotti correttamente sui dispositivi mobili.

![Problema risolto](../assets/fix.svg) In precedenza, quando si approvava un ordine di acquisto con uno sconto scaduto, l’ordine veniva collocato per l’intero importo e non veniva aggiornato il totale dell’ordine di acquisto. Ora il totale dell’ordine di acquisto viene aggiornato per mostrare il totale corretto.

![Problema risolto](../assets/fix.svg) Nella versione 2.3.4 è stato introdotto un problema a causa del quale gli attributi di estensione personalizzati non venivano copiati dall’indirizzo del cliente all’indirizzo del preventivo. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) Se è installato B2B, viene visualizzato un errore SQL durante l’assegnazione di categorie a cataloghi condivisi. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) A causa di un valore di tipo di variabile errato, gli amministratori non hanno potuto aggiungere prodotti configurabili a un ordine. I menu a discesa delle opzioni non si popolano. Questa funzione ora funziona correttamente.

![Problema risolto](../assets/fix.svg) In precedenza, quando si modificavano le autorizzazioni per le categorie per il gruppo Non connesso, si verificava un errore durante il salvataggio delle modifiche. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) È stata aggiunta una correzione per consentire agli amministratori dei negozi di aggiungere prodotti a un ordine che non si trova nel catalogo condiviso. In precedenza, veniva visualizzato un messaggio di errore quando si aggiungeva un elemento non presente nel catalogo.

![Problema risolto](../assets/fix.svg) In precedenza, dopo l’esecuzione del comando `php bin/magento indexer:set-dimensions-mode catalog_product_price website` se si tenta di creare un catalogo condiviso, si verifica un errore. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) Quando si aggiunge una società e si assegna l’amministratore della società a un sito Web non predefinito, viene inviato l’ID sito errato, causando un errore. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) In precedenza, dopo lo spostamento di un cliente in un altro gruppo di clienti, l’aggiunta di un prodotto a un ordine mediante _Ordine rapido_ fallirebbe con un errore. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) In precedenza, quando si tentava di estrarre utilizzando WebAPI con una virgoletta B2B, veniva inviato un valore errato all’API, causando un errore. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) In precedenza, quando si impostava una società su &quot;Attiva&quot; tramite l’API, si verificava un errore. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) A causa di un evento non necessario `form` , la pagina dell&#39;ordine viene aggiornata automaticamente quando si preme Invio dopo aver modificato le spese di spedizione proposte. Questo problema è stato risolto.

![Problema risolto](../assets/fix.svg) In precedenza, quando si impostava un limite di visualizzazione dei prodotti in una pagina di catalogo e tale limite era inferiore al numero di prodotti totali, si verificava un errore. Questa funzione ora funziona come previsto.

![Problema risolto](../assets/fix.svg) In precedenza, quando si modificava l’amministratore di una società, l’indirizzo dell’amministratore originale veniva copiato nel nuovo amministratore, assegnando loro due indirizzi. Ora viene aggiunto solo l’indirizzo corretto.

![Problema risolto](../assets/fix.svg) In precedenza, l’utilizzo dell’API per salvare un articolo dell’offerta quando Git era impostato su &quot;Consentito e notifica al cliente&quot; non riusciva. Questa chiamata API ora funziona come previsto.

![Problema risolto](../assets/fix.svg) L&#39;imposta sul prodotto fissa viene ora visualizzata nella pagina dei dettagli Preventivi.

![Problema risolto](../assets/fix.svg) In precedenza, se si faceva clic su un allegato nella scheda Commenti della pagina Citazioni, il file non veniva scaricato. Questo comportamento ora funziona come previsto.

### Problemi noti

- Adobe Commerce genera un’eccezione durante l’aggiornamento a B2B 1.2.0 in una distribuzione multisito. Quando `setup:upgrade` viene eseguito, questo errore si verifica in `PurchaseOrder` modulo: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Soluzione alternativa**: installa `B2B-716 Add NonTransactionableInterface` interfaccia con `InitPurchaseOrderSalesSequence` aggiornamento rapido delle patch di dati, ora disponibile dal **Il mio account** > **Download** sezione di `magento.com`.
- Se un codice di sconto scade prima dell&#39;approvazione di un ordine di acquisto (OA), l&#39;OA continua a visualizzare l&#39;importo scontato, ma dopo l&#39;approvazione dell&#39;OA l&#39;ordine viene collocato al totale non scontato. **Soluzione alternativa**: installa `B2B-709 Purchase Order Discount patch` hotfix per questo problema, ora disponibile nella sezione **Il mio account** > **Download** sezione di `magento.com`.
- Se gli articoli di un ordine di acquisto sono esauriti o la quantità è insufficiente quando l&#39;ordine di acquisto viene convertito in un ordine effettivo, si verifica un errore. Se gli ordini inevasi sono abilitati, l&#39;ordine viene elaborato normalmente.
