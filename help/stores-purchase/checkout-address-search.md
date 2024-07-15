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

Quando questa funzione è abilitata e il numero di indirizzi salvati del cliente soddisfa o supera il limite configurato, i passaggi _Spedizione_ e _Verifica e pagamenti_ visualizzano un solo indirizzo (impostazione predefinita). Il cliente può cambiare l&#39;indirizzo selezionato facendo clic su **Cambia indirizzo** e quindi cercando l&#39;indirizzo corretto per città, stato, via o CAP. Questa funzione supporta anche la selezione degli indirizzi per l&#39;estrazione del Registro di sistema dei regali.

![Estrazione con indirizzi di spedizione salvati visualizzati](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Se il cliente non ha un indirizzo di spedizione predefinito, nella pagina _Spedizione_ viene visualizzato _Nessun indirizzo selezionato_. In questo caso, il cliente deve fare clic su **Cambia indirizzo** per selezionare un indirizzo salvato oppure fare clic su **Nuovo indirizzo** per aggiungere e selezionare un indirizzo prima di procedere con l&#39;estrazione. Se il cliente non dispone di un indirizzo di fatturazione predefinito, nella pagina _Verifica e pagamenti_ viene visualizzato l&#39;indirizzo selezionato per la spedizione insieme all&#39;opzione _Modifica indirizzo_.

![Estrai senza indirizzo selezionato nel messaggio](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Ricerca di virgolette per indirizzi bloccati

![Adobe Commerce B2B](../assets/b2b.svg) (disponibile solo con Adobe Commerce B2B)

L&#39;abilitazione della ricerca degli indirizzi influisce anche sul pagamento degli ordini creati da preventivi in cui il numero di indirizzi salvati del cliente soddisfa o supera il limite configurato. Quando il preventivo è completo e il cliente procede al pagamento, viene visualizzato solo l&#39;indirizzo di spedizione selezionato. Nella pagina viene inoltre visualizzato un messaggio che indica che l&#39;indirizzo di spedizione è bloccato e può essere modificato solo nel preventivo.

![Indirizzo di spedizione bloccato per un preventivo](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Abilita ricerca indirizzo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Checkout Options]**.

   ![Configurazione - Opzioni di estrazione](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Opzioni di estrazione](../configuration-reference/sales/checkout.md#checkout-options) nella _Guida di riferimento alla configurazione_.

1. Imposta **[!UICONTROL Enable Address Search]** su `Yes`.

1. Per specificare la soglia per l&#39;inclusione della funzionalità di ricerca degli indirizzi, impostare l&#39;opzione **[!UICONTROL Number of Customer Addresses Limit]**.

   Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per apportare questa modifica.

   Quando il numero di indirizzi salvati del cliente raggiunge o supera questo limite, nella pagina viene visualizzato l&#39;indirizzo predefinito (se presente) o _Nessun indirizzo selezionato_ con l&#39;opzione _Cambia indirizzo_. Il limite predefinito è `10`.

1. Fare clic su **[!UICONTROL Save Config]**.
