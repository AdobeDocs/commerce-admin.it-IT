---
title: Ambito account cliente
description: L’ambito degli account cliente può essere limitato al sito web in cui è stato creato l’account o condiviso con tutti i siti web e i negozi nella gerarchia del negozio.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 2541b2d55516e2a9c824825100c8348d81201ca9
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Ambito account cliente

L&#39;intestazione di ogni pagina del negozio estende l&#39;invito agli acquirenti a _Accedi o registra_ per un account con il tuo negozio. I clienti che aprono un account possono usufruire di una serie di vantaggi, tra cui:

* **Crea account cliente** - I visitatori possono creare un account cliente per utilizzare la vetrina come cliente registrato.
* **Creare un account società** A seconda della configurazione, un visitatore del tuo negozio può scegliere di creare un account aziendale. Per ulteriori informazioni, consulta [B2B per Adobe Commerce](../b2b/introduction.md).
* **Pagamento più rapido** — I clienti registrati passano attraverso il checkout più rapidamente perché molte delle informazioni sono già nei loro account.
* **Self-service** — I clienti registrati possono aggiornare le informazioni, controllare lo stato degli ordini e persino riordinare i prodotti dai loro account.

I clienti possono accedere al proprio account facendo clic sul pulsante **[!UICONTROL My Account]** nell’intestazione del negozio. Dal proprio account, i clienti possono visualizzare e modificare le informazioni, inclusi gli indirizzi passati e correnti, le preferenze di fatturazione e spedizione, gli abbonamenti alle newsletter, la lista dei desideri e altro ancora.

![Il mio account](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Imposta l&#39;ambito degli account cliente

L’ambito degli account cliente può essere limitato al sito web in cui è stato creato l’account o condiviso con tutti i siti web e i negozi nella gerarchia del negozio.

>[!NOTE]
>
>Se il sito web viene escluso dal gruppo di clienti, al cliente non è consentito accedere al sito web quando l’ambito degli account del cliente è limitato al sito web o condiviso con tutti i siti web. Consulta [Creare un gruppo di clienti](customer-groups.md#create-a-customer-group) per ulteriori informazioni sull&#39;esclusione di siti Web dai gruppi.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandi **[!UICONTROL Account Sharing Options]** sezione.

   ![Opzioni di condivisione account](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Share Customer Accounts]** a uno dei seguenti elementi:

   | Opzione | Descrizione |
   | --- | --- |
   | `Global` | Condivide le informazioni sull&#39;account del cliente con ogni sito Web e negozio dell&#39;installazione. |
   | `Per Website` | Limita le informazioni sull&#39;account del cliente al sito Web in cui è stato creato l&#39;account. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Se necessario, cancellare il **[!UICONTROL User system value]** per apportare la modifica.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Quando `Global` è selezionato nelle informazioni del cliente in **Il mio account** (indirizzi e informazioni sull’account, ad esempio i recapiti) vengono condivisi.
