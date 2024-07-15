---
title: Clienti online
description: L'opzione _Now Online_ del menu [!UICONTROL Customers ] elenca tutti i clienti e i visitatori attualmente in linea nel tuo negozio.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Clienti online

L&#39;opzione **[!UICONTROL Now Online]** del menu [!DNL Customers] elenca tutti i clienti e i visitatori attualmente online nel tuo store. L&#39;intervallo di tempo per cui i clienti vengono visualizzati come attualmente online è impostato nella configurazione e determina per quanto tempo l&#39;attività [!DNL Customer's] è visibile dall&#39;amministratore. Per impostazione predefinita, l’intervallo è di 15 minuti. La sessione termina se la tastiera non viene utilizzata in questo periodo di tempo e i clienti devono accedere nuovamente al proprio account per continuare a fare acquisti. È importante notare che il contenuto dei carrelli viene salvato per un accesso successivo.

![Clienti online](assets/customers-now-online.png){width="700" zoomable="yes"}

Lo stato online dei clienti viene aggiornato solo al momento dell’accesso del cliente, della registrazione o di qualsiasi altro evento che cambia lo stato. Include eventi correlati al carrello, come l’aggiunta, la rimozione e la modifica di prodotti.

>[!NOTE]
>
>Le sole visite alle pagine non aggiornano lo stato online del cliente. Per raccogliere tali informazioni, si consiglia di [configurare le Google Analytics](../merchandising-promotions/google-analytics.md) (da sole o con [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) o utilizzare altro software di analisi con Adobe Commerce.

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
