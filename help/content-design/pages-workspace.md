---
title: Controlli dell’area di lavoro pagina
description: Scopri gli strumenti di Workspace utilizzati per individuare e aggiornare le pagine di contenuto.
exl-id: c53e3e70-9f88-46ec-b44d-133a2ff5d0d5
feature: Page Content, Admin Workspace
source-git-commit: fc8ebeeae56378967e95bda9bbf898c469b3a4c0
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Controlli dell’area di lavoro pagina

L&#39;area di lavoro della pagina include strumenti che consentono di trovare rapidamente le pagine necessarie e comandi per eseguire la manutenzione ordinaria su una o più pagine. È inoltre possibile aggiornare rapidamente le proprietà della pagina dalla griglia.

![Griglia pagine](./assets/pages-grid.png){width="700" zoomable="yes"}

## Aggiorna rapidamente le proprietà della pagina

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.
1. Fare clic su una riga qualsiasi della griglia.

   ![Le proprietà della pagina sono modificabili nella griglia Pagine](./assets/page-grid-properties-update.png){width="600" zoomable="yes"}

   Per selezionare più record, selezionare la casella di controllo di ogni riga che si desidera aggiornare.

1. Aggiorna una delle seguenti proprietà:

   - **[!UICONTROL Title]**
   - **[!UICONTROL URL Key]**
   - **[!UICONTROL Status]**
   - **[!UICONTROL Layout]**

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Controlli Workspace

| Controllo | Descrizione |
|--- |--- |
| [!UICONTROL Add New Page] | Aggiunge una pagina. |
| [!UICONTROL Search] | Avvia una ricerca nel catalogo in base ai filtri correnti. |
| [!UICONTROL Actions] | Elenca tutte le azioni che possono essere applicate agli elementi selezionati nell&#39;elenco. Per applicare un&#39;azione a una pagina o a più pagine, selezionare la casella di controllo nella prima colonna di ogni record soggetto all&#39;azione. Opzioni: `Delete` / `Disable` / `Enable` / `Edit` |
| [!UICONTROL Select] | Il controllo nell&#39;intestazione della prima colonna può essere utilizzato per selezionare più record come destinazione dell&#39;azione. Selezionare la casella di controllo nella prima colonna di ogni record che si desidera selezionare. Opzioni: `Select All` / `Deselect All` |
| [!UICONTROL Save Edits] | Applica l&#39;azione corrente ai record selezionati. |
| [!UICONTROL Edit] | Apre il record in modalità di modifica. È possibile eseguire la stessa operazione facendo clic in un punto qualsiasi della riga. |

{style="table-layout:auto"}

## Colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Select] | La casella di controllo nella prima colonna viene utilizzata per selezionare più record. Opzioni: `Select All` / `Deselect All` |
| [!UICONTROL ID] | L’ID è un numero incrementale assegnato a ogni pagina. |
| [!UICONTROL Title] | Titolo visualizzato nella parte superiore della pagina. |
| [!UICONTROL URL Key] | La chiave URL è simile al nome di un file e identifica la pagina nell’URL. |
| [!UICONTROL Layout] | Determina se la pagina viene visualizzata con barre laterali a destra o a sinistra dell&#39;area del contenuto principale. Opzioni: `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Store View] | Utilizzato per associare la pagina a una visualizzazione specifica dello store. |
| [!UICONTROL Status] | Indica se la pagina è online o offline. Opzioni: `Enabled` / `Disabled` |
| [!UICONTROL Created] | Data di creazione della pagina. |
| [!UICONTROL Modified] | Data dell’ultima modifica apportata alla pagina. |
| [!UICONTROL Action] | Le azioni applicabili a un singolo record includono:<br/>**[!UICONTROL Edit]**- Apre la pagina in modalità di modifica.<br/>**[!UICONTROL Delete]** - Elimina la pagina.<br/>**[!UICONTROL View]**- Visualizza la pagina in modalità anteprima. |

{style="table-layout:auto"}

## Altre colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Custom design from/to] | Specifica la data di inizio e di fine in cui la struttura selezionata viene applicata alla pagina. ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source). |
| [!UICONTROL Custom Theme] | Applica un tema personalizzato alla pagina |
| [!UICONTROL Custom Layout] | Determina il layout personalizzato della pagina |
| [!UICONTROL Meta Title] | Titolo metadati per la pagina |
| [!UICONTROL Meta Keywords] | Parole chiave meta per la pagina |
| [!UICONTROL Meta Description] | La metadescrizione della pagina |

