---
title: Trasferire un account Adobe Commerce
description: Scopri come trasferire un account Adobe Commerce a un nuovo proprietario o indirizzo e-mail, scegliere il tipo di trasferimento corretto, verificare le modifiche e-mail e contattare il supporto tecnico.
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
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Trasferire un account Adobe Commerce

Con il cambiare delle responsabilità aziendali, potrebbe essere necessario trasferire l’account Adobe Commerce a un nuovo proprietario o a un altro indirizzo e-mail. Questo trasferimento richiede una modifica all’e-mail utente principale associata all’account.

Le informazioni seguenti descrivono il processo di trasferimento di un account Adobe Commerce (MAGEID). Non include modifiche ad Adobe Commerce sulla proprietà del progetto di infrastruttura cloud o sulla proprietà [!DNL New Relic]. Per ulteriori informazioni sull&#39;accesso ai progetti cloud, vedere [Gestire l&#39;accesso degli utenti](https://experienceleague.adobe.com/it/docs/commerce-cloud-service/user-guide/project/user-access) nella _Guida di Commerce sull&#39;infrastruttura cloud_.

>[!IMPORTANT]
>
>Se il nuovo proprietario dell&#39;account ha acquistato estensioni utilizzando Accesso condiviso, l&#39;accesso a tali estensioni viene perso non appena inizia il trasferimento dell&#39;account.
>
>Prima di richiedere il trasferimento dell&#39;account, assicurati che il nuovo proprietario recuperi gli ID ordine per gli acquisti da [loro [!DNL Commerce Marketplace] account](https://commercemarketplace.adobe.com/sales/order/history/) e richieda un rimborso al [[!DNL Commerce Marketplace] team](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Gli acquisti di estensione non possono essere trasferiti a un account diverso.

## Identificare il tipo di trasferimento

Il processo di trasferimento dell’account Adobe Commerce appropriato dipende dallo stato dell’account del proprietario corrente e del nuovo proprietario e dal fatto che l’indirizzo e-mail del proprietario corrente sia ancora accessibile. Ad esempio, se il proprietario corrente ha lasciato la società, potrebbe essere ancora necessario accedere alle e-mail inviate a tale indirizzo.

Gli scenari seguenti descrivono le opzioni di trasferimento disponibili in base a queste condizioni.

