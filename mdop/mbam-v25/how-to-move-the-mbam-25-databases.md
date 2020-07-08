---
title: Come spostare i database di MBAM 2.5
description: Come spostare i database di MBAM 2.5
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804198"
---
# Come spostare i database di MBAM 2.5

Usare queste procedure per trasferire i database seguenti da un computer a un altro; dal server a al server B, ad esempio:

-   Database di conformità e controllo

-   Database di ripristino

>[!NOTE]
>È importante che i database vengano ripristinati nel computer B prima di eseguire la configurazione guidata di MBAM per aggiornarli/configurarli.

Se i database non sono presenti, la configurazione guidata crea nuovi database vuoti. Quando i database esistenti vengono ripristinati, questo processo interrompe la configurazione di MBAM.

Ripristinare prima i database, quindi eseguire la configurazione guidata di MBAM, scegliere l'opzione database e la configurazione guidata verrà "connessa" ai database ripristinati. aggiornarli, se necessario, come parte del processo.

**Se si stanno spostando più funzionalità, spostarle nell'ordine seguente:**

1.  Database di ripristino

2.  Database di conformità e controllo

3.  Rapporti

4.  Sito Web di amministrazione e monitoraggio

5.  Portale self-service

>[!Note]
>Per eseguire gli script di Windows PowerShell di esempio forniti in questo argomento, è necessario aggiornare i criteri di esecuzione di Windows PowerShell per consentire l'esecuzione di script. Per istruzioni, vedere [eseguire script di Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .

## Trasferire il database di ripristino

I passaggi di alto livello per lo spostamento del database di ripristino sono i seguenti:

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

2.  Eseguire il backup del database di ripristino nel server A

3.  Trasferire il database di ripristino dal server a al server B

4.  Ripristinare il database di ripristino nel server B

5.  Configurare l'accesso al database nel server B e aggiornare i dati di connessione

6.  Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B

7.  Riprendere l'istanza del sito Web di amministrazione e monitoraggio

### Come si trasferisce il database di ripristino

**Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.** In ogni server che sta usando il sito Web di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di amministrazione e monitoraggio.

Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Per eseguire questo comando, è necessario aggiungere il modulo Internet Information Services (IIS) per Windows PowerShell all'istanza corrente di Windows PowerShell.

### Eseguire il backup del database di ripristino nel server A

1.  Usare l'attività di **backup** in SQL Server Management Studio per eseguire il backup del database di ripristino nel server a.  Per impostazione predefinita, il nome del database è il **database di ripristino MBAM**.

2.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente e modificare il database di ripristino di MBAM per usare la modalità di recupero completo:

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

3.  Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente:

    **$Password $** -password che si usa per crittografare il file della chiave privata.

4.  In Windows PowerShell eseguire lo script archiviato nel file e simile al seguente:

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente:

    **$ServerName $ \ $SqlInstanceName $** -nome del server e istanza da cui verrà eseguito il backup del database di ripristino.

### Trasferire il database di ripristino dal server a al server B

USA Esplora risorse per trasferire il file **Data. bak del database di ripristino di mbam** dal server a al server B.

Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
Usare le informazioni nella tabella seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

| **Parametro**        | **Descrizione**  |
|----------------------|------------------|
| $SERVERNAME $       | Nome del server in cui verranno copiati i file. |
| $DESTINATIONSHARE $ | Nome della condivisione e del percorso in cui verranno copiati i file. |


### Ripristinare il database di ripristino nel server B

1.  Ripristinare il database di ripristino nel server B usando l'attività **Ripristina database** in SQL Server Management Studio.

2.  Al termine dell'attività precedente, selezionare **da dispositivo**e quindi selezionare il file di backup del database.

3.  Usare il comando **Aggiungi** per selezionare il file **Data. bak del database di ripristino di mbam** e fare clic su **OK** per completare il processo di ripristino.

