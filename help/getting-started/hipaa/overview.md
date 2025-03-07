---
title: Preparazione HIPAA su Adobe Commerce
description: Scopri come aggiungere l’estensione compatibile con HIPAA di Adobe Commerce e ottenere funzioni e funzionalità aggiuntive per rispettare gli obblighi HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e18b0b0ea308a6126b6cd35f943b133c75adff3
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 1%

---

# Preparazione HIPAA su Adobe Commerce

>[!IMPORTANT]
>
>**Dichiarazione di non responsabilità**<br/>
>Queste informazioni hanno lo scopo di aiutare i clienti di Adobe a rispondere alle loro domande sui servizi compatibili con HIPAA di Adobe. Non si tratta di una consulenza legale. Gli esercenti devono consultare il proprio consulente legale per comprendere i propri obblighi in base all’HIPAA e l’uso e la configurazione appropriati dei prodotti Adobe.

>[!BEGINSHADEBOX]

**Legge sulla portabilità e responsabilità dell&#39;assicurazione sanitaria (HIPAA)**

Il Health Insurance Portability and Accountability Act (HIPAA) è la principale legge federale sulla privacy sanitaria negli Stati Uniti ed è applicato dal Dipartimento della Salute e dei Servizi Umani (HHS). HIPAA si applica a _Entità coperte_ (come fornitori di assistenza sanitaria, assicuratori e stanze di compensazione) e _Associati commerciali_ (come le entità che forniscono servizi alle entità coperte). I requisiti HIPAA sono impostati in tre regole separate: Regola di privacy, Regola di sicurezza e Regola di notifica delle violazioni. Adobe funge da Business Associate per alcuni prodotti, che Adobe classifica come &quot;HIPAA-Ready Services&quot;. I dati regolamentati da HIPAA sono denominati _Informazioni sanitarie protette_ o PHI. Il PHI è un sottoinsieme di informazioni sulla salute che (1) è creato o ricevuto da un operatore sanitario, un piano sanitario o un centro di assistenza sanitaria, (2) si riferisce alla salute fisica o mentale o alle condizioni di un individuo passate, presenti o future, alla fornitura di assistenza sanitaria a un individuo, o al pagamento passato, presente o futuro per la fornitura di assistenza sanitaria a un individuo, e (3) identifica l&#39;individuo o in relazione al quale vi è una base ragionevole per credere che le informazioni possano essere utilizzate per identificare l&#39;individuo. Le Regole sulla privacy e sulla sicurezza HIPAA richiedono che un&#39;entità coperta ottenga garanzie scritte da un associato commerciale sotto forma di un Contratto di associazione commerciale (Business Associate Agreement, BAA), che richiedano all&#39;associato commerciale di salvaguardare la privacy e la sicurezza del PHI dellʼentità coperta. Per ulteriori informazioni, vedere [Prodotti e servizi HIPAA e Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) nel Centro protezione di Adobe.

>[!ENDSHADEBOX]

## Predisposto per Adobe Commerce HIPAA

L’estensione Adobe Commerce HIPAA-Ready aggiunge ulteriori funzioni e funzionalità alle installazioni di Adobe Commerce che consentono ai commercianti di rispettare i rispettivi obblighi HIPAA.

L&#39;estensione compatibile con HIPAA di Adobe Commerce, `magento/hipaa-ee`, è disponibile per Adobe Commerce su infrastrutture cloud o progetti Adobe Managed Services. Il processo di installazione compatibile con HIPAA di Adobe Commerce disabilita alcuni servizi e funzionalità nativi per soddisfare i requisiti HIPAA. Consulta [Servizi e funzionalità disabilitati](#disabled-services-and-features).

>[!NOTE]
>
>L’accesso alle funzionalità pronte per l’HIPAA è disponibile solo per i commercianti che hanno acquistato il componente aggiuntivo per il servizio sanitario per Adobe Commerce.

