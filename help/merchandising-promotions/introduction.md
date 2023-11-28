---
title: Introduzione al merchandising e alle promozioni di Commerce
description: Scopri gli strumenti Commerce per creare promozioni mirate e opportunità di coinvolgimento dei clienti.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Introduzione al merchandising e alle promozioni di Commerce

Promozioni mirate, opportunità di coinvolgimento per i clienti e opportunità per trasformare gli acquirenti in acquirenti. Gestisci le relazioni con i clienti sostenendo le attività successive all’acquisto e offrendo sconti speciali ai clienti fidelizzati. Scopri le best practice e le tecniche per supportare le iniziative SEO (Search Engine Optimization).

## Merchandising

_Merchandising_ è un termine utilizzato nel commercio al dettaglio per descrivere l&#39;arte e la scienza dello sviluppo della piantina e della presentazione dei prodotti. Potresti pensare al [navigazione basata su categorie](../catalog/navigation-top.md) come la planimetria del negozio, e la presentazione dinamica dei prodotti come le condizioni che si possono applicare all&#39;elenco dei prodotti nel negozio. Inoltre, puoi implementare programmi che incrementano le vendite dei prodotti:

- [Visual Merchandiser](visual-merchandiser.md) - Insieme di strumenti avanzati che consente di posizionare i prodotti e di applicare condizioni che determinano quali prodotti vengono visualizzati nell&#39;elenco delle categorie.

- [Registri regali](gift-registries.md) - Offrite ai vostri clienti la possibilità di creare registri di regali per occasioni speciali e di invitare amici e familiari ad acquistare i regali dal registro.

- [Premi e fedeltà](rewards-loyalty.md) : utilizza un sistema a punti per implementare programmi specifici che stimolino il coinvolgimento dei clienti e ne promuovano la fidelizzazione. È possibile assegnare punti per un&#39;ampia gamma di attività relative a transazioni e clienti e controllare l&#39;assegnazione, il saldo e la scadenza dei punti.

- [Vendite ed eventi privati](events-private-sales.md) : utilizza la base di clienti esistente per generare nuovi lead o nuovi clienti oppure per scaricare le scorte in eccesso tramite vendite private e altri eventi di catalogo.

