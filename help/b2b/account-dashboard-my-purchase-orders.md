---
title: '[!UICONTROL My Purchase Orders]'
description: Scopri gli ordini di acquisto e come utilizzarli dalle aziende per gestire i loro acquisti.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Quando gli ordini fornitore sono [abilitati per una società](purchase-order-flow.md), qualsiasi ordine per un cliente connesso a un account utente della società viene creato automaticamente come ordine fornitore (OA). Gli utenti aziendali con le autorizzazioni necessarie possono creare, modificare ed eliminare gli OA creati, insieme agli OA creati dagli utenti subordinati.

![I miei ordini di acquisto](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Gli ordini di acquisto creano una _istantanea_ dei prezzi degli articoli, degli sconti e dei prezzi di spedizione al momento della creazione dell&#39;ordine. Se il prezzo di un articolo cambia dopo la creazione dell&#39;ordine di acquisto, viene utilizzato il prezzo originale.

## Gestire gli ordini fornitore

Dalla pagina _Visualizza ordine di acquisto_, il cliente può gestire l&#39;ordine di acquisto, a seconda delle sue [autorizzazioni di ruolo](account-company-roles-permissions.md).

- Per visualizzare l&#39;OA, fare clic su **[!UICONTROL View]**.
- Per visualizzare eventuali commenti sull&#39;oggetto Criteri di gruppo, fare clic sulla scheda **[!UICONTROL Comments]**.
- Per visualizzare una cronologia completa degli ordini, fare clic sulla scheda **[!UICONTROL History Log]**.

>[!IMPORTANT]
>
>Se un articolo in un ordine di acquisto è esaurito o la quantità disponibile è insufficiente, quando l&#39;ordine di acquisto viene convertito in un ordine effettivo si verifica un errore. Se gli ordini inevasi sono abilitati, l&#39;ordine viene elaborato normalmente.

## Nuovo ordine fornitore da ordine fornitore esistente

Se il cliente dispone di un ordine di acquisto esistente e desidera aggiungere nuovi articoli, può generare un ordine di acquisto duplicato con nuovi prodotti aggiunti al nuovo ordine di acquisto. Il cliente completa i seguenti passaggi:

1. Nella pagina _Il mio ordine di acquisto_, il cliente individua l&#39;ordine di acquisto e fa clic sul collegamento **[!UICONTROL View]**.

1. Il cliente fa clic su **[!UICONTROL Add Items to Shopping Cart]**.

   Viene visualizzata la pagina Carrello acquisti con tutti gli elementi elencati.

1. Apporta qualsiasi aggiunta o modifica.

1. (Facoltativo) Utilizza **[!UICONTROL Custom Reference Number]** per aggiungere un numero di fattura/OA interno all&#39;ordine.

1. Segue il normale flusso di lavoro di estrazione e fa clic su **[!UICONTROL Place Purchase Order]**.

Se nel carrello sono presenti elementi quando si fa clic su _[!UICONTROL Add Items to Shopping Cart]_, viene visualizzata una finestra di dialogo. Questa finestra di dialogo consente di scegliere se unire gli articoli del carrello con i nuovi articoli o sostituire gli articoli nel carrello con gli articoli nell’ordine di acquisto.

L&#39;ordine fornitore originale può essere chiuso se non è più necessario.

## Approvazioni ordini fornitore

Per un cliente designato come approvatore in base alla struttura della società o al ruolo aziendale assegnato, nella pagina del dashboard _[!UICONTROL My Purchase Orders]_&#x200B;viene visualizzata la scheda **[!UICONTROL Requires My Approval]**. Il cliente fa clic su questa scheda per esaminare gli OA in attesa di approvazione. Il contatore indica il numero di ordini in attesa di approvazione.

Dopo aver fatto clic su **[!UICONTROL View]** per un ordine di acquisto e aver esaminato i dettagli, l&#39;approvatore può fare clic su **[!UICONTROL Approve]** o **[!UICONTROL Reject]**.

### Approvazione/rifiuto in blocco

A partire da Adobe Commerce 2.4.1, gli approvatori possono approvare o rifiutare più ordini di acquisto contemporaneamente.

1. Nella pagina _[!UICONTROL My Purchase Order]_, fa clic sulla scheda **[!UICONTROL Requires My Approval]**.

1. Selezionare la casella di controllo per ogni ordine fornitore da approvare o rifiutare.

1. Fai clic su **[!UICONTROL Approve Selected]** o **[!UICONTROL Reject Selected]**.

Un cliente può selezionare solo gli ordini di acquisto con uno stato che consente un&#39;azione. Gli amministratori della società possono effettuare approvazioni in blocco o rifiuti per qualsiasi ordine di acquisto attivo nella propria società.
