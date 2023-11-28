---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] pagina dell’amministratore di Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] è stato sviluppato da [!DNL Visa] promuovere transazioni online sicure. Esempi di [!DNL 3-D Secure] le soluzioni create dalle reti di carte sono verificate da [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey], e [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] è leader globale nell’autenticazione delle transazioni digitali ed è interamente controllata da [!DNL Visa].

[!DNL 3-D Secure] La versione 2.0 supporta numerosi miglioramenti, tra cui metodi di autenticazione e flusso di autenticazione avanzati e una migliore condivisione dei dati tra esercente ed emittente.

>[!NOTE]
>
>Il [Braintree](../../stores-purchase/braintree.md) il gateway di pagamento supporta anche [!DNL 3-D Secure] verifica.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Environment] | Sito Web | Indica la modalità operativa del [!DNL CardinalCommerce] account. Se l’esecuzione avviene in un ambiente di test, scegli &quot;Sandbox&quot;. Opzioni: Sandbox / Produzione (predefinito) |
| [!UICONTROL Org Unit ID] | Sito Web | L&#39;ID dell&#39;unità organizzativa dal tuo [!DNL CardinalCommerce] account esercente. |
| [!UICONTROL API Key] | Sito Web | La chiave API dal tuo [!DNL CardinalCommerce] account esercente. |
| [!UICONTROL API Identifier] | Sito Web | L’identificatore API dal tuo [!DNL CardinalCommerce] account esercente. |
| [!UICONTROL Debug] | Sito Web | Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
