---
title: Transazioni
description: Scopri la pagina Transazioni e come utilizzarla per monitorare l’attività tra il tuo Negozio e un sistema di pagamento.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
TQID: https://experienceleague.adobe.com/WyZwtVw-F-pGxxfcHMU-UTz8GVROVyM-YYaLzivMLBM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 0%

---

# Transazioni

La pagina _Transazioni_ elenca tutte le attività di pagamento che hanno avuto luogo tra il tuo Negozio e un sistema di pagamento e fornisce l&#39;accesso a informazioni più dettagliate.

## Visualizza transazioni

Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![Griglia transazioni](./assets/transactions.png){width="600" zoomable="yes"}

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Un identificatore numerico univoco assegnato a ogni transazione. |
| [!UICONTROL Order ID] | Identificatore univoco assegnato quando un cliente effettua un ordine. |
| [!UICONTROL Transaction ID] | Identificatore numerico univoco assegnato quando una transazione si verifica dopo che un cliente ha effettuato un ordine. |
| [!UICONTROL Parent Transaction ID] | Numero ID della transazione padre. |
| [!UICONTROL Payment Method] | Il metodo di pagamento associato a una transazione. |
| [!UICONTROL Transaction Type] | Tipo di transazione, che può essere Ordine, Autorizzazione, Acquisizione, Annullamento o Rimborso. |
| [!UICONTROL Closed] | Indica se una transazione è chiusa o meno. |
| [!UICONTROL Created] | Ora e data di creazione della transazione. |

{style="table-layout:auto"}

## Visualizza dettagli transazione

Fare clic sulla voce da visualizzare.

Nella pagina dei dettagli della transazione è possibile visualizzare la griglia dei dettagli della transazione e delle transazioni figlio.

### Dati transazione

Questa sezione include informazioni relative alla transazione e fornisce un collegamento alla pagina dell&#39;ordine nella colonna **ID ordine**.

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Transaction ID] | Numero ID transazione. |
| [!UICONTROL Parent Transaction ID] | Numero ID corrispondente della transazione padre, se applicabile. |
| [!UICONTROL Transaction Type] | Tipo di transazione, che può essere Ordine, Autorizzazione, Acquisizione, Annullamento o Rimborso. |
| [!UICONTROL Is Closed] | Indica se una transazione è chiusa o meno. |
| [!UICONTROL Created At] | Ora e data di creazione della transazione. |

{style="table-layout:auto"}

### Transazioni figlio

Le transazioni secondarie vengono visualizzate nella griglia dopo la creazione delle fatture per [ordini](orders.md). Questo formato consente di tenere traccia della cronologia delle transazioni, seguendo una gerarchia di transazioni.

### [!UICONTROL Transaction Details]

Questa sezione include le informazioni aggiuntive per una determinata transazione. Le informazioni vengono visualizzate sotto forma di chiavi e valori. Le chiavi disponibili sono:

- authAmount
- authCode
- RispostaVSR
- BillTo
- cardCodeResponse
- cliente
- customerIP
- lineItems
- marketType
- ordine
- pagamento
- prodotto
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settleImporto
- soluzione
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>Se i dettagli della transazione non sono disponibili o sono obsoleti, fare clic su **[!UICONTROL Fetch]** nella barra dei pulsanti per aggiornarli.
