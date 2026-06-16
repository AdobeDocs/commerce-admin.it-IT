---
title: Conformità a PSD2
description: Scopri i requisiti della direttiva sui servizi di pagamento (PSD2) che potrebbero interessare il tuo negozio.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# Conformità a PSD2

A partire dal 14 settembre 2019, l&#39;Unione Europea richiede che tutti i commercianti nell&#39;UE e nel Regno Unito soddisfino i requisiti di [autenticazione forte del cliente](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) della direttiva sui servizi di pagamento (PSD2). I commercianti di tutti gli altri paesi sono incoraggiati a conformarsi a PSD2 come best practice.

>[!NOTE]
>
>Questo argomento è inteso solo a scopo informativo e non deve essere interpretato come consulenza legale. Per determinare se e come la tua azienda debba conformarsi ad obblighi di legge, consulta il tuo consulente legale.

L&#39;autenticazione avanzata del cliente è un componente chiave di PSD2 e richiede due dei seguenti elementi:

- Qualcosa che solo il cliente ha (password o PIN)
- Qualcosa che solo il cliente sa (token di sicurezza univoco generato dal telefono o dalla chiave fob)
- Qualcosa che riguarda solo il cliente (autenticazione biometrica come un&#39;impronta digitale o un riconoscimento facciale)

Le banche europee possono rifiutare i pagamenti che non soddisfano i requisiti. Tuttavia, le transazioni a basso rischio e a basso valore potrebbero ancora essere accettate e i pagamenti successivi in una sottoscrizione ricorrente.

A causa di questa modifica significativa e per garantire che i pagamenti dei clienti non vengano rifiutati, Adobe ha introdotto le seguenti modifiche e raccomandazioni per le integrazioni di pagamenti native [!DNL Commerce].

| Metodo di pagamento | Requisiti di conformità |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Per la maggior parte delle soluzioni PayPal, non è richiesta alcuna azione per conformarsi a PSD2, perché i requisiti sono gestiti da PayPal. Per informazioni su soluzioni specifiche, vedi la nota nella parte superiore di ciascun argomento di PayPal. |
| [Braintree](../stores-purchase/braintree.md) | A partire dal passaggio all’estensione installata nella versione 2.4.0, i requisiti vengono gestiti tramite il modulo Braintree Payments incluso e non è richiesta alcuna azione per conformarsi a PSD2. <br /><br />**_Nota:_** Per rispettare PSD2 utilizzando l&#39;integrazione di base nelle versioni precedenti, eseguire una delle operazioni seguenti:<br/>- (consigliato) Installare l&#39;estensione ufficiale dell&#39;integrazione dei pagamenti Braintree da [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}.<br/>- Abilitare e configurare il metodo di pagamento Braintree nella configurazione [!DNL Commerce].<br/><br/>Queste integrazioni di base precedenti supportano la verifica 3D Secure 2.0. Tuttavia, le implementazioni Braintree eseguite su JavaScript SDK v2 non supportano 3D Secure 2.0. |
| Altro | Per tutte le altre integrazioni di pagamenti, controllare le estensioni disponibili in [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}. Chiedi al tuo provider di pagamenti di consigliare una soluzione per il supporto dei requisiti di PSD2. |

{style="table-layout:auto"}
