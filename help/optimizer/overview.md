---
title: Panoramica dei servizi di merchandising
description: Scopri gli strumenti di configurazione del catalogo, merchandising, reporting e monitoraggio per le istanze as a Cloud Service di Adobe Commerce fornite con CCDM.
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo alle istanze Adobe Commerce as a Cloud Service con provisioning CCDM (infrastruttura SaaS gestita da Adobe)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# Panoramica di Merchandising Services con CCDM

Le istanze as a Cloud Service di Adobe Commerce fornite con il modello dati catalogo componibile (CCDM) forniscono strumenti di configurazione, merchandising, reporting e monitoraggio del catalogo in [Amministratore Commerce in Adobe Unified Experience](../getting-started/admin-unified-experience.md). Il CCDM è la stessa base di catalogo che alimenta Adobe Commerce Optimizer.

Con i servizi di merchandising è possibile:

- Utilizza i dati del catalogo dalla tua istanza di Adobe Commerce as a Cloud Service per supportare le esperienze della vetrina.
- Configura le viste e i criteri del catalogo per definire gli assortimenti di prodotti della vetrina.
- Applica le regole di merchandising in tutte le visualizzazioni catalogo o personalizzale in base a una visualizzazione specifica.
- Configura consigli di prodotto, facet di ricerca e sinonimi.
- Rivedi le prestazioni della vetrina tramite Metriche di successo e rapporti sulle prestazioni delle ricerche.
- Monitora la sincronizzazione del catalogo e gli eventi della vetrina acquisiti.

Commerce Foundation rimane la fonte di verità per prodotti e prezzi e continua a gestire il carrello, il pagamento e altre operazioni transazionali.

## Presentazione rapida

>[!BEGINTABS]

>[!TAB Configurazione del catalogo]

Configura il contesto del catalogo disponibile in una vetrina.

- **Visualizzazioni catalogo** - Combina origini catalogo, criteri e listini prezzi per definire i prodotti e i prezzi recuperabili da una vetrina. Vedi [Visualizzazioni catalogo](./setup/catalog-view.md).
- **Livelli catalogo**—Ignora gli attributi di prodotto selezionati senza modificare i dati di origine. Quando si utilizza AEM Assets per le immagini dei prodotti, il livello AEM-Assets viene applicato tramite Visualizzazioni prodotto. Vedi [Livelli catalogo](./setup/catalog-layer.md).
- **Visualizzazioni catalogo privato** - Abilita la protezione del catalogo per richiedere un token firmato valido durante il recupero dei dati di una visualizzazione del catalogo. Vedi [Visualizzazioni catalogo privato](./setup/private-catalog-view.md).

>[!TAB Criteri]

I criteri filtrano i prodotti disponibili tramite una vista a catalogo in base agli attributi del prodotto. Ad esempio, una policy può limitare un assortimento a una particolare marca o categoria di prodotti.

I criteri determinano l’assortimento di prodotti disponibile. Non sostituiscono la protezione del catalogo, che controlla l’accesso a una visualizzazione di catalogo privata.

>[!TAB Merchandising]

Configura il modo in cui i clienti scoprono i prodotti e come questi vengono promossi all’interno dell’assortimento disponibile.

- **Opportunità**: verifica le prestazioni del prodotto, il comportamento dell&#39;acquirente e le tendenze di ricerca per identificare le aree in cui è possibile apportare miglioramenti al merchandising.
- **Recommendations**—Crea e gestisci unità di consigli in Commerce Admin. I consigli utilizzano i dati del catalogo e il comportamento dell’acquirente aggregato per suggerire prodotti rilevanti, ad esempio &quot;hanno visualizzato anche i clienti che hanno visualizzato questo prodotto&quot;.
- **Regole di merchandising**—Controlla il modo in cui i prodotti vengono promossi e classificati. Le regole possono essere applicate a tutte le visualizzazioni di catalogo o personalizzate per una visualizzazione specifica. Consulta [Creare una regola di merchandising](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#create-a-rule).
- **Facet** - Configura i filtri utilizzati dagli acquirenti per limitare i risultati del prodotto in base ad attributi quali marchio, dimensione o prezzo.
- **Sinonimi**: associa termini di ricerca equivalenti per aiutare gli acquirenti a trovare prodotti utilizzando parole diverse per lo stesso concetto.
- **Impostazioni** - Configura le opzioni di ricerca e merchandising, inclusi i facet di prezzo, la lingua e la ricerca avanzata.

I criteri determinano quali prodotti sono disponibili tramite una vista catalogo. Le regole di merchandising controllano il modo in cui i prodotti all’interno di tale assortimento vengono promossi e classificati.

Per informazioni dettagliate sulla corrispondenza e la classificazione dei risultati della ricerca, vedere [Corrispondenza e classificazione della ricerca](./manage-results/search-relevance-matching.md).

>[!TAB Rapporti]

Utilizza i rapporti per rivedere l’attività della vetrina e informare le decisioni di merchandising.

- **Metriche di successo**—Rivedi i ricavi, la conversione, il coinvolgimento, l&#39;acquisizione e il tasso di mancato recapito in base all&#39;attività della vetrina.
- **Prestazioni di ricerca** - Esaminare i termini di ricerca utilizzati dagli acquirenti e le relative prestazioni per identificare le aree in cui perfezionare l&#39;individuazione dei prodotti.

Il reporting dipende dai dati dell&#39;attività della vetrina raccolti dall&#39;implementazione.

>[!TAB Configurazione di sistema]

Monitora la sincronizzazione del catalogo e la raccolta degli eventi storefront per esaminare i problemi di disponibilità e implementazione dei dati.

- **Sincronizzazione catalogo** - Controlla lo stato di sincronizzazione per i dati del catalogo trasferiti da Commerce Foundation.
- **Eventi**: rivedi gli eventi di vetrina acquisiti utilizzati dall&#39;individuazione del prodotto, dai consigli e dal reporting. Utilizza la pagina Eventi per verificare la raccolta di dati comportamentali e indagare su eventi mancanti o imprevisti.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## Conferma che un’istanza utilizzi CCDM

1. Accedi a Commerce Admin tramite Unified Shell e seleziona l’istanza Adobe Commerce as a Cloud Service desiderata.
1. Conferma che le pagine di merchandising CCDM, come Visualizzazioni catalogo e Criteri, siano disponibili nella navigazione dell’istanza.
1. Se tali pagine non sono disponibili, verifica di aver selezionato l’istanza corretta e di utilizzare Unified Shell.

   Contatta il supporto Adobe o il team di provisioning Commerce per verificare lo stato di provisioning CCDM dell’istanza.

Lo stato Pronta dell’istanza conferma che è stato eseguito il provisioning, ma non conferma di per sé che utilizza CCDM.

