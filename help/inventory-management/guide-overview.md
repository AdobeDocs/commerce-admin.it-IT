---
title: "Guida di Inventory management [!DNL Inventory Management] Guida"
description: Informazioni complete su [!DNL Inventory Management] per gli amministratori di Adobe Commerce e di Magento Open Source, incluse le attività di migrazione e configurazione.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# [!DNL Inventory Management] Panoramica della guida

Questa guida è destinata agli amministratori di Adobe Commerce e Magento Open Source. Fornisce informazioni dettagliate sull’abilitazione di questo modulo, inclusa la configurazione e la gestione delle sue funzioni. È necessario conoscere le nozioni di base [!DNL Commerce] configurazione e funzionalità.

[!DNL Inventory Management] dispone di due aree per gli amministratori:

- Amministratore: utilizza quest’area per accedere all’interfaccia utente di configurazione e ai rapporti.
- Interfaccia della riga di comando: utilizzare questo strumento per eseguire attività di installazione e di configurazione back-end.

Questa guida tratta i seguenti argomenti:

| Oggetto | Descrizione |
| ------- | ----------- |
| [Introduzione](introduction.md) | Panoramica di [!DNL Inventory Management] funzionalità che è possibile utilizzare per gestire le scorte in più posizioni in modo che l’archivio Commerce rifletta accuratamente l’inventario fisico. |
| [Note sulla versione](release-notes.md) | Consulta le note sulla versione per informazioni su tutte [!DNL Inventory Management] versioni. |
| Nozioni di base sull’inventario | Scopri le nozioni di base sulla gestione dell’inventario: [Scorte e fonti](sources-stocks.md), [selezione origine e prenotazioni](selection-reservations.md), [stato ordine e prenotazione](order-status.md), e [tipi di prodotto](product-types.md) |
| Introduzione | Scopri di più su [!DNL Inventory Management] e come si inserisce nell’istanza Commerce e nelle operazioni di archiviazione: [Aggiornamenti di Commerce](migrate.md), [installazione e aggiornamento dei moduli](install-update.md), [tipi di origini esercente](merchant-sourcing.md), e [modifiche alla struttura di sourcing](expand-restructure.md) |
| [Configurazione](configuration.md) | Scopri la configurazione di [!DNL Inventory Management] opzioni che determinano la disponibilità dell&#39;origine, i prodotti di vetrina e la spedizione dell&#39;ordine. |
| [Gestire le origini](sources-manage.md) | Scopri le origini e come definiscono le ubicazioni fisiche in cui viene gestito e spedito l’inventario dei prodotti per l’evasione degli ordini o dove sono disponibili i servizi. |
| [Gestisci scorte](stocks-manage.md) | Scopri come le scorte vengono utilizzate per rappresentare un inventario virtuale e aggregato dei prodotti per le origini dei canali di vendita. |
| [Gestione quantità](quantities-manage.md) | Scopri come assegnare origini e quantità per nuovi prodotti o modificare prodotti esistenti. |
| [Gestione di ordini e spedizioni](shipments.md) | Ulteriori informazioni sulle opzioni aggiuntive [!DNL Inventory Management] caratteristiche e opzioni per la gestione delle quantità di magazzino mediante il processo di spedizione. |
| [Riferimento CLI](cli.md) | Scopri i comandi forniti da [!DNL Inventory Management] per gestire i dati di inventario e le impostazioni di configurazione. |

{style="table-layout:auto"}

## Informazioni per sviluppatori

Consulta [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) nella documentazione per gli sviluppatori di, per informazioni dettagliate sull’architettura dei moduli, le API e la personalizzazione degli algoritmi.

## Documentazione di Commerce

{{docs-links}}

## Risoluzione dei problemi e supporto

Se hai bisogno di informazioni o hai domande che non sono trattate in questa guida, utilizza le risorse seguenti:

- [Numero elevato di incoerenze nella prenotazione](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Problemi di incoerenza dell’inventario](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [L&#39;inventario dei campioni non barrati raggiunge &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Lo stato delle scorte non è corretto dopo l&#39;installazione del magazzino](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Ticket di supporto](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)- Inviate un ticket per ricevere ulteriore aiuto.
