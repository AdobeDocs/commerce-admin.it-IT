---
title: Impostazione vettore di spedizione
description: Scopri il supporto per gli account di spedizione commerciali disponibile per il tuo negozio.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Impostazione vettore di spedizione

Se hai un account commerciale con un vettore supportato, puoi offrire ai tuoi clienti la comodità di scegliere tale vettore durante il pagamento. Le tariffe vengono scaricate automaticamente, pertanto non è necessario cercare le informazioni.

>[!NOTE]
>
>Consulta [Commerce Marketplace](../getting-started/commerce-marketplace.md) per ulteriori servizi di spedizione per l&#39;installazione di Commerce.

Prima di poter offrire ai clienti una selezione di vettori di spedizione, devi completare i seguenti passaggi:

- Configura le [impostazioni di spedizione](shipping-settings.md) per stabilire il punto di origine per l&#39;archivio.

- Configurare le impostazioni per ogni servizio vettore che si desidera offrire.

   - [**UPS**](ups.md) - United Parcel Service (UPS) offre servizi di spedizione nazionali e internazionali via terra e via aerea a più di 220 paesi.
   - [**USPS**](usps.md) - Il servizio postale degli Stati Uniti (USPS) è il servizio postale indipendente del governo degli Stati Uniti. USPS offre servizi di spedizione nazionali e internazionali via terra e per via aerea.
   - [**FedEx**](fedex.md) - FedEx offre servizi di spedizione nazionali e internazionali via terra e via aria verso più di 220 paesi.
   - [**DHL**](dhl.md) - DHL offre servizi internazionali integrati e soluzioni personalizzate incentrate sul cliente per la gestione e il trasporto di lettere, merci e informazioni.

## Peso dimensionale

Il peso dimensionale, talvolta chiamato peso volumetrico, è una pratica comune dell&#39;industria che basa il prezzo di trasporto su una combinazione di peso e volume del pacchetto. In termini semplici, il peso dimensionale determina la tariffa di spedizione in base alla quantità di spazio occupato da un pacchetto nel vano di carico del vettore. Il peso dimensionale è tipicamente utilizzato quando un pacchetto è relativamente leggero rispetto al suo volume.

Tutti i principali vettori applicano il peso dimensionale ad alcune spedizioni. Tuttavia, il modo in cui viene applicato il prezzo del peso dimensionale varia da un vettore all&#39;altro. Se la tua azienda ha un elevato volume di spedizioni, anche una leggera differenza nel prezzo di spedizione può tradursi in migliaia di dollari nel corso di un anno.

## Configurazione

Le opzioni di configurazione variano a seconda del gestore. Tuttavia, tutti richiedono i seguenti passaggi:

1. Apri un conto di spedizione con il vettore.

1. Inserisci il numero di account o l’ID utente e l’URL del gateway per il sistema nella configurazione dell’archivio.

### API degli strumenti web USPS obsoleta

Le versioni 2.4.6, 2.4.7 e 2.4.8 di Adobe Commerce utilizzano le API legacy degli strumenti web per l’integrazione preconfigurata delle soluzioni di spedizione con USPS. USPS ha introdotto le API USPS, una piattaforma basata su REST che sostituisce le API legacy degli strumenti web.

Il 25 gennaio 2026, USPS ritirerà le API degli strumenti web legacy. Dopo questa data, tutte le richieste alle API degli strumenti web avranno esito negativo.

Per evitare interruzioni dei servizi di spedizione USPS, effettua le seguenti azioni prima del 25 gennaio 2026:

- Applica la patch di qualità per la migrazione di [API REST USPS](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/usps-rest-api-migration-patch.html) (AC-1520) per aggiungere il supporto per l&#39;integrazione con le API REST USPS.

- Aggiorna la configurazione USPS di Commerce per utilizzare le API REST:

   - [Configurazione vettore di spedizione USPS](usps.md)

   - [Configurazione etichetta spedizione](shipping-label-create.md)

