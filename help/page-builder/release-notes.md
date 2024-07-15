---
title: Note sulla versione per  [!DNL Page Builder]
description: Consulta le note sulla versione per informazioni su tutte le  [!DNL Page Builder]  versioni.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Note sulla versione per [!DNL Page Builder]

Queste note sulla versione descrivono le versioni di [!DNL Page Builder] e includono:

![Nuove](../assets/new.svg) nuove funzionalità

![Problema risolto](../assets/fix.svg) correzioni e miglioramenti

![Problema noto](../assets/bug.svg) Problemi noti

>[!IMPORTANT]
>
>A partire dalla versione 2.4.3, [!DNL Page Builder] è ora disponibile come estensione in bundle nel Magento Open Source. Ora è lo strumento di modifica dei contenuti predefinito sia per Adobe Commerce che per Magento Open Source e può sostituire l’editor WYSIWG con qualsiasi modulo di terze parti.

## 1.7.2 per Commerce 2.4.5

![Nuovo](../assets/new.svg) **Nuova entità wrapper - [!DNL Columns] contenitore introdotto per i layout di colonna** - In precedenza, gli utenti potevano aggiungere colonne solo all&#39;interno di un altro tipo di contenuto contenitore/wrapper, ad esempio [!DNL Tab] o [!DNL Row]. Ora [!DNL Column] ha il proprio wrapper e può essere aggiunto direttamente sull&#39;area di visualizzazione. Inoltre, il contenitore [!DNL Columns] dispone di un elemento impostazioni in cui gli utenti possono specificare la configurazione per questa entità wrapper.<!--- PB-500-->

![Nuovo](../assets/new.svg) **Nuove opzioni di menu per duplicare, nascondere ed eliminare i gruppi di colonne**. Con queste nuove opzioni, gli utenti possono duplicare, nascondere ed eliminare [!DNL Columns] gruppi, esattamente come con i tipi di contenuto.<!--- PB-507-->

![Nuovo](../assets/new.svg) <!-- Issue 594 -->**È stato aggiunto il supporto per nuove colonne su più righe al gruppo di colonne**. Con questa aggiunta, gli utenti possono manipolare più righe di colonne all&#39;interno di un gruppo [!DNL Columns] per rendere molto più flessibili i layout delle colonne.<!--- PB-108-->

Per informazioni sull&#39;utilizzo del nuovo gruppo [!DNL Columns], vedere [Layout - Colonna](./column.md).

## 1.7.1 per Commerce 2.4.4

![Problema risolto](../assets/fix.svg) Il Page Builder è ora compatibile con PHP 8.1.<!--- AC-1300-->

![Problema risolto](../assets/fix.svg) I commercianti possono ora aggiungere testo alternativo (`alt_text`) alle immagini (immagine, banner, diapositiva) per migliorare l&#39;accessibilità del contenuto.<!--- PB-1193-->

![È stato risolto il problema](../assets/fix.svg). Gli utenti amministratori con autorizzazioni limitate alla sola modifica del contenuto non visualizzano più un errore quando utilizzano Page Builder per aggiungere un widget di prodotto a una pagina CMS. Page Builder visualizza anche un conteggio accurato dei prodotti nella pagina delle impostazioni del widget. In precedenza, Page Builder richiedeva le autorizzazioni per il modulo Catalogo durante il recupero del conteggio dei prodotti e visualizzava questo errore: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problema risolto](../assets/fix.svg) I problemi di visualizzazione del menu Formato Page Builder ora vengono risolti con l&#39;aggiornamento della libreria TinyMCE 5. <!--- AC-446-->

![Problema risolto](../assets/fix.svg) È ora possibile utilizzare il mouse per modificare un valore **Text To Display** nel popup Inserisci collegamento. <!--- AC-982-->

![Problema risolto](../assets/fix.svg) In Page Builder vengono ora visualizzate tutte le opzioni come previsto nel menu delle opzioni Dimensione carattere. In precedenza, non venivano visualizzate tutte le opzioni. <!--- AC-1056-->

![È stato risolto il problema](../assets/fix.svg). La dipendenza del Compositore `phpgt/dom` per l&#39;estensione `magento/magento2-page-builder` è stata aggiornata alle versioni più recenti. <!--- magento/magento2-page-builder/pull/779-->

