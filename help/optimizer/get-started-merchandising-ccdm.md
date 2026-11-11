---
title: Attività Catalogo merchandising per ruolo
description: Trova le linee guida per amministratori, sviluppatori e merchandiser che lavorano con le istanze di Adobe Commerce as a Cloud Service fornite con CCDM.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo alle istanze Adobe Commerce as a Cloud Service con provisioning CCDM (infrastruttura SaaS gestita da Adobe)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# Attività di merchandising catalogo per ruolo

Utilizza questo riferimento alle attività per trovare indicazioni per configurare i dati del catalogo, integrare la vetrina, gestire il merchandising e rivedere le prestazioni nelle istanze di Adobe Commerce as a Cloud Service fornite con il provisioning Composable Catalog Data Model (CCDM).

Le responsabilità variano a seconda dell&#39;implementazione. Nelle sezioni seguenti le attività vengono raggruppate in base ai ruoli che in genere le eseguono.

- Gli amministratori gestiscono prodotti, prezzi e configurazione B2B in Commerce Foundation.
- Gli sviluppatori configurano l’integrazione storefront e verificano le richieste del catalogo e la raccolta di dati comportamentali.
- I commercianti configurano l’individuazione dei prodotti e i consigli e utilizzano il reporting per prendere decisioni informate sul merchandising.

I dati su prodotti e prezzi vengono sincronizzati con il CCDM tramite l’integrazione nativa di Adobe Commerce as a Cloud Service. Non è necessaria alcuna installazione separata del connettore o dell’app App Builder.

## Preparare il catalogo e la vetrina

Completa le attività applicabili all’implementazione. Le viste del catalogo B2C possono essere create manualmente. Le viste del catalogo B2B, i criteri e i listini prezzi vengono generati dalla configurazione B2B in Commerce Foundation.

| Attività | Descrizione | Risorse |
| --- | --- | --- |
| **Configura prodotti e prezzi** | Gestisci prodotti e prezzi in Commerce Foundation. I dati di determinazione prezzi vengono sincronizzati con il modello CCDM come listini prezzi. Non creare i prezzi in modo indipendente in CCDM. | [Elenco prodotti](../catalog/products-list.md), [Crea un prodotto](../catalog/product-create.md), [Ambito prezzo](../catalog/catalog-price-scope.md) e [Prezzi avanzati](../catalog/pricing-advanced.md) |
| **Configurare le visualizzazioni dello store** | Configura le viste store e i dati localizzati dei prodotti richiesti per la vetrina in Commerce Foundation. | [Visualizzazioni store](../stores-purchase/store-views.md) |
| **Configurare cataloghi e società condivisi B2B** | Per le implementazioni B2B, configura cataloghi condivisi e relazioni aziendali in Commerce Foundation prima di rivedere la configurazione del catalogo generato. | [Cataloghi condivisi](../b2b/catalog-shared.md) e [Aziende](../b2b/account-companies.md) |
| **Configurare le visualizzazioni e i criteri del catalogo B2C** | Crea viste catalogo e seleziona i criteri che definiscono l’assortimento di prodotti disponibile. Associare i listini prezzi sincronizzati applicabili a ogni visualizzazione. | [Visualizzazioni catalogo](./setup/catalog-view.md) |
| **Rivedi le visualizzazioni del catalogo B2B** | Verificare che la sincronizzazione nativa abbia generato le visualizzazioni di catalogo, i criteri e i listini prezzi previsti. Gestisci la configurazione B2B sottostante in Commerce Foundation anziché creare manualmente strutture duplicate. | [Visualizzazioni catalogo B2B](./setup/catalog-view.md#b2b-catalog-views) |
| **Configura la vetrina** | Configura la vetrina per richiedere il contesto del catalogo previsto. Per integrazioni personalizzate o di altro tipo nella vetrina, controlla le intestazioni di richiesta del catalogo applicabili. | [Configurazione vetrina](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

Prima di configurare il merchandising, verifica che la vetrina restituisca i prodotti e i prezzi previsti. Test del componente aggiuntivo al carrello, del carrello e del pagamento per verificare che i prezzi delle transazioni corrispondano alla configurazione di Commerce Foundation prevista.

## Configurare le prestazioni di merchandising e revisione

| Attività | Descrizione | Risorse |
| --- | --- | --- |
| **Configura individuazione prodotto** | Imposta regole di merchandising, facet e sinonimi. Le regole possono essere applicate a tutte le visualizzazioni di catalogo o personalizzate per una visualizzazione specifica. | [Panoramica sul merchandising](./merchandising/overview.md) |
| **Verifica impostazioni di ricerca** | Esamina la configurazione di ricerca e le opzioni di ricerca semantica disponibili per l’implementazione. | [Impostazioni merchandising](./settings.md) e [Ricerca semantica](./setup/semantic-search.md) |
| **Configura consigli** | Crea unità di consigli e verifica che la vetrina raccolga i dati comportamentali richiesti dall&#39;implementazione. | [Panoramica sui consigli](./merchandising/recommendations/overview.md) |
| **Verifica prestazioni** | Utilizza le metriche di successo e i rapporti sulle prestazioni delle ricerche per valutare l’attività della vetrina e orientare le decisioni di merchandising. | [Metriche di successo](./manage-results/success-metrics.md) e [Prestazioni di ricerca](./manage-results/search-performance.md) |

## Passaggi successivi

Dopo aver configurato il merchandising e aver esaminato le prestazioni, continua a monitorare e regolare le regole, i facet e i consigli in base alle esigenze per ottimizzare l’esperienza della vetrina.
