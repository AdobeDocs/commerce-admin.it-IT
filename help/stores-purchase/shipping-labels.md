---
title: Etichette di spedizione
description: Scopri il flusso di lavoro delle etichette di spedizione per le spedizioni regolari e i prodotti con autorizzazione per la restituzione del materiale promozionale.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: 'https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 04d3134c-2afb-5bd7-ac14-e19fa935e848
    internal-label: Shipping/Delivery
  - id: 4820f335-ec9f-5611-8fe3-f5b7e3e56967
    internal-label: Orders
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%
---
# Etichette di spedizione

Commerce include un elevato livello di integrazione con i principali vettori di spedizione, che consente di accedere ai sistemi di spedizione dei vettori per tenere traccia degli ordini, creare etichette di spedizione e altro ancora. Le etichette di spedizione possono essere create per le spedizioni regolari e i prodotti con autorizzazione alla restituzione. Oltre alle informazioni fornite dal vettore di spedizione, l&#39;etichetta include anche il numero di ordine Commerce, il numero del pacchetto e la quantità totale di pacchetti per la spedizione.

![Etichetta spedizione prioritaria USPS](./assets/shipping-usps-priority-label.png){width="300"}

- [Configurare le etichette di spedizione](shipping-label-configure.md)
- [Creare etichette e pacchetti di spedizione](shipping-label-create.md)

## Flusso di lavoro etichetta spedizione

Le etichette di spedizione possono essere prodotte al momento della creazione di una spedizione o successivamente. Le etichette di spedizione vengono memorizzate in formato PDF e scaricate nel computer.

### Passaggio 1: il commerciante invia la richiesta di etichetta di spedizione

Il gestore del negozio completa le informazioni necessarie per generare le etichette e invia la richiesta.

### Passaggio 2: richiesta inviata al vettore

Commerce contatta il vettore di spedizione e crea un ordine nel sistema del vettore. Viene creato un ordine separato per ogni pacchetto spedito.

### Passaggio 3: il gestore invia l’etichetta e il numero di tracciamento

Il vettore invia l&#39;etichetta di spedizione e il numero di registrazione per la spedizione.

- Una singola spedizione con più pacchetti riceve più etichette di spedizione.

- Se si generano più volte le stesse etichette di spedizione, i numeri di registrazione originali vengono mantenuti.

- Per i prodotti restituiti con numeri RMA, i vecchi numeri di tracciamento vengono sostituiti da nuovi.

### Passaggio 4: l&#39;esercente scarica e stampa l&#39;etichetta

Una volta generata l&#39;etichetta di spedizione, la nuova spedizione viene salvata e l&#39;etichetta può essere stampata. Se non è possibile creare l&#39;etichetta di spedizione a causa di problemi di connessione o per altri motivi, la spedizione non viene creata. A seconda delle impostazioni del browser, è possibile aprire e stampare il file PDF. Ogni etichetta viene visualizzata in una pagina separata di PDF.
