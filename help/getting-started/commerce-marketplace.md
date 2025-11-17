---
title: '[!DNL Adobe Commerce Marketplace]'
description: Scopri di più su  [!DNL Commerce Marketplace], che offre ai commercianti una selezione curata di soluzioni e fornisce agli sviluppatori qualificati gli strumenti, la piattaforma e la posizione principale per creare un business prospero.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 17ec998812d21ab5815546e0f015965c2d35c853
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] è l&#39;archivio delle applicazioni che offre ai commercianti una selezione di soluzioni curata e fornisce agli sviluppatori qualificati gli strumenti, la piattaforma e la posizione principale per creare un&#39;azienda prospera. [!DNL Commerce Marketplace] offre una selezione di estensioni disponibili gratuitamente e altre che sono in vendita. Gli acquisti possono essere pagati con carta di credito o [PayPal][2].

Tutte le estensioni disponibili in [!DNL Commerce Marketplace] hanno superato una revisione approfondita. Il [Programma per la qualità delle estensioni][3] (EQP) combina competenze, linee guida per lo sviluppo e strumenti di verifica di [!DNL Commerce] per garantire che tutte le estensioni su Commerce Marketplace soddisfino gli standard di codifica e le best practice. Il processo di revisione include sia un controllo automatico che una revisione manuale del controllo qualità. Durante il processo, la struttura e il codice di ciascuna estensione vengono esaminati e testati per rilevare eventuali segni di infezione da virus/malware e qualsiasi indicazione di plagio. La revisione include un esame tecnico approfondito e un controllo di integrità condotto da un tecnico [!DNL Commerce], con particolare attenzione alla documentazione, alla struttura della codifica, alle prestazioni, alla scalabilità, alla sicurezza e alla compatibilità con il core [!DNL Commerce].

Anche se è possibile acquistare estensioni da altre origini, solo le estensioni disponibili in [!DNL Commerce Marketplace] vengono verificate tramite un&#39;approfondita analisi tecnica e di marketing all&#39;interno del programma per la qualità delle estensioni.

## Risorse dell’app

Gli sviluppatori hanno tradizionalmente utilizzato PHP per creare estensioni in-process per aggiungere funzionalità, servizi e integrazioni ad Adobe Commerce. Creando app con estensibilità out-of-process, invece di estensioni, puoi evitare problemi di compatibilità.

Le risorse seguenti forniscono un punto di partenza per consentire ai nuovi utenti di acquisire familiarità con le app:

### Risorse Commerce

