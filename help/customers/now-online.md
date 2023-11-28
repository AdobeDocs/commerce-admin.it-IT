---
title: Clienti online
description: Opzione _Now Online_ (Ora online) nella [!UICONTROL Customers ]Il menu elenca tutti i clienti e i visitatori attualmente online nel tuo negozio.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Clienti online

Il **[!UICONTROL Now Online]** opzione sul [!DNL Customers] Il menu elenca tutti i clienti e i visitatori attualmente online nel tuo negozio. L’intervallo di tempo per il quale i clienti vengono visualizzati come attualmente online è impostato nella configurazione e determina per quanto tempo [!DNL Customer's] l&#39;attività è visibile dall&#39;amministratore. Per impostazione predefinita, l’intervallo è di 15 minuti. La sessione termina se la tastiera non viene utilizzata in questo periodo di tempo e i clienti devono accedere nuovamente al proprio account per continuare a fare acquisti. È importante notare che il contenuto dei carrelli viene salvato per un accesso successivo.

![Clienti online](assets/customers-now-online.png){width="700" zoomable="yes"}

Lo stato online dei clienti viene aggiornato solo al momento dell’accesso del cliente, della registrazione o di qualsiasi altro evento che cambia lo stato. Include eventi correlati al carrello, come l’aggiunta, la rimozione e la modifica di prodotti.

>[!NOTE]
>
>Le sole visite alle pagine non aggiornano lo stato online del cliente. Per raccogliere tali informazioni, si raccomanda di: [configurare le Google Analytics](../merchandising-promotions/google-analytics.md) (da solo o con [Gestione tag Google](../merchandising-promotions/google-tag-manager.md)) o utilizzare un altro software di analisi con Adobe Commerce.

## Visualizza tutti i clienti attualmente online

Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Per informazioni su come aiutare un cliente online a completare un acquisto, consulta [Assistenza agli acquisti](../stores-purchase/introduction.md#shopping-assistance).

## Configurare l’intervallo di tempo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandi **[!UICONTROL Online Customers Options]** ed effettuare le seguenti operazioni:

   ![Opzioni cliente online](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Per **[!UICONTROL Online Minutes Interval]**, immetti il numero di minuti affinché la sessione del cliente sia visibile dall’amministratore. Lascia vuoto il campo per accettare l’intervallo predefinito di 15 minuti.

   - Per **[!UICONTROL Customer Data Lifetime]**, inserisci il numero di minuti che precedono la scadenza dei dati non salvati immessi dal cliente.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

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
