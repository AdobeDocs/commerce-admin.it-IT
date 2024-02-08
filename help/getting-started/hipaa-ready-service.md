---
title: Preparazione HIPAA su Adobe Commerce
description: Scopri come aggiungere il modulo HIPAA-Ready di Adobe Commerce e ottenere funzioni e funzionalità aggiuntive per rispettare gli obblighi HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 3364a07b4c79a60ed813bf669a04711b69dae6f9
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---

# Preparazione HIPAA su Adobe Commerce

>[!IMPORTANT]
>
>**Dichiarazione di non responsabilità legale**<br/>
>Queste informazioni hanno lo scopo di aiutare i clienti Adobi a rispondere alle loro domande sui servizi compatibili con HIPAA di Adobe. Non si tratta di una consulenza legale. Gli esercenti devono consultare il proprio consulente legale per comprendere i propri obblighi ai sensi dell&#39;HIPAA e l&#39;uso e la configurazione appropriati dei prodotti Adobe.

## Health Insurance Portability and Accountability Act (HIPAA)

Il Health Insurance Portability and Accountability Act (HIPAA) è la principale legge federale sulla privacy sanitaria negli Stati Uniti ed è applicato dal Dipartimento della Salute e dei Servizi Umani (HHS). L’HIPAA si applica a _Entità coperte_ (ad esempio prestatori di assistenza sanitaria, assicuratori e stanze di compensazione) e _Associati commerciali_ (quali gli enti che forniscono servizi agli enti disciplinati). I requisiti HIPAA sono impostati in tre regole separate: Regola di privacy, Regola di sicurezza e Regola di notifica delle violazioni. Adobe funge da Business Associate per alcuni prodotti, che Adobe classifica come &quot;HIPAA-Ready Services&quot;. I dati disciplinati dall’HIPAA sono denominati _Informazioni sulla salute protette_ o PHI. Il PHI è un sottoinsieme di informazioni sulla salute che (1) è creato o ricevuto da un operatore sanitario, un piano sanitario o un centro di assistenza sanitaria, (2) si riferisce alla salute fisica o mentale o alle condizioni di un individuo passate, presenti o future, alla fornitura di assistenza sanitaria a un individuo, o al pagamento passato, presente o futuro per la fornitura di assistenza sanitaria a un individuo, e (3) identifica l&#39;individuo o in relazione al quale vi è una base ragionevole per credere che le informazioni possano essere utilizzate per identificare l&#39;individuo. Le Regole sulla privacy e sulla sicurezza HIPAA richiedono che un&#39;entità coperta ottenga garanzie scritte da un associato commerciale sotto forma di un Contratto di associazione commerciale (Business Associate Agreement, BAA), che richiedano all&#39;associato commerciale di salvaguardare la privacy e la sicurezza del PHI dellʼentità coperta.

## Predisposto per Adobe Commerce HIPAA

Adobe Commerce HIPAA-Ready dispone di funzioni e funzionalità aggiuntive che consentono ai commercianti di adempiere ai rispettivi obblighi HIPAA. È possibile installare Adobe Commerce HIPAA-Ready (`magento/hipaa-ee`) all&#39;infrastruttura cloud di Adobe Commerce. Ci sono anche alcune funzionalità che devono essere disabilitate per essere conformi con HIPAA.

*Questi materiali sono esclusivamente a scopo informativo. La comunicazione di tali informazioni non conferisce al destinatario alcun diritto contrattuale o di altro tipo. Sebbene siano stati compiuti sforzi per garantire l&#39;accuratezza delle informazioni alla data in cui sono state fornite, non viene fatta alcuna dichiarazione che tali informazioni siano esatte e complete e l&#39;Adobe non si assume alcun obbligo di aggiornare tali informazioni quando la normativa o i prodotti dell&#39;Adobe cambiano. Inoltre, il presente documento non deve essere distribuito ad alcuna parte diversa dal destinatario previsto senza il consenso scritto di Adobe.*

## Requisiti di sistema

