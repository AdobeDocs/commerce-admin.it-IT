---
title: Aggiungi ricerca registro regali
description: Scopri come inserire una casella di ricerca del registro dei regali per aiutare i visitatori a memorizzare i prodotti acquistati dai registri dei clienti.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# Aggiungi ricerca registro regali

{{ee-feature}}

Il [Widget](../content-design/widgets.md) può essere utilizzato per posizionare una casella di ricerca del registro di sistema di regali più ovunque nel tuo negozio. È possibile specificare le opzioni di ricerca disponibili per i clienti, ad esempio nome, indirizzo e-mail e ID registro regali. Quando il cliente fa clic sul pulsante Cerca, i risultati vengono visualizzati nella pagina Ricerca registro regali. Se la ricerca non restituisce alcun risultato, il cliente può riprovare con altri parametri.

![Esempio di vetrina: ricerca nel registro regali](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Configurare la ricerca nel Registro di sistema per i regali

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Widget]**.

1. Scegli la **[!UICONTROL Settings]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Type]** a `Gift Registry Search`.

   - Imposta **[!UICONTROL Design Theme]** al tema utilizzato dallo store.

   - Clic **[!UICONTROL Continue]**.

   ![Registro regali - Impostazioni di ricerca](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. In _[!UICONTROL Storefront Properties]_eseguire le operazioni seguenti:

   - Immetti un **[!UICONTROL Widget Title]** per riferimento interno.

   - Imposta **[!UICONTROL Assign to Store Views]** alle viste dello store in cui sarà disponibile la Ricerca nel Registro regali.

   - Imposta **[!UICONTROL Sort Order]** per determinare l’ordine di visualizzazione del blocco di ricerca del registro dei regali quando vi sono altri blocchi assegnati alla stessa posizione sulla pagina.

   ![Registro regali - proprietà vetrina](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. In **[!UICONTROL Layout Updates]** , fare clic su **[!UICONTROL Add Layout Update]**.

1. Per determinare la posizione in cui viene visualizzata la ricerca nel Registro regali, eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Display On]** alle pagine del Negozio in cui desideri visualizzare il blocco di ricerca del Registro dei regali.

   - Se applicabile, scegliere il **[!UICONTROL Categories]** dove desideri che appaia.

   - Imposta **[!UICONTROL Container]** nella posizione sulla pagina per inserire il blocco di ricerca del registro dei regali.

   ![Registro regali - Aggiornamenti del layout](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Per determinare in che modo i visitatori del sito possono cercare i registri delle donazioni, selezionare tutte le opzioni seguenti:

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Registro regali - opzioni widget](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache delle pagine, fai clic sul collegamento nel messaggio nella parte superiore dell’area di lavoro e segui le istruzioni.

## Descrizioni dei campi

### [!UICONTROL Settings]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Type] | Identifica `Gift Registry Search` come tipo di Widget. |
| [!UICONTROL Design Theme] | Tema utilizzato dall&#39;archivio in cui verrà visualizzata la ricerca nel Registro regali. |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Widget Title] | Nome per riferimento interno. |
| [!UICONTROL Assign to Store Views] | Identifica le visualizzazioni dello store in cui sarà disponibile la Ricerca nel Registro regali. |
| [!UICONTROL Sort Order] | Indica l’ordine di visualizzazione del blocco di ricerca del Registro dei regali se nella stessa posizione sono presenti altri blocchi assegnati. |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Display On] | Indica le pagine o i tipi di pagine specifici in cui viene visualizzato il blocco Ricerca registro regali. |
| [!UICONTROL Categories] | Se applicabile, identifica le pagine della categoria in cui viene visualizzata la Ricerca nel registro regali. |
| [!UICONTROL Container] | Indica il blocco di layout della pagina in cui viene inserita la ricerca nel Registro regali. Le opzioni variano in base al modello e al tema. |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | Determina i tipi di ricerche che possono essere eseguite con la Ricerca nel Registro regali. Opzioni: `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