{style="table-layout:auto"}

## Ricerca pagina

È possibile utilizzare la casella di ricerca nella parte superiore sinistra della griglia _[!UICONTROL Pages]_per trovare pagine specifiche per parola chiave. Per una ricerca più avanzata, puoi [filtrare](../getting-started/admin-grid-controls.md) la ricerca per più parametri.

### Ricerca per parola chiave

1. Immetti un termine di ricerca nella casella di ricerca della pagina.

1. Per visualizzare i risultati, fare clic sull&#39;icona Cerca (![Icona Lente di ingrandimento](../assets/icon-magnify-search.png)).

   I risultati includono tutte le pagine che contengono la parola chiave.

### Filtrare i risultati della ricerca

1. Se necessario, fare clic su **[!UICONTROL Clear All]** per cancellare i criteri di ricerca precedenti.

1. Per visualizzare la selezione dei filtri di ricerca, fare clic su **[!UICONTROL Filters]** !Scheda ([Icona funnel](../assets/icon-filter-search.png)).

1. Completa tutti i filtri necessari per descrivere le pagine che desideri trovare.

1. Fare clic su **[!UICONTROL Apply Filters]** per visualizzare i risultati.

### Filtri di ricerca

| Filtro | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Filtra la ricerca per ID record pagina. |
| [!UICONTROL Title] | Filtra la ricerca in base al titolo della pagina. |
| [!UICONTROL URL Key] | Filtra la ricerca in base alla chiave URL. |
| [!UICONTROL Created] | Filtra la ricerca in base alla data di creazione della pagina. |
| [!UICONTROL Modified] | Filtra la ricerca in base alla data dell’ultima modifica apportata alla pagina. |
| [!UICONTROL Store View] | Filtra la ricerca in base alla vista Store. Opzioni: `All available` / `Store Views` |
| [!UICONTROL Layout] | Filtra la ricerca in base al layout della pagina. Opzioni: `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Status] | Filtra la ricerca in base allo stato della pagina. Opzioni: `Disabled` / `Published` |
| [!UICONTROL Custom design from / to] | Filtra la ricerca in base alla data di inizio e di fine quando il design selezionato viene applicato alla pagina. ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source). |
| [!UICONTROL Asset] | Filtrare la ricerca in base alle risorse del titolo della pagina |
| [!UICONTROL Custom Layout] | Filtra la ricerca in base a un layout personalizzato. Opzioni: `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` / `Page -- Full Width` / `Category -- Full Width` / `Product -- Full Width` |
| [!UICONTROL Custom Theme] | Filtra la ricerca in base a un tema personalizzato. Opzioni predefinite: `Magento Blank` / `Magento Luma` |
| [!UICONTROL Meta Keywords] | Filtra la ricerca in base alle parole chiave meta della pagina. |
| [!UICONTROL Meta Title] | Filtra la ricerca in base al titolo meta della pagina. |
| [!UICONTROL Meta Description] | Filtra la ricerca in base alla metadescrizione della pagina. |

{style="table-layout:auto"}

### Strumenti di ricerca

| Strumento | Descrizione |
|--- |--- |
| [!UICONTROL Apply Filters] | Applica tutti i filtri ai risultati della ricerca. |
| [!UICONTROL Cancel] | Annulla la ricerca corrente. |
| [!UICONTROL Clear All] | Cancella tutti i filtri di ricerca. |

{style="table-layout:auto"}

## Azioni pagina

Le pagine possono essere modificate, disattivate, attivate ed eliminate. Per applicare un&#39;azione a una singola pagina, seleziona la casella di controllo nella prima colonna. Per selezionare o deselezionare tutte le pagine, utilizzare il controllo di selezione nella parte superiore della colonna.

![Azioni pagina](./assets/pages-select.png){width="400" zoomable="yes"}

### Azione singola

Utilizza la colonna _[!UICONTROL Action]_all&#39;estrema destra per applicare una delle seguenti azioni alla singola pagina:

- [!UICONTROL Edit] - apre la pagina in modalità di modifica
- [!UICONTROL Delete] - elimina la pagina (richiede conferma)
- [!UICONTROL View] - apre una pagina direttamente nella vetrina

![Azioni a pagina singola](./assets/page-grid-actions.png){width="600" zoomable="yes"}

### Azioni di massa

Applica una delle azioni seguenti a più pagine selezionate contemporaneamente utilizzando il selettore _[!UICONTROL Action]_in alto a sinistra:

- [!UICONTROL Delete] - elimina le pagine (richiede conferma)
- [!UICONTROL Disable] - disabilita le pagine nella vetrina
- [!UICONTROL Enable] - abilita le pagine nella vetrina
- [!UICONTROL Edit] - apre le colonne nella griglia in modalità di modifica (**[!UICONTROL Title]**, **[!UICONTROL URL Key]**, **[!UICONTROL Layout]** e **[!UICONTROL Status]**)

## Layout griglia pagina

La selezione delle colonne e il relativo ordine nella griglia possono essere modificati in base alle preferenze dell&#39;utente. Per mantenere la nuova disposizione delle colonne, è possibile salvarla come vista.

### Modificare la selezione delle colonne

Nell&#39;angolo superiore destro fare clic sul controllo _Colonne_ (![Icona colonna](../assets/icon-columns.png)) ed eseguire le operazioni seguenti:

- Selezionare la casella di controllo delle colonne che si desidera aggiungere alla griglia.

- Deselezionare la casella di controllo delle colonne che si desidera rimuovere dalla griglia.

### Spostare una colonna

1. Fai clic sull’intestazione della colonna e tieni premuto.

1. Trascinare la colonna nella nuova posizione e rilasciare.

### Salvare una visualizzazione

1. Fare clic sul controllo _Visualizza_ (![Icona occhio](../assets/icon-view-eye.png)) e quindi su **[!UICONTROL Save View As]**.

1. Immettere un nome per la visualizzazione.

1. Per salvare la visualizzazione, fare clic sulla _freccia_ (![icona freccia](../assets/icon-arrow-save.png)).

   Il nome della vista viene ora visualizzato come vista corrente.

### Modificare la visualizzazione

Fare clic sul controllo _Visualizza_ (![Icona occhio](../assets/icon-view-eye.png)) ed eseguire una delle operazioni seguenti:

- Scegliere la visualizzazione che si desidera utilizzare.

- Modificare il nome di una visualizzazione facendo clic sull&#39;icona Modifica (![icona matita](../assets/icon-edit-pencil.png)) e aggiornando il nome.

  ![La visualizzazione salvata viene visualizzata nei controlli di visualizzazione con un&#39;icona di modifica](./assets/pages-default-grid-control.png){width="600" zoomable="yes"}

## Modifiche pianificate

{{ee-feature}}

Le modifiche apportate alla pagina possono essere applicate in base alla pianificazione e raggruppate con altre modifiche apportate al contenuto. Puoi creare una campagna in base alle modifiche pianificate per una pagina o applicare le modifiche a una campagna esistente. Per ulteriori informazioni, vedere [Gestione temporanea dei contenuti](content-staging.md).

Quando configuri le pianificazioni per le modifiche di pagina e le campagne di modifica, tieni presente quanto segue:

- Tutti gli aggiornamenti pianificati vengono applicati consecutivamente, il che significa che qualsiasi entità può avere un solo aggiornamento pianificato in un determinato punto. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere un aggiornamento pianificato diverso per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

- Se una campagna è collegata a più pagine, è possibile modificarla solo dal [dashboard di gestione temporanea dei contenuti](content-staging-dashboard.md).

- Se inizialmente viene creata una campagna attiva senza una data di fine, non è possibile modificarla in un secondo momento in modo da includere una data di fine. In tal caso, è necessario creare una campagna duplicata e immettere la data di fine necessaria.

- La data di inizio e la data di fine della campagna devono essere definite utilizzando il fuso orario di amministrazione **_predefinito_**, convertito dal fuso orario locale di ciascun sito Web. Prendi in considerazione un esempio in cui hai più siti web in fusi orari diversi, ma desideri avviare una campagna basata su un fuso orario negli Stati Uniti. In questo caso, è necessario pianificare un aggiornamento separato per ogni fuso orario locale e impostare **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** in convertiti da ogni fuso orario del sito Web locale al fuso orario predefinito dell&#39;amministratore.

- Puoi pianificare e visualizzare in anteprima le modifiche per gli aggiornamenti dei prodotti. Per ulteriori informazioni, vedere [Pianificazione di un aggiornamento](content-staging-scheduled-update.md).

>[!NOTE]
>
>La scheda [!UICONTROL Custom Design Update] è stata rimossa in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e non può essere modificata direttamente nella pagina. Devi creare un aggiornamento pianificato per queste attivazioni.

![Nella home page vengono visualizzate le modifiche pianificate nella parte superiore](./assets/page-scheduled-change.png){width="600" zoomable="yes"}

