---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] dell'amministratore di Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

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
