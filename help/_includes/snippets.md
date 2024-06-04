---
title: Snippet
description: Riutilizzo di note ed elementi visivi per annotare una funzione o una pagina applicata a una specifica edizione
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Snippet

## Funzionalità solo EE {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Funzione di Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Funzione esclusiva solo in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

## Funzionalità solo B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Funzione B2B di Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Funzione esclusiva disponibile solo con <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a></td></tr>
</table>

## Funzionalità solo CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Funzione Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Per il Magento Open Source è necessario un metodo alternativo (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

## Nota di autenticazione dell’amministratore IMS {#ims-admin-note}

>[!NOTE]
>
>I commercianti di Adobe Commerce che dispongono di un Adobe ID e desiderano un accesso semplificato ai prodotti Adobe Commerce e Adobe Business possono integrare l’autenticazione amministratore di Commerce con il flusso di lavoro di autenticazione IMS di Adobe. Dopo l’abilitazione di questa integrazione per l’archivio Commerce, per accedere ogni utente amministratore deve utilizzare le proprie credenziali di Adobe, non le credenziali dell’account Commerce. Consulta [Panoramica sull’integrazione di Adobe Commerce con Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Nota API GTag {#gtag-api-note}

>[!NOTE]
>
>A partire dalla versione 2.4.5, l’integrazione dei servizi Google viene aggiornata per supportare l’utilizzo delle API GTag. GTag è un meccanismo unificato per l’integrazione con le funzionalità di Google per le pagine web e supporta le funzionalità e le opportunità più recenti per il tracciamento e la gestione dei contenuti tramite Google Services. Per ulteriori informazioni, vedere [Documentazione per gli sviluppatori Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Nota di salto automatico riscrittura URL {#url-rewrite-skip}

>[!NOTE]
>
>Quando i reindirizzamenti automatici sono attivati e si salva una categoria, tutte le riscritture di prodotti e categorie vengono generate in tempo reale e memorizzate nelle tabelle di riscrittura per impostazione predefinita. Questo processo potrebbe causare problemi di prestazioni significativi per le categorie con molti prodotti assegnati. La soluzione consiste nel modificare questa impostazione predefinita e saltare la generazione di riscritture URL categoria/prodotti dei prodotti per il salvataggio categoria. In questo caso, le riscritture del prodotto vengono generate solo per l’URL canonico del prodotto. Consulta [Reindirizzamenti automatici dei prodotti](/help/merchandising-promotions/url-redirect-product-automatic.md) per ulteriori informazioni.

## Nota sui parametri di riscrittura URL {#url-rewrite-params}

>[!IMPORTANT]
>
>Durante il reindirizzamento, tutti i parametri di GET specificati nell’URL vengono rimossi per motivi di sicurezza.

## Nuova regola di prezzo {#new-price-rule}

>[!NOTE]
>
>Le regole di prezzo vengono elaborate automaticamente con altre regole di sistema. La frequenza di elaborazione dipende dalla [configurazione cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Quando crei una regola del prezzo, lascia il tempo necessario per l&#39;accesso al sistema. Quando sei sicuro che sia nel sistema, verifica la regola.

## Impostazioni di configurazione {#config}

Per accedere alle impostazioni di configurazione dell&#39;archivio, scegliere **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**dal_ Amministratore _barra laterale.

## API UPS obsoleta {#ups-api}

>[!IMPORTANT]
>
>A partire da giugno 2024, i commercianti di Adobe Commerce non potranno più negoziare con l’integrazione corrente del gruppo di continuità. Questo perché le API del servizio United Parcel Service (UPS) utilizzate dall’integrazione nativa di Adobe Commerce non supportano attualmente il modello di sicurezza OAuth 2.0 richiesto. Per ulteriori informazioni su questa modifica, consulta [_Guida alla migrazione della chiave di accesso al portale per sviluppatori_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Gli esercenti devono [applicare un aggiornamento della patch di qualità](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) al loro archivio per migrare dall’API SOAP all’API RESTful, che supporta i protocolli di autenticazione OAuth 2.0.


## Documentazione disponibile {#docs-links}

| Risorsa documentazione | Descrizione |
|----------------------- | ----------- |
| [Documentazione di Adobe Commerce 2.4 per esercenti](../landing/home.md) | Documentazione di Adobe Commerce incentrata sugli esercenti |
| [Documentazione dei servizi per Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentazione per supportare una raccolta di servizi che consentono ai commercianti di integrare i componenti chiave della propria attività con il negozio. |
| [Guida di Commerce sull’infrastruttura cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Procedure dettagliate per la distribuzione di Adobe Commerce su una piattaforma cloud con hosting gestito e automatizzato. |
| [Guide operative di Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentazione di sistema su concetti, processi, strumenti e best practice per sviluppare, distribuire e gestire progetti Adobe Commerce. |
| [Documentazione per gli sviluppatori di Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentazione incentrata sugli sviluppatori utilizzata per personalizzare Adobe Commerce e integrarlo con sistemi di terze parti |

{style="table-layout:auto"}
