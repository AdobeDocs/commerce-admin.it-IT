---
title: Visualizzazioni catalogo
description: Scopri cosa sono le visualizzazioni catalogo e come crearle per organizzare il catalogo dei prodotti in base alla struttura aziendale, alle politiche e ai prezzi.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo alle istanze Adobe Commerce as a Cloud Service con provisioning CCDM (infrastruttura SaaS gestita da Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# Visualizzazioni catalogo

Una vista catalogo definisce i prodotti e i prezzi che un negozio può recuperare. Nelle istanze as a Cloud Service di Adobe Commerce fornite con il modello dati di catalogo componibile (CCDM), le viste catalogo utilizzano la stessa base di catalogo che alimenta Adobe Commerce Optimizer.

Le viste catalogo combinano origini di catalogo, criteri e listini prezzi per definire il contesto del catalogo di una vetrina. I criteri determinano l’assortimento di prodotti disponibile. Le regole di merchandising controllano il modo in cui i prodotti all’interno di tale assortimento vengono promossi e classificati e possono essere applicate in tutte le visualizzazioni di catalogo o essere personalizzate per una visualizzazione specifica. Consulta [Creare una regola di merchandising](../merchandising/rules/add.md).

Commerce Foundation rimane la fonte di verità per prodotti e prezzi. I dati su prodotti e prezzi si sincronizzano in un solo modo con il CCDM attraverso l’integrazione nativa di Adobe Commerce as a Cloud Service, senza l’installazione di un connettore separato o l’app App Builder. La configurazione di siti Web, store e store-view rimane in Commerce Foundation, che gestisce anche il carrello, il pagamento, le promozioni, i clienti, gli ordini e i pagamenti.

>[!NOTE]
>
>Per le istanze con provisioning CCDM, utilizza [Amministratore Commerce in Adobe Unified Experience](../../getting-started/admin-unified-experience.md) per configurare le visualizzazioni e i criteri del catalogo e associare i listini prezzi sincronizzati alle visualizzazioni del catalogo. Le istanze che utilizzano Catalog Service con Live Search e Product Recommendations non hanno accesso a queste schermate di gestione del catalogo.

## Funzionamento delle visualizzazioni del catalogo

Una vista catalogo riunisce i dati e la configurazione del catalogo per un contesto storefront. Può essere utilizzato per rappresentare un’unità aziendale, un marchio, un’area geografica o un’altra esperienza di vetrina.

- **[Le origini del catalogo](catalog-sources.md)** forniscono dati di prodotto per le esperienze del catalogo.
- **[I criteri](policies.md)** filtrano i dati dei prodotti per una visualizzazione catalogo.
- **[I listini prezzi](pricebooks.md)** forniscono i dati relativi ai prezzi associati a una visualizzazione catalogo.

Le viste catalogo non sostituiscono la struttura del sito web, dello store e della vista store in Adobe Commerce as a Cloud Service. Commerce Foundation continua a gestire tale struttura e le operazioni transazionali.

I dati del catalogo vengono sincronizzati in un solo modo da Commerce Foundation a CCDM. CCDM supporta le esperienze di catalogo della vetrina e l’individuazione dei prodotti. Commerce Foundation continua a gestire carrello, pagamento, promozioni, clienti e ordini.

## Prima di iniziare

Prima di configurare una vista catalogo:

- [Verificare che l&#39;istanza di Adobe Commerce as a Cloud Service utilizzi CCDM](../overview.md).
- Verificare che i dati del catalogo necessari per la vetrina siano stati compilati e [sincronizzati](data-sync.md).
- Identifica l&#39;[origine catalogo](catalog-sources.md), i [criteri](policies.md) e i [listini prezzi](pricebooks.md) necessari per il contesto storefront.
- Determina se devi creare manualmente le viste del catalogo B2C o esaminare le viste del catalogo B2B generate dalla sincronizzazione nativa.

>[!NOTE]
>
>Per le implementazioni B2B, la sincronizzazione nativa genera viste di catalogo, criteri e listini prezzi dalla configurazione B2B in Commerce Foundation. Non creare manualmente duplicati di queste strutture generate automaticamente.

## Creare una vista catalogo per un’implementazione B2C

Utilizza questo flusso di lavoro quando l’implementazione B2C richiede che le viste catalogo siano configurate manualmente.

1. Accedi a [Amministratore Commerce in Unified Experience](../../getting-started/admin-unified-experience.md) e seleziona l&#39;istanza di Adobe Commerce as a Cloud Service con provisioning CCDM.
1. Nel menu di navigazione a sinistra, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**.
1. Selezionare **[!UICONTROL Create catalog view]**.
1. Immettere un nome per la vista catalogo.
1. Selezionare l&#39;[origine o le origini del catalogo](catalog-sources.md) per il contesto storefront.
1. Associa i [criteri](policies.md) pertinenti alla visualizzazione del catalogo.
1. Associare i listini prezzi pertinenti alla vista catalogo [configurando la disponibilità del listino prezzi](pricebooks.md).
1. Crea la vista catalogo.

## Visualizzazioni del catalogo B2B

Per le implementazioni B2B, la sincronizzazione nativa genera viste di catalogo, criteri e listini prezzi dalla configurazione B2B in Commerce Foundation. Gestisci il catalogo B2B sottostante e le relazioni aziendali in Commerce Foundation anziché creare manualmente strutture duplicate in CCDM.

Per le istruzioni di installazione, vedere [Creare un catalogo condiviso](../../b2b/catalog-shared-create.md) e [Assegnare società a un catalogo condiviso](../../b2b/catalog-shared-assign-companies.md).

Dopo aver configurato le relazioni B2B:

1. Conferma che [sincronizzazione](data-sync.md) è stata completata.
2. Esamina le visualizzazioni del catalogo generate, [criteri](policies.md) e [listini prezzi](pricebooks.md) in [Amministratore Commerce in Unified Experience](../../getting-started/admin-unified-experience.md).
3. Verifica che la vetrina mostri l&#39;assortimento di prodotti e i prezzi previsti per la società.
4. Test di componenti aggiuntivi per carrello, carrello e pagamento per verificare che la disponibilità del prodotto e i prezzi delle transazioni corrispondano alla configurazione B2B prevista.

## Listino prezzi e pagamento

I listini prezzi forniscono i dati di determinazione prezzi disponibili tramite una vista catalogo. In Adobe Commerce as a Cloud Service, Commerce Foundation rimane la fonte di verità per i prezzi e i dati di determinazione dei prezzi si sincronizzano con il CCDM tramite l&#39;integrazione nativa. Durante la configurazione di una vista catalogo, utilizzare i listini prezzi sincronizzati applicabili anziché creare in modo indipendente i prezzi in CCDM.

Per il carrello e il pagamento utilizzare i prezzi di Commerce Foundation. Verifica che i prezzi visualizzati nella vetrina corrispondano ai prezzi applicabili del carrello e del pagamento.

## Rivedere e convalidare una vista catalogo

Dopo aver configurato una vista catalogo, verifica l’esperienza della vetrina completa:

- Verificare che i dati del catalogo previsti siano [sincronizzati](data-sync.md).
- Conferma che la visualizzazione del catalogo sia associata ai [criteri](policies.md) e ai [listini prezzi](pricebooks.md) previsti.
- Verifica che la vetrina restituisca l’assortimento di prodotto previsto.
- Verificare i prezzi visualizzati rispetto ai prezzi corrispondenti di Commerce Foundation.
- Test di componenti aggiuntivi per il carrello, il carrello e il pagamento.

Per le implementazioni B2B, conferma anche che le strutture di catalogo generate dalla sincronizzazione corrispondano alla configurazione dell’azienda e del catalogo previsti.

## Risoluzione dei problemi

### Prodotti mancanti nella vetrina

- [Verificare che l&#39;istanza utilizzi CCDM](../overview.md).
- Verificare che i dati del catalogo siano [sincronizzati](data-sync.md).
- Verifica che la vetrina utilizzi il contesto del catalogo previsto.
- Esamina i [criteri](policies.md) associati alla visualizzazione del catalogo.

### Prezzo visualizzato imprevisto

- Verificare che il [listino prezzi dedicato](pricebooks.md) sia associato alla visualizzazione del catalogo.
- Verificare che i dati relativi al prezzo siano [sincronizzati](data-sync.md) e coerenti con Commerce Foundation.

  Consulta [Listini prezzi](pricebooks.md) per il sito Web e le mappature dei prezzi per gruppo di clienti.

- Convalida di nuovo il prezzo nel carrello ed effettua il pagamento.

### Le schermate del catalogo CCDM non sono visibili in Commerce Admin

[Conferma che l&#39;istanza selezionata utilizza CCDM](../overview.md) e che stai accedendo a [Commerce Admin in Unified Experience](../../getting-started/admin-unified-experience.md). Un&#39;istanza che esegue Catalog Services v1 non dispone delle schermate di amministrazione CCDM.

## Contenuto correlato

- [Guida introduttiva ad Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/getting-started)
- [Panoramica del catalogo condiviso B2B di Adobe Commerce](../../b2b/catalog-shared.md)
- [Note sulla versione di Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/release-notes)
- [Sincronizzazione catalogo](data-sync.md)
