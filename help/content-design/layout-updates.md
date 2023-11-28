---
title: Aggiornamenti del layout
description: Scopri come utilizzare gli aggiornamenti del layout per personalizzare il layout di una pagina.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# Aggiornamenti del layout

Prima di iniziare a lavorare con gli aggiornamenti del layout personalizzato, è importante comprendere come vengono costruite le pagine del negozio e la differenza tra i termini *layout* e *aggiornamento del layout*. Layout si riferisce alla composizione visiva e strutturale della pagina. L&#39;aggiornamento del layout si riferisce a un insieme specifico di istruzioni XML che possono sostituire o personalizzare la modalità di costruzione della pagina.

Il layout XML della [!DNL Commerce] store è una struttura gerarchica di contenitori e blocchi. Alcuni elementi vengono visualizzati in ogni pagina, altri solo in pagine specifiche. Per ulteriori informazioni su layout, contenitori e blocchi, consulta [Panoramica dei layout](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) nel _Guida per gli sviluppatori di front-end_.

Il [Widget](widgets.md) è un modo semplice per aggiungere un [blocco di contenuto](blocks.md) al layout predefinito di una pagina. Per aggiornamenti più avanzati, è necessario salvare il codice di aggiornamento del layout XML sul server e quindi fare riferimento al file come aggiornamento del layout personalizzato dall&#39;amministratore. Per una panoramica del processo, vedi [Usa aggiornamenti layout](layout-updates.md#place-a-block-using-layout-updates).

Nel diagramma seguente, i nomi che fanno riferimento ai contenitori sono neri e i tipi di blocchi, o percorsi di classi di blocchi, sono blu.

![Diagramma di layout a blocchi standard](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Tipo di blocco | Descrizione |
|--- |--- |
| `page/html` | Il nome di questo blocco è `root` ed è uno dei pochi blocchi principali nel layout. Puoi anche creare un blocco personalizzato e denominarlo `root`, nome standard per i blocchi di questo tipo. Può esistere un solo blocco di questo tipo per pagina. |
| `page/html_head` | Il nome del blocco è `head` ed è un figlio del blocco principale. Può esistere un solo blocco di questo tipo per pagina e non deve essere rimosso. |
| `page/html_notices` | Il nome del blocco è `global_notices` ed è un figlio del blocco principale. Se questo blocco viene rimosso dal layout, gli avvisi globali non vengono visualizzati nella pagina. Può esistere un solo blocco di questo tipo per pagina. |
| `page/html_header` | Il nome del blocco è `header` ed è un figlio del blocco principale. Questo blocco corrisponde all’intestazione visiva nella parte superiore della pagina e contiene diversi blocchi standard. Può esistere un solo blocco di questo tipo per pagina e non deve essere rimosso. |
| `page/html_wrapper` | Anche se incluso nel layout predefinito, questo blocco è obsoleto ed è incluso solo per garantire la compatibilità con le versioni precedenti. Non utilizzare blocchi di questo tipo. |
| `page/html_breadcrumbs` | Il nome di questo blocco è `breadcrumbs` ed è un elemento secondario del blocco intestazione. Questo blocco visualizza le breadcrumb per la pagina corrente. Può esistere un solo blocco di questo tipo per pagina. |
| `page/html_footer` | Il nome del blocco è `footer` ed è un figlio del blocco principale. Il blocco piè di pagina corrisponde al piè di pagina visivo nella parte inferiore della pagina e contiene diversi blocchi standard. Può esistere un solo blocco di questo tipo per pagina e non deve essere rimosso. |
| `page/template_links` | Nel layout standard sono presenti due blocchi di questo tipo. Il `top.links` Il blocco è un elemento secondario del blocco intestazione e corrisponde al menu di navigazione superiore. Il `footer_links` è un elemento figlio del blocco piè di pagina e corrisponde al menu di navigazione inferiore. <br/><br/>**_Nota:_**È possibile manipolare i collegamenti dei modelli, come mostrato negli esempi. |
| `page/switch` | Esistono due blocchi di questo tipo in un layout standard. Il `store_language` block è un elemento figlio del blocco di intestazione e corrisponde al selettore della lingua principale. Il `store_switcher` block è un elemento figlio del blocco footer e corrisponde al commutatore store inferiore. |
| core/messages | Esistono due blocchi di questo tipo in un layout standard. Il `global_messages` blocco visualizza messaggi globali. Il `messages` viene utilizzato per visualizzare tutti gli altri messaggi. Se rimuovi questi blocchi, il cliente non visualizza alcun messaggio. |
| `core/text_list` | Questo tipo di blocco è ampiamente utilizzato in [!DNL Commerce] come segnaposto per il rendering dei blocchi figlio. |
| `core/profiler` | Esiste una sola istanza di questo tipo di blocco per pagina. Viene utilizzato per il [!DNL Commerce] e non devono essere utilizzati per altri scopi. |

{style="table-layout:auto"}

## Posizionare un blocco utilizzando gli aggiornamenti del layout

[Aggiornamenti del layout](layout-updates.md) consentire di personalizzare il layout di una pagina. Gli aggiornamenti del layout offrono maggiore flessibilità rispetto a [widget](widgets.md), ma richiedono l&#39;accesso al server e una conoscenza di base di XML.

Nei passaggi seguenti viene illustrato come utilizzare un aggiornamento del layout per posizionare un blocco in una pagina. Per esempi specifici e informazioni sulla sintassi, consulta [Attività comuni di personalizzazione del layout](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) nel _Guida per gli sviluppatori di front-end_.

### Passaggio 1: creare il blocco

1. Creare [blocco](block-add.md) che vuoi inserire.

1. Prendi nota della `block_id`, perché viene utilizzato nelle istruzioni di aggiornamento del layout.

### Passaggio 2: creare l’aggiornamento del layout in XML

1. Componi le istruzioni di layout in XML in [Fare riferimento a un blocco CMS](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Salva il [istruzioni di layout](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) sul server nella cartella di layout in cui vengono salvati i file XML per il tema.

   Ad esempio:

   `<theme_dir>/<Namespace>_<Module>/layout`

   Il punto di manipolazione di layout è il nome del file che inizia con `cms_page_view_selectable_`, seguito dalla chiave URL della pagina CMS, dall’opzione di aggiornamento del layout e dalla `xml` suffisso file. Nell&#39;esempio seguente, `customer-service` è la chiave URL della pagina e `ChatTool` è l’opzione selezionata per applicare l’aggiornamento del layout alla pagina.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Elemento | Descrizione |
   |--- |--- |
   | Identificatore pagina CMS | Chiave URL della pagina con qualsiasi barra (`/`) sostituito da un carattere di sottolineatura (`_`). |
   | Nome aggiornamento layout | Opzione visualizzata per _Aggiornamento del layout personalizzato_. |

   {style="table-layout:auto"}

### Passaggio 3: Includere un riferimento all’aggiornamento del layout dalla pagina

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Individua la pagina in cui desideri inserire il blocco e aprila in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Design]** sezione.

1. Per visualizzare tutti gli aggiornamenti di layout disponibili associati alla pagina, fare clic sul pulsante **[!UICONTROL Custom Layout Update]** menu.

   ![Elenco aggiornamenti layout personalizzato](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Seleziona l’aggiornamento del layout da applicare alla pagina.

### Passaggio 4: salvare e aggiornare la cache

1. Al termine, fai clic su **[!UICONTROL Save & Close]**.

1. Nel messaggio nella parte superiore dell’area di lavoro, fai clic su **[!UICONTROL Cache Management]** e aggiorna tutti gli elementi della cache non validi.
