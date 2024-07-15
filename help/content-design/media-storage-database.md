---
title: Utilizzare un database multimediale
description: Scopri come utilizzare un database di file multimediali per archiviare i tuoi [!DNL Commerce]  file multimediali.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Utilizzare un database multimediale

>[!IMPORTANT]
>
>Il metodo di archiviazione dei supporti del database è obsoleto a partire da Adobe Commerce e dal Magento Open Source 2.4.3.

Per impostazione predefinita, tutte le immagini, i file CSS compilati e i file JavaScript compilati dell&#39;istanza [!DNL Commerce] sono archiviati nel file system del server Web. È possibile scegliere di memorizzare questi file in un database su un server di database. Uno dei vantaggi di questo approccio è la possibilità di sincronizzazione automatica e inversa tra il file system del server web e il database. È possibile utilizzare il database predefinito per archiviare i supporti o crearne uno. Per poter utilizzare un database appena creato come archivio dei supporti, è necessario aggiungere le relative informazioni e le relative credenziali di accesso al file `env.php`.

## Flusso di lavoro database

1. **Il browser richiede il supporto**: nel browser del cliente viene aperta una pagina dell&#39;archivio e il browser richiede il supporto specificato nel HTML.

1. **Il sistema cerca i file multimediali nel file system**. Il sistema cerca i file multimediali nel file system e, se li trova, li trasmette al browser.

1. **Il sistema individua il supporto nel database**. Se il supporto non viene trovato nel file system, viene inviata una richiesta per il supporto al database specificato nella configurazione.

1. **Il sistema individua i supporti nel database**. Uno script PHP trasferisce i file dal database al file system e li invia al browser del cliente. La richiesta del browser per i file multimediali attiva lo script in modo che venga eseguito come segue:

   - Se il server Web [riscrive](../merchandising-promotions/url-rewrite.md) è abilitato per [!DNL Commerce] e supportato dal server, lo script PHP viene eseguito solo quando il supporto richiesto non è presente nel file system.
   - Se le riscritture del server Web sono disabilitate per [!DNL Commerce] o non sono supportate dal server, lo script PHP viene eseguito comunque, anche se il supporto richiesto è disponibile nel file system.

## Utilizzare un database per l&#39;archiviazione dei supporti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** su `Default Config` per applicare la configurazione a livello globale.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Storage Configuration for Media]** ed effettuare le seguenti operazioni:

   ![Configurazione avanzata - configurazione archiviazione per supporti](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Media Storage]** su `Database`.

   - Impostare **[!UICONTROL Select Media Database]** sul database che si desidera utilizzare.

   - Per trasferire il supporto esistente al database appena selezionato, fare clic su **[!UICONTROL Synchronize]**.

   - Immetti **[!UICONTROL Environment Update Time]** in secondi.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
