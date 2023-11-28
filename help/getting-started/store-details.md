---
title: Dettagli store
description: Scopri come aggiornare le informazioni di base per il tuo store.
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# Dettagli store

Le informazioni di base per il negozio includono il nome e l&#39;indirizzo del negozio, il numero di telefono e l&#39;indirizzo di posta elettronica visualizzati nei messaggi di posta elettronica, nelle fatture e in altre comunicazioni inviate ai clienti.

![Configurazione generale - Dettagli archivio](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

Il _[!UICONTROL Store Information]_La sezione fornisce le informazioni di base che vengono visualizzate nei documenti di vendita e in altre comunicazioni.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sotto **[!UICONTROL General]** nel pannello di navigazione a sinistra, scegli **[!UICONTROL General]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Store Information]** sezione.

   ![Configurazione generale - Informazioni archivio](./assets/general-store-information.png){width="700"}

1. Imposta le opzioni in base ai dettagli del tuo Negozio:

   - Inserisci il **[!UICONTROL Store Name]** che desideri utilizzare in tutte le comunicazioni.

   - Inserisci il **[!UICONTROL Store Phone Number]**, formattato nel modo desiderato.

   - Per **[!UICONTROL Store Hours of Operation]**, immettere gli orari in cui il negozio è aperto. Ad esempio: `Mon - Fri, 9-5, Sat 9-noon PST`.

   - Seleziona la **[!UICONTROL Country]** dove si trova la tua azienda.

   - Seleziona la **[!UICONTROL Region/State]** con il paese.

   - Inserisci il **[!UICONTROL Store Address]**. Se l&#39;indirizzo è lungo, continuare l&#39;indirizzo il **Indirizzo negozio riga 2**.

   - Se applicabile, inserire **[!UICONTROL VAT Number]** del tuo negozio.

     Per verificare il numero, fare clic su **[!UICONTROL Validate VAT Number]** pulsante. Per ulteriori informazioni, consulta [Convalida ID IVA](../stores-purchase/vat.md#vat-id-validation).

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni sulle opzioni di configurazione delle informazioni di archiviazione, vedere [_Guida di riferimento alla configurazione_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

Le impostazioni internazionali determinano il numero di impostazioni utilizzate nell&#39;archivio. Alcuni sono:

- Lingua
- Paese
- Aliquota fiscale
- Valuta
- Prezzo
- Formato numero

L&#39;impostazione locale determina il fuso orario e la lingua utilizzati per ciascun archivio e identifica i giorni della settimana lavorativa nell&#39;area.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL General]**, scegli **[!UICONTROL General]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Locale Options]** sezione.

   ![Configurazione generale - Opzioni internazionali](./assets/general-locale-options.png){width="700"}

1. Seleziona il **[!UICONTROL Timezone]** dall&#39;elenco.

1. Imposta **[!UICONTROL Locale]** nella lingua del negozio.

1. Imposta **[!UICONTROL Weight Unit]** all&#39;unità di misura utilizzata in genere per le spedizioni dalla lingua.

1. Imposta **[!UICONTROL First Day of the Week]** al giorno considerato come il primo giorno della settimana nella sua zona.

1. In **[!UICONTROL Weekend Days]** seleziona i giorni che cadono in un weekend nella tua area.

   Per selezionare più giorni, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ogni elemento.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni sulle opzioni di configurazione delle impostazioni locali, vedere [Guida di riferimento alla configurazione](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

In molti paesi, lo stato, la provincia o la regione è una parte obbligatoria di un indirizzo postale. Le informazioni vengono utilizzate per le informazioni relative alla spedizione e alla fatturazione, per il calcolo delle aliquote e così via. Per i paesi in cui lo stato non è obbligatorio, il campo può essere omesso completamente dall’indirizzo o incluso come campo facoltativo.

Poiché i formati di indirizzo standard variano da un paese all&#39;altro, è possibile modificare anche il modello utilizzato per formattare l&#39;indirizzo per fatture, documenti di trasporto ed etichette di spedizione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sotto **[!UICONTROL General]** nel pannello di navigazione a sinistra, scegli **[!UICONTROL General]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL State Options]** sezione.

   ![Configurazione generale - Opzioni stato](./assets/general-state-options.png){width="700"}

1. Utilizza il **[!UICONTROL State is required for]** per selezionare ogni paese in cui è richiesta la voce Regione/Stato.

1. Imposta **[!UICONTROL Allow to Choose State if it is Optional for Country]** a uno dei seguenti elementi:

   `Yes` - Nei paesi in cui il campo Stato non è obbligatorio, includere il campo Stato come voce facoltativa.

   `No` - Nei paesi in cui il campo Stato non è obbligatorio, omette il campo Stato.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni sulle opzioni di configurazione dello stato, vedere [Guida di riferimento alla configurazione](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

Le opzioni per paese identificano il paese in cui è situata la tua azienda e i paesi da cui accetti il pagamento.

### Imposta le opzioni paese per il tuo store

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL General]**, scegli **[!UICONTROL General]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Country Options]** sezione.

   >[!NOTE]
   >
   >Se necessario, cancellare il **[!UICONTROL Use system value]** per ogni impostazione che si desidera modificare.

   ![Configurazione generale - Impostazioni paese](./assets/general-country-options.png){width="700"}

1. Scegli la **[!UICONTROL Default Country]** dove si trova la tua azienda.

1. In **[!UICONTROL Allow Countries]** selezionare ogni paese dal quale si accettano gli ordini.

   Per impostazione predefinita, vengono selezionati tutti i paesi dell’elenco. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ogni elemento.

1. Utilizza il **[!UICONTROL Zip/Postal Code is Optional for]** elenco per selezionare ogni paese in cui si svolge un&#39;attività commerciale che non richiede l&#39;inclusione di un CAP nell&#39;indirizzo stradale.

1. In **[!UICONTROL European Union Countries]** selezionare ogni paese nell&#39;UE in cui si svolge la propria attività.

   Per impostazione predefinita, vengono selezionati tutti i paesi dell&#39;UE. Per selezionare i paesi desiderati, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ogni elemento.

1. In **[!UICONTROL Top Destinations]** selezionare i paesi principali di destinazione per le vendite.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Impostare le opzioni paese per un metodo di consegna specifico

È inoltre possibile configurare la spedizione a paesi specifici per ciascun paese disponibile [metodo di consegna](../stores-purchase/delivery.md) (UPS, FedEx e così via).

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Selezionare il vettore di spedizione a cui si desidera applicare paesi specifici.

1. Per **[!UICONTROL Ship to Applicable Countries]**, deseleziona la **[!UICONTROL Use system value]** e seleziona la **[!UICONTROL Specific Countries]** opzione.

1. In **[!UICONTROL Top Destinations]** selezionare i paesi principali di destinazione per la spedizione.

   ![Esempio di impostazione delle opzioni paese per il metodo di consegna DHL](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Risorse per la risoluzione dei problemi

Per assistenza nella risoluzione dei problemi di configurazione del paese, vedi quanto segue [!DNL Commerce] Articoli della Knowledge Base:

- [Come aggiungere un paese](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html)
- [Il countryId fornito non esiste](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-15/mdva-33393-magento-patch-provided-countryid-does-not-exist.html)

## [!UICONTROL Merchant Location]

L’impostazione Posizione esercente viene utilizzata per configurare [metodi di pagamento](../stores-purchase/payments.md). Se non è presente alcun valore per questa impostazione, il [Paese predefinito](#uicontrol-country-options) viene utilizzata l&#39;impostazione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **Località esercente** e scegli il tuo **[!UICONTROL Merchant Country]**.

   ![Impostazione della posizione esercente](./assets/payment-methods-merchant-location.png){width="600"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni sulle opzioni di configurazione dei metodi di pagamento, vedi [Guida di riferimento alla configurazione](../configuration-reference/sales/payment-methods.md).

## Valuta

Impostazione valuta: definisce la base [valuta](../stores-purchase/currency-configuration.md) e qualsiasi altra valuta accettata come pagamento. Stabilisce inoltre la connessione e la pianificazione di importazione utilizzate per aggiornare automaticamente i tassi di valuta.

Simboli di valuta: definisce la [simboli di valuta](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) che compaiono nei prezzi dei prodotti e nei documenti di vendita quali ordini e fatture. [!DNL Commerce] supporta le valute di oltre 200 paesi in tutto il mondo.

Aggiornamento dei tassi di divisa - I tassi di divisa possono essere [aggiornato](../stores-purchase/currency-update.md) manualmente o importato nel tuo store secondo necessità, o secondo una pianificazione predefinita.

Selettore valuta: se sono disponibili più valute, la [selettore valuta](../stores-purchase/currency.md) è disponibile nell’intestazione del negozio.

## [!UICONTROL Store Email Addresses]

Puoi avere fino a cinque indirizzi e-mail diversi per rappresentare funzioni o reparti distinti per ogni negozio o visualizzazione. Oltre alle seguenti identità e-mail predefinite, puoi impostare alcune identità personalizzate in base alle tue esigenze.

- Contatto generale
- Rappresentante commerciale
- Assistenza clienti

Ogni identità e il relativo indirizzo e-mail associato possono essere associati a specifici messaggi e-mail automatizzati e vengono visualizzati come mittente dei messaggi e-mail inviati dal tuo archivio.

### Passaggio 1: configurare gli indirizzi e-mail per il dominio

Prima di poter configurare gli indirizzi e-mail per lo store, ciascuno di essi deve essere configurato come indirizzo e-mail valido per il dominio. Per creare ogni indirizzo e-mail necessario, segui le istruzioni dell’amministratore del server o del provider di hosting e-mail.

### Passaggio 2: configurare gli indirizzi e-mail per il negozio

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sotto **[!UICONTROL General]** nel pannello di navigazione a sinistra, scegli **[!UICONTROL Store Email Addresses]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General Contact]** ed effettuare le seguenti operazioni:

   ![Configurazione generale - Archivia indirizzi e-mail](./assets/store-email-addresses-general-contact.png){width="600"}

   - Per **[!UICONTROL Sender Name]**, immettere il nome della persona associata all&#39;identità del contatto generale da visualizzare come mittente di qualsiasi messaggio di posta elettronica.

   - Per **[!UICONTROL Sender Email]**, immetti l’indirizzo e-mail associato.

1. Ripeti questa procedura per ogni indirizzo e-mail del negozio che intendi utilizzare.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Passaggio 3: aggiornare la configurazione dell’e-mail di vendita

Se utilizzi indirizzi e-mail personalizzati, assicurati di aggiornare la configurazione di eventuali messaggi e-mail correlati, in modo che l’identità corretta venga visualizzata come mittente.

1. Nel pannello di navigazione a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales Emails]**.

   La pagina include una sezione separata per ciascuno dei seguenti elementi:

   - Commenti ordine e ordine
   - Commenti su fatture e fatture
   - Commenti spedizione
   - Commenti per nota di credito e nota di credito
   - RMA, autorizzazione RMA, commenti dell&#39;amministratore RMA e commenti dei clienti RMA ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

1. A partire da **[!UICONTROL Order]**, espandi la sezione per ogni messaggio e assicurati che sia selezionato il mittente corretto.

   ![Configurazione vendite - e-mail di vendita](./assets/sales-emails-order.png){width="600"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni sulle opzioni di configurazione delle e-mail di vendita, vedi [_Guida di riferimento alla configurazione_](../configuration-reference/sales/sales-emails.md).

## Modulo Contattaci

Il _Contattaci_ I collegamenti a piè di pagina rappresentano un modo semplice per i clienti di tenersi in contatto con voi. I clienti possono completare il modulo per inviare un messaggio al tuo negozio. Uno standard [!DNL Commerce] installazione visualizza il valore predefinito _Contattaci_ modulo. Dopo aver inviato il modulo, viene visualizzato un messaggio di ringraziamento

È importante comprendere che il modulo Contattaci predefinito viene renderizzato direttamente dal codice anziché da una pagina CMS.

![Pagina Contattaci predefinita](./assets/page-contact-us-default.png){width="700"}

Il piè di pagina del Negozio include un collegamento alla pagina Contattaci disponibile in tutto il negozio.

![Collegamento Contattaci nel piè di pagina](./assets/storefront-footer-contact-us.png){width="700"}

I dati di esempio di Luma includono informazioni aggiuntive sulla pagina Contattaci che mostrano come personalizzare la pagina per il tuo store.

![Pagina Contattaci](./assets/storefront-contact-us.png){width="700"}

### Configurare il modulo per i contatti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL General]**, scegli **[!UICONTROL Contacts]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Contact Us]** sezione e set **[!UICONTROL Enable Contact Us]** a `Yes`.

   ![Configurazione generale - contattaci](./assets/contacts-contact-us.png){width="600"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Email Options]** e impostare le opzioni di contatto e-mail:

   ![Configurazione generale - Opzioni e-mail](./assets/contacts-email-options.png){width="600"}

   - Per **[!UICONTROL Send Emails to]**, immetti l&#39;indirizzo e-mail a cui vengono inviati i messaggi del modulo Contattaci.

   - Imposta **[!UICONTROL Email Sender]** all&#39;identità dello store che appare come mittente del messaggio dal modulo Contattaci. Ad esempio: E-mail personalizzata 2.

   - Imposta **[!UICONTROL Email Template]** al modello utilizzato per i messaggi inviati dal modulo Contattaci.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Personalizzare il contenuto

Puoi personalizzare il contenuto in _Contattaci_ per soddisfare le esigenze del punto vendita e le esigenze del servizio clienti.

### Metodo 1: utilizzo dei dati di esempio

I dati di esempio Luma includono _Contattaci Info_ blocco che può essere personalizzato per il tuo negozio. Il `contact-us-info` [blocco](../content-design/blocks.md) può essere facilmente modificato per aggiungere il tuo contenuto alla pagina Contattaci.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Trova il **[!UICONTROL Contact Us Info]** nell’elenco e apri in **[!UICONTROL Edit]** modalità.

   ![Blocco Info per contattarci](./assets/content-block-contact-us-info.png){width="700"}

1. Nella parte inferiore della pagina del blocco, fai clic su **[!UICONTROL Edit with Page Builder]**.

   ![Blocco di contenuto - Contattaci esempio](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >Se è stato [[!DNL Page Builder] disabilitato](../page-builder/setup.md#disable-dnl-page-builder), puoi utilizzare l’editor [barra strumenti](../content-design/editor.md) per formattare il testo e aggiungere [immagini](../content-design/editor-insert-image.md) e [collegamenti](../content-design/editor-insert-link.md).

1. Passa il puntatore del mouse sul contenitore HTML per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](../page-builder/assets/pb-icon-settings.png) ).

1. Modifica il codice HTML in base alle informazioni di contatto del tuo Negozio e fai clic su **[!UICONTROL Save]**.

   ![Blocco di contenuto - Modifica codice HTML](./assets/content-block-contact-us-html.png){width="700"}

1. Esci da [!DNL Page Builder] posiziona nell’area di visualizzazione e fai clic su **[!UICONTROL Save Block]**.

### Metodo 2: senza dati campione

>[!IMPORTANT]
>
>A partire dalla versione 2.4.0, il modulo di contatto non può più chiamare all’interno di un blocco CMS o di una pagina CMS. Tutte le personalizzazioni del modulo del contatto devono essere eseguite utilizzando modelli XML layout o modelli di tema personalizzati.

Per impostazione predefinita, gli acquirenti accedono al modulo di contatto utilizzando _Collegamento di contatto_ nel piè di pagina delle pagine della vetrina. Per ulteriori informazioni sulla personalizzazione della pagina di contatto, consultare [Guida per gli sviluppatori di front-end][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
