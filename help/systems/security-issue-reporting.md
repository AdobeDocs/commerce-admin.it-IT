---
title: Segnalazione dei problemi di sicurezza
description: Scopri come configurare le informazioni di contatto e i collegamenti relativi alla sicurezza che possono essere utilizzati dai ricercatori sulla sicurezza per segnalare i problemi di sicurezza relativi al sito.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# Segnalazione dei problemi di sicurezza

Il `security.txt` Il file contiene informazioni di contatto e collegamenti relativi alla sicurezza che possono essere utilizzati dai ricercatori sulla sicurezza per segnalare problemi di sicurezza relativi al sito. Se le informazioni di protezione cambiano nel tempo, verificare che le informazioni in `security.txt` il file è aggiornato.

**_Per configurare security.txt:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL Security]_, fai clic su **[!UICONTROL Security.txt]**.

1. In _[!UICONTROL General]_sezione, set **[!UICONTROL Enable]**a `Yes`.

   ![Configurazione generale della sicurezza](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Sotto _[!UICONTROL Contact Information]_, immetti quanto segue:

   - L’indirizzo e-mail e il numero di telefono della persona che gestisce i problemi di sicurezza per il tuo negozio.

   - L’URL del sito del Negozio **[!UICONTROL Contact Page]**. Questa pagina può essere un elenco di contatti per la sicurezza dello store oppure _Contattaci_ pagina.

   ![Configurazione delle informazioni di contatto](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Sotto _[!UICONTROL Other Information]_, immetti quanto segue:

   - URL del file pubblico **[!UICONTROL Encryption]** chiave. Ad esempio: `https://example.com/pgp-key.txt`

   - URL di un **[!UICONTROL Acknowledgments]** pagina in cui i ricercatori della sicurezza sono riconosciuti per i loro sforzi per conto del vostro negozio.

   - Il tuo **[!UICONTROL Preferred Languages]** per le comunicazioni relative alla sicurezza. Inserisci i due caratteri standard [codice lingua](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) per ogni lingua supportata, separata da una virgola. Ad esempio, per specificare inglese, spagnolo e francese, immetti `en, es, fr`. Tutte le lingue specificate hanno la stessa priorità, indipendentemente dall&#39;ordine di visualizzazione.

   - L’URL di un **[!UICONTROL Hiring]** pagina che elenca le opportunità di lavoro correlate alla sicurezza con il tuo store.

   - L’URL della tua sicurezza **[!UICONTROL Policy]** pagina.

   - URL di un file digitale **[!UICONTROL Signature]** file salvato sul server. Ad esempio: `https://mystore.com/.well-known/security.txt.sig`

   La firma digitale deve essere impostata dall&#39;interfaccia CLI (Command-Line Interface) del server. Per ulteriori informazioni, consulta [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) su GitHub.

   ![Altre informazioni](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
