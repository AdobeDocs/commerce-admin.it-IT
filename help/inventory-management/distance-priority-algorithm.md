---
title: Configurare l'algoritmo di priorità della distanza
description: Impostare la configurazione per confrontare l'ubicazione dell'indirizzo di destinazione di spedizione con le ubicazioni di origine per determinare l'origine più vicina per evadere le spedizioni.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---

# Configurare l&#39;algoritmo di priorità della distanza

L&#39;algoritmo Distance Priority confronta l&#39;ubicazione dell&#39;indirizzo di destinazione della spedizione con le ubicazioni di origine per determinare l&#39;origine più vicina per evadere le spedizioni. La distanza può essere determinata in base alla distanza fisica o al tempo trascorso in viaggio da un luogo all&#39;altro, utilizzando dati di banca dati o indicazioni stradali, pedonali o ciclabili. Utilizza questo [algoritmo di selezione Source](selection-reservations.md) per consigliare l&#39;origine più vicina agli indirizzi di destinazione per la spedizione.

>[!NOTE]
>
>Se utilizzi l&#39;algoritmo di priorità distanza, è consigliabile immettere l&#39;indirizzo stradale completo e le coordinate GPS per le [sorgenti](sources-add.md).

Sono disponibili due opzioni per calcolare la distanza e il tempo necessari per trovare l&#39;origine più vicina per l&#39;evasione della spedizione:

- **Google MAP** - Utilizza i servizi [Google Maps Platform][1] per calcolare la distanza e l&#39;ora tra l&#39;indirizzo di destinazione di spedizione e le posizioni di origine. Questa opzione utilizza la latitudine e la longitudine (coordinate GPS) della sorgente e può utilizzare l’indirizzo stradale a seconda della modalità di calcolo. È necessaria una chiave API di Google con [API di geocodifica][2] e [API della matrice di distanza][3] abilitate. È possibile che vengano addebitati costi tramite Google.

- **Calcolo offline** - Calcola la distanza utilizzando i dati del codice geografico scaricati e importati utilizzando i codici postali e le coordinate GPS per determinare l&#39;origine più vicina all&#39;indirizzo di destinazione della spedizione. Per configurare questa opzione, potrebbe essere necessario richiedere l&#39;assistenza dello sviluppatore per scaricare e importare inizialmente i geocodici utilizzando le istruzioni della riga di comando.

>[!NOTE]
>
>Per i siti Web multisstore con più paesi, configura la [destinazione imposta predefinita](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} per ogni paese.

## Utilizzare le mappe di Google

Per iniziare, non è necessario un account Google. Il processo include la creazione di un account Google e di un progetto, se necessario. Questa opzione richiede l’aggiunta di un account di fatturazione e di un metodo di pagamento al tuo account Google per completare le configurazioni e utilizzare l’algoritmo.
Tuttavia, l’algoritmo basato sulla distanza di Google MAP è consigliato in quanto più avanzato e preciso rispetto al calcolo offline.

### Passaggio 1: creare la chiave API di Google

