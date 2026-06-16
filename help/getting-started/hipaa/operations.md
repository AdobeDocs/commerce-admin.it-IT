---
title: Operazioni
description: Linee guida per la migrazione a un’offerta compatibile con HIPAA e per l’utilizzo dell’ambiente di staging secondario per la risoluzione dei problemi.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/w3CGUMXmuXy8006HmWG0K-q3ntjbHFAaC61O6t7S4Ao
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 0%

---

# Operazioni

{{ee-feature}}

Utilizzare queste linee guida per informazioni sulla migrazione all&#39;offerta compatibile con HIPAA per Adobe Commerce e sull&#39;utilizzo dell&#39;ambiente `staging_for_support` per la risoluzione dei problemi.

## Migrazione

I clienti che eseguono la migrazione da un’offerta Commerce non HIPAA a un’offerta compatibile con HIPAA devono attenersi alle seguenti linee guida:

1. **Elimina spazi di dati esistenti**: prima della migrazione, tutti gli spazi di dati esistenti devono essere eliminati per evitare la commistione di dati sensibili e non sensibili nel livello SaaS di Adobe Commerce. Crea un ticket di supporto per eliminare gli spazi dei dati.
1. **Configura nuovo ambiente**: l&#39;installazione di [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) nella nuova istanza di HIPAA Commerce deve essere configurata solo dopo l&#39;eliminazione degli spazi dei dati. Il nuovo ambiente SaaS HIPAA deve essere utilizzato solo dopo l’eliminazione dei vecchi spazi di dati. La configurazione di Commerce Services Connector attiva automaticamente la creazione di nuovi spazi di dati SaaS.
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

- **Servizi Commerce non conformi HIPAA**: i clienti non devono utilizzare i servizi Adobe Commerce, ad esempio Live Search, Product Recommendations, Payment Services, Sales Channels o Commerce Intelligence perché non sono pronti HIPAA. I clienti devono utilizzare solo [servizi compatibili con HIPAA](overview.md).

- **Connessione dati** - Solo l&#39;agente di raccolta back-office nell&#39;estensione [Connessione dati](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview) è pronto per HIPAA. I clienti non devono inviare file PHI a servizi di connessione dati non conformi HIPAA, come eventi storefront e Audience Activation. I clienti devono assicurarsi che la raccolta dati della vetrina sia disabilitata.

- **Catalog Service**—Per progettazione, [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview) non elabora PHI, pertanto non rientra nell&#39;ambito per l&#39;audit e la conformità di conformità HIPAA. I clienti devono assicurarsi di utilizzare questo servizio sulla base della propria valutazione dei casi d’uso e in consultazione con il consulente legale. I clienti non devono inoltre utilizzare Catalog Service tramite il servizio federato per evitare il rischio di passare PHI a servizi non conformi HIPAA.

- **Esportazione dati SaaS**. Il servizio [Esportazione dati SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) deve essere configurato per l&#39;invio di dati solo per i componenti pronti per HIPAA in Adobe Commerce.
