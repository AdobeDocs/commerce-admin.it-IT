---
title: Visualizzazioni dello store
description: Scopri come aggiungere e modificare una visualizzazione store.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 2%

---

# Visualizzazioni dello store

Le visualizzazioni del Negozio vengono in genere utilizzate per rendere il negozio disponibile in diverse lingue. Gli acquirenti possono utilizzare il selettore della lingua nell’intestazione del negozio per modificare la visualizzazione del negozio.

![Ambito - Più visualizzazioni dello store](./assets/scope-multiview.svg){width="550"}

## Aggiungi una visualizzazione store

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Tutti i Negozi](./assets/stores-all.png){width="700" zoomable="yes"}

1. Clic **[!UICONTROL Create Store View]**.

   ![Crea visualizzazione punto vendita](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Store]** all&#39;archivio padre della visualizzazione.

1. Immetti un **[!UICONTROL Name]** per questa visualizzazione store.

   Il nome viene visualizzato nel selettore della lingua nell’intestazione dello store. Ad esempio: `Spanish`.

1. Per **[!UICONTROL Code]**, immetti il codice che identifica la visualizzazione (in caratteri minuscoli).

   Ad esempio: `spanish`.

1. Per attivare la vista, impostare **[!UICONTROL Status]** a `Enabled`.

1. (Facoltativo) Inserisci un **[!UICONTROL Sort Order]** numero per determinare la sequenza in cui questa vista è elencata con altre viste.

1. Clic **[!UICONTROL Save Store View]**.

## Modificare una visualizzazione dello store

Poiché il nome della vista viene visualizzato nel selettore lingua, potrebbe essere utile modificare il nome della vista predefinita in modo più descrittivo. Il _Nome_ è semplicemente un’etichetta e può essere facilmente modificato.

Se nell&#39;installazione di Adobe Commerce o di Magento Open Source è presente una configurazione multisito o multi-store, non modificare il campo Codice store senza verificare che nel file non sia presente alcun riferimento al valore `index.php` file. Se non hai accesso al server per esaminare il file, chiedi aiuto a uno sviluppatore.

| Campo | Valore originale | Valore aggiornato |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. In _[!UICONTROL Store View]_nella griglia, fare clic sul nome della visualizzazione che si desidera modificare.

   Quando si modifica la vista predefinita, la _[!UICONTROL Store]_e_[!UICONTROL Status]_ campi non disponibili.

   ![Visualizzazione store - Modifica visualizzazione predefinita](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Aggiorna i campi seguenti in base alle esigenze:

   - **[!UICONTROL Store]** (solo visualizzazioni non predefinite)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (solo se non utilizzato in `index.php`)
   - **[!UICONTROL Status]** (solo visualizzazioni non predefinite)
   - **[!UICONTROL Sort Order]**

1. Clic **[!UICONTROL Save Store View]**.
