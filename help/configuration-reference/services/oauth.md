---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Services] &gt; [!UICONTROL OAuth] pagina dell’amministratore di Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Scadenza token di accesso](./assets/oauth-token-expire.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Globale | Determina il periodo di tempo, in ore, prima della scadenza di un token API del cliente. Il token cliente non scade mai se il campo è vuoto. Valore predefinito: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Globale | Determina il periodo di tempo, in ore, prima della scadenza di un token API amministratore. Il token di amministrazione non scade mai se il campo è vuoto. Valore predefinito: `4` |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>Gli algoritmi di crittografia e durata dei token API Bearer e admin sono controllati da [Autenticazione JWT](magento-web-api.md#jwt-authentication) impostazioni di configurazione.

## [!UICONTROL Cleanup Settings]

![Impostazioni pulizia](./assets/oauth-cleanup.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Globale | Specifica il numero di richieste OAuth prima dell&#39;avvio della pulizia. Non inserire `0` per disattivare la pulizia. |
| [!UICONTROL Enable WSDL Cache] | Globale | Determina la durata delle voci in minuti, prima che vengano pulite. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Consumer Settings]

![Impostazioni consumer](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Globale | Specifica il numero di secondi richiesti per il timeout del sistema quando i clienti pubblicano le proprie credenziali. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Globale | Specifica il numero massimo di reindirizzamenti correlati a una pubblicazione di credenziali consumer. |
| [!UICONTROL Expiration Period] | Globale | Determina quanti secondi prima della scadenza di una chiave/segreto inutilizzata dopo l’inizio dello scambio di token OAuth. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authentication Locks]

![Blocchi di autenticazione](./assets/oauth-locks.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Globale | Specifica il numero massimo di errori di autenticazione per bloccare l&#39;account. |
| [!UICONTROL Lockout Time (seconds)] | Globale | Specifica il periodo di tempo in secondi dopo il quale l&#39;account viene sbloccato. |

{:style=&quot;table-layout:auto&quot;}
