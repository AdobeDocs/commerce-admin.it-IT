---
title: Reimposta password cliente
description: I clienti in genere reimpostano le password dalla vetrina, ma un amministratore dello store può avviare una reimpostazione della password o un accesso forzato dall’amministratore.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Reimposta password cliente

I clienti in genere reimpostano le password dalla vetrina facendo clic su _[!UICONTROL Forgot Your Password?]_. Tuttavia, l’amministratore dello store può avviare una reimpostazione della password o un accesso forzato dall’amministratore.

| Funzione | Descrizione |
| --- | --- |
| Reimposta password | Un messaggio e-mail di reimpostazione della password viene inviato direttamente all’account e-mail del cliente. L&#39;amministratore del negozio non può accedere alla password del cliente. |
| Forza accesso | Revoca i token di accesso OAuth associati all’account cliente. Può essere utilizzato solo con account cliente a cui sono stati assegnati token OAuth, come parte di una [integrazione](../systems/integrations.md) API Web. Per ulteriori informazioni, consulta [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione per gli sviluppatori. <br/><br/>Gli account cliente standard creati dalla vetrina o dall&#39;amministratore non dispongono di token OAuth. |

{style="table-layout:auto"}

## Reimpostare una password dalla vetrina

1. Nella pagina di accesso, il cliente fa clic su **[!UICONTROL Forgot Your Password?]**.

1. Quando richiesto, immette il **[!UICONTROL Email Address]** associato al proprio account e fa clic su **[!UICONTROL Reset My Password]**.

   ![Password dimenticata](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Se l’indirizzo e-mail inserito corrisponde a quello associato all’account, il cliente riceve un’e-mail di conferma del ripristino della password con un collegamento per reimpostare la password.

1. All&#39;arrivo dell&#39;e-mail, il cliente fa clic sul collegamento _reimposta password_ e, quando richiesto, immette **[!UICONTROL New Password]**.

1. Lo immette nuovamente per confermare e fa clic su **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >La nuova password deve contenere almeno sei caratteri, senza spazi. Quando ricevono la conferma che la password è aggiornata, possono utilizzare la nuova password per accedere al proprio account. Per impostazione predefinita, il collegamento _reimposta password_ è valido per 24 ore.

## Reimpostare una password dall’amministratore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trovare l&#39;account cliente nella griglia e fare clic su **[!UICONTROL Edit]** nella colonna _Azione_.

1. Nel set di opzioni nella parte superiore della pagina, fare clic su **[!UICONTROL Reset Password]**.

   Il numero di richieste di reimpostazione della password consentite entro un&#39;ora è impostato nell&#39;argomento [configurazione](../configuration-reference/customers/customer-configuration.md).

## Revocare i token OAuth di un cliente

>[!IMPORTANT]
>
>Non procedere se non hai una piena comprensione dell’autenticazione API.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trovare l&#39;account cliente nella griglia e fare clic su **[!UICONTROL Edit]** nella colonna _Azione_.

1. Nel set di opzioni nella parte superiore della pagina, fare clic su **[!UICONTROL Force Sign In]**.

1. Quando viene richiesto di confermare, fare clic su **OK**.
