---
title: Visualizzazioni dello store
description: Scopri come aggiungere e modificare una visualizzazione store.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
TQID: https://experienceleague.adobe.com/2VMBTnzG3lqsNEyx-e46rqDs1wHofaDeHL3j3SuqxOE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# Visualizzazioni dello store

Le visualizzazioni del Negozio vengono in genere utilizzate per rendere il negozio disponibile in diverse lingue. Gli acquirenti possono utilizzare il selettore della lingua nell’intestazione del negozio per modificare la visualizzazione del negozio.

![Ambito - più visualizzazioni dello store](./assets/scope-multiview.svg){width="550"}

## Aggiungi una visualizzazione store

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Tutti gli store](./assets/stores-all.png){width="700" zoomable="yes"}

1. Fare clic su **[!UICONTROL Create Store View]**.

   ![Crea visualizzazione archivio](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Store]** sull&#39;archivio padre della visualizzazione.

1. Immettere **[!UICONTROL Name]** per la visualizzazione archivio.

   Il nome viene visualizzato nel selettore della lingua nell’intestazione dello store. Esempio: `Spanish`.

1. Per **[!UICONTROL Code]**, immettere il codice che identifica la visualizzazione (in caratteri minuscoli).

   Esempio: `spanish`.

1. Per attivare la visualizzazione, impostare **[!UICONTROL Status]** su `Enabled`.

1. (Facoltativo) Immettere un numero **[!UICONTROL Sort Order]** per determinare la sequenza in cui la visualizzazione è elencata con altre visualizzazioni.

1. Fare clic su **[!UICONTROL Save Store View]**.

## Modificare una visualizzazione dello store

Poiché il nome della vista viene visualizzato nel selettore lingua, potrebbe essere utile modificare il nome della vista predefinita in modo più descrittivo. Il campo _Name_ è semplicemente un&#39;etichetta e può essere facilmente modificato.

Se nell&#39;installazione di Adobe Commerce o Magento Open Source è presente una configurazione multisito o multisito, non modificare il campo Codice archivio senza verificare che nel file `index.php` non sia presente alcun riferimento al valore. Se non hai accesso al server per esaminare il file, chiedi aiuto a uno sviluppatore.

| Campo | Valore originale | Valore aggiornato |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Nella colonna _[!UICONTROL Store View]_della griglia fare clic sul nome della visualizzazione che si desidera modificare.

   Durante la modifica della visualizzazione predefinita, i campi _[!UICONTROL Store]_e_[!UICONTROL Status]_ non sono disponibili.

   ![Visualizzazione archivio - modifica visualizzazione predefinita](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Aggiorna i campi seguenti in base alle esigenze:

   - **[!UICONTROL Store]** (solo visualizzazioni non predefinite)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (solo se non utilizzato in `index.php`)
   - **[!UICONTROL Status]** (solo visualizzazioni non predefinite)
   - **[!UICONTROL Sort Order]**

1. Fare clic su **[!UICONTROL Save Store View]**.
