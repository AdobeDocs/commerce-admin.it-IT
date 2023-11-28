---
title: Note sulla versione per [!DNL Page Builder]
description: Consulta le note sulla versione per informazioni su tutte [!DNL Page Builder] versioni.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Note sulla versione di [!DNL Page Builder]

Queste note sulla versione descrivono le versioni di [!DNL Page Builder] e includono:

![Nuovo](../assets/new.svg) Nuove funzioni

![Problema risolto](../assets/fix.svg) Correzioni e miglioramenti

![Problema noto](../assets/bug.svg) Problemi noti

>[!IMPORTANT]
>
>A partire dalla versione 2.4.3 di, [!DNL Page Builder] è ora disponibile come estensione in bundle in Magento Open Source. Ora è lo strumento di modifica dei contenuti predefinito sia per Adobe Commerce che per Magento Open Source e può sostituire l’editor WYSIWG con qualsiasi modulo di terze parti.

## 1.7.2 per Commerce 2.4.5

![Nuovo](../assets/new.svg) **Nuova entità wrapper - [!DNL Columns] contenitore introdotto per i layout di colonna** - In precedenza, gli utenti potevano aggiungere colonne solo all’interno di un altro tipo di contenuto contenitore/wrapper, ad esempio [!DNL Tab] o [!DNL Row]. Ora, il [!DNL Column] dispone di un proprio wrapper e può essere aggiunto direttamente sullo stage. Inoltre, il [!DNL Columns] il contenitore dispone di un elemento impostazioni in cui gli utenti possono specificare la configurazione per questa entità wrapper.<!--- PB-500-->

![Nuovo](../assets/new.svg) **Nuove opzioni di menu per duplicare, nascondere ed eliminare i gruppi Colonne** - Con queste nuove opzioni, gli utenti possono duplicare, nascondere ed eliminare [!DNL Columns] gruppi, proprio come per i tipi di contenuto.<!--- PB-507-->

![Nuovo](../assets/new.svg) <!-- Issue 594 -->**Al gruppo di colonne è stato aggiunto il supporto per nuove colonne su più righe** - Con questa aggiunta, gli utenti possono manipolare più righe di colonne all&#39;interno di una [!DNL Columns] per rendere i layout di colonna molto più flessibili.<!--- PB-108-->

Consulta [Layout - Colonna](./column.md) per informazioni sull&#39;utilizzo del nuovo [!DNL Columns] gruppo.

## 1.7.1 per Commerce 2.4.4

![Problema risolto](../assets/fix.svg) Page Builder è ora compatibile con PHP 8.1.<!--- AC-1300-->

![Problema risolto](../assets/fix.svg) Gli esercenti possono ora aggiungere testo alternativo (`alt_text`) alle immagini (immagine, banner, diapositiva) per migliorare l&#39;accessibilità dei contenuti.<!--- PB-1193-->

![Problema risolto](../assets/fix.svg) Gli utenti amministratori con autorizzazioni limitate alla sola modifica del contenuto non visualizzano più un errore quando utilizzano Page Builder per aggiungere un widget di prodotto a una pagina CMS. Page Builder visualizza anche un conteggio accurato dei prodotti nella pagina delle impostazioni del widget. In precedenza, Page Builder richiedeva le autorizzazioni per il modulo Catalog durante il recupero del conteggio dei prodotti e visualizzava questo errore: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problema risolto](../assets/fix.svg) I problemi relativi alla visualizzazione del menu Formato Page Builder ora vengono risolti con l’aggiornamento della libreria TinyMCE 5. <!--- AC-446-->

![Problema risolto](../assets/fix.svg) È ora possibile utilizzare il mouse per modificare **Testo da visualizzare** nella finestra a comparsa Inserisci collegamento. <!--- AC-982-->

![Problema risolto](../assets/fix.svg) Page Builder visualizza ora tutte le opzioni come previsto nel menu delle opzioni Dimensione font. In precedenza, non venivano visualizzate tutte le opzioni. <!--- AC-1056-->

![Problema risolto](../assets/fix.svg) È stato aggiornato il `phpgt/dom` Dipendenza compositore per `magento/magento2-page-builder` alle versioni più recenti. <!--- magento/magento2-page-builder/pull/779-->

![Problema risolto](../assets/fix.svg) Page Builder non ridimensiona più le finestre di dialogo Inserisci collegamento e Inserisci immagine durante la visualizzazione del cursore in una piccola colonna. <!--- AC-973-->

