---
title: Abilita sincronizzazione risorse
description: Scopri come collegare i progetti Adobe Commerce e Experience Manager Assets per abilitare la sincronizzazione delle risorse tra questi due sistemi.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Abilita sincronizzazione risorse

>[!BEGINSHADEBOX]

**Prerequisiti**

- [Configurare AEM Experience Manager Assets per la gestione delle risorse Commerce](#aem-assets-configure-aem)
- [Installa e configura l&#39;integrazione AEM Assets per Commerce](#aem-assets-configure-commerce.md) per aggiungere l&#39;estensione e generare le credenziali e le connessioni necessarie per utilizzare l&#39;estensione.

>[!ENDSHADEBOX]

Durante questo processo di abilitazione, puoi registrare l’ID tenant fornendo il programma e l’ID ambiente per l’ambiente di authoring AEM. Questi ID identificano il progetto AEM Assets a cui ti stai connettendo e forniscono le credenziali per abilitare la comunicazione e i flussi di lavoro tra Commerce e AEM Assets.

Dopo aver identificato il progetto AEM Assets, seleziona la regola di corrispondenza da utilizzare per sincronizzare le risorse tra Adobe Commerce e AEM Assets.

L’integrazione di AEM Assets per Commerce supporta due regole di corrispondenza per la sincronizzazione delle risorse tra Adobe Commerce e AEM Assets.

- **Corrispondenza per SKU prodotto**: questa è la regola di corrispondenza predefinita che corrisponde alle risorse in base allo SKU (Stock Keeping Unit) del prodotto. Lo SKU è un identificatore univoco per ciascun prodotto. Questa regola associa lo SKU nei metadati della risorsa allo SKU del prodotto Commerce per garantire che le risorse siano associate ai prodotti corretti.

- **Corrispondenza personalizzata**: questa regola di corrispondenza è destinata a scenari più complessi o a requisiti aziendali specifici che richiedono una logica di corrispondenza personalizzata. Per utilizzare questa regola, è necessario che in Adobe Developer App Builder sia implementato un codice personalizzato che definisca la corrispondenza tra le risorse e i prodotti. Ulteriori dettagli disponibili a breve...

Per l&#39;onboarding iniziale, utilizza la regola predefinita `Match by product sku`. Se necessario, puoi modificare la regola corrispondente in un secondo momento.

## Abilitare l’integrazione

1. Ottieni l&#39;ID del progetto e dell&#39;ambiente per [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Apri la console AEM Sites e seleziona **[!UICONTROL Assets]**.

   1. Copia e salva gli ID di progetto e ambiente dall&#39;URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Dall’amministratore di Commerce, apri la configurazione dell’integrazione di AEM Assets.

   1. Selezionare **[!UICONTROL Store]** > Configurazione > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]**.

   1. Espandere **[!UICONTROL Experience Manager Assets integration]**.

      ![L&#39;integrazione di AEM Assets abilita l&#39;integrazione](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Identificare il progetto Experience Manager Assets a cui connettersi immettendo **[!UICONTROL Program ID]** e **[!UICONTROL Environment ID]**.

1. Aggiungere le credenziali OAUTH per autenticare le richieste API tra Adobe Commerce e il servizio ARES selezionando **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**, ad esempio `Assets integration`.

1. Consenti a Commerce di accettare gli aggiornamenti in arrivo da AEM Assets impostando **[!UICONTROL Enable integration]** su `Yes`.

   Dopo aver abilitato l’integrazione, puoi configurare la regola di corrispondenza delle risorse.

   ![Regola di corrispondenza risorse selezionate per integrazione AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definisci la regola di corrispondenza per la sincronizzazione delle risorse.

   1. Selezionare **[!UICONTROL Match by product SKU]**.

   1. Aggiungi il nome del campo di metadati [AEM Assets](aem-assets-configure-aem.md#configure-metadata) definito per gli SKU dei prodotti Commerce nel campo **[!UICONTROL Match by product SKU attribute name]**, ad esempio `commerce:skus`.

1. Applicare la configurazione e avviare il processo di sincronizzazione selezionando **[!UICONTROL Save Config]**.
