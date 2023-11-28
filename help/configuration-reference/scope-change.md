---
title: Ambito di configurazione
description: Scopri come impostare l’ambito per le impostazioni di configurazione in Commerce Admin.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: eb61d90c0a3bf5cac976fc8b79b23dc717aca3e6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Ambito di configurazione

Il selettore della visualizzazione archivio nell’angolo in alto a sinistra di molte pagine di configurazione filtra la visualizzazione della pagina per un ambito specifico e imposta il valore di alcune entità utilizzate da Commerce. Elenca ogni livello della gerarchia per nome e viene utilizzato per modificare l&#39;ambito in un altro livello. Le impostazioni che rappresentano l&#39;ambito corrente sono disattivate, pertanto sono disponibili solo quelle che rappresentano l&#39;impostazione di ambito corrente. L&#39;ambito è inizialmente impostato su _Configurazione predefinita_. Per gli utenti amministratori con accesso limitato, l’elenco delle visualizzazioni di store disponibili include solo quelle per le quali l’utente dispone di [autorizzazione](../systems/permissions.md) per accedere a.

| Livello | Descrizione |
|--- |--- |
| [!UICONTROL Default Config] | Configurazione di sistema predefinita. |
| [!UICONTROL Main Website] | Nome del sito Web nella parte superiore della gerarchia. |
| [!UICONTROL Main Website Store] | Nome dell&#39;archivio predefinito associato al sito Web padre. |
| [!UICONTROL Default Store View] | Nome della visualizzazione predefinita associata all&#39;archivio padre. |
| [!UICONTROL Stores Configuration] | Passa alla griglia Negozi ed è come scegliere [!UICONTROL Stores] > [!UICONTROL All Stores] dalla barra laterale Amministratore. |

{:style=&quot;table-layout:auto&quot;}

