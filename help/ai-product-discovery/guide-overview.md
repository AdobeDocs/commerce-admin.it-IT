---
title: Rilevamento di prodotti AI
description: Scopri in che modo l'arricchimento del catalogo [!DNL Adobe Commerce] e l'arricchimento PDP colmano le lacune nei dati strutturati dei prodotti e nella copia incentrata sull'acquirente per l'individuazione dei prodotti AI.
role: Admin, User, Leader
source-git-commit: f2cf82dad7ec3c86a3b9a0a5635556ac2e77dd05
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%
---
# Rilevamento di prodotti AI

L&#39;individuazione dei prodotti è il modo in cui i consumatori trovano e valutano i prodotti che soddisfano le loro esigenze. Negli strumenti di intelligenza artificiale per conversazioni come [!DNL ChatGPT] e [!DNL Gemini], gli acquirenti possono descrivere ciò che desiderano nel linguaggio quotidiano e utilizzare le risposte generate dall&#39;intelligenza artificiale per esplorare e confrontare i prodotti. L’utilità di tali risposte dipende in parte dalla possibilità per gli agenti di IA di accedere e interpretare i dati pertinenti dei prodotti.

## Per chi è questa guida {#who-this-guide-is-for}

- Professionisti del marketing digitale e commercianti che desiderano che i dati dei prodotti siano accurati e utili nell’individuazione dei prodotti basata sull’intelligenza artificiale.
- Merchandising che necessitano di un metodo controllato per arricchire i prodotti selezionati o preparare una copia per una campagna.
- [!DNL Adobe Commerce] amministratori responsabili dell&#39;accesso ai dati, ai servizi e agli amministratori del catalogo.

## Perché l&#39;individuazione dei prodotti è importante

Gli acquirenti spesso descrivono un bisogno, un uso o una preferenza, anziché cercare un nome di prodotto o un attributo tecnico esatto. Per far corrispondere tali richieste con i prodotti pertinenti, gli agenti di IA necessitano di informazioni sui prodotti strutturate e significative per gli acquirenti.

Quando i registri dei prodotti sono incompleti, incoerenti o incentrati solo sulle specifiche tecniche, gli agenti possono avere difficoltà a capire quali prodotti si adattano alle intenzioni degli acquirenti. Gli acquirenti possono perdere prodotti importanti e i commercianti possono dover dedicare del tempo alla correzione e all&#39;arricchimento manuale dei contenuti del catalogo.

Inoltre, le query senza marchio creano nuove opportunità per l’individuazione dei prodotti. Quando gli acquirenti descrivono le loro esigenze senza specificare un marchio, le superfici di IA mostrano prodotti rilevanti per i diversi marchi concorrenti in base al grado di corrispondenza tra tali prodotti e l’intento degli acquirenti. Per i commercianti, questo crea l’opportunità di raggiungere nuovi clienti che potrebbero non avere familiarità con il proprio marchio, espandendo la visibilità dei prodotti oltre la consapevolezza del marchio esistente.

Tuttavia, l’individuazione dei prodotti sulle superfici di IA presenta alcune difficoltà, ad esempio lacune nel catalogo che possono limitare l’individuazione dei prodotti basata sull’intelligenza artificiale.

[!DNL Adobe Commerce] risolve questi problemi di lacuna del catalogo fornendo due flussi di lavoro di arricchimento complementari: arricchimento della pagina dei dettagli del prodotto e arricchimento del catalogo. Questi due arricchimenti migliorano il modo in cui gli agenti di intelligenza artificiale accedono, comprendono e abbinano i prodotti agli intenti dell’acquirente. Sono accessibili nel menu _Admin_ > **AI Product Discovery**.

## I dati di prodotto sono difficili da trovare e interpretare

Le informazioni sui prodotti sono spesso distribuite tra attributi, varianti, opzioni, categorie e altri campi del catalogo. Anche se queste informazioni possono essere disponibili per gli acquirenti nella vetrina, non sono sempre accessibili o facilmente interpretabili dai crawler di intelligenza artificiale. I dettagli del prodotto presentati tramite contenuti con rendering dinamico, componenti dipendenti da JavaScript, procedure guidate interattive per gli acquisti, pop-up o pagine collegate possono essere difficili da recuperare per i crawler.

