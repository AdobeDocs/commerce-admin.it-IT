---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] dell'amministratore di Commerce.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>Un [carrello acquisti persistente](../../stores-purchase/cart-persistent.md) consente di conservare gli elementi non acquistati rimasti nel carrello e di salvarli per un periodo configurato in _Durata persistenza_. I cookie devono essere consentiti nel browser del cliente per l’utilizzo di un carrello persistente.

## [!UICONTROL General Options]

![Opzioni generali](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Sito Web | Determina se la persistenza è abilitata. |
| [!UICONTROL Persistence Lifetime (seconds)] | Sito Web | Definisce la durata del cookie persistente in secondi. Il valore massimo consentito è di 3153600000 secondi (100 anni). |
| [!UICONTROL Enable "Remember Me"] | Sito Web | Definisce se la casella di controllo _Ricorda utente_ viene visualizzata nelle pagine di accesso e registrazione dell&#39;archivio. Opzioni: <br/>**`Yes`**- Visualizza la casella di controllo _Ricorda utente_.<br/>**`No`** - Non visualizza la casella di controllo _Ricorda utente_ e il cookie persistente viene utilizzato solo per i clienti che lo hanno già. |
| [!UICONTROL "Remember Me" Default Value] | Sito Web | Definisce lo stato predefinito per la casella di controllo _Ricorda utente_. |
| [!UICONTROL Clear Persistence on Log Out] | Sito Web | Definisce se il cookie persistente viene eliminato quando un cliente store si disconnette. Indipendentemente dalla configurazione, se un cliente non si disconnette ma il cookie di sessione scade, il cookie persistente viene comunque utilizzato. |
| [!UICONTROL Persist Shopping Cart] | Sito Web | Definisce se l’utilizzo del cookie persistente consente di accedere ai dati del carrello dell’account corrispondente. Opzioni: <br/>**`Yes`**- Il contenuto del carrello viene salvato al termine della sessione.<br/>**`No`** - Il contenuto del carrello acquisti non viene salvato al termine della sessione. |
| [!UICONTROL Persist Wish List] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato degli elenchi dei desideri del cliente viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**- Il contenuto della lista dei desideri viene salvato al termine della sessione.<br/>**`No`** - La lista dei desideri non viene salvata al termine della sessione. |
| [!UICONTROL Persist Recently Ordered Items] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato degli elementi ordinati di recente viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**- Lo stato degli elementi ordinati di recente viene salvato al termine della sessione.<br/>**`No`** - Lo stato degli elementi ordinati di recente non viene salvato al termine della sessione. |
| [!UICONTROL Persist Currently Compared Products] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato dei prodotti attualmente confrontati viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**- Lo stato dei prodotti attualmente confrontati viene salvato al termine della sessione.<br/>**`No`** - Lo stato dei prodotti attualmente confrontati non viene salvato al termine della sessione. |
| [!UICONTROL Persist Comparison History] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato della cronologia di confronto viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**- Lo stato della cronologia di confronto viene salvato al termine della sessione.<br/>**`No`** - Lo stato della cronologia di confronto non viene salvato al termine della sessione. |
| [!UICONTROL Persist Recently Viewed Products] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato dei prodotti visualizzati di recente viene mantenuto al termine della sessione. Opzioni: <br/>**`Yes`**- Lo stato dei prodotti visualizzati di recente viene salvato al termine della sessione.<br/>**`No`** - Lo stato dei prodotti visualizzati di recente non viene salvato al termine della sessione. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se lo stato dell&#39;appartenenza al gruppo e i criteri di segmentazione dei clienti vengono mantenuti al termine della sessione. Opzioni: <br/>**`Yes`**- Lo stato dei dati di segmentazione e appartenenza al gruppo del cliente viene salvato al termine della sessione.<br/>**`No`** - Lo stato dei dati di segmentazione e appartenenza al gruppo del cliente non viene salvato al termine della sessione. |

{style="table-layout:auto"}
