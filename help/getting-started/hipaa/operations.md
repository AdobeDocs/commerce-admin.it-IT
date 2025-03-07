---
title: Operazioni
description: Linee guida per la migrazione a un’offerta compatibile con HIPAA e per l’utilizzo dell’ambiente di staging secondario per la risoluzione dei problemi.
source-git-commit: 999d3126ae368000fc2c58c315473739012f3934
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# Operazioni

Utilizzare queste linee guida per informazioni sulla migrazione all&#39;offerta compatibile con HIPAA per Adobe Commerce e sull&#39;utilizzo dell&#39;ambiente `staging_for_support` per la risoluzione dei problemi.

## Migrazione

I clienti che eseguono la migrazione da un’offerta Commerce non HIPAA a un’offerta compatibile con HIPAA devono attenersi alle seguenti linee guida:

1. **Elimina spazi di dati esistenti**: prima della migrazione, tutti gli spazi di dati esistenti devono essere eliminati per evitare la commistione di dati sensibili e non sensibili nel livello SaaS di Adobe Commerce. Crea un ticket di supporto per eliminare gli spazi dei dati.
1. **Configura nuovo ambiente**: l&#39;installazione di [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) nella nuova istanza di HIPAA Commerce deve essere configurata solo dopo l&#39;eliminazione degli spazi dei dati. Il nuovo ambiente SaaS HIPAA deve essere utilizzato solo dopo l’eliminazione dei vecchi spazi di dati. La configurazione di Commerce Services Connector attiva automaticamente la creazione di nuovi spazi di dati SaaS.
1. **Strategia di migrazione**: l&#39;eliminazione degli spazi di dati SaaS è un processo irreversibile ed elimina tutti i dati del catalogo e le configurazioni correlate. Se desideri trasferire i dati o le configurazioni obsoleti, è necessario implementare una strategia di migrazione. Questa strategia è responsabilità del commerciante. Un ticket di supporto per l’eliminazione degli spazi di dati esistenti deve essere creato solo dopo il backup dei dati di migrazione (se applicabile).

>[!NOTE]
>Per eliminare gli spazi di dati esistenti, i clienti devono creare un ticket di supporto Adobe Commerce denominato &quot;Migrazione HIPAA: eliminazione degli spazi di dati SaaS&quot;, fornire `MAGEID` e gli ID progetto SaaS da eliminare.

## Risoluzione dei problemi con il supporto Adobe Commerce

L&#39;offerta compatibile con HIPAA di Adobe Commerce include un ambiente `staging_for_support` aggiuntivo che deve essere utilizzato dal team di supporto Adobe Commerce per la risoluzione dei problemi.

I clienti devono assicurarsi che l&#39;ambiente `staging_for_support`:

- Non contiene dati sensibili, come, ma non limitato a, Informazioni sanitarie protette (PHI).
- Non deve essere utilizzato per alcuna attività di produzione.
- Non deve essere assegnato un nome diverso da `staging_for_support` per evitare confusione.
- È tenuto aggiornato con il codice e la configurazione dell’ambiente di produzione per garantire che la risoluzione dei problemi venga eseguita in un ambiente il più vicino possibile alla produzione.

## Servizi Commerce

- **Servizi Commerce non conformi HIPAA**: i clienti non devono utilizzare i servizi Adobe Commerce, ad esempio Live Search, Product Recommendations, Payment Services, Sales Channel o Commerce Intelligence perché non sono pronti per HIPAA. I clienti devono utilizzare solo [servizi compatibili con HIPAA](overview.md).

- **Connessione dati** - Solo l&#39;agente di raccolta back-office nell&#39;estensione [Connessione dati](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) è pronto per HIPAA. I clienti non devono inviare PHI a servizi di connessione dati non conformi HIPAA, come eventi e Audienci Activation di vetrina. I clienti devono assicurarsi che la raccolta dati della vetrina sia disabilitata.

- **Catalog Service**—Per progettazione, [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview) non elabora PHI, pertanto non rientra nell&#39;ambito per l&#39;audit e la conformità di conformità HIPAA. I clienti devono assicurarsi di utilizzare questo servizio sulla base della propria valutazione dei casi d’uso e in consultazione con il consulente legale. I clienti non devono inoltre utilizzare Catalog Service tramite il servizio federato per evitare il rischio di passare PHI a servizi non conformi HIPAA.

- **Esportazione dati SaaS**. Il servizio [Esportazione dati SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) deve essere configurato per l&#39;invio di dati solo per i componenti pronti per HIPAA in Adobe Commerce.
