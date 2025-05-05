---
title: Configurazione della valuta
description: Scopri come impostare l’ambito della valuta di base e come specificare le valute accettate e la valuta da utilizzare per la visualizzazione del prezzo.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Configurazione della valuta

Prima di impostare i singoli tassi di valuta, è necessario impostare l&#39;ambito della [valuta di base](../configuration-reference/general/currency-setup.md). Per impostazione predefinita, è impostata su globale. L&#39;impostazione della valuta di base viene applicata all&#39;intera [gerarchia archivio](../getting-started/websites-stores-views.md). Se si dispone di un&#39;installazione Adobe Commerce multisito o di Magento Open Source, è possibile gestire più valute di base impostando l&#39;ambito a livello di sito Web.

È inoltre possibile specificare le valute accettate e la valuta da utilizzare per la visualizzazione di [prezzi](../catalog/catalog-price-scope.md) nel punto vendita. Nel diagramma seguente, l&#39;ambito della valuta di base viene impostato a livello di sito Web, in modo che ogni sito Web possa avere una valuta di base diversa.

![Diagramma ambito valuta](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Passaggio 1: scegliere le divise accettate

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Scope]** sulla visualizzazione archivio in cui si applica la configurazione.

1. Nel pannello a sinistra in _Generale_, scegli **[!UICONTROL Currency Setup]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Currency Options]** e impostare le opzioni seguenti:

   - **[!UICONTROL Base Currency]** — Imposta sulla valuta principale utilizzata per le transazioni online.

   - **[!UICONTROL Default Display Currency]** — Imposta sulla valuta utilizzata per visualizzare i prezzi nella visualizzazione punto vendita.

   - **[!UICONTROL Allowed Currencies]** — Selezionare tutte le valute accettate come pagamento nella visualizzazione punto vendita. Assicurati anche di selezionare la valuta principale.

     Per più valute, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   ![Configurazione generale - Opzioni di valuta](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Opzioni valuta](../configuration-reference/general/currency-setup.md) nella _Guida di riferimento alla configurazione_.

1. Quando viene richiesto di aggiornare la cache, fare clic su _Chiudi_ ( ![Chiudi casella](../assets/icon-close-x.png) ) nell&#39;angolo superiore destro del messaggio di sistema.

   È possibile [aggiornare la cache](../systems/cache-management.md) in un secondo momento.

1. Definire l&#39;ambito della valuta di base:

   - Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

   - Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Price]**. (Questa sezione viene visualizzata solo se l&#39;ambito è impostato come **[!UICONTROL Store View:]** _Configurazione predefinita_.)

   - Imposta **[!UICONTROL Catalog Price Scope]** su `Global` o `Website`.

   ![Configurazione catalogo - opzioni prezzo](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Passaggio 2: configurare la connessione di importazione

1. Scorri fino alla parte superiore della pagina.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL Currency Setup]**.

1. Configurare la connessione al servizio valuta:

   Sono disponibili tre opzioni di servizio: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ e _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >A partire dalla versione 2.4.6, il servizio [[!DNL Fixer.io]](https://fixer.io/) è obsoleto e sostituito con il servizio [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Si consiglia di utilizzare un account APILayer invece di un account [!DNL Fixer.io] obsoleto.

   - _Per connettersi al servizio [fixer.io](https://fixer.io/):_

      - Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Fixer.io]**.

      - Immettere fixer.io **[!UICONTROL API key]**.

      - Per **[!UICONTROL Connection Timeout in Seconds]**, immettere il numero di secondi di inattività consentiti prima del timeout della connessione.

     ![Configurazione generale - Impostazione valuta - Opzioni Fixer.io](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Per connettersi al [[!DNL Fixer Api (APILayer)] servizio](https://apilayer.com/):_

      - Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Fixer Api (APILayer)]**.

      - Immetti [!DNL APILayer] **[!UICONTROL API key]**.

      - Per **[!UICONTROL Connection Timeout in Seconds]**, immettere il numero di secondi di inattività consentiti prima del timeout della connessione.

     ![Configurazione generale - Impostazione valuta - Opzioni API Fixer (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Per connettersi al [[!DNL Currency Convertor API] servizio](https://free.currencyconverterapi.com/):_

      - Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Currency Convertor API]**.

      - Immettere il convertitore di valuta **[!UICONTROL API key]**.

      - Per **[!UICONTROL Connection Timeout in Seconds]**, immettere il numero di secondi di inattività consentiti prima del timeout della connessione.

     ![Configurazione generale - Impostazione valuta - Opzioni API di Convertitore valuta](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Passaggio 3: configurare le impostazioni di importazione pianificate

1. Continuando con l&#39;installazione della valuta, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Scheduled Import Settings]**.

   ![Configurazione generale - impostazioni di importazione pianificate per la valuta](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Per aggiornare automaticamente i tassi di valuta, impostare **[!UICONTROL Enabled]** su `Yes`.

1. Impostare le opzioni di aggiornamento:

   - **[!UICONTROL Service]** — Imposta sul provider di tariffe. Il valore predefinito è `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** — Impostare su ora, minuto e secondo l&#39;aggiornamento delle tariffe in base alla pianificazione.

   - **[!UICONTROL Frequency]** — Per determinare la frequenza con cui vengono aggiornati i tassi, impostare una delle seguenti opzioni:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** — Immettere l&#39;indirizzo di posta elettronica della persona che deve ricevere la notifica e-mail se si verifica un errore durante il processo di importazione.

     Per immettere più indirizzi e-mail, separali con una virgola.

   - **[!UICONTROL Error Email Sender]** - Imposta il [contatto archivio](../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente della notifica di errore.

   - **[!UICONTROL Error Email Template]** — Imposta sul modello di messaggio di posta elettronica utilizzato per la notifica di errore.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic sul collegamento **[!UICONTROL Cache Management]** e aggiornare la cache non valida.

   ![Messaggio di sistema - aggiorna la cache non valida](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Passaggio 4: aggiornare i tassi di valuta

I tassi di cambio devono essere aggiornati con i valori correnti prima che diventino effettivi. [Aggiorna le tariffe](currency-update.md) manualmente o per importarle automaticamente.

## Passaggio 5: personalizzare i simboli di valuta (facoltativo)

La gestione dei simboli di valuta consente di personalizzare il simbolo associato a ciascuna valuta accettata come pagamento nel Negozio.

![Simboli di valuta](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Ogni valuta abilitata per l&#39;archivio viene visualizzata nell&#39;elenco _[!UICONTROL Currency]_.

1. Modificare le impostazioni nell&#39;elenco in base alle esigenze:

   - Immettere un simbolo personalizzato per ogni valuta che si desidera utilizzare oppure selezionare la casella di controllo **[!UICONTROL Use Standard]** per ogni valuta.

   - Per ignorare il simbolo predefinito, deselezionare la casella di controllo _[!UICONTROL Use Standard]_&#x200B;e immettere il simbolo che si desidera utilizzare.

   >[!NOTE]
   >
   >Non è possibile modificare l&#39;allineamento del simbolo di valuta da sinistra a destra.

1. Al termine, fare clic su **[!UICONTROL Save Currency Symbols]**.

1. Quando viene richiesto di aggiornare la cache, fare clic sul collegamento **[!UICONTROL Cache Management]** e aggiornare la cache non valida.
