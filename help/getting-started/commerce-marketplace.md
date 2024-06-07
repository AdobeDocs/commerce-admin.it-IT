---
title: '[!DNL Adobe Commerce Marketplace]'
description: Scopri di più su [!DNL Commerce Marketplace], che offre ai commercianti una selezione curata di soluzioni e fornisce agli sviluppatori qualificati gli strumenti, la piattaforma e la posizione ideale per creare un business prospero.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 02e7c71fc47e6850371bfbdc1be50f65ec8015e9
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] è l’application store che offre ai commercianti una selezione curata di soluzioni e fornisce agli sviluppatori qualificati gli strumenti, la piattaforma e la posizione ideale per creare un’azienda prospera. [!DNL Commerce Marketplace] offre una selezione di estensioni disponibili gratuitamente e altre che sono in vendita. Gli acquisti possono essere pagati con carta di credito o [PayPal][2].

Tutte le estensioni disponibili su [!DNL Commerce Marketplace] hanno superato un esame approfondito. Il [Programma di qualità dell’estensione][3] (EQP) combina [!DNL Commerce] competenze, linee guida per lo sviluppo e strumenti di verifica per garantire che tutte le estensioni Commerci Marketplace soddisfino gli standard di codifica e le best practice. Il processo di revisione include sia un controllo automatico che una revisione manuale del controllo qualità. Durante il processo, la struttura e il codice di ciascuna estensione vengono esaminati e testati per rilevare eventuali segni di infezione da virus/malware e qualsiasi indicazione di plagio. La revisione comprende un esame tecnico approfondito e un controllo di integrità effettuato da un [!DNL Commerce] con particolare attenzione alla documentazione, alla struttura di codifica, alle prestazioni, alla scalabilità, alla sicurezza e alla compatibilità con [!DNL Commerce] core.

Anche se è possibile acquistare estensioni da altre origini, solo le estensioni disponibili in [!DNL Commerce Marketplace] sono verificati tramite un’ampia revisione tecnica e di marketing all’interno del programma di qualità dell’estensione.

## Risorse dell’app

Gli sviluppatori hanno tradizionalmente utilizzato PHP per creare estensioni in-process per aggiungere funzionalità, servizi e integrazioni ad Adobe Commerce. Creando app con estensibilità out-of-process, invece di estensioni, puoi evitare problemi di compatibilità.

Le risorse seguenti forniscono un punto di partenza per consentire ai nuovi utenti di acquisire familiarità con le app:

### Risorse Commerce

