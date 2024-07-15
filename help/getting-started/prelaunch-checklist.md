---
title: Elenco di controllo pre-avvio
description: Utilizza questo elenco per controllare le impostazioni di configurazione richieste per assicurarti che tutto sia corretto prima che il tuo archivio vada in produzione.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
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
