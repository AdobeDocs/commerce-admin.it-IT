---
title: Elenco di controllo pre-avvio
description: Utilizza questo elenco per controllare le impostazioni di configurazione richieste per assicurarti che tutto sia corretto prima che il tuo archivio vada in produzione.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/cthgB115wuL6ewlKBtfOXwfqevj2jpbdARQHB9pvIcc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 416
ht-degree: 0%

---

# Elenco di controllo pre-avvio

Dopo aver completato la progettazione, lo sviluppo e il test dell&#39;archivio, verificare le seguenti impostazioni di configurazione per verificare che tutto sia corretto prima che l&#39;archivio _venga attivato_. Per una descrizione completa di tutte le impostazioni di configurazione, vedi [_Riferimento configurazione_](../configuration-reference/guide-overview.md).

## Impostazioni generali

- [URL archivio](../stores-purchase/store-urls.md) - Verifica che gli URL archivio per la vetrina e l&#39;amministratore siano corretti per un ambiente di produzione live.
- Certificato di sicurezza: prima di avviare l’archivio, installa un certificato di sicurezza firmato e attendibile al 100% per il dominio specificato nell’URL di base.
- [Archivia indirizzi e-mail](../getting-started/store-details.md#store-email-addresses) - Completa tutti gli indirizzi e-mail utilizzati per inviare e ricevere notifiche e-mail, ad esempio nuovi ordini, fatture, spedizioni, note di credito, avvisi sul prezzo del prodotto e newsletter. Assicurati che ogni campo contenga un indirizzo e-mail aziendale valido.

## Impostazioni marketing

- [Modelli e-mail](../systems/email-templates.md) - Aggiorna i modelli e-mail predefiniti per riflettere il tuo marchio. Se crei dei modelli, assicurati di aggiornare la configurazione.
- [Comunicazioni di vendita](../stores-purchase/introduction.md#order-management-and-operations) - Assicurarsi che le fatture e i documenti di trasporto includano le informazioni aziendali corrette e riflettano il proprio marchio.
- [Strumenti Google](../merchandising-promotions/google-tools.md) - [!DNL Commerce] fornisce l&#39;integrazione con l&#39;API Google per consentire alla tua azienda di utilizzare Google Analytics e Google AdWords.

## Impostazioni di vendita

- [Opzioni carrello](../stores-purchase/cart-configuration.md) - Esaminare le impostazioni di configurazione del carrello per verificare se è necessario apportare modifiche, ad esempio impostare l&#39;importo minimo dell&#39;ordine e la durata dei prezzi nel carrello.
- [Opzioni di estrazione](../stores-purchase/checkout-process.md#checkout-options) - Esaminare le opzioni di estrazione per verificare se è necessario apportare modifiche, ad esempio impostare termini e condizioni e configurare l&#39;estrazione guest.
- [Imposte](../stores-purchase/taxes.md) - Assicurati che le imposte siano configurate correttamente in base alle tue regole fiscali aziendali e ai requisiti locali.
- [Metodi di consegna](../stores-purchase/delivery.md) - Abilita tutti i gestori e i metodi di consegna che devono essere utilizzati dalla società.
- [PayPal](../stores-purchase/paypal.md) - Se intendi offrire ai tuoi clienti la comodità di pagare con PayPal, apri un conto PayPal per esercenti e imposta un metodo di pagamento. Esegui alcune transazioni di test in modalità sandbox prima che il negozio diventi attivo.
- [Metodi di pagamento](../stores-purchase/payments.md) - Abilita i metodi di pagamento che intendi utilizzare e accertati che siano configurati correttamente. Controlla le impostazioni dello stato dell’ordine, la valuta accettata, i paesi consentiti e così via.

## Impostazioni di sistema

[Cron (Attività pianificate)](../systems/cron.md) - I processi Cron vengono utilizzati per elaborare e-mail, regole dei prezzi di catalogo, newsletter, avvisi cliente, sitemap di Google, aggiornare i tassi di valuta e così via. Verificare che i processi Cron siano impostati per l&#39;esecuzione nell&#39;intervallo di tempo appropriato, in minuti.
