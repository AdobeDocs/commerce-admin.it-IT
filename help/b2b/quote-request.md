---
title: Richiesta di offerta
description: Scopri in che modo i clienti associati a un account aziendale possono inviare una richiesta di preventivo.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
TQID: 'https://experienceleague.adobe.com/lRPDBgKHCTklbiZ1QWsvXD--n86T-IySJDu9nv-umsU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 792a7e9b-6519-5e99-a913-56c3dd2408da
    internal-label: Quotes
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '258'
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
   - Salva il preventivo come bozza selezionando **[!UICONTROL Save as Draft]**.

     Se l&#39;acquirente salva il preventivo come bozza, il preventivo sarà disponibile in [!UICONTROL My Quotes] nello stato `Draft`. Le proposte di preventivo non sono visibili al venditore finché l&#39;acquirente non le invia per la revisione.