*Questi materiali sono esclusivamente a scopo informativo. La comunicazione di tali informazioni non conferisce al destinatario alcun diritto contrattuale o di altro tipo. Sebbene siano stati compiuti sforzi per garantire l&#39;accuratezza delle informazioni alla data in cui sono state fornite, non viene fornita alcuna dichiarazione che tali informazioni siano esatte e complete. Adobe non si impegna ad aggiornare queste informazioni in base ai cambiamenti della legge o dei prodotti Adobe. Inoltre, questo documento non può essere distribuito ad altre parti oltre al destinatario previsto senza il consenso scritto di Adobe.*

## Requisiti di sistema

Adobe Commerce deve essere implementato su Adobe Commerce nell’infrastruttura cloud o su Adobe Commerce Managed Services con versione 2.4.6-p3 - 2.4.6-p8 (nessuna versione beta).

## Installazione

**Prerequisito**

>[!BEGINSHADEBOX]

- Adobe ha eseguito il provisioning del tuo account Adobe Commerce per accedere all’estensione HIPAA Ready.
- Accedi a [repo.magento.com](https://repo.magento.com) per installare l&#39;estensione. Per generare le chiavi e ottenere i diritti necessari, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Installare la versione più recente dell&#39;estensione dei servizi pronti per HIPAA di Adobe (`magento/hipaa-ee`) in un&#39;istanza che esegue Adobe Commerce versione 2.4.6-p3 - 2.4.6-p8. L&#39;estensione viene distribuita come metapacchetto del compositore dall&#39;archivio [repo.magento.com](https://repo.magento.com). Il metapackage include la raccolta di moduli che abilitano le funzionalità HIPAA per un’istanza Adobe Commerce.

>[!NOTE]
>
>Per verificare che i dati dell&#39;evento di back office inviati ad Experience Platform siano pronti per HIPAA, vedere la [guida all&#39;estensione Data Connection](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. Sulla workstation locale, passa alla directory del progetto per il progetto Adobe Commerce su infrastruttura cloud.

   >[!NOTE]
   >
   >Per informazioni sulla gestione locale degli ambienti di progetto Commerce, vedere [Gestione dei rami con CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) nella _Guida utente di Adobe Commerce on Cloud Infrastructure_.

1. Seleziona il ramo dell’ambiente da aggiornare utilizzando Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Aggiungere il metapacchetto `magento/hipaa-ee` alla configurazione del compositore utilizzando l&#39;interfaccia CLI del compositore.

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

L&#39;estensione `magento/hipaa-ee` introduce alcune modifiche e miglioramenti al prodotto Commerce di base. Le sezioni seguenti forniscono dettagli su queste modifiche e su come modificano il prodotto di base.

### Registri azioni

La registrazione dei controlli è un requisito HIPAA. In Adobe Commerce, la funzione [Registri azioni](../../systems/action-log.md) registra ogni modifica apportata da un utente amministratore che lavora nell&#39;archivio. Per soddisfare i requisiti HIPAA per il registro di controllo, la funzione è stata aggiornata per registrare tutte le azioni degli utenti e dei clienti amministratori eseguite tramite l’interfaccia utente di amministrazione e tramite chiamate API.

I registri di azioni acquisiscono anche eventi quando i servizi Adobe accedono ai dati del tuo archivio. Puoi identificare questi eventi filtrando l’azione &quot;Dati inviati all’esterno&quot; nel rapporto Action Logs (Registri azioni).

#### Rapporto Registri azioni

La griglia del report _Registri azioni_ (**[!UICONTROL System]** > Registri azioni > Report) è stata modificata per adattarsi alle azioni dei clienti eseguite tramite l&#39;interfaccia utente e l&#39;API di amministrazione.

1. Sono state aggiunte due colonne:
   - ***Source***: visualizza la posizione in cui è stata eseguita l&#39;azione.
Valori: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo client***: visualizza il tipo di client.
Valori: Cliente | Amministratore | Integrazione

2. La colonna ***Nome utente*** è stata rinominata ***Identificatore client***
   - ***Identificatore client***: visualizza l&#39;ID di accesso per l&#39;utente che ha eseguito l&#39;azione.
Valori:
      - un messaggio e-mail se il tipo di client è Cliente
      - un nome utente se il tipo di client è Admin
      - un nome se il tipo di client è Integrazione

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
- Paginazione griglia non disponibile.
- I risultati della ricerca precedente e i filtri applicati non vengono salvati quando si esce dalla pagina.

La funzionalità di restrizione dei risultati di ricerca si applica anche all&#39;API REST per la ricerca clienti (`/V1/customers/search`).

- Se non vengono applicati filtri o se i filtri sono insufficienti, l’API restituisce un messaggio di errore per indicare che è necessario il numero di filtri necessario per eseguire una ricerca.
- Quando gli utenti autorizzati applicano un numero sufficiente di filtri, l’API restituisce i risultati entro il limite specificato.
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
| Importa | <ul><li>Un utente amministratore esegue un’importazione<li>Un utente amministratore scarica un file importato<li>Un utente amministratore scarica un file di errore<ul/> |
| Esporta | <ul><li>Richieste di utenti amministratore<li>Un utente amministratore scarica un file esportato<ul/> |
| Importazioni/esportazioni programmate | <ul><li>Un utente amministratore pianifica l’esportazione<li>Un utente amministratore modifica un’esportazione pianificata<li>Un utente amministratore esegue un’esportazione pianificata<li>Un utente amministratore elimina un’esportazione pianificata<li>Un utente amministratore pianifica un’importazione<li>Un utente amministratore modifica un’importazione pianificata<li>Un utente amministratore esegue un’importazione pianificata<li>Un utente amministratore elimina un’importazione pianificata<li>Un utente amministratore esegue un’eliminazione in blocco delle operazioni di importazione/esportazione<ul/> |

### Miglioramenti alla visualizzazione e miglioramento del filtraggio e dell’ordinamento

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
| InviaGriglia | No | No | No | No |
| Servizio e-mail semplice AWS | Sì | Sì | Sì | No |

### Servizi Adobe Commerce

La tabella seguente identifica i servizi Adobe Commerce disponibili per l’offerta compatibile con HIPAA. Tali servizi includono, tra l&#39;altro:

| Servizio | Non di produzione | Produzione |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | Sì | Sì |
| [Mesh API per Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/) | Sì | Sì |
| [Esportazione dati SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) | Sì | Sì |
| [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) | No | No |
| [Consigli di prodotto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/overview) | No | No |
| [Servizi di pagamento](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/payment-services/guide-overview) | No | No |
| [Eventi back office connessione dati](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice) | Sì | Sì |
| [Eventi Storefront Connessione Dati](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#storefront-events) | No | No |
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

Le seguenti funzioni sono disattivate per impostazione predefinita nel modulo HIPAA-readiness. Gli esercenti possono abilitare ognuna di queste funzioni a proprio rischio.

- **[E-mail transazionale](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—SendGrid è disabilitato per impostazione predefinita perché il servizio non è compatibile con HIPAA. Adobe Commerce fornisce un&#39;opzione di integrazione che puoi utilizzare con il tuo account [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Per informazioni dettagliate sulla configurazione, contatta il tuo Customer Technical Account Manager o il servizio di assistenza Adobe Commerce.

- **[Pagamento per gli ospiti](../../stores-purchase/checkout-guest.md)** - Questa funzionalità rappresenta un potenziale rischio per vari aspetti dell&#39;HIPAA, tra cui la registrazione, il controllo degli accessi, l&#39;igiene e la derivazione PHI e potenzialmente altri.

- **[Funzione newsletter](../../merchandising-promotions/newsletters.md)** - Questa funzione è disabilitata per impedire l&#39;utilizzo di PHI in un contesto di marketing.

- **[Impostazione avanzata del servizio Reporting](../../getting-started/business-intelligence.md)**. Questa impostazione di configurazione è disabilitata per impedire l&#39;utilizzo di PHI per l&#39;analisi e il reporting.
