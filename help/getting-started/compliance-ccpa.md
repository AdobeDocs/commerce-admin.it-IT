---
title: Conformità CCPA
description: Scopri il California Consumer Privacy Act (CCPA), che estende i diritti dei consumatori in California per determinare come vengono raccolte, memorizzate e utilizzate le loro informazioni personali.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2256'
ht-degree: 0%

---

# Conformità CCPA

>[!NOTE]
>
>Queste informazioni fanno parte di una serie di argomenti che consentono ai commercianti e agli sviluppatori di Adobe Commerce di comprendere le implicazioni del California Consumer Privacy Act. Le informazioni si basano sul testo dello statuto. Per verificare se il CCPA è applicabile alla tua attività, rivolgiti al tuo avvocato.

Il [California Consumer Privacy Act][5] (CCPA) estende i diritti dei consumatori in California per determinare in che modo le loro informazioni personali vengono raccolte, memorizzate e utilizzate. L&#39;accento è posto sulla protezione dei consumatori dalla vendita o dallo scambio non autorizzati o dalle loro informazioni personali. Il CCPA è stato approvato nel 2018 ed è entrato in vigore il 1° gennaio 2020.

Il CCPA conferisce ai consumatori i seguenti nuovi diritti:

- **Diritto di conoscere** le categorie di informazioni personali raccolte, utilizzate, condivise o vendute negli ultimi 12 mesi.
- **Diritto di eliminare** alcuni tipi di informazioni personali in possesso di un&#39;azienda e/o dei relativi provider di servizi.
- **Diritto di rinuncia** alla vendita delle informazioni personali.
- **Diritto alla non discriminazione** in termini di prezzo o di servizio per aver esercitato un diritto alla privacy in base al CCPA.

Ai fini del CCPA, le informazioni personali in questo contesto sono definite come:

>Informazioni che identificano, si riferiscono, descrivono, possono essere associate o ragionevolmente collegate, direttamente o indirettamente, a uno specifico consumatore o famiglia. (Sezione 1798.140)

A questo proposito, copre alcuni elementi di dati che non possono essere considerati dati personali nel contesto di altre leggi o regolamenti. I commercianti devono tenerlo presente quando decidono se e come conformarsi alla legge.

Il CCPA richiede inoltre alle aziende di fornire _una ragionevole sicurezza_ e include disposizioni più ampie sulla protezione dei dati per i consumatori, incluso il diritto di intraprendere azioni legali in caso di violazione dei dati.

Rivolgiti al tuo consulente legale per determinare se e come è necessario conformarsi ai requisiti del CCPA che possono essere applicabili a te e alla tua azienda. Ciò include i nuovi requisiti di notifica, rinuncia e conservazione dei documenti che le aziende devono implementare in conformità alla legge.

## Requisiti aziendali

Il CCPA si applica alle aziende a scopo di lucro che operano in California e soddisfano uno dei seguenti requisiti:

- Avere un fatturato lordo annuo di oltre 25 milioni di dollari
- Acquistare, ricevere o vendere le informazioni personali di almeno 100.000 residenti in California, famiglie o dispositivi
- Ottieni il 50% o più dei ricavi annuali dalla vendita delle informazioni personali dei residenti della California.

## Guida alla conformità CCPA

Questa sezione fornisce un profilo di alto livello dei passaggi necessari affinché gli esercenti rispettino le normative sulla privacy, come il California Consumer Privacy Act (CCPA).

### RGPD e CCPA

Se la tua azienda deve rispettare sia il [Regolamento generale sulla protezione dei dati](compliance-gdpr.md) (RGPD) che il CCPA, puoi utilizzare parte del lavoro svolto dal programma di conformità al RGPD per il CCPA. Anche se le normative hanno alcune somiglianze, alcune differenze includono:

- La definizione di informazioni personali varia a seconda del regolamento.
- Il RGPD richiede ai consumatori di dare il consenso prima che i loro dati personali possano essere utilizzati per alcuni scopi; il CCPA fornisce ai consumatori il diritto di negare il consenso.
- Il CCPA prevede requisiti aggiuntivi per l&#39;inventario dei dati e la mappatura.
- Le normative hanno requisiti diversi in materia di informativa sulla privacy.

Le aziende che si conformano al RGPD potrebbero avere obblighi aggiuntivi ai sensi del CCPA. Per ulteriori informazioni, consulta la [Scheda informativa CCPA][3]{:target=&quot;_blank&quot;}.

