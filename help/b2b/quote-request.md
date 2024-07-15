---
title: Richiesta di offerta
description: Scopri in che modo i clienti associati a un account aziendale possono inviare una richiesta di preventivo.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: b53d77364f09e587813c50221ebd85ac633f1296
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Richiesta di offerta

Se i preventivi sono abilitati nella [configurazione delle funzionalità di vendita](configure-quotes.md), un acquirente autorizzato di una società può avviare il processo di negoziazione del prezzo richiedendo un preventivo dal carrello. Se un buyer non è pronto a sottomettere un preventivo per la negoziazione, può salvarlo come bozza.

>[!NOTE]
>
>Una richiesta di preventivo non può includere codici sconto o gift card.

## Esperienza di richiesta di preventivo del cliente

1. Il cliente accede al proprio account utente come acquirente con [autorizzazione](account-company-roles-permissions.md) per richiedere un preventivo.

1. Aggiunge al carrello i prodotti da includere nell&#39;offerta.

   >[!TIP]
   > 
   >I clienti possono aggiungere più rapidamente un elenco di SKU di prodotto al carrello utilizzando [Ordine rapido](quick-order.md).

1. Seleziona **[!UICONTROL Request a Quote]**.

   ![Richiesta di un preventivo dal carrello](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. Nella casella **[!UICONTROL Add your comment]**, il cliente immette una breve nota per descrivere la richiesta.

1. Immette un **[!UICONTROL Quote Name]**.

   ![Inserimento di commenti e nome](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Se necessario, allega un documento o un&#39;immagine di supporto all&#39;offerta:

   - Seleziona **[!UICONTROL Attach file]**.
   - Seleziona il file dal proprio sistema.

   Per impostazione predefinita, un [file allegato](configure-quotes.md) può avere una dimensione massima di 2 MB, in uno qualsiasi dei seguenti formati di file: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG o JPEG, PNG.

1. Crea ed elabora il preventivo:

   - Invia il preventivo al venditore selezionando **[!UICONTROL Request a Quote]**.
   - Funzionalità [!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti al programma Beta"}**[!UICONTROL Save as Draft]**.

     Se l&#39;acquirente salva il preventivo come bozza, il preventivo sarà disponibile in [!UICONTROL My Quotes] nello stato `Draft`. Le proposte di preventivo non sono visibili al venditore finché l&#39;acquirente non le invia per la revisione.
