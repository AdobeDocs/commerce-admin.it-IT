---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] pagina dell’amministratore di Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Queste impostazioni sono disponibili quando [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) è installato.

![Impostazioni Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Ambito](../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Globale | Opzioni:<br/><br/>**`Once Daily`**: seleziona questa opzione per cancellare la cronologia delle attività del tuo Negozio una volta al giorno.<br/><br/>**`Once Weekly`**: seleziona questa opzione per cancellare la cronologia delle attività del Negozio una volta alla settimana.<br/><br/>**`Once Monthly`**: (Impostazione predefinita) seleziona questa opzione per cancellare la cronologia delle attività del tuo Negozio una volta al mese. |
| [!UICONTROL Background Tasks (CRON) Source] | Globale | Seleziona `Magento CRON` per specificare che [!DNL Amazon Sales Channel] utilizza le impostazioni Commerce cron per determinare gli intervalli di comunicazione e sincronizzazione dei dati con Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Globale | Seleziona `Enabled` per raccogliere dati di sincronizzazione aggiuntivi quando è necessaria la risoluzione dei problemi.<br/><br/>Questa opzione è disabilitata per impostazione predefinita e deve essere abilitata solo quando necessario per la risoluzione dei problemi, in quanto la registrazione continua influisce negativamente sulle prestazioni. Se questa opzione è abilitata per la risoluzione dei problemi, deve essere disabilitata al termine.<br/><br/>**_Nota _**: la registrazione del Sales Channel Amazon viene scritta in `/var/log/channel_amazon.log` e possono essere visualizzati in [modalità sviluppatore](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Globale | Seleziona `Enabled` per bloccare tutte le richieste API in uscita che cambiano lo stato. Le modifiche potenziali vengono salvate ma non inviate finché non viene disattivata la modalità di sola lettura. Per avviare nuovamente i trasferimenti di dati, seleziona `Disabled`.<br/><br/>Quando si esegue la migrazione di un database a una nuova copia dell’istanza (rilevata quando l’URL di un archivio cambia nella configurazione), viene abilitata automaticamente la modalità di sola lettura.<br/><br/>È progettato per essere utilizzato su copie dell’istanza di produzione, come _Staging_ o _QA_, e non devono essere utilizzati nell’istanza di produzione.<br/><br/>**_Nota _**: la cache di configurazione deve essere cancellata per [!UICONTROL Read-Only Mode] per attivare. |

{style="table-layout:auto"}
