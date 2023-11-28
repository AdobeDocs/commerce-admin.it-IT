---
title: Rilevamento funzionalità browser
description: Scopri come configurare il rilevamento delle funzionalità del browser e visualizzare un avviso nel caso in cui sia necessario modificare le impostazioni del browser del cliente.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Rilevamento funzionalità browser

Come la maggior parte dei siti web e delle applicazioni su Internet, Adobe Commerce e Magento Open Source richiedono che il browser del visitatore consenta sia i cookie che JavaScript per il funzionamento completo. Tuttavia, a volte il browser di un utente è impostato sull’impostazione di privacy più alta che impedisce sia i cookie che JavaScript. Il tuo store può essere configurato per testare le funzionalità del browser di ogni visitatore e visualizzare un avviso se le impostazioni devono essere modificate.

- Se le impostazioni della privacy del browser non consentono i cookie, puoi configurare il sistema per reindirizzarli automaticamente al [Abilita cookie](../content-design/pages.md#enable-cookies) , che spiega come creare le impostazioni consigliate con la maggior parte dei browser.
- Se le impostazioni della privacy del browser non consentono JavaScript, puoi configurare il sistema in modo che visualizzi il seguente messaggio sopra l’intestazione di ogni pagina.

Per informazioni tecniche, consulta [Browser supportati](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) nel _Guida all’installazione_.

## Configurare il rilevamento delle funzionalità del browser

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Browser Capabilities Detection]** ed effettuare le seguenti operazioni:

   - Per visualizzare istruzioni che spiegano come configurare il browser per l’autorizzazione dei cookie, imposta **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** a `Yes`.

   - Per visualizzare un banner sopra l’intestazione quando JavaScript è disabilitato nel browser dell’utente, imposta **[!UICONTROL Show Notice if JavaScript is Disabled]** a `Yes`.

   - Per visualizzare un banner sopra l&#39;intestazione quando Local Storage è disabilitato nel browser dell&#39;utente, impostare **[!UICONTROL Show Notice if Local Storage is Disabled]** a `Yes`.

   ![Configurazione generale - Rilevamento delle funzionalità del browser web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
