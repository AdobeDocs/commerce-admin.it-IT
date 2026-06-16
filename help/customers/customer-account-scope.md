---
title: Ambito account cliente
description: L’ambito degli account cliente può essere limitato al sito web in cui è stato creato l’account o condiviso con tutti i siti web e i negozi nella gerarchia del negozio.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 0%

---

# Ambito account cliente

L&#39;intestazione di ogni pagina del tuo archivio estende un invito per gli acquirenti a _Accedi o registrati_ per un account con il tuo archivio. I clienti che aprono un account possono usufruire di una serie di vantaggi, tra cui:

* **Crea account cliente** - I visitatori possono creare un account cliente in modo da poter utilizzare la vetrina come cliente registrato.
* **Crea un account aziendale** A seconda della configurazione, un visitatore del tuo archivio può scegliere di creare un account aziendale. Per ulteriori informazioni, vedere [Adobe Commerce B2B](../b2b/introduction.md).
* **Estrazione più rapida**: i clienti registrati passano più rapidamente all&#39;estrazione perché molte delle informazioni sono già presenti nei loro account.
* **Self-service**: i clienti registrati possono aggiornare le proprie informazioni, controllare lo stato degli ordini e persino riordinare i propri account.

I clienti possono accedere al proprio account facendo clic sul collegamento **[!UICONTROL My Account]** nell&#39;intestazione dello store. Dal proprio account, i clienti possono visualizzare e modificare le informazioni, inclusi gli indirizzi passati e correnti, le preferenze di fatturazione e spedizione, gli abbonamenti alle newsletter, la lista dei desideri e altro ancora.

![Il mio account](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Imposta l&#39;ambito degli account cliente

L’ambito degli account cliente può essere limitato al sito web in cui è stato creato l’account o condiviso con tutti i siti web e i negozi nella gerarchia del negozio.

>[!NOTE]
>
>Se il sito web viene escluso dal gruppo di clienti, al cliente non è consentito accedere al sito web quando l’ambito degli account del cliente è limitato al sito web o condiviso con tutti i siti web. Per ulteriori informazioni sull&#39;esclusione di siti Web dai gruppi, vedere [Creare un gruppo di clienti](customer-groups.md#create-a-customer-group).

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandere la sezione **[!UICONTROL Account Sharing Options]**.

   ![Opzioni di condivisione account](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Share Customer Accounts]** su uno dei seguenti:

   | Opzione | Descrizione |
   | --- | --- |
   | `Global` | Condivide le informazioni sull&#39;account del cliente con ogni sito Web e negozio dell&#39;installazione. |
   | `Per Website` | Limita le informazioni sull&#39;account del cliente al sito Web in cui è stato creato l&#39;account. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Se necessario, deselezionare la casella di controllo **[!UICONTROL User system value]** per apportare la modifica.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Quando `Global` è selezionato, le informazioni del cliente in **Il mio account** (indirizzi e informazioni sull&#39;account come i dettagli di contatto) vengono condivise.
