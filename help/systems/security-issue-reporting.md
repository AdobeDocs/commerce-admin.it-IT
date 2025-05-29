---
title: Segnalazione dei problemi di sicurezza
description: Scopri come configurare le informazioni di contatto e i collegamenti relativi alla sicurezza che possono essere utilizzati dai ricercatori sulla sicurezza per segnalare i problemi di sicurezza relativi al sito.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Segnalazione dei problemi di sicurezza

Il file `security.txt` contiene le informazioni di contatto e i collegamenti relativi alla sicurezza che possono essere utilizzati dai ricercatori sulla sicurezza per segnalare problemi di sicurezza relativi al sito. Se le informazioni di protezione cambiano nel tempo, verificare che le informazioni nel file `security.txt` siano aggiornate.

**_Per configurare security.txt:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL Security]_, fai clic su **[!UICONTROL Security.txt]**.

1. Nella sezione _[!UICONTROL General]_, impostare **[!UICONTROL Enable]**&#x200B;su `Yes`.

   ![Configurazione generale della sicurezza](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. In _[!UICONTROL Contact Information]_&#x200B;immettere quanto segue:

   - L’indirizzo e-mail e il numero di telefono della persona che gestisce i problemi di sicurezza per il tuo negozio.

   - URL di **[!UICONTROL Contact Page]** dell&#39;archivio. Questa pagina può essere un elenco di contatti per la sicurezza dello store o la pagina _Contattaci_.

   ![Configurazione informazioni di contatto](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. In _[!UICONTROL Other Information]_&#x200B;immettere quanto segue:

   - URL della chiave **[!UICONTROL Encryption]** pubblica. Esempio: `https://example.com/pgp-key.txt`

   - L&#39;URL di una pagina **[!UICONTROL Acknowledgments]** in cui i ricercatori della sicurezza sono riconosciuti per le loro attività per conto del tuo archivio.

   - **[!UICONTROL Preferred Languages]** per le comunicazioni relative alla sicurezza. Immetti il [codice lingua](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard di due caratteri per ogni lingua supportata, separati da una virgola. Ad esempio, per specificare inglese, spagnolo e francese, immettere `en, es, fr`. Tutte le lingue specificate hanno la stessa priorità, indipendentemente dall&#39;ordine di visualizzazione.

   - L&#39;URL di una pagina **[!UICONTROL Hiring]** in cui sono elencate le opportunità di lavoro relative alla sicurezza nel tuo store.

   - URL della pagina **[!UICONTROL Policy]** di protezione.

   - URL di un file **[!UICONTROL Signature]** digitale salvato sul server. Esempio: `https://mystore.com/.well-known/security.txt.sig`

   La firma digitale deve essere impostata dall&#39;interfaccia CLI (Command-Line Interface) del server. Per ulteriori informazioni, consulta [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) su GitHub.

   ![Altre informazioni](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
