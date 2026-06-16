---
title: '[!UICONTROL Security] > [!UICONTROL Security.txt]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Security] > [!UICONTROL Security.txt] dell'amministratore di Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Per ulteriori informazioni sulla modifica di queste impostazioni di configurazione, vedere [Segnalazione dei problemi di sicurezza](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Generale](./assets/txt-general.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable] | Sito Web | Quando questa opzione è attivata, viene salvato un file `security.txt` contenente le informazioni necessarie ai ricercatori di sicurezza per segnalare potenziali vulnerabilità. Opzioni:<br />**`Yes`**- Crea il file `security.txt` in base alle informazioni immesse nelle sezioni _Informazioni di contatto_ e _Altre informazioni_.<br />**`No`** - (impostazione predefinita) Non crea il file `security.txt`. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Informazioni di contatto](./assets/txt-contact-info.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Email] | Sito Web | L’indirizzo e-mail a cui possono essere inviati i rapporti sulla sicurezza. |
| [!UICONTROL Phone] | Sito Web | Numero di telefono che può essere utilizzato per segnalare problemi di sicurezza. |
| [!UICONTROL Contact Page] | Sito Web | L&#39;URL di una pagina del sito in cui sono elencati i contatti di sicurezza o la pagina _Contattaci_. Esempi: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Altre informazioni](./assets/txt-other-info.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Encryption] | Sito Web | URL che punta alla posizione di una chiave di crittografia che i ricercatori della sicurezza possono utilizzare per inviare comunicazioni crittografate. _**Non immettere la chiave di crittografia in questo campo.**_ <br/><br/>È responsabilità del ricercatore verificare che la chiave provenga da una fonte attendibile. I ricercatori non devono presumere che la chiave sia la stessa utilizzata per generare la firma digitale. Esempio:<br />Chiave OpenPGP dal server Web - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Sito Web | URL che punta a una pagina dell&#39;archivio in cui vengono riconosciuti i ricercatori di sicurezza, ad esempio `https://mystore.com/hall-of-fame.html`. Per prevenire attacchi futuri, includi solo una descrizione generale senza rivelare informazioni specifiche sui problemi di vulnerabilità. Esempio:<br />Ringraziamo i seguenti ricercatori:<br />(aaaa/mm/gg) Justin Thyme - SQL injection |
| [!UICONTROL Preferred Languages] | Sito Web | Specifica almeno una lingua preferita per i rapporti sulla sicurezza. Separa più [codici di lingua](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) di due caratteri con una virgola. Tutte le lingue specificate hanno la stessa priorità. Ad esempio, per specificare inglese, spagnolo e francese, immettere `en, es, fr`. |
| [!UICONTROL Hiring] | Sito Web | URL di una pagina del sito in cui sono elencate le posizioni lavorative relative alla sicurezza. Esempio: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Sito Web | URL della pagina che descrive i criteri di sicurezza e le procedure di reporting sulle vulnerabilità. Esempio: `https://mystore.com/security-reporting.html` Predefinito: `https://mystore.com/security` |
| [!UICONTROL Signature] | Sito Web | Collegamento al file della firma digitale. La firma digitale deve essere generata dalla riga di comando e viene salvata nella cartella `.well-known` sul server. Per ulteriori informazioni, vedere [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) su GitHub. Esempio: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
