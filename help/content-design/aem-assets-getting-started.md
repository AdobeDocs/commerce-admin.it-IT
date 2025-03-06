---
title: Configurare l’integrazione di AEM Assets per Commerce
description: Scopri come impostare e configurare l’ambiente Experience Manager Assets per gestire le risorse Commerce per il tuo store.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 98c40c779e1fe705cf1bd47331537bc7b7235921
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Configurare l’integrazione di AEM Assets per Commerce

La configurazione dell’integrazione Adobe Experience Manager Assets per Commerce richiede l’accesso amministrativo per personalizzare la configurazione dell’applicazione e dell’ambiente.

- Accesso amministrativo al programma Cloud Manager in cui viene eseguito il provisioning degli ambienti AEM Assets as a Cloud Service.

- Accesso amministrativo all’ambiente Adobe Commerce e possibilità di recuperare o generare le chiavi API necessarie per l’autenticazione.

## Requisiti per l’utilizzo dell’integrazione

Per sfruttare questa integrazione, le aziende devono soddisfare i seguenti requisiti:

- Licenze attive per Adobe Commerce, Adobe Experience Manager Assets e [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Compositore: 2.x

- Adobe Experience Manager è dotato di [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/overview)

- L&#39;utente di Adobe Commerce che configura l&#39;integrazione deve avere accesso all&#39;organizzazione [IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) in cui è stato eseguito il provisioning del progetto AEM Assets.

## Vantaggi chiave

- **Nessun costo aggiuntivo**: questa integrazione viene fornita gratuitamente ai commercianti che soddisfano i requisiti di licenza.

- **Soluzione Adobe ufficiale**: sviluppata, mantenuta e completamente supportata da Adobe, per garantire stabilità e allineamento con i futuri miglioramenti della piattaforma.

- **Adobe Managed Support Model**: Adobe gestisce l&#39;assistenza e la risoluzione dei problemi, garantendo la massima tranquillità e una risoluzione semplificata.

## Passaggi successivi

L’abilitazione dell’integrazione di Commerce con Experience Manager Assets è un processo in tre fasi:

1. [Installa il pacchetto AEM Assets](aem-assets-configure-aem.md).

1. [Installa pacchetti Adobe Commerce](aem-assets-configure-aem.md).

1. [Configura la risorsa di integrazione](aem-assets-setup-synchronization.md).
