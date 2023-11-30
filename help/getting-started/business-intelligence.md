---
title: '''[!DNL Commerce Intelligence] strumenti"'
description: Scopri in che modo Adobe Commerce e gli esercenti di Magento Open Source possono utilizzare gli strumenti Commerce Intelligence per acquisire le informazioni utilizzate per prendere decisioni aziendali valide.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 78bcac16713f9ec87faf7029732972db73216e79
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 0%

---

# [!DNL Commerce Intelligence] strumenti

Utilizza gli strumenti Commerce Intelligence per ottenere le informazioni utilizzate per prendere decisioni aziendali valide.

## [!DNL Commerce Intelligence] account

Quando si attiva una [!DNL Commerce Intelligence] tramite Adobe, puoi accedere a cinque dashboard con circa 70 rapporti. Questi rapporti sono progettati per fornire approfondimenti sui tuoi dati e rispondere a domande come &quot;Come stanno crescendo i miei ordini mese su mese?&quot;, &quot;Chi sono i miei clienti più fedeli?&quot; e &quot;La mia strategia coupon funziona?&quot; Per informazioni dettagliate su questo set di strumenti, vedere [Guida utente di Commerce Intelligence][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] è incluso in Adobe Commerce e Magento Open Source. Questa funzione consente di accedere a una suite di rapporti dinamici basati sui dati di prodotti, ordini e clienti, con una dashboard personalizzata personalizzata in base alle esigenze aziendali. Mentre [!DNL Advanced Reporting] utilizza [!DNL Commerce Intelligence] per le analisi, non è necessario disporre di un account Commerce Intelligence da utilizzare [!DNL Advanced Reporting].

Per informazioni tecniche, vedere [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} nella documentazione per gli sviluppatori.

>[!NOTE]
>
>Problemi di compatibilità con [!DNL Adobe Commerce Intelligence], Commerce non è al momento in grado di supportare la generazione di rapporti avanzati utilizzando AWS S3 Bucket come supporto per il file di dati di origine in [!DNL Commerce Intelligence].

![Dashboard report avanzati](./assets/reporting-advanced.png){width="700"}

### Requisiti

* Il sito Web deve essere eseguito su un server Web pubblico.

* Il dominio deve disporre di un certificato di sicurezza (SSL) valido.

* [!DNL Commerce] deve essere stato installato o aggiornato correttamente senza errori.

* In [!DNL Commerce] configurazione per [archiviare gli URL](../stores-purchase/store-urls.md), il **[!UICONTROL Base URL (Secure)]** l&#39;impostazione per la visualizzazione archivio deve puntare all&#39;URL protetto. Ad esempio: `https://yourdomain.com`.

* In [!DNL Commerce] configurazione degli URL del punto vendita, **[!UICONTROL Use Secure URLs on Storefront]** e **[!UICONTROL Use Secure URLs in Admin]** deve essere impostato su `Yes`.

* [[!DNL Commerce] crontab][3] è stato creato e i processi cron sono in esecuzione sul server installato.

>[!NOTE]
>
>[!DNL Advanced Reporting] può essere utilizzato solo con [!DNL Commerce] che hanno utilizzato in modo continuativo un unico [valuta di base](../stores-purchase/currency-configuration.md).


### Passaggio 1: abilitare [!DNL Advanced Reporting]

In [!DNL Commerce] configurazione, [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) è attivato per impostazione predefinita e viene avviato automaticamente se cron è [configurato](../configuration-reference/advanced/system.md) e in esecuzione. Il tentativo di stabilire l’abbonamento viene avviato all’inizio di ogni ora nelle successive 24 ore fino al completamento dell’operazione. Lo stato dell’abbonamento è &quot;in sospeso&quot; fino a quando l’abbonamento non viene stabilito correttamente.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra, dove **[!UICONTROL General]** è espanso, scegli **[!UICONTROL Advanced Reporting]** ed effettuare le seguenti operazioni:

   * Verifica che **[!UICONTROL Advanced Reporting Service]** è impostato su `Enable` (impostazione predefinita).

   * Imposta il **[!UICONTROL Time of day to send data]** all’ora, al minuto e al secondo secondo, secondo un orologio da 24 ore, in cui desideri che il servizio riceva i dati aggiornati dal tuo store. Per impostazione predefinita, i dati vengono inviati alle 02:00.

   * Sotto **[!UICONTROL Industry Data]**, scegli il **[!UICONTROL Industry]** descrive al meglio la tua attività.

   ![Configurazione report avanzato](./assets/advanced-reporting-config.png){width="400"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, fai clic su **[[!UICONTROL Cache Management]](../systems/cache-management.md)** nel messaggio nella parte superiore della pagina e aggiorna tutte le cache non valide.

1. Attendi durante la notte o fino a dopo l’ora del prossimo aggiornamento pianificato. Quindi, controlla lo stato dell’abbonamento. Se lo stato è ancora _in sospeso_, assicurarsi che l&#39;installazione soddisfi tutti i requisiti.

### Passaggio 2: accesso [!DNL Advanced Reporting]

1. Effettuare una delle seguenti operazioni:

   * Il giorno _Amministratore_ barra laterale, scegli **[!UICONTROL Dashboard]**. Quindi, fai clic su **[!UICONTROL Go to Advanced Reporting]**.
   * Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   Il [!DNL Advanced Reporting] la dashboard fornisce un rapido riepilogo degli ordini, dei clienti e dei prodotti. Accertati di scorrere verso il basso per visualizzare l’intera dashboard.

1. Per ottenere una migliore visualizzazione dei dati, impostare **[!UICONTROL Filters]** nell’angolo in alto a destra del periodo di tempo e della vista archivio che desideri includere nel rapporto. Quindi, effettua le seguenti operazioni:

   * Passa il cursore sopra un punto dati per ulteriori informazioni.
   * Per visualizzare tutti i rapporti del dashboard, fai clic su ogni scheda.

   ![Punto dati](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Accesso [!DNL Advanced Reporting] risorse di dati

Nell’angolo superiore destro del dashboard Reporting avanzato, fai clic su **[!UICONTROL Additional Resources]**.

![Risorse dati di Advanced Reporting](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Risoluzione dei problemi

Se ricevi un messaggio 404 &quot;Pagina non trovata&quot;, verifica che il tuo negozio soddisfi i requisiti per [!DNL Advanced Reporting]. Quindi, segui le istruzioni per verificare che l’integrazione sia installata.

### Verifica che l’integrazione sia attiva

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Verificare che **[!UICONTROL Magento Analytics user]** L&#39;integrazione viene visualizzata nell&#39;elenco e nella **[!UICONTROL Status]** è `Active`.

1. Per ristabilire l’utente, fai clic su **[!UICONTROL Reauthorize]** ed effettuare le seguenti operazioni:

   ![Riautorizza](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Quando richiesto, fai clic su **[!UICONTROL Reauthorize]** per approvare l’accesso alle risorse API.

     ![Autorizza nuovamente l’accesso alle risorse API](./assets/advanced-reporting-integration-api.png){width="600"}

   * Verifica che l’elenco dei token di integrazione per le estensioni sia completo. Quindi, fai clic su **Fine**.

     ![Token di integrazione](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Cerca il messaggio che indica l’integrazione `Magento Analytics user` viene nuovamente autorizzato.

1. Attendi durante la notte o fino a dopo l’ora del prossimo aggiornamento pianificato.

### Verifica valuta di base singola

[!DNL Advanced Reporting] può essere utilizzato solo con [!DNL Commerce] installazioni che hanno utilizzato un solo [valuta di base](../stores-purchase/currency-configuration.md) dall&#39;installazione. Il risultato è che nella cronologia tutti gli ordini utilizzano la stessa valuta di base. [!DNL Advanced Reporting] non funziona se, in qualsiasi momento, è stata modificata la valuta di base e nella cronologia sono presenti ordini elaborati con valute di base diverse.

Per determinare se il tuo negozio ha più valute di base, puoi eseguire una query sul tuo [!DNL Commerce] dalla riga di comando utilizzando il seguente esempio MySQL. Potrebbe essere necessario modificare i nomi delle tabelle in modo che corrispondano alla struttura dati:

```sql
select distinct base_currency_code from sales_order;
```

### Discrepanza dei dati

Se noti che il `Data last updated...` La didascalia mostra la data di ieri e non quella di oggi. Potrebbe verificarsi un ritardo fino a un giorno negli aggiornamenti di Advanced Reporting. Questo ritardo è dovuto a una coda più grande del previsto.

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


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
