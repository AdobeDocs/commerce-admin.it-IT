---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] > [!UICONTROL Payment Methods] dell'amministratore di Commerce.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
TQID: https://experienceleague.adobe.com/Z6f-lyypn4xUeVxiR0SQ81PswzU69X3sVCqEa8bTDnc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
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
source-wordcount: 1746
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Payment Services per Adobe Commerce e Magento Open Source fornisce una soluzione self-service chiavi in mano, che include test sandbox e una configurazione semplice, per fornire un’elaborazione dei pagamenti solida e sicura. Per ulteriori informazioni su questo potente set di strumenti e su come può offrirti insight e il controllo di cui hai bisogno per creare la migliore esperienza per i tuoi acquirenti, consulta la [_Guida utente per i servizi di pagamento_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

![Posizione commerciante](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Sito Web | Identifica il paese in cui l&#39;esercente è registrato per esercitare l&#39;attività. |

{style="table-layout:auto"}

## Soluzioni consigliate

Le seguenti soluzioni di pagamento sono consigliate come un modo semplice per gli esercenti che stanno iniziando ad accettare il pagamento online tramite conto PayPal o carta di credito. Man mano che la tua azienda cresce, puoi combinarli con altre soluzioni di pagamento PayPal.

- [Servizi di pagamento](payment-services.md)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [Pagamento PayPal Express](paypal-express-checkout.md)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [Braintree](braintree.md)

>[!NOTE]
>
>Alcune integrazioni di pagamenti ed estensioni in bundle sono state rimosse nelle versioni 2.4.x e spostate in Commerce Marketplace. Puoi trovare le ultime estensioni ufficiali di integrazione dei pagamenti in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>>**Amazon Pay** e **Klarna**: le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includono queste estensioni sviluppate dal fornitore. A partire dalla versione 2.4.4, queste estensioni non sono più in bundle con la versione di base e devono essere installate e aggiornate da Commerce Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.
><br/>>Se una di queste estensioni in bundle è abilitata e configurata, devi aggiornare il file `composer.json` come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Per ulteriori informazioni, vedere [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.<br/>
><br/>>**Worldpay**, **Eway**, **CyberSource** e **Authorize.Net**: per informazioni dettagliate sull&#39;esecuzione di una transizione sicura da queste integrazioni di pagamento, vedere [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Altri metodi PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

PayPal offre diverse soluzioni di pagamento che soddisfano le esigenze delle aziende di ogni dimensione e che operano in tutto il mondo. PayPal consente di accettare pagamenti da tutte le principali carte di debito e di credito. PayPal offre ulteriore comodità senza sforzi aggiuntivi, perché anche i clienti che non hanno un conto PayPal possono pagare i loro acquisti con PayPal.

### Metodi all-in-one PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

- [Pagamento PayPal anticipato](paypal-payments-advanced.md)
- [Pagamenti PayPal Pro](paypal-payments-pro.md)
- [Pagamenti PayPal Standard](paypal-payments-standard.md)

### Gateway di pagamento PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

- [PayPal Payflow Pro](paypal-payflow-pro.md) (Comprende Pagamento rapido)
- [PayPal Payflow Link](paypal-payflow-link.md) (Include Pagamento Espresso)

## Metodi di pagamento di base

I seguenti metodi di pagamento sono incorporati in Commerce e non utilizzano un fornitore di servizi di pagamento di terze parti per elaborare la transazione. Molti dei metodi di pagamento di base sono gestiti offline anziché online.

### [!UICONTROL Check / Money Order]

![Assegno/vaglia postale](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Determina se i clienti possono pagare tramite assegno o vaglia postale. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Il nome di questo metodo di pagamento che viene visualizzato ai clienti durante il pagamento. |
| [!UICONTROL New Order Status] | Sito Web | Determina lo stato iniziale dell&#39;[ordine](../../stores-purchase/order-status.md) assegnato agli ordini pagati tramite assegno o vaglia postale. Valore predefinito: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sito Web | Determina i paesi da cui si accetta il pagamento tramite assegno o vaglia postale. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sito Web | Identifica i paesi specifici da cui si accetta il pagamento tramite assegno o vaglia postale. |
| [!UICONTROL Make Check Payable to] | Visualizzazione store | Il nome dell&#39;entità a cui gli assegni e i vaglia postali dovrebbero essere esigibili. |
| [!UICONTROL Send Check to] | Visualizzazione store | Indirizzo stradale o casella postale presso il quale devono essere inviati gli assegni e i vaglia postali. |
| [!UICONTROL Minimum Order Total] | Sito Web | Importo minimo dell&#39;ordine che può essere pagato tramite assegno o vaglia postale. |
| [!UICONTROL Maximum Order Total] | Sito Web | L&#39;importo massimo dell&#39;ordine che può essere pagato tramite assegno o vaglia postale. <br/><br/>**_Note:_** Un ordine è idoneo se il totale è compreso tra, o corrisponde, al totale minimo o massimo dell&#39;ordine. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione del pagamento tramite assegno o vaglia postale se elencato con altri metodi di pagamento durante il pagamento. Immetti `0` per collocarlo all&#39;inizio dell&#39;elenco. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Bonifico bancario](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Determina se i clienti possono pagare trasferendo il pagamento direttamente dalla banca al conto dell&#39;esercente. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Il nome di questo metodo di pagamento che viene visualizzato ai clienti durante il pagamento. |
| [!UICONTROL New Order Status] | Sito Web | Determina lo stato dell&#39;ordine iniziale assegnato agli ordini pagati tramite bonifico bancario. Valore predefinito: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sito Web | Determina i paesi da cui si accetta il pagamento tramite bonifico bancario. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sito Web | Identifica i paesi specifici da cui si accetta il pagamento tramite bonifico bancario. |
| [!UICONTROL Minimum Order Total] | Sito Web | Importo minimo dell&#39;ordine che può essere pagato tramite bonifico bancario. |
| [!UICONTROL Maximum Order Total] | Sito Web | L&#39;importo massimo dell&#39;ordine che può essere pagato tramite bonifico bancario. <br/><br/>**_Note:_** Un ordine è idoneo se il totale è compreso tra, o corrisponde, al totale minimo o massimo dell&#39;ordine. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione del pagamento tramite bonifico bancario se elencato con altri metodi di pagamento durante il pagamento. Immetti `0` per collocarlo all&#39;inizio dell&#39;elenco. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Pagamento sull&#39;account](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Determina se le società possono utilizzare il credito aziendale per effettuare acquisti. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Il nome di questo metodo di pagamento che viene visualizzato ai clienti durante il pagamento. |
| [!UICONTROL New Order Status] | Sito Web | Determina lo stato dei nuovi ordini addebitati a un conto della società. Opzioni: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Sito Web | Determina i paesi in cui le aziende possono addebitare gli acquisti sui propri conti. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sito Web | Identifica i paesi specifici in cui le aziende possono addebitare gli acquisti sui propri conti. |
| [!UICONTROL Minimum Order Total] | Sito Web | Specifica l&#39;importo dell&#39;ordine più piccolo che può essere addebitato a un conto aziendale. |
| [!UICONTROL Maximum Order Total] | Sito Web | L&#39;importo massimo dell&#39;ordine che può essere addebitato a un conto aziendale. <br/><br/>**_Note:_** Un ordine è idoneo se il totale è compreso tra, o corrisponde, al totale minimo o massimo dell&#39;ordine. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione del pagamento dell&#39;acconto se elencato con altri metodi di pagamento durante il pagamento. Immetti `0` per collocarlo all&#39;inizio dell&#39;elenco. |

{style="table-layout:auto"}

>[!NOTE]
>
>Il pagamento in conto non è supportato per gli ordini con [più indirizzi di spedizione](../../stores-purchase/shipping-settings.md#multiple-addresses) e non viene visualizzato tra le opzioni di pagamento.

### [!UICONTROL Cash On Delivery Payment]

![Pagamento Alla Consegna](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Determina se i clienti possono pagare trasferendo il pagamento direttamente dalla banca al conto dell&#39;esercente. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Il nome di questo metodo di pagamento che viene visualizzato ai clienti durante il pagamento. |
| [!UICONTROL New Order Status] | Sito Web | Determina lo stato dell&#39;ordine iniziale assegnato agli ordini pagati tramite bonifico bancario. Valore predefinito: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sito Web | Determina i paesi da cui si accetta il pagamento tramite bonifico bancario. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sito Web | Identifica i paesi specifici da cui si accetta il pagamento tramite bonifico bancario. |
| [!UICONTROL Minimum Order Total] | Sito Web | Specifica l&#39;importo minimo dell&#39;ordine che può essere pagato tramite bonifico bancario. |
| [!UICONTROL Maximum Order Total] | Sito Web | L&#39;importo massimo dell&#39;ordine che può essere pagato tramite bonifico bancario. <br/><br/>**_Note:_** Un ordine è idoneo se il totale è compreso tra, o corrisponde, al totale minimo o massimo dell&#39;ordine. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione del pagamento tramite bonifico bancario se elencato con altri metodi di pagamento durante il pagamento. Immetti `0` per collocarlo all&#39;inizio dell&#39;elenco. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Estrazione Subtotale Zero](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Title] | Visualizzazione store | Nome utilizzato per questo metodo di pagamento durante l&#39;estrazione. Valore predefinito: nessuna informazione di pagamento richiesta |
| [!UICONTROL Enabled] | Sito Web | Determina se l&#39;opzione Estrazione subtotale zero è disponibile per consentire all&#39;amministratore del negozio di gestire gli ordini con un subtotale pari a zero, ad esempio quelli che sono stati tassati, ma che uno sconto ha ridotto l&#39;importo a zero. Opzioni: `Yes` / `No` |
| [!UICONTROL New Order Status] | Sito Web | Determina lo stato dell&#39;ordine iniziale assegnato agli ordini elaborati come Checkout subtotale zero. Valore predefinito: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sito Web | Determina i paesi da cui è possibile applicare il Check-Out del subtotale zero. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sito Web | Identifica i paesi specifici per i quali è possibile applicare il Checkout subtotale zero. |
| [!UICONTROL Sort Order] | Sito Web | Un numero che determina l&#39;ordine in cui il titolo, ad esempio &quot;Nessuna informazione di pagamento è richiesta&quot;, viene visualizzato quando elencato con altri metodi di pagamento durante il pagamento. Immetti `0` per collocarlo all&#39;inizio dell&#39;elenco. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Le azioni di pagamento sono configurate _per metodo di pagamento_. L&#39;azione di pagamento determina quando vengono acquisiti i fondi e quando vengono create le fatture per gli ordini di vendita.

Per un elenco completo delle singole opzioni di configurazione, consulta la sezione Impostazioni di base di ogni singolo metodo di pagamento.

| Azione di pagamento | Descrizione |
|--- |---|
| [!UICONTROL Authorization] | Approva l&#39;acquisto, ma blocca i fondi. L&#39;importo non viene prelevato fino a quando non viene catturato dal commerciante. |
| [!UICONTROL Authorize] | Autorizza il conto dell&#39;acquirente per il totale dell&#39;ordine ma non acquisisce il pagamento. Acquisisci il pagamento creando una fattura. È possibile annullare o annullare gli ordini autorizzati. |
| [!UICONTROL Authorize and Capture] | Autorizza il conto dell&#39;acquirente per il totale dell&#39;ordine e acquisisce il pagamento. Viene creata automaticamente una fattura. È possibile rimborsare i fondi acquisiti tramite nota di credito. Non puoi annullare un ordine una volta acquisito il pagamento. |
| [!UICONTROL Charge on shipment] | Amazon riceve una richiesta di acquisizione e addebita al cliente una fattura creata in Commerce. |
| [!UICONTROL Charge on order] | Amazon crea la fattura e addebita al cliente quando l&#39;ordine viene effettuato. |
| [!UICONTROL Not Capture] | Quando la fattura viene inviata, il sistema non acquisisce il pagamento. Si presume che il pagamento venga acquisito tramite Commerce in un secondo momento. Nella fattura completata è presente un pulsante Acquisisci. Prima dell&#39;acquisizione, è possibile annullare la fattura. Dopo l&#39;acquisizione, è possibile creare una nota di accredito e annullare la fattura. |
| [!UICONTROL Order] | Rappresenta un accordo con PayPal che consente all&#39;esercente di acquisire uno o più importi fino al totale dell&#39;ordine dal conto dell&#39;acquirente del cliente, entro un periodo di tempo definito (fino a 29 giorni). |
| [!UICONTROL Sale] | L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente. |

{style="table-layout:auto"}

>[!NOTE]
>
>Non selezionare l&#39;opzione _[!UICONTROL Not Capture]_&#x200B;a meno che non si sia certi che il pagamento verrà acquisito tramite Commerce in un secondo momento. Non è possibile creare una nota di accredito finché il pagamento non viene acquisito utilizzando il pulsante Acquisisci.

## [!UICONTROL Purchase Order]

![Ordine di acquisto](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Determina se i clienti possono pagare per ordine di acquisto (OA). Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Il nome di questo metodo di pagamento che viene visualizzato ai clienti durante il pagamento. |
| [!UICONTROL New Order Status] | Sito Web | Determina lo stato iniziale dell&#39;[ordine](../../stores-purchase/order-status.md) assegnato agli ordini pagati da OA. Valore predefinito: In sospeso |
| [!UICONTROL Payment from Applicable Countries] | Sito Web | Determina i paesi dai quali si accetta il pagamento tramite OA. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sito Web | Identifica i paesi specifici da cui si accetta il pagamento tramite OA. |
| [!UICONTROL Minimum Order Total] | Sito Web | Importo minimo dell&#39;ordine che può essere pagato da OA. |
| [!UICONTROL Maximum Order Total] | Sito Web | Importo massimo dell&#39;ordine che può essere pagato da OA. <br/><br/>**_Note:_** Un ordine è idoneo se il totale è compreso tra, o corrisponde, al totale minimo o massimo dell&#39;ordine. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione del pagamento tramite OA quando viene elencato con altri metodi di pagamento durante il pagamento. Immetti `0` per collocarlo all&#39;inizio dell&#39;elenco. |

{style="table-layout:auto"}
