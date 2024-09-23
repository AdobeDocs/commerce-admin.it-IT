---
title: Configurare l’integrazione di AEM Assets
description: Scopri i requisiti e i passaggi per configurare l’integrazione tra Adobe Commerce e AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Configurare l’integrazione di AEM Assets

Abilita le funzionalità avanzate di gestione delle risorse configurando l’ambiente AEM Assets e installando e configurando l’integrazione di AEM Assets per Commerce.

Quando l’integrazione è attiva, gli amministratori possono utilizzare Experience Manager Assets as a Cloud Service come unica fonte di verità per la creazione e la gestione delle risorse e come strumento centrale di gestione delle risorse digitali (DAM) per creare, gestire, organizzare e distribuire le risorse per i progetti Commerce.

## Requisiti

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Compositore: 2.x
- Per Adobe Experience Manager è stato eseguito il provisioning con [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/overview)
- L&#39;utente di Adobe Commerce che configura l&#39;integrazione deve avere accesso all&#39;organizzazione [IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) in cui è stato eseguito il provisioning del progetto AEM Assets.

## Configurare l’integrazione

>[!BEGINSHADEBOX]

**Prerequisiti**

La configurazione dell’integrazione AEM Assets richiede l’accesso amministrativo per personalizzare la configurazione dell’applicazione e dell’ambiente.

- Accesso amministrativo al programma Cloud Manager in cui viene eseguito il provisioning degli ambienti AEM Assets as a Cloud Service.
- Accesso amministrativo all’ambiente Adobe Commerce e possibilità di recuperare o generare le chiavi API necessarie per l’autenticazione.

>[!ENDSHADEBOX]

L’abilitazione dell’integrazione di Commerce con Experience Manager Assets è un processo in tre fasi:

1. [Configura il progetto Experience Manager Assets per gestire le risorse Commerce](aem-assets-configure-aem.md).

1. [Installare l&#39;estensione di integrazione Experience Manager Assets e configurare Adobe Commerce](aem-assets-configure-aem.md).

1. [Abilita sincronizzazione risorse](aem-assets-setup-synchronization.md).
