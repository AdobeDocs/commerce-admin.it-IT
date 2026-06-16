---
title: Modifiche pianificate per le regole prezzo carrello
description: Scopri come applicare le regole di prezzo del carrello alla pianificazione come parte di una campagna e raggruppate con altre modifiche al contenuto.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/S4sSXY-SSMabdW-rkaqr-cMexe0q1-k6AbTNvb7pR14
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 0%

---

# Modifiche pianificate per le regole prezzo carrello

{{ee-feature}}

Le regole di prezzo del carrello possono essere applicate secondo programma come parte di una campagna e raggruppate con altre modifiche al contenuto. Puoi creare una campagna in base alle modifiche pianificate per una regola di prezzo o applicare le modifiche a una campagna esistente.

>[!NOTE]
>
>I campi [!UICONTROL From] e [!UICONTROL To] sono stati rimossi in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce e non possono essere modificati direttamente nella regola del prezzo del carrello. Devi creare un aggiornamento pianificato per queste attivazioni.

![Regole prezzo carrello - modifiche pianificate](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Tutti gli aggiornamenti pianificati vengono applicati consecutivamente. Ciò significa che qualsiasi entità può avere un solo aggiornamento pianificato in un determinato momento. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere diversi aggiornamenti pianificati per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

Se nella stessa campagna sono in esecuzione più regole di prezzo, l&#39;impostazione _[!UICONTROL Priority]_&#x200B;della regola di prezzo determina quale regola ha la precedenza. Per ulteriori informazioni, consulta [Gestione temporanea dei contenuti](../content-design/content-staging.md).

>[!NOTE]
>
>Se inizialmente viene creata una campagna attiva senza una data di fine, non è possibile modificarla in un secondo momento in modo da includere una data di fine. In tal caso, è necessario creare una campagna duplicata e immettere la data di fine necessaria.

>[!NOTE]
>
>Se una campagna è collegata a più regole di prezzo del carrello, è possibile modificarla solo dal [dashboard staging contenuto](../content-design/content-staging-dashboard.md).

Considera le seguenti avvertenze:

- Se una campagna che include una regola di prezzo viene creata inizialmente senza una data di fine, non sarà possibile modificarla in seguito per includere una data di fine. È consigliabile aggiungere una data di fine al momento della creazione della campagna o creare una versione duplicata della campagna esistente e aggiungere la data di fine al duplicato, in base alle esigenze.
- Quando utilizzi un aggiornamento pianificato per abilitare una regola del prezzo del carrello con una data di fine, assicurati di impostare la regola come inizialmente disabilitata. Le regole già attive non rispettano la data di fine.
- I coupon non sono collegati alle regole di prezzo del carrello. Un aggiornamento pianificato non fornisce l&#39;accesso ai campi _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_&#x200B;e_[!UICONTROL Uses per Customer]_ nella scheda _[!UICONTROL Rule Information]_. Inoltre, tutte le impostazioni della scheda&#x200B;_[!UICONTROL Manage Coupon Codes]_ non sono disponibili.

>[!IMPORTANT]
>
>Le campagne **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** devono essere definite utilizzando il fuso orario di amministrazione **_default_**, che viene convertito dal fuso orario locale di ciascun sito Web. Prendi in considerazione un esempio in cui disponi di più siti web in fusi orari diversi, ma desideri avviare una campagna basata su un fuso orario degli Stati Uniti. In questo caso, è necessario pianificare un aggiornamento separato per ogni fuso orario locale e impostare **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** convertiti da ogni fuso orario del sito Web locale sul fuso orario predefinito dell&#39;amministratore.