### Roadmap di conformità

È necessario uno sforzo coordinato per sviluppare e attuare un piano volto a garantire la conformità. Utilizza questa roadmap come guida per mobilitare le risorse e assegnare priorità alle attività in modo da poter procedere su più fronti. Il processo è essenzialmente lo stesso per tutte le installazioni di [!DNL Commerce], con la seguente eccezione:

- **Adobe Commerce sull&#39;infrastruttura cloud**: i commercianti con negozi ospitati nell&#39;Adobe [infrastruttura cloud][4]{:target=&quot;_blank&quot;} possono richiedere al proprio Adobe Commerce Technical Account Manager o al Supporto tecnico di rispondere alle richieste dei consumatori.

- **On-Premise**: i commercianti con installazioni on-premise di Adobe Commerce o di un Magento Open Source devono sviluppare i propri processi e strumenti per rispondere e gestire le richieste dei consumatori relative alle normative sulla privacy.

#### Passaggio 1: riunire un team cross-functional per gestire il problema della conformità normativa

Crea un team che rappresenti i seguenti ruoli funzionali nella tua azienda e pianifica una sessione di formazione per aggiornarli sulla legislazione. Quindi, assegna le attività richieste alle parti interessate per ruolo.

- Strategia e operazioni aziendali
- Note legali
- Information Technology
- Esperienza utente
- Servizio clienti
- Supporto amministrativo

Dal punto di vista aziendale, devi determinare se l’azienda estende queste misure di protezione della privacy solo ai consumatori della California, o le rende disponibili a tutti i consumatori, indipendentemente dalla loro posizione.

#### Passaggio 2: fare l’inventario delle proprietà digitali

**Parti interessate:** Supporto legale, amministrativo e IT

Crea un inventario delle tue proprietà digitali, comprese tutte le integrazioni e gli utenti che hanno accesso ai dati dei tuoi consumatori.

1. Determina quali informazioni personali pubbliche e private vengono raccolte tramite i tuoi siti web e le tue app mobili. Un database Commerce standard, ad esempio, memorizza i seguenti tipi di informazioni personali pubbliche e private:

   - **Pubblico**: elenchi dei desideri, recensioni dei prodotti

   - **Privato**: Informazioni Cliente, Informazioni Ordine, Punti Premio, Registro Regali, Rubrica, Credito Negozio, Metodi Di Pagamento, Contratti Di Fatturazione, Iscrizioni Newsletter, Inviti.

     Se l&#39;installazione di [!DNL Commerce] è stata personalizzata, è possibile che vengano raccolte informazioni personali aggiuntive. Le informazioni personali potrebbero inoltre risiedere in [cookie](./compliance-cookie-law.md), tag e altre tecnologie che raccolgono informazioni.

