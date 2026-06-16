---
title: Introduzione ad Inventory management
description: Scopri come utilizzare le  [!DNL Inventory Management] funzionalità per gestire le scorte in più posizioni in modo che lo store [!DNL Commerce] rifletta accuratamente l'inventario fisico.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 0%

---

# Introduzione ad Inventory management

[!DNL Inventory Management] per [!DNL Commerce] offre gli strumenti per gestire l&#39;inventario dei prodotti. I commercianti con un singolo punto vendita in più magazzini, magazzini, ubicazioni di prelievo, corrieri diretti e altro ancora possono utilizzare queste funzioni per gestire le quantità per le vendite e gestire le spedizioni per completare gli ordini. Puoi tenere traccia delle quantità di magazzino, fornire ai clienti quantità di scorte vendibili precise per tutti i siti web e spedire in base a raccomandazioni basate sulla distanza o sulla priorità. Puoi anche configurare le configurazioni di prodotto preferite a livello globale (per tutti i negozi e i prodotti), per origine e per prodotto. Queste funzionalità crescono con la tua azienda, consentendoti di lavorare da un singolo magazzino o da una rete di spedizione complessa con alcune impostazioni aggiuntive.

Le funzionalità di [!DNL Inventory Management] includono:

- Configurazioni diverse per i commercianti il cui inventario proviene da un’unica origine e da più origini
- Scorte per tenere traccia delle quantità aggregate disponibili tramite le origini assegnate
- Protezione da estrazione simultanea
- Algoritmi di corrispondenza spedizione

>[!NOTE]
>
>Queste funzionalità sono state sviluppate come parte del progetto [Inventory management](https://github.com/magento/inventory) (precedentemente MSI) tramite il programma di progettazione della community.<br/>
>
>Il modulo [!DNL Inventory Management] è installato con Magento Open Source e Adobe Commerce, con tutte le funzionalità abilitate per impostazione predefinita. Per informazioni sulle modifiche incluse nelle versioni dei moduli, consulta le [Note sulla versione](release-notes.md).

## Terminologia di base

È importante comprendere i seguenti termini mentre si lavora con [!DNL Inventory Management]:

[!UICONTROL **Origini**] rappresentano le posizioni fisiche in cui vengono archiviati e spediti i prodotti disponibili. Queste sedi possono includere magazzini, negozi fisici, centri di distribuzione e corrieri diretti. Qualsiasi posizione può essere designata come origine per i prodotti virtuali.

[!UICONTROL **Scorte**] mappano un canale di vendita (attualmente limitato a siti Web) alle posizioni di origine e alle scorte disponibili. Un titolo può essere associato a più canali di vendita, ma un canale di vendita può essere assegnato a un solo titolo.

[!UICONTROL **Quantità venduta aggregata**] è l&#39;inventario virtuale totale che può essere venduto tramite un canale di vendita. L&#39;importo viene calcolato in tutte le origini assegnate a una scorta.

[!UICONTROL **Prenotazioni**] traccia le detrazioni dalla quantità vendibile quando i clienti aggiungono prodotti ai carrelli e completano il pagamento. Quando un ordine viene spedito, la prenotazione cancella e deduce gli importi spediti dalle quantità di magazzino di origine specifiche.
