---
title: '[!DNL Google Analytics]'
description: Scopri come utilizzare [!DNL Google Analytics] per raccogliere metriche utili per i siti Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] consente di definire dimensioni e metriche personalizzate aggiuntive per il tracciamento, con supporto per le interazioni offline e con le app mobili e accesso agli aggiornamenti continui. [!DNL Google Analytics] 4 è la soluzione di misurazione di nuova generazione di Google e sta sostituendo [!DNL Universal Analytics]. Il 1° luglio 2023, le proprietà standard di Universal Analytics cesseranno l’elaborazione dei nuovi hit.

>[!NOTE]
>
>Se la tua azienda è soggetta a normative sulla privacy come [Regolamento generale sulla protezione dei dati](../getting-started/compliance-gdpr.md) e/o [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), vedi [Impostazioni privacy Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Se si abilita [Modalità di restrizione cookie](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] non raccoglie dati sui visitatori a meno che non abbiano accettato i cookie.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Passaggio 1: configurazione [!UICONTROL Google Analytics] 4

Se non si dispone già di un [!DNL Google Analytics] 4 impostare il sito, seguire uno dei seguenti metodi:

- [Configurare la raccolta dati di Analytics per la prima volta](https://support.google.com/analytics/answer/9304153)
- [Aggiungere Google Analytics 4 a un sito con [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Passaggio 2: completare la configurazione di Commerce

1. Accedi all’amministratore per il tuo archivio Commerce.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Google API]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Google GTag]** sezione.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Google Analytics4]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable]** a `Yes`.

   - Lascia **[!UICONTROL Account type]** as `Google Analytics4`.

   - Immetti il **[!UICONTROL Measurement ID]**. Per ulteriori informazioni, consulta [Guida di Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Se desideri eseguire test A/B e altri test delle prestazioni sul contenuto, imposta **Esperimenti sui contenuti** a `Yes`.

   ![Configurazione vendite - API Google per Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Il 1° luglio 2023, le proprietà standard di Universal Analytics non elaboreranno più i dati. Se fai ancora affidamento su [!DNL Universal Analytics], si consiglia di: [prepararsi a utilizzare le Google Analytics 4](https://support.google.com/analytics/answer/10759417) avanti.

### Passaggio 1: configurare Google Universal Analytics

Visita il sito Web Google e registrati per [Google Universal Analytics][1] account.

### Passaggio 2: completare la configurazione di Commerce

1. Accedi all’amministratore per il tuo archivio Commerce.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Google API]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Google Analytics]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable]** a `Yes`.

   - Immetti il [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Se desideri eseguire test A/B e altri test delle prestazioni sul contenuto, imposta **[!UICONTROL Content Experiments]** a `Yes`.

   ![Configurazione delle vendite - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## E-commerce avanzato

Ecommerce avanzato è un plug-in per [!DNL Google Universal Analytics] questo ti dà informazioni sul comportamento di acquisto dei tuoi clienti. Puoi utilizzare l’e-commerce avanzato per generare rapporti sulle attività chiave dei clienti, ad esempio quando i clienti aggiungono articoli al carrello, iniziano il processo di pagamento o completano un acquisto. Puoi anche identificare e analizzare i pattern di acquirenti che abbandonano i carrelli senza effettuare un acquisto.

Le seguenti istruzioni mostrano come configurare [!DNL Google Tag Manager] con [!DNL Universal Analytics] produrre report e dati di e-commerce migliorati.

### Passaggio 1: Registrati agli account Google

1. Registrati per un [Gestione tag Google](google-tag-manager.md) e completare la configurazione di Commerce.

1. Registrati per un nuovo [Google Universal Analytics][1] account.

### Passaggio 2: Configurare l’e-commerce avanzato

1. Accedi al tuo account Google Universal Analytics.

1. Crea una proprietà per Analisi e-commerce avanzate con le seguenti impostazioni:

   - Stato: ON
   - Prodotti correlati: ON
   - Abilita reportistica e-commerce avanzata: ON
   - Etichette per il pagamento: (non obbligatorio)

1. Al termine, fai clic su **[!UICONTROL Submit]**.

### Passaggio 3: Creare tag e trigger

1. Accedi al tuo [!DNL Google Tag Manager] e creare i seguenti trigger:

   | Nome | Tipo di evento | Filtro |
   |--- |--- |--- |
   | `addToCart` | Evento personalizzato |  |
   | `checkout` | Evento personalizzato |  |
   | `checkout only` | Visualizzazione pagina | L’URL della pagina corrisponde a RegEx /checkout/.* |
   | `checkoutOption` | Evento personalizzato |  |
   | `gtm.dom` | Evento personalizzato |  |
   | `productClick` | Evento personalizzato |  |
   | `promotionClick` | Evento personalizzato |  |
   | `removeFromCart` | Evento personalizzato |  |

   >[!NOTE]
   >
   >Il [!UICONTROL Checkout] l’evento viene attivato solo per i metodi di pagamento di base incorporati in Commerce (ad esempio `Check / Money Order` e `Cash On Delivery Payment`). Questo evento non viene eseguito per `PayPal checkout` e altri metodi di pagamento esterno, che utilizzano il reindirizzamento alla cassa da risorse esterne.

1. Crea i seguenti tag di Universal Analytics con la stessa configurazione di base.

   - Tag Universal Analytics

     | Nome | Tipo | Attivazione dei trigger |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | pagamento |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Configurazione tag di base

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (ID di tracciamento dall’account Universal Analytics). |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | Vero |
     | [!UICONTROL Use data layer] | Vero |
     | [!UICONTROL Use Debug version] | Vero |

1. Completa le singole configurazioni di tracciamento.

   - Immetti quanto segue **[!UICONTROL Add to Cart]** impostazioni di tracciamento:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Aggiungi al carrello |
     | [!UICONTROL Trigger] | addToCart |

   - Immetti quanto segue **[!UICONTROL Checkout option]** impostazioni di tracciamento:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Opzione Checkout |
     | [!UICONTROL Trigger] | checkoutOption |

   - Immetti quanto segue **[!UICONTROL PageView]** impostazioni di tracciamento:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Completa quanto segue **[!UICONTROL Product Click]** configurazione tracciamento:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Clic prodotto |
     | [!UICONTROL Trigger] | productClick |

   - Completa quanto segue **[!UICONTROL Promotion Click]** configurazione tracciamento:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Clic su promozione |
     | [!UICONTROL Trigger] | promotionClick |

   - Completa quanto segue **[!UICONTROL Remove from Cart]** configurazione tracciamento:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Rimuovi dal carrello |
     | [!UICONTROL Trigger] | removeFromCart |

1. Al termine, fai clic su **[!UICONTROL Preview]** e verificare che i tag funzionino correttamente.

1. Dopo aver verificato le impostazioni, fai clic su **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