- [Configurazione di eventi di I/O per Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configurazione degli eventi per Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configurazione dell&#39;interfaccia utente di amministrazione di SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversione di un&#39;estensione in un&#39;app](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Risorse di App Builder

- [Panoramica di Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configurazione di Mesh API per Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Distribuzione di app App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD per le app App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Guida introduttiva di App Builder/Developer Console
   - [Guida introduttiva ad App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Informazioni su progetti e aree di lavoro](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credenziali

Prima di installare un&#39;estensione acquistata da [!DNL Commerce Marketplace], accedi al tuo account [!DNL Commerce] e verifica di disporre di una chiave di accesso attiva. Puoi accedere al tuo account [!DNL Commerce] dall&#39;intestazione di [[!DNL Marketplace]][1] o [Magento.com][6].

La chiave di accesso è un insieme di chiavi pubbliche e private utilizzate per sincronizzare l&#39;installazione di [!DNL Commerce] con l&#39;account [!DNL Commerce] e verificare le credenziali. Dopo la sincronizzazione dell&#39;account, è necessario immettere la chiave privata ogni volta che si installa un&#39;estensione o un modulo da Commerce Marketplace o si aggiorna l&#39;installazione di [!DNL Commerce].

È possibile creare più chiavi di accesso per scopi diversi e attivarle o disattivarle in base alle esigenze. È tuttavia necessario utilizzare la stessa chiave di accesso utilizzata per installare il software [!DNL Commerce]. Ad esempio, non puoi utilizzare una chiave di accesso Magento Open Source per aggiornare Adobe Commerce, o viceversa. Non è inoltre possibile utilizzare una chiave di accesso appartenente a un altro utente o proveniente da un [account condiviso](commerce-account-share.md).

### Creare una chiave di accesso

1. Accedi al tuo account [!DNL Commerce].

1. Nella pagina _[!UICONTROL My Account]_&#x200B;scegliere la scheda **[!UICONTROL Marketplace]**.

1. Nell&#39;angolo superiore destro accanto al tuo nome, fai clic sulla freccia giù e scegli **[!UICONTROL My Profile]**.

   ![Il tuo profilo [!DNL Marketplace]](./assets/marketplace-profile.png){width="600"}

1. Nella scheda _[!UICONTROL Marketplace]_&#x200B;in&#x200B;_[!UICONTROL My Products]_, fare clic su **[!UICONTROL Access Keys]** e quindi eseguire una delle operazioni seguenti:

   - Controlla se disponi già di un set di chiavi di accesso per gli acquisti Marketplace. È possibile creare più set di chiavi di accesso per scopi diversi.

   ![Chiavi di accesso](./assets/access-keys.png){width="600"}

   - Fare clic su **[!UICONTROL Create a New Access Key]**. Immettere un nome per la nuova coppia di chiavi e fare clic su **[!UICONTROL OK]**. I caratteri validi includono caratteri maiuscoli e minuscoli e trattini invece di spazi.

1. Al termine, fare clic su **[!UICONTROL OK]**.

   La nuova chiave di accesso è abilitata e viene visualizzata nell’elenco.

   Osserva il collegamento _Copia_ dopo ogni chiave pubblica e privata. Nel passaggio successivo, copierai e incollerai questi valori per sincronizzare il tuo archivio con Commerce Marketplace.

## Processo di installazione

>[!IMPORTANT]
>
>A partire da Adobe Commerce e Magento Open Source 2.4.0, l&#39;Installazione guidata Web viene rimossa ed è necessario utilizzare la riga di comando per [installare](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=it) o [aggiornare](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html?lang=it) l&#39;istanza. Questo requisito include anche [moduli](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=it) e [estensioni](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=it).

Il processo di installazione per [!DNL Marketplace] acquisti è diverso per _installazioni on-premise_ di Commerce rispetto alle installazioni in hosting su [Adobe Cloud Architecture][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Supporto

Se hai bisogno di assistenza per l’installazione o l’utilizzo di un’estensione, consulta prima la documentazione che accompagna l’estensione. Se non riesci a trovare la risposta alla domanda, utilizza le informazioni di contatto nell’elenco delle estensioni per contattare direttamente lo sviluppatore. Se gli acquisti sul Marketplace non soddisfano le tue esigenze, puoi [richiedere un rimborso](#refund-requests) entro 25 giorni dalla data di acquisto. Adobe esamina tutte le richieste di rimborso e (se approvato) emette il rimborso appropriato. Per problemi relativi a Commerce Marketplace:

Metodo 1: inviare una richiesta di supporto dal modulo [Adobe Commerce Marketplace - Contattaci](https://commercemarketplace.adobe.com/contact-us/).

Metodo 2: [Supporto e-mail](mailto:commercemarketplacesupport@adobe.com).

### Problemi di cassa

I campi dell’indirizzo nel profilo dell’account devono essere compilati a scopo di verifica nel sistema di acquisto di Marketplace.

1. Aggiungi i campi dell’indirizzo nel tuo profilo account Marketplace.
1. Salva il profilo aggiornato.
1. Continua con il pagamento.

### Problemi di accesso

I problemi di accesso sono in genere correlati a una mancata corrispondenza tra il MAGEID e l’indirizzo e-mail nel database degli account. Per assistenza, contatta il supporto Marketplace.

>[!INFO]
>
>Gli acquisti di app ed estensioni non possono essere [trasferiti](#purchase-transfers) a un nuovo account.

### Domande open source

Il team di supporto per il Marketplace risolve i problemi relativi solo ai siti [commerce.adobe.com/](https://commercemarketplace.adobe.com/) e [commerce.developer.adobe.com/](https://commercedeveloper.adobe.com/). Domande su Magento Open Source possono essere indirizzate al [Forum della community](https://community.magento.com/) o a [un partner](https://business.adobe.com/it/products/magento/partners.html) che possa fornire assistenza con Magento Open Source.

### Richieste di rimborso

Per richiedere un rimborso per un acquisto Marketplace, accedi al tuo account e segui questi passaggi:

1. Fai clic su [!UICONTROL **Il mio profilo**] > [!UICONTROL **Cronologia acquisti**].
1. Individua l&#39;acquisto e fai clic su [!UICONTROL **Richiedi un rimborso**].
1. Compilare il modulo dell&#39;ordine di rimborso.

L’assistenza Marketplace richiederà informazioni dopo la generazione della richiesta di rimborso. L’opzione di rimborso è disponibile per 25 giorni dopo la data di acquisto. Consulta il [Contratto cliente per Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Fatture ordine

Puoi scaricare le fatture ordine dalla [!UICONTROL **Cronologia acquisti**] nel tuo account Marketplace. La fattura non fornisce l&#39;IVA o l&#39;indirizzo del venditore perché al momento non è un requisito del Marketplace.

Per scaricare una fattura d&#39;ordine per un acquisto Marketplace, accedi al tuo account Marketplace e segui questi passaggi:

1. Fai clic su [!UICONTROL **Il mio profilo**] > [!UICONTROL **Cronologia acquisti**].
1. Individua l’acquisto.
1. Fare clic sull&#39;icona della stampante nell&#39;angolo superiore destro dell&#39;ordine.

### Trasferimenti di acquisto

Il team di supporto Marketplace non è in grado di trasferire gli acquisti a un account diverso. Per evitare problemi di installazione e distribuzione, è necessario acquistare tutte le app e le estensioni con l&#39;account Commerce primario. Adobe Commerce ha diritto a un identificatore univoco. Poiché Composer è utilizzato per l&#39;installazione, è possibile utilizzare un solo set di [chiavi di accesso](#create-an-access-key) associate all&#39;account primario. L&#39;unica soluzione disponibile è [richiedere un rimborso](#refund-requests) dall&#39;account di acquisto Marketplace (se consentito dai criteri di rimborso di Adobe Commerce).

Puoi [condividere](commerce-account-share.md) un&#39;istanza di Commerce tramite l&#39;account principale. L&#39;accesso condiviso concede autorizzazioni speciali a un account subordinato da un account principale. Il punto di accesso condiviso viene generato dall&#39;account principale. L’account principale può essere l’account autorizzato di Commerce, l’account principale dell’esercente o un account condiviso all’interno di un’organizzazione.

Queste autorizzazioni speciali concedono lo stesso livello di accesso su Adobe Commerce come principale, ma non viene trasferito ad Adobe Commerce Marketplace o Developer Portal. Ciò significa che l’acquisto di un’estensione da un account subordinato nel Marketplace non può essere condiviso con l’account principale. L&#39;accesso condiviso è una strada unidirezionale (account principale subordinato). Non funziona quando un account subordinato tenta di ricondividere con primario.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/it/products/magento/magento-commerce.html
