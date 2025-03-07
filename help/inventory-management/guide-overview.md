---
title: Guida di Inventory management [!DNL Inventory Management] Guida
description: Informazioni complete su [!DNL Inventory Management] per gli amministratori di Adobe Commerce e di Magento Open Source, incluse migrazione e configurazione.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Panoramica della guida di [!DNL Inventory Management]

Questa guida è destinata agli amministratori di Adobe Commerce e Magento Open Source. Fornisce informazioni dettagliate sull’abilitazione di questo modulo, inclusa la configurazione e la gestione delle sue funzioni. Si presuppone una conoscenza di base della configurazione e delle funzionalità di base di [!DNL Commerce].

[!DNL Inventory Management] dispone di due aree per gli amministratori:

- Amministratore: utilizza quest’area per accedere all’interfaccia utente di configurazione e ai rapporti.
- Interfaccia della riga di comando: utilizzare questo strumento per eseguire attività di installazione e di configurazione back-end.

Questa guida tratta i seguenti argomenti:

| Oggetto | Descrizione |
| ------- | ----------- |
| [Introduzione](introduction.md) | Panoramica delle funzionalità di [!DNL Inventory Management] che è possibile utilizzare per gestire le scorte in più posizioni in modo che l&#39;archivio Commerce rifletta accuratamente l&#39;inventario fisico. |
| [Note sulla versione](release-notes.md) | Consultare le note sulla versione per informazioni su tutte le [!DNL Inventory Management] versioni. |
| Nozioni di base sull’inventario | Scopri le nozioni di base sulla gestione dell’inventario: [Scorte e origini](sources-stocks.md), [selezione origine e prenotazioni](selection-reservations.md), [stato ordine e prenotazione](order-status.md) e [tipi di prodotto](product-types.md) |
| Introduzione | Scopri il modulo [!DNL Inventory Management] e come si inserisce nell&#39;istanza di Commerce e nelle operazioni di archiviazione: [Aggiornamenti di Commerce](migrate.md), [Installazione e aggiornamento del modulo](install-update.md), [Tipi di merchant sourcing](merchant-sourcing.md) e [Modifiche alla struttura di sourcing](expand-restructure.md) |
| [Configurazione](configuration.md) | Scopri la configurazione delle opzioni [!DNL Inventory Management] che determinano la disponibilità dell&#39;origine, i prodotti di vetrina e la spedizione dell&#39;ordine. |
| [Gestisci origini](sources-manage.md) | Scopri le origini e come definiscono le ubicazioni fisiche in cui viene gestito e spedito l’inventario dei prodotti per l’evasione degli ordini o dove sono disponibili i servizi. |
| [Gestisci scorte](stocks-manage.md) | Scopri come le scorte vengono utilizzate per rappresentare un inventario virtuale e aggregato dei prodotti per le origini dei canali di vendita. |
| [Gestione quantità](quantities-manage.md) | Scopri come assegnare origini e quantità per nuovi prodotti o modificare prodotti esistenti. |
| [Gestione di ordini e spedizioni](shipments.md) | Ulteriori informazioni sulle funzioni e sulle opzioni aggiuntive di [!DNL Inventory Management] per la gestione delle quantità di magazzino tramite il processo di spedizione. |
| [Riferimento CLI](cli.md) | Scopri i comandi forniti dal modulo [!DNL Inventory Management] per gestire i dati di inventario e le impostazioni di configurazione. |

{style="table-layout:auto"}

## Informazioni per sviluppatori

Per informazioni dettagliate sull&#39;architettura dei moduli, le API e la personalizzazione degli algoritmi, vedere [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) nella documentazione per gli sviluppatori.

## Documentazione di Commerce

{{docs-links}}

## Risoluzione dei problemi e supporto

Se hai bisogno di informazioni o hai domande che non sono trattate in questa guida, utilizza le risorse seguenti:

- [Stato scorte non corretto dopo l&#39;installazione del magazzino](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Ticket di supporto](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) - Invia un ticket per ricevere ulteriore assistenza.