>[!TIP]
>
>Per informazioni sul Product Recommendations e su come fornirti le informazioni e i controlli necessari per creare l’esperienza migliore per i tuoi acquirenti, consulta la sezione [Guida utente di Recommendations del prodotto](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

## Promozioni

In Adobe Commerce, utilizza le funzioni di promozione per impostare relazioni di prodotto e utilizzare le regole di prezzo per attivare gli sconti in base a varie condizioni. Puoi utilizzare le regole di prezzo per offrire incentivi ai clienti, ad esempio:

- Invia ai tuoi migliori clienti un coupon per uno sconto su un prodotto specifico
- Spedizione gratuita per acquisti superiori a un determinato importo
- Pianificare una promozione per un periodo di tempo specifico

Una regola è una raccolta di condizioni (una o più) che applicano modifiche ai prezzi dei prodotti quando una o tutte sono soddisfatte. Ogni regola può avere più condizioni, applicabili quando tutte o una qualsiasi istruzione (una o più, ma non tutte) sono vere o false.

### Condizioni

Le condizioni sono istruzioni che definiscono l’elenco di prodotti e situazioni per l’applicazione della regola. Gli attributi e le opzioni per le condizioni differiscono tra i tipi di regole disponibili. Quando viene soddisfatta, l’azione viene completata come sconti, buy-one-get-one (BOGO) e altre opzioni. Le regole possono essere semplici o complicate in base alle esigenze aziendali, agli sconti stagionali e alle promozioni e alle opportunità di un anno. Ad esempio, puoi aggiungere alcune opzioni per le festività e fornire la spedizione gratuita per tutto l’anno quando i carrelli hanno un subtotale elevato.

>[!NOTE]
>
>Se desideri definire una condizione in base a un attributo di prodotto specifico, **[!UICONTROL Use for Promo Rule Conditions]** deve essere impostato su `Yes` per l’attributo nel tuo [Proprietà vetrina](../catalog/attribute-product-create.md).


### Regole di prezzo

Per [regole di prezzo catalogo](price-rules-catalog.md), vengono create condizioni basate su [set di attributi](../catalog/attribute-sets.md) nel catalogo, funzioni di confronto e attributi selezionati. Puoi creare condizioni come le frasi selezionando alcune istruzioni. Ad esempio, puoi creare due regole di prezzo per applicare sconti per abbigliamento per bambini e abbigliamento per uomo/donna in base alla categoria.

![Diagramma: esempio di regole di prezzo del catalogo](./assets/diagram-catalog-price-rules.png){width="500"}

[Regola prezzo carrello](price-rules-cart.md) Le condizioni possono essere basate su qualsiasi categoria figlio del negozio [radice](../catalog/category-root.md). Le regole di prezzo sono stabilite in anticipo e si attivano ogni volta che le condizioni richieste sono soddisfatte. Queste regole utilizzano attributi, incluse combinazioni di attributi di prodotto come la corrispondenza di uno SKU nel carrello utilizzando gli attributi di prodotto. Queste regole possono anche utilizzare condizioni di quantità per la selezione del prodotto, combinazioni di condizioni per regole complicate e attributi del carrello come subtotale.

![Diagramma: esempio di regole di prezzo del carrello](./assets/diagram-cart-price-rules.png){width="500"}

## Comunicazioni e SEO

Masterizzazione [Ottimizzazione dei motori di ricerca (SEO)](seo-overview.md) è fondamentale per attirare potenziali acquirenti. Scopri come ottimizzare i motori di ricerca e come ottimizzare il contenuto e la presentazione del sito per migliorare il modo in cui le pagine vengono indicizzate dai motori di ricerca.

Una delle attività da completare prima di lanciare il tuo store è quella di rivedere i modelli e-mail utilizzati per tutte le comunicazioni inviate dal tuo store, per assicurarsi che riflettano il tuo marchio. Ma dovresti fare un ulteriore passo in avanti sviluppando altre comunicazioni che promuovano il tuo marchio e i tuoi prodotti presso i clienti esistenti. Puoi personalizzare il contenuto con variabili e tag di markup.

>[!NOTE]
>
>Adobe Commerce e le versioni di Magento Open Source da 2.4.0 a 2.4.3 includevano l’estensione dotdigital sviluppata da un fornitore e utilizzata per l’integrazione con dotdigital Engagement Cloud. A partire dalla versione 2.4.4, questa estensione non è più inclusa nella versione core e deve essere installata e aggiornata dalla versione Commerci Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.
><br><br>
>Se l’estensione in bundle è abilitata e configurata, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Consulta [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nel _Guida all’aggiornamento_ per ulteriori informazioni.

- [Newsletter](newsletters.md) : redazione di newsletter, gestione dell&#39;elenco degli abbonati, sviluppo di contenuti e traffico verso il negozio.

- [Feed RSS](social-rss.md#rss-feeds) : utilizza i feed RSS per pubblicare le informazioni sui prodotti sui siti di aggregazione degli acquisti e persino per includerli nelle newsletter. I clienti possono abbonarsi ai feed RSS per conoscere i nuovi prodotti e le promozioni.

- [Social network](social-rss.md#social-networks) : integra il tuo store con i social network installando un’estensione Marketplace o aggiungendo un plug-in alle pagine dei contenuti.

## Strumenti di marketing Google

La configurazione del negozio è integrata con i seguenti strumenti di Google per ottimizzare i contenuti, analizzare il traffico e collegare il catalogo ad aggregatori di acquisti e marketplace.

>[!NOTE]
>
>A partire dalla versione 2.4.5, l’integrazione dei servizi Google viene aggiornata per supportare l’utilizzo delle API GTag. GTag è un meccanismo unificato per l’integrazione con le funzionalità di Google per le pagine web e supporta le funzionalità e le opportunità più recenti per il tracciamento e la gestione dei contenuti tramite Google Services. Per ulteriori informazioni, vedere [Documentazione per gli sviluppatori Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) : utilizza Google Universal Analytics per definire dimensioni e metriche personalizzate aggiuntive per il tracciamento, con supporto per le interazioni offline e con le app mobili e accesso agli aggiornamenti continui.

- [Esperimenti sui contenuti Google](google-content-experiments.md) : configura un test A/B di prodotti, categorie o pagine di contenuti utilizzando Contenuto Google Analytics

- [Gestione tag Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) Solo per Adobe Commerce: utilizza Google Tag Manager per gestire i numerosi tag relativi agli eventi delle campagne di marketing.

- [Google AdWords](google-adwords.md) : crea una campagna Google AdWords e tieni traccia delle conversioni per il tuo store.
