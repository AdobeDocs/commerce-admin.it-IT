---
title: "[!UICONTROL My Purchase Orders]"
description: Scopri gli ordini di acquisto e come utilizzarli dalle aziende per gestire i loro acquisti.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Quando gli ordini di acquisto sono [abilitato per un’azienda](purchase-order-flow.md), qualsiasi ordine di un cliente effettuato con l&#39;accesso a un account utente della società viene automaticamente creato come ordine di acquisto (OA). Gli utenti aziendali con le autorizzazioni necessarie possono creare, modificare ed eliminare gli OA creati, insieme agli OA creati dagli utenti subordinati.

![I miei ordini di acquisto](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Gli ordini di acquisto creano un _istantanea_ di prezzi degli articoli, sconti e prezzi di spedizione al momento della creazione dell&#39;ordine. Se il prezzo di un articolo cambia dopo la creazione dell&#39;ordine di acquisto, viene utilizzato il prezzo originale.

## Gestire gli ordini fornitore

Dalla sezione _Visualizza ordine di acquisto_ pagina, il cliente può gestire l&#39;ordine di acquisto, a seconda [autorizzazioni ruolo](account-company-roles-permissions.md).

- Per visualizzare l&#39;OA, fare clic su **[!UICONTROL View]**.
- Per visualizzare eventuali commenti sull&#39;ordine di acquisto, fare clic sul pulsante **[!UICONTROL Comments]** scheda.
- Per visualizzare una cronologia completa degli ordini, fare clic su **[!UICONTROL History Log]** scheda.

>[!IMPORTANT]
>
>Se un articolo in un ordine di acquisto è esaurito o la quantità disponibile è insufficiente, quando l&#39;ordine di acquisto viene convertito in un ordine effettivo si verifica un errore. Se gli ordini inevasi sono abilitati, l&#39;ordine viene elaborato normalmente.

## Nuovo ordine fornitore da ordine fornitore esistente

Se il cliente dispone di un ordine di acquisto esistente e desidera aggiungere nuovi articoli, può generare un ordine di acquisto duplicato con nuovi prodotti aggiunti al nuovo ordine di acquisto. Il cliente completa i seguenti passaggi:

1. Il giorno _Il mio ordine di acquisto_ , il cliente individua l&#39;ordine di acquisto e fa clic sul pulsante **[!UICONTROL View]** collegamento.

1. Il cliente fa clic **[!UICONTROL Add Items to Shopping Cart]**.

   Viene visualizzata la pagina Carrello acquisti con tutti gli elementi elencati.

1. Apporta qualsiasi aggiunta o modifica.

1. (Facoltativo) Utilizza il **[!UICONTROL Custom Reference Number]** per aggiungere un numero di fattura/OA interno all&#39;ordine.

1. Segue il normale flusso di lavoro di pagamento e fa clic su **[!UICONTROL Place Purchase Order]**.

Se hanno articoli nel carrello quando fanno clic su _[!UICONTROL Add Items to Shopping Cart]_, il sistema visualizza una finestra di dialogo. Questa finestra di dialogo consente di scegliere se unire gli articoli del carrello con i nuovi articoli o sostituire gli articoli nel carrello con gli articoli nell’ordine di acquisto.

L&#39;ordine fornitore originale può essere chiuso se non è più necessario.

## Approvazioni ordini fornitore

Per un cliente designato come approvatore in base alla struttura aziendale o al ruolo aziendale assegnato, il _[!UICONTROL My Purchase Orders]_nella pagina del dashboard viene visualizzato **[!UICONTROL Requires My Approval]**scheda. Il cliente fa clic su questa scheda per esaminare gli OA in attesa di approvazione. Il contatore indica il numero di ordini in attesa di approvazione.

Dopo aver fatto clic su **[!UICONTROL View]** per un ordine di acquisto e la revisione dei dettagli, l&#39;approvatore può fare clic su **[!UICONTROL Approve]** o **[!UICONTROL Reject]**.

### Approvazione/rifiuto in blocco

A partire da Adobe Commerce 2.4.1, gli approvatori possono approvare o rifiutare più ordini di acquisto contemporaneamente.

1. Il giorno _[!UICONTROL My Purchase Order]_, fa clic su **[!UICONTROL Requires My Approval]**scheda.

1. Selezionare la casella di controllo per ogni ordine fornitore da approvare o rifiutare.

1. Clic **[!UICONTROL Approve Selected]** o **[!UICONTROL Reject Selected]**.

Un cliente può selezionare solo gli ordini di acquisto con uno stato che consente un&#39;azione. Gli amministratori della società possono effettuare approvazioni in blocco o rifiuti per qualsiasi ordine di acquisto attivo nella propria società.
