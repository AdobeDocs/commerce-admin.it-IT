---
title: Assegnare un gruppo di clienti a una società
description: Scopri come assegnare un gruppo di clienti a un account aziendale nel tuo store di Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
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
source-wordcount: 236
ht-degree: 0%

---

# Assegnare un gruppo di clienti a una società

L’assegnazione di un gruppo di clienti a un’azienda equivale essenzialmente all’assegnazione di un catalogo condiviso. Se il Catalogo condiviso non è abilitato [nella configurazione](enable-basic-features.md), a una società viene assegnato un gruppo di clienti anziché un Catalogo condiviso.

- È possibile assegnare un solo gruppo di clienti o un catalogo condiviso alla volta a una società. Impossibile eliminare un gruppo di clienti associato a un catalogo condiviso.
- La modifica del gruppo di clienti assegnato alla società aggiorna i profili di tutti i membri della società.
- Se l&#39;assegnazione del gruppo di clienti viene cambiata da un catalogo condiviso a un gruppo di clienti normale, i membri della società perdono l&#39;accesso al catalogo condiviso e il catalogo principale diventa disponibile dalla vetrina.
- Dopo aver modificato il gruppo della società, un utente della società deve disconnettersi e accedere allo Storefront per visualizzare i nuovi prezzi nel catalogo.

## Modificare il gruppo di clienti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Trovare la società nella griglia e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

   ![Modifica società](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Nella pagina dell&#39;azienda, scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advanced Settings]**.

1. Imposta il **[!UICONTROL Customer Group]** appropriato.

   L&#39;elenco [!UICONTROL Customer Group] include tutti i cataloghi condivisi esistenti, anche se Cataloghi condivisi è disabilitato nella configurazione.

   ![Cambia gruppo clienti o catalogo condiviso](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL Proceed]**.

1. Fare clic su **[!UICONTROL Save]**.
