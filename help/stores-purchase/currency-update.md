---
title: Aggiorna tassi di cambio
description: Scopri come impostare i tassi di valuta manualmente o importarli nel tuo store.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
TQID: https://experienceleague.adobe.com/tEt15Mzt7MeDtf6MZfu9n6EsvJKUCNBdGhUo0-RK3zk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Aggiorna tassi di cambio

I tassi di cambio possono essere impostati manualmente o importati nello store. Per fare in modo che il tuo negozio abbia i tassi più attuali, puoi configurare i tassi di valuta per essere aggiornati automaticamente secondo programma.

Prima di importare i tassi di valuta, completare l&#39;[impostazione dei tassi di valuta](currency-configuration.md) per specificare le valute accettate e stabilire la connessione e la pianificazione dell&#39;importazione.

![Tassi di cambio](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Aggiornare manualmente un tasso di valuta

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Fare clic sul tasso che si desidera modificare e immettere il nuovo valore per ogni valuta supportata.

1. Al termine, fare clic su **[!UICONTROL Save Currency Rates]**.

## Importa tassi di valuta

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Impostare **[!UICONTROL Import Service]** sul provider del tasso di valuta.

   Il provider predefinito è `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >A partire dalla versione 2.4.6, il servizio [[!DNL Fixer.io]](https://fixer.io/) è obsoleto e sostituito con il servizio [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Si consiglia di utilizzare un account APILayer invece di un account [!DNL Fixer.io] obsoleto.

1. Fare clic su **[!UICONTROL Import]**.

   I tassi aggiornati vengono visualizzati nell&#39;elenco _[!UICONTROL Currency Rates]_. Se i tassi sono cambiati dopo l’ultimo aggiornamento, il vecchio tasso viene visualizzato di seguito come riferimento.

1. Al termine, fare clic su **[!UICONTROL Save Currency Rates]**.

1. Quando viene richiesto di aggiornare la cache, fare clic sul collegamento **[!UICONTROL Cache Management]** e aggiornare la cache non valida.

   ![Messaggio di sistema - aggiorna la cache non valida](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Importa tassi di valuta secondo programma

1. Verifica che [Cron](../systems/cron.md) sia abilitato per il tuo archivio.

1. Per specificare le valute accettate e stabilire la connessione e la pianificazione per l&#39;importazione, completare l&#39;[Impostazione tasso valuta](currency-configuration.md).

1. Per verificare che le tariffe siano state importate nei tempi previsti, controllare l&#39;elenco _[!UICONTROL Currency Rates]_.

1. Attendere il periodo di tempo dell&#39;impostazione della frequenza stabilita per la pianificazione e controllare nuovamente le tariffe.
