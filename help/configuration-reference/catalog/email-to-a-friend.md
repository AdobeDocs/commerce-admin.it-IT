---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Catalog] > [!UICONTROL Email to a Friend] dell'amministratore di Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Modelli e-mail](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Visualizzazione store | Attiva il processo che consente ai clienti di inviare e-mail agli amici sui prodotti presenti nel negozio. Opzioni: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Visualizzazione store | Identifica il modello di e-mail utilizzato per i messaggi generati dalla funzione _Invia un&#39;e-mail a un amico_. Modello predefinito: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Visualizzazione store | Determina se il mittente deve essere un cliente registrato per inviare e-mail su un prodotto agli amici. Opzioni: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Visualizzazione store | Limita il numero di persone che possono essere nella lista di distribuzione per una singola e-mail. |
| [!UICONTROL Max Products Sent in 1  Hour] | Visualizzazione store | Limita il numero di prodotti che possono essere condivisi da un singolo utente in un periodo di un’ora. |
| [!UICONTROL Limit Sending By] | Visualizzazione store | Determina il metodo utilizzato per identificare il mittente. Le opzioni includono: <br/>**`IP Address`**- (scelta consigliata) Identifica il mittente in base all&#39;indirizzo IP del computer utilizzato per inviare le e-mail del prodotto.<br/>**`Cookie (unsafe)`** - Identifica il mittente tramite un cookie del browser. Questo metodo non è sicuro perché l’utente può eliminare il cookie per evitare la restrizione. |

{style="table-layout:auto"}
