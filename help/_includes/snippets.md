---
title: Snippet
description: Riutilizzo di note ed elementi visivi per annotare una funzione o una pagina applicata a una specifica edizione
source-git-commit: 0ffeaa42e0207322da1b55a9fd6b6b2cf24ff4ba
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Snippet

## Funzionalità solo EE {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Funzione di Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Funzionalità esclusiva solo in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

## Funzionalità solo B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Funzione B2B di Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Funzionalità esclusiva disponibile solo con <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a></td></tr>
</table>

## Funzionalità solo CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Funzione Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> È necessario un metodo alternativo per Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

## Nota di autenticazione dell’amministratore IMS {#ims-admin-note}

>[!NOTE]
>
>I commercianti di Adobe Commerce che dispongono di un Adobe ID e desiderano un accesso semplificato ai prodotti aziendali Adobe Commerce e Adobe possono integrare l’autenticazione dell’amministratore Commerce con il flusso di lavoro di autenticazione IMS di Adobe. Una volta abilitata l’integrazione per il tuo archivio Commerce, per accedere ogni utente amministratore deve utilizzare le credenziali Adobe, non le credenziali dell’account Commerce. Consulta [Panoramica sull&#39;integrazione di Adobe Commerce con Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Nota API GTag {#gtag-api-note}

>[!NOTE]
>
>A partire dalla versione 2.4.5, l’integrazione dei servizi Google viene aggiornata per supportare l’utilizzo delle API GTag. GTag è un meccanismo unificato per l’integrazione con le funzionalità di Google per le pagine web e supporta le funzionalità e le opportunità più recenti per il tracciamento e la gestione dei contenuti tramite Google Services.

## Nota di salto automatico riscrittura URL {#url-rewrite-skip}

>[!NOTE]
>
>Quando i reindirizzamenti automatici sono attivati e si salva una categoria, tutte le riscritture di prodotti e categorie vengono generate in tempo reale e memorizzate nelle tabelle di riscrittura per impostazione predefinita. Questo processo potrebbe causare problemi di prestazioni significativi per le categorie con molti prodotti assegnati. La soluzione consiste nel modificare questa impostazione predefinita e saltare la generazione di riscritture URL categoria/prodotti dei prodotti per il salvataggio categoria. In questo caso, le riscritture del prodotto vengono generate solo per l’URL canonico del prodotto. Per ulteriori informazioni, vedere [Reindirizzamenti automatici dei prodotti](/help/merchandising-promotions/url-redirect-product-automatic.md).

## Nota sui parametri di riscrittura URL {#url-rewrite-params}

>[!IMPORTANT]
>
>Durante il processo di reindirizzamento, tutti i parametri GET specificati nell’URL vengono rimossi per motivi di sicurezza.

## Nuova regola di prezzo {#new-price-rule}

>[!NOTE]
>
>Le regole di prezzo vengono elaborate automaticamente con altre regole di sistema. La frequenza di elaborazione dipende dalla configurazione [cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Quando crei una regola del prezzo, lascia il tempo necessario per l&#39;accesso al sistema. Quando sei sicuro che sia nel sistema, verifica la regola.

## Impostazioni di configurazione {#config}

Per accedere alle impostazioni di configurazione dell&#39;archivio, scegliere **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**dalla barra laterale_ Amministratore _.

## API UPS obsoleta {#ups-api}

>[!IMPORTANT]
>
>A partire da giugno 2024, i commercianti di Adobe Commerce non potranno più negoziare con l’integrazione corrente del gruppo di continuità. Questo perché le API del servizio United Parcel Service (UPS) utilizzate dall’integrazione nativa di Adobe Commerce non supportano attualmente il modello di sicurezza OAuth 2.0 richiesto. Per abilitare l&#39;integrazione, [crea un&#39;applicazione sulla piattaforma di sviluppo UPS](https://developer.ups.com/get-started) per ottenere le credenziali richieste per OAuth 2.0. Utilizzare le nuove credenziali come `username` e `password` nella configurazione di Commerce UPS Shipping. Per ulteriori informazioni sulla modifica del modello di protezione, vedere [Guida alla migrazione della chiave di accesso al portale per sviluppatori_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>I commercianti devono [applicare un aggiornamento della patch di qualità](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) al proprio archivio per migrare dall&#39;API SOAP all&#39;API RESTful, che supporta i protocolli di autenticazione OAuth 2.0.


## Documentazione disponibile {#docs-links}

| Risorsa documentazione | Descrizione |
|----------------------- | ----------- |
| [Guide utente amministratore di Adobe Commerce 2.4](../landing/home.md) | Documentazione e risorse per gli esercenti che lavorano nell’Amministratore. |
| [Servizi per la documentazione di Adobe Commerce](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | Documentazione a supporto di una raccolta di servizi di merchandising che consentono ai commercianti di integrare componenti chiave della propria attività con il negozio. |
| [Guida di Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Procedure dettagliate per la distribuzione di Adobe Commerce su una piattaforma cloud con hosting gestito e automatizzato. |
| [Guide operative di Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentazione dei sistemi su concetti, processi, strumenti e best practice per sviluppare, distribuire e gestire progetti Adobe Commerce on-premise e sul cloud. |
| [Documentazione per gli sviluppatori di Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentazione incentrata sugli sviluppatori utilizzata per personalizzare Adobe Commerce e integrarlo con sistemi di terze parti. |

{style="table-layout:auto"}

## Compatibilità B2B {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B versione 1.4.2+ è compatibile con PHP 8.2. Se aggiorni l’istanza di Commerce alla versione 2.4.7+, assicurati che l’istanza utilizzi la versione PHP 8.2 per mantenere la compatibilità con la versione B2B di Adobe Commerce. Inoltre, la versione 1.4.2+ di B2B non supporta [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).
