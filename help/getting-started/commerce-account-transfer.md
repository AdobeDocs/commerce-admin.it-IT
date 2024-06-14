---
title: Trasferire un account Commerce
description: Scopri come trasferire il tuo account Commerce a un altro proprietario o indirizzo e-mail.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 59a88468dabfd1042b664f658225de2504b66b1b
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Trasferire un account Commerce

Con il cambiare delle responsabilità aziendali, potrebbe essere necessario trasferire la proprietà dell&#39;account Commerce esistente a un nuovo proprietario o a un altro indirizzo e-mail. Questo trasferimento richiede una modifica all’e-mail utente principale associata all’account.

Le informazioni seguenti descrivono il processo di trasferimento di un account Commerce (MAGEID). Non include le modifiche relative alla proprietà dell’account Cloud (progetto Cloud o New Relic). Per ulteriori informazioni sull’accesso ai progetti cloud, consulta [Gestire l’accesso degli utenti](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) nel _Guida di Commerce sull’infrastruttura cloud_.

## Identificare il tipo di trasferimento

La modalità di completamento di questo trasferimento dipende da quale dei seguenti scenari descrive la tua situazione come il proprietario corrente dell’account e il nuovo proprietario (indirizzo e-mail) a cui desideri trasferire l’account:

| Tipo di trasferimento | Proprietario corrente | Nuovo proprietario |
| ------------- | ------------- | --------- |
| [Nuovo Adobe ID e modifica dell’e-mail](#new-adobe-id-and-email-change) | Ha un MAGEID che è **_non connesso_** con un account di accesso di Adobe. | Non dispone di un MAGEID e non è connesso a un account di accesso di Adobe. |
| [Modifica e-mail](#email-change) | Ha un MAGEID che è **_connesso_** con un account di accesso Adobe senza altri prodotti/servizi Adobe associati. | Non dispone di un MAGEID e non è connesso a un account di accesso di Adobe. |
| [Switch Adobe ID](#adobe-id-account-switch) | Ha un MAGEID che è **_connesso_** con un account di accesso Adobe senza altri prodotti/servizi Adobe associati. | Dispone di un MAGEID ed è connesso a un account di accesso Adobe senza altri prodotti/servizi Adobe associati. |

{style="table-layout:auto"}

>[!NOTE]
>
>Mentre Adobe Commerce continua a integrarsi con altre soluzioni Adobe, un account Commerce (MAGEID) ora richiede un’associazione con un accesso Adobe. Questo Adobe ID utilizza lo stesso indirizzo e-mail connesso al tuo account Commerce.

>[!NOTE]
>
>Se il proprietario corrente o il nuovo proprietario dispone di un account di accesso Adobe associato ad altri prodotti/servizi Adobe, puoi aprire un [ticket di supporto](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) per assistenza nel trasferimento di un account Commerce a un altro Adobe ID.

## Nuovo Adobe ID e modifica dell’e-mail

>[!IMPORTANT]
>
>Rivedi [tipi di trasferimento](#identify-your-transfer-type) e assicurati di soddisfare i prerequisiti per questa sequenza di passaggi.

Questo tipo di trasferimento richiede innanzitutto la creazione di un Adobe ID associato, quindi la modifica dell’account nell’indirizzo e-mail del nuovo proprietario.

1. Vai al tuo [Account Commerce](https://account.magento.com/customer/account/login/).

1. Clic **[!UICONTROL Sign in with Adobe ID]**.

1. Clic **[!UICONTROL Create an account]**.

1. Immettere l&#39;indirizzo e-mail del proprietario corrente e una password.

1. Clic **[!UICONTROL Continue]**.

   Viene creato un Adobe ID che viene collegato all’account Commerce corrente (MAGEID). Con questo collegamento di account, il _[!UICONTROL Email]_è bloccato da qualsiasi modifica. L’indirizzo e-mail associato è gestito dall’account Adobe ID.

1. Accedi a [account.adobe.com](https://account.adobe.com/).

1. Clic **[!UICONTROL Change Email]**.

1. Immettere l&#39;indirizzo e-mail del nuovo proprietario.

1. Clic **[!UICONTROL Change]**.

   Viene generato un messaggio e-mail di verifica inviato al nuovo indirizzo e-mail. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato al nuovo indirizzo e-mail.

1. Clic **[!UICONTROL Verify]**.

## Modifica e-mail

>[!IMPORTANT]
>
>Rivedi [tipi di trasferimento](#identify-your-transfer-type) e assicurati di soddisfare i prerequisiti per questa sequenza di passaggi.

1. Accedi a [account.adobe.com](https://account.adobe.com/) e completa l’accesso di Adobe.

1. Sotto il nome account e l’avatar, fai clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail del nuovo proprietario.

1. Clic **[!UICONTROL Change]**.

   Viene generato un messaggio e-mail di verifica inviato al nuovo indirizzo e-mail. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato al nuovo indirizzo e-mail.

1. Clic **[!UICONTROL Verify]**.

## Passaggio a un altro account di Adobe ID

>[!IMPORTANT]
>
>Rivedi [tipi di trasferimento](#identify-your-transfer-type) e assicurati di soddisfare i prerequisiti per questa sequenza di passaggi.

Nel caso in cui il proprietario corrente e il nuovo proprietario dispongano di ID Adobe esistenti, entrambi gli account devono rimanere, ma gli indirizzi e-mail devono essere scambiati. A tal fine è necessario utilizzare un _temporaneo_ indirizzo e-mail valido, ma non associato a e Adobe ID.

### Passare a un account temporaneo

Il proprietario corrente completa questi passaggi per associare il proprio Adobe ID a un altro indirizzo e-mail temporaneo.

1. Accedi a [account.adobe.com](https://account.adobe.com/) e completa l’accesso di Adobe.

1. Sotto il nome account e l’avatar, fai clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti un indirizzo e-mail temporaneo valido non utilizzato da un Adobe ID.

   Devi avere accesso all’indirizzo e-mail in modo da poter recuperare l’e-mail con il codice di conferma.

1. Clic **[!UICONTROL Change]**.

   Viene generato un messaggio e-mail di verifica inviato all&#39;indirizzo e-mail temporaneo. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immetti il codice di conferma inviato all’indirizzo e-mail temporaneo.

1. Clic **[!UICONTROL Verify]**.

1. Esci dall’account Adobe.

### Nuovi passaggi del proprietario

Dopo che il proprietario corrente ha completato il trasferimento a un indirizzo e-mail temporaneo, completa questi passaggi per cambiare l’account passando al proprietario corrente.

1. Accedi a [account.adobe.com](https://account.adobe.com/) e completa l’accesso di Adobe.

1. Sotto il nome account e l’avatar, fai clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail originale del proprietario corrente.

1. Clic **[!UICONTROL Change]**.

   Viene generato un messaggio e-mail di verifica inviato a tale indirizzo e-mail. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immettere il codice di conferma inviato al proprietario corrente.

1. Clic **[!UICONTROL Verify]**.

1. Esci dall’account Adobe.

### Passaggi successivi

Dopo che il nuovo proprietario ha trasferito correttamente il proprio account di Adobe al proprietario corrente (ora precedente), completa questi passaggi per trasferire la proprietà.

1. Accedi a [account.adobe.com](https://account.adobe.com/) (primo account utilizzato nella serie di passaggi) e completare l’accesso di Adobe.

   Questo accesso richiede l’utilizzo dell’indirizzo e-mail temporaneo.

1. Sotto il nome account e l’avatar, fai clic su **[!UICONTROL Change Email]**.

1. Nella finestra di dialogo, immetti l’indirizzo e-mail del nuovo proprietario.

1. Clic **[!UICONTROL Change]**.

   Viene generato un messaggio e-mail di verifica inviato a tale indirizzo e-mail. L’e-mail contiene un codice di conferma necessario per completare la modifica dell’indirizzo e-mail.

1. Immettere il codice di conferma inviato al nuovo proprietario.

1. Clic **[!UICONTROL Verify]**.

1. **Inviare una richiesta di supporto** per informare il team di supporto dell’aggiornamento dell’indirizzo e-mail del proprietario dell’account.

Il Supporto dovrà eseguire ulteriori passaggi, ad esempio l’aggiornamento dell’indirizzo e-mail sul [Commerce Marketplace](https://commercemarketplace.adobe.com/) profilo.
