---
title: Strumenti del sito Google
description: Scopri le integrazioni degli strumenti di Google che puoi utilizzare per ottimizzare i contenuti, analizzare il traffico e collegare il catalogo ad aggregatori di acquisti e marketplace.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Strumenti del sito Google

La configurazione del negozio è integrata con i seguenti strumenti di Google per ottimizzare i contenuti, analizzare il traffico e collegare il catalogo ad aggregatori di acquisti e marketplace.

- [Google Analytics](google-analytics.md) - Utilizzo _Google Universal Analytics_ definire dimensioni e metriche personalizzate aggiuntive per il tracciamento, con supporto per le interazioni offline e con le app mobili e accesso agli aggiornamenti continui.

- [Esperimenti sui contenuti Google](google-content-experiments.md) : configura un test A/B per prodotti, categorie o pagine di contenuti utilizzando gli esperimenti sui contenuti Google Analytics.

- [Gestione tag Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) Solo per Adobe Commerce: utilizza Google Tag Manager per gestire i numerosi tag relativi agli eventi delle campagne di marketing.

- [Google AdWords](google-adwords.md) : crea una campagna Google AdWords e tieni traccia delle conversioni per il tuo store.

{{gtag-api-note}}

## Impostazioni privacy Google

Se la tua azienda deve rispettare le normative sulla privacy come [RGPD](../getting-started/compliance-gdpr.md) o [CCPA](../getting-started/compliance-ccpa.md), modifica le impostazioni predefinite degli strumenti di Google per soddisfare i requisiti di privacy. Segui questi passaggi per assicurarti che l’utilizzo dei dati dei clienti sia conforme alle normative.

### Passaggio 1: aggiornare le impostazioni di Google

1. [Accedi][1]{: target=&quot;_blank&quot;} all’account di Google Analytics della tua azienda.

1. Nella parte inferiore della barra laterale sinistra, scegli **[!UICONTROL Admin]**, quindi individuare l&#39;account che si desidera modificare (se applicabile).

1. In **[!UICONTROL Account]** , fare clic su **[!UICONTROL Account Settings]**.

1. Disattiva la condivisione dei dati per soddisfare i requisiti della normativa sulla privacy.

   Le impostazioni di Google Analytics predefinite condividono i dati aziendali con Google e altre parti. Per disattivare la condivisione dei dati, deselezionare la casella di controllo di selezione per le impostazioni seguenti:

   - Prodotti e servizi Google
   - Benchmarking
   - Supporto tecnico
   - Account specialists

1. Accetta _Modifica elaborazione dati_.

   I Termini di elaborazione dei dati di Google Ads descrivono il modo in cui Google elabora i dati e le misure adottate per garantire la sicurezza dei dati per le aziende soggette al RGPD. Con la modifica viene inoltre conservato un registro delle persone giuridiche e delle informazioni di contatto. A [ulteriori informazioni][2]{: target=&quot;_blank&quot;}, fai clic sul collegamento nel messaggio nella parte superiore della pagina.

   - Scorri verso il basso fino a **[!UICONTROL Data Processing Amendment]**.
   - Clic **[!UICONTROL Review Amendment]** per leggere _Termini di elaborazione dei dati di Google Ads_.
   - Clic **[!UICONTROL Accept]**.
   - Clic **[!UICONTROL Save]**.

1. Completa il _Amministrazione DPA_ dettagli.

   - Clic **[!UICONTROL Manage DPA Details]** per aprire una pagina di amministrazione di DPA in cui è possibile modificare i contatti e le persone giuridiche dell&#39;organizzazione.

   - In **[!UICONTROL Legal Entities]** , fare clic sul pulsante _Modifica_ ( ![Icona modifica Google](./assets/google-icon-edit.png) ) e aggiungi uno o più nomi registrati per la tua organizzazione. Al termine, fai clic su **[!UICONTROL Save]**.

   - In **Contatti** , fare clic sul pulsante _Aggiungi_ ( ![Icona di aggiunta Google](./assets/google-icon-add.png) ) e immettere le informazioni per il primo contatto. Quindi, seleziona la casella di controllo di ciascun ruolo applicabile e fai clic su **[!UICONTROL Add]**.

      - Contatto principale - (Indirizzo e-mail di notifica) Il contatto a cui vengono inviate le notifiche.
      - Responsabile della protezione dei dati: (se applicabile) la persona designata per facilitare la conformità alla normativa sulla privacy.
      - Rappresentante dello Spazio economico europeo (SEE): (se applicabile) la persona che rappresenta i clienti al di fuori dell’UE in relazione ai loro obblighi in materia di RGPD.

     Ripetere l&#39;operazione per aggiungere un altro contatto, se applicabile.

### Passaggio 2: modificare le librerie JS di Google

Google supporta tre librerie JavaScript per misurare l’utilizzo del sito web, a seconda del prodotto Google: `gtag.js`, `analytics.js`, e `ga.js`. Per soddisfare i requisiti di privacy, il codice standard può essere modificato come segue:

#### Anonimizzare gli indirizzi IP

Per rendere anonimi gli indirizzi IP utilizzati da **_Google Universal Analytics_**, aggiungi lo snippet seguente al `analytics.js` libreria sul server web:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Per ulteriori informazioni, consulta [Guida di riferimento per i campi di Analytics.js][3]{: target=&quot;_blank&quot;} nella Guida di Google.

Se utilizzi il precedente `ga.js` , aggiungi il seguente snippet:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Per rendere anonimi gli indirizzi IP utilizzati da **_Gestione tag Google_**, imposta `anonymize_ip` parametro a `true` nel `gtag.js` sul server web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Per ulteriori informazioni, consulta [Anonimizzazione degli IP in Analytics][4] nella Guida di Google.

#### Forza SSL

Per forzare la trasmissione di tutti i dati Google su un livello di socket sicuro (SSL), aggiungi il seguente snippet al `analytics.js` sul server web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Passaggio 3: aggiornare l’informativa sulla privacy

Aggiorna il tuo [informativa sulla privacy](../getting-started/privacy-policy.md) per dichiarare che la tua azienda:

- Usa Google Analytics
- Maschera gli indirizzi IP per nascondere le informazioni personali
- Ha disattivato Condivisione dati di Google
- Non utilizza altri servizi Google con i cookie Google Analytics

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