La chiave proviene dalla [piattaforma Google Maps][1] e deve avere [API Geocoding][2] e [API Distance Matrix][3] abilitate. Per ulteriori informazioni, vedere [Configurazione dell&#39;algoritmo di priorità della distanza](distance-priority-algorithm.md).

1. Visita [Google Maps Platform][1] e fai clic su **[!UICONTROL Get Started]**.

1. Per abilitare la piattaforma, selezionare **[!UICONTROL Maps, Routes, and Places]** e fare clic su **[!UICONTROL Continue]**.

   ![Piattaforma Google Maps per la tua chiave](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Accedi con un account Google o crea un account.

1. Configura un progetto:

   - Seleziona un progetto o immetti un nuovo nome per il progetto.

   - Per accettare i termini, selezionare `Yes`.

   - Fare clic su **[!UICONTROL Next]**.

1. Inserire un conto di fatturazione o crearne uno. Puoi saltare e aggiungere un account di fatturazione in un secondo momento.

   Per utilizzare questo servizio è necessario un account di fatturazione.

1. Per aprire e configurare le opzioni della piattaforma Google Cloud, fare clic su **[!UICONTROL Console]**.

   - Apri il progetto.

   - Espandere il menu e fare clic su **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Servizi API Google](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - Cerca [API geocodifica][2] e [API matrice distanza][3]. Seleziona e abilita ciascun servizio.

1. Espandere il menu, fare clic su **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]** e copiare la chiave API Google.

   ![Copia chiave API Google](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### Passaggio 2: configurare il provider Google MAP

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Inventory]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sezione _[!UICONTROL Distance Provider for Distance Based SSA]_&#x200B;e impostare **[!UICONTROL Provider]**&#x200B;su `Google MAP`.

   ![Provider per SSA basato sulla distanza](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Google Distance Provider]_&#x200B;e configurare le impostazioni:

   - Per **[!UICONTROL Google API Key]**, immetti la chiave copiata dal tuo account Google.

   - Per **[!UICONTROL Computation mode]**, selezionare una configurazione.

     >[!NOTE]
     >
     >Quando si utilizza questo algoritmo per la spedizione, se percorsi e dati non vengono restituiti per la modalità di calcolo selezionata (guida, bicicletta o deambulazione) per una spedizione, SSA utilizza per impostazione predefinita la priorità Source. Si consiglia di impostare la priorità [ per le origini per stock](stocks-prioritize-sources.md).

     | Opzione | Descrizione |
     | ----- | ----- |
     | `Driving` | (Impostazione predefinita) Richiede indicazioni stradali standard utilizzando la rete stradale. |
     | `Walking` | Richiede indicazioni stradali utilizzando percorsi pedonali e marciapiedi (se disponibili). |
     | `Bicycling` | Richiede indicazioni per il ciclismo utilizzando piste ciclabili e strade preferite (se disponibili). Il servizio [Distance Matrix Service][4] è disponibile solo negli Stati Uniti e in alcune città canadesi. |

   - Per **[!UICONTROL Value]**, selezionare un tipo di valore:

     | Opzione | Descrizione |
     | ----- | ----- |
     | `Distance` | (Impostazione predefinita) Restituisce la distanza tra punti nelle metriche (chilometri e metri) o imperiali (miglia e piedi). |
     | `Time to Destination` | Restituisce il tempo necessario per spostarsi dalle posizioni di origine all&#39;indirizzo di spedizione in ore e minuti. |

   ![Provider distanza Google](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Usa calcolo offline

I calcoli offline utilizzano i codici paese per determinare la distanza tra la destinazione di spedizione e gli indirizzi di origine. Per configurare questa opzione potrebbe essere necessaria l’assistenza per gli sviluppatori. Utilizza un comando CLI [!DNL Inventory Management] per scaricare e importare dati da [geonames.org][5].

>[!NOTE]
>
>I geocodici importati da [geonames.org][5] presentano limitazioni per alcuni paesi, ad esempio Canada e Irlanda. Per ulteriori informazioni, consultare [File del codice postale GeoNames][6].

### Passaggio 1: scaricare e importare i geocodici

Completa la configurazione della riga di comando per scaricare e importare i paesi di geocodici da spedire e avere posizioni di origine in. Questo passaggio potrebbe richiedere l&#39;assistenza degli sviluppatori per le attività della riga di comando. Consulta [Importa geocodici](cli.md#import-geocodes).

Completa questi comandi ogni volta che desideri aggiungere altri geocodici.

### Passaggio 2: impostare il calcolo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Inventory]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Distance Provider for Distance Based SSA]_.

1. Deselezionare la casella di controllo **[!UICONTROL Use system value]** e impostare **[!UICONTROL Provider]** su `Offline Calculation`.

   ![Provider di distanze per SSA basato sulla distanza](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
