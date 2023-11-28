---
title: Reimposta password cliente
description: I clienti in genere reimpostano le password dalla vetrina, ma un amministratore dello store può avviare una reimpostazione della password o un accesso forzato dall’amministratore.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Reimposta password cliente

In genere, i clienti reimpostano le password dalla vetrina facendo clic su _[!UICONTROL Forgot Your Password?]_. Tuttavia, l’amministratore dello store può avviare una reimpostazione della password o un accesso forzato dall’amministratore.

| Funzione | Descrizione |
| --- | --- |
| Reimposta password | Un messaggio e-mail di reimpostazione della password viene inviato direttamente all’account e-mail del cliente. L&#39;amministratore del negozio non può accedere alla password del cliente. |
| Forza accesso | Revoca i token di accesso OAuth associati all’account cliente. Può essere utilizzato solo con account cliente a cui sono stati assegnati token OAuth, come parte di un’API web [integrazione](../systems/integrations.md). Per ulteriori informazioni, consulta [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione per gli sviluppatori. <br/><br/>Gli account cliente standard creati dalla vetrina o dall’amministratore non dispongono di token OAuth. |

{style="table-layout:auto"}

## Reimpostare una password dalla vetrina

1. Nella pagina di accesso, il cliente fa clic su **[!UICONTROL Forgot Your Password?]**.

1. Quando richiesto, immette il **[!UICONTROL Email Address]** che è associato al loro account e ai clic **[!UICONTROL Reset My Password]**.

   ![Password dimenticata](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Se l’indirizzo e-mail inserito corrisponde a quello associato all’account, il cliente riceve un’e-mail di conferma del ripristino della password con un collegamento per reimpostare la password.

1. Quando l’e-mail arriva, il cliente fa clic su _reimpostare la password_ collega e immette il loro **[!UICONTROL New Password]** quando richiesto.

1. Lo immette nuovamente per confermare e fa clic su **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >La nuova password deve contenere almeno sei caratteri, senza spazi. Quando ricevono la conferma che la password è aggiornata, possono utilizzare la nuova password per accedere al proprio account. Per impostazione predefinita, il _reimpostare la password_ il collegamento è valido per 24 ore.

## Reimpostare una password dall’amministratore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trova il conto cliente nella griglia e fai clic su **[!UICONTROL Edit]** nel _Azione_ colonna.

1. Nell’insieme di opzioni nella parte superiore della pagina, fai clic su **[!UICONTROL Reset Password]**.

   Il numero di richieste di reimpostazione della password consentite entro un&#39;ora è impostato in [configurazione](../configuration-reference/customers/customer-configuration.md) argomento.

## Revocare i token OAuth di un cliente

>[!IMPORTANT]
>
>Non procedere se non hai una piena comprensione dell’autenticazione API.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trova il conto cliente nella griglia e fai clic su **[!UICONTROL Edit]** nel _Azione_ colonna.

1. Nell’insieme di opzioni nella parte superiore della pagina, fai clic su **[!UICONTROL Force Sign In]**.

1. Quando viene richiesto di confermare, fai clic su **OK**.
