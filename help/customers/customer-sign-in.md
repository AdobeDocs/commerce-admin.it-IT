---
title: Accesso cliente
description: La funzione di accesso del cliente sullo storefront consente un facile accesso agli account dei clienti.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
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
