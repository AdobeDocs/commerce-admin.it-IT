---
title: '[!DNL Commerce Intelligence] strumenti'
description: Scopri come i commercianti di Adobe Commerce e Magento Open Source possono utilizzare gli strumenti di Commerce Intelligence per ottenere l’insight utilizzato per prendere decisioni aziendali valide.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 0%

---

# [!DNL Commerce Intelligence] strumenti

Utilizza gli strumenti di Commerce Intelligence per ottenere l’insight utilizzato per prendere valide decisioni aziendali.

## Account [!DNL Commerce Intelligence]

Quando attivi un account [!DNL Commerce Intelligence] tramite Adobe, puoi accedere a cinque dashboard con circa 70 rapporti. Questi rapporti sono progettati per fornire approfondimenti sui tuoi dati e rispondere a domande come &quot;Come stanno crescendo i miei ordini mese su mese?&quot;, &quot;Chi sono i miei clienti più fedeli?&quot; e &quot;La mia strategia coupon funziona?&quot; Per informazioni dettagliate su questo set di strumenti, consulta la [Guida utente di Commerce Intelligence](https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html).

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] è incluso in Adobe Commerce e Magento Open Source. Questa funzione consente di accedere a una suite di rapporti dinamici basati sui dati di prodotti, ordini e clienti, con una dashboard personalizzata personalizzata in base alle esigenze aziendali. Mentre [!DNL Advanced Reporting] utilizza [!DNL Commerce Intelligence] per l&#39;analisi, non è necessario disporre di un account Commerce Intelligence per utilizzare [!DNL Advanced Reporting].

Per informazioni tecniche, vedere l&#39;argomento [[!DNL Advanced Reporting]](https://developer.adobe.com/commerce/php/development/advanced-reporting/){:target="_blank"} nella documentazione per gli sviluppatori.

>[!NOTE]
>
>A causa di problemi di compatibilità con [!DNL Adobe Commerce Intelligence], Commerce non è al momento in grado di supportare la generazione di rapporti avanzati utilizzando il bucket AWS S3 come supporto per il file di dati di origine in [!DNL Commerce Intelligence].

![Dashboard report avanzato](./assets/reporting-advanced.png){width="700"}

### Requisiti

* Il sito Web deve essere eseguito su un server Web pubblico.

* Il dominio deve disporre di un certificato di sicurezza (SSL) valido.

* Installazione o aggiornamento di [!DNL Commerce] completato senza errori.

* Nella configurazione [!DNL Commerce] per [URL archivio](../stores-purchase/store-urls.md), l&#39;impostazione **[!UICONTROL Base URL (Secure)]** per la visualizzazione archivio deve puntare all&#39;URL protetto. Esempio: `https://yourdomain.com`.

* Nella configurazione [!DNL Commerce] per gli URL dell&#39;archivio, **[!UICONTROL Use Secure URLs on Storefront]** e **[!UICONTROL Use Secure URLs in Admin]** devono essere impostati su `Yes`.

* [[!DNL Commerce] crontab](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) è stato creato e i processi cron sono in esecuzione sul server installato.

>[!NOTE]
>
>[!DNL Advanced Reporting] può essere utilizzato solo con [!DNL Commerce] installazioni che hanno utilizzato continuamente una singola [valuta di base](../stores-purchase/currency-configuration.md).


### Passaggio 1: abilitare [!DNL Advanced Reporting]

