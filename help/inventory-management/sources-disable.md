---
title: Disabilita origini magazzino
description: Scopri come disabilitare le origini e modificare le informazioni, inclusi posizione e punto di contatto.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
TQID: https://experienceleague.adobe.com/l-S7b-E9rREgJ4AX5Zd6nneSDJe-OioeD-vk8YeSAak
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 406
ht-degree: 0%

---

# Disabilita origini

Per garantire che tutti i dati dell&#39;ordine rimangano in [!DNL Commerce], non è possibile eliminare le origini. Origini, ordini e spedizioni sono direttamente collegati tra loro. Puoi disattivare le origini e modificare le informazioni, inclusi la posizione e il punto di contatto.

A seconda dello stato delle posizioni, potrebbe essere utile disattivare un&#39;origine. Un&#39;origine disabilitata mantiene tutte le assegnazioni per scorte e prodotti, ma non è accessibile per scorte e ordini.

Quando un&#39;origine è disabilitata:

- [!DNL Inventory Management] ignora e non elenca l&#39;origine per l&#39;elaborazione della spedizione o dell&#39;ordine.
- Le scorte non accedono alle quantità di magazzino dall&#39;origine per i totali di magazzino aggregati.
- Le spedizioni degli ordini non possono essere assegnate ad ubicazioni disabilitate.

Non è possibile disattivare il Source predefinito. [!DNL Commerce] utilizza questa origine per tutti i prodotti nuovi e importati, per i prodotti bundle e per il supporto di sistemi di terze parti. Puoi abilitare o disabilitare le origini personalizzate in qualsiasi momento.

L&#39;impostazione di un&#39;origine su `disabled` è utile nelle situazioni seguenti:

- Aggiunta di un negozio o di un magazzino: quando si aprono nuovi magazzini o si portano in linea nuovi magazzini e ubicazioni di spedizione, aggiungere una voce di origine per impostare l&#39;inventario dei prodotti utilizzando l&#39;importazione e connettersi alle scorte potenziali.
- Spedizioni stagionali - Le vacanze possono essere un periodo molto impegnativo dell&#39;anno. Puoi limitare la spedizione solo da specifiche sedi di spedizione, come i magazzini, per mantenere le sedi di mattoni e malta ben rifornite e concentrate sugli acquirenti locali. Oppure è possibile aggiungere nuove sedi di spedizione per un periodo di tempo limitato per gestire tassi più elevati di vendite e ordini in entrata.
- Chiusura di un&#39;ubicazione: quando si chiude un&#39;ubicazione per lo spostamento in nuovi impianti o in modo permanente, disattivare l&#39;opzione per interrompere le nuove spedizioni dall&#39;ubicazione.

## Disattiva una o più origini personalizzate

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Selezionare la casella di controllo per ogni origine personalizzata abilitata che si desidera disabilitare.

1. Fare clic sul menu _Azioni_ nell&#39;angolo superiore sinistro e scegliere **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] origini - Menu Azioni](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Nella finestra di dialogo di conferma, fare clic su **[!UICONTROL OK]**.

## Abilitare o disabilitare una singola origine personalizzata

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Individuare un&#39;origine personalizzata e fare clic su **[!UICONTROL Edit]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _Generale_ e modificare **[!UICONTROL Is Enabled]**:

   | Opzione | Descrizione |
   | ----- | ----- |
   | `Yes` | Source è abilitato. La quantità viene aggiunta alla quantità vendibile. Nell&#39;elenco di origine viene indicata la quantità corrente durante la spedizione degli ordini. L’algoritmo di selezione Source ne verifica l’origine per la spedizione. |
   | `No` | Source è disabilitato. Le quantità non vengono aggiunte alle quantità di vendita. L&#39;origine non viene elencata per gli ordini di spedizione. Le opzioni di spedizione ignorano questa origine. |

1. Fare clic su **[!UICONTROL Save and Close]**.
