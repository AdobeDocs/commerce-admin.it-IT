---
title: Integrazione di Experience Manager Assets per Commerce
description: Scopri come integrare Experience Manager Assets con la tua istanza  [!DNL Commerce]  per accedere a innumerevoli risorse multimediali da utilizzare nel tuo store.
feature: CMS, Media, Configuration, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Integrazione di Experience Manager Assets per Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

L’integrazione tra Commerce e Adobe Experience Manager (AEM) Assets combina le solide funzionalità di AEM as a Digital Asset Management (DAM) con Adobe Commerce per migliorare le esperienze di eCommerce. Questa integrazione sfrutta le potenti funzioni di gestione delle risorse dell’AEM per fornire un modo semplice, scalabile ed efficiente di gestire e distribuire le risorse tra i vari store commerce.

**Funzioni chiave**

- **Gestione centralizzata delle risorse**

   - **AEM Assets as the Single Source of Truth**-AEM Assets funge da archivio centrale per tutte le risorse digitali, garantendo che tutte le piattaforme di e-commerce abbiano accesso alle risorse approvate del marchio.

   - **Gestione in blocco delle risorse**: le organizzazioni possono gestire in modo efficiente grandi volumi di risorse grazie alle solide funzionalità di gestione delle risorse dell&#39;AEM. In questo modo, gli addetti al marketing e i commercianti possono mappare in modo efficiente set di immagini di grandi dimensioni per le nuove linee di prodotti.

- **Esperienze Commerce personalizzate**-Utilizzando i servizi GenAI nell&#39;AEM, le organizzazioni possono generare milioni di varianti di prodotto per esperienze e-commerce personalizzate. Gli addetti al marketing e i commercianti possono utilizzare queste immagini per creare vetrine dinamiche per il lancio di prodotti e campagne stagionali, aumentando il coinvolgimento e aumentando i tassi di conversione.

- **Corrispondenza risorse automatizzata**-L&#39;integrazione include un servizio del motore di regole che abbina automaticamente le risorse in AEM ai prodotti in Adobe Commerce in base allo SKU o ad altri attributi chiave. Il servizio garantisce che le risorse e le varianti di prodotto più recenti siano sempre disponibili sugli store di e-commerce. Inoltre, riduce lo sforzo manuale necessario per gestire le risorse, liberando tempo per attività più strategiche.

- **Processi semplificati**
   - **Abilita e configura l&#39;integrazione dall&#39;amministratore di Commerce**. Gli amministratori e gli sviluppatori possono installare e configurare l&#39;integrazione da Adobe Commerce utilizzando strumenti e processi familiari.
   - **Aggiornamenti dinamici**-Mantieni aggiornate le immagini del prodotto con le ultime modifiche apportate al sistema di gestione delle risorse. Questi aggiornamenti automatizzati garantiscono che le vetrine commerciali dispongano sempre delle informazioni di prodotto più aggiornate.
   - **Gestione efficiente del catalogo**-Semplifica la manutenzione del catalogo prodotti automatizzando la pulizia e l&#39;aggiornamento delle risorse.

## Integrare Commerce e Experience Manager Assets

>[!BEGINSHADEBOX]

**Prerequisiti**

- Adobe Commerce deve essere configurato con l&#39;integrazione dell&#39;amministratore [Commerce con Adobe ID](/help/getting-started/adobe-ims-config.md) a cui è assegnato un ID organizzazione.
- Experience Manager Assets deve essere assegnato come prodotto allo stesso ID organizzazione.
- L’utente che configura l’integrazione deve disporre di un account nella stessa organizzazione con diritti di amministratore per accedere ad Adobe Commerce e Experience Manager Assets.

>[!ENDSHADEBOX]

Abilitare l’integrazione di Commerce con Experience Manager Assets completando le seguenti attività:

1. [Configurare il progetto Experience Manager Assets per gestire le risorse Commerce](aem-assets-configure-aem.md)

1. [Installare l’estensione Experience Manager Assets Integration e configurare Adobe Commerce](aem-assets-configure-commerce.md)

1. [Abilita sincronizzazione risorse](aem-assets-setup-synchronization.md)
