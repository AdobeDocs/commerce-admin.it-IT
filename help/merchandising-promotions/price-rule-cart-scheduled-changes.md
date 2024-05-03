---
title: Modifiche pianificate per le regole prezzo carrello
description: Scopri come applicare le regole di prezzo del carrello alla pianificazione come parte di una campagna e raggruppate con altre modifiche al contenuto.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Modifiche pianificate per le regole prezzo carrello

{{ee-feature}}

Le regole di prezzo del carrello possono essere applicate secondo programma come parte di una campagna e raggruppate con altre modifiche al contenuto. Puoi creare una campagna in base alle modifiche pianificate per una regola di prezzo o applicare le modifiche a una campagna esistente.

>[!NOTE]
>
>Il [!UICONTROL From] e [!UICONTROL To] i campi sono stati rimossi in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e non possono essere modificati direttamente nella regola del prezzo del carrello. Devi creare un aggiornamento pianificato per queste attivazioni.

![Regole prezzo carrello - modifiche pianificate](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Tutti gli aggiornamenti pianificati vengono applicati consecutivamente. Ciò significa che qualsiasi entità può avere un solo aggiornamento pianificato in un determinato momento. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere diversi aggiornamenti pianificati per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

Se nella stessa campagna sono in esecuzione più regole di prezzo, il _[!UICONTROL Priority]_l&#39;impostazione della regola del prezzo determina quale regola ha la precedenza. Per ulteriori informazioni, consulta [Staging dei contenuti](../content-design/content-staging.md).

Considera le seguenti avvertenze:

- Se una campagna che include una regola di prezzo viene creata inizialmente senza una data di fine, non sarà possibile modificarla in seguito per includere una data di fine. È consigliabile aggiungere una data di fine al momento della creazione della campagna o creare una versione duplicata della campagna esistente e aggiungere la data di fine al duplicato, in base alle esigenze.
- Quando utilizzi un aggiornamento pianificato per abilitare una regola del prezzo del carrello con una data di fine, assicurati di impostare la regola come inizialmente disabilitata. Le regole già attive non rispettano la data di fine.
- I coupon non sono collegati alle regole di prezzo del carrello. Un aggiornamento pianificato non fornisce l’accesso al _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_, e_[!UICONTROL Uses per Customer]_ campi sul _[!UICONTROL Rule Information]_scheda. Inoltre, tutte le impostazioni da_[!UICONTROL Manage Coupon Codes]_ non sono disponibili.

>[!IMPORTANT]
>
>Campagna **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** deve essere definito utilizzando **_predefinito_** Fuso orario amministratore, che viene convertito dal fuso orario locale di ciascun sito web. Prendi in considerazione un esempio in cui disponi di più siti web in fusi orari diversi, ma desideri avviare una campagna basata su un fuso orario degli Stati Uniti. In questo caso, è necessario pianificare un aggiornamento separato per ogni fuso orario locale e impostare **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** convertito da ogni fuso orario del sito Web locale al fuso orario predefinito dell&#39;amministratore.
