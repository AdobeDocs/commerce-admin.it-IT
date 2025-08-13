---
title: Strumenti del sito Google
description: Scopri le integrazioni degli strumenti di Google che puoi utilizzare per ottimizzare i contenuti, analizzare il traffico e collegare il catalogo ad aggregatori di acquisti e marketplace.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Strumenti del sito Google

La configurazione del negozio è integrata con i seguenti strumenti di Google per ottimizzare i contenuti, analizzare il traffico e collegare il catalogo ad aggregatori di acquisti e marketplace.

- [Google Analytics](google-analytics.md) - Utilizza _Google Universal Analytics_ per definire dimensioni e metriche personalizzate aggiuntive per il tracciamento, con supporto per le interazioni offline e con le app mobili e accesso agli aggiornamenti in corso.

- [Gestione tag Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Utilizza Gestione tag Google per gestire i numerosi tag relativi agli eventi delle campagne di marketing.

- [Google AdWords](google-adwords.md) - Crea una campagna Google AdWords e tieni traccia delle conversioni per il tuo archivio.

{{gtag-api-note}}

## Impostazioni privacy Google

Se la tua azienda deve rispettare le normative sulla privacy come [RGPD](../getting-started/compliance-gdpr.md) o [CCPA](../getting-started/compliance-ccpa.md), modifica le impostazioni predefinite degli strumenti di Google per soddisfare i requisiti sulla privacy. Segui questi passaggi per assicurarti che l’utilizzo dei dati dei clienti sia conforme alle normative.

### Passaggio 1: aggiornare le impostazioni di Google

1. [Accedi][1]{: target="_blank"} all&#39;account Google Analytics della tua azienda.

1. Nella parte inferiore della barra laterale sinistra, scegli **[!UICONTROL Admin]**, quindi individua l&#39;account che desideri modificare (se applicabile).

1. Nella colonna **[!UICONTROL Account]** fare clic su **[!UICONTROL Account Settings]**.

1. Disattiva la condivisione dei dati per soddisfare i requisiti della normativa sulla privacy.

   Le impostazioni predefinite di Google Analytics condividono i dati aziendali con Google e altre parti. Per disattivare la condivisione dei dati, deselezionare la casella di controllo di selezione per le impostazioni seguenti:

   - Prodotti e servizi Google
   - Benchmarking
   - Supporto tecnico
   - Account specialists

1. Accetta la _modifica elaborazione dati_.

   I Termini di elaborazione dei dati di Google Ads descrivono il modo in cui Google elabora i dati e le misure adottate per garantire la sicurezza dei dati per le aziende soggette al RGPD. Con la modifica viene inoltre conservato un registro delle persone giuridiche e delle informazioni di contatto. Per [ulteriori informazioni][2]{: target="_blank"}, fare clic sul collegamento nel messaggio nella parte superiore della pagina.

   - Scorrere la pagina fino a **[!UICONTROL Data Processing Amendment]**.
   - Fai clic su **[!UICONTROL Review Amendment]** per leggere i _Termini di elaborazione dati di Google Ads_.
   - Fare clic su **[!UICONTROL Accept]**.
   - Fare clic su **[!UICONTROL Save]**.

1. Completare i dettagli di _Amministrazione DPA_.

   - Fare clic su **[!UICONTROL Manage DPA Details]** per aprire una pagina di amministrazione DPA in cui è possibile modificare i contatti e le persone giuridiche dell&#39;organizzazione.

   - Nella sezione **[!UICONTROL Legal Entities]**, fai clic sull&#39;icona _Modifica_ ( ![icona Modifica Google](./assets/google-icon-edit.png) ) e aggiungi uno o più nomi registrati per la tua organizzazione. Al termine, fare clic su **[!UICONTROL Save]**.

   - Nella sezione **Contatti**, fai clic sull&#39;icona _Aggiungi_ ( ![icona di aggiunta di Google](./assets/google-icon-add.png) ) e immetti le informazioni per il primo contatto. Selezionare quindi la casella di controllo di ogni ruolo applicabile e fare clic su **[!UICONTROL Add]**.

      - Contatto principale - (Indirizzo e-mail di notifica) Il contatto a cui vengono inviate le notifiche.
      - Responsabile della protezione dei dati: (se applicabile) la persona designata per facilitare la conformità alla normativa sulla privacy.
      - Rappresentante dello Spazio economico europeo (SEE): (se applicabile) la persona che rappresenta i clienti al di fuori dell’UE in relazione ai loro obblighi in materia di RGPD.

     Ripetere l&#39;operazione per aggiungere un altro contatto, se applicabile.

### Passaggio 2: modificare le librerie JS di Google

Google supporta tre librerie JavaScript per misurare l&#39;utilizzo del sito Web, a seconda del prodotto Google: `gtag.js`, `analytics.js` e `ga.js`. Per soddisfare i requisiti di privacy, il codice standard può essere modificato come segue:

#### Anonimizzare gli indirizzi IP

Per rendere anonimi gli indirizzi IP utilizzati da **_Google Universal Analytics_**, aggiungere il frammento seguente alla libreria `analytics.js` nel server Web:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Per ulteriori informazioni, consulta la [Guida di riferimento per i campi di Analytics.js][3]{: target="_blank"} nella Guida di Google.

Se si utilizza la libreria `ga.js` legacy, aggiungere il frammento seguente:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Per rendere anonimi gli indirizzi IP utilizzati da **_Google Tag Manager_**, impostare il parametro `anonymize_ip` su `true` nella libreria `gtag.js` del server Web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Per ulteriori informazioni, vedere [Anonimizzazione IP in Analytics][4] nella Guida di Google.

#### Forza SSL

Per forzare la trasmissione di tutti i dati Google su un livello di socket sicuro (SSL), aggiungere il seguente frammento alla libreria `analytics.js` sul server Web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Passaggio 3: aggiornare l’informativa sulla privacy

Aggiorna l&#39;[informativa sulla privacy](../getting-started/privacy-policy.md) per indicare che la tua azienda:

- Utilizza Google Analytics
- Maschera gli indirizzi IP per nascondere le informazioni personali
- Ha disattivato Condivisione dati di Google
- Non utilizza altri servizi Google con i cookie di Google Analytics

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
