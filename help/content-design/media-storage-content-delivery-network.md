---
title: Utilizzare una rete per la distribuzione dei contenuti
description: Scopri come utilizzare una rete CDN (Content Delivery Network) per archiviare i file multimediali.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Utilizzare una rete per la distribuzione dei contenuti

È possibile utilizzare una rete CDN (Content Delivery Network) per archiviare i file multimediali. Adobe Commerce su infrastruttura cloud include la rete CDN Fastly (vedi [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) nella _Guida di Commerce su infrastruttura cloud_). Un&#39;istanza di Commerce installata _on-premise_ non include un&#39;integrazione con alcun CDN specifico. È possibile utilizzare il CDN desiderato.

Dopo aver configurato la rete CDN, devi completare la configurazione dall’amministratore. Le modifiche possono essere apportate a livello globale o a livello di sito web. Quando si utilizza una rete CDN per l’archiviazione dei contenuti multimediali, tutti i percorsi dei contenuti multimediali nelle pagine dello store di Commerce vengono modificati in percorsi CDN specificati nella configurazione.

## Flusso di lavoro CDN

1. **Il browser richiede il supporto**: nel browser del cliente viene aperta una pagina dell&#39;archivio e il browser richiede il supporto specificato in HTML.
1. **Richiesta inviata a CDN; immagini trovate e servite** - La richiesta viene inviata prima al CDN. Se le immagini sono archiviate nella rete CDN, i file multimediali vengono trasmessi al browser del cliente.
1. **File multimediali non trovato, richiesta inviata al server Web [!DNL Commerce]**. Se la rete CDN non contiene i file multimediali, la richiesta viene inviata al server Web [!DNL Commerce]. Se i file multimediali si trovano nel file system, il server Web li invia al browser del cliente.

>[!IMPORTANT]
>
>Per motivi di sicurezza, quando una rete CDN viene utilizzata come archiviazione di contenuti multimediali, JavaScript potrebbe non funzionare correttamente se la rete CDN si trova all’esterno del sottodominio.

## Configurare una rete per la distribuzione dei contenuti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** come necessario.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Base URLs]** ed effettuare le seguenti operazioni:

   ![Configurazione generale - URL di base Web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Aggiorna **[!UICONTROL Base URL for Static View Files]** con l&#39;URL del percorso nella rete CDN in cui sono archiviati i file di visualizzazione statica.

   - Aggiorna **[!UICONTROL Base URL for User Media Files]** con l&#39;URL dei file JavaScript sulla rete CDN.

     Entrambi questi campi possono essere lasciati vuoti o iniziare con il segnaposto: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Base URLs (Secure)]** ed effettuare le seguenti operazioni:

   ![Configurazione generale - URL di base Web (protetto)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Aggiorna **[!UICONTROL Secure Base URL for Static View Files]** con l&#39;URL del percorso nella rete CDN in cui sono archiviati i file di visualizzazione statica.

   - Aggiorna **[!UICONTROL Secure Base URL for User Media Files]** con l&#39;URL dei file JavaScript sulla rete CDN.

     Entrambi questi campi possono essere lasciati vuoti o iniziare con il segnaposto: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