| Tipo di trasferimento | Proprietario corrente | Nuovo proprietario |
| ------------- | ------------- | --------- |
| [Nuova Adobe ID e modifica e-mail](#new-adobe-id-and-email-change) | Ha un MAGEID che non è stato connesso a un Adobe ID | Non dispone di un MAGEID e non dispone di un Adobe ID. |
| [Solo modifica e-mail](#email-change) | Dispone di un MAGEID connesso a un Adobe ID. | Ha un Adobe ID, ma non ha un MAGEID connesso all’account. |
| [Opzione account Adobe ID](#adobe-id-account-switch) | Dispone di un MAGEID connesso a un Adobe ID. | Ha un MAGEID ed è connesso a un Adobe ID. |

{style="table-layout:auto"}

>[!NOTE]
>
>Mentre Adobe Commerce continua a integrarsi con altre soluzioni Adobe, un account Adobe Commerce (MAGEID) ora richiede un’associazione con un Adobe ID. Adobe ID utilizza lo stesso indirizzo e-mail connesso al tuo account [Adobe Commerce](https://experienceleague.adobe.com/it/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

## Verificare una modifica e-mail in Adobe ID

Diversi percorsi di trasferimento utilizzano lo stesso flusso di lavoro di verifica in [account.adobe.com](https://account.adobe.com/). Dopo aver immesso l&#39;indirizzo di posta elettronica di destinazione e aver fatto clic su **[!UICONTROL Change]**, completare i passaggi seguenti:

1. Apri il messaggio di verifica inviato all’indirizzo inserito e individua il codice di conferma.

1. Immetti il codice di conferma.

1. Fare clic su **[!UICONTROL Verify]**.

## Nuovo Adobe ID e modifica dell’e-mail

>[!IMPORTANT]
>
>Rivedi i [tipi di trasferimento](#identify-your-transfer-type) e verifica che il percorso corrisponda alla tua situazione:
>
>- L&#39;attuale proprietario è ancora con l&#39;azienda.
>- Il proprietario corrente non dispone di un Adobe ID o dispone di un Adobe ID non connesso al proprio account [Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/it/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Il nuovo proprietario non dispone di un Adobe ID e non dispone di un account Adobe Commerce.

Usa questo percorso quando il proprietario corrente dispone di un MAGEID non ancora collegato a un Adobe ID. Il proprietario corrente crea e collega innanzitutto un Adobe ID, quindi modifica l’indirizzo e-mail di Adobe ID in quello del nuovo proprietario.

1. Vai alla pagina di accesso dell&#39;[account Adobe Commerce](https://account.magento.com/customer/account/login/).

1. Fare clic su **[!UICONTROL Sign in with Adobe ID]**.

1. Fare clic su **[!UICONTROL Create an account]**.

1. Immettere l&#39;indirizzo e-mail e la password del proprietario corrente.

1. Fare clic su **[!UICONTROL Continue]**.

   Questo passaggio crea un Adobe ID e lo collega all’account Adobe Commerce corrente (MAGEID). Con questo collegamento di account, il campo _[!UICONTROL Email]_&#x200B;è bloccato da eventuali modifiche. La configurazione dell’indirizzo e-mail associato viene gestita dall’account Adobe ID.

1. Passa a [account.adobe.com](https://account.adobe.com/).

1. Fare clic su **[!UICONTROL Change Email]**.

1. Immettere l&#39;indirizzo e-mail del nuovo proprietario.

   Se il nuovo indirizzo e-mail è già collegato a un altro account nel sistema, non può essere utilizzato direttamente per il trasferimento. Segui invece il percorso del [cambio account Adobe ID](#adobe-id-account-switch) e utilizza un [indirizzo e-mail temporaneo](#change-to-a-temporary-account).

1. Completa i [passaggi di verifica e-mail](#verify-an-adobe-id-email-change).

Dopo che il nuovo proprietario avrà verificato l&#39;indirizzo e-mail, continuare con [Passaggi finali](#final-steps) in modo che il supporto Adobe Commerce possa aggiornare i record dell&#39;account, ad esempio il profilo [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

>[!VIDEO](https://video.tv.adobe.com/v/3447667/?captions=ita&learn=on){transcript=true}

## Solo modifica e-mail {#email-change}

>[!IMPORTANT]
>
>Rivedi i [tipi di trasferimento](#identify-your-transfer-type) e verifica che il percorso corrisponda alla tua situazione:
>
>- L&#39;attuale proprietario è ancora con l&#39;azienda.
>- Il proprietario corrente dispone di un Adobe ID connesso al proprio account [Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/it/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Il nuovo proprietario dispone di un Adobe ID non connesso a un account Adobe Commerce.

Prima di iniziare, tieni presente che con questo tipo di trasferimento il proprietario dell’account corrente perde l’accesso ad altri prodotti Adobe associati a tale Adobe ID.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe.

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail del nuovo proprietario.

   Se il nuovo indirizzo e-mail è già collegato a un altro account nel sistema, non può essere utilizzato direttamente per il trasferimento. Segui invece il percorso del [cambio account Adobe ID](#adobe-id-account-switch) e utilizza un [indirizzo e-mail temporaneo](#change-to-a-temporary-account).

1. Completa i [passaggi di verifica e-mail](#verify-an-adobe-id-email-change).

Dopo che il nuovo proprietario avrà verificato l&#39;indirizzo e-mail, continuare con [Passaggi finali](#final-steps) in modo che il supporto Adobe Commerce possa aggiornare i record dell&#39;account, ad esempio il profilo [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Passaggio a un altro account di Adobe ID

>[!IMPORTANT]
>
>Rivedi i [tipi di trasferimento](#identify-your-transfer-type) e verifica che il percorso corrisponda alla tua situazione:
>
>- Il proprietario corrente non fa più parte della società, ma le e-mail inviate all&#39;indirizzo e-mail della società del proprietario corrente sono ancora accessibili, altrimenti il team IT può inoltrarle a un contatto autorizzato.
>- Il proprietario corrente dispone di un Adobe ID connesso al proprio account [Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/it/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- Il nuovo proprietario dispone di un Adobe ID connesso al proprio account Adobe Commerce.

Questo tipo di trasferimento utilizza un indirizzo e-mail temporaneo per cambiare la proprietà dell’account quando sia il proprietario corrente che il nuovo proprietario dispongono di Adobe ID esistenti e desideri mantenere entrambi gli Adobe ID. Per completare il trasferimento di proprietà, devi utilizzare un indirizzo e-mail temporaneo non associato a un Adobe ID.

### Passare a un account temporaneo

Completa questi passaggi per associare l’Adobe ID del proprietario corrente a un indirizzo e-mail temporaneo. Devi avere accesso a quell’indirizzo e-mail in modo da poter recuperare il codice di conferma.

>[!NOTE]
>
>Se non riesci ad accedere all’e-mail del proprietario corrente, chiedi al tuo team IT di configurare l’inoltro e-mail per l’indirizzo e-mail dell’account nel sistema e-mail dell’azienda. Se non è possibile configurare l&#39;inoltro di posta elettronica, verificare che il nuovo proprietario dell&#39;account disponga di un Adobe ID, quindi [inviare una richiesta di supporto](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) con tutti i dettagli necessari per avviare il trasferimento dell&#39;account.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe.

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti un indirizzo e-mail temporaneo valido non utilizzato da un Adobe ID.

1. Completa i [passaggi di verifica e-mail](#verify-an-adobe-id-email-change).

1. Esci dall’account Adobe.

### Nuovi passaggi del proprietario

Dopo che il proprietario corrente ha completato il trasferimento a un indirizzo e-mail temporaneo, il nuovo proprietario deve completare questi passaggi per cambiare il proprio indirizzo e-mail di Adobe ID con l&#39;indirizzo e-mail originale del proprietario corrente.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe.

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail originale del proprietario corrente.

1. Completa i [passaggi di verifica e-mail](#verify-an-adobe-id-email-change).

1. Esci dall’account Adobe.

### Passaggi successivi

Dopo che il nuovo proprietario ha configurato correttamente il proprio Adobe ID con l’indirizzo e-mail originale del proprietario corrente, completa questi passaggi per assegnare tale indirizzo e-mail al nuovo proprietario.

1. Passa a [account.adobe.com](https://account.adobe.com/) e completa l&#39;accesso ad Adobe utilizzando l&#39;indirizzo e-mail per [account temporaneo](#change-to-a-temporary-account).

1. Sotto il nome account e l&#39;avatar, fare clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail del nuovo proprietario.

1. Completa i [passaggi di verifica e-mail](#verify-an-adobe-id-email-change).

Dopo che il nuovo proprietario avrà verificato l&#39;indirizzo e-mail, continuare con [Passaggi finali](#final-steps) in modo che il supporto Adobe Commerce possa aggiornare i record dell&#39;account, ad esempio il profilo [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Passaggi finali

Completa questi passaggi dopo aver completato il processo [Nuovo Adobe ID e modifica e-mail](#new-adobe-id-and-email-change), [Solo modifica e-mail](#email-change) o [Cambio account Adobe ID](#adobe-id-account-switch).

1. Come nuovo proprietario, [invia una richiesta di supporto](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case).

   Includi i seguenti dettagli:

   - Indirizzo e-mail del proprietario dell’account precedente
   - Indirizzo e-mail del nuovo proprietario
   - Nota relativa al completamento del trasferimento di un account Adobe Commerce e all’aggiornamento dell’indirizzo e-mail di Adobe ID

1. Attendi che il supporto Adobe Commerce confermi l’aggiornamento.

   Il supporto aggiorna anche i record correlati, ad esempio l&#39;indirizzo di posta elettronica nel profilo [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

Una volta completata la richiesta, il nuovo proprietario può accedere all’account Adobe Commerce con il proprio Adobe ID. MAGEID rimane l’identificatore di adesione per l’account.
