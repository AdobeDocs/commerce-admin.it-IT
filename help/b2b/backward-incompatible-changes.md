---
title: Modifiche Adobe Commerce B2B non compatibili con le versioni precedenti
description: Scopri le modifiche nelle versioni B2B di Adobe Commerce che potrebbero richiedere l’aggiornamento del codice personalizzato.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Modifiche Adobe Commerce B2B non compatibili con le versioni precedenti

Rivedi le informazioni di riferimento di alto livello per tutte le modifiche non compatibili con le versioni precedenti in B2B per le versioni di Adobe Commerce. Consulta la sezione Elementi di rilievo per informazioni sulle modifiche non compatibili che hanno un impatto notevole e richiedono una spiegazione dettagliata e istruzioni speciali.

## In evidenza

### Da 1.4.2 a 1.5.0

Con l&#39;aggiunta dell&#39;assegnazione multisocietà, gli account utente della società possono ora avere più valori `company_id`. `Magento\Company\Api\Data\CompanyCustomerInterface` è stato aggiornato per impostare `company_id` predefinito per un utente. Il valore predefinito è impostato sulla prima società assegnata all&#39;account utente della società.

Se si esegue l&#39;aggiornamento da una versione precedente, Adobe consiglia di implementare i metodi seguenti nelle classi che utilizzano `Magento\Company\Api\Data\CompanyCustomerInterface`.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Riferimento

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
