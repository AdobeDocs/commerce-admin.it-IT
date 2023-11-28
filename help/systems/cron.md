---
title: Cron (attività pianificate)
description: Scopri come controllare l’esecuzione e la pianificazione dei processi cron di Commerce dall’amministratore.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Cron (attività pianificate)

Adobe Commerce e Magento Open Source eseguono alcune operazioni in base alla pianificazione eseguendo periodicamente uno script. Puoi controllare l’esecuzione e la pianificazione dei processi di Commerce cron dall’amministratore. Le operazioni di archiviazione eseguite in base a una pianificazione cron includono, tra l’altro:

- [E-mail](email-communications.md)
- [Regole prezzo catalogo](../merchandising-promotions/price-rules-catalog.md)
- [Newsletter](../merchandising-promotions/newsletters.md)
- [Generazione mappa del sito XML](../merchandising-promotions/sitemap-xml.md)
- [Aggiornamenti dei tassi di cambio](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce Services deve essere installato in crontab per garantire che i componenti core e alcune estensioni di terze parti funzionino come previsto. Consulta la [istruzioni in _Guida all’installazione_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) per informazioni dettagliate sull&#39;installazione dei servizi in crontab.

Inoltre, puoi configurare quanto segue in modo che venga eseguito in base a una pianificazione cron:

- Aggiornamenti alla griglia di Order System e reindicizzazione
- Durata pagamento in sospeso

Assicurati che il [URL di base](../stores-purchase/store-urls.md) per l’archivio sono impostati correttamente in modo che gli URL generati durante le operazioni cron siano corretti. Per l’infrastruttura cloud di Adobe Commerce, consulta [Imposta processi cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) nel _Guida di Commerce su infrastruttura cloud_. Per on-premise, consulta [Configurare ed eseguire con](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) nel _Guida alla configurazione_.

## Configura cron

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Cron]** sezione.

   ![Configurazione avanzata - attività cron](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Completa le seguenti impostazioni per **[!UICONTROL Index]** e **[!UICONTROL Default]** gruppi.

   Le impostazioni sono le stesse in ogni sezione.

   - **[!UICONTROL Generate Schedules Every]** - Definisce la frequenza di generazione della pianificazione (in minuti). Le pianificazioni vengono memorizzate nel database.
   - **[!UICONTROL Schedule Ahead for]** - Definisce l&#39;anticipo di pianificazione dei processi cron (in minuti). Ad esempio, se questa impostazione è impostata su `10` e il cron viene eseguito, i processi cron vengono pianificati per i successivi 10 minuti.
   - **[!UICONTROL Missed if not Run Within]** - Definisce il tempo (in minuti) utilizzato per determinare un lavoro saltato. Se il processo cron non viene eseguito all&#39;ora pianificata e il tempo specificato è trascorso, non è possibile eseguirlo e lo stato è impostato su `Missed`.
   - **[!UICONTROL History Cleanup Every]** - Definisce il tempo (in minuti) per la cancellazione della cronologia delle attività terminate dal database.
   - **[!UICONTROL Success History Lifetime]** - Definisce la durata (in minuti) della cronologia dei processi cron con un `Successful` Lo stato rimane nel database.
   - **[!UICONTROL Failure History Lifetime]** - Definisce la durata (in minuti) della cronologia dei processi cron con un `Error` Lo stato rimane nel database.
   - **[!UICONTROL Use Separate Process]** - Definisce se tutti gli OdL cron del gruppo vengono eseguiti in un processo di sistema separato. Opzioni: `Yes` / `No`

   ![Configurazione avanzata - Indice gruppo cron](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
