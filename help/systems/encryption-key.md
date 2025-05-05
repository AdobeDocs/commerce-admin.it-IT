---
title: Chiave di crittografia
description: Scopri come modificare la tua chiave di crittografia, operazione che deve essere eseguita regolarmente per migliorare la sicurezza.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Chiave di crittografia

>[!NOTE]
>
>Se si è tentato di completare questi passaggi e si sono verificati dei problemi, vedere l&#39;articolo della Knowledge Base [Risoluzione dei problemi relativi alla rotazione della chiave di crittografia: CVE-2024-34102](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102).

Adobe Commerce e Magento Open Source utilizzano una chiave di crittografia per proteggere le password e altri dati sensibili. Viene utilizzato un algoritmo [!DNL ChaCha20-Poly1305] standard del settore con una chiave a 256 bit per crittografare tutti i dati che richiedono la crittografia. Ciò include i dati della carta di credito e le password di integrazione (modulo di pagamento e spedizione). Inoltre, viene utilizzato un forte algoritmo di hash sicuro (SHA-256) per eseguire l’hashing di tutti i dati che non richiedono decrittografia.

Durante l&#39;installazione iniziale, viene richiesto di consentire a Commerce di generare una chiave di crittografia o di immetterne una propria. Lo strumento per la chiave di crittografia consente di modificare la chiave in base alle esigenze. La chiave di crittografia deve essere cambiata regolarmente per migliorare la sicurezza e in qualsiasi momento la chiave originale potrebbe essere compromessa.

Per informazioni tecniche, vedere [Installazione locale avanzata](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=it) nella _Guida all&#39;installazione_ e [Nuova crittografia dei dati](https://developer.adobe.com/commerce/php/development/security/data-encryption/) nella _Guida per gli sviluppatori PHP_.

>[!IMPORTANT]
>
>- Prima di seguire queste istruzioni per modificare la chiave di crittografia, verificare che il file seguente sia scrivibile: `[your store]/app/etc/env.php`
>- La funzione di modifica della chiave di crittografia nelle impostazioni dell’amministratore è obsoleta ed è stata rimossa nella versione 2.4.8. È necessario utilizzare il comando CLI descritto in questa pagina per modificare la chiave di crittografia dopo l&#39;aggiornamento alla versione 2.4.8.

**Per modificare una chiave di crittografia:**

Le seguenti istruzioni richiedono l&#39;accesso a un terminale.

1. Attiva [modalità manutenzione](https://experienceleague.adobe.com/it/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Disattiva processi cron.

   _Progetti infrastruttura cloud:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Progetti locali_

   ```bash
   crontab -e
   ```

1. Modificare la chiave di crittografia utilizzando uno dei metodi seguenti.

   +++Comando CLI

   Eseguire il seguente comando CLI e assicurarsi che venga completato senza errori. Se devi crittografare di nuovo alcuni valori di configurazione del sistema o campi di pagamento, consulta la [guida dettagliata sulla ri-crittografia](https://developer.adobe.com/commerce/php/development/security/data-encryption/) nella _Guida per lo sviluppo di PHP_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Impostazioni amministratore

   >[!IMPORTANT]
   >
   >Questa funzione è diventata obsoleta ed è stata rimossa nella versione 2.4.8. Adobe consiglia di modificare le chiavi di crittografia con CLI.

   1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Chiave di crittografia del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Effettuare una delle seguenti operazioni:

      - Per generare una nuova chiave, impostare **[!UICONTROL Auto-generate Key]** su `Yes`.
      - Per utilizzare una chiave diversa, impostare **[!UICONTROL Auto-generate Key]** su `No`. Quindi nel campo **[!UICONTROL New Key]**, immettere o incollare la chiave che si desidera utilizzare.

   1. Fare clic su **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Conserva un record della nuova chiave in un luogo sicuro. È necessario per decrittografare i dati, se si verificano problemi con i file.

   +++

1. Svuota la cache.

   _Progetti infrastruttura cloud:_

   ```bash
   magento-cloud cc
   ```

   _Progetti locali:_

   ```bash
   bin/magento cache:flush
   ```

1. Abilita processi cron.

   _Progetti infrastruttura cloud:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Progetti locali:_

   ```bash
   crontab -e
   ```

1. Disattiva la modalità di manutenzione.

   ```bash
   bin/magento maintenance:disable
   ```
