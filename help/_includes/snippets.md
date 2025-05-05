---
title: Frammenti
description: Note ed elementi visivi riutilizzati per annotare l'applicazione di una funzione o di una pagina a un'edizione specifica
source-git-commit: e82b979ee2c5f51caba6a2aa416c5f20dbce110a
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Frammenti

## Caratteristica solo EE {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Funzione Adobe Systems Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Funzionalità esclusiva solo in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=it#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

## B2B unica funzione {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Funzione B2B di Adobe Systems Commerce" src="../assets/b2b.svg" width="20" height="20" /> Funzionalità esclusiva disponibile solo con <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=it">Adobe Systems Commerce B2B</a></td></tr>
</table>

## Funzionalità solo CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Funzione Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> È necessario un metodo alternativo per Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=it#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

## Nota di autenticazione dell’amministratore IMS {#ims-admin-note}

>[!NOTE]
>
>I commercianti di Adobe Commerce che dispongono di un Adobe ID e desiderano un accesso semplificato ai prodotti aziendali Adobe Commerce e Adobe possono integrare l’autenticazione dell’amministratore Commerce con il flusso di lavoro di autenticazione IMS di Adobe. Una volta abilitata l’integrazione per il tuo archivio Commerce, per accedere ogni utente amministratore deve utilizzare le credenziali Adobe, non le credenziali dell’account Commerce. Consulta [Panoramica sull&#39;integrazione di Adobe Commerce con Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Nota API GTag {#gtag-api-note}

>[!NOTE]
>
>A partire dalla versione 2.4.5, l’integrazione dei servizi Google viene aggiornata per supportare l’utilizzo delle API GTag. GTag è un meccanismo unificato per l’integrazione con le funzionalità di Google per le pagine web e supporta le funzionalità e le opportunità più recenti per il tracciamento e la gestione dei contenuti tramite Google Services. Per ulteriori informazioni, consulta la [documentazione per gli sviluppatori di Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Nota di salto automatico riscrittura URL {#url-rewrite-skip}

>[!NOTE]
>
>Quando i reindirizzamenti automatici sono abilitati e si salva una categoria, tutte le riscritture di prodotti e categorie vengono generate in tempo reale e memorizzate in tabelle di riscrittura per impostazione predefinita. Questo processo potrebbe causare notevoli problemi di prestazioni per le categorie a cui sono assegnati molti prodotti. La soluzione è cambiare questa impostazione predefinita e saltare la generazione di categoria/prodotti URL la riscrittura dei prodotti per il salvataggio della categoria. In questo caso, le riscritture dei prodotti vengono generate solo per il prodotto canonico URL. Per ulteriori informazioni, consulta [Reindirizzamenti automatici dei](/help/merchandising-promotions/url-redirect-product-automatic.md) prodotti.

## URL nota sui parametri di riscrittura {#url-rewrite-params}

>[!IMPORTANT]
>
>Durante il processo di reindirizzamento, tutti i parametri GET specificati nel URL vengono rimossi per motivi di sicurezza.

## Nuovo prezzo regola {#new-price-rule}

>[!NOTE]
>
>Le regole di prezzo vengono elaborate automaticamente con altre regole di sistema. La frequenza di elaborazione dipende dalla configurazione[&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=it) cron. Quando crei un regola di prezzi, concedi abbastanza tempo per farlo entrare nel sistema. Se sei sicuro che sia nel sistema, prova il regola.

## Impostazioni di configurazione {#config}

Per accesso le impostazioni di configurazione store, scegli **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;dalla_ barra laterale Amministratore _.

## Elementi obsoleti dell'API UPS {#ups-api}

>[!IMPORTANT]
>
>A partire da giugno 2024, i commercianti di Adobe Commerce non potranno più negoziare con l’integrazione corrente del gruppo di continuità. Questo perché le API del servizio United Parcel Service (UPS) utilizzate dall’integrazione nativa di Adobe Commerce non supportano attualmente il modello di sicurezza OAuth 2.0 richiesto. Per abilitare l&#39;integrazione, [crea un&#39;applicazione sulla piattaforma di sviluppo UPS](https://developer.ups.com/get-started) per ottenere le credenziali richieste per OAuth 2.0. Utilizzare le nuove credenziali come `username` e `password` nella configurazione di Commerce UPS Shipping. Per ulteriori informazioni sulla modifica del modello di protezione, vedere [Guida alla migrazione della chiave di accesso al portale per sviluppatori_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>I commercianti devono [applicare un aggiornamento della patch di qualità](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=it) al proprio archivio per migrare dall&#39;API SOAP all&#39;API RESTful, che supporta i protocolli di autenticazione OAuth 2.0.


## Documentazione disponibile {#docs-links}

| Risorsa documentazione | Descrizione |
|----------------------- | ----------- |
| [Guide utente amministrative di Adobe Systems Commerce 2.4](../landing/home.md) | Documentazione e risorse per gli esercenti che lavorano nell&#39;area di amministrazione. |
| [Servizi per Adobe Systems Commerce Documentazione](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=it) | Documentazione supportare una raccolta di servizi merchandising che aiutino i commercianti a integrare componenti chiave della loro attività con i loro store. |
| [Guida di Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=it) | Procedure dettagliate per la distribuzione di Adobe Systems Commerce su una piattaforma di hosting cloud gestita e automatizzata. |
| [Guide operative di Adobe Systems Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=it) | Documentazione di sistema su concetti, processi, strumenti e best practice per sviluppare, distribuire e gestire progetti Adobe Systems Commerce on Cloud e locali. |
| [Documentazione per sviluppatori di Adobe Systems Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentazione incentrata sugli sviluppatori utilizzata per personalizzare Adobe Systems Commerce e integrare con sistemi di terze parti. |

{style="table-layout:auto"}

## Compatibilità B2B {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B versione 1.4.2+ è compatibile con PHP 8.2. Se aggiorni l’istanza di Commerce alla versione 2.4.7+, assicurati che l’istanza utilizzi la versione PHP 8.2 per mantenere la compatibilità con la versione B2B di Adobe Commerce. Inoltre, la versione 1.4.2+ di B2B non supporta [GraphQL Application Server](https://experienceleague.adobe.com/it/docs/commerce-operations/performance-best-practices/concepts/application-server).
