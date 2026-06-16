---
title: Panoramica sui pagamenti
description: Scopri i metodi e i servizi di pagamento supportati in modalità nativa in Adobe Commerce e Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
TQID: https://experienceleague.adobe.com/nu9qbRkc1OWOxkg-eERyZKuGwj0oc8wXDdSCMqGxe1I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157id: c32adafa-ed01-4b31-997e-2413013911b0
subfeature_v2: id: f2261633-201d-46c5-8a66-999e70527a83
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 900
ht-degree: 0%

---

# Panoramica sui pagamenti

Adobe Commerce e Magento Open Source supportano un’ampia gamma di metodi e servizi di pagamento. Ciò include diversi metodi di pagamento offline, tra cui il pagamento tramite assegno o vaglia postale e il contrassegno (contrassegno). Sono inoltre disponibili integrazioni native per numerose soluzioni di pagamento online e gateway, tra cui Braintree come estensione sviluppata da un fornitore in bundle.

>[!TIP]
>
>Payment Services per Adobe Commerce e Magento Open Source fornisce una soluzione self-service chiavi in mano, che include test sandbox e una configurazione semplice, per fornire un’elaborazione dei pagamenti solida e sicura. Per ulteriori informazioni su questo potente set di strumenti e su come può offrirti insight e il controllo di cui hai bisogno per creare la migliore esperienza per i tuoi acquirenti, consulta la [Guida utente per i servizi di pagamento](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html). Questa è la soluzione di pagamento predefinita in [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview).

>[!NOTE]
>
>Rivedi le [linee guida per la conformità PCI](../getting-started/compliance-pci.md) che delineano i requisiti impostati dal settore delle carte di pagamento (PCI) per le aziende che accettano il pagamento tramite carta di credito su Internet.

## Variazioni nella versione 2.4

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Alcune integrazioni di pagamenti ed estensioni in bundle sono state rimosse nelle versioni 2.4.x e spostate in Commerce Marketplace. Puoi trovare le ultime estensioni ufficiali di integrazione dei pagamenti in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.

- **Amazon Pay** e **Klarna**: le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includono queste estensioni sviluppate dal fornitore. A partire dalla versione 2.4.4, queste estensioni non sono più in bundle con la versione di base e devono essere installate e aggiornate da Commerce Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.

  Se hai abilitato e configurato una di queste estensioni in bundle, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Per ulteriori informazioni, vedere [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.

- **Worldpay**, **Eway**, **CyberSource** e **Authorize.Net**: per informazioni dettagliate sull&#39;esecuzione di una transizione sicura da queste integrazioni di pagamento, vedere [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Metodi di pagamento offline

Adobe Commerce e Magento Open Source includono diversi metodi di pagamento offline integrati che non richiedono i servizi di un’azienda di elaborazione dei pagamenti di terze parti:

- [Estrazione subtotale pari a zero](zero-subtotal-checkout.md)
- [Pagamento in contanti alla consegna](cash-on-delivery.md)
- [Pagamento bonifico](bank-transfer.md)
- [Assegno/vaglia postale](check-money-order.md)
- [Ordine di acquisto](purchase-order.md)
- [Pagamento sull&#39;account](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B)

## Metodi di pagamento online

Adobe Commerce e Magento Open Source supportano numerose soluzioni di pagamento che offrono servizi di vendita in tutte le parti del mondo. A differenza delle soluzioni di pagamento che trasferiscono il controllo a un&#39;altra sede per completare la transazione, un gateway di pagamento consente di accettare pagamenti con carta di credito direttamente dal tuo negozio senza che il cliente lasci la tua sede.

### Soluzioni consigliate

- [Servizi di pagamento](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [Pagamento PayPal Express](paypal-express-checkout.md)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} [Braintree](braintree.md)

### Altre soluzioni di pagamento PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Consulta [Soluzioni di pagamento PayPal](paypal.md) per ulteriori informazioni sulle opzioni del metodo di pagamento PayPal.

#### Soluzioni PayPal all-in-one

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

- [Pagamenti PayPal avanzati](paypal-payments-advanced.md)
- [Pagamenti PayPal Pro](paypal-payments-pro.md)
- [Pagamenti PayPal Standard](paypal-payments-standard.md)

#### Gateway di pagamento PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Collegamento flusso di pagamento PayPal](paypal-payflow-link.md)

## Protezione dalle frodi

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

I servizi e i filtri antifrode esaminano gli ordini inviati prima che la transazione venga elaborata per rilevare gli ordini fraudolenti e proteggerti dalle spese di chargeback. Adobe Commerce e Magento Open Source supportano le seguenti soluzioni di protezione dalle frodi:

- [Filtro gestione frodi PayPal](paypal.md#paypal-fraud-management-filters)

- [Soluzioni antifrode sul marketplace](https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection)

>[!NOTE]
>
>Per supportare gli aggiornamenti per la conformità in materia di sicurezza, la protezione antifrode Signifyd viene rimossa da Commerce a partire dalla versione 2.4.0. Se utilizzi l&#39;integrazione Signifyd in una versione 2.3.x o precedente, ti consigliamo di passare all&#39;estensione [Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}. Assicurati di mantenere gli aggiornamenti per l’estensione in conformità alle linee guida del fornitore.

## Risorse per la risoluzione dei problemi

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Per informazioni sulla risoluzione dei problemi relativi ai pagamenti, vedere la [Knowledge Base di supporto](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html).
