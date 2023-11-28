---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL General] &gt; [!UICONTROL Currency Setup] pagina dell’amministratore di Commerce.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 2%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Consulta [Configurazione della valuta](../../stores-purchase/currency-configuration.md) per ulteriori dettagli su queste configurazioni.

## [!UICONTROL Currency Options]

![Divisa Imposta > Opzioni divisa](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Sito Web | La valuta principale utilizzata per tutte le transazioni di pagamento online. Per più viste punto vendita, l&#39;ambito del prezzo deve essere impostato nel [Catalogo](../catalog/catalog.md) configurazione. |
| [!UICONTROL Default Display Currency] | Visualizzazione store | Valuta principale utilizzata per visualizzare i prezzi. |
| [!UICONTROL Allowed Currencies] | Visualizzazione store | Le valute accettate dal tuo negozio per il pagamento. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>A partire dalla versione 2.4.6 di, le [[!DNL Fixer.io]](https://fixer.io/) il servizio è obsoleto e sostituito con il [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) servizio. Si consiglia vivamente di utilizzare un account APILayer invece di un account obsoleto [!DNL Fixer.io] account.

![Valuta Imposta > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL API key] | Globale | Chiave utilizzata per accedere al servizio di conversione tramite [!DNL fixer.io] account. Per ulteriori informazioni, consulta [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | Globale | Determina il numero di secondi di inattività prima del timeout di una sessione Fixer.io. Valore predefinito: `100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixer Api (APILayer)]

![Valuta Imposta > Api fisso (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL API key] | Globale | Chiave utilizzata per accedere al servizio di conversione tramite [!DNL APILayer] account. Per ulteriori informazioni, consulta [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Globale | Determina il numero di secondi di inattività prima di un [!DNL APILayer] sessione scaduta. Il valore predefinito è `100`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Currency Converter API]

![Impostazione valuta > API Convertitore valuta](./assets/currency-setup-converter.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL API key] | Globale | Chiave utilizzata per accedere al servizio di conversione. Per ulteriori informazioni, consulta [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Globale | Determina il numero di secondi di inattività prima di un [!DNL Currency Converter] sessione scaduta. Valore predefinito:`100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Scheduled Import Settings]

![Valuta Imposta > Impostazioni importazione programmate](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Visualizzazione store | Determina se l&#39;importazione programmata è abilitata per i tassi di valuta. Opzioni: `Yes` / `No` |
| [!UICONTROL Service] | Visualizzazione store | Specifica il servizio che fornisce i dati per l&#39;importazione pianificata. Il valore predefinito è `fixer.io` |
| [!UICONTROL Start Time] | Visualizzazione store | Indica l&#39;ora di inizio per ora, minuto e secondo, in base a un orologio da 24 ore. |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui viene eseguita l&#39;importazione pianificata. Opzioni: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Visualizzazione store | Identifica l’indirizzo e-mail di ogni persona a cui viene inviata una notifica tramite e-mail relativa a errori di importazione pianificati. Per più destinatari, separa ogni voce con una virgola. |
| [!UICONTROL Error Email Sender] | Sito Web | Identifica il contatto del punto vendita che viene visualizzato come mittente della notifica e-mail di errore. Mittente predefinito: `General Contact` |
| [!UICONTROL Error Email Template] | Sito Web | Specifica il modello utilizzato come base per la notifica e-mail di errore. Modello predefinito: `Currency Update Warnings` |

{:style=&quot;table-layout:auto&quot;}
