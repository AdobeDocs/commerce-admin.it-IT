---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales Channels] > [!UICONTROL Global Settings] dell'amministratore di Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Queste impostazioni sono disponibili quando [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) è installato.

![Impostazioni Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Globale | Opzioni:<br/><br/>**`Once Daily`**: selezionare questa opzione per cancellare la cronologia delle attività dello store una volta al giorno.<br/><br/>**`Once Weekly`**: Selezionare questa opzione per cancellare la cronologia delle attività dello store una volta alla settimana.<br/><br/>**`Once Monthly`**: (impostazione predefinita) Selezionare questa opzione per cancellare la cronologia delle attività dello store una volta al mese. |
| [!UICONTROL Background Tasks (CRON) Source] | Globale | Selezionare `Magento CRON` per specificare che [!DNL Amazon Sales Channel] utilizza le impostazioni cron di Commerce per determinare gli intervalli di sincronizzazione delle comunicazioni e dei dati con Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Globale | Selezionare `Enabled` per raccogliere ulteriori dati di sincronizzazione quando è necessaria la risoluzione dei problemi.<br/><br/>Questa opzione è disabilitata per impostazione predefinita e dovrebbe essere abilitata solo quando necessario per la risoluzione dei problemi, in quanto la registrazione continua influisce negativamente sulle prestazioni. Se questa opzione è abilitata per la risoluzione dei problemi, deve essere disabilitata al termine. |
| [!UICONTROL Read-Only Mode] | Globale | Selezionare `Enabled` per bloccare tutte le richieste API in uscita per la modifica dello stato. Le modifiche potenziali vengono salvate ma non inviate finché non viene disattivata la modalità di sola lettura. Per riavviare i trasferimenti di dati, selezionare `Disabled`.<br/><br/>Quando si esegue la migrazione di un database a una nuova copia dell&#39;istanza (rilevata quando l&#39;URL di un archivio cambia nella configurazione), viene attivata automaticamente la modalità di sola lettura.<br/><br/>Questo elemento è progettato per l&#39;utilizzo in copie dell&#39;istanza di produzione, come _Gestione temporanea_ o _Controllo qualità_, e non deve essere utilizzato nell&#39;istanza di produzione.<br/><br/>**_Nota _**: per l&#39;abilitazione di [!UICONTROL Read-Only Mode] è necessario cancellare la cache di configurazione. |

{style="table-layout:auto"}