La conformità HIPAA su Adobe Commerce ha gli stessi requisiti di sistema di Adobe Commerce con i requisiti aggiuntivi:

- Adobe Commerce versione 2.4.6-p3 o successiva (non beta)
- Adobe Commerce su infrastruttura cloud o Adobe Commerce su Managed Services
- Ultima versione di `magento/hipaa-ee` estensione

## Installazione

I servizi HIPAA-Ready di Adobe sono tecnicamente un metapacchetto compositore `magento/hipaa-ee` che contiene collegamenti a moduli speciali. Questo metapacchetto risiede nell’archivio [repo.magento.com](https://repo.magento.com).

1. Per poter installare `magento/hipaa-ee` metapackage, devi averne accesso. Per generare le chiavi e ottenere i diritti necessari, consulta [Ottieni le chiavi di autenticazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Controlla l’ambiente in cui installerai il pacchetto e assicurati che soddisfi i requisiti generali [requisiti di sistema](#system-requirements).

1. Aggiungi il metapacchetto `magento/hipaa-ee` alla configurazione del compositore.

   Il modo più semplice è quello di utilizzare il Compositore CLI. Ad esempio:

   ```shell
   composer require magento/hipaa-ee
   ```

1. Se Adobe Commerce non è ancora installato, puoi avviare l’installazione (segui la [Istruzioni di installazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Se Adobe Commerce è già installato, dopo aver scaricato i moduli esegui `bin/magento setup:upgrade` e quindi seguire le raccomandazioni.

   ```shell
   bin/magento setup:upgrade
   ```

   Quando questo comando è in esecuzione, i moduli appena scaricati vengono attivati e gli script per installarli vengono avviati. Per ulteriori informazioni sulla gestione dei moduli, consulta [Abilitare o disabilitare i moduli](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. Al termine dell&#39;installazione o dell&#39;aggiornamento, è necessario verificare se `Hipaa*` sono stati inclusi moduli pertinenti.

   Esegui il comando:

   ```shell
   bin/magento module:status
   ```

   Se il pacchetto del compositore HIPAA è stato aggiunto correttamente, i moduli HIPAA vengono visualizzati nell&#39;output del comando. Ad esempio:

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

La registrazione dei controlli è un requisito HIPAA. In Adobe Commerce, il [Registri azioni](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) Questa funzione registra ogni modifica apportata da un utente amministratore che lavora nel tuo store. Per soddisfare i requisiti HIPAA relativi al registro di controllo, sono state apportate modifiche alla funzione per registrare tutte le azioni degli utenti e dei clienti amministratori eseguite tramite l’interfaccia utente di amministrazione e tramite chiamate API.

#### Rapporto Registri azioni

Il _Registri azioni_ griglia dei rapporti (**[!UICONTROL System]** > Action Logs > Report) è stato modificato per adattarsi alle azioni dei clienti eseguite tramite l’interfaccia utente e l’API di amministrazione.

1. Due colonne aggiuntive:
   - ***Sorgente***: mostra dove è stata eseguita l’azione.\
     Valori: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo di client***: visualizza il tipo di client.\
     Valori: Cliente | Amministratore | Integrazione


2. Rinomina ***Nome utente*** a ***Identificatore client***
   - ***Identificatore client***: visualizza l’ID di accesso dell’utente che ha eseguito l’azione\
     Valori:
      - un messaggio e-mail se il tipo di client è Cliente
      - un nome utente se il tipo di client è Admin
      - un nome se il tipo di client è Integrazione

3. Rinomina ***Nome azione completo*** a ***Target***
   - ***Target***: visualizza il nome dell’azione\
     Valori:
      - un endpoint se Source è REST API o SOAP API
      - un nome di query/mutazione se GraphQL API
      - un nome di azione se interfaccia utente amministratore o interfaccia utente cliente.

#### Configurare le azioni amministratore per la registrazione

Questa funzione non è disponibile perché tutte le azioni devono essere registrate per impostazione predefinita.

### Funzioni di importazione/esportazione

I miglioramenti apportati alle funzioni di importazione/esportazione si concentrano sul miglioramento dell’esperienza amministrativa e sulla fornitura di una migliore visibilità sulle azioni degli utenti.

>[!NOTE]
>
>Questi ***I miglioramenti non alterano la logica di base Importa/Esporta***; estendono invece la funzionalità per offrire una registrazione più completa e una migliore attribuzione dei dati. Le funzionalità fondamentali di importazione/esportazione rimangono invariate. Gli utenti possono continuare a utilizzare le funzioni e i flussi di lavoro esistenti senza interruzioni.

#### Registrazione azioni amministrative

Uno dei principali miglioramenti delle funzioni di importazione/esportazione è la registrazione avanzata delle azioni amministrative. Questo introduce la possibilità di approfondire le attività associate all’importazione/esportazione dei dati, contribuendo a migliorare il tracciamento e la verificabilità. Le seguenti azioni vengono ora registrate e riportate nel **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**griglia:

| Tipo | Azioni |
| ---- | ------- |
| Importa | <ul><li>Un utente amministratore esegue un’importazione<li>Un utente amministratore scarica un file importato<li>Un utente amministratore scarica un file di errore<ul/> |
| Esporta | <ul><li>Richieste di utenti amministratore<li>Un utente amministratore scarica un file esportato<ul/> |
| Importazioni/esportazioni programmate | <ul><li>Un utente amministratore pianifica l’esportazione<li>Un utente amministratore modifica un’esportazione pianificata<li>Un utente amministratore esegue un’esportazione pianificata<li>Un utente amministratore elimina un’esportazione pianificata<li>Un utente amministratore pianifica un’importazione<li>Un utente amministratore modifica un’importazione pianificata<li>Un utente amministratore esegue un’importazione pianificata<li>Un utente amministratore elimina un’importazione pianificata<li>Un utente amministratore esegue un’eliminazione in blocco delle operazioni di importazione/esportazione<ul/> |

### Miglioramenti alla visualizzazione e miglioramento di filtri/ordinamenti

Per consentire agli utenti amministratori di disporre di griglie con maggiori informazioni, sono stati apportati diversi miglioramenti alla visualizzazione dei dati e alle funzionalità di filtro e ordinamento:

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

#### Importazioni/esportazioni programmate ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- È stato aggiunto un **[!UICONTROL ID]** colonna.
- È stato aggiunto un **[!UICONTROL Scheduled At]** column (_data e ora in cui è stata pianificata l’importazione o l’esportazione_).
- È stato aggiunto un **[!UICONTROL User]** column (_nome utente di un utente amministratore che ha pianificato l’importazione/esportazione_).

## Funzioni disattivate per la conformità HIPAA

### Servizi SaaS

Nessuno dei servizi SaaS offerti per Adobe Commerce è disponibile nell’ambito dell’offerta compatibile con HIPAA. Ciò include, ma non è limitato a:

- Live Search
- Mesh API
- App Builder
- Servizio catalogo

### Estrazione guest disattivata per impostazione predefinita

- Il checkout degli ospiti presenta un potenziale rischio per vari aspetti dell&#39;HIPAA, tra cui la registrazione, il controllo degli accessi, l&#39;igiene e la derivazione PHI, e potenzialmente di più.
- Il Checkout ospite è disabilitato per impostazione predefinita nel modulo di preparazione HIPAA, ma può essere abilitato dai miei commercianti a proprio rischio e pericolo.

### Funzione newsletter disabilitata per impostazione predefinita

- La funzione newsletter è disabilitata per impostazione predefinita per impedire l’utilizzo di PHI in un contesto di marketing, ma può essere abilitata dal commerciante a proprio rischio.

### Impostazione predefinita del servizio Advanced Reporting disabilitata

L’impostazione del servizio di reporting avanzato è disabilitata per impostazione predefinita per impedire l’utilizzo di PHI per l’analisi e il reporting, ma può essere abilitata dall’esercente a proprio rischio.
