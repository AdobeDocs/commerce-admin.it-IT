---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Security] &gt; [!UICONTROL Security.txt] pagina dell’amministratore di Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Per ulteriori informazioni sulla modifica di queste impostazioni di configurazione, vedi [Segnalazione dei problemi di sicurezza](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Generale](./assets/txt-general.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable] | Sito Web | Quando è attivata, `security.txt` il file viene salvato e contiene le informazioni necessarie ai ricercatori di sicurezza per segnalare potenziali vulnerabilità. Opzioni:<br />**`Yes`**- Crea il `security.txt` file in base alle informazioni immesse nel _Informazioni di contatto_ e _Altre informazioni_ sezioni.<br />**`No`** - (impostazione predefinita) Non crea il `security.txt` file. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Contact information]

![Informazioni di contatto](./assets/txt-contact-info.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Email] | Sito Web | L’indirizzo e-mail a cui possono essere inviati i rapporti sulla sicurezza. |
| [!UICONTROL Phone] | Sito Web | Numero di telefono che può essere utilizzato per segnalare problemi di sicurezza. |
| [!UICONTROL Contact Page] | Sito Web | URL di una pagina del sito in cui sono elencati i contatti di protezione o _Contattaci_ pagina. Esempi: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Other information]

![Altre informazioni](./assets/txt-other-info.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Encryption] | Sito Web | URL che punta alla posizione di una chiave di crittografia che i ricercatori della sicurezza possono utilizzare per inviare comunicazioni crittografate. _**Non immettere la chiave di crittografia in questo campo.**_ <br/><br/>È responsabilità del ricercatore verificare che la chiave provenga da una fonte affidabile. I ricercatori non devono presumere che la chiave sia la stessa utilizzata per generare la firma digitale. Esempio:<br />Chiave OpenPGP dal server web - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Sito Web | URL che punta a una pagina del tuo negozio in cui vengono riconosciuti i ricercatori di sicurezza, ad esempio`https://mystore.com/hall-of-fame.html`. Per prevenire attacchi futuri, includi solo una descrizione generale senza rivelare informazioni specifiche sui problemi di vulnerabilità. Esempio:<br />Ringraziamo i seguenti ricercatori:<br />(aaaa/mm/gg) Justin Thyme - SQL injection |
| [!UICONTROL Preferred Languages] | Sito Web | Specifica almeno una lingua preferita per i rapporti sulla sicurezza. Separa più caratteri a due caratteri [codici di lingua](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) con una virgola. Tutte le lingue specificate hanno la stessa priorità. Ad esempio, per specificare inglese, spagnolo e francese, immetti `en, es, fr`. |
| [!UICONTROL Hiring] | Sito Web | URL di una pagina del sito in cui sono elencate le posizioni lavorative relative alla sicurezza. Esempio: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Sito Web | URL della pagina che descrive i criteri di sicurezza e le procedure di reporting sulle vulnerabilità. Esempio: `https://mystore.com/security-reporting.html` Predefinito: `https://mystore.com/security` |
| [!UICONTROL Signature] | Sito Web | Collegamento al file della firma digitale. La firma digitale deve essere generata dalla riga di comando e viene salvata in `.well-known` sul server. Per ulteriori informazioni, consulta [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) su GitHub. Esempio: `https://mystore.com/.well-known/security.txt.sig` |

{:style=&quot;table-layout:auto&quot;}
