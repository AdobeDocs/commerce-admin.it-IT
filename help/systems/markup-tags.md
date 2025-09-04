---
title: Tag di markup
description: Scopri i tag di markup che contengono snippet di codice per fare riferimento a un oggetto nell’archivio.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Tag di markup

Un tag di markup è una direttiva che contiene uno snippet di codice con un riferimento relativo a un oggetto nell’archivio, ad esempio una variabile, un URL, un’immagine o un blocco. I tag di markup possono essere utilizzati ovunque sia disponibile l&#39;editor e incorporati nel HTML dei modelli [email](email-templates.md) e [newsletter](../merchandising-promotions/newsletter-template.md), nonché di altri tipi di [content](../content-design/introduction.md#content).

I tag di markup sono racchiusi tra parentesi graffe e doppie e possono essere generati dallo strumento Widget o digitati direttamente nel contenuto di HTML. Ad esempio, invece di utilizzare come codifica fissa il percorso completo di una pagina, puoi utilizzare un tag di markup per rappresentare l’URL del negozio. I tag di markup descritti negli esempi seguenti includono:

{{$include /help/_includes/directives-caution.md}}

## Variabile personalizzata

Il tag di markup Variable può essere utilizzato per inserire una [variabile personalizzata](variables-custom.md) in un modello e-mail, blocchi, newsletter e pagine di contenuto.

\{\{CustomVar code= &quot;variabile_personalizzata&quot;}}

## URL store

Il tag di markup URL store rappresenta l’URL di base del sito web e viene utilizzato come sostituto della prima parte di un URL completo, incluso il nome di dominio. Esistono due versioni di questo tag di markup: una che viene indirizzata direttamente all&#39;archivio e l&#39;altra con una barra (`/`) alla fine utilizzata quando viene aggiunto un percorso.

\{\{store url=&#39;apparel/shoes/womens&#39;}}

## URL contenuto multimediale

Il tag di markup URL per elementi multimediali dinamici rappresenta la posizione e il nome file di un&#39;immagine memorizzata in una rete CDN (Content Delivery Network). Il tag può essere utilizzato per inserire un’immagine in una pagina, un blocco, un banner o un modello e-mail.

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## ID blocco

Il tag di markup Block ID (ID blocco) è uno dei più semplici da utilizzare e può essere utilizzato per inserire un blocco direttamente in una pagina CMS o anche nidificato all’interno di un altro blocco. Puoi utilizzare questa tecnica per modificare un blocco per diverse promozioni o lingue. Il tag di markup ID blocco fa riferimento a un blocco tramite il relativo identificatore.

\{\{block id=&#39;block-id&#39;}}

## Tag modello

Un tag modello fa riferimento a un file modello PHTML e può essere utilizzato per visualizzare il blocco in una pagina CMS o in un blocco statico. Il codice nell&#39;esempio seguente può essere aggiunto a una pagina o a un blocco per visualizzare il modulo Contattaci.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}}

Il codice riportato nell’esempio successivo può essere aggiunto a una pagina o a un blocco per visualizzare un elenco di prodotti in una categoria specifica, in base all’ID categoria.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## Codice widget

Lo strumento Widget può essere utilizzato per visualizzare elenchi di prodotti o per inserire collegamenti complessi, ad esempio quelli che portano a una pagina di prodotto specifica, in base all’ID prodotto. Il codice generato include il riferimento del blocco, la posizione del modulo di codice e il modello PHTML corrispondente. Una volta generato il codice, puoi copiarlo e incollarlo da una posizione all’altra.

Il codice nell’esempio seguente può essere aggiunto a una pagina o a un blocco per visualizzare l’elenco dei nuovi prodotti.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

Il codice nell’esempio successivo può essere aggiunto a una pagina o a un blocco per visualizzare un collegamento a un prodotto specifico, per ID prodotto.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;My Product Link&quot; title=&quot;My Product Link&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## Utilizzare i tag di markup nei collegamenti

Puoi utilizzare i tag di markup con i tag di ancoraggio di HTML e collegarti direttamente a qualsiasi pagina del negozio. Il collegamento può essere incorporato in pagine di contenuto, blocchi o modelli e-mail e newsletter. Puoi usare questa tecnica anche per collegare un’immagine a una pagina specifica.

### Passaggio 1: Identificare l’URL di destinazione

Se possibile, accedi alla pagina a cui desideri collegarti e copia l’URL completo dalla barra degli indirizzi del browser. La parte dell&#39;URL necessaria segue `.com/`. In caso contrario, copia la chiave URL dalla pagina CMS che desideri utilizzare come destinazione del collegamento.

#### URL completo alla pagina della categoria

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### URL completo della pagina del prodotto

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### URL completo della pagina CMS

`https://mystore.com/about-us`

### Passaggio 2: Aggiungi il markup all’URL

Il tag URL store rappresenta l&#39;URL di base del sito Web e viene utilizzato come sostituto della parte dell&#39;indirizzo HTTP dell&#39;URL dell&#39;archivio, inclusi il nome di dominio e `.com`. Esistono due versioni del tag, che puoi utilizzare, a seconda dei risultati che desideri ottenere.

`store direct_url` - Collegamenti diretti a una pagina.

`store url` - Inserisce una barra alla fine, in modo che sia possibile aggiungere altri riferimenti come percorso.

Negli esempi seguenti, la chiave URL è racchiusa tra virgolette singole e l&#39;intero tag di markup è racchiuso tra parentesi graffe. Se utilizzato con un tag di ancoraggio, il tag di markup viene posizionato all&#39;interno delle virgolette doppie dell&#39;ancoraggio. Per evitare confusione, è possibile alternare tra virgolette singole e doppie per ogni insieme di virgolette nidificato.

Se si sta iniziando con un URL completo, eliminare la parte dell&#39;indirizzo HTTP (`http://` o `https://`) dell&#39;URL, fino al `.com/` incluso. Al suo posto, immetti il tag di markup URL del Negozio, fino alla virgoletta singola di apertura.

#### Archivia tag di markup URL

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

In caso contrario, immetti la prima parte del tag di markup URL store e incolla la chiave URL o il percorso copiato in precedenza.

### Archivia tag di markup URL con chiave URL

`{{store url=`

Per completare il tag di markup, immettere le virgolette doppie di chiusura e le parentesi graffe.

`{{store url='apparel/shoes/womens'}}`

### Passaggio 3: Completa il tag di ancoraggio

Racchiudi il tag di markup completato all’interno di un tag di ancoraggio, utilizzando il tag di markup invece dell’URL di destinazione. Quindi, aggiungi il testo del collegamento e il tag di ancoraggio di chiusura.

#### Markup nel tag di ancoraggio

\&lt;a href=&quot;\{\{tag markup inserito qui}}&quot;>Testo collegamento\&lt;/a>

Incolla il tag di ancoraggio completato nel codice di qualsiasi pagina, blocco, banner o modello e-mail di CMS in cui desideri visualizzare il collegamento.

### Collegamento completo con markup

\&lt;a href=&quot;\{\{store url=&#39;vestel/shoes&#39;}}&quot;>Vendita di scarpe\&lt;/a>

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
