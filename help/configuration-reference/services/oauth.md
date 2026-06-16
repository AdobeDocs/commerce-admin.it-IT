---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Services] > [!UICONTROL OAuth] dell'amministratore di Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Scadenza token di accesso](./assets/oauth-token-expire.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Globale | Determina il periodo di tempo, in ore, prima della scadenza di un token API del cliente. Il token cliente non scade mai se il campo è vuoto. Valore predefinito: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Globale | Determina il periodo di tempo, in ore, prima della scadenza di un token API amministratore. Il token di amministrazione non scade mai se il campo è vuoto. Valore predefinito: `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>Gli algoritmi di crittografia e durata del token API Bearer e dell&#39;amministratore sono controllati dalle impostazioni di configurazione [JWT Authentication](magento-web-api.md#jwt-authentication).

## [!UICONTROL Cleanup Settings]

![Impostazioni pulizia](./assets/oauth-cleanup.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Globale | Specifica il numero di richieste OAuth prima dell&#39;avvio della pulizia. Non immettere `0` per disabilitare la pulizia. |
| [!UICONTROL Enable WSDL Cache] | Globale | Determina la durata delle voci in minuti, prima che vengano pulite. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Impostazioni consumer](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Globale | Specifica il numero di secondi richiesti per il timeout del sistema quando i clienti pubblicano le proprie credenziali. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Globale | Specifica il numero massimo di reindirizzamenti correlati a una pubblicazione di credenziali consumer. |
| [!UICONTROL Expiration Period] | Globale | Determina quanti secondi prima della scadenza di una chiave/segreto inutilizzata dopo l’inizio dello scambio di token OAuth. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Blocchi di autenticazione](./assets/oauth-locks.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Globale | Specifica il numero massimo di errori di autenticazione per bloccare l&#39;account. |
| [!UICONTROL Lockout Time (seconds)] | Globale | Specifica il periodo di tempo in secondi dopo il quale l&#39;account viene sbloccato. |

{style="table-layout:auto"}