![Problema risolto](../assets/fix.svg) In Page Builder non vengono più ridimensionate le finestre di dialogo Inserisci collegamento e Inserisci immagine durante la visualizzazione del dispositivo di scorrimento in una piccola colonna. <!--- AC-973-->

![Problema risolto](../assets/fix.svg) Il menu Page Builder Table Properties (Proprietà tabella di Page Builder) ora viene visualizzato come previsto. <!--- AC-407-->

![È stato risolto il problema](../assets/fix.svg) I punti del cursore non vengono più visualizzati nel modale Inserisci collegamento o immagine quando il cursore non è posizionato. <!--- AC-406-->

![Problema risolto](../assets/fix.svg) La dimensione del carattere utilizzata per visualizzare le opzioni del menu Tabella è stata ottimizzata. <!--- AC-396-->

![È stato corretto il problema](../assets/fix.svg). Sono state corrette le anomalie relative al posizionamento delle finestre di dialogo Inserisci/Modifica immagine e Inserisci/Modifica collegamento. <!--- AC-397-->

![Problema risolto](../assets/fix.svg) Il Page Builder non genera più un errore quando si fa clic su **Editor di testo** per un banner. <!--- AC-398-->

![Problema risolto](../assets/fix.svg) Durante l&#39;aggiornamento Page Builder non converte più tutti i blocchi dinamici in un&#39;unica lingua. <!--- MC-42265-->

## 1.6.0 per Adobe Commerce 2.4.2

![Nuovo](../assets/new.svg) <!-- Issue 558 -->**Nuovo stile [!DNL Page Builder]** - [!DNL Page Builder] ha apportato notevoli miglioramenti alla modalità di creazione degli stili del contenuto. Le modifiche ora semplificano la creazione di semplici selettori CSS per ignorare gli stili del tipo di contenuto esistenti. Queste modifiche consentono di creare [!DNL Page Builder] temi con tempi di risposta avanzati per tutti i tipi di contenuto.

![Nuovo](../assets/new.svg) <!-- Issue 429 -->**Contenitore riga ora facoltativo** - È ora possibile creare contenuto in [!DNL Page Builder] senza richiedere un contenitore Riga. Oltre alla riga, è ora possibile trascinare e rilasciare direttamente sullo stage i seguenti tipi di contenuto: HTML, Blocco, Blocco dinamico, Colonne e Schede.

![Nuovo](../assets/new.svg) <!-- Issue 636 -->**Nuovo commutatore del riquadro di visualizzazione reattivo** - È ora possibile visualizzare in anteprima il contenuto di [!DNL Page Builder] con larghezze del dispositivo diverse (punti di interruzione) utilizzando i nuovi pulsanti del commutatore del riquadro di visualizzazione Amministratore sopra l&#39;area di visualizzazione. Il selettore del riquadro di visualizzazione simula lo stile del contenuto quando viene visualizzato nella vetrina utilizzando dispositivi diversi.

![Nuovo](../assets/new.svg) <!-- Issue 637 -->**Nuovi campi modulo specifici per punti di interruzione** - È ora possibile impostare i valori dei campi del tipo di contenuto su punti di interruzione specifici per i riquadri di visualizzazione. Gli indicatori delle icone accanto ai campi mostrano il riquadro di visualizzazione a cui viene applicato il valore del campo del tipo di contenuto.

![Nuovo](../assets/new.svg) <!-- Issue 559 -->**Voci di campo modulo predefinite rimosse** - Le impostazioni avanzate del modulo per i margini, i bordi e le proprietà correlate ai bordi (bordo, larghezza del bordo e raggio del bordo) ora sono impostate come `default`, in modo che i valori possano essere definiti dal CSS di un modulo.

![Nuovo](../assets/new.svg) <!-- Issue 635, 557,  -->**Spaziatura tra le pagine aggiunta** - Le righe e le colonne ora forniscono spazio aggiuntivo per i tipi di contenuto contenuti contenuti nell&#39;area di visualizzazione, ma non nell&#39;area di visualizzazione. La spaziatura tra gli intervalli consente di accedere più facilmente ai menu delle opzioni del mouse over sia per il tipo di contenuto contenitore che per quello contenuto.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-37348 -->**È stato corretto lo scorrimento automatico delle recensioni**. Lo scorrimento automatico delle recensioni dei prodotti nella vetrina è ora risolto.

