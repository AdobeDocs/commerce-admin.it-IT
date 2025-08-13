---
title: Introduzione al merchandising e alle promozioni di Commerce
description: Scopri gli strumenti di Commerce per la creazione di promozioni e opportunità mirate per il coinvolgimento cliente.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 1%

---

# Introduzione al merchandising e alle promozioni di Commerce

Promozioni mirate, opportunità di coinvolgimento per i clienti e opportunità per trasformare gli acquirenti in acquirenti. Gestisci le relazioni con i clienti sostenendo le attività successive all’acquisto e offrendo sconti speciali ai clienti fidelizzati. Scopri le best practice e le tecniche per supportare le iniziative SEO (Search Engine Optimization).

## Merchandising

_Merchandising_ è un termine utilizzato nel settore retail per descrivere l&#39;arte e la scienza dello sviluppo della piantina e della presentazione dei prodotti. È possibile considerare la [navigazione basata su categorie](../catalog/navigation-top.md) come la piantina del negozio e la presentazione dinamica dei prodotti come le condizioni applicabili all&#39;elenco dei prodotti nel negozio. Inoltre, puoi implementare programmi che incrementano le vendite dei prodotti:

- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [Visual Merchandiser](visual-merchandiser.md) - Un insieme di strumenti avanzati che ti consente di posizionare i prodotti e di applicare condizioni che determinano quali prodotti vengono visualizzati nell&#39;elenco delle categorie.

- [Registri regali](gift-registries.md) - Offri ai tuoi clienti la possibilità di creare registri regali per occasioni speciali e di invitare amici e familiari ad acquistare i regali dal registro regali.

- [Premi e fidelizzazione](rewards-loyalty.md): utilizza un sistema a punti per implementare programmi univoci che stimolano il coinvolgimento dei clienti e ne promuovono la fidelizzazione. È possibile assegnare punti per un&#39;ampia gamma di attività relative a transazioni e clienti e controllare l&#39;assegnazione, il saldo e la scadenza dei punti.

- [Vendite ed eventi privati](events-private-sales.md) - Utilizza la base clienti esistente per generare nuovi clienti potenziali o per scaricare le scorte in eccesso tramite vendite private e altri eventi di catalogo.

>[!TIP]
>
>Per informazioni sui consigli di prodotto e su come possono offrirti insight e il controllo di cui hai bisogno per creare la migliore esperienza per i tuoi acquirenti, consulta la [Guida utente dei consigli di prodotto](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html).

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
>Se vuoi definire una condizione basata su un attributo di prodotto specifico, **[!UICONTROL Use for Promo Rule Conditions]** deve essere impostato su `Yes` per l&#39;attributo nelle [Proprietà storefront](../catalog/attribute-product-create.md).


### Regole di prezzo

Per [regole prezzo catalogo](price-rules-catalog.md), è possibile creare condizioni basate su [set di attributi](../catalog/attribute-sets.md) nel catalogo, funzioni di confronto e attributi selezionati. Puoi creare condizioni come le frasi selezionando alcune istruzioni. Ad esempio, puoi creare due regole di prezzo per applicare sconti per abbigliamento per bambini e abbigliamento per uomo/donna in base alla categoria.

![Diagramma - esempio di regole del prezzo di catalogo](./assets/diagram-catalog-price-rules.png){width="500"}

[Le condizioni per il prezzo del carrello](price-rules-cart.md) possono essere basate su qualsiasi categoria figlio dell&#39;archivio [root](../catalog/category-root.md). Le regole di prezzo sono stabilite in anticipo e si attivano ogni volta che le condizioni richieste sono soddisfatte. Queste regole utilizzano attributi, incluse combinazioni di attributi di prodotto come la corrispondenza di uno SKU nel carrello utilizzando gli attributi di prodotto. Queste regole possono anche utilizzare condizioni di quantità per la selezione del prodotto, combinazioni di condizioni per regole complicate e attributi del carrello come subtotale.

![Diagramma - Esempio di regole del prezzo del carrello](./assets/diagram-cart-price-rules.png){width="500"}

## Comunicazioni e SEO

La masterizzazione di [Search Engine Optimization (SEO)](seo-overview.md) è fondamentale per coinvolgere potenziali acquirenti. Scopri come ottimizzare i motori di ricerca e come ottimizzare il contenuto e la presentazione del sito per migliorare il modo in cui le pagine vengono indicizzate dai motori di ricerca.

Una delle attività da completare prima di lanciare il tuo store è quella di rivedere i modelli e-mail utilizzati per tutte le comunicazioni inviate dal tuo store, per assicurarsi che riflettano il tuo marchio. Ma dovresti fare un ulteriore passo in avanti sviluppando altre comunicazioni che promuovano il tuo marchio e i tuoi prodotti presso i clienti esistenti. Puoi personalizzare il contenuto con variabili e tag di markup.

>[!NOTE]
>
>Le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includono l’estensione sviluppata da un fornitore digitale e utilizzata per l’integrazione con Engagement Cloud digitale. A partire dalla versione 2.4.4, questa estensione non è più inclusa nella versione core e deve essere installata e aggiornata da Commerce Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.
>&#x200B;><br><br>
>&#x200B;>Se l’estensione in bundle è abilitata e configurata, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Per ulteriori informazioni, vedere [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.

- [Newsletter](newsletters.md) - Produci newsletter, gestisci l&#39;elenco degli abbonati, sviluppa contenuti e indirizza il traffico verso il tuo archivio.

- [Feed RSS](social-rss.md#rss-feeds) - Utilizzare i feed RSS per pubblicare le informazioni sui prodotti nei siti di aggregazione acquisti e persino includerli nelle newsletter. I clienti possono abbonarsi ai feed RSS per conoscere i nuovi prodotti e le promozioni.

- [Social network](social-rss.md#social-networks) - Integra lo store con i social network installando un&#39;estensione Marketplace o aggiungendo un plug-in alle pagine di contenuto.

## Strumenti di marketing Google

La configurazione del negozio è integrata con i seguenti strumenti di Google per ottimizzare i contenuti, analizzare il traffico e collegare il catalogo ad aggregatori di acquisti e marketplace.

>[!NOTE]
>
>A partire dalla versione 2.4.5, l’integrazione dei servizi Google viene aggiornata per supportare l’utilizzo delle API GTag. GTag è un meccanismo unificato per l’integrazione con le funzionalità di Google per le pagine web e supporta le funzionalità e le opportunità più recenti per il tracciamento e la gestione dei contenuti tramite Google Services. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md): utilizza Google Universal Analytics per definire dimensioni e metriche personalizzate aggiuntive per il tracciamento, con supporto per le interazioni offline e con app mobili e accesso agli aggiornamenti in corso.

- [Gestione tag Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Utilizza Gestione tag Google per gestire i numerosi tag relativi agli eventi delle campagne di marketing.

- [Google AdWords](google-adwords.md) - Crea una campagna Google AdWords e tieni traccia delle conversioni per il tuo archivio.
