---
title: Elenco di controllo pre-avvio
description: Utilizza questo elenco per controllare le impostazioni di configurazione richieste per assicurarti che tutto sia corretto prima che il tuo archivio vada in produzione.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Elenco di controllo pre-avvio

Dopo aver completato la progettazione, lo sviluppo e il test del punto vendita, controlla le seguenti impostazioni di configurazione per assicurarti che tutto sia corretto prima del punto vendita _diventa live_. Per una descrizione completa di ogni impostazione di configurazione, vedi [_Riferimento configurazione_](../configuration-reference/guide-overview.md).

## Impostazioni generali

- [URL store](../stores-purchase/store-urls.md) : verifica che gli URL dello store per la vetrina e l’Amministratore siano corretti per un ambiente di produzione live.
- Certificato di sicurezza: prima di avviare l’archivio, installa un certificato di sicurezza firmato e attendibile al 100% per il dominio specificato nell’URL di base.
- [Memorizza indirizzi e-mail](../getting-started/store-details.md#store-email-addresses) : completa tutti gli indirizzi e-mail utilizzati per inviare e ricevere notifiche e-mail, ad esempio nuovi ordini, fatture, spedizioni, note di credito, avvisi sul prezzo dei prodotti e newsletter. Assicurati che ogni campo contenga un indirizzo e-mail aziendale valido.

## Impostazioni marketing

- [Modelli e-mail](../systems/email-templates.md) : aggiorna i modelli e-mail predefiniti per riflettere il tuo marchio. Se crei dei modelli, assicurati di aggiornare la configurazione.
- [Comunicazioni di vendita](../stores-purchase/introduction.md#order-management-and-operations) - Assicurati che le fatture e i documenti di trasporto includano le informazioni aziendali corrette e riflettano il tuo marchio.
- [Strumenti Google](../merchandising-promotions/google-tools.md) - [!DNL Commerce] offre integrazione con le API Google per consentire alla tua azienda di utilizzare Google Analytics e Google AdWords.

## Impostazioni di vendita

- [Opzioni carrello](../stores-purchase/cart-configuration.md) - Osserva le impostazioni di configurazione del carrello per verificare se è necessario apportare modifiche, ad esempio per impostare l’importo minimo dell’ordine e la durata dei prezzi nel carrello.
- [Opzioni di pagamento](../stores-purchase/checkout-process.md#checkout-options) - Esaminare le opzioni di pagamento per verificare se è necessario apportare modifiche, ad esempio impostare termini e condizioni e configurare il pagamento come ospite.
- [Imposte](../stores-purchase/taxes.md) : assicurati che le imposte siano configurate correttamente in base alle tue regole fiscali aziendali e ai requisiti locali.
- [Metodi di consegna](../stores-purchase/delivery.md) - Abilita tutti i vettori e i metodi di consegna che devono essere utilizzati dall&#39;azienda.
- [PayPal](../stores-purchase/paypal.md) - Se intendi offrire ai clienti la comodità di pagare con PayPal, apri un conto PayPal per esercenti e imposta un metodo di pagamento. Esegui alcune transazioni di test in modalità sandbox prima che il negozio diventi attivo.
- [Metodi di pagamento](../stores-purchase/payments.md) : abilita i metodi di pagamento che intendi utilizzare e assicurati che siano configurati correttamente. Controlla le impostazioni dello stato dell’ordine, la valuta accettata, i paesi consentiti e così via.

## Impostazioni di sistema

[Cron (attività pianificate)](../systems/cron.md) - I processi Cron vengono utilizzati per elaborare e-mail, regole dei prezzi di catalogo, newsletter, avvisi sui clienti, sitemap di Google, tassi di valuta di aggiornamento e così via. Verificare che i processi Cron siano impostati per l&#39;esecuzione nell&#39;intervallo di tempo appropriato, in minuti.
