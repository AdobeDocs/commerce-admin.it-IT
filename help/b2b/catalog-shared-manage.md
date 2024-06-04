---
title: Gestire i cataloghi condivisi
description: Scopri le informazioni e gli strumenti disponibili nella pagina Cataloghi condivisi.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Gestire i cataloghi condivisi

Il _[!UICONTROL Shared Catalogs]_fornisce accesso agli strumenti necessari per la gestione dei cataloghi condivisi. La pagina è simile all’area di lavoro Amministratore standard, con filtri e controlli delle azioni. Nella griglia sono elencati tutti i cataloghi condivisi, incluso il catalogo condiviso pubblico predefinito e tutti i cataloghi personalizzati impostati.

## Aggiornare la selezione del prodotto

La selezione dei prodotti in qualsiasi catalogo condiviso può essere facilmente aggiornata dalla sezione _[!UICONTROL Action]_della griglia dei cataloghi condivisi. Le modifiche apportate sono visibili ai membri di qualsiasi account aziendale associato. Il processo è essenzialmente lo stesso della scelta dei prodotti per un nuovo [struttura del catalogo](catalog-shared-pricing-structure.md), ad eccezione del fatto che l’ambito della configurazione non può essere modificato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso nella griglia, vai al **[!UICONTROL Action]** e seleziona **[!UICONTROL Set Pricing and Structure]**.

   ![Griglia del catalogo condiviso e menu delle azioni](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Segui le istruzioni in [Passaggio 2: scegliere i prodotti](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   È possibile ignorare il primo elemento perché l&#39;ambito di un catalogo condiviso non può essere modificato dopo il primo salvataggio.

Se utilizzi un prodotto specifico, il _[!UICONTROL Products In Shared Catalog]_sezione elenca ogni catalogo condiviso in cui il prodotto è disponibile. Per ulteriori informazioni, consulta [Aggiungere prodotti a un catalogo condiviso](catalog-shared-product-add.md).

![Prodotto in cataloghi condivisi](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Aggiorna prezzi personalizzati

I prezzi personalizzati dei prodotti in qualsiasi catalogo condiviso possono essere facilmente aggiornati dalla colonna Azione della griglia Cataloghi condivisi. Le modifiche apportate sono visibili nella vetrina ai membri della società o del gruppo di clienti associato. Il processo è essenzialmente lo stesso dell&#39;impostazione di prezzi personalizzati per un nuovo [catalogo condiviso](catalog-shared-pricing-structure.md), ad eccezione del fatto che l’ambito della configurazione non può essere modificato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso nella griglia che si desidera aggiornare, passare alla **[!UICONTROL Action]** e seleziona **[!UICONTROL Set Pricing and Structure]**.

1. Il giorno _[!UICONTROL Catalog Structure]_pagina, fai clic su **[!UICONTROL Configure]**ed effettuare una delle seguenti operazioni:

   - Nell’indicatore di avanzamento nella parte superiore della pagina, fai clic su **[!UICONTROL Pricing]**.
   - Nell’angolo superiore destro, fai clic su **[!UICONTROL Next]**.

1. Segui le istruzioni in [Passaggio 3: impostare i prezzi personalizzati](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Aggiorna autorizzazioni categoria

[Autorizzazioni categoria](../catalog/category-permissions.md) sono impostate automaticamente su `Allow` per i prodotti che vengono aggiunti dalla struttura ad albero delle categorie a un catalogo condiviso. In seguito puoi modificare le autorizzazioni o creare regole aggiuntive, in base alle esigenze.

>[!NOTE]
>
>**[Versione 1.3.0 di B2B](release-notes.md#b2b-v130) e versioni successive** — Quando si crea un catalogo condiviso, ogni [autorizzazione categoria](../catalog/category-permissions.md) per il catalogo è impostato su `Allow` per _[!UICONTROL Display Product Prices]_e_[!UICONTROL Add to Cart]_ per i gruppi di clienti a cui viene assegnato questo accesso nelle impostazioni di autorizzazione per il catalogo. In precedenza, queste impostazioni venivano impostate automaticamente su `Deny` anche quando le autorizzazioni del catalogo sono state impostate su `Allow`.

>[!IMPORTANT]
>
>Tutti gli esistenti [impostazioni delle autorizzazioni del gruppo](../configuration-reference/catalog/catalog.md#category-permissions) vengono ignorati da **_tutto_** categorie nel catalogo quando **_[!UICONTROL Shared Catalog]_** la funzione è abilitata. [!UICONTROL Shared Catalog] controlla completamente tutte le autorizzazioni di categoria nel catalogo quando questo è abilitato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la categoria dei prodotti da aggiornare.

   Per includere tutti i prodotti, selezionare la categoria di livello superiore nella struttura.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Category Permissions]** sezione.

1. Clic **[!UICONTROL New Permission]** ed effettuare le seguenti operazioni:

   ![Nuova autorizzazione](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Scegli la **[!UICONTROL Customer Group]** che corrisponde al catalogo condiviso e modifica le impostazioni delle autorizzazioni in base alle esigenze.

     ![Regola di autorizzazioni per categoria](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Per creare una regola di autorizzazioni per un altro gruppo di clienti, fai clic su **[!UICONTROL New Permissions]** e ripetere il processo.

   - Per eliminare una regola di autorizzazione, fai clic su _Elimina_ ![Cestino](../assets/icon-delete-trashcan-solid.png) icona.

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Aggiorna i dettagli del catalogo

Le informazioni dettagliate di qualsiasi catalogo condiviso possono essere facilmente aggiornate dalla colonna Azione della griglia Cataloghi condivisi. Le modifiche apportate vengono applicate a tutti gli account società associati.

![Impostazioni generali](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso che desideri aggiornare, vai al **[!UICONTROL Action]** e seleziona **[!UICONTROL General Settings]**.

   ![Dettagli catalogo](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Aggiorna le informazioni di dettaglio del catalogo in base alle esigenze.

   - La modifica del nome di un catalogo condiviso comporta anche la modifica del nome del gruppo di clienti corrispondente.
   - Modifica del tipo di catalogo da `Custom` a `Public` converte il catalogo pubblico esistente in un catalogo personalizzato. Tutte le aziende associate al catalogo pubblico originale vengono riassegnate al sostituto. Impossibile convertire un catalogo pubblico in un catalogo personalizzato.

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Riferimento pagina di catalogo condiviso

### Barra dei pulsanti

| Pulsante | Descrizione |
|--- |--- |
| [!UICONTROL Back] | Torna alla pagina Cataloghi condivisi senza salvare il nuovo catalogo condiviso. |
| [!UICONTROL Delete] | Elimina il catalogo e riassegna tutte le società associate e i relativi membri al catalogo condiviso pubblico. |
| [!UICONTROL Reset] | Cancella la forma di eventuali modifiche non salvate e ripristina le informazioni di dettaglio del catalogo originale. |
| [!UICONTROL Duplicate] | Crea un [copia duplicata del catalogo](catalog-shared-create.md). Per un catalogo personalizzato, il modello di prezzo e la struttura dell&#39;originale, ma senza le associazioni aziendali. Se viene duplicato un catalogo condiviso pubblico, il tipo del catalogo duplicato diventa `custom`. Viene creato anche un gruppo di clienti corrispondente con lo stesso nome del catalogo duplicato. Per impostazione predefinita, un catalogo duplicato è denominato _Duplicato di_ il catalogo originale. |
| [!UICONTROL Save and Continue Edit] | Salva tutte le modifiche e mantiene aperta la maschera in modalità di modifica. |
| [!UICONTROL Save] | Salva le modifiche, chiude il modulo e torna alla pagina Cataloghi condivisi. |

{style="table-layout:auto"}

### Dettagli catalogo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Name] | Identifica il catalogo condiviso in Admin (Amministrazione) e negli account cliente in cui è disponibile. Il nome del catalogo deve essere descrittivo e non deve superare i 32 caratteri. Non è possibile avere due cataloghi condivisi con lo stesso nome. Massimo caratteri: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica un catalogo con prezzi personalizzati che è disponibile solo per le società specifiche a cui è assegnato.<br/>**[!UICONTROL Public]**: identifica il catalogo condiviso disponibile per tutti i visitatori ospiti e per i clienti connessi che non sono associati a un’azienda. Al momento dell’installazione di Adobe Commerce B2B viene creato un catalogo condiviso pubblico &quot;predefinito&quot;, che deve tuttavia essere configurato dall’amministratore. Può esistere un solo catalogo condiviso pubblico alla volta. |
| [!UICONTROL Customer Tax Class] | Determina la classe di imposta utilizzata per gli acquisti effettuati dal catalogo. Le opzioni includono tutte le classi di imposta disponibili. |
| [!UICONTROL Description] | Breve spiegazione di come utilizzare il catalogo. |

{style="table-layout:auto"}