Anche quando queste informazioni sono accessibili, possono non essere strutturate in modo che gli agenti di intelligenza artificiale possano interpretarle in modo affidabile. Di conseguenza, gli agenti di intelligenza artificiale potrebbero non comprendere completamente le funzioni, le opzioni e le funzionalità di un prodotto, limitando la loro capacità di abbinare in modo accurato i prodotti alle esigenze degli acquirenti.

### Rendere disponibili i dati strutturati con l&#39;arricchimento della pagina dettagli prodotto

L’arricchimento PDP crea un payload di dati strutturati contenente informazioni rilevanti sul prodotto, inclusi attributi, varianti, opzioni, punti elenco delle funzioni, relazioni tra categorie, prezzi e disponibilità. In questo modo gli agenti AI hanno una conoscenza più completa e strutturata delle funzioni, delle funzionalità e delle configurazioni disponibili di un prodotto.

Utilizzando [Ottimizza con la tecnologia Edge](#prerequisites), le informazioni sul prodotto arricchite sono rese direttamente accessibili ai crawler di intelligenza artificiale senza richiedere modifiche alla vetrina visibile dall&#39;utente. I commercianti possono migliorare il modo in cui le informazioni sui prodotti vengono presentate agli agenti di intelligenza artificiale senza modificare i layout della vetrina, introdurre nuovi componenti rivolti agli acquirenti o richiedere uno sviluppo personalizzato della vetrina.

Consulta [arricchimento della pagina dei dettagli del prodotto](pdp-enrichment.md).

## Il catalogo prodotti non riflette le intenzioni dell’acquirente

Gli acquirenti descrivono sempre più le loro esigenze, i loro problemi e i casi d’uso previsti nel linguaggio naturale piuttosto che cercare nomi di prodotti o specifiche tecniche specifiche. Tuttavia, i nomi e le descrizioni dei prodotti si concentrano spesso su attributi tecnici senza comunicare chiaramente i vantaggi, i casi di utilizzo o i problemi reali a cui il prodotto è destinato.

Questo crea un divario tra il modo in cui i consumatori esprimono le loro esigenze e il modo in cui i prodotti vengono descritti nel catalogo. Senza un contenuto di prodotto chiaro e incentrato sull’acquirente, gli agenti di intelligenza artificiale potrebbero avere difficoltà a interpretare il valore e la rilevanza di un prodotto secondo le intenzioni dell’acquirente, trascurando potenzialmente i prodotti adatti a favore di alternative le cui descrizioni sono più chiaramente in linea con le sue esigenze.

### Ottimizzare il contenuto del catalogo dei prodotti con le intenzioni degli acquirenti mediante l’arricchimento del catalogo

L’arricchimento del catalogo trasforma gli attributi tecnici dei prodotti e le informazioni esistenti sul catalogo in nomi e descrizioni di prodotti incentrati sull’acquirente che comunicano chiaramente i vantaggi, le funzionalità e i casi di utilizzo reali di un prodotto. I nomi e le descrizioni dei prodotti sono tra le fonti di informazioni più influenti utilizzate dalle superfici di IA per comprendere le funzionalità dei prodotti e determinarne la rilevanza per gli intenti dell’acquirente.

Collegando le specifiche tecniche dei prodotti alle esigenze e ai problemi descritti dagli acquirenti nel linguaggio naturale, l’arricchimento dei cataloghi aiuta gli agenti di intelligenza artificiale a comprendere meglio il valore di un prodotto, a ridurre l’ambiguità nell’interpretazione delle sue funzionalità e a far corrispondere in modo più accurato i prodotti rilevanti agli intenti degli acquirenti.

I commercianti possono esaminare e approvare i miglioramenti suggeriti prima di applicarli direttamente al catalogo dei prodotti Adobe Commerce. In questo modo i punti di vendita e i canali di vendita basati sul catalogo possono comunicare in modo coerente agli acquirenti le stesse informazioni sui prodotti, arricchite e basate sui valori, attraverso diversi punti di contatto.

Vedi [Arricchimento del catalogo](catalog-enrichment.md).

#### Regole di governance del brand

Le regole di governance del brand consentono di definire i requisiti della copia del prodotto per l’arricchimento del catalogo, tra cui lunghezza, frasi, tono e maiuscole. Queste regole si applicano solo all’arricchimento del catalogo, non all’arricchimento PDP.

Consulta [Creare regole per il marchio di arricchimento del catalogo](brand-governance.md).
