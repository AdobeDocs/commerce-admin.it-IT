---
title: '[!DNL Google Analytics]'
description: Scopri come utilizzare  [!DNL Google Analytics] per raccogliere metriche utili per i siti Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/3YXwPB-1yDciblELQDGHXfnv1hwPJAW4Us0iG6vCf0k
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 766
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] consente di definire dimensioni e metriche personalizzate aggiuntive per il tracciamento, con il supporto per le interazioni offline e dell&#39;app mobile e l&#39;accesso agli aggiornamenti in corso. [!DNL Google Analytics] 4 è la soluzione di misurazione di nuova generazione di Google e sostituisce [!DNL Universal Analytics]. Il 1° luglio 2023, le proprietà standard di Universal Analytics cesseranno l’elaborazione dei nuovi hit.

>[!NOTE]
>
>Se la tua azienda è soggetta alle normative sulla privacy come il [Regolamento generale sulla protezione dei dati](../getting-started/compliance-gdpr.md) e/o il [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), consulta [Impostazioni sulla privacy di Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Se si attiva la [Modalità di restrizione cookie](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] non raccoglie dati sui visitatori a meno che non abbiano accettato i cookie.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Passaggio 1: configurare [!UICONTROL Google Analytics] 4

Se non si dispone già di una configurazione di [!DNL Google Analytics] 4 per il sito, seguire uno dei metodi seguenti:

- [Configurare la raccolta dati di Analytics per la prima volta](https://support.google.com/analytics/answer/9304153)
- [Aggiungi Google Analytics 4 a un sito con  [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Passaggio 2: completare la configurazione di Commerce

1. Accedi all’amministratore per il tuo archivio Commerce.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Google API]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Google GTag]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sottosezione **[!UICONTROL Google Analytics4]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable]** su `Yes`.

   - Lascia **[!UICONTROL Account type]** come `Google Analytics4`.

   - Immetti **[!UICONTROL Measurement ID]**. Per ulteriori informazioni, vedere [Guida di Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Se desideri eseguire test A/B e altri test delle prestazioni sul contenuto, imposta **Esperimenti contenuto** su `Yes`.

   ![Configurazione vendite - API Google per Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Il 1° luglio 2023, le proprietà standard di Universal Analytics non elaboreranno più i dati. Se utilizzi ancora [!DNL Universal Analytics], ti consigliamo di [prepararti a utilizzare Google Analytics 4](https://support.google.com/analytics/answer/10759417) in futuro.

### Passaggio 1: configurare Google Universal Analytics

Visita il sito Web Google e registrati per un account [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en).

### Passaggio 2: completare la configurazione di Commerce

1. Accedi all’amministratore per il tuo archivio Commerce.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Google API]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Google Analytics]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable]** su `Yes`.

   - Immetti [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Per eseguire test A/B e altri test delle prestazioni sul contenuto, impostare **[!UICONTROL Content Experiments]** su `Yes`.

   ![Configurazione vendite - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## E-commerce avanzato

L&#39;e-commerce avanzato è un plug-in per [!DNL Google Universal Analytics] che ti permette di conoscere il comportamento di acquisto dei tuoi clienti in insight. Puoi utilizzare l’e-commerce avanzato per generare rapporti sulle attività chiave dei clienti, ad esempio quando i clienti aggiungono articoli al carrello, iniziano il processo di pagamento o completano un acquisto. Puoi anche identificare e analizzare i pattern di acquirenti che abbandonano i carrelli senza effettuare un acquisto.

Nelle istruzioni seguenti viene illustrato come configurare [!DNL Google Tag Manager] con [!DNL Universal Analytics] per la produzione di report e dati di e-commerce avanzati.

### Passaggio 1: Registrati agli account Google

1. Registrati a un account [Google Tag Manager](google-tag-manager.md) e completa la configurazione di Commerce.

1. Registrati per un nuovo account [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en).

### Passaggio 2: Configurare l’e-commerce avanzato

1. Accedi al tuo account Google Universal Analytics.

1. Crea una proprietà per Analisi e-commerce avanzate con le seguenti impostazioni:

   - Stato: ON
   - Prodotti correlati: ON
   - Abilita reportistica e-commerce avanzata: ON
   - Etichette per il pagamento: (non obbligatorio)

1. Al termine, fare clic su **[!UICONTROL Submit]**.

### Passaggio 3: Creare tag e trigger

1. Accedi al tuo account [!DNL Google Tag Manager] e crea i seguenti trigger:

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
   >L&#39;evento [!UICONTROL Checkout] viene attivato solo per i metodi di pagamento di base incorporati di Commerce (ad esempio `Check / Money Order` e `Cash On Delivery Payment`). Questo evento non viene eseguito per `PayPal checkout` e altri metodi di pagamento esterni che utilizzano il reindirizzamento all&#39;estrazione da risorse esterne.

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

   - Immetti le seguenti impostazioni di tracciamento **[!UICONTROL Add to Cart]**:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Aggiungi al carrello |
     | [!UICONTROL Trigger] | addToCart |

   - Immetti le seguenti impostazioni di tracciamento **[!UICONTROL Checkout option]**:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Opzione Checkout |
     | [!UICONTROL Trigger] | checkoutOption |

   - Immetti le seguenti impostazioni di tracciamento **[!UICONTROL PageView]**:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Completa la seguente configurazione di tracciamento **[!UICONTROL Product Click]**:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Clic prodotto |
     | [!UICONTROL Trigger] | productClick |

   - Completa la seguente configurazione di tracciamento **[!UICONTROL Promotion Click]**:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Clic su promozione |
     | [!UICONTROL Trigger] | promotionClick |

   - Completa la seguente configurazione di tracciamento **[!UICONTROL Remove from Cart]**:

     | Impostazione | Valore |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | E-commerce |
     | [!UICONTROL Action] | Rimuovi dal carrello |
     | [!UICONTROL Trigger] | removeFromCart |

1. Al termine, fare clic su **[!UICONTROL Preview]** e verificare che i tag funzionino correttamente.

1. Dopo aver verificato le impostazioni, fare clic su **[!UICONTROL Publish]**.
