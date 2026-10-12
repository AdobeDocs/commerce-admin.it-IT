---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] > [!UICONTROL 3D Secure] dell'amministratore di Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: 'https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 3dcbfa9e-51f8-569c-a0e4-7f59098f730f
    internal-label: Payments
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 5%
---
# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] è stato sviluppato da [!DNL Visa] per promuovere transazioni online sicure. Esempi di [!DNL 3-D Secure] soluzioni create da reti con schede sono verificate da [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] e [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] è un leader globale nell&#39;autenticazione delle transazioni digitali e una consociata interamente controllata da [!DNL Visa].

[!DNL 3-D Secure] versione 2.0 supporta numerosi miglioramenti, tra cui metodi di autenticazione e flusso di autenticazione avanzati e una migliore condivisione dei dati tra esercente ed emittente.

>[!NOTE]
>
>Il gateway di pagamento [Braintree](../../stores-purchase/braintree.md) supporta anche la verifica [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Environment] | Sito Web | Indica la modalità operativa dell&#39;account [!DNL CardinalCommerce]. Se l’esecuzione avviene in un ambiente di test, scegli &quot;Sandbox&quot;. Opzioni: Sandbox / Produzione (predefinito) |
| [!UICONTROL Org Unit ID] | Sito Web | L&#39;ID dell&#39;unità organizzativa dall&#39;account esercente [!DNL CardinalCommerce]. |
| [!UICONTROL API Key] | Sito Web | La chiave API dal tuo account esercente [!DNL CardinalCommerce]. |
| [!UICONTROL API Identifier] | Sito Web | L&#39;identificatore API dell&#39;account esercente [!DNL CardinalCommerce]. |
| [!UICONTROL Debug] | Sito Web | Opzioni: `Yes` / `No` |

{style="table-layout:auto"}
