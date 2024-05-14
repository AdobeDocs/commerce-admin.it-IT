---
title: Preparazione HIPAA su Adobe Commerce
description: Scopri come aggiungere il modulo HIPAA-Ready di Adobe Commerce e ottenere funzioni e funzionalità aggiuntive per rispettare gli obblighi HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# Preparazione HIPAA su Adobe Commerce

>[!IMPORTANT]
>
>**Dichiarazione di non responsabilità legale**<br/>
>Queste informazioni hanno lo scopo di aiutare i clienti Adobi a rispondere alle loro domande sui servizi compatibili con HIPAA di Adobe. Non si tratta di una consulenza legale. Gli esercenti devono consultare il proprio consulente legale per comprendere i propri obblighi ai sensi dell&#39;HIPAA e l&#39;uso e la configurazione appropriati dei prodotti Adobe.

>[!BEGINSHADEBOX]

**Health Insurance Portability and Accountability Act (HIPAA)**

Il Health Insurance Portability and Accountability Act (HIPAA) è la principale legge federale sulla privacy sanitaria negli Stati Uniti ed è applicato dal Dipartimento della Salute e dei Servizi Umani (HHS). L’HIPAA si applica a _Entità coperte_ (ad esempio prestatori di assistenza sanitaria, assicuratori e stanze di compensazione) e _Associati commerciali_ (quali gli enti che forniscono servizi agli enti disciplinati). I requisiti HIPAA sono impostati in tre regole separate: Regola di privacy, Regola di sicurezza e Regola di notifica delle violazioni. Adobe funge da Business Associate per alcuni prodotti, che Adobe classifica come &quot;HIPAA-Ready Services&quot;. I dati disciplinati dall’HIPAA sono denominati _Informazioni sulla salute protette_ o PHI. Il PHI è un sottoinsieme di informazioni sulla salute che (1) è creato o ricevuto da un operatore sanitario, un piano sanitario o un centro di assistenza sanitaria, (2) si riferisce alla salute fisica o mentale o alle condizioni di un individuo passate, presenti o future, alla fornitura di assistenza sanitaria a un individuo, o al pagamento passato, presente o futuro per la fornitura di assistenza sanitaria a un individuo, e (3) identifica l&#39;individuo o in relazione al quale vi è una base ragionevole per credere che le informazioni possano essere utilizzate per identificare l&#39;individuo. Le Regole sulla privacy e sulla sicurezza HIPAA richiedono che un&#39;entità coperta ottenga garanzie scritte da un associato commerciale sotto forma di un Contratto di associazione commerciale (Business Associate Agreement, BAA), che richiedano all&#39;associato commerciale di salvaguardare la privacy e la sicurezza del PHI dellʼentità coperta. Per ulteriori informazioni, consulta [HIPAA e prodotti e servizi per l’Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) nel Centro protezione Adobe.

>[!ENDSHADEBOX]

## Predisposto per Adobe Commerce HIPAA

Adobe Commerce HIPAA-Ready dispone di funzioni e funzionalità aggiuntive che consentono ai commercianti di adempiere ai rispettivi obblighi HIPAA.

