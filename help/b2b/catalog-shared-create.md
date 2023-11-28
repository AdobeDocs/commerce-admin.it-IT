---
title: Creare un catalogo condiviso
description: Scopri come creare cataloghi condivisi e duplicare quelli esistenti.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Creare un catalogo condiviso

Quando un [catalogo condiviso](catalog-shared.md) viene creata automaticamente una [gruppo di clienti](account-company-customer-group.md) con lo stesso nome. Ad esempio, se crei un catalogo condiviso denominato _Catalogo ABC_, il sistema crea anche un _Catalogo ABC_ gruppo di clienti. L’assegnazione di un’azienda al catalogo personalizzato condiviso è fondamentalmente identica all’assegnazione a un gruppo di clienti.

Un nuovo catalogo condiviso non include prodotti, prezzi personalizzati o associazioni aziendali. Un catalogo pubblico, che è il catalogo condiviso predefinito creato quando i cataloghi condivisi sono abilitati, viene assegnato automaticamente agli ospiti e ai clienti che non sono associati a una società.

![Cataloghi condivisi](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Prima di poter utilizzare un catalogo condiviso, è necessario configurarne i seguenti aspetti:

- Ambito del catalogo
- Selezione del prodotto
- Prezzi personalizzati
- Assegnazioni società

## Limite di prezzo

Se hai un’installazione multisito, assicurati di configurare l’ambito del prezzo prima di creare i cataloghi condivisi. Il [ambito del prezzo](../catalog/catalog-price-scope.md) può essere impostato su `Global` o `Website`. Tuttavia, può essere impostato solo all&#39;inizio del processo di configurazione. Il selettore del sito web viene visualizzato durante il passaggio 2 della [impostazione catalogo condiviso](catalog-shared-pricing-structure.md).

![Selettore siti Web](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **Catalogo** e scegli **Catalogo** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **Prezzo** sezione.

1. Imposta **Ambito prezzo catalogo** a `Website`.

   ![Ambito prezzo catalogo](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

## Passaggio 1: creare il catalogo condiviso

Esistono due modi per creare un catalogo condiviso. Puoi creare un catalogo condiviso di qualsiasi tipo o duplicare un catalogo condiviso esistente. Un nuovo catalogo condiviso non include prodotti e non è ancora assegnato a un’azienda.

### Metodo 1: aggiunta di un nuovo catalogo condiviso

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Shared Catalog]** ed effettuare le seguenti operazioni:

   - Immetti un **[!UICONTROL Name]** per il catalogo condiviso.

     Il nome assegnato viene utilizzato in tutta la dashboard dell’amministratore e del cliente, se applicabile, per fare riferimento al catalogo condiviso. Diventa anche il nome del gruppo di clienti corrispondente.

   - Seleziona **[!UICONTROL Type]** : `Custom` o `Public`.

   - Scegli la scheda appropriata **[!UICONTROL Customer Tax Class]** questo vale per gli acquisti effettuati dal catalogo condiviso.

     Per ulteriori informazioni sull&#39;impostazione e la definizione delle classi di imposta, vedere [Classi di imposta](../stores-purchase/tax-class.md).

     L’esempio seguente mostra un nuovo catalogo personalizzato per un cliente all’ingrosso specifico.

     ![Nuovo catalogo condiviso](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Invio **[!UICONTROL Description]**

1. Al termine, fai clic su **[!UICONTROL Save]**.

   Il nuovo catalogo viene visualizzato nel _[!UICONTROL Shared Catalogs]_griglia.

### Metodo 2: duplicare un catalogo condiviso esistente

Un catalogo personalizzato duplicato mantiene il modello di prezzo e la struttura dell&#39;originale, ma non le associazioni aziendali. Viene creato anche un gruppo di clienti corrispondente con lo stesso nome del catalogo duplicato. Per impostazione predefinita, un catalogo duplicato è denominato _Duplicato di_ il catalogo originale.

Se viene duplicato un catalogo condiviso pubblico, il tipo del catalogo duplicato diventa `custom`.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso nella griglia che si desidera duplicare, passare alla **[!UICONTROL Action]** e seleziona **[!UICONTROL General Settings]**.

1. Nelle opzioni nella parte superiore della pagina, fai clic su **[!UICONTROL Duplicate]**.

   ![Duplica catalogo condiviso](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Aggiorna i campi seguenti per il nuovo catalogo:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Al termine, fai clic su **[!UICONTROL Save]**.

   Il duplicato viene visualizzato nel _[!UICONTROL Shared Catalogs]_grid, con un ID univoco.

## Passaggio 2: completare la configurazione

Dopo aver creato un nuovo catalogo condiviso, questo deve essere configurato con la selezione di prodotti appropriata, [assegnazioni società](catalog-shared-assign-companies.md), e [autorizzazioni categoria](../catalog/category-permissions.md). Per continuare, vedi [Imposta prezzi e struttura](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[Versione 1.3.0 di B2B](release-notes.md#b2b-v130) e versioni successive** — Quando si crea un catalogo condiviso, ogni [autorizzazione categoria](../catalog/category-permissions.md) per il catalogo è impostato su _[!UICONTROL Allow for the Display Product Prices]_e_[!UICONTROL Add to Cart]_ per i gruppi di clienti a cui viene assegnato questo accesso nelle impostazioni di autorizzazione per il catalogo. In precedenza, queste impostazioni venivano impostate automaticamente su `Deny` anche quando le autorizzazioni del catalogo sono state impostate su `Allow`.

## Demo del catalogo condiviso

Per vedere una dimostrazione della gestione del catalogo condiviso, guarda questo video:

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## Riferimento pagina di catalogo condiviso

### Barra dei pulsanti

| Pulsante | Descrizione |
|--- |--- |
| [!UICONTROL Back] | Torna alla pagina Cataloghi condivisi senza salvare il nuovo catalogo condiviso. |
| [!UICONTROL Reset] | Cancella la forma di eventuali modifiche non salvate e ripristina le informazioni di dettaglio del catalogo originale. |
| [!UICONTROL Save and Continue Edit] | Salva tutte le modifiche e mantiene aperta la maschera in modalità di modifica. |
| [!UICONTROL Save] | Salva le modifiche, chiude il modulo e torna alla pagina Cataloghi condivisi. |

{style="table-layout:auto"}

### Dettagli catalogo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Name] | Identifica il catalogo condiviso in Admin (Amministrazione) e negli account cliente in cui è disponibile. Il nome del catalogo deve essere descrittivo e non deve superare i 32 caratteri. Non è possibile avere due cataloghi condivisi con lo stesso nome. Massimo caratteri: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica un catalogo con prezzi personalizzati che è disponibile solo per le società specifiche a cui è assegnato.<br/>**[!UICONTROL Public]**: identifica il catalogo condiviso disponibile per tutti i visitatori ospiti e per i clienti connessi che non sono associati a un’azienda. Quando si crea un catalogo condiviso pubblico predefinito [!DNL B2B for Adobe Commerce] è installato, ma deve essere configurato da un amministratore di archivio. Può esistere un solo catalogo condiviso pubblico alla volta. |
| [!UICONTROL Customer Tax Class] | Determina la classe di imposta utilizzata per gli acquisti effettuati dal catalogo. Le opzioni includono tutte le classi di imposta disponibili. |
| [!UICONTROL Description] | Breve spiegazione di come utilizzare il catalogo. |

{style="table-layout:auto"}

### Colonne griglia

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Identificatore numerico univoco assegnato all’entità di catalogo condiviso. |
| [!UICONTROL Name] | Nome del catalogo condiviso. |
| [!UICONTROL Type] | Indica il tipo di catalogo condiviso. Può essere `Public` o `Custom`. |
| [!UICONTROL Created At] | La data in cui il catalogo condiviso è stato creato nel sistema. |
| [!UICONTROL Created By] | Nome dell&#39;utente amministratore che ha creato un catalogo condiviso. |
| [!UICONTROL Action] | L’elenco delle azioni. Opzioni: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
