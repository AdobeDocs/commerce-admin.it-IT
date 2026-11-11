---
title: Listino prezzi
description: Scopri come i listini prezzi vengono mappati dai dati di catalogo e determinazione prezzi in [!DNL Adobe Commerce].
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo alle istanze Adobe Commerce as a Cloud Service con provisioning CCDM (infrastruttura SaaS gestita da Adobe)."
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# Listino prezzi

I listini prezzi definiscono i prezzi dei prodotti per un&#39;origine catalogo per i diversi livelli cliente e mercati. Supportano una gerarchia di listini prezzi padre e figlio.

![Gerarchia listino prezzi](../assets/price-book-hier.png)

## Concetti chiave

| Termine | Descrizione |
| ------ | ------------- |
| **Listino prezzi** | Raggruppamento logico che definisce i prezzi per un’origine di catalogo, ad esempio area geografica specifica o livello cliente, e viene utilizzato per gestire i prezzi dei prodotti. |
| **Fallback listino prezzi** | Il listino prezzi più alto di una gerarchia. Non ha alcun padre ed è il listino prezzi *only* che definisce la valuta per se stesso e per tutti i listini prezzi discendenti.<br/><br/>Se durante la creazione del listino prezzi non è stato definito alcun padre tramite l&#39;API, viene creato un nuovo listino prezzi di fallback. |
| **Listino prezzi principale** | Un listino prezzi di livello superiore da cui un listino prezzi dedicato figlio può ereditare i prezzi se non sono impostati in modo esplicito nel figlio. |
| **Profondità gerarchia** | Massimo di tre livelli (Fallback -> Figlio -> Nipote)<br/><br/>non applicato al momento dell&#39;acquisizione. |
| **Valuta** | Definito solo per il listino prezzi di riserva. Ereditato da tutti i libri prezzi per bambini.<br/><br/>Se non viene specificata la valuta durante la creazione del listino prezzi di fallback (tramite l&#39;API), la valuta viene impostata automaticamente su USD. |
| **Prezzo del prodotto** | Il prezzo specifico assegnato a un prodotto (SKU) all’interno di un particolare listino prezzi. |
| **Sconti** | Gli sconti sono definiti nel prezzo del prodotto. Non ereditato. |

## Implementazione del listino prezzi dedicato

Quando si utilizza Adobe Commerce as a Cloud Service con Composable Catalog Data Model (CCDM), i listini prezzi vengono mappati dai dati di catalogo e di determinazione prezzi. Non vengono create manualmente.

Ad alto livello, la mappatura è:

- **Visualizzazione archivio → origine catalogo**: i dati di prodotto della visualizzazione archivio, inclusi gli attributi localizzati, vengono mappati su un&#39;origine catalogo.
- **Sito Web → Listino prezzi o listino prezzi dedicato**—La determinazione prezzi del sito Web viene mappata sul listino prezzi dedicato o sui listini prezzi dedicato.
- **Inserimenti nel listino prezzi del gruppo di clienti → Inserimenti nel listino prezzi**: i dati di determinazione prezzi del gruppo di clienti vengono mappati ai dati di determinazione prezzi pertinenti.

Gestisci la configurazione del catalogo di origine, del sito Web e della determinazione prezzi nella configurazione di Adobe Commerce, quindi assegna i listini prezzi mappati nella vista del catalogo pertinente configurando i listini prezzi disponibili. Se non viene assegnato alcun listino prezzi, nella vista catalogo viene utilizzato il listino prezzi predefinito.

Una vista catalogo utilizza la configurazione dei listini prezzi disponibile con i relativi dati e criteri di catalogo per determinare l&#39;esperienza di merchandising, inclusi i prezzi restituiti per i prodotti.

>[!NOTE]
>
>Per Commerce B2B, il sistema crea e assegna un singolo listino prezzi dedicato a ogni vista di catalogo in base alla configurazione del catalogo condiviso. Non è necessario configurare la disponibilità del listino prezzi dedicato per queste visualizzazioni.

## Prezzi di pagamento

I listini prezzi supportano l&#39;esperienza di cataloghi di merchandising e vetrine. Commerce Core continua a gestire il carrello e il pagamento. Un prezzo disponibile solo in CCDM non diventa automaticamente il prezzo utilizzato dal pagamento.

Mantenere i prezzi coerenti con la configurazione Commerce Core e verificare i prezzi visualizzati, i componenti aggiuntivi al carrello, le promozioni e il pagamento come parte della convalida dell&#39;implementazione.

## Visualizza listini prezzi

Al termine della sincronizzazione dei dati del catalogo, visualizzare i listini prezzi disponibili e i relativi ID nell&#39;area di lavoro **[!UICONTROL Catalog views]**.

1. Vai a _Configurazione archivio_ e fai clic su **[!UICONTROL Catalog views]**.

1. Fare clic su **[!UICONTROL Create catalog view]**.

1. Esaminare i listini prezzi disponibili nella sezione **[!UICONTROL Price Books]** della configurazione della vista catalogo.

   ![Nomi e ID listino prezzi](../assets/price-book-name-ids.png)

## Configura disponibilità listino prezzi dedicato

Associa i listini prezzi mappati alle viste catalogo configurando i listini prezzi disponibili nell’area di lavoro Visualizzazioni catalogo in Amministrazione Commerce.

>[!NOTE]
>
>Una visualizzazione del catalogo privato (con [!UICONTROL Catalog Protection] abilitato) può fare riferimento a un solo listino prezzi dedicato.

1. Dall&#39;area di lavoro **[!UICONTROL Catalog views]**, selezionare la visualizzazione del catalogo da configurare.

1. Nella sezione **[!UICONTROL Price Books]** selezionare i listini prezzi disponibili per i negozi supportati dalla visualizzazione catalogo.
