---
title: Disabilita origini magazzino
description: Scopri come disabilitare le origini e modificare le informazioni, inclusi posizione e punto di contatto.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Disabilita origini

Per garantire che tutti i dati dell&#39;ordine vengano conservati in [!DNL Commerce], le origini non possono essere eliminate. Origini, ordini e spedizioni sono direttamente collegati tra loro. Puoi disattivare le origini e modificare le informazioni, inclusi la posizione e il punto di contatto.

A seconda dello stato delle posizioni, potrebbe essere utile disattivare un&#39;origine. Un&#39;origine disabilitata mantiene tutte le assegnazioni per scorte e prodotti, ma non è accessibile per scorte e ordini.

Quando un&#39;origine è disabilitata:

- [!DNL Inventory Management] ignora e non elenca l&#39;origine per la spedizione o l&#39;elaborazione dell&#39;ordine.
- Le scorte non accedono alle quantità di magazzino dall&#39;origine per i totali di magazzino aggregati.
- Le spedizioni degli ordini non possono essere assegnate ad ubicazioni disabilitate.

Impossibile disattivare l&#39;origine predefinita. [!DNL Commerce] utilizza questa origine per tutti i prodotti nuovi e importati, per i prodotti bundle e per il supporto di sistemi di terze parti. Puoi abilitare o disabilitare le origini personalizzate in qualsiasi momento.

Impostazione di un&#39;origine su `disabled` è utile nelle seguenti situazioni:

- Aggiunta di un negozio o di un magazzino: quando si aprono nuovi magazzini o si portano in linea nuovi magazzini e ubicazioni di spedizione, aggiungere una voce di origine per impostare l&#39;inventario dei prodotti utilizzando l&#39;importazione e connettersi alle scorte potenziali.
- Spedizioni stagionali - Le vacanze possono essere un periodo molto impegnativo dell&#39;anno. Puoi limitare la spedizione solo da specifiche sedi di spedizione, come i magazzini, per mantenere le sedi di mattoni e malta ben rifornite e concentrate sugli acquirenti locali. Oppure è possibile aggiungere nuove sedi di spedizione per un periodo di tempo limitato per gestire tassi più elevati di vendite e ordini in entrata.
- Chiusura di un&#39;ubicazione: quando si chiude un&#39;ubicazione per lo spostamento in nuovi impianti o in modo permanente, disattivare l&#39;opzione per interrompere le nuove spedizioni dall&#39;ubicazione.

## Disattiva una o più origini personalizzate

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Selezionare la casella di controllo per ogni origine personalizzata abilitata che si desidera disabilitare.

1. Fai clic su _Azioni_ nell&#39;angolo in alto a sinistra e scegliere **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] origini - Menu Azioni](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL OK]**.

## Abilitare o disabilitare una singola origine personalizzata

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Individua un’origine personalizzata e fai clic su **[!UICONTROL Edit]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _Generale_ sezione e modifica **[!UICONTROL Is Enabled]**:

   | Opzione | Descrizione |
   | ----- | ----- |
   | `Yes` | Origine abilitata. La quantità viene aggiunta alla quantità vendibile. Nell&#39;elenco di origine viene indicata la quantità corrente durante la spedizione degli ordini. L’algoritmo di selezione dell’origine ne verifica la spedizione. |
   | `No` | Origine disabilitata. Le quantità non vengono aggiunte alle quantità di vendita. L&#39;origine non viene elencata per gli ordini di spedizione. Le opzioni di spedizione ignorano questa origine. |

1. Clic **[!UICONTROL Save and Close]**.