Nella configurazione [!DNL Commerce], [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) è abilitato per impostazione predefinita e viene avviato automaticamente se cron è [configurato](../configuration-reference/advanced/system.md) ed in esecuzione. Il tentativo di stabilire l’abbonamento viene avviato all’inizio di ogni ora nelle successive 24 ore fino al completamento dell’operazione. Lo stato dell’abbonamento è &quot;in sospeso&quot; fino a quando l’abbonamento non viene stabilito correttamente.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in cui è espanso **[!UICONTROL General]**, scegliere **[!UICONTROL Advanced Reporting]** ed effettuare le seguenti operazioni:

   * Verificare che **[!UICONTROL Advanced Reporting Service]** sia impostato su `Enable` (impostazione predefinita).

   * Impostare **[!UICONTROL Time of day to send data]** sull&#39;ora, il minuto e il secondo, in base a un orologio di 24 ore, in modo che il servizio riceva i dati aggiornati dall&#39;archivio. Per impostazione predefinita, i dati vengono inviati alle 2:00.

   * In **[!UICONTROL Industry Data]**, scegli **[!UICONTROL Industry]** che descrive meglio la tua attività.

   ![Configurazione report avanzata](./assets/advanced-reporting-config.png){width="400"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, fare clic su **[[!UICONTROL Cache Management]](../systems/cache-management.md)** nel messaggio nella parte superiore della pagina e aggiornare le cache non valide.

1. Attendi durante la notte o fino a dopo l’ora del prossimo aggiornamento pianificato. Quindi, controlla lo stato dell’abbonamento. Se lo stato è ancora _In sospeso_, assicurati che l&#39;installazione soddisfi tutti i requisiti.

### Passaggio 2: accedere a [!DNL Advanced Reporting]

1. Effettuare una delle seguenti operazioni:

   * Nella barra laterale _Admin_, scegli **[!UICONTROL Dashboard]**. Quindi fare clic su **[!UICONTROL Go to Advanced Reporting]**.
   * Nella barra laterale _Admin_, passa a **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   Il dashboard di [!DNL Advanced Reporting] fornisce un rapido riepilogo degli ordini, dei clienti e dei prodotti. Accertati di scorrere verso il basso per visualizzare l’intera dashboard.

1. Per ottenere una migliore visualizzazione dei dati, impostare **[!UICONTROL Filters]** nell&#39;angolo superiore destro sul periodo di tempo e la visualizzazione archivio che si desidera includere nel report. Quindi, effettua le seguenti operazioni:

   * Passa il cursore sopra un punto dati per ulteriori informazioni.
   * Per visualizzare tutti i rapporti del dashboard, fai clic su ogni scheda.

   ![Punto dati](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Accedi a [!DNL Advanced Reporting] risorse dati

Nell&#39;angolo superiore destro del dashboard Reporting avanzato, fare clic su **[!UICONTROL Additional Resources]**.

![Risorse dati di Reporting avanzato](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Risoluzione dei problemi

Se ricevi il messaggio 404 &quot;Pagina non trovata&quot;, verifica che l&#39;archivio soddisfi i requisiti per [!DNL Advanced Reporting]. Quindi, segui le istruzioni per verificare che l’integrazione sia installata.

### Verifica che l’integrazione sia attiva

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Verificare che l&#39;integrazione **[!UICONTROL Magento Analytics user]** sia presente nell&#39;elenco e che **[!UICONTROL Status]** sia `Active`.

1. Per ristabilire l&#39;utente, fare clic su **[!UICONTROL Reauthorize]** ed eseguire le operazioni seguenti:

   ![Riautorizza](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Quando richiesto, fare clic su **[!UICONTROL Reauthorize]** per approvare l&#39;accesso alle risorse API.

     ![Autorizza nuovamente l&#39;accesso alle risorse API](./assets/advanced-reporting-integration-api.png){width="600"}

   * Verifica che l’elenco dei token di integrazione per le estensioni sia completo. Quindi fare clic su **Fine**.

     ![Token di integrazione](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Cercare il messaggio che indica che l&#39;integrazione `Magento Analytics user` è stata nuovamente autorizzata.

1. Attendi durante la notte o fino a dopo l’ora del prossimo aggiornamento pianificato.

### Verifica valuta di base singola

[!DNL Advanced Reporting] può essere utilizzato solo con [!DNL Commerce] installazioni che hanno utilizzato una sola [valuta di base](../stores-purchase/currency-configuration.md) dall&#39;installazione. Il risultato è che nella cronologia tutti gli ordini utilizzano la stessa valuta di base. [!DNL Advanced Reporting] non funziona se in qualsiasi momento hai modificato la tua valuta di base e nella cronologia sono presenti ordini elaborati con valute di base diverse.

Per determinare se l&#39;archivio dispone di più valute di base, è possibile eseguire una query sul database [!DNL Commerce] dalla riga di comando utilizzando il seguente esempio di MySQL. Potrebbe essere necessario modificare i nomi delle tabelle in modo che corrispondano alla struttura dati:

```sql
select distinct base_currency_code from sales_order;
```

### Discrepanza dei dati

Se la didascalia di `Data last updated...` mostra la data di ieri e non quella di oggi, potrebbe verificarsi un ritardo di un giorno negli aggiornamenti di Advanced Reporting. Questo ritardo è dovuto a una coda più grande del previsto.

## Rapporti dashboard

**[!UICONTROL Orders]**

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Revenue] | Mostra tutti i ricavi ricevuti dalla visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Orders] | Mostra tutti gli ordini effettuati attraverso la vista del negozio durante il periodo di tempo definito. |
| [!UICONTROL AOV] | Mostra il valore medio dell&#39;ordine inserito nella vista del negozio durante il periodo di tempo definito. |
| [!UICONTROL Refunds] | Mostra tutti i rimborsi elaborati tramite la visualizzazione del punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Tax Collected] | Mostra tutte le imposte raccolte tramite la visualizzazione del punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Shipping Collected] | Mostra tutte le spese di spedizione raccolte tramite la visualizzazione del punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Orders by Status] | Mostra il numero di ordini per stato, per la visualizzazione del negozio durante il periodo di tempo definito. |
| [!UICONTROL Orders by Status] | Elenca un riepilogo del numero di ordini per stato. |
| [!UICONTROL Coupon Usage] | Elenca tutti i codici coupon e il numero di utenti per ciascuno, riscattati tramite la visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Orders and Revenue by Billing Region] | Elenca il numero di ordini e ricavi per area per la visualizzazione del punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Tax Collected by Billing Region] | Elenca l&#39;importo dell&#39;imposta riscossa per area per la visualizzazione del punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | Elenca le spese di spedizione riscosse per area per la visualizzazione del punto vendita durante il periodo di tempo definito. |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Unique Customers] | Mostra il numero di conti cliente univoci associati alla visualizzazione del punto vendita durante il periodo di tempo definito. |
| [!UICONTROL New Registered Accounts] | Mostra il numero di nuovi account cliente registrati nella visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Top Coupon Users] | Elenca gli utenti dei buoni sconto in base all&#39;ID cliente e il numero di ordini con buoni sconto per la visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Customer KPI Table] | Elenca il numero di ordini, ricavi e valore medio dell&#39;ordine in base all&#39;ID cliente per la visualizzazione del punto vendita durante il periodo di tempo definito. |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | Mostra il numero di prodotti venduti attraverso la visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Products Added to Wishlists] | Elenca tutti i prodotti aggiunti alla lista dei desideri tramite la visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Best Selling Products by Quantity] | Elenca i prodotti più venduti e la quantità venduta tramite la visualizzazione punto vendita durante il periodo di tempo definito. |
| [!UICONTROL Best Selling Products by Revenue] | Elenca i prodotti più venduti e i ricavi generati dalla vendita del prodotto tramite la visualizzazione punto vendita durante il periodo di tempo definito. |

{style="table-layout:auto"}
