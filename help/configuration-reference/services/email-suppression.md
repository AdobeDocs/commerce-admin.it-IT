---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression] dell'amministratore di Commerce.
feature: Configuration, Communications
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service e Adobe Commerce Optimizer (infrastruttura SaaS gestita da Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression] consente agli amministratori di disattivare categorie specifiche di e-mail di sistema automatizzato senza influire sul resto dell&#39;e-mail dello store o richiedere il coinvolgimento degli sviluppatori. Utilizza questa funzione per interrompere temporaneamente o definitivamente determinate notifiche, ad esempio per ordinare e-mail durante una migrazione di dati o per inviare e-mail di marketing.

>[!IMPORTANT]
>
>Le notifiche di amministrazione relative alla sicurezza, come i codici di autenticazione a due fattori e le e-mail di reimpostazione della password amministratore, non vengono mai eliminate da questa funzione.

Le impostazioni di questa pagina vengono applicate per [visualizzazione archivio](../../getting-started/websites-stores-views.md#scope-settings) in modo da poter eliminare diverse categorie di posta elettronica per diversi storefront.

>[!NOTE]
>
>Se si disattiva l’eliminazione, viene ripristinata immediatamente la normale consegna delle e-mail, ma le e-mail inviate durante il periodo di eliminazione non vengono accodate.

## [!UICONTROL Email Suppression]

![Eliminazione e-mail](./assets/email-suppression.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | Visualizzazione store | Interruttore principale di accensione/spegnimento per la funzione. Se è impostato su `No` (impostazione predefinita), tutte le altre impostazioni di questa pagina vengono ignorate e tutti i messaggi e-mail vengono inviati normalmente. |
| [!UICONTROL Disabled Functional Areas] | Visualizzazione store | Seleziona una o più categorie aziendali le cui e-mail vengono eliminate. Consulta [Categorie di business](#business-categories) per conoscere il contenuto di ogni categoria. |
| [!UICONTROL Disabled Template IDs] | Visualizzazione store | Elenco facoltativo separato da virgole di modelli e-mail specifici da eliminare singolarmente, indipendentemente dalla categoria. Utilizzare il codice del modello (ad esempio, `customer_password_forgot_email_template`) o l&#39;ID del modello numerico per un modello personalizzato creato in Amministrazione. |

{style="table-layout:auto"}

### Categorie aziendali {#business-categories}

| Categoria | E-mail tipiche incluse |
|--- |--- |
| Account cliente | Creazione dell’account, reimpostazione della password, modifiche alle informazioni sull’account. |
| Order Management | Conferma ordine, fattura, spedizione, nota di accredito, annullamento ordine. |
| Restituisce (RMA) | Restituisci notifiche di autorizzazione merce. |
| Pagamento e pagamento | E-mail relative a pagamento e collegamento a pagamento. |
| Marketing | Newsletter, avvisi sui prodotti, condivisione di elenchi di desideri, e-mail a un amico, promemoria, inviti, registro di regali. |
| Crediti e premi del negozio | Biglietti regalo, punti premio, memorizzare le modifiche del saldo del credito. |
| B2B | Notifiche relative a società, offerte negoziabili e ordini di acquisto. |
| Notifiche di sistema | Notifiche operative come importazioni pianificate, esportazioni ed e-mail dei moduli di contatto. |

{style="table-layout:auto"}