![Problema risolto](../assets/fix.svg) Il menu Proprietà tabella di Page Builder viene ora visualizzato come previsto. <!--- AC-407-->

![Problema risolto](../assets/fix.svg) I punti cursore non vengono più visualizzati sul collegamento Inserisci o sul modale dell&#39;immagine quando il mouse non passa il puntatore sul cursore. <!--- AC-406-->

![Problema risolto](../assets/fix.svg) La dimensione del carattere utilizzata per visualizzare le opzioni del menu Tabella è stata ottimizzata. <!--- AC-396-->

![Problema risolto](../assets/fix.svg) Sono state corrette le anomalie con il posizionamento delle finestre di dialogo Inserisci/Modifica immagine e Inserisci/Modifica collegamento. <!--- AC-397-->

![Problema risolto](../assets/fix.svg) Page Builder non genera più un errore quando si fa clic su **Editor di testo** per un banner. <!--- AC-398-->

![Problema risolto](../assets/fix.svg) Durante l’aggiornamento, Page Builder non converte più tutti i blocchi dinamici in una sola lingua. <!--- MC-42265-->

## 1.6.0 per Adobe Commerce 2.4.2

![Nuovo](../assets/new.svg) <!-- Issue 558 -->**Nuovo [!DNL Page Builder] stile** - [!DNL Page Builder] sono stati apportati notevoli miglioramenti alla modalità di assegnazione degli stili dei contenuti. Le modifiche ora semplificano la creazione di semplici selettori CSS per ignorare gli stili del tipo di contenuto esistenti. Queste modifiche consentono di creare [!DNL Page Builder] con tempi di risposta avanzati per tutti i tipi di contenuto.

![Nuovo](../assets/new.svg) <!-- Issue 429 -->**Contenitore righe ora facoltativo** - È ora possibile creare contenuti in [!DNL Page Builder] senza richiedere un contenitore Riga. Oltre alla riga, è ora possibile trascinare e rilasciare direttamente sullo stage i seguenti tipi di contenuto: HTML, Blocco, Blocco dinamico, Colonne e Schede.

![Nuovo](../assets/new.svg) <!-- Issue 636 -->**Nuovo switcher del viewport reattivo** - È ora possibile visualizzare in anteprima [!DNL Page Builder] contenuti a diverse larghezze del dispositivo (punti di interruzione) utilizzando i nuovi pulsanti del selettore del riquadro di visualizzazione Amministratore sopra l’area di visualizzazione. Il selettore del riquadro di visualizzazione simula lo stile del contenuto quando viene visualizzato nella vetrina utilizzando dispositivi diversi.

![Nuovo](../assets/new.svg) <!-- Issue 637 -->**Nuovi campi modulo specifici per punti di interruzione** - È ora possibile impostare i valori dei campi del tipo di contenuto su punti di interruzione specifici del riquadro di visualizzazione. Gli indicatori delle icone accanto ai campi mostrano il riquadro di visualizzazione a cui viene applicato il valore del campo del tipo di contenuto.

![Nuovo](../assets/new.svg) <!-- Issue 559 -->**Voci di campo modulo predefinite rimosse** - Le impostazioni avanzate dei moduli per i margini, le pagine affiancate e le proprietà relative ai bordi (bordo, larghezza bordo e raggio bordo) sono ora impostate come `default`, in modo che i valori possano essere definiti dal CSS di un modulo.

![Nuovo](../assets/new.svg) <!-- Issue 635, 557,  -->**Spaziatura tra le fasi aggiunta** - Le righe e le colonne ora forniscono spazio aggiuntivo per i tipi di contenuto contenuti contenuti nell’area di visualizzazione, ma non nell’area di visualizzazione. La spaziatura tra gli intervalli consente di accedere più facilmente ai menu delle opzioni del mouse over sia per il tipo di contenuto contenitore che per quello contenuto.

![Problema risolto](../assets/fix.svg) <!-- MC-37348 -->**È stato corretto lo scorrimento automatico in recensioni** - Lo scorrimento automatico delle recensioni dei prodotti sullo storefront è ora fisso.

![Problema risolto](../assets/fix.svg) <!-- MC-36227 -->**Contenuto ritagliato fisso** - Non vengono più ritagliate lunghe descrizioni di prodotti e categorie.

