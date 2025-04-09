---
title: Preparazione HIPAA per Adobe Systems Commerce
description: Scopri come aggiungere l’estensione compatibile con HIPAA di Adobe Commerce e ottenere funzioni e funzionalità aggiuntive per rispettare gli obblighi HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 2807c36fdb4ca169c31a5e92b4dab278a45c474c
workflow-type: tm+mt
source-wordcount: '2375'
ht-degree: 1%

---

# Preparazione HIPAA per Adobe Systems Commerce

>[!IMPORTANT]
>
>**Legali**<br/>
>Queste informazioni hanno lo scopo di aiutare Adobe Systems clienti a rispondere alle loro domande relative ai servizi HIPAA-Ready di Adobe Systems. Non costituisce consulenza legale. I commercianti dovrebbero consultare il proprio consulente legale per comprendere i loro obblighi ai sensi dell&#39;HIPAA e l&#39;uso e la configurazione appropriati dei prodotti di Adobe Systems.

>[!BEGINSHADEBOX]

**Legge sulla portabilità e la responsabilità dell&#39;assicurazione sanitaria (HIPAA)**

L&#39;Health Insurance Portability and Accountability Act (HIPAA) è la principale legge federale sulla privacy sanitaria negli Stati Uniti ed è applicata dal Dipartimento della salute e dei servizi umani degli Stati Uniti (HHS). L&#39;HIPAA si applica alle _Entità_ coperte (come fornitori di assistenza sanitaria, assicuratori e stanze di compensazione) e _ai Aziende associati_ (come le entità che forniscono servizi alle entità coperte). I requisiti HIPAA sono stabiliti in tre regole separate: Regola sulla privacy, Regola di sicurezza e Regola di notifica delle violazioni. Adobe Systems agisce come Aziende Associate per determinati prodotti, che Adobe Systems classifica come &quot;Servizi predisposti per la normativa HIPAA&quot;. I dati regolati dall&#39;HIPAA sono indicati come _informazioni_ sanitarie protette o PHI. PHI è un sottoinsieme di informazioni sanitarie che (1) è creato o ricevuto da un fornitore di assistenza sanitaria, un piano sanitario o una stanza di compensazione sanitaria, (2) si riferisce alla salute fisica o mentale passata, presente o futura o alla condizione di un individuo, alla fornitura di assistenza sanitaria a un individuo o al pagamento passato, presente o futuro per la fornitura di assistenza sanitaria a un individuo,  e (3) identifica l&#39;individuo o rispetto al quale vi è una ragionevole base per ritenere che le informazioni possano essere utilizzate per identificare l&#39;individuo. Le Norme sulla privacy e sulla sicurezza HIPAA richiedono che un&#39;Entità coperta ottenga garanzie scritte da un Aziende Associato sotto forma di Aziende Associate Agreement o BAA, che richiede all&#39;Aziende Associate di salvaguardare la privacy e la sicurezza del PHI dell&#39;Entità Coperta. Per ulteriori informazioni, vedere [Prodotti e servizi](https://www.adobe.com/trust/compliance/hipaa-ready.html) HIPAA e Adobe Systems nel Centro protezione Adobe Systems.

>[!ENDSHADEBOX]

## Pronto per Adobe Systems Commerce per HIPAA

L&#39;estensione HIPAA-Ready di Adobe Systems Commerce aggiunge ulteriori caratteristiche e funzionalità alle installazioni di Adobe Systems Commerce che consentono ai commercianti di rispettare i rispettivi obblighi HIPAA.

L&#39;estensione `magento/hipaa-ee` HIPAA-Ready di Adobe Systems Commerce è disponibile per Adobe Systems Commerce su progetti infrastruttura cloud o Adobe Systems Managed Services. Il processo di installazione HIPAA-Ready di Adobe Systems Commerce disabilita alcuni servizi e funzionalità di nativo per conformarsi ai requisiti HIPAA. Vedere [Servizi e funzionalità](#disabled-services-and-features) disabilitati.

>[!NOTE]
>
>L&#39;accesso alle caratteristiche e alle funzionalità compatibili con HIPAA è disponibile solo per i commercianti che hanno acquistato il componente aggiuntivo per l&#39;assistenza sanitaria per Adobe Systems Commerce.

