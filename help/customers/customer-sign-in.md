---
title: Accesso cliente
description: La funzione di accesso del cliente sullo storefront consente un facile accesso agli account dei clienti.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/WuMuGVXByzb0PlpkKHnJCT-s7ToHtb1odvTu18LxB-I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 0%

---

# Accesso cliente

I clienti possono accedere facilmente ai propri account da ogni pagina del tuo negozio. A seconda della [configurazione](../customers/account-options-new.md), i clienti possono essere reindirizzati al dashboard dell&#39;account o continuare a fare acquisti dopo aver effettuato l&#39;accesso ai loro account.

Se [CAPTCHA](../systems/security-captcha.md) è abilitato nella configurazione, la persona deve completare correttamente un test che ne verifichi la presenza come utente umano prima di poter accedere ai propri account.

Quando i clienti dimenticano le password, viene inviato un collegamento di reimpostazione all’indirizzo e-mail associato all’account. La configurazione delle [opzioni password](../customers/password-options.md) controlla l&#39;esperienza del cliente per i tentativi di accesso:

- Numero di tentativi di immissione di una password da parte di un cliente
- Numero di minuti tra un tentativo e l&#39;altro
- Numero totale di tentativi prima che l’account venga bloccato
- Lunghezza del blocco

![Collegamento di accesso nell&#39;intestazione della vetrina](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Accedi a un account cliente

1. Nell&#39;intestazione dello store, il cliente fa clic su **[!UICONTROL Sign in]**.

   ![Accesso cliente](assets/login.png){width="700" zoomable="yes"}

1. Immette l&#39;indirizzo **[!UICONTROL Email]** e **[!UICONTROL Password]**.

1. Clic su **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Se non riesce a ricordare la password, il cliente può fare clic su **[!UICONTROL Forgot Your Password?]** e seguire le [istruzioni](../customers/password-reset.md) per reimpostare la password.

## Imposta il reindirizzamento al dashboard account dopo l’accesso del cliente

Puoi configurare il negozio in modo da reindirizzare i clienti al dashboard dell’account dopo che hanno effettuato l’accesso o da farli continuare a fare acquisti.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandere la sezione **[!UICONTROL Login Options]**.

1. Imposta **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** su uno dei seguenti:

   - `Yes` - Il dashboard account viene visualizzato quando i clienti accedono ai propri account.
   - `No` - I clienti possono continuare a fare acquisti dopo aver effettuato l&#39;accesso ai loro account.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Accedi con Amazon

Per i negozi con un&#39;integrazione configurata di [!DNL Amazon Pay] e [!DNL Login with Amazon], i clienti possono accedere al proprio account buyer di Amazon.

1. Nell&#39;intestazione dello store, il cliente fa clic su **[!UICONTROL Sign in]**.

1. Clic su **[!UICONTROL Login with Amazon]**.

   ![Accesso con Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Quando viene richiesto di effettuare l&#39;accesso, il cliente immette **[!UICONTROL email address]** e **[!UICONTROL password]** per il proprio account buyer di Amazon.

   ![Immissione delle credenziali di Amazon](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Per concedere ad Amazon l&#39;autorizzazione a condividere le seguenti informazioni dal proprio account con lo store durante l&#39;elaborazione degli acquisti, fai clic su **OK**.

   - Nome
   - Indirizzo e-mail
   - Indirizzi di spedizione

   ![Concedi l&#39;autorizzazione per la condivisione dei dati](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Esci da un account cliente

1. Nell&#39;angolo superiore destro accanto a _[!UICONTROL Welcome, Customer Name!]_, il cliente fa clic sul selettore di menu **[!UICONTROL v]**.

1. Scegli **[!UICONTROL Sign Out]**.

Dopo la disconnessione, il cliente viene reindirizzato alla home page.
