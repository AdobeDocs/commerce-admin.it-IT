---
title: Configurare l’integrazione di AEM Assets per Commerce
description: Scopri come integrare Experience Manager Assets con la tua istanza  [!DNL Commerce]  per accedere a innumerevoli risorse multimediali da utilizzare nel tuo store.
feature: CMS, Media, Configuration
source-git-commit: c109edc9d9277baafd61da1df0f1917f07089353
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Configurare l’integrazione di AEM Assets per Commerce

La configurazione dell’integrazione AEM Assets richiede l’accesso amministrativo per personalizzare la configurazione dell’applicazione e dell’ambiente.

- Accesso amministrativo al programma Cloud Manager in cui viene eseguito il provisioning degli ambienti AEM Assets as a Cloud Service.

- Accesso amministrativo all’ambiente Adobe Commerce e possibilità di recuperare o generare le chiavi API necessarie per l’autenticazione.

## Requisiti per l’utilizzo dell’integrazione

Per sfruttare questa integrazione, le aziende devono soddisfare i seguenti requisiti:

- Licenze attive per Adobe Commerce, AEM Assets e [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Compositore: 2.x

- Adobe Experience Manager è dotato di [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/overview)

- L&#39;utente di Adobe Commerce che configura l&#39;integrazione deve avere accesso all&#39;organizzazione [IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) in cui è stato eseguito il provisioning del progetto AEM Assets.

## Vantaggi chiave

- **Nessun costo aggiuntivo**: questa integrazione viene fornita gratuitamente ai commercianti che soddisfano i requisiti di licenza.

- **Soluzione Adobe ufficiale**: sviluppata, mantenuta e completamente supportata da Adobe, per garantire stabilità e allineamento con i futuri miglioramenti della piattaforma.

- **Adobe Managed Support Model**: l&#39;assistenza e la risoluzione dei problemi vengono gestite direttamente da Adobe, garantendo la massima tranquillità e la risoluzione semplificata dei problemi.

## Passaggi successivi

L’abilitazione dell’integrazione di Commerce con Experience Manager Assets è un processo in tre fasi:

1. [Configura il progetto AEM Assets per gestire le risorse Adobe Commerce](aem-assets-configure-aem.md).

1. [Installa l&#39;estensione per l&#39;integrazione delle risorse di AEM e configura Adobe Commerce](aem-assets-configure-aem.md).

1. [Abilita sincronizzazione risorse](aem-assets-setup-synchronization.md).
