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

La pagina _[!UICONTROL Shared Catalogs]_&#x200B;fornisce l&#39;accesso agli strumenti necessari per la gestione dei cataloghi condivisi. La pagina è simile all’area di lavoro Amministratore standard, con filtri e controlli delle azioni. Nella griglia sono elencati tutti i cataloghi condivisi, incluso il catalogo condiviso pubblico predefinito e tutti i cataloghi personalizzati impostati.

## Aggiornare la selezione del prodotto

La selezione dei prodotti in qualsiasi catalogo condiviso può essere facilmente aggiornata dalla colonna _[!UICONTROL Action]_&#x200B;della griglia dei cataloghi condivisi. Le modifiche apportate sono visibili ai membri di qualsiasi account aziendale associato. Il processo è essenzialmente uguale alla scelta dei prodotti per una nuova [struttura catalogo](catalog-shared-pricing-structure.md), con la differenza che l&#39;ambito della configurazione non può essere modificato.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso nella griglia, passare alla colonna **[!UICONTROL Action]** e selezionare **[!UICONTROL Set Pricing and Structure]**.

   ![Griglia del catalogo condiviso e menu azioni](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Segui le istruzioni in [Passaggio 2: Scegli i prodotti](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   È possibile ignorare il primo elemento perché l&#39;ambito di un catalogo condiviso non può essere modificato dopo il primo salvataggio.

Se si utilizza un prodotto specifico, nella sezione _[!UICONTROL Products In Shared Catalog]_&#x200B;sono elencati tutti i cataloghi condivisi in cui il prodotto è disponibile. Per ulteriori informazioni, consulta [Aggiungere prodotti a un catalogo condiviso](catalog-shared-product-add.md).

![Prodotto in cataloghi condivisi](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Aggiorna prezzi personalizzati

I prezzi personalizzati dei prodotti in qualsiasi catalogo condiviso possono essere facilmente aggiornati dalla colonna Azione della griglia Cataloghi condivisi. Le modifiche apportate sono visibili nella vetrina ai membri della società o del gruppo di clienti associato. Il processo è essenzialmente identico all&#39;impostazione di prezzi personalizzati per un nuovo [catalogo condiviso](catalog-shared-pricing-structure.md), con la differenza che non è possibile modificare l&#39;ambito della configurazione.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso nella griglia da aggiornare, passare alla colonna **[!UICONTROL Action]** e selezionare **[!UICONTROL Set Pricing and Structure]**.

1. Nella pagina _[!UICONTROL Catalog Structure]_, fare clic su **[!UICONTROL Configure]**&#x200B;ed eseguire una delle operazioni seguenti:

   - Nell&#39;indicatore di avanzamento nella parte superiore della pagina fare clic su **[!UICONTROL Pricing]**.
   - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Next]**.

1. Segui le istruzioni in [Passaggio 3: imposta prezzi personalizzati](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Aggiorna autorizzazioni categoria

[Le autorizzazioni per le categorie](../catalog/category-permissions.md) vengono impostate automaticamente su `Allow` per i prodotti aggiunti dalla struttura ad albero delle categorie a un catalogo condiviso. In seguito puoi modificare le autorizzazioni o creare regole aggiuntive, in base alle esigenze.

>[!NOTE]
>
>**[Versione B2B 1.3.0](release-notes.md#b2b-v130) e successiva** — Quando si crea un catalogo condiviso, ogni [autorizzazione di categoria](../catalog/category-permissions.md) per il catalogo è impostata su `Allow` per _[!UICONTROL Display Product Prices]_&#x200B;e&#x200B;_[!UICONTROL Add to Cart]_ per i gruppi di clienti a cui viene assegnato questo accesso nelle impostazioni delle autorizzazioni del catalogo. In precedenza, queste impostazioni venivano impostate automaticamente su `Deny` anche quando le autorizzazioni del catalogo erano impostate su `Allow`.

>[!IMPORTANT]
>
>Tutte le [impostazioni delle autorizzazioni di gruppo](../configuration-reference/catalog/catalog.md#category-permissions) esistenti vengono ignorate da **_tutte_** categorie nel catalogo quando la funzionalità **_[!UICONTROL Shared Catalog]_** è abilitata. [!UICONTROL Shared Catalog] controlla completamente tutte le autorizzazioni di categoria nel catalogo quando è abilitato.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la categoria dei prodotti da aggiornare.

   Per includere tutti i prodotti, selezionare la categoria di livello superiore nella struttura.

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Category Permissions]**.

1. Fare clic su **[!UICONTROL New Permission]** ed effettuare le seguenti operazioni:

   ![Nuova autorizzazione](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Scegliere il **[!UICONTROL Customer Group]** che corrisponde al catalogo condiviso e modificare le impostazioni delle autorizzazioni in base alle esigenze.

     ![Regola autorizzazioni categoria](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Per creare una regola di autorizzazioni per un altro gruppo di clienti, fare clic su **[!UICONTROL New Permissions]** e ripetere il processo.

   - Per eliminare una regola di autorizzazione, fare clic sull&#39;icona _Elimina_ ![Cestino](../assets/icon-delete-trashcan-solid.png).

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Aggiorna i dettagli del catalogo

Le informazioni dettagliate di qualsiasi catalogo condiviso possono essere facilmente aggiornate dalla colonna Azione della griglia Cataloghi condivisi. Le modifiche apportate vengono applicate a tutti gli account società associati.

![Impostazioni generali](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Per il catalogo condiviso da aggiornare, passare alla colonna **[!UICONTROL Action]** e selezionare **[!UICONTROL General Settings]**.

   ![Dettagli catalogo](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Aggiorna le informazioni di dettaglio del catalogo in base alle esigenze.

   - La modifica del nome di un catalogo condiviso comporta anche la modifica del nome del gruppo di clienti corrispondente.
   - Se si modifica il tipo di catalogo da `Custom` a `Public`, il catalogo pubblico esistente verrà convertito in un catalogo personalizzato. Tutte le aziende associate al catalogo pubblico originale vengono riassegnate al sostituto. Impossibile convertire un catalogo pubblico in un catalogo personalizzato.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Riferimento pagina di catalogo condiviso

### Barra dei pulsanti

| Pulsante | Descrizione |
|--- |--- |
| [!UICONTROL Back] | Torna alla pagina Cataloghi condivisi senza salvare il nuovo catalogo condiviso. |
| [!UICONTROL Delete] | Elimina il catalogo e riassegna tutte le società associate e i relativi membri al catalogo condiviso pubblico. |
| [!UICONTROL Reset] | Cancella la forma di eventuali modifiche non salvate e ripristina le informazioni di dettaglio del catalogo originale. |
| [!UICONTROL Duplicate] | Crea una [copia duplicata del catalogo](catalog-shared-create.md). Per un catalogo personalizzato, il modello di prezzo e la struttura dell&#39;originale, ma senza le associazioni aziendali. Se viene duplicato un catalogo condiviso pubblico, il tipo del catalogo duplicato diventa `custom`. Viene creato anche un gruppo di clienti corrispondente con lo stesso nome del catalogo duplicato. Per impostazione predefinita, un catalogo duplicato è denominato _Duplicato di_ il catalogo originale. |
| [!UICONTROL Save and Continue Edit] | Salva tutte le modifiche e mantiene aperta la maschera in modalità di modifica. |
| [!UICONTROL Save] | Salva le modifiche, chiude il modulo e torna alla pagina Cataloghi condivisi. |

{style="table-layout:auto"}

### Dettagli catalogo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Name] | Identifica il catalogo condiviso in Admin (Amministrazione) e negli account cliente in cui è disponibile. Il nome del catalogo deve essere descrittivo e non deve superare i 32 caratteri. Non è possibile avere due cataloghi condivisi con lo stesso nome. Massimo caratteri: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica un catalogo con prezzi personalizzati che è disponibile solo per le società specifiche a cui è assegnato.<br/>**[!UICONTROL Public]**- Identifica il catalogo condiviso disponibile per tutti i visitatori ospiti e per i clienti connessi che non sono associati a un&#39;azienda. Al momento dell’installazione di Adobe Commerce B2B viene creato un catalogo condiviso pubblico &quot;predefinito&quot;, che deve tuttavia essere configurato dall’amministratore. Può esistere un solo catalogo condiviso pubblico alla volta. |
| [!UICONTROL Customer Tax Class] | Determina la classe di imposta utilizzata per gli acquisti effettuati dal catalogo. Le opzioni includono tutte le classi di imposta disponibili. |
| [!UICONTROL Description] | Breve spiegazione di come utilizzare il catalogo. |

{style="table-layout:auto"}
