---
title: Configurare Experience Manager Assets
description: Aggiungi i metadati della risorsa necessari per consentire all’integrazione di AEM Assets per Commerce di sincronizzare le risorse tra i progetti Adobe Commerce e Experience Manager Assets.
feature: CMS, Media, Integration
source-git-commit: f04648a41fc16154d5f10278f810114d707b670c
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Configurare Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Per gestire le risorse multimediali del tuo negozio tramite l’integrazione AEM Assets per Commerce, il progetto AEM Assets richiede l’aggiunta di alcuni metadati per garantire che tu possa facilmente cercare e gestire le risorse Commerce. Questi metadati facilitano anche la sincronizzazione delle risorse tra Adobe Commerce e Experience Manager Assets. Dopo aver definito i campi di metadati, la mappatura iniziale di questi campi viene eseguita automaticamente la prima volta che una risorsa Commerce viene condivisa con Experience Manager Assets.

Per l’integrazione, puoi configurare due tipi di metadati:

- **[Profilo metadati](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** ti consente di applicare metadati predefiniti alle risorse all&#39;interno di una cartella. Tutte le risorse nella cartella ereditano i metadati predefiniti configurati nel profilo.

- **[Lo schema metadati](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** definisce il layout della pagina delle proprietà e il set di campi che possono essere utilizzati come proprietà dei metadati in una risorsa AEM.

## Configurare i metadati

Per l’onboarding iniziale, aggiungi i seguenti metadati Commerce sia a un profilo di metadati di AEM Assets che a uno schema di metadati.

| Tipo di campo | Etichetta | Proprietà | Valore predefinito |
|------ | ------- | ---------- | ------------- |
| Testo | **Esiste in Adobe Commerce?** | `./jcr:content/metadata/commerce:isCommerce` | sì |
| Testo con più valori | **SKU** | `./jcr:content/metadata/commerce:skus` | nessuno |
| Testo con più valori | **Posizioni** | `./jcr:content/metadata/commerce:positions` | nessuno |
| Testo con più valori | **Ruoli** | `./jcr:content/metadata/commerce:roles` | nessuno |


### Aggiungere campi Commerce a un profilo di metadati

1. Dall’area di lavoro di Adobe Experience Manager, vai all’area di lavoro di amministrazione del contenuto di Author per AEM Assets facendo clic sull’icona Adobe Experience Manager.

   ![Authoring di AEM Assets](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Apri gli strumenti di amministrazione selezionando l’icona a forma di martello.

   ![L&#39;amministratore dell&#39;autore AEM gestisce i profili di metadati](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Aprire la pagina di configurazione del profilo facendo clic su **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** un profilo di metadati per l&#39;integrazione Commerce.

   ![Amministrazione autori AEM aggiungono profili metadati ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Aggiungi una scheda per i metadati di Commerce.

   1. A sinistra, fare clic su **[!UICONTROL Settings]**.

   1. Fare clic su **[!UICONTROL +]** nella sezione scheda e quindi specificare **[!UICONTROL Tab Name]**, `Commerce`.

1. Aggiungi i [campi metadati](#configure-metadata) al modulo.

   ![L&#39;amministratore dell&#39;autore AEM aggiunge campi di metadati al profilo](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Salva l’aggiornamento.

1. Applica il profilo di metadati `Commerce integration` alla cartella in cui sono memorizzate le risorse Commerce.

   1. Dalla pagina [!UICONTROL  Metadata Profiles], seleziona il profilo di integrazione di Commerce.

   1. Dal menu Azioni, selezionare **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Seleziona la cartella contenente le risorse Commerce.

      Crea una cartella Commerce se non esiste.

   1. Fare clic su **[!UICONTROL Apply]**.

### Aggiungere campi Commerce a un modulo schema metadati

1. Dal pannello di amministrazione dei contenuti di AEM Author per Assets, apri **[!UICONTROL Metadata Schemas]** ([!UICONTROL Manage metadata schema forms]).

   ![Schema metadati aggiornamento amministratore autore AEM](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create]** uno schema metadati per Commerce.

   ![Schema metadati aggiornamento amministratore autore AEM](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. In [!UICONTROL Metadata Schema Form], creare i campi `Does Commerce exist?` e `Commerce mappings` e mappare le proprietà.

1. Fare clic su **[!UICONTROL Save]**.


## Publish una risorsa

Dopo aver configurato i metadati AEM e il profilo dello schema per le risorse Commerce, crea la prima risorsa Commerce per mappare i campi dei metadati Commerce.

1. Da Experience Manager, vai a [!UICONTROL Assets > Files] e seleziona la cartella **Commerce**.

1. Caricare un&#39;immagine per un progetto Commerce trascinando il file nella cartella o facendo clic su **[!UICONTROL Add Assets]**.

1. Verificare la configurazione dei metadati: **isCommerce** è impostato su `true` e che la proprietà `commerce:skus` sia impostata sullo SKU per il prodotto Commerce associato all&#39;immagine.

1. Approva la risorsa.


## Aggiungere una risorsa alla cartella Commerce

Crea almeno una risorsa nella cartella AEM Assets Commerce a cui sono assegnati gli attributi di metadati Commerce.

Questa risorsa è necessaria per impostare la sincronizzazione tra l’istanza di Commerce e AEM Assets.

## Mappare i metadati per le risorse

I metadati vengono mappati quando una risorsa Commerce viene pubblicata per la prima volta.  da Commerce per la prima volta. Le risorse multimediali i cui campi incorporati o personalizzati vengono mappati automaticamente sui campi specificati la prima volta che una risorsa viene inviata a Experience Manager Assets.

Prima di iniziare il mapping delle risorse, completa le seguenti attività:

- [Installare e configurare l’integrazione di AEM Assets per Commerce](aem-assets-configure-commerce.md)
- [Configurare i servizi di sincronizzazione per trasferire le risorse tra l’ambiente del progetto Adobe Commerce e l’ambiente del progetto AEM Assets](aem-assets-setup-synchronization.md)
