---
title: '[!DNL Google Content Experiments]'
description: Scopri come utilizzare  [!DNL Google Content Experiments] per impostare un test A/B di prodotti, categorie o pagine di contenuti Commerce.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

L’esempio seguente mostra come impostare un test A/B di prodotti, categorie o pagine di contenuto utilizzando Esperimenti di contenuto Google Analytics. È consigliabile mantenere aperte due schede del browser mentre si lavora attraverso le istruzioni, perché è necessario eseguire un salto avanti e indietro tra l&#39;amministratore di Commerce e l&#39;account [!DNL Google Analytics].

>[!NOTE]
>
>[!DNL Google Content Experiments] è stato dichiarato obsoleto ed è stata pianificata la sostituzione con [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Passaggio 1: Abilita esperimenti di contenuto (Commerce)

1. Accedi all’amministratore dell’installazione di Commerce.

1. Segui le istruzioni per abilitare [Google Analytics](google-analytics.md) con Content Experiments nella configurazione di Commerce.

   ![Configurazione vendite - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Passaggio 2: Impostare le varianti (Commerce)

Crea più varianti dello stesso prodotto, categoria o pagina.

- Ogni variante deve avere una [chiave URL](../catalog/catalog-urls.md) univoca.
- Ogni variante deve avere la stessa [visualizzazione archivio](../getting-started/websites-stores-views.md#scope-settings) selezionata.

Puoi creare fino a dieci varianti di ogni entità da testare. Per i prodotti, utilizza [Salva e duplica](../catalog/product-workspace.md) per risparmiare tempo.

## Passaggio 3: Configurare l’esperimento (Google)

>[!NOTE]
>
>Per creare un esperimento devi disporre delle autorizzazioni appropriate per l’account Google.

1. Apri un&#39;altra scheda del browser e accedi al tuo account [Google Analytics][2].

   Se necessario, passare a **[!UICONTROL Account]** e **[!UICONTROL Property]**.

1. Nella barra laterale a sinistra, scegliere **[!UICONTROL Admin]** e utilizzare uno dei metodi seguenti:

   **Metodo 1:** Scegliere una visualizzazione esistente

   Nell&#39;intestazione della colonna _[!UICONTROL View]_&#x200B;fare clic sulla freccia giù e scegliere la visualizzazione che fornirà i dati per l&#39;esperimento.

   **Metodo 2:** Creare una nuova visualizzazione di report

   - Nell&#39;intestazione della colonna _Visualizza_ fare clic su **[!UICONTROL Create View]** ed eseguire le operazioni seguenti:

      - Identificare il percorso dell&#39;esperimento come `Website` o `Mobile app`.

      - Immettere un **[!UICONTROL Reporting View Name]** descrittivo.

      - Specificare **[!UICONTROL Reporting Time Zone]**.

   - Al termine, fare clic su **[!UICONTROL Create View]** e quindi sulla freccia indietro per tornare alla pagina precedente.

1. Nel pannello a sinistra in _[!UICONTROL Reports]_, scegli **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Fare clic su **[!UICONTROL Create experiment]** ed effettuare le seguenti operazioni:

   - Specifica la percentuale di traffico da reindirizzare.

   - Specificare **[!UICONTROL Original Page URL]** e gli URL di ogni **[!UICONTROL page variation]** che si desidera verificare.

   - Completa le altre opzioni.

1. Una volta configurato l&#39;esperimento, fare clic su **[!UICONTROL Manually Insert the Code]** e copiare il frammento di codice.

## Passaggio 4: Incolla snippet di codice (Commerce)

1. Torna all’amministratore dell’installazione di Commerce e apri la versione originale del prodotto, della categoria o della pagina in modalità di modifica.

1. Espandere la sezione **[!UICONTROL View Optimization]** per il prodotto, la categoria o la pagina.

1. Incollare il frammento di codice copiato dalle Google Analytics nella casella di testo **[!UICONTROL Experiment Code]**.

   >[!NOTE]
   >
   >Non incollare il frammento di codice in nessuna delle varianti.

   ![Ottimizzazione visualizzazione prodotto](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Passaggio 5: rivedere e avviare l’esperimento (Google)

1. Torna all&#39;account [Google Analytics][2].

1. Controlla le impostazioni dell’esperimento.

1. Se si è pronti per iniziare, fare clic su **[!UICONTROL Start Experiment]**.

   In caso contrario, fare clic su **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
