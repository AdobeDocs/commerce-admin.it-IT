---
title: Trasferire un account Commerce
description: Scopri come trasferire il tuo account Commerce a un altro proprietario o indirizzo e-mail.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1273
ht-degree: 0%

---

# Trasferire un account Commerce

Con il cambiare delle responsabilità aziendali, potrebbe essere necessario trasferire l&#39;account Commerce a un nuovo proprietario o a un altro indirizzo e-mail. Questo trasferimento richiede una modifica all’e-mail utente principale associata all’account.

Le informazioni seguenti descrivono il processo di trasferimento di un account Commerce (MAGEID). Non include le modifiche relative alla proprietà dell’account Cloud (progetto Cloud o New Relic). Per ulteriori informazioni sull&#39;accesso ai progetti cloud, vedere [Gestire l&#39;accesso degli utenti](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=it) nella _Guida di Commerce sull&#39;infrastruttura cloud_.

>[!IMPORTANT]
>
>Se il nuovo proprietario dell&#39;account ha acquistato estensioni utilizzando Accesso condiviso, l&#39;accesso a tali estensioni viene perso non appena il processo di trasferimento dell&#39;account è stato avviato. Prima di richiedere il trasferimento dell&#39;account, assicurati che il nuovo proprietario recuperi gli ID ordine per gli acquisti dall&#39;[account Marketplace](https://commercemarketplace.adobe.com/sales/order/history/) e richieda un rimborso per tali estensioni al [team Marketplace](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Non è possibile trasferire gli acquisti dell’estensione a un altro account.

## Identificare il tipo di trasferimento

Il tipo di trasferimento dell&#39;account Commerce dipende dalle credenziali dell&#39;account Commerce disponibili per il proprietario corrente e il nuovo proprietario. Gli scenari seguenti descrivono i diversi tipi di trasferimento in base a queste credenziali.