- [Configurazione di eventi di I/O per Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configurazione di eventi per Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configurazione dell’SDK per l’interfaccia di amministrazione](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversione di un’estensione in un’app](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Risorse di App Builder

- [Panoramica di Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configurazione di Mesh API per Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Distribuzione delle app di App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD per le app di App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Guida introduttiva ad App Builder/Developer Console
   - [Guida introduttiva ad App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Informazioni su progetti e aree di lavoro](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credenziali

Prima di installare un’estensione acquistata da [!DNL Commerce Marketplace], accedere al [!DNL Commerce] e verificare di disporre di una chiave di accesso attiva. Puoi accedere al tuo [!DNL Commerce] account dall&#39;intestazione di [[!DNL Marketplace]][1] o [Magento.com][6].

La chiave di accesso è un set di chiavi pubbliche e private utilizzate per sincronizzare [!DNL Commerce] installazione con [!DNL Commerce] e verificare le credenziali. Dopo aver sincronizzato l’account, ogni volta che installi un’estensione o un modulo da Commerci Marketplace o aggiorni la tua chiave privata, devi immettere la tua [!DNL Commerce] installazione.

È possibile creare più chiavi di accesso per scopi diversi e attivarle o disattivarle in base alle esigenze. Tuttavia, è necessario utilizzare la stessa chiave di accesso utilizzata per installare [!DNL Commerce] software. Ad esempio, non puoi utilizzare una chiave di accesso al Magento Open Source per aggiornare Adobe Commerce, o viceversa. Inoltre, non puoi utilizzare una chiave di accesso che appartiene a un altro utente o che proviene da un [account condiviso](commerce-account-share.md).

### Creare una chiave di accesso

1. Accedi al tuo [!DNL Commerce] account.

1. Il giorno _[!UICONTROL My Account]_pagina, scegli la **[!UICONTROL Marketplace]**scheda.

1. Nell’angolo superiore destro accanto al nome, fai clic sulla freccia giù e scegli **[!UICONTROL My Profile]**.

   ![Il tuo [!DNL Marketplace] profilo](./assets/marketplace-profile.png){width="600"}

1. Il giorno _[!UICONTROL Marketplace]_scheda in_[!UICONTROL My Products]_, fai clic su **[!UICONTROL Access Keys]**, quindi eseguire una delle operazioni seguenti:

   - Controlla se disponi già di un set di chiavi di accesso per gli acquisti Marketplace. È possibile creare più set di chiavi di accesso per scopi diversi.

   ![Chiavi di accesso](./assets/access-keys.png){width="600"}

   - Clic **[!UICONTROL Create a New Access Key]**. Immetti un nome per la nuova coppia di chiavi e fai clic su **[!UICONTROL OK]**. I caratteri validi includono caratteri maiuscoli e minuscoli e trattini invece di spazi.

1. Al termine, fai clic su **[!UICONTROL OK]**.

   La nuova chiave di accesso è abilitata e viene visualizzata nell’elenco.

   Osserva _Copia_ dopo ogni chiave pubblica e privata. Nel passaggio successivo, copierai e incollerai questi valori per sincronizzare l’archivio con Commerci Marketplace.

## Processo di installazione

>[!IMPORTANT]
>
>A partire da Adobe Commerce e Magento Open Source 2.4.0, l&#39;Installazione guidata Web viene rimossa ed è necessario utilizzare la riga di comando per [installare](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) o [aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) la tua istanza. Questo requisito comprende anche: [moduli](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) e [estensioni](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Il processo di installazione per [!DNL Marketplace] gli acquisti sono diversi per _on-premise_ installazioni di Commerce rispetto alle installazioni in hosting su [Architettura Adobe Cloud][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Supporto

Se hai bisogno di assistenza per l’installazione o l’utilizzo di un’estensione, consulta prima la documentazione che accompagna l’estensione. Se non riesci a trovare la risposta alla domanda, utilizza le informazioni di contatto nell’elenco delle estensioni per contattare direttamente lo sviluppatore. Se gli acquisti sul Marketplace non soddisfano le tue esigenze, puoi [richiedere un rimborso](#refund-requests) entro 25 giorni dalla data di acquisto. L&#39;Adobe esamina tutte le richieste di rimborso e (se approvato) emette il rimborso appropriato. Per i problemi di supporto relativi alla Commerce Marketplace, vedi [[!DNL Marketplace] Centro risorse][5].

### Problemi di cassa

I campi dell’indirizzo nel profilo dell’account devono essere compilati a scopo di verifica nel sistema di acquisto di Marketplace.

1. Aggiungi i campi dell’indirizzo nel tuo profilo account Marketplace.
1. Salva il profilo aggiornato.
1. Continua con il pagamento.

### Problemi di accesso

I problemi di accesso sono in genere correlati a una mancata corrispondenza tra il MAGEID e l’indirizzo e-mail nel database degli account. Per assistenza, contatta il supporto Marketplace.

>[!INFO]
>
>Gli acquisti di app ed estensioni non possono essere [trasferita](#purchase-transfers) a un nuovo account.

### Domande open source

Il team di supporto Marketplace risolve i problemi relativi al [commerce.adobe.com/](https://commercemarketplace.adobe.com/) e [commerce developer.adobe.com/](https://commercedeveloper.adobe.com/) solo siti. Per eventuali domande sul Magento Open Source, contattare [Forum della community](https://community.magento.com/) o [contatta un partner](https://business.adobe.com/products/magento/partners.html) che possono aiutare con il Magento Open Source.

### Richieste di rimborso

Per richiedere un rimborso per un acquisto Marketplace, accedi al tuo account e segui questi passaggi:

1. Clic [!UICONTROL **Il mio profilo**] > [!UICONTROL **Cronologia acquisti**].
1. Individua l’acquisto e fai clic su [!UICONTROL **Richiedi un rimborso**].
1. Compilare il modulo dell&#39;ordine di rimborso.

L’assistenza Marketplace richiederà informazioni dopo la generazione della richiesta di rimborso. L’opzione di rimborso è disponibile per 25 giorni dopo la data di acquisto. Consulta la [Contratto per i clienti del Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Fatture ordine

È possibile scaricare le fatture degli ordini da [!UICONTROL **Cronologia acquisti**] nel tuo account Marketplace. La fattura non fornisce l&#39;IVA o l&#39;indirizzo del venditore perché al momento non è un requisito del Marketplace.

Per scaricare una fattura d&#39;ordine per un acquisto Marketplace, accedi al tuo account Marketplace e segui questi passaggi:

1. Clic [!UICONTROL **Il mio profilo**] > [!UICONTROL **Cronologia acquisti**].
1. Individua l’acquisto.
1. Fare clic sull&#39;icona della stampante nell&#39;angolo superiore destro dell&#39;ordine.

### Trasferimenti di acquisto

Il team di supporto Marketplace non è in grado di trasferire gli acquisti a un account diverso. Per evitare problemi di installazione e distribuzione, è necessario acquistare tutte le app e le estensioni con l&#39;account Commerce primario. Adobe Commerce ha diritto a un identificatore univoco. Poiché Composer viene utilizzato per l&#39;installazione, è disponibile un solo set di [tasti di scelta](#create-an-access-key) può essere utilizzato associato all’account principale. L&#39;unica soluzione disponibile è [richiedere un rimborso](#refund-requests) dal conto acquisti Marketplace (se consentito dalla politica di rimborso di Adobe Commerce).

È possibile [condividere](commerce-account-share.md) un’istanza di Commerce tramite l’account principale. L&#39;accesso condiviso concede autorizzazioni speciali a un account subordinato da un account principale. Il punto di accesso condiviso viene generato dall&#39;account principale. L’account principale può essere l’account autorizzato di Commerce, l’account principale dell’esercente o un account condiviso all’interno di un’organizzazione.

Queste autorizzazioni speciali concedono lo stesso livello di accesso su Adobe Commerce come principale, ma non viene trasferito ad Adobe Commerce Marketplace o Developer Portal. Ciò significa che l’acquisto di un’estensione da un account subordinato nel Marketplace non può essere condiviso con l’account principale. L&#39;accesso condiviso è una strada unidirezionale (account principale subordinato). Non funziona quando un account subordinato tenta di ricondividere con primario.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
