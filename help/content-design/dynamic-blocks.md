---
title: Blocchi dinamici
description: Utilizza i blocchi dinamici per creare contenuti avanzati e interattivi basati su una logica basata sulle regole di prezzo e sui segmenti di clienti.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Blocchi dinamici

{{ee-feature}}

Creare contenuti avanzati e interattivi basati sulla logica da [regole di prezzo](../merchandising-promotions/introduction.md#price-rules) e [segmenti cliente](../customers/customer-segments.md). Esistente [blocchi dinamici](../page-builder/dynamic-block.md) può essere aggiunto direttamente al [!DNL Page Builder] [fase](../page-builder/workspace.md). Per un esempio dettagliato e dettagliato sull’utilizzo dei blocchi dinamici, consulta [Tutorial 2: blocchi](../page-builder/2-blocks.md).

>[!NOTE]
>
>Il _[!UICONTROL Banner]_opzione in [[!UICONTROL Content] menu](content-menu.md) è stato dichiarato obsoleto nella versione 2.3.1 e rimosso nella versione 2.4.0. La sua funzionalità è sostituita da Blocchi dinamici.

![[!DNL Page Builder] - blocco dinamico con regola di prezzo e segmento cliente](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Passaggio 1: creare un blocco dinamico

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Elenco blocchi dinamici](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Dynamic Block]**.

   ![Nuovo blocco dinamico](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Se applicabile, impostare **[!UICONTROL Store View]** a una visualizzazione store specifica in cui deve apparire il blocco dinamico.

1. Per attivare il blocco dinamico, impostare **[!UICONTROL Enable Dynamic Block]** a `Yes`.

1. Per riferimento interno, inserisci un valore descrittivo **[!UICONTROL Dynamic Block Name]**.

1. Imposta **[!UICONTROL Dynamic Block Type]** nell&#39;area della pagina in cui si desidera visualizzare il blocco dinamico e fare clic su **[!UICONTROL Done]**.

   ![Impostazione del tipo di blocco dinamico](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. In **[!UICONTROL Customer Segment]** , seleziona la casella di controllo di ciascun segmento che desideri visualizzare nel blocco dinamico e fai clic su **[!UICONTROL Done]** per salvare l&#39;impostazione.

   ![Scelta di un segmento di cliente](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Se non viene creato alcun segmento, il blocco dinamico è visibile a tutti.
   >- Se il cliente non appartiene ad alcun segmento e il blocco dinamico viene creato per tutti i segmenti, il contenuto del blocco dinamico viene comunque visualizzato.
   >- Se tutti i segmenti cliente assegnati a un blocco dinamico vengono eliminati, il relativo contenuto è visibile a tutti.

### Utilizzare i tipi di pubblico di Real-Time CDP in blocchi dinamici

Se [installato](../customers/audience-activation.md#install-the-extension) e [configurato](../customers/audience-activation.md#configure-the-extension) il [!DNL Audience Activation] estensione, viene visualizzata una sezione denominata **[!UICONTROL Audiences]**.

![Scegli un pubblico Real-Time CDP](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

In **[!UICONTROL Real-Time CDP Audience]** , seleziona la casella di controllo di ogni pubblico che desideri visualizzare il blocco dinamico e fai clic su **[!UICONTROL Done]** per salvare l&#39;impostazione.

## Passaggio 2: Completare il contenuto

Utilizza il [!DNL Page Builder] [workspace](../page-builder/workspace.md) per completare il contenuto.

![[!DNL Page Builder] - dynamic block workspace](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Passaggio 3: scegliere una promozione correlata

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Fare clic sul tipo di promozione che si desidera associare al blocco dinamico:

   - **[!UICONTROL Add Cart Price Rules]** (vedere [Regole prezzo carrello](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (vedere [Regole prezzo catalogo](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Le regole del prezzo del catalogo non sono supportate per i tipi di pubblico di Real-Time CDP.

1. Nell’elenco delle regole disponibili, seleziona la casella di controllo di ciascuna regola che desideri utilizzare e fai clic su **[!UICONTROL Add Selected]**.

1. Al termine del blocco dinamico, fai clic su **[!UICONTROL Save]**.

## Passaggio 4: aggiungere il blocco dinamico a una pagina

1. Apri la pagina in cui desideri visualizzare il blocco dinamico.

1. Utilizza il [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) tipo di contenuto per aggiungere il blocco dinamico all’area di visualizzazione.

## Descrizioni dei campi e degli strumenti

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Store View] | Specifica le visualizzazioni dello store in cui il blocco dinamico deve essere disponibile. |
| [!UICONTROL Enable Dynamic Block] | Attiva o disattiva il blocco dinamico. Opzioni: Sì / No |
| [!UICONTROL Dynamic Block Name] | Nome descrittivo che identifica il blocco dinamico nell’amministratore. |
| [!UICONTROL Dynamic Block Type] | Identifica il luogo in [layout di pagina standard](layout-updates.md) dove viene posizionato il blocco dinamico. Opzioni: <br/>**[!UICONTROL Content Area]**- Posiziona il blocco dinamico nell&#39;area [area contenuto](layout-updates.md) della pagina.<br/>**[!UICONTROL Footer]** - Inserisce il blocco dinamico nella pagina. [footer](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Inserisce il blocco dinamico nella pagina. [intestazione](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Posiziona il blocco dinamico nel [barra laterale a sinistra](page-layout.md#standard-page-layouts) di un layout a due o tre colonne. <br/>**[!UICONTROL Right Column]**- Posiziona il blocco dinamico nel [barra laterale destra](page-layout.md#standard-page-layouts) di un layout a due o tre colonne. |
| Segmento cliente | Associa un segmento di un cliente al blocco dinamico per determinare quali clienti possono visualizzarlo. |
| Pubblico Real-Time CDP | Associa una [Pubblico Real-Time CDP](../customers/audience-activation.md) con il blocco dinamico per determinare quali clienti possono visualizzarlo. |

{style="table-layout:auto"}

### Sommario

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Layout] | Aggiungere righe, colonne o schede all&#39;area di visualizzazione. |
| [!UICONTROL Elements] | Aggiungere testo, intestazioni, pulsanti, divisori e codice HTML a qualsiasi contenitore di layout sullo stage. |
| [!UICONTROL Media] | Aggiungi immagini, video, banner, cursori e mappe Google a qualsiasi contenitore di layout esistente sullo stage. |
| [!UICONTROL Add Content] | Aggiungi allo stage blocchi esistenti, blocchi dinamici e prodotti. |

{style="table-layout:auto"}

### Promozioni correlate

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Associa un elemento esistente [regola prezzo carrello](../merchandising-promotions/price-rules-cart.md) con il blocco dinamico come promozione. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Associa un elemento esistente [regola prezzo catalogo](../merchandising-promotions/price-rules-catalog.md) con il blocco dinamico come promozione. |

{style="table-layout:auto"}
