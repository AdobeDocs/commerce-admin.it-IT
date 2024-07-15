---
title: Impostazione pagina
description: Scopri come configurare le impostazioni predefinite per le parti principali di una pagina del negozio.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Impostazione pagina

Le sezioni principali della pagina sono controllate, in parte, da un set di tag HTML standard. Alcuni di questi tag possono essere utilizzati per determinare la selezione di font, colore, dimensioni, colori di sfondo e immagini utilizzati in ogni sezione della pagina. Altre impostazioni controllano gli elementi della pagina, ad esempio il logo nell&#39;intestazione e l&#39;avviso di copyright nel piè di pagina. Queste sezioni corrispondono alla struttura sottostante della pagina HTML e molte delle proprietà di base possono essere impostate dall’amministratore.

- [Testa HTML](#html-head)
- [Intestazione](#header)
- [Piè di pagina](#footer)

![Sezioni pagina HTML](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## Testa HTML

Le impostazioni nella sezione HTML Head corrispondono al tag `<head>` di una pagina HTML e possono essere configurate per ogni visualizzazione dello store. Oltre ai metadati per il titolo della pagina, la descrizione e le parole chiave, la sezione include un collegamento al favicon e script vari. In questa sezione sono anche configurate le istruzioni per i robot dei motori di ricerca e la visualizzazione dell’avviso di dimostrazione del negozio.

### Configurare l’intestazione del HTML

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione archivio da configurare e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. In _Altre impostazioni_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL HTML Head]**.

   ![Impostazioni di configurazione HTML Head](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Aggiorna [favicon](../getting-started/storefront-branding.md#add-a-favicon) se necessario.

1. Aggiorna le impostazioni del titolo della pagina in base alle tue esigenze:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   È possibile utilizzare un suffisso e/o un prefisso con il titolo predefinito per creare un titolo in due o tre parti. È possibile aggiungere una barra verticale o due punti come separatore tra il prefisso o il suffisso e il titolo predefinito.

1. Aggiungi o modifica i metadati che supportano l’ottimizzazione SEO (Search Engine Optimization) e aiutano a indirizzare i clienti verso il tuo store dai risultati della ricerca:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Immetti **[!UICONTROL Scripts and Style Sheets]** come necessario.

1. Abilita o disabilita l&#39;[avviso archivio demo](../getting-started/storefront-branding.md#set-the-store-demo-notice) se necessario.

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.

### Descrizioni dei campi HTML Head

| Campo | Ambito | Descrizione |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Visualizzazione store | Carica la piccola immagine grafica visualizzata nella barra degli indirizzi e nella scheda del browser. Tipi di file consentiti: ICO, PNG, APNG, GIF e JPG JPEG. Non tutti i browser supportano questi formati. |
| [!UICONTROL Default Page Title] | Visualizzazione store | Titolo visualizzato sulla barra del titolo di ogni pagina visualizzata in un browser. Il titolo predefinito viene utilizzato per tutte le pagine, a meno che non venga specificato un altro titolo per le singole pagine. |
| [!UICONTROL Page Title Prefix] | Visualizzazione store | È possibile aggiungere un prefisso prima del titolo per creare un titolo in due o tre parti. È possibile utilizzare una barra verticale o due punti come separatore alla fine del prefisso per differenziarlo dal testo del titolo principale. |
| [!UICONTROL Page Title Suffix] | Visualizzazione store | È possibile aggiungere un suffisso dopo il titolo per creare un titolo in due o tre parti. È possibile utilizzare una barra verticale o due punti come separatore alla fine del prefisso per differenziarlo dal testo del titolo principale. |
| [!UICONTROL Default Meta Description] | Visualizzazione store | La descrizione fornisce un riepilogo del sito per gli elenchi dei motori di ricerca e non può superare i 160 caratteri. |
| [!UICONTROL Default Meta Keywords] | Visualizzazione store | Una serie di parole chiave che descrivono il tuo archivio, ciascuna separata da una virgola. |
| [!UICONTROL Scripts and Style Sheets] | Visualizzazione store | Contiene gli script che devono essere inclusi nel HTML prima del tag di chiusura `<head>`. È ad esempio possibile immettere qui qualsiasi JavaScript di terze parti che deve essere inserito prima del tag `<body>`. |
| [!UICONTROL Display Demo Store Notice] | Visualizzazione store | Controlla la visualizzazione dell&#39;avviso dell&#39;archivio demo nella parte superiore della pagina. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## Intestazione

La configurazione dell’intestazione identifica il percorso del logo dell’archivio e specifica il testo alternativo del logo e il messaggio di benvenuto.

![Impostazioni di configurazione intestazione](./assets/configuration-header.png){width="400" zoomable="yes"}

### Configurare l’intestazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione archivio da configurare e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. In _Altre impostazioni_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Header]**.

1. Apporta le modifiche necessarie per la visualizzazione dello store:

   - Impostazioni [Logo](../getting-started/storefront-branding.md#upload-your-logo)
   - [Impostazioni del messaggio di benvenuto](../getting-started/storefront-branding.md#change-the-welcome-message)

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.

### Descrizioni dei campi dell’intestazione

| Campo | Ambito | Descrizione |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Visualizzazione store | Identifica il percorso del logo visualizzato nell&#39;intestazione. Tipi di file supportati: PNG, GIF, JPG JPEG |
| [!UICONTROL Logo Attribute Width] | Visualizzazione store | Larghezza dell&#39;immagine del logo in pixel. |
| [!UICONTROL Logo Attribute Height] | Visualizzazione store | Altezza dell&#39;immagine del logo in pixel. |
| [!UICONTROL Welcome Text] | Visualizzazione store | Il messaggio di benvenuto viene visualizzato nell’intestazione della pagina e include il nome dei clienti che hanno effettuato l’accesso. |
| [!UICONTROL Logo Image Alt] | Visualizzazione store | Testo Alt associato al logo. |
| [!UICONTROL Translate Title] | Visualizzazione store | Determina se tradurre `Page Title` o `Meta Title`. |

{style="table-layout:auto"}

## Piè di pagina

Nella sezione Configurazione piè di pagina è possibile aggiornare l&#39;[avviso di copyright](../getting-started/storefront-branding.md#change-the-copyright-notice) visualizzato nella parte inferiore della pagina e immettere script vari che devono essere posizionati prima del tag di chiusura `<body>`.

![Impostazioni configurazione piè di pagina](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Configurare il piè di pagina

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione archivio da configurare e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. In _Altre impostazioni_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Footer]**.

1. Apportare le modifiche necessarie alle impostazioni **[!UICONTROL Copyright]** e **[!UICONTROL Miscellaneous HTML]**.

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.

## Descrizioni dei campi piè di pagina

| Campo | Ambito | Descrizione |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Visualizzazione store | Una casella di input in cui è possibile caricare script vari nel server che devono essere inseriti immediatamente prima del tag di chiusura `<body>`. |
| [!UICONTROL Copyright] | Visualizzazione store | Dichiarazione di copyright visualizzata nella parte inferiore di ogni pagina. Per includere il simbolo di copyright, utilizzare l&#39;entità carattere HTML `\&copy;` come indicato di seguito: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Sostituire l&#39;avviso di copyright di esempio con il proprio. |
| [!UICONTROL Display Report Bugs Link] | Visualizzazione store | Determina se il collegamento al report di bug (supportato per alcuni temi) è abilitato o disabilitato. |

{style="table-layout:auto"}