![Problema risolto](../assets/fix.svg) <!-- MC-36227 -->**Contenuto ritagliato fisso** - Le descrizioni di prodotti e categorie lunghe non vengono più ritagliate.

![Problema risolto](../assets/fix.svg) <!-- MC-35402 -->**Contenuto categoria full-bleed fisso** - Il contenuto categoria può ora essere visualizzato in layout full-width o full-bleed.

![Problema risolto](../assets/fix.svg) <!-- MC-37989 -->**Miglioramenti della sicurezza**

## 1.5.1 per Adobe Commerce 2.4.1-p1

![È stato risolto il problema](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Visualizzazione dell&#39;errore**. È stato risolto un problema a causa del quale [!DNL Page Builder] visualizzava un errore durante l&#39;aggiunta delle sottocategorie del catalogo nell&#39;amministratore.

## 1.5.0 per Adobe Commerce 2.4.1

![Nuovo](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Modifica coinvolgente a schermo intero** - La modifica del contenuto di [!DNL Page Builder] è ora a schermo intero solo per tutte le aree controllate da [!DNL Page Builder]. Questa modifica include pagine CMS, pagine di prodotti e categorie, blocchi e blocchi dinamici. La modifica a schermo intero consente di mettere a fuoco i contenuti e offre una visualizzazione che corrisponde meglio all&#39;esperienza utente nella vetrina.

![Nuovi](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] anteprime dei contenuti **- Per impostazione predefinita, [!DNL Page Builder] ora fornisce anteprime dei contenuti non solo per pagine CMS, blocchi e blocchi dinamici, ma anche per pagine di prodotti e categorie. È possibile configurare questa funzione in modo che sia attivata o disattivata per le pagine di prodotti e categorie utilizzando la nuova impostazione Anteprima contenuto [!DNL Page Builder], a cui si accede nella configurazione dello store in Gestione contenuto > Strumenti di contenuto avanzati.

![Nuovo](../assets/new.svg) <!-- Issue 543 -->**Accesso migliorato alle descrizioni brevi del prodotto** - Per impostazione predefinita, viene ora visualizzata una descrizione breve del prodotto prima della descrizione più lunga. Questa modifica determina una corrispondenza con l’ordine in cui vengono visualizzate nella vetrina e impedisce la necessità di scorrere il contenuto della descrizione più lunga per accedere alla descrizione breve.

![Nuovo](../assets/new.svg) <!-- Issue 419 -->**Impedisce i collegamenti nidificati nei banner e nelle diapositive**. L&#39;aggiunta di collegamenti sia al contenuto che agli elementi esterni dei banner e delle diapositive ha creato collegamenti nidificati che non sono visualizzati o si comportano correttamente nella vetrina. Per risolvere il problema, non è più possibile aggiungere collegamenti a *sia* nell&#39;area Testo messaggio che nell&#39;attributo Collegamento per i banner e le diapositive.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 421 --> È stato risolto il problema per cui l&#39;impostazione di un raggio del bordo vuoto in un elemento Scheda causava errori e interruzioni nel contenuto dell&#39;elemento Scheda.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 422 --> È stato risolto il problema che impediva il salvataggio del modulo Prodotti quando si aggiungevano determinate combinazioni di condizioni al filtro Condizione prodotti.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 425 -->È stato risolto un problema a causa del quale il tipo di contenuto Slider non si comportava correttamente quando l&#39;impostazione Ciclo infinito era disabilitata.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 426 -->È stato corretto il prezzo minimo annunciato in modo che ora funzioni in [!DNL Page Builder].

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 436 -->In Safari e IE 11 era stato impedito di trascinare un&#39;immagine nell&#39;area di caricamento dei banner e delle diapositive.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 525 -->È stato risolto il problema a causa del quale il tipo di contenuto Slider non rispondeva in Firefox.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 567 -->È stato risolto il problema che causava la creazione di selettori non corretti nel DOM da parte della configurazione del widget per aspetti diversi.

![È stato risolto un problema](../assets/fix.svg) <!-- Issue 609 -->È stato risolto il problema che impediva l&#39;accesso al modulo e ad altre opzioni nella barra degli strumenti Intestazione.

![È stato risolto il problema](../assets/fix.svg) <!-- Issue 612, 613 -->Sono stati risolti dei problemi a causa dei quali i cursori e le righe multiple che utilizzano sfondi parallasse non venivano riprodotti correttamente dopo aver attivato più volte la modalità a schermo intero.

![È stato risolto il problema](../assets/fix.svg) <!--MC-35220-->È stato risolto il problema che impediva il salvataggio di [!DNL Page Builder] durante il tentativo di copiare il contenuto da un tipo di contenuto Titolo a un tipo di contenuto Testo.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-34620 -->È stato corretto il tipo di contenuto Testo per gestire e salvare correttamente i caratteri non latini 1.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-34679 -->Sono stati corretti [!DNL Page Builder] stili CSS a causa dei quali in Safari 13.1 veniva eseguito erroneamente il rendering del menu del sito del tema Luma per piccole porte di visualizzazione e schermi mobili.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-34848 -->È stato corretto il tipo di contenuto HTML per visualizzare correttamente nello storefront widget incorporati come &quot;Ordina per SKU&quot;.

## 1.4.1 per Adobe Commerce 2.4.0-p1

![Nuovo](../assets/new.svg) <!-- PB-590 --> aggiornato a TinyMCE 4. È stato rimosso TinyMCE 3 per migliorare la sicurezza.

## 1.4.0 per Adobe Commerce 2.4.0

![Nuovo](../assets/new.svg) <!-- PB-494 -->Aggiunto supporto per PHP 7.4.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-31247 -->È stato risolto un problema a causa del quale il tipo di contenuto Prodotti non mostrava prodotti configurabili quando la condizione era impostata sul prezzo.

![È stato risolto il problema](../assets/fix.svg) <!-- PB-179 -->È stata corretta la configurazione di allineamento dei prodotti in modo da posizionare solo il contenitore dei prodotti stesso, non il contenuto del contenitore dei prodotti, ad esempio il nome, il prezzo, i pulsanti, le immagini e altri elementi del prodotto.

![Problema risolto](../assets/fix.svg) <!-- MC-33556 -->Miglioramenti delle prestazioni.

![È stato risolto il problema](../assets/fix.svg). Miglioramenti della sicurezza.

## 1.3.3-p1 per Adobe Commerce 2.3.6-p1

![È stato risolto il problema](../assets/fix.svg). Miglioramenti della sicurezza.

## 1.3.3 per Adobe Commerce 2.3.6

![È stato risolto il problema](../assets/fix.svg) <!-- MC-32766 -->È stato corretto il tipo di contenuto Testo per salvare correttamente le direttive delle variabili aggiunte agli attributi html.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-34590 -->È stato corretto il tipo di contenuto Testo per gestire e salvare correttamente i caratteri non latini 1.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-34677 -->Sono stati corretti [!DNL Page Builder] stili CSS a causa dei quali in Safari 13.1 veniva eseguito erroneamente il rendering del menu del sito del tema Luma per piccole porte di visualizzazione e schermi mobili.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-34846 -->È stato corretto il tipo di contenuto HTML per visualizzare correttamente i widget incorporati come _Ordina per SKU_ nella vetrina.

![È stato risolto un problema](../assets/fix.svg) che a volte impediva agli utenti di salvare i moduli di tipo contenuto. L&#39;errore (&quot;[!DNL Page Builder] ha eseguito il rendering per 5 secondi senza rilasciare blocchi&quot;) ha causato la rotazione indefinita dell&#39;icona del caricatore dopo aver tentato di salvare un modulo.

## 1.3.2 per Adobe Commerce 2.3.5-p2

![Nuovi](../assets/new.svg) miglioramenti alla sicurezza.

## 1.3.1 per Adobe Commerce 2.3.5-p1

Questa versione di [!DNL Page Builder] è solo un aggiornamento del numero di versione per Adobe Commerce 2.3.5-p1. Tutte le funzioni descritte per la versione 1.3.0 si applicano anche a questa versione.

## 1.3.0 per Adobe Commerce 2.3.5

![Nuovo](../assets/new.svg) **Modelli** - [!DNL Page Builder] ora dispone di modelli che possono essere creati dal contenuto esistente e applicati alle nuove aree di contenuto. I modelli [!DNL Page Builder] salvano sia il contenuto che i layout di pagine, blocchi, blocchi dinamici, attributi di prodotto e descrizioni delle categorie esistenti. Ad esempio, puoi salvare come modello una pagina CMS [!DNL Page Builder] esistente e quindi applicare tale modello (con tutti i relativi contenuti e layout) per creare rapidamente pagine CMS per il sito. Questa nuova funzione è documentata qui: [Modelli](templates.md).

![Nuovo](../assets/new.svg) **Sfondi video per righe, banner e cursori** - [!DNL Page Builder] righe, banner e cursori ora possono utilizzare video per i loro sfondi. Queste nuove funzioni sono documentate qui: [Rows](row.md), [Banners](banner.md), [Sliders](slider.md).

![Nuovo](../assets/new.svg) **Il supporto video è stato aggiunto e migliorato**. [!DNL Page Builder] ora supporta una più ampia varietà di formati video. Oltre ai video YouTube e Vimeo, il tipo di contenuto Video e gli sfondi video supportano ora collegamenti URL video a formati video come `.mp4` e altri formati supportati dal browser. Il tipo di contenuto Video aggiunge anche una funzione di riproduzione automatica. Queste nuove funzioni sono documentate qui: [Tipo di contenuto video](video.md).

![Nuovo](../assets/new.svg) **Righe, banner e cursori a piena altezza** - [!DNL Page Builder] Le righe, i banner e i cursori possono ora impostare la loro altezza sull&#39;altezza completa della pagina utilizzando un numero con qualsiasi unità CSS (px, %, vh, em) o un calcolo tra unità (100vh - 237px). Queste nuove funzioni sono documentate qui: [Rows](row.md), [Banners](banner.md), [Sliders](slider.md).

![Nuova](../assets/new.svg) **Libreria di aggiornamento del tipo di contenuto** - Gli sviluppatori possono ora creare versioni di [!DNL Page Builder] tipi di contenuto senza introdurre problemi incompatibili con le versioni precedenti. Prima di questa versione, modifiche significative alle configurazioni dei tipi di contenuto creavano problemi di visualizzazione e perdita di dati con i tipi di contenuto [!DNL Page Builder] salvati in precedenza. La nuova libreria di aggiornamento elimina questi problemi. La libreria è progettata per aggiornare le versioni precedenti dei tipi di contenuto salvati nel database in modo che corrispondano alle modifiche di configurazione apportate nelle nuove versioni. [!DNL Page Builder] esegue la libreria di aggiornamento sui tipi di contenuto nativi in base alle esigenze per una nuova versione. Questa modifica assicura che i tipi di contenuto [!DNL Page Builder] incorporati vengano sempre aggiornati in modo da corrispondere alle modifiche apportate ai tipi di contenuto per una versione più recente.

>[!IMPORTANT]
>
>Se hai creato altre entità di database per l&#39;archiviazione del contenuto di [!DNL Page Builder], _devi_ aggiungerle al tuo `etc/di.xml`. In caso contrario, il contenuto di [!DNL Page Builder] archiviato nell&#39;entità non verrà aggiornato, causando la potenziale perdita di dati e problemi di visualizzazione. Ad esempio, se hai creato un&#39;entità blog che memorizza il contenuto [!DNL Page Builder], devi aggiungere l&#39;entità blog al file `etc/di.xml` come tipo `UpgradableEntitiesPool` in modo che la libreria di aggiornamento possa aggiornare i tipi di contenuto [!DNL Page Builder] utilizzati nel blog. Per ulteriori informazioni e istruzioni sull&#39;utilizzo della libreria di aggiornamento, vedere [Aggiornare i tipi di contenuto](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) nella _Guida per gli sviluppatori di Page Builder_.

![Nuovo](../assets/new.svg) **Documentazione per l&#39;aggiunta di nuovi aspetti** - Sono state pubblicate informazioni per gli sviluppatori relative a [aggiunta di aspetti](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) per tipi di contenuto esistenti o personalizzati.

![Problema risolto](../assets/fix.svg) **Varie correzioni**

- <!-- PB-50 -->È stato risolto un problema a causa del quale il menu TinyMCE per il contenuto della diapositiva veniva visualizzato sotto altri tipi di contenuto se il contenitore principale della diapositiva era duplicato.
- <!-- PB-166 -->[!DNL Page Builder] è stato aggiornato per implementare un metodo di eliminazione per evitare perdite di memoria in alcuni scenari.
- <!-- PB-170 -->Sono state migliorate le prestazioni di TinyMCE quando si utilizzano più istanze in Admin Stage.
- <!-- PB-252 -->È stato risolto un problema a causa del quale il tipo di contenuto Blocco dinamico non viene riprodotto in Admin stage se la riga superiore è contrassegnata come nascosta.
- <!-- PB-273 -->È stato perfezionato il passaggio del mouse sugli eventi in Admin Stage, rimuovendo un ritardo di 200 ms dai vari controlli dell’interfaccia utente. Questa modifica semplifica l’utilizzo degli elementi di contenuto nidificati nell’area di visualizzazione.
- <!-- PB-294 -->È stato risolto un problema che causava l’escape errato del simbolo di valuta nel widget Elenco prodotti all’interno del Blocco/Blocco dinamico nella fase di amministrazione.
- <!-- PB-296 -->È stato risolto un problema che impediva il funzionamento del totale dei prodotti nel pannello di modifica [!DNL Page Builder] per i prodotti MSI azionari personalizzati.
- <!-- PB-317 -->È stato risolto un problema a causa del quale il salvataggio di contenuto [!DNL Page Builder] con immagini di sfondo in Microsoft Edge non riproduceva tali immagini nella vetrina.
- <!-- PB-390 -->È stato risolto un problema che impediva il salvataggio del contenuto [!DNL Page Builder] nidificato se gli utenti facevano clic sul pulsante Salva prima del rendering completo della pagina.
- <!-- PB-418 -->È stata corretta un&#39;eccezione di errore generata nei processi cron a causa di [!DNL Page Builder] analisi.

## 1.2.2 per Adobe Commerce 2.3.4-p2

![Nuovi](../assets/new.svg) miglioramenti alla sicurezza.

## 1.2.1 per Adobe Commerce 2.3.4-p1

![Nuovi](../assets/new.svg) miglioramenti alla sicurezza.

## 1.2.0 per Adobe Commerce 2.3.4

Integrazione ![New](../assets/new.svg) **[!DNL Page Builder]con PWA Studio** - Aggiunta del rendering del contenuto [!DNL Page Builder] all&#39;app Venia in PWA Studio. È ora possibile visualizzare il contenuto [!DNL Page Builder] nell&#39;app PWA Studio Venia. Per informazioni su questa nuova funzionalità, consulta la documentazione di [!DNL Page Builder] in [PWA Studi].

![Nuovo](../assets/new.svg) **Carosello prodotto aggiunto** - <!-- PB-77, PB-173, PB-175 -->Il tipo di contenuto Prodotti ora fornisce un&#39;opzione per visualizzare i prodotti in un formato carosello/cursore, incluse diverse opzioni per personalizzare il carosello in base alle tue esigenze.

![Nuovo](../assets/new.svg) **Ordinamento SKU prodotto aggiunto** - <!-- PB-69 -->Il tipo di contenuto Prodotti ora fornisce un&#39;opzione per ordinare i prodotti in base allo SKU nell&#39;ordine in cui li si aggiunge a un elenco in Admin.

![Nuovo](../assets/new.svg) **Ordinamento categoria prodotto aggiunto** - <!-- PB-181 -->. Il tipo di contenuto Prodotti ora fornisce un&#39;opzione per ordinare i prodotti in base alla categoria _posizione_, visualizzandoli nello stesso ordine in cui compaiono nel catalogo Commerce.

![Nuovo](../assets/new.svg) **Aggiunti totali di selezione prodotti** - <!-- PB-107 -->. L’editor di amministrazione del tipo di contenuto Prodotti ora visualizza il numero totale di prodotti che corrispondono alle opzioni di selezione dei prodotti.

![Problema risolto](../assets/fix.svg) **Varie correzioni**

- <!-- PB-237 -->Miglioramenti di sicurezza.
- <!-- PB-41 -->Sono state corrette le ricerche all’interno dei componenti di selezione dell’interfaccia utente per effettuare una sola richiesta AJAX per termine di ricerca.
- <!-- PB-76, PB-84-->Le anteprime dei prodotti nell&#39;amministratore sono state aggiornate per corrispondere alla vetrina, incluse le opzioni di valutazione a stelle, colore e dimensione del prodotto, se pertinenti.
- <!-- PB-169 -->È stato risolto un problema che impediva il salvataggio di [!DNL Page Builder] se in Commerce erano abilitati la minimizzazione e il bundling di JavaScript.
- <!-- PB-241 -->Sono state corrette le anteprime amministratore di Prodotti, Blocchi e Blocchi dinamici per eseguire correttamente il rendering sulle installazioni di Commerce che definiscono URL diversi per l’Amministratore e il front-end.
- <!-- PB-238 -->Sono state corrette le anteprime amministratore di Prodotti, Blocchi e Blocchi dinamici per eseguire correttamente il rendering sulle installazioni di Commerce con B2B installato con l&#39;opzione _Solo accesso_ abilitata. Prima di questa correzione, l&#39;anteprima di [!DNL Page Builder] causerebbe il reindirizzamento della pagina all&#39;accesso dell&#39;account cliente.
- <!-- PB-239 -->È stato corretto un errore di sessione che poteva verificarsi durante l&#39;anteprima di una pagina grande nell&#39;amministratore [!DNL Page Builder].
- <!-- PB-248 -->Sono stati aggiornati [!DNL Page Builder] stili in meno per impedire la duplicazione degli stili della vetrina.

## 1.1.1 per Adobe Commerce 2.3.3-p1

![Nuovi](../assets/new.svg) miglioramenti alla sicurezza.

## 1.1.0 per Adobe Commerce 2.3.3

![Nuovo](../assets/new.svg) <!-- MC-15250 -->È stato aggiunto l&#39;ordinamento esplicito dei prodotti al tipo di contenuto Prodotti.

![Nuovo](../assets/new.svg) <!-- MC-17823 -->Sono stati aggiunti pulsanti per l&#39;inserimento di immagini, widget e variabili nel tipo di contenuto HTML.

![È stato corretto il problema](../assets/fix.svg). È stata migliorata la sicurezza di [!DNL Page Builder].

![Problema risolto](../assets/fix.svg) <!-- MC-1805 -->Aggiornamento di [!DNL Page Builder] per supportare PHP versione 7.3.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-4137 -->Aggiornamento di TinyMCE alla versione 4.9.5. Questo aggiornamento, insieme ai miglioramenti aggiuntivi, ha risolto diversi problemi dell’editor in linea TinyMCE:

- Le variabili, le immagini e i collegamenti alle immagini vengono aggiunti nel punto in cui si trova il cursore.
- Le tabelle e le celle di tabella possono essere allineate al centro.
- Copia/Incolla ora incolla il contenuto nella posizione del cursore.
- I collegamenti possono essere applicati al testo selezionato.
- I punti elenco sono allineati correttamente.
- Le modifiche all’interno dell’editor in linea possono essere salvate senza prima fare clic all’esterno dell’editor.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-3880 -->È stato risolto un problema a causa del quale l&#39;altezza minima e l&#39;allineamento verticale erano incoerenti tra le sezioni nel pannello di modifica per ogni tipo di contenuto.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-14994 -->È stato risolto un problema a causa del quale la barra degli strumenti del tipo di contenuto Intestazione non era posizionata correttamente la prima volta che veniva rilasciata sull&#39;area di visualizzazione.

![È stato risolto il problema](../assets/fix.svg) <!-- MC-15742 -->Sono stati corretti i margini hardcoded nei tipi di contenuto Slider e Video.

![È stato risolto un problema](../assets/fix.svg) <!-- MC-16241 -->È stato risolto un problema a causa del quale il simbolo dell&#39;asterisco richiesto veniva visualizzato due volte nei campi modulo.

## 1.0.3 per Adobe Commerce 2.3.2-p2

![Nuovi](../assets/new.svg) miglioramenti alla sicurezza.

## 1.0.2 per Adobe Commerce 2.3.2-p1

![Nuovi](../assets/new.svg) miglioramenti alla sicurezza.

## 1.0.1 per Adobe Commerce 2.3.2

![Nuovo](../assets/new.svg) Assicura la compatibilità con Adobe Commerce 2.3.2.

## 1.0.0 per Adobe Commerce 2.3.1

![Nuovo](../assets/new.svg) rilascio di disponibilità generale


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