4.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

    FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

    WITH REPLACE
    ```

5.  Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

    **$Password $** -password usata per crittografare il file della chiave privata.

6.  In Windows PowerShell eseguire lo script archiviato nel file e simile al seguente:

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

    **$ServerName $ \ $SqlInstanceName $** -nome del server e istanza in cui verrà ripristinato il database di ripristino.

### Configurare l'accesso al database nel server B e aggiornare i dati di connessione

1. Verificare che l'account di accesso dell'utente di Microsoft SQL Server che consente l'accesso al database di ripristino nel database ripristinato sia mappato all'indirizzo di Access fornito durante il processo di configurazione.

   >[!NOTE]
   >Se l'account di accesso non è lo stesso, creare un account di accesso tramite SQL Server Management Studio e associarlo all'utente del database esistente.

2. Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per i siti Web di MBAM.

3. Modificare la chiave del registro di sistema seguente:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. Aggiornare il valore dell' **origine dati** con il nome del server e dell'istanza, ad esempio \ $ServerName \ $ \ \ \ $SqlInstanceName, in cui è stato spostato il database di ripristino.

5. Aggiornare il valore del **catalogo iniziale** con il nome del database recuperato.

6. Per automatizzare il processo, è possibile usare il prompt dei comandi di Windows PowerShell per immettere una riga di comando nel server di amministrazione e monitoraggio simile al seguente:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   >Questa stringa di connessione è condivisa da tutte le applicazioni Web di MBAM locali. Pertanto, deve essere aggiornata solo una volta per ogni server.


7. Usare la tabella seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

   |Parametro|Descrizione|
   |---------|-----------|
   |$SERVERNAME $/\ $SQLINSTANCENAME $|Nome server e istanza di SQL Server in cui si trova il database di ripristino.|
   |$DATABASE $|Nome del database di ripristino.|


### Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B

1.  Installare il software MBAM 2,5 Server sul server B. Per informazioni dettagliate, vedere [installazione del software server MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **database di ripristino** . Per informazioni dettagliate su come configurare i database, vedere [come configurare i database di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamDatabase** per configurare il database di ripristino.


### Riprendere l'istanza del sito Web di amministrazione e monitoraggio

Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di amministrazione e monitoraggio.

Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Per eseguire questo comando, è necessario aggiungere il modulo IIS per Windows PowerShell all'istanza corrente di Windows PowerShell.

## Trasferire il database di conformità e controllo

I passaggi di alto livello per lo spostamento del database di conformità e controllo sono i seguenti:

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

2.  Eseguire il backup del database di conformità e controllo nel server A

3.  Trasferire il database di conformità e controllo dal server a al server B

4.  Ripristinare il database di conformità e controllo nel server B

5.  Configurare l'accesso al database nel server B e aggiornare i dati di connessione

6.  Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B

7.  Riprendere l'istanza del sito Web di amministrazione e monitoraggio

### Come si trasferisce il database di conformità e controllo

**Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.**  In ogni server che sta usando il sito Web di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di amministrazione e monitoraggio.

Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Per eseguire questo comando, è necessario aggiungere il modulo Internet Information Services (IIS) per Windows PowerShell all'istanza corrente di Windows PowerShell.

### Eseguire il backup del database di conformità e controllo nel server A

1.  Usare l'attività di **backup** in SQL Server Management Studio per eseguire il backup del database di conformità e controllo nel server a. Per impostazione predefinita, il nome del database è **mbam compliance database status**.

2.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  Eseguire lo script archiviato nel file con estensione SQL usando un comando di Windows PowerShell simile al seguente:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  Usando il valore seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente:

    **$ServerName $ \ $SqlInstanceName $** -nome del server e istanza da cui verrà eseguito il backup del database di conformità e controllo.

### Trasferire il database di conformità e controllo dal server a al server B * *

1.  USA Esplora risorse per trasferire il file **Data. bak di database di stato della conformità di mbam** dal server a al server B.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  Usando la tabella seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

    | **Parametro**        | **Descrizione**                                               |
    |----------------------|---------------------------------------------------------------|
    | $SERVERNAME $       | Nome del server in cui verranno copiati i file.         |
    | $DESTINATIONSHARE $ | Nome della condivisione e del percorso in cui verranno copiati i file. |


### Ripristinare il database di conformità e controllo nel server B

1.  Ripristinare il database di conformità e controllo nel server B usando l'attività **Ripristina database** in SQL Server Management Studio.

2.  Al termine dell'attività precedente, selezionare **da dispositivo**e quindi selezionare il file di backup del database.

3.  Usare il comando **Aggiungi** per selezionare il file **Data. bak di database di stato della conformità di mbam** e fare clic su **OK** per completare il processo di ripristino.

4.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  In Windows PowerShell eseguire lo script archiviato nel file e simile al seguente:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  Usando il valore seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

    **$ServerName $ \ $SqlInstanceName $** -nome del server e istanza in cui verrà ripristinato il database di conformità e controllo.

### Configurare l'accesso al database nel server B e aggiornare i dati di connessione

1. Verificare che l'account di accesso dell'utente di Microsoft SQL Server che consente l'accesso al database di conformità e di controllo nel database ripristinato sia mappato con quello specificato durante il processo di configurazione.

   >[!NOTE]
   >Se l'account di accesso non è lo stesso, creare un account di accesso tramite SQL Server Management Studio e associarlo all'utente del database esistente.

2. Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per il sito Web.

3. Modificare la chiave del registro di sistema seguente:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. Aggiornare il valore dell' **origine dati** con il nome del server e dell'istanza, ad esempio \ $ServerName \ $ \ \ \ $SqlInstanceName, in cui è stato spostato il database di ripristino.

5. Aggiornare il valore del **catalogo iniziale** con il nome del database recuperato.

6. Per automatizzare il processo, è possibile usare il prompt dei comandi di Windows PowerShell per immettere una riga di comando nel server di amministrazione e monitoraggio simile al seguente:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >Questa stringa di connessione è condivisa da tutte le applicazioni Web di MBAM locali. Pertanto, deve essere aggiornata solo una volta per ogni server.


7. Usando la tabella seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.

   |Parametro | Descrizione |
   |---------|------------|
   |$SERVERNAME $ \ $SQLINSTANCENAME $ | Nome server e istanza di SQL Server in cui si trova il database di ripristino.|
   |$DATABASE $|Nome del database recuperato.|

### Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B

1.  Installare il software MBAM 2,5 Server sul server B. Per informazioni dettagliate, vedere [installazione del software server MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **di database di conformità e controllo** . Per informazioni dettagliate su come configurare i database, vedere [come configurare i database di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamDatabase** per configurare il database di conformità e controllo.


### Riprendere l'istanza del sito Web di amministrazione e monitoraggio

Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di amministrazione e monitoraggio.

Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Per eseguire questo comando, è necessario aggiungere il modulo IIS per Windows PowerShell all'istanza corrente di Windows PowerShell.
