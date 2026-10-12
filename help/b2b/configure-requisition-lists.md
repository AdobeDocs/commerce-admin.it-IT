---
title: Configura massimo elenco richieste di acquisto
description: Scopri la configurazione dell’elenco richieste di acquisto, che controlla il numero massimo che può essere gestito per ogni account cliente.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
TQID: 'https://experienceleague.adobe.com/we9sPvRg20kEV4EpfemuA7WW-rjv7G6evjr5MwzRGyM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%
---
# Configura massimo elenco richieste di acquisto

Quando la funzione Elenco richieste di acquisto è abilitata, i clienti possono creare più elenchi di articoli acquistati di frequente e utilizzarli per l&#39;inserimento degli ordini. È disponibile sia per gli utenti connessi che per gli ospiti. È possibile abilitare gli elenchi di richieste di acquisto quando si [configurano le funzionalità B2B](enable-basic-features.md).

Un cliente può avere più elenchi che si concentrano su prodotti di fornitori, acquirenti, team, campagne o qualsiasi altra cosa che semplifica i flussi di lavoro comuni. [La funzionalità dell&#39;elenco di richieste](requisition-lists.md) è simile a quella degli elenchi di desideri, con le seguenti differenze:

- L&#39;elenco delle richieste di acquisto non viene cancellato dopo l&#39;invio degli articoli al carrello. Può essere utilizzato più volte.
- L&#39;interfaccia utente per gli elenchi delle richieste di acquisto utilizza una vista compatta per visualizzare molti elementi.

Per impostazione predefinita, i clienti possono gestire fino a 999 elenchi di richieste di acquisto per il proprio conto. Tuttavia, puoi modificare la configurazione e specificare un numero inferiore per ridurre il carico sullo store.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Requisition Lists]**.

   ![Elenchi richieste - Impostazione generale](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Number of Requisition Lists]**, immettere il numero massimo di elenchi di richieste di acquisto che è possibile gestire per ogni conto cliente.

   Il numero minimo è `2` e il massimo è `999`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
