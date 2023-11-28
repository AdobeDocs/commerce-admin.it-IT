---
title: Utilizzare una rete per la distribuzione dei contenuti
description: Scopri come utilizzare una rete CDN (Content Delivery Network) per archiviare i file multimediali.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Utilizzare una rete per la distribuzione dei contenuti

È possibile utilizzare una rete CDN (Content Delivery Network) per archiviare i file multimediali. Adobe Commerce sull’infrastruttura cloud include la rete CDN Fastly (consulta [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) nel _Guida di Commerce su infrastruttura cloud_). Un’istanza Commerce installata _on premise_ non include un’integrazione con alcuna rete CDN specifica, puoi utilizzare la rete CDN desiderata.

Dopo aver configurato la rete CDN, devi completare la configurazione dall’amministratore. Le modifiche possono essere apportate a livello globale o a livello di sito web. Quando si utilizza una rete CDN per l’archiviazione dei contenuti multimediali, tutti i percorsi ai contenuti multimediali nelle pagine dell’archivio Commerce vengono modificati in base ai percorsi CDN specificati nella configurazione.

## Flusso di lavoro CDN

1. **Il browser richiede contenuti multimediali** - Una pagina del negozio si apre nel browser del cliente e il browser richiede il supporto specificato nel HTML.
1. **Richiesta inviata a CDN; immagini trovate e servite** - La richiesta viene inviata prima al CDN. Se le immagini sono archiviate nella rete CDN, i file multimediali vengono trasmessi al browser del cliente.
1. **File multimediale non trovato, richiesta inviata a [!DNL Commerce] server web** - Se la rete CDN non dispone dei file multimediali, la richiesta viene inviata al [!DNL Commerce] server web. Se i file multimediali si trovano nel file system, il server Web li invia al browser del cliente.

>[!IMPORTANT]
>
>Per motivi di sicurezza, quando una rete CDN viene utilizzata come archiviazione dei contenuti multimediali, JavaScript potrebbe non funzionare correttamente se la rete CDN si trova all’esterno del sottodominio.

## Configurare una rete per la distribuzione dei contenuti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** secondo necessità.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Base URLs]** ed effettuare le seguenti operazioni:

   ![Configurazione generale: URL della base web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Aggiornare il **[!UICONTROL Base URL for Static View Files]** con l’URL della posizione sulla rete CDN in cui sono memorizzati i file di visualizzazione statica.

   - Aggiornare il **[!UICONTROL Base URL for User Media Files]** con l’URL dei file JavaScript sulla rete CDN.

     Entrambi questi campi possono essere lasciati vuoti o iniziare con il segnaposto: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Base URLs (Secure)]** ed effettuare le seguenti operazioni:

   ![Configurazione generale - URL della base web (protetti)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Aggiornare il **[!UICONTROL Secure Base URL for Static View Files]** con l’URL della posizione sulla rete CDN in cui sono memorizzati i file di visualizzazione statica.

   - Aggiornare il **[!UICONTROL Secure Base URL for User Media Files]** con l’URL dei file JavaScript sulla rete CDN.

     Entrambi questi campi possono essere lasciati vuoti o iniziare con il segnaposto: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
