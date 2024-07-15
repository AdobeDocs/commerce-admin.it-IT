---
title: Panoramica sui pagamenti
description: Scopri i metodi e i servizi di pagamento supportati in modalità nativa in Adobe Commerce e Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Panoramica sui pagamenti

Adobe Commerce e il Magento Open Source supportano vari metodi e servizi di pagamento che puoi offrire per facilitare il pagamento e offrire ai clienti la massima comodità. Questo elenco include diversi metodi di pagamento offline, tra cui il pagamento tramite assegno o vaglia postale e il contrassegno (contrassegno). Sono inoltre disponibili integrazioni native per numerose soluzioni di pagamento online e gateway, inclusa Braintree come estensione sviluppata da un fornitore in bundle.

>[!TIP]
>
>Payment Services per Adobe Commerce e Magento Open Source fornisce una soluzione self-service chiavi in mano, che include test sandbox e una configurazione semplice, per fornire un’elaborazione dei pagamenti solida e sicura. Per ulteriori informazioni su questo potente set di strumenti e su come può fornirti le informazioni e il controllo necessari per creare la migliore esperienza per i tuoi acquirenti, consulta la [Guida utente per i servizi di pagamento](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>Rivedi le [linee guida per la conformità PCI](../getting-started/compliance-pci.md) che delineano i requisiti impostati dal settore delle carte di pagamento (PCI) per le aziende che accettano il pagamento tramite carta di credito su Internet.

## Variazioni nella versione 2.4

Alcune integrazioni di pagamenti ed estensioni in bundle sono state rimosse nelle versioni 2.4.x e spostate in Commerce Marketplace. Puoi trovare le ultime estensioni ufficiali di integrazione dei pagamenti in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.

- **Amazon Pay** e **Klarna**: le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includono queste estensioni sviluppate dal fornitore. A partire dalla versione 2.4.4, queste estensioni non sono più incluse nella versione di base e devono essere installate e aggiornate dalla versione di Commerce Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.

  Se hai abilitato e configurato una di queste estensioni in bundle, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Per ulteriori informazioni, vedere [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.

- **Worldpay**, **Eway**, **CyberSource** e **Authorize.Net**: per informazioni dettagliate sull&#39;esecuzione di una transizione sicura da queste integrazioni di pagamento, vedere [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## Metodi di pagamento offline

Adobe Commerce e Magento Open Source includono diversi metodi di pagamento offline integrati che non richiedono i servizi di una società di elaborazione dei pagamenti di terze parti:

- [Estrazione subtotale pari a zero](zero-subtotal-checkout.md)
- [Pagamento in contanti alla consegna](cash-on-delivery.md)
- [Pagamento bonifico](bank-transfer.md)
- [Assegno/vaglia postale](check-money-order.md)
- [Ordine di acquisto](purchase-order.md)
- [Pagamento sull&#39;account](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile con Adobe Commerce B2B)

## Metodi di pagamento online

Adobe Commerce e il Magento Open Source supportano numerose soluzioni di pagamento che offrono servizi commerciali in tutte le parti del mondo. A differenza delle soluzioni di pagamento che trasferiscono il controllo a un&#39;altra sede per completare la transazione, un gateway di pagamento consente di accettare pagamenti con carta di credito direttamente dal tuo negozio senza che il cliente lasci la tua sede.

### Soluzioni consigliate

- [Servizi di pagamento](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [Pagamento PayPal Express](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Altre soluzioni di pagamento PayPal

Consulta [Soluzioni di pagamento PayPal](paypal.md) per ulteriori informazioni sulle opzioni del metodo di pagamento PayPal.

#### Soluzioni PayPal all-in-one

- [Pagamenti PayPal avanzati](paypal-payments-advanced.md)
- [Pagamenti PayPal Pro](paypal-payments-pro.md)
- [Pagamenti PayPal Standard](paypal-payments-standard.md)

#### Gateway di pagamento PayPal

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Collegamento flusso di pagamento PayPal](paypal-payflow-link.md)

## Protezione dalle frodi

I servizi e i filtri antifrode esaminano gli ordini inviati prima che la transazione venga elaborata per rilevare gli ordini fraudolenti e proteggerti dalle spese di chargeback. Adobe Commerce e il Magento Open Source supportano le seguenti soluzioni di protezione dalle frodi:

- [Filtro gestione frodi PayPal](paypal.md#paypal-fraud-management-filters)

- [Soluzioni di protezione dalle frodi nel Marketplace][1]

>[!NOTE]
>
>Per supportare gli aggiornamenti per la conformità in materia di sicurezza, la protezione antifrode Signifyd viene rimossa da Commerce a partire dalla versione 2.4.0. Se utilizzi l’integrazione Signifyd in una versione 2.3.x o precedente, ti consigliamo di passare all’estensione [Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target=&quot;_blank&quot;}. Assicurati di mantenere gli aggiornamenti per l’estensione in conformità alle linee guida del fornitore.

## Risorse per la risoluzione dei problemi

Per informazioni sulla risoluzione dei problemi relativi ai pagamenti, vedere la [Knowledge Base di supporto](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