Adobe Commerce HIPAA-Ready viene fornito come estensione Adobe Commerce, `magento/hipaa-ee` disponibile per Adobe Commerce su infrastrutture cloud o progetti Adobe Managed Services. Il processo di installazione compatibile con HIPAA di Adobe Commerce disabilita alcuni servizi e funzionalità nativi per soddisfare i requisiti HIPAA. Consulta [Servizi e funzionalità disattivati](#disabled-services-and-features).

*Questi materiali sono esclusivamente a scopo informativo. La comunicazione di tali informazioni non conferisce al destinatario alcun diritto contrattuale o di altro tipo. Sebbene siano stati compiuti sforzi per garantire l&#39;accuratezza delle informazioni alla data in cui sono state fornite, non viene fornita alcuna dichiarazione che tali informazioni siano esatte e complete. Adobe non si assume alcun obbligo di aggiornare queste informazioni in seguito al cambiamento della normativa o dei prodotti Adobe. Inoltre, il presente documento non deve essere distribuito ad alcuna parte diversa dal destinatario previsto senza il consenso scritto di Adobe.*

## Requisiti di sistema

Adobe Commerce deve essere implementato su Adobe Commerce nell’infrastruttura cloud o su Adobe Commerce Managed Services con versione 2.4.6-p3 o successiva (nessuna versione beta).

## Installazione

Installa la versione più recente dell’estensione HIPAA-Ready Services di Adobe (`magento/hipaa-ee`) su un&#39;istanza che esegue Adobe Commerce versione 2.4.6-p3 o successiva. L&#39;estensione viene distribuita come metapacchetto del compositore dal [repo.magento.com](https://repo.magento.com) archivio.

>[!BEGINSHADEBOX]

**Prerequisito**

Devi avere accesso a [repo.magento.com](https://repo.magento.com) per installare l’estensione. Per generare le chiavi e ottenere i diritti necessari, consulta [Ottieni le chiavi di autenticazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. Sulla workstation locale, passa alla directory del progetto per il progetto Adobe Commerce su infrastruttura cloud.

   >[!NOTE]
   >
   >Per informazioni sulla gestione locale degli ambienti di progetto Commerce, vedi  [Gestione dei rami con CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) nel _Guida utente di Adobe Commerce su infrastruttura cloud_.

1. Estrai il ramo dell’ambiente da aggiornare utilizzando Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Aggiungi il metapacchetto `magento/hipaa-ee` alla configurazione del compositore utilizzando Composer CLI.

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

   Inviando gli aggiornamenti si avvia [Processo di distribuzione cloud Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) per applicare le modifiche. Controlla lo stato della distribuzione da [registro di distribuzione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verificare l&#39;installazione

Dopo aver distribuito gli aggiornamenti, verifica che `Hipaa*` l&#39;estensione è installata

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
   <truncated for brevity>
   ```

   Tutti i moduli con prefisso `Magento_Hipaa` deve trovarsi nella sezione moduli attivati.

## Miglioramenti funzionali per la conformità HIPAA

Il `magento/hipaa-ee` introduce alcune modifiche e alcuni miglioramenti al prodotto Commerce di base. Le sezioni seguenti forniscono dettagli su queste modifiche e su come modificano il prodotto di base.

### Registri azioni

La registrazione dei controlli è un requisito HIPAA. In Adobe Commerce, il [Registri azioni](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) Questa funzione registra ogni modifica apportata da un utente amministratore che lavora nel tuo store. Per soddisfare i requisiti HIPAA per il registro di controllo, la funzione è stata aggiornata per registrare tutte le azioni degli utenti e dei clienti amministratori eseguite tramite l’interfaccia utente di amministrazione e tramite chiamate API.

#### Rapporto Registri azioni

Il _Registri azioni_ griglia dei rapporti (**[!UICONTROL System]** > Action Logs > Report) è stato modificato per adattarsi alle azioni dei clienti eseguite tramite l’interfaccia utente e l’API di amministrazione.

1. Sono state aggiunte due colonne:
   - ***Sorgente***: mostra dove è stata eseguita l’azione.
Valori: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo di client***: visualizza il tipo di client.
Valori: Cliente | Amministratore | Integrazione

2. Rinominato il ***Nome utente*** colonna a ***Identificatore client***
   - ***Identificatore client***: visualizza l’ID di accesso dell’utente che ha eseguito l’azione.
Valori:
      - un messaggio e-mail se il tipo di client è Cliente
      - un nome utente se il tipo di client è Admin
      - un nome se il tipo di client è Integrazione

3. Rinominato il ***Nome azione completo*** colonna a ***Target***
   - ***Target***: visualizza il nome dell’azione.
Valori:
      - un endpoint se Source è un’API REST o un’API SOAP
      - un nome di query o mutazione se un’API GraphQL
      - un nome di azione se si tratta di un’interfaccia utente amministratore o cliente.

#### Configurare le azioni amministratore per la registrazione

Questa funzione non è disponibile perché tutte le azioni devono essere registrate per impostazione predefinita.

### Importazione ed esportazione di feature

I miglioramenti apportati alle funzioni di importazione ed esportazione si concentrano sul miglioramento dell&#39;esperienza amministrativa e sulla fornitura di una migliore visibilità sulle azioni degli utenti.

>[!NOTE]
>
>Questi ***I miglioramenti non alterano la logica di base Importa ed Esporta***; estendono invece la funzionalità per offrire una registrazione più completa e una migliore attribuzione dei dati. Le funzionalità fondamentali di importazione ed esportazione rimangono invariate. Gli utenti possono continuare a utilizzare le funzioni e i flussi di lavoro esistenti senza interruzioni.

#### Registrazione azioni amministrative

Uno dei miglioramenti principali nelle funzioni di importazione ed esportazione è la registrazione avanzata delle azioni amministrative. Questo miglioramento introduce la possibilità di approfondire le attività associate all’importazione e all’esportazione dei dati, contribuendo a migliorare il tracciamento e la verificabilità. Le seguenti azioni vengono ora registrate e riportate nel **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**griglia:

| Tipo | Azioni |
| ---- | ------- |
| Importa | <ul><li>Un utente amministratore esegue un’importazione<li>Un utente amministratore scarica un file importato<li>Un utente amministratore scarica un file di errore<ul/> |
| Esporta | <ul><li>Richieste di utenti amministratore<li>Un utente amministratore scarica un file esportato<ul/> |
| Importazioni/esportazioni programmate | <ul><li>Un utente amministratore pianifica l’esportazione<li>Un utente amministratore modifica un’esportazione pianificata<li>Un utente amministratore esegue un’esportazione pianificata<li>Un utente amministratore elimina un’esportazione pianificata<li>Un utente amministratore pianifica un’importazione<li>Un utente amministratore modifica un’importazione pianificata<li>Un utente amministratore esegue un’importazione pianificata<li>Un utente amministratore elimina un’importazione pianificata<li>Un utente amministratore esegue un’eliminazione in blocco delle operazioni di importazione/esportazione<ul/> |

### Miglioramenti alla visualizzazione e miglioramento del filtraggio e dell’ordinamento

Per consentire agli utenti amministratori di disporre di griglie con maggiori informazioni, il servizio HIPAA-Ready fornisce diversi miglioramenti per visualizzare, filtrare e ordinare i dati.

#### Cronologia importazione ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Attivazione del filtro per tutte le colonne ad eccezione di **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, e **[!UICONTROL Summary]**.

#### Esporta ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- È stato aggiunto un **[!UICONTROL ID]** colonna.
- È stato aggiunto un **[!UICONTROL Requested At]** column (_data e ora in cui è stata richiesta l’esportazione_).
- È stato aggiunto un **[!UICONTROL User]** column (_nome utente di un amministratore che ha eseguito la richiesta_).
- È stato rimosso un elemento **[!UICONTROL Action]** colonna.
- Spostato il **[!UICONTROL Download]** collegamento a un **[!UICONTROL File name]** column (_come la griglia Cronologia importazione_).
- Disabilitata l&#39;azione responsabile dell&#39;eliminazione di un file esportato (_per migliorare il tracciamento_).
- Ordinamento abilitato per tutte le colonne eccetto **[!UICONTROL File name]**.
- Attivazione del filtro per tutte le colonne.

#### Importazioni ed esportazioni programmate ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- È stato aggiunto un **[!UICONTROL ID]** colonna.
- È stato aggiunto un **[!UICONTROL Scheduled At]** colonna (la _data e ora in cui è stata pianificata l’importazione o l’esportazione_).
- È stato aggiunto un **[!UICONTROL User]** colonna (la _nome utente di un utente amministratore che ha pianificato l’importazione o l’esportazione_).

## Servizi e funzionalità disattivati

Per soddisfare i requisiti HIPAA, alcuni servizi e funzionalità supportati da Adobe Commerce non sono disponibili o sono disabilitati per impostazione predefinita. I commercianti hanno la possibilità di riattivare o utilizzare questi servizi e funzioni a proprio rischio.

### Servizi

- **Servizi Adobe Commerce**—Nessun servizio Adobe Commerce o servizio di estensibilità disponibile nell’ambito dell’offerta compatibile con HIPAA. Tali servizi includono, tra l&#39;altro:

   - Live Search
   - Mesh API
   - App Builder
   - Servizio catalogo

- **[Servizio SendGrid](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**- Il servizio è disabilitato per impostazione predefinita perché l&#39;applicazione non è compatibile con HIPAA. Gli esercenti possono inviare una richiesta di supporto per abilitare Sendgrid, ma devono riconoscere che si assumono il rischio di utilizzare il servizio.

### Funzioni disattivate per impostazione predefinita

Le seguenti funzioni sono disattivate per impostazione predefinita nel modulo HIPAA-readiness. Gli esercenti possono abilitare ognuna di queste funzioni a proprio rischio.

- **[Pagamento per gli ospiti](../stores-purchase/checkout-guest.md)**- Questa funzione presenta un rischio potenziale per vari aspetti dell&#39;HIPAA, tra cui la registrazione, il controllo degli accessi, l&#39;igiene e la derivazione PHI e potenzialmente altro ancora.

- **[Funzione newsletter](../merchandising-promotions/newsletters.md)**- Questa funzione è disattivata per impedire l&#39;utilizzo di PHI in un contesto di marketing.

- **[Impostazione avanzata del servizio di reporting](../getting-started/business-intelligence.md)**— Questa impostazione di configurazione è disabilitata per impedire l&#39;utilizzo di PHI per l&#39;analisi e il reporting.