1. Identifica le parti con cui condividi i dati. L&#39;elenco dovrebbe includere i prestatori di servizi e i terzi. Le terze parti includono reti pubblicitarie, fornitori di servizi Internet, fornitori di analisi dei dati, enti governativi, sistemi operativi e piattaforme, social network e rivenditori di dati dei consumatori che non raccolgono direttamente informazioni personali dai tuoi consumatori.

   - **Fornitori di servizi**: entità che hanno accesso ai tuoi dati dei consumatori per uno scopo aziendale e forniscono servizi per tuo conto. Ad Adobe, è un provider di servizi, così come alcuni sviluppatori di personalizzazioni, estensioni e servizi.

     Controlla le impostazioni predefinite di Google Universal Analytics, Google Tag Manager e di tutti gli altri servizi dati utilizzati e apporta le modifiche necessarie per rispettare il regolamento. Per ulteriori informazioni, consulta [Impostazioni privacy di Google](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Altre terze parti**: entità con cui condividi o vendi dati di consumo. Ad esempio, puoi condividere i dati dei consumatori con una rete pubblicitaria in cambio di pubblicità.

#### Passaggio 3: mappare il percorso del cliente e il processo di raccolta dei dati nei negozi

**Parti interessate:** Esperienza utente, Tecnologia dell&#39;informazione, Supporto amministrativo

1. Identificare ogni punto del [percorso di clienti] in cui vengono raccolte le informazioni personali e il tipo di informazioni raccolte in ogni passaggio.

   I visitatori del tuo sito devono essere avvisati in anticipo, o al punto di raccolta dei dati. Ad esempio, un archivio senza integrazioni personalizzate raccoglie informazioni personali durante la creazione di un account cliente e durante il pagamento. Se il tuo archivio dispone di integrazioni personalizzate, ci potrebbero essere elementi di dati e attributi aggiuntivi da identificare.

1. Per i diagrammi di flusso dei dati e i mapping di entità di database applicabili a ogni versione, vedere i seguenti argomenti:

   - [Riferimento informazioni personali (2.x)][1]
   - [Riferimento informazioni personali (1.x)][2]

   ![diagramma](./assets/privacy-frontend-diagram.svg)

#### Passaggio 4: stabilire procedure e meccanismi per rispondere alle richieste dei clienti

**Parti interessate:** Servizio clienti, Information Technology, Esperienza utente, Supporto amministrativo

Dal punto di vista della gestione dei dati, ogni richiesta di informazioni personali coinvolge le seguenti parti:

- **Interessati** (Consumatori): in base al CCPA, qualsiasi persona in California che fornisce informazioni personali per effettuare un acquisto e/o gestire un account cliente potrebbe inviare una richiesta per accedere ai propri dati personali o eliminarli.

- **Entità operanti come aziende nell&#39;ambito del CCPA** (marchi): [!DNL Commerce] commercianti raccolgono e archiviano informazioni personali dai propri clienti e ospiti che effettuano acquisti nei propri negozi.

- **Responsabile del trattamento dei dati** (fornitori di tecnologia): Adobe Commerce e il Magento Open Source fungono da responsabili del trattamento dei dati personali memorizzati nell&#39;ambito dei servizi forniti ai commercianti. In qualità di responsabile del trattamento, Adobe tratta i dati personali in conformità alle autorizzazioni e alle istruzioni dell’esercente, in base al contratto di licenza.

I commercianti sono responsabili di:

1. Identifica le parti coinvolte nella richiesta di accesso dell’interessato (DSAR) e verifica l’identità di chiunque richieda di esserne a conoscenza, rinunciarvi o eliminarlo. Questo vale per una persona che ha un account cliente protetto da password o che fa acquisti nel tuo negozio come ospite.

1. Divulgare e fornire informazioni a un consumatore in risposta alla sua richiesta di diritti entro 45 giorni dal ricevimento di una richiesta verificabile da parte del consumatore, a meno che ciò non sia possibile. (La legge contiene alcuni altri requisiti che impongono alle aziende di mantenere la conformità per ritardi fino a 45 giorni aggiuntivi).

   I commercianti devono rispondere a ciascuna DSAR entro 45 giorni, a partire dal giorno di ricezione della richiesta. Se necessario, i commercianti possono richiedere fino a 45 giorni in più per rispondere, per un totale massimo di 90 giorni dal giorno in cui viene ricevuta la richiesta. Ciò richiede che l&#39;esercente informi il cliente per spiegare il motivo del ritardo.

1. Sviluppa un meccanismo per presentare le notifiche richieste nel tuo store e raccogliere le risposte dei consumatori.

1. Stabilisci le procedure di risposta e documenta ciascuna delle seguenti richieste:

   - **Richieste di informazioni** - I visitatori del tuo Negozio devono essere informati di qualsiasi accordo in base al quale devi vendere o condividere le loro informazioni personali con terze parti e deve essere loro consentito di rinunciare. I dettagli sull&#39;utilizzo dei dati personali e le parti con cui si condividono o si vendono i dati possono essere mantenuti nell&#39;informativa sulla privacy.

   - **Richieste di rinuncia** - Se i dati personali vengono venduti o trasferiti a terzi in cambio di un corrispettivo prezioso, il CCPA richiede un collegamento _Non vendere le mie informazioni_ in ogni punto in cui vengono raccolti. Ulteriori controlli di input abilitati dall’utente, come caselle di controllo e pulsanti, possono essere utilizzati nelle comunicazioni e-mail, nelle impostazioni delle preferenze del sito web o nei moduli del sito web al punto di raccolta dei dati per consentire ai singoli utenti di inviare una richiesta di rinuncia valida.

   - **Richieste da eliminare**

      - I commercianti i cui negozi sono ospitati su Adobe Commerce Cloud devono contattare il supporto Adobe per assistenza nell’eliminazione di informazioni personali. Per ulteriori informazioni, contatta l’Adobe Technical Account Manager o l’Assistenza clienti.
      - I commercianti che eseguono installazioni di Adobe Commerce o Magento Open Source on-premise devono implementare il proprio processo e script per eliminare le informazioni personali su richiesta.

#### Passaggio 5: scrivi il contenuto per le notifiche cliente richieste

**Parti interessate:** Assistenza legale, Servizio clienti, Esperienza utente, Tecnologia dell&#39;informazione, Supporto amministrativo

1. In collaborazione con il tuo consulente legale, determina i tipi di avvisi da aggiungere al sito web per adempiere agli obblighi previsti dal CCPA.

   - **Avviso di raccolta**: un avviso dato in corrispondenza o prima dell&#39;ora in cui le informazioni personali vengono raccolte dal consumatore. L’avviso deve essere scritto in un linguaggio semplice e deve essere di facile comprensione per la persona media. L’avviso deve essere ben visibile e fornito in una o più lingue del contenuto del sito web.

   - **Avviso di diritto di rinuncia**: un avviso che informa i consumatori del loro diritto di rinuncia alla vendita delle loro informazioni personali.

   - **Avviso di incentivo finanziario**: un avviso che spiega ogni incentivo finanziario, prezzo o differenza di servizio ricevuto dalla società in cambio di informazioni personali.

   - **Come inviare una richiesta per la raccolta e l&#39;utilizzo di informazioni personali**: istruzioni per l&#39;invio di una richiesta di divulgazione delle informazioni personali raccolte sull&#39;utente, tra cui:

      - Informazioni personali specifiche raccolte sul consumatore
      - Categorie di informazioni personali raccolte sul consumatore
      - Categorie di fonti da cui vengono raccolte le informazioni personali
      - Categorie di informazioni personali sul consumatore che hai venduto o divulgato per uno scopo commerciale
      - Categorie di terzi a cui le informazioni personali sono state vendute o divulgate per uno scopo aziendale
      - I motivi per cui la tua azienda raccoglie e/o vende informazioni personali

1. Invia il contenuto al team e, se possibile, al tuo consulente legale per una revisione.

1. Determina dove vengono visualizzati gli avvisi, come funzionano (per ogni visita, all’autenticazione o al click-through), e la loro posizione e formato in relazione agli altri contenuti.

1. Passa il contenuto approvato al tuo team di sviluppo.

#### Passaggio 6: rivedi i contratti con i provider di servizi

**Parti interessate:** Supporto legale e amministrativo

Rivedi e, se necessario, aggiorna tutti i contratti dei fornitori di servizi per riflettere i requisiti del CCPA.

#### Passaggio 7: aggiornare l’informativa sulla privacy

**Parti interessate:** Supporto legale e amministrativo

Rivedi la tua attuale politica sulla privacy e considera quali informazioni aggiuntive sono necessarie, se presenti.

- **Utilizzo dei dati personali**: è necessario divulgare i dati personali raccolti e gli incentivi finanziari ricevuti in cambio della vendita dei dati personali. È inoltre necessario spiegare in che modo l’incentivo è consentito ai sensi del CCPA e come viene calcolato il valore delle informazioni personali.

- **Età del consenso**: se raccogli o utilizzi informazioni personali su minori, potresti essere soggetto ai seguenti requisiti:

   - **Minori &lt; 13**: per i minori di età inferiore ai 13 anni è necessaria l&#39;autorizzazione per i genitori a partecipare alla vendita dei propri dati personali.

   - **Minori di età compresa tra 13 e &lt; 16**: i minori di età compresa tra almeno 13 e 16 anni possono acconsentire alla vendita delle loro informazioni personali, a condizione che l&#39;azienda stabilisca un processo ragionevole per documentare l&#39;azione. Il processo deve essere descritto nell&#39;[informativa sulla privacy](privacy-policy.md) dell&#39;azienda. Quando un’azienda riceve richieste da minori di questa fascia di età, deve informarli del loro diritto di rinuncia in un secondo momento e spiegare come farlo.

  >[!IMPORTANT]
  >
  >Ai commercianti è vietato archiviare i dati personali dei bambini sulla piattaforma o sui sistemi [!DNL Commerce]. Se vi è motivo di ritenere che i dati raccolti appartengano a un minore, è necessario rimuoverli immediatamente da una piattaforma [!DNL Commerce] per evitare la violazione delle condizioni di licenza Adobe.

#### Passaggio 8: documentare tutte le procedure correlate e conservare i record

**Parti interessate:** Servizio clienti, supporto amministrativo

Per 24 mesi dopo il ricevimento di ogni singola richiesta di diritti, conserva un registro della richiesta e della risposta della tua azienda.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
