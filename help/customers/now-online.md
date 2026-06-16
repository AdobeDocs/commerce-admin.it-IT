---
title: Clienti online
description: L'opzione _Now Online_ del menu [!UICONTROL Customers &#x200B;] elenca tutti i clienti e i visitatori attualmente in linea nel tuo negozio.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
TQID: https://experienceleague.adobe.com/jtyDgy3jFmn0XymAYcpc2AOLLWSTDw-3OGkvG9a1SDc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 0%

---

# Clienti online

L&#39;opzione **[!UICONTROL Now Online]** del menu [!DNL Customers] elenca tutti i clienti e i visitatori attualmente online nel tuo store. L&#39;intervallo di tempo per cui i clienti vengono visualizzati come attualmente online è impostato nella configurazione e determina per quanto tempo l&#39;attività [!DNL Customer's] è visibile dall&#39;amministratore. Per impostazione predefinita, l’intervallo è di 15 minuti. La sessione termina se la tastiera non viene utilizzata in questo periodo di tempo e i clienti devono accedere nuovamente al proprio account per continuare a fare acquisti. È importante notare che il contenuto dei carrelli viene salvato per un accesso successivo.

![Clienti online](assets/customers-now-online.png){width="700" zoomable="yes"}

Lo stato online dei clienti viene aggiornato solo al momento dell’accesso del cliente, della registrazione o di qualsiasi altro evento che cambia lo stato. Include eventi correlati al carrello, come l’aggiunta, la rimozione e la modifica di prodotti.

>[!NOTE]
>
>Le sole visite alle pagine non aggiornano lo stato online del cliente. Per raccogliere tali informazioni, si consiglia di [configurare Google Analytics](../merchandising-promotions/google-analytics.md) (da solo o con [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) o utilizzare altro software di analisi con Adobe Commerce.

## Visualizza tutti i clienti attualmente online

Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Per informazioni su come aiutare un cliente online a completare un acquisto, consulta [Assistenza per la spesa](../stores-purchase/introduction.md#shopping-assistance).

## Configurare l’intervallo di tempo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandere la sezione **[!UICONTROL Online Customers Options]** ed eseguire le operazioni seguenti:

   ![Opzioni cliente online](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Per **[!UICONTROL Online Minutes Interval]**, immettere il numero di minuti per cui la sessione del cliente deve essere visibile dall&#39;amministratore. Lascia vuoto il campo per accettare l’intervallo predefinito di 15 minuti.

   - Per **[!UICONTROL Customer Data Lifetime]**, immettere il numero di minuti prima della scadenza dei dati non salvati immessi dal cliente.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Descrizioni delle colonne

| Colonna | Descrizione |
| --- | --- |
| **[!UICONTROL ID]** | L’ID cliente di un cliente registrato. |
| **[!UICONTROL First Name]** | Il nome di un cliente registrato. |
| **[!UICONTROL Last Name]** | Cognome di un cliente registrato. |
| **[!UICONTROL Email]** | L’indirizzo e-mail di un cliente registrato. |
| **[!UICONTROL Last Activity]** | La data e l’ora dell’ultima attività del cliente nel tuo negozio. |
| **[!UICONTROL Type]** | Opzioni: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | L’ultimo URL visitato dal cliente. |
| **[!UICONTROL Company]** | Il nome dell’azienda a cui appartiene l’utente. |

{style="table-layout:auto"}
