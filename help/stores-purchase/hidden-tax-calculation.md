---
title: Calcolo imposte nascoste
description: Scopri come configurare un calcolo delle imposte nascoste quando è presente uno sconto con imposte incorporate.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
TQID: https://experienceleague.adobe.com/KkluEZ6WopfZzfFvnd0XA93av21JP0mxXBS4A4czvA0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 1%

---

# Calcolo imposte nascoste

_Tassa nascosta_ è l&#39;importo dell&#39;IVA di un importo di sconto. È diverso da zero quando tutte queste condizioni sono vere:

- I prezzi del catalogo includono le imposte
- L&#39;aliquota IVA non è zero
- È presente uno sconto

Quando è presente uno sconto con imposta incorporata, Commerce calcola una _imposta nascosta_ che viene aggiunta nuovamente per calcolare il prezzo scontato.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Esempio

1. Prezzo intero dell&#39;articolo, IVA inclusa: $100
1. IVA al: 20%
1. Sconto del 10% applicato al prezzo dell&#39;articolo, escluse le imposte:

### Risultato previsto non valido

- Prezzo articolo al netto delle imposte senza sconto=100 USD
- Prezzo dell&#39;articolo al lordo delle imposte senza sconto=100/1,2=83,33 USD
- Sconto=83,33 \ *0,1=8,33 USD
- Imposta=(83,33-8,33) \ *0,2=**15 USD (non valido)**
- Totale ordine IVA esclusa=83,33-8,33=**75 USD (non valido)**
- Totale ordine comprensivo di imposta=75+15=**90 USD (non valido)**

### Risultato effettivo valido nel carrello

![Calcolo imposte nascoste nel carrello](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Calcoli validi

1. Il prezzo completo dell&#39;articolo senza imposte è: $100 / 1,2 = **$83,33**

1. Importo IVA sul prezzo intero dell&#39;articolo: $100 - $83,33 = $16,67

   _Può essere calcolato anche come: $100 \ * (1 - 1/1.2)._

1. Lo sconto del 10% su $83,33 è: **$8,33** (quando non si applica lo sconto sulle imposte)

1. Il prezzo scontato dell&#39;articolo con imposta è: $100 - $8,33 = $91,67

   >[!NOTE]
   >
   >Questa equazione illustra la percezione del cliente su come vengono applicati gli sconti.

1. Il prezzo scontato dell&#39;articolo senza imposte è: $91,67 / 1,2 = $76,39

1. Importo IVA sul prezzo scontato: $91,67 - $76,39 = **$15,28 (valido)**

   _Può essere calcolato anche come: $91,67 \ * (1 - 1/1,2)._

1. Imposta nascosta o _Compensazione imposta sconto_ è la differenza tra l&#39;importo IVA del prezzo completo e il prezzo scontato: $16,67 - $15,28 = **$1,39**

   _Un altro modo per vederlo: l&#39;imposta nascosta è l&#39;importo IVA riportato nello sconto di $8,33 \* (1 - 1/1,2)._

1. Comprensione abituale da parte del cliente del prezzo scontato (totale ordine):

   _Prezzo intero dell&#39;articolo comprese le imposte **meno**&#x200B;l&#39;importo dello sconto: $100 - $8,33 = $91,67_

1. **Modalità di calcolo del prezzo scontato in Commerce** (vedere la formula precedente):

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