*Questi materiali sono destinati esclusivamente a scopo informativo. La fornitura di queste informazioni non conferisce al destinatario alcun diritto contrattuale o di altro tipo. Sebbene siano stati compiuti sforzi per garantire l&#39;accuratezza delle informazioni alla data in cui sono state fornite, non viene fornita alcuna dichiarazione che tali informazioni siano accurate e complete. Adobe Systems non si assume alcun obbligo di aggiornare queste informazioni man mano che la legge o i prodotti Adobe Systems cambiano. Inoltre, questo documento non deve essere distribuito a soggetti diversi dal destinatario previsto senza il consenso scritto di Adobe Systems.*

## requisiti di sistema

Nella tabella seguente viene illustrata la compatibilità tra le versioni di Adobe Systems Commerce e l&#39;estensione compatibile con HIPAA:

| Adobe Commerce | Supportato | Note |
|----------------|-----------|-------|
| 2,4,7-p4 - 2,4,7-p5 | 1.2.0. | Il supporto per la versione 2.4.7-P4 richiede un [hotfix](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/hotfix-for-hipaa-package-1-2-0-compatibility-with-adobe-commerce-2-4-7-p4) |
| 2,4,6-p9 - 2,4,6-p10 | 1.2.0. | |
| 2.4.6-p8 | 1.1.0. | Il supporto per [servizi dati](#adobe-commerce-services) è stato introdotto in 1.1.0 |
| 2,4,6-p3 - 2,4,6-p7 | 1,0,0 | |

>[!IMPORTANT]
>
>- L’estensione compatibile con HIPAA è disponibile solo per progetti Adobe Commerce on Cloud o Adobe Commerce Managed Services.
>- L&#39;estensione è disponibile come metapacchetto Compositore da `repo.magento.com`.
>- L’accesso alle funzioni e alle funzionalità compatibili con HIPAA richiede il componente aggiuntivo del servizio sanitario per Adobe Commerce.
>- Le versioni beta di Adobe Commerce non sono supportate.

## Installazione

**Prerequisito**

>[!BEGINSHADEBOX]

- Adobe ha eseguito il provisioning del tuo account Adobe Commerce per accedere all’estensione HIPAA Ready.
- Accedi a [repo.magento.com](https://repo.magento.com) per installare l&#39;estensione. Per generare le chiavi e ottenere i diritti necessari, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Installare la versione più recente dell&#39;estensione dei servizi pronti per HIPAA di Adobe (`magento/hipaa-ee`) in un&#39;istanza che esegue Adobe Commerce versione 2.4.7-p5 o 2.4.6-p3 fino a 2.4.6-p8. L&#39;estensione viene distribuita come metapacchetto del compositore dall&#39;archivio [repo.magento.com](https://repo.magento.com). Il metapacchetto include la raccolta di moduli che abilitano le funzionalità HIPAA per un istanza di Adobe Systems Commerce.

>[!NOTE]
>
>Per assicurarsi che i dati degli eventi di back office inviati al Experience Platform siano compatibili con HIPAA, vedere la Guida](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension) all&#39;estensione della [connessione dati.

1. Nella workstation locale, passare alla directory del progetto per il progetto Adobe Systems Commerce su infrastruttura cloud.

   >[!NOTE]
   >
   >Per informazioni sulla gestione locale degli ambienti di progetto Commerce, vedere [Gestione delle filiali con l&#39;interfaccia della riga di comando](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) nel Guida utente _Adobe Systems Commerce sull&#39;infrastruttura_ cloud.

1. Estrai il ramo dell&#39;ambiente per aggiornarlo utilizzando l&#39;interfaccia della riga di comando Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Aggiungi il metapacchetto `magento/hipaa-ee` alla configurazione del compositore usando la CLI del compositore.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Aggiornare le dipendenze del pacchetto.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Aggiungi, esegui il commit e invia il codice aggiornato all&#39;ambiente cloud.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Inviando gli aggiornamenti si avvia il [processo di distribuzione cloud di Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) per applicare le modifiche. Controllare lo stato della distribuzione dal [registro distribuzione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verificare l&#39;installazione

Dopo aver distribuito gli aggiornamenti, verificare che l&#39;estensione `Hipaa*` sia installata

1. Utilizza SSH per accedere all’ambiente cloud remoto.

   ```shell
   magento-cloud ssh
   ```

1. Dalla riga di comando, utilizza Adobe Commerce CLI per verificare lo stato del modulo.

   ```shell
   bin/magento module:status
   ```

1. Verificare che i moduli HIPAA siano inclusi nell&#39;elenco dei moduli abilitati:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   Tutti i moduli con prefisso `Magento_Hipaa` devono trovarsi nella sezione dei moduli abilitati.

## Miglioramenti funzionali per la conformità HIPAA

L&#39;estensione `magento/hipaa-ee` introduce alcune modifiche e miglioramenti al prodotto Commerce di base. Nelle sezioni seguenti vengono fornite informazioni dettagliate su queste modifiche e su come modificano il prodotto di base.

### Registri delle azioni

La registrazione di controllo è un requisito HIPAA. In Adobe Systems Commerce, la [funzione Registri azioni](../../systems/action-log.md) registra ogni modifica apportata da un utente amministratore che lavora nel tuo store. Per soddisfare i requisiti HIPAA per il registro di controllo, la funzionalità è stata aggiornata per registrare tutte le utente dell&#39;amministratore e le azioni dei clienti eseguite tramite il interfaccia di amministrazione e le chiamate API.

I registri azioni acquisiscono anche eventi quando i servizi Adobe Systems accesso i tuoi dati store. È possibile identificare questi eventi filtrando l&#39;azione &quot;Dati inviati all&#39;esterno&quot; nel rapporto Registri azioni.

#### Rapporto Registri azioni

La _griglia del report Action Logs_ (**[!UICONTROL System]** > Action Logs > Report) viene modificata per adattarsi alle azioni dei clienti eseguite tramite l&#39;interfaccia di amministrazione e l&#39;API.

1. Sono state aggiunte due colonne:
   - ***Origine***: mostra dove è stata eseguita l&#39;azione.
Valori: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo di*** client: visualizza il tipo di client.
Valori: Cliente | Amministratore | Integrazione

2. Nome utente rinominato ****** in ***Identificatore client***
   - ***Identificatore*** client: visualizza l&#39;ID login del utente che ha eseguito l&#39;azione.
Valori:
      - un&#39;e-mail se il tipo di client è cliente
      - un nome utente se il tipo di client è Admin
      - un nome se Tipo client è Integrazione

3. La colonna ***Nome azione completo*** è stata rinominata ***Destinazione***
   - ***Destinazione***: visualizza il nome dell&#39;azione.
Valori:
      - un endpoint se Source è un’API REST o un’API SOAP
      - un nome di query o mutazione se un’API GraphQL
      - un nome di azione se si tratta di un’interfaccia utente amministratore o cliente.

#### Configurare le azioni amministratore per la registrazione

Questa funzione non è disponibile perché tutte le azioni devono essere registrate per impostazione predefinita.

### Limitazione dei risultati di ricerca dei clienti HIPAA

La funzionalità HIPAA Customer Search Results Restriction di Adobe Commerce garantisce la conformità alle normative HIPAA limitando l’accesso alle informazioni sanitarie protette (PHI) e alle informazioni personali identificabili (PII). Questa funzione limita la possibilità di cercare e visualizzare i record dei clienti in base ai ruoli utente, garantendo che solo gli utenti autorizzati possano accedere a tali informazioni.

#### Funzioni principali

- **Restrizioni ricerca**: gli utenti senza i ruoli necessari non possono cercare o visualizzare i record dei clienti.
- **Ricerca obbligatoria per l&#39;accesso**: a differenza del comportamento predefinito di Adobe Commerce, non è possibile visualizzare le informazioni del cliente senza eseguire una ricerca. In questo modo gli utenti devono conoscere dettagli specifici di un cliente per individuare le proprie informazioni.
- **Risultati ricerca limitati**: i risultati della ricerca che soddisfano i criteri sono limitati a 10 record, in modo che venga visualizzato solo un numero gestibile di record alla volta.
- **Numero minimo di filtri**: gli utenti devono applicare un minimo di tre filtri (ad esempio e-mail, cognome e stato) per eseguire una ricerca, assicurandosi che le ricerche siano specifiche e mirate.
- **Notifiche filtro**: quando le restrizioni di ricerca sono abilitate, agli utenti viene notificato di applicare i filtri per perfezionare i risultati della ricerca.

#### Configurazione

La configurazione per limitare il numero di clienti nei risultati di ricerca si trova nel pannello di amministrazione in **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**. Questa configurazione è attivata per impostazione predefinita quando è installata l&#39;estensione `hipaa-ee`.

- **Limita numero di clienti nella griglia**: questa impostazione consente di abilitare o disabilitare il limite del numero di clienti visualizzato nei risultati della ricerca nella griglia.
- **Limite risultati ricerca griglia clienti**: questa impostazione specifica il numero massimo di record cliente che è possibile visualizzare nei risultati della ricerca griglia.

#### Aree funzionali interessate

Le griglie clienti nella pagina Ordine di creazione amministratore (**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**) e nella pagina Clienti (**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**) sono interessate dalla funzionalità di restrizione dei risultati di ricerca.

- I filtri vengono aperti per impostazione predefinita.
- Per eseguire una ricerca, gli utenti devono applicare almeno tre filtri.
- Per impostazione predefinita, i risultati della ricerca sono limitati a 10 record.
- Se ci sono più record che corrispondono ai criteri di ricerca, le notifiche informeranno gli utenti del limite di risultati e della necessità di perfezionare la ricerca.
- L&#39;impaginazione della griglia non è disponibile.
- Precedente ricerca risultati e filtri applicati non vengono salvati quando ci si allontana dalla pagina.

La funzionalità di restrizione dei risultati del ricerca si applica anche all&#39;API REST per ricerca del cliente (`/V1/customers/search`).

- Senza filtri applicati o con filtri insufficienti, l&#39;API restituisce un messaggio di errore che indica che è necessario il numero richiesto di filtri per eseguire un ricerca.
- Quando un numero sufficiente di filtri viene applicato da utenti autorizzati, l&#39;API restituisce risultati entro il limite specificato.
- Quando i risultati sono limitati, alla risposta viene aggiunto un messaggio che indica il numero totale di record trovati e il limite applicato corrente.

### Importazione ed esportazione di feature

I miglioramenti apportati alle funzioni di importazione ed esportazione si concentrano sul miglioramento dell&#39;esperienza amministrativa e sulla fornitura di una migliore visibilità sulle azioni degli utenti.

>[!NOTE]
>
>Questi miglioramenti di ***non modificano la logica di base per l&#39;importazione e l&#39;esportazione***, ma estendono la funzionalità per offrire una registrazione più completa e una migliore attribuzione dei dati. Le funzionalità fondamentali di importazione ed esportazione rimangono invariate. Gli utenti possono continuare a utilizzare le funzioni e i flussi di lavoro esistenti senza interruzioni.

#### Registrazione azioni amministrative

Uno dei miglioramenti principali nelle funzioni di importazione ed esportazione è la registrazione avanzata delle azioni amministrative. Questo miglioramento introduce la possibilità di approfondire le attività associate all’importazione e all’esportazione dei dati, contribuendo a migliorare il tracciamento e la verificabilità. Le azioni seguenti vengono ora registrate e riportate nella griglia **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Tipo | Azioni |
| ---- | ------- |
| Importa | <ul><li>Un utente amministratore esegue un&#39;importazione<li>Un amministratore utente scarica un file importato<li>Un utente amministratore scarica un file di errore<ul/> |
| Esportazione | <ul><li>Un amministratore utente le richieste<li>Un utente amministratore scarica un file esportato<ul/> |
| Importazioni/esportazioni programmate | <ul><li>Un amministratore utente pianifica l&#39;esportazione<li>Un amministratore utente modifica un&#39;esportazione pianificata<li>Un utente amministratore esegue un&#39;esportazione pianificata<li>Un amministratore utente elimina un&#39;esportazione pianificata<li>Un utente amministratore pianifica un&#39;importazione<li>Un amministratore modifica utente un&#39;importazione pianificata<li>Un utente amministratore esegue un&#39;importazione pianificata<li>Un utente amministratore elimina un&#39;importazione pianificata<li>Un utente Admin esegue un&#39;eliminazione collettiva delle operazioni di importazione/esportazione<ul/> |

### Miglioramenti alla visualizzazione e ottimizzazione di filtri e ordinamento

Per consentire agli utenti amministratori di disporre di griglie con maggiori informazioni, il servizio HIPAA-Ready fornisce diversi miglioramenti per visualizzare, filtrare e ordinare i dati.

#### Cronologia importazione ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- È stato abilitato il filtro per tutte le colonne ad eccezione di **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** e **[!UICONTROL Summary]**.

#### Esporta ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Aggiunta colonna **[!UICONTROL ID]**.
- È stata aggiunta una colonna **[!UICONTROL Requested At]** (_data e ora in cui è stata richiesta l&#39;esportazione_).
- Aggiunta colonna **[!UICONTROL User]** (_username di un amministratore che ha eseguito la richiesta_).
- È stata rimossa una colonna **[!UICONTROL Action]**.
- Il collegamento **[!UICONTROL Download]** è stato spostato in una colonna **[!UICONTROL File name]** (_come la griglia Cronologia importazione_).
- Disabilitata l&#39;azione responsabile dell&#39;eliminazione di un file esportato (_per migliorare il tracciamento_).
- Ordinamento abilitato per tutte le colonne eccetto **[!UICONTROL File name]**.
- Attivazione del filtro per tutte le colonne.

#### Importazioni ed esportazioni pianificate ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Aggiunta colonna **[!UICONTROL ID]**.
- È stata aggiunta una colonna **[!UICONTROL Scheduled At]** (la _data e ora in cui è stata pianificata l&#39;importazione o l&#39;esportazione_).
- È stata aggiunta una colonna **[!UICONTROL User]** (il _nome utente di un utente amministratore che ha pianificato l&#39;importazione o l&#39;esportazione_).

## Servizi e strumenti compatibili con HIPAA

Questa sezione descrive i servizi Adobe pronti per HIPAA che sono disponibili per l’utilizzo con l’offerta HIPAA per Adobe Commerce. Descrive inoltre gli strumenti che è possibile utilizzare per monitorare i principali controlli di sicurezza e conformità per il negozio.

| Servizio | Produzione | Staging | staging_for_support | Sviluppo |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce con componente aggiuntivo per il settore sanitario | Sì | Sì | Sì | No |
| SendGrid | No | No | No | No |
| Servizio e-mail semplice AWS | Sì | Sì | Sì | No |

### Servizi Adobe Commerce

La tabella seguente identifica i servizi Adobe Commerce disponibili per l’offerta compatibile con HIPAA. Tali servizi includono, tra l&#39;altro:

| Servizio | Non di produzione | Produzione |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | Sì | Sì |
| [Mesh API per Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/) | Sì | Sì |
| [Esportazione dati SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) | Sì | Sì |
| [Live search](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) | No | No |
| [Raccomandazioni del prodotto](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | No | No |
| [Servizi di pagamento](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview) | No | No |
| [Eventi back office connessione dati](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | Sì | Sì |
| [Eventi Storefront Connessione Dati](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#storefront-events) | No | No |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | No | No |

### Strumenti

Lo strumento [Analisi sicurezza](../../systems/security-scan.md) per Adobe Commerce consente di monitorare l&#39;archivio per verificare che tutti i controlli di sicurezza richiesti siano attivati e operativi. Oltre ai controlli di sicurezza standard, Adobe ha migliorato lo strumento per visualizzare i controlli specifici HIPAA per i clienti che utilizzano l’offerta HIPAA per Adobe Commerce. I controlli HIPAA nello strumento Security Scan sono progettati per garantire che:

- I moduli di controllo non sono disabilitati
- L&#39;autenticazione a due fattori (2FA) non è disabilitata
- Le funzioni di marketing sono disabilitate
- Tutte le estensioni installate corrispondono a un inserisco nell&#39;elenco Consentiti predefinito per la
- Nessun servizio Adobe non supportato installato

È possibile [configurare lo strumento](../../systems/security-scan.md#run-a-security-scan) per inviare notifiche e-mail con i dettagli delle analisi pianificate o [visualizzare manualmente i report](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report).

## Funzioni disattivate

Per soddisfare i requisiti HIPAA, alcune funzioni supportate da Adobe Commerce non sono disponibili o sono disabilitate per impostazione predefinita. I commercianti hanno la possibilità di riattivare o utilizzare queste funzioni a proprio rischio.

Le seguenti funzioni sono disabilitate per impostazione predefinita nel modulo di preparazione HIPAA. Gli esercenti possono abilitare ognuna di queste funzioni a proprio rischio.

- **[E-mail transazionale](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—SendGrid è disabilitato per impostazione predefinita perché il servizio non è compatibile con HIPAA. Adobe Commerce fornisce un&#39;opzione di integrazione che puoi utilizzare con il tuo account [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Per informazioni dettagliate sulla configurazione, contatta il tuo Customer Technical Account Manager o il servizio di assistenza Adobe Commerce.

- **[Pagamento per gli ospiti](../../stores-purchase/checkout-guest.md)** - Questa funzionalità rappresenta un potenziale rischio per vari aspetti dell&#39;HIPAA, tra cui la registrazione, il controllo degli accessi, l&#39;igiene e la derivazione PHI e potenzialmente altri.

- **[Funzione newsletter](../../merchandising-promotions/newsletters.md)** - Questa funzione è disabilitata per impedire l&#39;utilizzo di PHI in un contesto di marketing.

- **[Avanzate impostazione del servizio](../../getting-started/business-intelligence.md)** di reporting: questa impostazione di configurazione è disabilitata per impedire l&#39;utilizzo di PHI per l&#39;analisi e il reporting.
