---
title: Cron (attività pianificate)
description: Scopri come controllare l’esecuzione e la pianificazione dei processi cron di Commerce dall’amministratore.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Cron (attività pianificate)

Adobe Commerce e Magento Open Source eseguono periodicamente uno script per eseguire alcune operazioni secondo la pianificazione. Puoi controllare l’esecuzione e la pianificazione dei processi cron di Commerce dall’amministratore. Le operazioni di archiviazione eseguite in base a una pianificazione cron includono, tra l’altro:

- [E-mail](email-communications.md)
- [Regole prezzo catalogo](../merchandising-promotions/price-rules-catalog.md)
- [Newsletter](../merchandising-promotions/newsletters.md)
- [Generazione mappa del sito XML](../merchandising-promotions/sitemap-xml.md)
- [Aggiornamenti dei tassi di cambio](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>I servizi Commerce devono essere installati in crontab per garantire che i componenti core e alcune estensioni di terze parti funzionino come previsto. Per informazioni dettagliate sull&#39;installazione dei servizi in crontab, vedere le [istruzioni nella _Guida all&#39;installazione_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=it).

Inoltre, puoi configurare quanto segue in modo che venga eseguito in base a una pianificazione cron:

- Aggiornamenti alla griglia di Order System e reindicizzazione
- Durata pagamento in sospeso

Verificare che gli [URL di base](../stores-purchase/store-urls.md) per l&#39;archivio siano impostati correttamente in modo che gli URL generati durante le operazioni cron siano corretti. Per Adobe Commerce su infrastruttura cloud, consulta [Configurare i processi cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html?lang=it) nella _Guida di Commerce su infrastruttura cloud_. Per informazioni on-premise, vedere [Configurare ed eseguire con](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=it) nella _Guida alla configurazione_.

## Configura cron

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Cron]**.

   ![Configurazione avanzata - attività cron](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Completare le impostazioni seguenti per i gruppi **[!UICONTROL Index]** e **[!UICONTROL Default]**.

   Le impostazioni sono le stesse in ogni sezione.

   - **[!UICONTROL Generate Schedules Every]** - Definisce la frequenza di generazione della pianificazione (in minuti). Le pianificazioni vengono memorizzate nel database.
   - **[!UICONTROL Schedule Ahead for]** - Definisce l&#39;anticipo di pianificazione dei processi cron (in minuti). Ad esempio, se questa impostazione è impostata su `10` e il cron viene eseguito, i processi cron verranno pianificati per i successivi 10 minuti.
   - **[!UICONTROL Missed if not Run Within]** - Definisce il tempo (in minuti) utilizzato per determinare un processo non eseguito. Se il processo cron non viene eseguito all&#39;ora pianificata e il tempo specificato è trascorso, non è possibile eseguirlo e lo stato è impostato su `Missed`.
   - **[!UICONTROL History Cleanup Every]** - Definisce il tempo (in minuti) per la cancellazione della cronologia delle attività terminate dal database.
   - **[!UICONTROL Success History Lifetime]** - Definisce il periodo di tempo (in minuti) in cui la cronologia dei processi cron con stato `Successful` rimane nel database.
   - **[!UICONTROL Failure History Lifetime]** - Definisce il periodo di tempo (in minuti) in cui la cronologia dei processi cron con stato `Error` rimane nel database.
   - **[!UICONTROL Use Separate Process]** - Definisce se tutti i processi cron del gruppo vengono eseguiti in un processo di sistema separato. Opzioni: `Yes` / `No`

   ![Configurazione avanzata - indice gruppo cron](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
