---
title: Utilizzare un database multimediale
description: Scopri come utilizzare un database multimediale per memorizzare i [!DNL Commerce] file multimediali.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Utilizzare un database multimediale

>[!IMPORTANT]
>
>Il metodo di archiviazione dei supporti del database è obsoleto a partire da Adobe Commerce e dal Magento Open Source 2.4.3.

Per impostazione predefinita, tutte le immagini, i file CSS compilati e i file JavaScript compilati del [!DNL Commerce] sono memorizzate nel file system sul server web. È possibile scegliere di memorizzare questi file in un database su un server di database. Uno dei vantaggi di questo approccio è la possibilità di sincronizzazione automatica e inversa tra il file system del server web e il database. È possibile utilizzare il database predefinito per archiviare i supporti o crearne uno. Per poter utilizzare un database appena creato come archivio multimediale, è necessario aggiungere informazioni su di esso e le relative credenziali di accesso al `env.php` file.

## Flusso di lavoro database

1. **Il browser richiede contenuti multimediali** - Una pagina del negozio si apre nel browser del cliente e il browser richiede il supporto specificato nel HTML.

1. **Il sistema cerca i supporti nel file system** - Il sistema cerca il supporto nel file system e, se lo trova, lo trasmette al browser.

1. **Il sistema individua i supporti nel database** - Se il supporto non viene trovato nel file system, viene inviata una richiesta per il supporto al database specificato nella configurazione.

1. **Il sistema individua i supporti nel database** - Uno script PHP trasferisce i file dal database al file system e li invia al browser del cliente. La richiesta del browser per i file multimediali attiva lo script in modo che venga eseguito come segue:

   - Se il server web [riscrive](../merchandising-promotions/url-rewrite.md) sono abilitati per [!DNL Commerce] e supportato dal server, lo script PHP viene eseguito solo quando il supporto richiesto non è presente nel file system.
   - Se le riscritture del server web sono disabilitate per [!DNL Commerce], o non supportato dal server, lo script PHP viene eseguito comunque, anche se il supporto richiesto è disponibile nel file system.

## Utilizzare un database per l&#39;archiviazione dei supporti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** a `Default Config` per applicare la configurazione a livello globale.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Storage Configuration for Media]** ed effettuare le seguenti operazioni:

   ![Configurazione avanzata: configurazione di archiviazione per i supporti](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Media Storage]** a `Database`.

   - Imposta **[!UICONTROL Select Media Database]** al database che si desidera utilizzare.

   - Per trasferire il supporto esistente nel database appena selezionato, fare clic su **[!UICONTROL Synchronize]**.

   - Inserisci il **[!UICONTROL Environment Update Time]** in secondi.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
