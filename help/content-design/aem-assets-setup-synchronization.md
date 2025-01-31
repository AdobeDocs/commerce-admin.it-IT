---
title: Abilita sincronizzazione risorse
description: Scopri come collegare i progetti Adobe Commerce e Experience Manager Assets per abilitare la sincronizzazione delle risorse tra questi due sistemi.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e9b3ede8945de0a6ed0cdb02e5675d736764d3e4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Abilita sincronizzazione risorse

Durante il processo di abilitazione, puoi registrare l’ID tenant per il progetto utilizzando il programma e l’ID ambiente per l’ambiente di authoring AEM. Questi ID identificano il progetto AEM Assets a cui ti stai connettendo e forniscono le credenziali per abilitare la comunicazione tra gli ambienti Commerce e AEM Assets.

Dopo aver identificato il progetto di risorse AEM, seleziona la regola corrispondente per la sincronizzazione delle risorse tra Adobe Commerce e AEM Assets.

- **[!UICONTROL Match by product SKU]**—Regola predefinita che corrisponde allo SKU nei metadati della risorsa con [SKU prodotto Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) per garantire che le risorse siano associate ai prodotti corretti.

- **[!UICONTROL Custom match]** - Regola di corrispondenza per scenari più complessi o requisiti aziendali specifici che richiedono una logica di corrispondenza personalizzata. L’implementazione della corrispondenza personalizzata richiede lo sviluppo di codice personalizzato in Adobe Developer App Builder per definire il modo in cui le risorse vengono associate ai prodotti. Ulteriori dettagli disponibili a breve...

Per l&#39;onboarding iniziale, utilizza la regola predefinita *Corrispondenza per SKU prodotto*.

## Prerequisiti

- [Configurare AEM Experience Manager Assets per la gestione delle risorse Commerce](#aem-assets-configure-aem)

- [Installa e configura l&#39;integrazione AEM Assets per Commerce](#aem-assets-configure-commerce.md) per aggiungere l&#39;estensione e generare le credenziali e le connessioni necessarie per utilizzare l&#39;estensione.

- Crea un ticket di supporto per richiedere l’abilitazione per l’integrazione AEM Assets. È necessario fornire **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** e **[!UICONTROL IMS Org ID]**.

  >[!TIP]
  >
  > (Facoltativo) Fornisci **[!UICONTROL Asset Selector IMS Client ID]** se disponibile.

## Configurare la connessione

1. Ottieni l&#39;ID del progetto e dell&#39;ambiente [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Apri la console AEM Sites e seleziona **[!UICONTROL Assets]**.

   1. Copia e salva gli ID di progetto e ambiente dall&#39;URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Dall’amministratore di Commerce, apri la configurazione dell’integrazione di AEM Assets.

   1. Vai a **[!UICONTROL Store]** > Configurazione > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![L&#39;integrazione di AEM Assets abilita l&#39;integrazione](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Immettere l&#39;ambiente AEM Assets **[!UICONTROL Program ID]** e **[!UICONTROL Environment ID]**.

1. Immettere **[!UICONTROL Asset Selector IMS Client ID]** se disponibile.

   [ID IMS](../getting-started/adobe-ims-config.md) è richiesto da [[!UICONTROL Assets Selector]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/overview-asset-selector), che seleziona le immagini per le categorie e/o [!DNL Page Builder].

1. Selezionare [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) per autenticare le richieste tra Commerce e il servizio di corrispondenza risorse.

1. Consenti a Commerce di accettare gli aggiornamenti in arrivo da AEM Assets impostando **[!UICONTROL Integration enabled]** su `Yes`.

   Dopo aver abilitato l’integrazione, configura la regola di corrispondenza delle risorse.

   ![Regola di corrispondenza risorse selezionate per integrazione AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definisci la regola di corrispondenza per la sincronizzazione delle risorse.

   1. Selezionare **[!UICONTROL Match by product SKU]**.

   1. Aggiungi il nome del campo di metadati [AEM Assets](aem-assets-configure-aem.md#configure-metadata) definito per gli SKU dei prodotti Commerce nel campo **[!UICONTROL Match by product SKU attribute name]**, ad esempio `commerce:skus`.

   ![Regola di corrispondenza risorse selezionate per integrazione AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Seleziona **[!UICONTROL Save Config]** per applicare gli aggiornamenti e avviare la sincronizzazione delle risorse
