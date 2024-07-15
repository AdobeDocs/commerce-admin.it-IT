---
title: Ambito di configurazione
description: Scopri come impostare l’ambito per le impostazioni di configurazione in Amministrazione Commerce.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Ambito di configurazione

Il selettore della visualizzazione archivio nell’angolo in alto a sinistra di molte pagine di configurazione filtra la visualizzazione della pagina per un ambito specifico e imposta il valore di alcune entità utilizzate da Commerce. Elenca ogni livello della gerarchia per nome e viene utilizzato per modificare l&#39;ambito in un altro livello. Le impostazioni che rappresentano l&#39;ambito corrente sono disattivate, pertanto sono disponibili solo quelle che rappresentano l&#39;impostazione di ambito corrente. L&#39;ambito è inizialmente impostato su _Configurazione predefinita_. Per gli utenti amministratori con accesso limitato, l&#39;elenco delle visualizzazioni di archivio disponibili include solo quelle per le quali l&#39;utente dispone di [autorizzazione](../systems/permissions.md) di accesso.

| Livello | Descrizione |
|--- |--- |
| [!UICONTROL Default Config] | Configurazione di sistema predefinita. |
| [!UICONTROL Main Website] | Nome del sito Web nella parte superiore della gerarchia. |
| [!UICONTROL Main Website Store] | Nome dell&#39;archivio predefinito associato al sito Web padre. |
| [!UICONTROL Default Store View] | Nome della visualizzazione predefinita associata all&#39;archivio padre. |
| [!UICONTROL Stores Configuration] | Passa alla griglia Negozi e equivale a scegliere [!UICONTROL Stores] > [!UICONTROL All Stores] dalla barra laterale Amministratore. |

{style="table-layout:auto"}

