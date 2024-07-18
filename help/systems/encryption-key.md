---
title: Chiave di crittografia
description: Scopri come generare automaticamente o aggiungere la tua chiave di crittografia, che deve essere modificata regolarmente per migliorare la sicurezza.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 2469b3853d074f7a7adfe822b645e41d1420259a
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Chiave di crittografia

Adobe Commerce e il Magento Open Source utilizzano una chiave di crittografia per proteggere le password e altri dati sensibili. Viene utilizzato un algoritmo [!DNL ChaCha20-Poly1305] standard del settore con una chiave a 256 bit per crittografare tutti i dati che richiedono la crittografia. Ciò include i dati della carta di credito e le password di integrazione (modulo di pagamento e spedizione). Inoltre, viene utilizzato un forte algoritmo di hash sicuro (SHA-256) per eseguire l’hashing di tutti i dati che non richiedono decrittografia.

Durante l&#39;installazione iniziale, viene richiesto di consentire a Commerce di generare una chiave di crittografia o di immetterne una propria. Lo strumento per la chiave di crittografia consente di modificare la chiave in base alle esigenze. La chiave di crittografia deve essere cambiata regolarmente per migliorare la sicurezza e in qualsiasi momento la chiave originale potrebbe essere compromessa. Ogni volta che la chiave viene modificata, tutti i dati legacy vengono codificati nuovamente utilizzando la nuova chiave.

Per informazioni tecniche, vedere [Installazione locale avanzata](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) nella _Guida all&#39;installazione_.

>[!IMPORTANT]
>
>Prima di seguire queste istruzioni per modificare la chiave di crittografia, verificare che il file seguente sia scrivibile: `[your store]/app/etc/env.php`

**Per modificare una chiave di crittografia:**

Le seguenti istruzioni richiedono l&#39;accesso a un terminale.

1. Attiva [modalità manutenzione](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

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

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Chiave di crittografia del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Effettuare una delle seguenti operazioni:

   - Per generare una nuova chiave, impostare **[!UICONTROL Auto-generate Key]** su `Yes`.
   - Per utilizzare una chiave diversa, impostare **[!UICONTROL Auto-generate Key]** su `No`. Quindi nel campo **[!UICONTROL New Key]**, immettere o incollare la chiave che si desidera utilizzare.

1. Fare clic su **[!UICONTROL Change Encryption Key]**.

   >[!NOTE]
   >
   >Conserva un record della nuova chiave in un luogo sicuro. È necessario per decrittografare i dati, se si verificano problemi con i file.

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
