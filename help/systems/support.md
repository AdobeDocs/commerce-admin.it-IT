---
title: Strumenti di supporto
description: Scopri gli strumenti di supporto forniti che puoi utilizzare per identificare i problemi nel sistema.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/bS1CIJI9ZXybrYA-EgekVKjXQhywA6jdpWOM-bvw4Mc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 0%

---

# Strumenti di supporto

{{ee-feature}}

Gli strumenti di supporto sono progettati per identificare i problemi noti nel sistema. Possono essere utilizzati come risorsa durante i processi di sviluppo e ottimizzazione e come strumento diagnostico per aiutare il nostro team di supporto a identificare e risolvere i problemi.

## Rapporti di sistema

Lo strumento di reporting di sistema consente di acquisire istantanee periodiche complete o parziali del sistema e di salvarle per riferimento futuro. Puoi confrontare le impostazioni delle prestazioni prima e dopo i cicli di sviluppo del codice o le modifiche alle impostazioni del server. Lo strumento di reporting di sistema può ridurre notevolmente il tempo impiegato per preparare e inviare le informazioni richieste dal Supporto per avviare un&#39;indagine.

Dalla griglia Rapporti di sistema è possibile visualizzare e scaricare i rapporti esistenti, eliminarli e crearli.

### Accedere ai report di sistema

Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Amministratore - Report di sistema](./assets/reports.png){width="600" zoomable="yes"}

### Generare un rapporto

1. Fare clic su **[!UICONTROL New Report]**.

1. Nell&#39;elenco **[!UICONTROL Groups]** selezionare ogni set di informazioni che si desidera includere nel report. Per impostazione predefinita, sono selezionati tutti i gruppi.

   ![Report di sistema - selezionare i gruppi](./assets/report-create.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Create]**.

   La generazione del rapporto potrebbe richiedere alcuni minuti, a seconda del numero di tipi di rapporto selezionati. Quando il report è pronto, viene visualizzato nella parte superiore della griglia con la data e l’ora generate.

### Visualizza informazioni modulo

Sono disponibili informazioni utili sui moduli installati.

**_Per visualizzare le informazioni del report per ciascun modulo installato:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Fare clic su **[!UICONTROL New Report]**.
1. Selezionare `Modules` dall&#39;elenco **[!UICONTROL Groups]**.
1. Fare clic su **[!UICONTROL Create]**.
1. Dopo la generazione del report, fare clic su **[!UICONTROL Select]** e quindi su **[!UICONTROL View]** per visualizzare tutte le versioni del modulo.
1. Fare clic su **[!UICONTROL Download]** per scaricare il report.

### Gestire i report di sistema

Nella colonna **[!UICONTROL Action]** della griglia selezionare una delle opzioni seguenti:

- `View` - Utilizzare questa funzione per visualizzare i dettagli del report.
- `Delete` - Utilizzare questa funzione per eliminare il report generato dall&#39;elenco.
- `Download` - Utilizzare questa funzione per salvare il report come file HTML.

### Visualizza dettagli report di sistema

1. Per il report necessario, selezionare **[!UICONTROL View]** nella colonna _[!UICONTROL Actions]_.

1. Nel pannello a sinistra, espandi ![Il selettore di espansione](../assets/icon-display-expand.png) in ogni sezione del rapporto per visualizzare i dettagli.

   ![Informazioni generali sul report di sistema](./assets/report-information.png){width="600" zoomable="yes"}

### Report di sistema disponibili

| Gruppo di rapporti | Informazioni incluse |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce Version<br>Data Count<br>Cache Status<br>Index Status |
| [!UICONTROL Environment] | Informazioni ambiente<br>Stato MySQL |
| [!UICONTROL Data] | Duplica Categorie Per Chiave URL<br>Duplica Prodotti Per Chiave URL<br>Duplica Prodotti Per SKU<br>Duplica Ordini Per Id Incremento<br>Duplica Utenti Per E-Mail<br>Dati Categorie Danneggiati |
| [!UICONTROL Modules] | Elenco Moduli Personalizzati<br>Elenco Moduli Disabilitati<br>Elenco Tutti I Moduli |
| [!UICONTROL Configuration] | Configurazione<br>Dati da `app/etc/env.php`<br>Metodi di spedizione<br>Metodi di pagamento<br>Matrice funzionalità pagamenti |
| [!UICONTROL Logs] | File di registro<br>Messaggi di sistema principali<br>Messaggi di sistema principali di oggi<br>Messaggi di debug principali<br>Messaggi di debug principali di oggi<br>Messaggi di eccezione principali<br>Messaggi di eccezione principali di oggi |
| [!UICONTROL Attributes] | Attributi EAV definiti dall&#39;utente<br>Nuovi attributi EAV<br>Tipi di entità<br>Tutti gli attributi EAV<br>Attributi EAV della categoria<br>Attributi EAV del prodotto<br>Attributi EAV del cliente<br>Attributo EAV dell&#39;indirizzo del cliente<br>Attributi EAV dell&#39;elemento RMA |
| [!UICONTROL Events] | Eventi globali personalizzati<br>Eventi amministrativi personalizzati<br>Eventi front-end personalizzati<br>Eventi doc personalizzati<br>Eventi Crontab personalizzati<br>Eventi REST personalizzati<br>Eventi SOAP personalizzati<br>Eventi globali core<br>Eventi front-end core<br>Eventi front-end core<br>Eventi doc core<br>Eventi Crontab core<br>Eventi REST core<br>Eventi SOAP core<br>Tutti gli eventi globali<br>Tutti gli eventi amministrativi<br>Tutti gli eventi front-end<br>Tutti gli eventi REST<br>Tutti gli eventi SOAP Eventi<br>Tutti gli eventi Crontab<br> |
| [!UICONTROL Cron] | Pianificazioni Cron per codice di stato<br>Pianificazioni Cron per codice processo<br>Errori nella coda Pianificazioni Cron<br>Elenco Pianificazioni Cron<br>Processi Cron globali personalizzati<br>Processi Cron configurabili personalizzati<br>Processi Cron globali core<br>Processi Cron configurabili core<br>Tutti i processi Cron globali<br>Tutti i processi Cron configurabili |
| [!UICONTROL Design] | Elenco Temi Adminhtml<br>Elenco Temi Front-End |
| [!UICONTROL Stores] | Struttura sito Web<br>Elenco siti Web<br>Elenco archivi<br>Elenco visualizzazioni archivio |
| Connettore OMS <br>_(visibile con integrazione OMS)_ | Versione connettore<br>Monitoraggio connettore<br>Risultati elaborazione messaggio |

{style="table-layout:auto"}
