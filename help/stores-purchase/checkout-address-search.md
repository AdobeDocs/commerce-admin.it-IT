---
title: Ricerca degli indirizzi al momento del pagamento
description: Scopri come includere la ricerca degli indirizzi al momento del pagamento nel tuo store.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Ricerca degli indirizzi al momento del pagamento

{{ee-feature}}

I clienti potrebbero avere molti indirizzi e informazioni salvati nella rubrica, in particolare clienti regolari, di ritorno o società che immettono più ordini e sedi di spedizione. La visualizzazione di molti indirizzi può rallentare notevolmente il caricamento e i processi di pagamento e causare un’esperienza di acquisto negativa. Per aumentare la reattività del pagamento, si consiglia di attivare e configurare la ricerca degli indirizzi per il sito.

>[!NOTE]
>
>La ricerca degli indirizzi non è attivata per impostazione predefinita. Puoi configurare questa funzione per includerla nel tuo sito.

Quando questa funzione è abilitata e il numero di indirizzi salvati del cliente soddisfa o supera il limite configurato, il _Spedizione_ e _Revisione e pagamenti_ i passaggi visualizzano un solo indirizzo (impostazione predefinita). Il cliente può modificare l’indirizzo selezionato facendo clic su **Cambia indirizzo** e quindi la ricerca dell&#39;indirizzo corretto per città, stato, strada o CAP. Questa funzione supporta anche la selezione degli indirizzi per l&#39;estrazione del Registro di sistema dei regali.

![Estrai con indirizzi di spedizione salvati visualizzati](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Se il cliente non ha un indirizzo di spedizione predefinito, il _Spedizione_ visualizzazioni pagina _Nessun indirizzo selezionato_. In questo caso, il cliente deve fare clic su **Cambia indirizzo** per selezionare un indirizzo salvato o fare clic su **Nuovo indirizzo** per aggiungere e selezionare un indirizzo prima di procedere con il pagamento. Se il cliente non ha un indirizzo di fatturazione predefinito, il _Revisione e pagamenti_ mostra l’indirizzo selezionato per la spedizione insieme al _Cambia indirizzo_ opzione.

![Estrai senza indirizzo selezionato messaggio](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Ricerca di virgolette per indirizzi bloccati

![Adobe Commerce B2B](../assets/b2b.svg) (Disponibile solo con Adobe Commerce B2B)

L&#39;abilitazione della ricerca degli indirizzi influisce anche sul pagamento degli ordini creati da preventivi in cui il numero di indirizzi salvati del cliente soddisfa o supera il limite configurato. Quando il preventivo è completo e il cliente procede al pagamento, viene visualizzato solo l&#39;indirizzo di spedizione selezionato. Nella pagina viene inoltre visualizzato un messaggio che indica che l&#39;indirizzo di spedizione è bloccato e può essere modificato solo nel preventivo.

![Indirizzo di spedizione bloccato per un preventivo](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Abilita ricerca indirizzo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Checkout Options]** sezione.

   ![Configurazione - Opzioni di pagamento](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedi [Opzioni di pagamento](../configuration-reference/sales/checkout.md#checkout-options) nel _Guida di riferimento alla configurazione_.

1. Imposta **[!UICONTROL Enable Address Search]** a `Yes`.

1. Per specificare la soglia per l&#39;inclusione della funzione di ricerca degli indirizzi, impostare **[!UICONTROL Number of Customer Addresses Limit]** opzione.

   Se necessario, cancellare il **[!UICONTROL Use system value]** per apportare questa modifica.

   Quando il numero di indirizzi salvati del cliente raggiunge o supera questo limite, la pagina visualizza l’indirizzo predefinito (se del caso) o _Nessun indirizzo selezionato_ con _Cambia indirizzo_ opzione. Il limite predefinito è `10`.

1. Clic **[!UICONTROL Save Config]**.
