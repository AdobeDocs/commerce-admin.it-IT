---
title: Conformità a PSD2
description: Scopri i requisiti della direttiva sui servizi di pagamento (PSD2) che potrebbero interessare il tuo negozio.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Conformità a PSD2

A partire dal 14 settembre 2019, l&#39;Unione Europea richiede che tutti gli esercenti nell&#39;UE e nel Regno Unito soddisfino i requisiti di [autenticazione forte del cliente](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) della direttiva sui servizi di pagamento (PSD2). I commercianti di tutti gli altri paesi sono incoraggiati a conformarsi alle PSD2 come best practice.

>[!NOTE]
>
>Questo argomento è inteso solo a scopo informativo e non deve essere interpretato come consulenza legale. Per determinare se e come la tua azienda debba conformarsi ad obblighi di legge, consulta il tuo consulente legale.

L’autenticazione avanzata del cliente è un componente chiave di PSD2 e richiede due dei seguenti elementi:

- Qualcosa che solo il cliente ha (password o PIN)
- Qualcosa che solo il cliente sa (token di sicurezza univoco generato dal telefono o dalla chiave fob)
- Qualcosa che riguarda solo il cliente (autenticazione biometrica come un&#39;impronta digitale o un riconoscimento facciale)

Le banche europee possono rifiutare i pagamenti che non soddisfano i requisiti. Tuttavia, le transazioni a basso rischio e a basso valore potrebbero ancora essere accettate e i pagamenti successivi in una sottoscrizione ricorrente.

A causa di questo cambiamento significativo e per garantire che i pagamenti dei clienti non vengano rifiutati, Adobe ha introdotto le seguenti modifiche e raccomandazioni per le integrazioni di pagamenti native [!DNL Commerce].

| Metodo di pagamento | Requisiti di conformità |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Per la maggior parte delle soluzioni PayPal, non è richiesta alcuna azione per conformarsi a PSD2, perché i requisiti sono gestiti da PayPal. Per informazioni su soluzioni specifiche, vedi la nota nella parte superiore di ciascun argomento di PayPal. |
| [Braintree](../stores-purchase/braintree.md) | A partire dal passaggio all’estensione installata nella versione 2.4.0, i requisiti vengono gestiti tramite il modulo Braintree Payments incluso e non è richiesta alcuna azione per conformarsi a PSD2. <br /><br />**_Nota:_**Per rispettare PSD2 utilizzando l&#39;integrazione di base nelle versioni precedenti, eseguire una delle operazioni seguenti:<br/>- (consigliato) Installare l&#39;estensione ufficiale per l&#39;integrazione dei pagamenti Braintree da [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/>- Abilitare e configurare il metodo di pagamento Braintree nella configurazione [!DNL Commerce].<br/><br/>Queste integrazioni di base precedenti supportano la verifica 3D Secure 2.0. Tuttavia, le implementazioni Braintree eseguite su JavaScript SDK v2 non supportano 3D Secure 2.0. |
| Altro | Per tutte le altre integrazioni di pagamenti, controlla le estensioni disponibili su [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Chiedi al tuo provider di pagamenti di consigliare una soluzione per il supporto dei requisiti di PSD2. |

{style="table-layout:auto"}