| Tipo di trasferimento | Proprietario corrente | Nuovo proprietario |
| ------------- | ------------- | --------- |
| [Nuova Adobe ID e modifica e-mail](#new-adobe-id-and-email-change) | Ha un MAGEID che **_non è stato connesso_** a un account di accesso di Adobe | Non dispone di un MAGEID e non è connesso a un account di accesso Adobe. |
| [Modifica e-mail](#email-change) | Dispone di un MAGEID **_connesso_** con un account di accesso Adobe. | Dispone di un account di accesso Adobe, ma **_non dispone di un MAGEID_** connesso a un account di accesso Adobe. |
| [Opzione account Adobe ID](#adobe-id-account-switch) | Dispone di un MAGEID **_connesso_** a un account di accesso Adobe. | Dispone di un MAGEID ed è connesso a un account di accesso Adobe. |

{style="table-layout:auto"}

>[!NOTE]
>
>Mentre Adobe Commerce continua a integrarsi con altre soluzioni Adobe, un account Commerce (MAGEID) ora richiede un’associazione con un accesso Adobe. Questo Adobe ID utilizza lo stesso indirizzo e-mail connesso al tuo account Commerce.

## Nuovo Adobe ID e modifica dell’e-mail

>[!IMPORTANT]
>
>Rivedi i [tipi di trasferimento](#identify-your-transfer-type) e accertati di soddisfare i prerequisiti per questa sequenza di passaggi.

Questo tipo di trasferimento richiede un Adobe ID collegato all’account Commerce esistente e quindi la modifica dell’account nell’indirizzo e-mail del nuovo proprietario.

1. Vai alla pagina [Accesso account Commerce](https://account.magento.com/customer/account/login/).

1. Fare clic su **[!UICONTROL Sign in with Adobe ID]**.

1. Fare clic su **[!UICONTROL Create an account]**.

1. Immettere l&#39;indirizzo e-mail del proprietario corrente e una password.

1. Fare clic su **[!UICONTROL Continue]**.

   Questo passaggio crea un Adobe ID e lo collega all’account Commerce corrente (MAGEID). Con questo collegamento di account, il campo _[!UICONTROL Email]_&#x200B;è bloccato da eventuali modifiche. La configurazione dell’indirizzo e-mail associato viene gestita dall’account Adobe ID.

1. Passa a [account.adobe.com](https://account.adobe.com/).

1. Fare clic su **[!UICONTROL Change Email]**.

1. Immettere l&#39;indirizzo e-mail del nuovo proprietario.

   Se il nuovo indirizzo e-mail è già collegato a un altro account nel sistema, non può essere utilizzato direttamente per il trasferimento. Il processo richiede invece l&#39;utilizzo di un [indirizzo e-mail temporaneo](#change-to-a-temporary-account) per facilitare la modifica.

1. Fare clic su **[!UICONTROL Change]**.

   Questo passaggio genera un messaggio e-mail di verifica inviato al nuovo indirizzo e-mail. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato al nuovo indirizzo e-mail.

1. Fare clic su **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Modifica e-mail

>[!IMPORTANT]
>
>Rivedi i [tipi di trasferimento](#identify-your-transfer-type) e accertati di soddisfare i prerequisiti per questa sequenza di passaggi.

Questo tipo di trasferimento fa sì che il proprietario dell’account corrente perda l’accesso ad altri prodotti Adobe.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe.

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail del nuovo proprietario.

   Se il nuovo indirizzo e-mail è già collegato a un altro account nel sistema, non può essere utilizzato direttamente per il trasferimento. Il processo richiede invece l&#39;utilizzo di un [indirizzo e-mail temporaneo](#change-to-a-temporary-account) per facilitare la modifica.

1. Fare clic su **[!UICONTROL Change]**.

   Questo passaggio genera un messaggio e-mail di verifica inviato al nuovo indirizzo e-mail. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato al nuovo indirizzo e-mail.

1. Fare clic su **[!UICONTROL Verify]**.

## Passaggio a un altro account di Adobe ID

>[!IMPORTANT]
>
>Rivedi i [tipi di trasferimento](#identify-your-transfer-type) e accertati di soddisfare i prerequisiti per questa sequenza di passaggi.

Questo tipo di trasferimento utilizza un indirizzo e-mail temporaneo per cambiare la proprietà dell’account quando sia il proprietario corrente che il nuovo proprietario dispongono di Adobe ID esistenti e desideri mantenere entrambi gli account. Per completare il trasferimento di proprietà, devi utilizzare un indirizzo e-mail temporaneo non associato a un Adobe ID.

### Passare a un account temporaneo

Il proprietario corrente completa questi passaggi per associare il proprio Adobe ID a un altro indirizzo e-mail temporaneo.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe.

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti un indirizzo e-mail temporaneo valido non utilizzato da un Adobe ID.

>[!NOTE]
>
>Devi avere accesso all’indirizzo e-mail in modo da poter recuperare l’e-mail con il codice di conferma.
>
>Se non riesci ad accedere all’e-mail dell’account, chiedi al tuo team IT di configurare l’inoltro e-mail per l’indirizzo e-mail dell’account nel sistema e-mail dell’azienda. Se non è possibile configurare l&#39;inoltro e-mail, verificare che il nuovo Proprietario account disponga di un Adobe ID, quindi [inviare una richiesta di supporto](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) con tutti i dettagli necessari per avviare il trasferimento dell&#39;account.

1. Fare clic su **[!UICONTROL Change]**.

   Questo passaggio genera un messaggio e-mail di verifica inviato all’indirizzo e-mail temporaneo. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato all’indirizzo e-mail temporaneo.

1. Fare clic su **[!UICONTROL Verify]**.

1. Esci dall’account Adobe.

### Nuovi passaggi del proprietario

Dopo che il proprietario corrente ha completato il trasferimento a un indirizzo e-mail temporaneo, il nuovo proprietario deve completare questi passaggi per modificare la configurazione dell&#39;account in modo che punti all&#39;indirizzo e-mail originale del proprietario corrente.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe.

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail originale del proprietario corrente.

1. Fare clic su **[!UICONTROL Change]**.

   Questo passaggio genera un messaggio e-mail di verifica inviato all’indirizzo e-mail originale del proprietario corrente. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato all&#39;indirizzo e-mail originale del proprietario corrente.

1. Fare clic su **[!UICONTROL Verify]**.

1. Esci dall’account Adobe.

### Passaggi successivi

Dopo che il nuovo proprietario ha configurato correttamente l’account Adobe con l’indirizzo e-mail originale del proprietario corrente, completa questi passaggi per trasferire la proprietà.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe utilizzando l&#39;indirizzo e-mail per [account temporaneo](#change-to-a-temporary-account).

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail del nuovo proprietario.

1. Fare clic su **[!UICONTROL Change]**.

   Questo passaggio genera un messaggio e-mail di verifica inviato al nuovo indirizzo e-mail del proprietario. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immettere il codice di conferma inviato all&#39;indirizzo di posta elettronica del nuovo proprietario.

1. Fare clic su **[!UICONTROL Verify]**.

## Passaggi finali

Dopo che il nuovo proprietario ha completato i passaggi del primo o del terzo caso d&#39;uso, deve [inviare una richiesta di supporto](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case) per informare il team di supporto dell&#39;aggiornamento dell&#39;indirizzo e-mail. Il team di supporto completa quindi altre attività, ad esempio l&#39;aggiornamento dell&#39;indirizzo di posta elettronica nel profilo [Commerce Marketplace](https://commercemarketplace.adobe.com/). Includi nella richiesta l’indirizzo e-mail del proprietario dell’account precedente.