![Problema risolto](../assets/fix.svg) <!-- MC-35402 -->**Contenuto categoria full-bleed fisso a larghezza intera** - Il contenuto della categoria può ora essere visualizzato in un layout a larghezza intera o a pagina intera.

![Problema risolto](../assets/fix.svg) <!-- MC-37989 -->**Miglioramenti di sicurezza**

## 1.5.1 per Adobe Commerce 2.4.1-p1

![Problema risolto](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Visualizzazione errori** - Risolto un problema in cui [!DNL Page Builder] mostrava un errore durante l’aggiunta delle sottocategorie Catalogo nell’Amministratore.

## 1.5.0 per Adobe Commerce 2.4.1

![Nuovo](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Editing coinvolgente a schermo intero** - Editing [!DNL Page Builder] il contenuto adesso è a schermo intero solo per tutte le aree controllate da [!DNL Page Builder]. Questa modifica include pagine CMS, pagine di prodotti e categorie, blocchi e blocchi dinamici. La modifica a schermo intero consente di mettere a fuoco i contenuti e offre una visualizzazione che corrisponde meglio all&#39;esperienza utente nella vetrina.

![Nuovo](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] anteprime dei contenuti **- Per impostazione predefinita, [!DNL Page Builder] ora fornisce anteprime di contenuto non solo per le pagine CMS, i blocchi e i blocchi dinamici, ma anche per le pagine di prodotti e categorie. È possibile configurare questa funzione in modo che sia attivata o disattivata per le pagine di prodotti e categorie utilizzando il nuovo [!DNL Page Builder] Impostazione Anteprima contenuto, accessibile nella configurazione dello store da Gestione contenuto > Strumenti di contenuto avanzati.

![Nuovo](../assets/new.svg) <!-- Issue 543 -->**Accesso migliorato alle descrizioni brevi dei prodotti** - Per impostazione predefinita, prima della descrizione più lunga viene ora visualizzata una breve descrizione del prodotto. Questa modifica determina una corrispondenza con l’ordine in cui vengono visualizzate nella vetrina e impedisce la necessità di scorrere il contenuto della descrizione più lunga per accedere alla descrizione breve.

![Nuovo](../assets/new.svg) <!-- Issue 419 -->**Impedire collegamenti nidificati nei banner e nelle diapositive** - L&#39;aggiunta di collegamenti sia al contenuto che agli elementi esterni dei banner e delle diapositive ha creato collegamenti nidificati che non venivano visualizzati o si comportavano correttamente nella vetrina. Per risolvere il problema, non è più possibile aggiungere collegamenti a *entrambi* nell&#39;area Testo messaggio e nell&#39;attributo Collegamento per i banner e le diapositive.

![Problema risolto](../assets/fix.svg) <!-- Issue 421 --> È stato risolto un problema a causa del quale l’impostazione di un raggio del bordo vuoto su un elemento Scheda causava errori e interrompeva il contenuto dell’elemento Scheda.

![Problema risolto](../assets/fix.svg) <!-- Issue 422 --> È stato risolto un problema a causa del quale l’aggiunta di determinate combinazioni di condizioni al filtro Condizione prodotti causava errori che impedivano il salvataggio del modulo Prodotti.

![Problema risolto](../assets/fix.svg) <!-- Issue 425 -->È stato risolto un problema che impediva il corretto funzionamento del tipo di contenuto Slider quando l’impostazione Ciclo infinito era disabilitata.

![Problema risolto](../assets/fix.svg) <!-- Issue 426 -->È stato corretto il prezzo minimo pubblicizzato in modo che ora funzioni in [!DNL Page Builder].

![Problema risolto](../assets/fix.svg) <!-- Issue 436 -->È stato risolto il problema in Safari e IE 11 che impediva il trascinamento e il rilascio di un’immagine nell’area di caricamento in Banner e Diapositive.

![Problema risolto](../assets/fix.svg) <!-- Issue 525 -->È stato risolto il problema a causa del quale il tipo di contenuto Slider non rispondeva in Firefox.

![Problema risolto](../assets/fix.svg) <!-- Issue 567 -->È stato risolto il problema che causava la creazione di selettori non corretti nel DOM per i diversi aspetti della configurazione del widget.

![Problema risolto](../assets/fix.svg) <!-- Issue 609 -->È stato risolto il problema che impediva l’accesso al modulo e ad altre opzioni nella barra degli strumenti Intestazione, nascondendo il menu di opzioni del tipo di contenuto.

![Problema risolto](../assets/fix.svg) <!-- Issue 612, 613 -->Sono stati risolti dei problemi a causa dei quali i cursori e le righe multiple che utilizzano sfondi parallasse non venivano riprodotti correttamente dopo aver attivato più volte la modalità a schermo intero.

![Problema risolto](../assets/fix.svg) <!--MC-35220-->È stato risolto il problema che impediva il tentativo di copiare il contenuto da un tipo di contenuto Titolo a un tipo di contenuto Testo [!DNL Page Builder] dal salvataggio.

![Problema risolto](../assets/fix.svg) <!-- MC-34620 -->È stato corretto il tipo di contenuto Testo per gestire e salvare correttamente i caratteri non latini 1.

![Problema risolto](../assets/fix.svg) <!-- MC-34679 -->Fisso [!DNL Page Builder] Stili CSS che hanno causato il rendering errato da parte di Safari 13.1 del menu del sito del tema Luma per piccole porte di visualizzazione e schermi mobili.

![Problema risolto](../assets/fix.svg) <!-- MC-34848 -->È stato corretto il tipo di contenuto HTML per visualizzare correttamente i widget incorporati come &quot;Ordina per SKU&quot; sullo storefront.

## 1.4.1 per Adobe Commerce 2.4.0-p1

![Nuovo](../assets/new.svg) <!-- PB-590 --> Aggiornato a TinyMCE 4. È stato rimosso TinyMCE 3 per migliorare la sicurezza.

## 1.4.0 per Adobe Commerce 2.4.0

![Nuovo](../assets/new.svg) <!-- PB-494 -->È stato aggiunto il supporto per PHP 7.4.

![Problema risolto](../assets/fix.svg) <!-- MC-31247 -->È stato risolto un problema a causa del quale il tipo di contenuto Prodotti non mostrava prodotti configurabili quando la condizione era impostata su prezzo.

![Problema risolto](../assets/fix.svg) <!-- PB-179 -->È stata corretta la configurazione di allineamento dei prodotti in modo da posizionare solo il contenitore di prodotti stesso, non il contenuto del contenitore di prodotti, come il nome del prodotto, il prezzo, i pulsanti, le immagini e altri elementi.

![Problema risolto](../assets/fix.svg) <!-- MC-33556 -->Miglioramenti delle prestazioni.

![Problema risolto](../assets/fix.svg) Miglioramenti di sicurezza.

## 1.3.3-p1 per Adobe Commerce 2.3.6-p1

![Problema risolto](../assets/fix.svg) Miglioramenti di sicurezza.

## 1.3.3 per Adobe Commerce 2.3.6

![Problema risolto](../assets/fix.svg) <!-- MC-32766 -->È stato corretto il tipo di contenuto Testo per salvare correttamente le direttive delle variabili aggiunte agli attributi html.

![Problema risolto](../assets/fix.svg) <!-- MC-34590 -->È stato corretto il tipo di contenuto Testo per gestire e salvare correttamente i caratteri non latini 1.

![Problema risolto](../assets/fix.svg) <!-- MC-34677 -->Fisso [!DNL Page Builder] Stili CSS che hanno causato il rendering errato da parte di Safari 13.1 del menu del sito del tema Luma per piccole porte di visualizzazione e schermi mobili.

![Problema risolto](../assets/fix.svg) <!-- MC-34846 -->È stato corretto il tipo di contenuto HTML per visualizzare correttamente i widget incorporati come _Ordina per SKU_ sul vetrina.

![Problema risolto](../assets/fix.svg) È stato corretto un errore che a volte impediva agli utenti di salvare i moduli per tipi di contenuto. L&#39;errore (&quot;[!DNL Page Builder] stava eseguendo il rendering per 5 secondi senza rilasciare blocchi&quot;) causava la rotazione indefinita dell’icona del caricatore dopo aver tentato di salvare un modulo.

## 1.3.2 per Adobe Commerce 2.3.5-p2

![Nuovo](../assets/new.svg) Miglioramenti di sicurezza.

## 1.3.1 per Adobe Commerce 2.3.5-p1

Questa versione di [!DNL Page Builder] è solo un aggiornamento del numero di versione per Adobe Commerce 2.3.5-p1. Tutte le funzioni descritte per la versione 1.3.0 si applicano anche a questa versione.

## 1.3.0 per Adobe Commerce 2.3.5

![Nuovo](../assets/new.svg) **Modelli** - [!DNL Page Builder] ora sono disponibili modelli che possono essere creati da contenuti esistenti e applicati a nuove aree di contenuto. [!DNL Page Builder] I modelli salvano sia il contenuto che i layout di pagine, blocchi, blocchi dinamici, attributi di prodotto e descrizioni di categorie esistenti. Ad esempio, puoi salvare un [!DNL Page Builder] Pagina CMS come modello e quindi applica quel modello (con tutti i relativi contenuti e layout) per creare rapidamente pagine CMS per il sito. Questa nuova funzione è documentata qui: [Modelli](templates.md).

![Nuovo](../assets/new.svg) **Sfondi video per righe, banner e cursori** - [!DNL Page Builder] Le righe, i banner e i cursori ora possono utilizzare i video per i loro sfondi. Queste nuove funzioni sono documentate qui: [Righe](row.md), [Banner](banner.md), [Cursori](slider.md).

![Nuovo](../assets/new.svg) **Miglioramenti e aggiunte al supporto video** - [!DNL Page Builder] ora supporta una più ampia varietà di formati video. Oltre ai video YouTube e Vimeo, il tipo di contenuto Video e gli sfondi video supportano ora collegamenti URL video a formati video come `.mp4` e altri formati supportati dal browser. Il tipo di contenuto Video aggiunge anche una funzione di riproduzione automatica. Queste nuove funzioni sono documentate qui: [Tipo di contenuto video](video.md).

![Nuovo](../assets/new.svg) **Righe, banner e cursori a piena altezza** - [!DNL Page Builder] Le righe, i banner e i cursori possono ora impostare l&#39;altezza massima della pagina utilizzando un numero con qualsiasi unità CSS (px, %, vh, em) o un calcolo tra unità (100vh - 237px). Queste nuove funzioni sono documentate qui: [Righe](row.md), [Banner](banner.md), [Cursori](slider.md).

![Nuovo](../assets/new.svg) **Libreria di aggiornamento del tipo di contenuto** - Gli sviluppatori possono ora creare versioni di [!DNL Page Builder] tipi di contenuto senza introdurre problemi di incompatibilità con le versioni precedenti. Prima di questa versione, modifiche significative alle configurazioni del tipo di contenuto creavano problemi di visualizzazione e perdita di dati con le versioni salvate in precedenza [!DNL Page Builder] tipi di contenuto. La nuova libreria di aggiornamento elimina questi problemi. La libreria è progettata per aggiornare le versioni precedenti dei tipi di contenuto salvati nel database in modo che corrispondano alle modifiche di configurazione apportate nelle nuove versioni. [!DNL Page Builder] esegue la libreria di aggiornamento sui tipi di contenuto nativi in base alle esigenze per una nuova versione. Questa modifica assicura che il [!DNL Page Builder] i tipi di contenuto vengono sempre aggiornati per corrispondere a eventuali modifiche apportate ai tipi di contenuto per una versione più recente.

>[!IMPORTANT]
>
>Se sono state create ulteriori entità di database per l&#39;archiviazione [!DNL Page Builder] contenuto, tu _deve_ aggiungi tali entità al tuo `etc/di.xml`. In caso contrario, il [!DNL Page Builder] il contenuto archiviato nell’entità non viene aggiornato, causando potenziale perdita di dati e problemi di visualizzazione. Ad esempio, se avete creato un&#39;entità blog che memorizza [!DNL Page Builder] contenuto, devi aggiungere la tua entità blog al tuo `etc/di.xml` file come `UpgradableEntitiesPool` in modo che la libreria di aggiornamento possa aggiornare [!DNL Page Builder] tipi di contenuto utilizzati nel blog. Per ulteriori informazioni e istruzioni sull&#39;utilizzo della libreria di aggiornamento, consulta [Aggiorna tipi di contenuto](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) nel _Guida per gli sviluppatori di Page Builder_.

![Nuovo](../assets/new.svg) **Documentazione per l&#39;aggiunta di nuovi aspetti** - Informazioni per gli sviluppatori pubblicate su [aggiunta di aspetti](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) per tipi di contenuto esistenti o personalizzati.

![Problema risolto](../assets/fix.svg) **Varie correzioni**

- <!-- PB-50 -->È stato risolto un problema a causa del quale il menu TinyMCE per il contenuto della diapositiva veniva visualizzato sotto altri tipi di contenuto se il contenitore principale della diapositiva era duplicato.
- <!-- PB-166 -->Aggiornato [!DNL Page Builder] implementare un metodo di distruzione per evitare perdite di memoria in alcuni scenari.
- <!-- PB-170 -->Sono state migliorate le prestazioni di TinyMCE quando si utilizzano più istanze in Admin Stage.
- <!-- PB-252 -->È stato risolto un problema a causa del quale il tipo di contenuto Blocco dinamico non viene riprodotto in Admin stage se la riga superiore è contrassegnata come nascosta.
- <!-- PB-273 -->È stato perfezionato il passaggio del mouse sugli eventi in Admin Stage, rimuovendo un ritardo di 200 ms dai vari controlli dell’interfaccia utente. Questa modifica semplifica l’utilizzo degli elementi di contenuto nidificati nell’area di visualizzazione.
- <!-- PB-294 -->È stato risolto un problema che causava l’escape errato del simbolo di valuta nel widget Elenco prodotti all’interno del Blocco/Blocco dinamico nella fase di amministrazione.
- <!-- PB-296 -->È stato risolto un problema a causa del quale il totale del prodotto in [!DNL Page Builder] il pannello di modifica non funzionava per i prodotti MSI stock personalizzati.
- <!-- PB-317 -->È stato risolto un problema in cui il salvataggio [!DNL Page Builder] il contenuto con immagini di sfondo su Microsoft Edge non esegue il rendering di tali immagini nella vetrina.
- <!-- PB-390 -->È stato risolto un problema in cui le [!DNL Page Builder] Il contenuto non viene salvato se gli utenti fanno clic sul pulsante Salva prima del rendering completo della pagina.
- <!-- PB-418 -->È stato corretto un errore di eccezione generato nei processi cron a causa di [!DNL Page Builder] analisi.

## 1.2.2 per Adobe Commerce 2.3.4-p2

![Nuovo](../assets/new.svg) Miglioramenti di sicurezza.

## 1.2.1 per Adobe Commerce 2.3.4-p1

![Nuovo](../assets/new.svg) Miglioramenti di sicurezza.

## 1.2.0 per Adobe Commerce 2.3.4

![Nuovo](../assets/new.svg)  **[!DNL Page Builder]integrazione con PWA Studi** - Aggiunto [!DNL Page Builder] rendering dei contenuti nell’app Venia in PWA Studi. [!DNL Page Builder] ora è possibile visualizzare il contenuto nell’app PWA Studi Venia. Consulta la [!DNL Page Builder] documentazione in [PWA Studi] per tutte le informazioni su questa nuova funzione.

![Nuovo](../assets/new.svg) **Carosello prodotto aggiunto** - <!-- PB-77, PB-173, PB-175 -->Il tipo di contenuto Prodotti ora offre un’opzione per visualizzare i prodotti in formato carosello/cursore, comprese diverse opzioni per personalizzare il carosello in base alle tue esigenze.

![Nuovo](../assets/new.svg) **Ordinamento SKU prodotto aggiunto** - <!-- PB-69 -->Il tipo di contenuto Prodotti ora fornisce un’opzione per ordinare i prodotti in base allo SKU nell’ordine in cui li aggiungi a un elenco in Admin.

![Nuovo](../assets/new.svg) **Ordinamento categorie di prodotti aggiunto** - <!-- PB-181 -->. Il tipo di contenuto Prodotti ora fornisce un’opzione per ordinare i prodotti per categoria _position_, visualizzandoli nello stesso ordine in cui appaiono nel Catalogo Commerce.

![Nuovo](../assets/new.svg) **Totali selezionati per il prodotto aggiunti** - <!-- PB-107 -->. L’editor di amministrazione del tipo di contenuto Prodotti ora visualizza il numero totale di prodotti che corrispondono alle opzioni di selezione dei prodotti.

![Problema risolto](../assets/fix.svg) **Varie correzioni**

- <!-- PB-237 -->Miglioramenti di sicurezza.
- <!-- PB-41 -->Sono state corrette le ricerche all’interno dei componenti di selezione dell’interfaccia utente per effettuare una sola richiesta AJAX per termine di ricerca.
- <!-- PB-76, PB-84-->Le anteprime dei prodotti nell&#39;amministratore sono state aggiornate per corrispondere alla vetrina, incluse le opzioni di valutazione a stelle, colore e dimensione del prodotto, se pertinenti.
- <!-- PB-169 -->È stato risolto un problema in cui [!DNL Page Builder] non poteva essere salvato quando la minimizzazione e il bundling JavaScript sono abilitati in Commerce.
- <!-- PB-241 -->Sono state corrette le anteprime amministratore di Prodotti, Blocchi e Blocchi dinamici per il corretto rendering nelle installazioni Commerce che definiscono URL diversi per l’Amministratore e il front-end.
- <!-- PB-238 -->Sono state corrette le anteprime amministratore di Prodotti, Blocchi e Blocchi dinamici per il corretto rendering nelle installazioni Commerce con B2B installato con _Solo accesso_ opzione abilitata. Prima di questa correzione, il [!DNL Page Builder] con l’anteprima, la pagina viene reindirizzata all’accesso dell’account cliente.
- <!-- PB-239 -->È stato corretto un errore di sessione che poteva verificarsi durante l’anteprima di una pagina di grandi dimensioni in [!DNL Page Builder] Amministratore
- <!-- PB-248 -->Aggiornato [!DNL Page Builder] MENO stili per evitare la duplicazione degli stili della vetrina.

## 1.1.1 per Adobe Commerce 2.3.3-p1

![Nuovo](../assets/new.svg) Miglioramenti di sicurezza.

## 1.1.0 per Adobe Commerce 2.3.3

![Nuovo](../assets/new.svg) <!-- MC-15250 -->Al tipo di contenuto Prodotti è stato aggiunto l’ordinamento esplicito dei prodotti.

![Nuovo](../assets/new.svg) <!-- MC-17823 -->Sono stati aggiunti pulsanti per l’inserimento di immagini, widget e variabili nel tipo di contenuto HTML.

![Problema risolto](../assets/fix.svg) Migliorato [!DNL Page Builder] sicurezza.

![Problema risolto](../assets/fix.svg) <!-- MC-1805 -->Aggiornato [!DNL Page Builder] per supportare PHP versione 7.3.

![Problema risolto](../assets/fix.svg) <!-- MC-4137 -->Aggiornamento di TinyMCE alla versione 4.9.5. Questo aggiornamento, insieme ai miglioramenti aggiuntivi, ha risolto diversi problemi dell’editor in linea TinyMCE:

- Le variabili, le immagini e i collegamenti alle immagini vengono aggiunti nel punto in cui si trova il cursore.
- Le tabelle e le celle di tabella possono essere allineate al centro.
- Copia/Incolla ora incolla il contenuto nella posizione del cursore.
- I collegamenti possono essere applicati al testo selezionato.
- I punti elenco sono allineati correttamente.
- Le modifiche all’interno dell’editor in linea possono essere salvate senza prima fare clic all’esterno dell’editor.

![Problema risolto](../assets/fix.svg) <!-- MC-3880 -->È stato risolto un problema a causa del quale l’altezza minima e l’allineamento verticale non erano coerenti tra le sezioni del pannello di modifica per ciascun tipo di contenuto.

![Problema risolto](../assets/fix.svg) <!-- MC-14994 -->È stato risolto un problema a causa del quale la barra degli strumenti del tipo di contenuto Titolo veniva posizionata in modo errato alla prima eliminazione nell’area di visualizzazione.

![Problema risolto](../assets/fix.svg) <!-- MC-15742 -->Sono stati corretti i margini hardcoded nei tipi di contenuto Slider e Video.

![Problema risolto](../assets/fix.svg) <!-- MC-16241 -->È stato risolto un problema a causa del quale il simbolo asterisco richiesto veniva visualizzato due volte nei campi modulo.

## 1.0.3 per Adobe Commerce 2.3.2-p2

![Nuovo](../assets/new.svg) Miglioramenti di sicurezza.

## 1.0.2 per Adobe Commerce 2.3.2-p1

![Nuovo](../assets/new.svg) Miglioramenti di sicurezza.

## 1.0.1 per Adobe Commerce 2.3.2

![Nuovo](../assets/new.svg) Garantisce la compatibilità con Adobe Commerce 2.3.2.

## 1.0.0 per Adobe Commerce 2.3.1

![Nuovo](../assets/new.svg) Versione di disponibilità generale


[PWA Studi]: https://developer.adobe.com/commerce/pwa-studio/