![Caselle di controllo Usa valore di sistema selezionate](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

La casella di controllo _[!UICONTROL Use System Value]_a destra di molte impostazioni di configurazione viene utilizzata per applicare o sostituire il valore del campo predefinito nell&#39;ambito di configurazione corrente. Il valore del campo predefinito non può essere modificato quando la casella di controllo è selezionata. Per modificare il valore, deselezionare la casella di controllo e immettere il nuovo valore. Viene richiesto di confermare ogni volta che si modifica il valore di sistema.

L&#39;etichetta della casella di controllo cambia in base all&#39;ambito corrente e fa sempre riferimento al livello padre che è un passo avanti nella gerarchia dell&#39;ambito. Poiché il livello padre è un contenitore per tutti gli elementi al di sotto di tale livello, l&#39;impostazione dell&#39;ambito dal livello padre viene ereditata a meno che non venga sostituita.

## Opzioni valore predefinito

| Casella di controllo | Descrizione |
|--- |--- |
| [!UICONTROL Use system value] | Questa casella di controllo viene visualizzata quando l&#39;ambito di configurazione è impostato su `Default Config`. |
| [!UICONTROL Use Default] | Questa casella di controllo viene visualizzata quando l&#39;ambito di configurazione è impostato su Principale `Website` e fa riferimento all&#39;archivio predefinito assegnato al sito Web. |
| [!UICONTROL Use Website] | Questa casella di controllo viene visualizzata quando l&#39;ambito di configurazione è impostato su una visualizzazione archivio specifica. Se questa opzione è selezionata, viene utilizzata l&#39;impostazione del sito Web padre associata alla visualizzazione Store. In questo caso, il livello di store viene ignorato perché si applica all&#39;archivio predefinito associato al sito Web. |

{style="table-layout:auto"}

## Impostare l&#39;ambito

Prima di impostare una configurazione che si applica solo a una visualizzazione specifica del sito Web, dello store o dello store, effettuare le seguenti operazioni:

1. Nella barra laterale _Admin_ eseguire una delle operazioni seguenti:

   - Per la maggior parte delle impostazioni di configurazione, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Per [impostazioni relative alla progettazione](../content-design/configuration.md), passare a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Quindi nella griglia scegliere la visualizzazione del punto vendita applicabile.

1. Passare all&#39;impostazione di configurazione da modificare ed effettuare le seguenti operazioni:

   - Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** sulla visualizzazione specifica in cui si applica la configurazione. Quando viene richiesto di confermare il cambio di ambito, fare clic su **[!UICONTROL OK]**.

     Dopo ogni campo viene visualizzata una casella di controllo e potrebbero essere disponibili campi aggiuntivi.

   - Deselezionare la casella di controllo **[!UICONTROL Use system value]** dopo qualsiasi campo che si desidera modificare. Quindi, aggiorna il valore della vista.

   - Ripeti questo processo per ogni campo da aggiornare sulla pagina.

   ![Impostazione delle opzioni Paese della visualizzazione archivio francese](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Riferimento rapido ambito

| Ambito | Descrizione |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Amministratore | Tutti i siti Web, gli store e le visualizzazioni dello store presenti nell&#39;installazione vengono gestiti dallo stesso amministratore. |
| Configurazione predefinita | Le impostazioni di [configurazione predefinita](../getting-started/websites-stores-views.md#scope-settings) globali vengono utilizzate nella gerarchia dell&#39;archivio, a meno che non vengano ignorate a un livello inferiore. |
| Catalogo | Il termine _catalogo_ si riferisce al database di prodotti nel suo complesso ed è disponibile in tutta l&#39;installazione. |
| Prezzi dei prodotti | I prezzi dei prodotti possono essere configurati per l’applicazione a livello globale o a livello di sito web. |
| Configurazioni prodotto | Gli attributi utilizzati come opzioni di [prodotto configurabile](../catalog/product-create-configurable.md) devono avere un ambito globale. |
| Clienti | Gli account cliente possono essere configurati per l’applicazione a livello globale o a livello di sito web. Ogni sito Web può avere un set separato di [account cliente](../customers/customer-account-scope.md) o condividere gli account cliente con altri siti Web nell&#39;installazione. |
| **[!UICONTROL Website]** |  |
| Dominio | Ulteriori [siti Web](../stores-purchase/introduction.md#store-structure) possono essere impostati come sottodomini del dominio primario oppure avere indirizzi IP e domini dedicati separati. |
| Clienti | Gli account cliente possono essere configurati per l’applicazione a livello globale o a livello di sito web. Ogni sito Web può avere un set separato di [account cliente](../customers/customer-account-scope.md) o condividere gli account cliente con altri siti Web nell&#39;installazione. |
| Valuta | A ogni sito Web può essere assegnata una [valuta di base](../stores-purchase/currency-configuration.md) diversa. La valuta di base viene utilizzata per elaborare tutte le transazioni, anche se al cliente potrebbe apparire una valuta di visualizzazione diversa, in base alle impostazioni internazionali della visualizzazione archivio. |
| Prodotti | I singoli prodotti vengono assegnati alla gerarchia a livello di sito web. Nella griglia Prodotti sono elencati tutti i prodotti del catalogo e i siti Web in cui sono disponibili. L&#39;impostazione [Prodotto in siti Web](../catalog/settings-basic-websites.md) identifica ogni sito Web in cui il prodotto è disponibile. |
| Prezzi dei prodotti | [I prezzi dei prodotti](../catalog/catalog-price-scope.md) possono essere configurati per l&#39;applicazione a livello globale o a livello di sito Web. |
| Metodi di pagamento | [I metodi di pagamento](../stores-purchase/payments.md) sono configurati a livello di sito Web, anche se il titolo e le istruzioni possono essere configurati per ogni visualizzazione dello store. |
| Pagamento | Il [processo di estrazione](../stores-purchase/checkout-process.md) si svolge a livello di sito Web, anche se è possibile configurare alcune opzioni di visualizzazione per ogni visualizzazione dello store. Tutti gli archivi associati a un sito Web hanno la stessa [configurazione di estrazione](../stores-purchase/checkout-process.md#checkout-options). |
| Paesi consentiti | I paesi consentiti possono essere configurati a livello di sito web. Le impostazioni [paesi consentiti](../getting-started/store-details.md#country-options) vengono utilizzate nell&#39;estrazione per limitare la provenienza di un cliente. |
| **[!UICONTROL Store]** |  |
| Dominio | Con più archivi, ogni archivio può avere lo stesso dominio, un sottodominio o domini chiaramente diversi. Per ulteriori informazioni, vedere [Aggiunta di archivi](../stores-purchase/stores.md#add-stores). |
| Categoria principale | Ogni negozio può avere un set separato di prodotti e menu principale che si basa su una categoria &quot;root&quot; e sottocategorie. Ogni catalogo ha una [categoria principale](../catalog/category-root.md) assegnata a livello di archivio. |
| **[!UICONTROL Store View]** |  |
| Sottocategorie | Le [sottocategorie](../catalog/category-create.md#category-structure) che compongono il menu principale (sotto la radice) vengono assegnate a livello di visualizzazione archivio. |
| Lingua | A ogni visualizzazione dello store può essere assegnata una [lingua](../getting-started/store-details.md#locale-options) diversa. La valuta di visualizzazione, le unità di misura e l&#39;interfaccia di amministrazione sono specifiche della lingua. |
| Lingue | Per supportare più lingue, tutto il contenuto, incluse le descrizioni dei prodotti, deve essere [tradotto](../stores-purchase/store-localize.md#localize-products) per ogni visualizzazione dello store. |
| Visualizza valuta | È possibile utilizzare una [valuta di visualizzazione](../stores-purchase/currency-configuration.md) diversa per ogni visualizzazione dello store, anche se le transazioni vengono elaborate a livello di sito Web utilizzando la valuta di base. |

{style="table-layout:auto"}
