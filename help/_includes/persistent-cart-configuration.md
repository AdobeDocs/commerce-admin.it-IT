---
title: Riferimento configurazione del carrello acquisti persistente
description: Contenuto riutilizzabile per il riferimento alla configurazione del carrello acquisti persistente.
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Opzioni generali](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| Campo | [Ambito](/help/getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Sito Web | Determina se la funzione di persistenza è abilitata. |
| [!UICONTROL Persistence Lifetime (seconds)] | Sito Web | Definisce la durata del cookie persistente in secondi. Il valore massimo consentito è di 34560000 secondi (400 giorni). Si tratta di una limitazione della durata massima consigliata dei cookie. |
| [!UICONTROL Enable "Remember Me"] | Sito Web | Definisce se la casella di controllo _Ricorda utente_ viene visualizzata nelle pagine di accesso e registrazione dell&#39;archivio. Opzioni: <br/>**`Yes`**- Visualizza la casella di controllo _Ricorda utente_.<br/>**`No`** - Non visualizza la casella di controllo _Ricorda utente_ e il cookie persistente viene utilizzato solo per i clienti che lo hanno già. |
| [!UICONTROL "Remember Me" Default Value] | Sito Web | Definisce lo stato predefinito per la casella di controllo _Ricorda utente_. |
| [!UICONTROL Clear Persistence on Log Out] | Sito Web | Definisce se il cookie persistente viene eliminato quando un cliente store si disconnette. Indipendentemente dalla configurazione di questa opzione, se un cliente non si disconnette ma il cookie di sessione scade, il cookie persistente viene comunque utilizzato. |
| [!UICONTROL Persist Shopping Cart] | Sito Web | Definisce se l’utilizzo del cookie persistente consente di accedere ai dati del carrello dell’account corrispondente. Opzioni: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Wish List] | Sito Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato degli elenchi dei desideri del cliente viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**- Il contenuto della lista dei desideri viene salvato al termine della sessione.<br/>**`No`** - La lista dei desideri non viene salvata al termine della sessione. |
| [!UICONTROL Persist Recently Ordered Items] | Sito Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato degli elementi ordinati di recente viene salvato al termine della sessione. Opzioni: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Sito Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato dei prodotti attualmente confrontati viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Comparison History] | Sito Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato della cronologia di confronto viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Sito Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato dei prodotti visualizzati di recente viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Sito Web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato dell&#39;appartenenza al gruppo e i criteri di segmentazione dei clienti vengono mantenuti al termine della sessione. Opzioni: <br/>**`Yes`**- Lo stato dei dati di segmentazione e appartenenza al gruppo del cliente viene salvato al termine della sessione.<br/>**`No`** - Lo stato dei dati di segmentazione e appartenenza al gruppo del cliente non viene salvato al termine della sessione. |

{style="table-layout:auto"}
