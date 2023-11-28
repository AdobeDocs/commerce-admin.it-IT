---
title: Introduzione ad Inventory management
description: Scopri come utilizzare [!DNL Inventory Management] funzioni per gestire le azioni in più sedi in modo che [!DNL Commerce] il magazzino riflette accuratamente l'inventario fisico.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Introduzione ad Inventory management

[!DNL Inventory Management] per [!DNL Commerce] offre gli strumenti per gestire l’inventario dei prodotti. I commercianti con un singolo punto vendita in più magazzini, magazzini, ubicazioni di prelievo, corrieri diretti e altro ancora possono utilizzare queste funzioni per gestire le quantità per le vendite e gestire le spedizioni per completare gli ordini. Puoi tenere traccia delle quantità di magazzino, fornire ai clienti quantità di scorte vendibili precise per tutti i siti web e spedire in base a raccomandazioni basate sulla distanza o sulla priorità. Puoi anche configurare le configurazioni di prodotto preferite a livello globale (per tutti i negozi e i prodotti), per origine e per prodotto. Queste funzionalità crescono con la tua azienda, consentendoti di lavorare da un singolo magazzino o da una rete di spedizione complessa con alcune impostazioni aggiuntive.

[!DNL Inventory Management] Le caratteristiche includono:

- Configurazioni diverse per i commercianti il cui inventario proviene da un’unica origine e da più origini
- Scorte per tenere traccia delle quantità aggregate disponibili tramite le origini assegnate
- Protezione da estrazione simultanea
- Algoritmi di corrispondenza spedizione

>[!NOTE]
>
>Queste funzioni sono state sviluppate nell&#39;ambito del [Inventory management](https://github.com/magento/inventory) (precedentemente MSI) tramite il programma di progettazione della community.<br/>
>
>Il [!DNL Inventory Management] Il modulo viene installato con Magento Open Source e Adobe Commerce, con tutte le funzioni abilitate per impostazione predefinita. Per informazioni sulle modifiche incluse nelle versioni dei moduli, vedi [Note sulla versione](release-notes.md).

## Terminologia di base

È importante comprendere i seguenti termini mentre si lavora con [!DNL Inventory Management]:

[!UICONTROL **Sorgenti**] rappresenta le ubicazioni fisiche in cui vengono immagazzinati e spediti i prodotti disponibili. Queste sedi possono includere magazzini, negozi fisici, centri di distribuzione e corrieri diretti. Qualsiasi posizione può essere designata come origine per i prodotti virtuali.

[!UICONTROL **Scorte**] mappare un canale di vendita (attualmente limitato a siti web) alle ubicazioni di origine e alle scorte disponibili. Un titolo può essere associato a più canali di vendita, ma un canale di vendita può essere assegnato a un solo titolo.

[!UICONTROL **Quantità vendibile aggregata**] è l&#39;inventario virtuale totale che può essere venduto tramite un canale di vendita. L&#39;importo viene calcolato in tutte le origini assegnate a una scorta.

[!UICONTROL **Prenotazioni**] traccia le detrazioni dalla quantità vendibile quando i clienti aggiungono prodotti ai carrelli e completano il pagamento. Quando un ordine viene spedito, la prenotazione cancella e deduce gli importi spediti dalle quantità di magazzino di origine specifiche.