![Caselle di controllo Usa valore di sistema selezionate](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

Il _[!UICONTROL Use System Value]_la casella di controllo a destra di molte impostazioni di configurazione viene utilizzata per applicare o sostituire il valore del campo predefinito nell&#39;ambito di configurazione corrente. Il valore del campo predefinito non può essere modificato quando la casella di controllo è selezionata. Per modificare il valore, deselezionare la casella di controllo e immettere il nuovo valore. Viene richiesto di confermare ogni volta che si modifica il valore di sistema.

L&#39;etichetta della casella di controllo cambia in base all&#39;ambito corrente e fa sempre riferimento al livello padre che è un passo avanti nella gerarchia dell&#39;ambito. Poiché il livello padre è un contenitore per tutti gli elementi al di sotto di tale livello, l&#39;impostazione dell&#39;ambito dal livello padre viene ereditata a meno che non venga sostituita.

## Opzioni valore predefinito

| Casella di controllo | Descrizione |
|--- |--- |
| [!UICONTROL Use system value] | Questa casella di controllo viene visualizzata quando l&#39;ambito di configurazione è impostato su `Default Config`. |
| [!UICONTROL Use Default] | Questa casella di controllo viene visualizzata quando l&#39;ambito di configurazione è impostato su Principale `Website`, e si riferisce all’archivio predefinito assegnato al sito web. |
| [!UICONTROL Use Website] | Questa casella di controllo viene visualizzata quando l&#39;ambito di configurazione è impostato su una visualizzazione archivio specifica. Se questa opzione è selezionata, viene utilizzata l&#39;impostazione del sito Web padre associata alla visualizzazione Store. In questo caso, il livello di store viene ignorato perché si applica all&#39;archivio predefinito associato al sito Web. |

{:style=&quot;table-layout:auto&quot;}

## Impostare l&#39;ambito

Prima di impostare una configurazione che si applica solo a una visualizzazione specifica del sito Web, dello store o dello store, effettuare le seguenti operazioni:

1. Il giorno _Amministratore_ barra laterale, effettuare una delle seguenti operazioni:

   - Per la maggior parte delle impostazioni di configurazione, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Per [impostazioni relative alla progettazione](../content-design/configuration.md), vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Quindi nella griglia scegliere la visualizzazione del punto vendita applicabile.

1. Passare all&#39;impostazione di configurazione da modificare ed effettuare le seguenti operazioni:

   - Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** alla vista specifica in cui si applica la configurazione. Quando viene richiesto di confermare il cambio di ambito, fare clic su **[!UICONTROL OK]**.

     Dopo ogni campo viene visualizzata una casella di controllo e potrebbero essere disponibili campi aggiuntivi.

   - Cancella **[!UICONTROL Use system value]** dopo qualsiasi campo da modificare. Quindi, aggiorna il valore della vista.

   - Ripeti questo processo per ogni campo da aggiornare sulla pagina.

   ![Impostazione delle opzioni Paese della visualizzazione Store francese](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Riferimento rapido ambito

| Ambito | Descrizione |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Amministratore | Tutti i siti Web, gli store e le visualizzazioni dello store presenti nell&#39;installazione vengono gestiti dallo stesso amministratore. |
| Configurazione predefinita | Il modello [configurazione predefinita](../getting-started/websites-stores-views.md#scope-settings) Le impostazioni vengono utilizzate nella gerarchia dell&#39;archivio, a meno che non vengano ignorate a un livello inferiore. |
| Catalogo | Il termine _catalogo_ si riferisce al database dei prodotti nel suo complesso ed è disponibile in tutta l’installazione. |
| Prezzi dei prodotti | I prezzi dei prodotti possono essere configurati per l’applicazione a livello globale o a livello di sito web. |
| Configurazioni prodotto | Attributi utilizzati come [prodotto configurabile](../catalog/product-create-configurable.md) le opzioni devono avere un ambito globale. |
| Clienti | Gli account cliente possono essere configurati per l’applicazione a livello globale o a livello di sito web. Ogni sito web può avere un set separato di [account cliente](../customers/customer-account-scope.md) o condividere gli account dei clienti con altri siti Web nell&#39;installazione. |
| **[!UICONTROL Website]** |  |
| Dominio | Aggiuntivo [siti web](../stores-purchase/introduction.md#store-structure) possono essere impostati come sottodomini del dominio primario o avere indirizzi IP e domini dedicati separati. |
| Clienti | Gli account cliente possono essere configurati per l’applicazione a livello globale o a livello di sito web. Ogni sito web può avere un set separato di [account cliente](../customers/customer-account-scope.md) o condividere gli account dei clienti con altri siti Web nell&#39;installazione. |
| Valuta | A ogni sito web può essere assegnato un diverso [valuta di base](../stores-purchase/currency-configuration.md). La valuta di base viene utilizzata per elaborare tutte le transazioni, anche se al cliente potrebbe apparire una valuta di visualizzazione diversa, in base alle impostazioni internazionali della visualizzazione archivio. |
| Prodotti | I singoli prodotti vengono assegnati alla gerarchia a livello di sito web. Nella griglia Prodotti sono elencati tutti i prodotti del catalogo e i siti Web in cui sono disponibili. Il [Prodotto nei siti Web](../catalog/settings-basic-websites.md) L&#39;impostazione identifica ogni sito Web in cui il prodotto è disponibile. |
| Prezzi dei prodotti | [Prezzi dei prodotti](../catalog/catalog-price-scope.md) può essere configurato per l’applicazione a livello globale o a livello di sito web. |
| Metodi di pagamento | [Metodi di pagamento](../stores-purchase/payments.md) sono configurati a livello di sito web, anche se il titolo e le istruzioni possono essere configurati per ogni visualizzazione store. |
| Pagamento | Il [processo di pagamento](../stores-purchase/checkout-process.md) ha luogo a livello di sito web, anche se è possibile configurare alcune opzioni di visualizzazione per ogni visualizzazione store. Tutti i negozi associati a un sito Web hanno lo stesso [configurazione checkout](../stores-purchase/checkout-process.md#checkout-options). |
| Paesi consentiti | I paesi consentiti possono essere configurati a livello di sito web. Il [paesi consentiti](../getting-started/store-details.md#country-options) Le impostazioni vengono utilizzate durante l&#39;estrazione per limitare la provenienza del cliente. |
| **[!UICONTROL Store]** |  |
| Dominio | Con più archivi, ogni archivio può avere lo stesso dominio, un sottodominio o domini chiaramente diversi. Per ulteriori informazioni, consulta [Aggiunta di store](../stores-purchase/stores.md#add-stores). |
| Categoria principale | Ogni negozio può avere un set separato di prodotti e menu principale che si basa su una categoria &quot;root&quot; e sottocategorie. Ogni catalogo ha una [categoria principale](../catalog/category-root.md) che viene assegnato a livello di negozio. |
| **[!UICONTROL Store View]** |  |
| Sottocategorie | Il [sottocategorie](../catalog/category-create.md#category-structure) che costituiscono il menu principale (sotto la directory principale) vengono assegnati a livello di visualizzazione store. |
| Lingua | A ogni visualizzazione dello store può essere assegnata una diversa [lingua](../getting-started/store-details.md#locale-options). La valuta di visualizzazione, le unità di misura e l&#39;interfaccia di amministrazione sono specifiche della lingua. |
| Lingue | Per supportare più lingue, tutto il contenuto, incluse le descrizioni dei prodotti, deve essere [tradotto](../stores-purchase/store-localize.md#localize-products) per ogni visualizzazione store. |
| Visualizza valuta | Un altro [valuta di visualizzazione](../stores-purchase/currency-configuration.md) può essere utilizzato per ogni visualizzazione store, anche se le transazioni vengono elaborate a livello di sito Web utilizzando la valuta di base. |

{:style=&quot;table-layout:auto&quot;}
