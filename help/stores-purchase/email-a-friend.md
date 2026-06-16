---
title: Invia un'e-mail a un amico
description: Scopri come fornire un collegamento e-mail che consenta ai clienti di condividere facilmente i collegamenti ai prodotti con i loro amici.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
TQID: https://experienceleague.adobe.com/a75E4X5mTDXeCQKysvIecdU3OhsICiWTtwh7k-oK9cw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# Invia un&#39;e-mail a un amico

Il collegamento E-mail consente ai clienti di condividere facilmente con gli amici i collegamenti ai prodotti. Nell’archivio Luma demo, il collegamento E-mail viene visualizzato come icona di busta. Il modello di messaggio può essere personalizzato per la tua voce e il tuo marchio. Per evitare lo spamming, puoi limitare il numero di destinatari per ogni e-mail e il numero di prodotti che possono essere condivisi in un periodo di un’ora.

![Vetrina di esempio - invia un&#39;e-mail a un amico](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Configurare e-mail-a-friend

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Email to a Friend]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Email Templates]** e impostare le opzioni:

   ![Configurazione del catalogo - modelli e-mail](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Modelli e-mail](../configuration-reference/catalog/email-to-a-friend.md) nella _Guida di riferimento alla configurazione_.

   Per modificare l&#39;impostazione predefinita di qualsiasi campo, deselezionare la casella di controllo **[!UICONTROL Use system value]** per rendere modificabile il campo.

   - Imposta **[!UICONTROL Enabled]** su `Yes`.

   - Impostare **[!UICONTROL Select Email Template]** sul modello da utilizzare come base per i messaggi.

   - Se desideri richiedere che solo i clienti registrati possano inviare e-mail agli amici, imposta **[!UICONTROL Allow for Guests]** su `No`.

   - Per **[!UICONTROL Max Recipients]**, immettere il numero massimo di amici che possono essere presenti nella lista di distribuzione per un singolo messaggio.

   - Per **[!UICONTROL Max Products Sent in 1 Hour]**, immetti il numero massimo di prodotti che possono essere condivisi da un singolo utente con gli amici in un periodo di un&#39;ora.

   - Impostare **[!UICONTROL Limit Sending By]** su uno dei seguenti metodi per identificare il mittente delle e-mail:

     `IP Address` - (scelta consigliata) Identifica il mittente in base all&#39;indirizzo IP del computer utilizzato per inviare le e-mail.

     `Cookie (unsafe)` - Identifica il mittente tramite il cookie del browser. Questo metodo è meno efficace perché il mittente può eliminare il cookie per aggirare il limite.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Invia un&#39;e-mail a un amico sul vetrina

Quando questa funzione è configurata, i clienti dei negozi seguono questi passaggi per condividere le informazioni sui prodotti con gli amici.

1. In una pagina del catalogo, il cliente fa clic sul collegamento **[!UICONTROL Email]**.

1. Se la funzione è configurata solo per gli utenti registrati, effettua una delle seguenti operazioni:

   - Accedi al tuo account cliente.
   - Registrati per un nuovo account.

1. Completa **[!UICONTROL Message]** e immette il destinatario **[!UICONTROL Name]** e **[!UICONTROL Email Address]**.

   Se necessario, il cliente può aggiungere altri destinatari:

   - Clic su **[!UICONTROL Add Invitee]**.

   - Immette **[!UICONTROL Name]** e **[!UICONTROL Email Address]** della persona aggiuntiva.

     Possono inviare il messaggio a tutte le persone aggiuntive consentite dalla configurazione. È possibile rimuovere l&#39;invitato aggiunto facendo clic sul collegamento **[!DNL Remove]**.

1. Quando è pronto per inviare il messaggio, fa clic su **[!UICONTROL Send Email]**.

   ![Vetrina di esempio - invia un&#39;e-mail a un amico](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
