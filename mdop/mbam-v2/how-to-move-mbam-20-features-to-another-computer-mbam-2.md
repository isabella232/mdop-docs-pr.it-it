---
title: Come spostare le funzionalità di MBAM 2.0 in un altro computer
description: Come spostare le funzionalità di MBAM 2.0 in un altro computer
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825076"
---
# Come spostare le funzionalità di MBAM 2.0 in un altro computer


In questo argomento vengono illustrati i passaggi da eseguire per trasferire una o più funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in un altro computer. Quando si spostano più funzionalità di amministrazione e monitoraggio di Microsoft BitLocker, è consigliabile spostarle nell'ordine seguente:

1.  Database di ripristino

2.  Database di conformità e controllo

3.  Report di conformità e controllo

4.  Amministrazione e monitoraggio

## Spostamento del database di ripristino


Per trasferire il database di ripristino da un computer a un altro, ad esempio dal server a al server B, eseguire la procedura seguente.

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio.

2.  Eseguire la configurazione di MBAM sul server B.

3.  Eseguire il backup del database di ripristino MBAM nel server A.

4.  Trasferire il database di ripristino MBAM dal server da A a B.

5.  Ripristinare il database di ripristino MBAM nel server B.

6.  Configurare l'accesso al database di ripristino di MBAM sul server B.

7.  Aggiornare i dati di connessione al database nei server di amministrazione e monitoraggio di MBAM.

8.  Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.

**Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ognuno dei server che gestiscono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM, che si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere la riga di comando simile alla seguente:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Per eseguire questa riga di comando di PowerShell, il modulo IIS per PowerShell deve essere aggiunto all'istanza corrente di PowerShell. È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per abilitare l'esecuzione di script.



**Eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare solo il **database di ripristino** per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere la riga di comando simile alla seguente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza in cui verrà spostato il database di ripristino.

    -   $DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e server di ogni server di amministrazione e monitoraggio di MBAM che contatterà il database di ripristino. Usare un punto e virgola per separare le coppie di domini e server nell'elenco, ad esempio $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $). Ogni nome del server deve essere seguito da un simbolo "$", come illustrato nell'esempio (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.



**Eseguire il backup del database di ripristino nel server A**

1.  Per eseguire il backup del database di ripristino nel server A, usare SQL Server Management Studio e l'attività denominata backup. Per impostazione predefinita, il nome del database è il **database di ripristino MBAM**.

2.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:

    Modificare il database di ripristino di MBAM per usare la modalità di recupero completo.

    ```sql
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

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $PASSWORD $-immettere una password che verrà usata per crittografare il file della chiave privata.



3.  Eseguire il file SQL con SQL Server PowerShell e una riga di comando simile alla seguente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza da cui verrà eseguito il backup del database di ripristino.



**Trasferire il database di ripristino e il certificato dal server a al server B**

1.  Trasferire il file seguente dal server a al server B usando Esplora risorse.

    -   Database di ripristino di MBAM data. bak

2.  Per trasferire il certificato per il database crittografato, usare la procedura seguente per l'automazione. Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $-immettere il nome del server in cui verranno copiati i file.

    -   $DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.



**Ripristinare il database di ripristino nel server B**

1.  Ripristinare il database di ripristino nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database**.

2.  Dopo aver completato l'attività, selezionare il file di backup del database selezionando l'opzione **da dispositivo** e quindi usando il comando **Aggiungi** per selezionare il file **Data. bak** del database di ripristino di mbam.

3.  Selezionare **OK** per completare il processo di ripristino.

4.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

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

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $PASSWORD $-immettere una password usata per crittografare il file della chiave privata.



5.  È possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza in cui verrà ripristinato il database di ripristino.



**Configurare l'accesso al database di ripristino nel server B**

1.  Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Recovery and hardware DB Access**.

2.  Verificare che il ripristino di mbam dell'accesso SQL **e l'accesso DB hardware** nel database ripristinato siano mappati al nome di accesso **$machineName $ \\MBAM Recovery and hardware DB Access**. Se non è mappato come descritto, crea un altro account di accesso con l'appartenenza a un gruppo simile e associalo al nome di accesso **$machineName $ \\MBAM Recovery and hardware DB Access**.

3.  Per automatizzare questa procedura, è possibile usare Windows PowerShell sul server B per immettere una riga di comando simile alla seguente:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM. Il nome del server deve essere seguito da un $, come illustrato nell'esempio, ad esempio MyDomain\\MyServerName1 $.



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Aggiornare i dati di connessione al database di ripristino nei server di amministrazione e monitoraggio di MBAM**

1. In ognuno dei server che esegue la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio:

   -   MBAMAdministrationService

   -   MBAMRecoveryAndHardwareService

2. Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.

3. Selezionare l'opzione **configurationStrings** dal controllo **elenco sezioni** .

4. Selezionare la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.

5. Nell' **Editor della raccolta**selezionare la riga denominata **KeyRecoveryConnectionString** durante l'aggiornamento della configurazione per l'applicazione MBAMAdministrationService o la riga denominata <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString durante l'aggiornamento della configurazione per MBAMRecoveryAndHardwareService.

6. Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome e l'istanza del server, ad esempio $SERVERNAME $ \ \ $SqlInstanceName $) in cui è stato spostato il database di ripristino.

7. Per automatizzare questa procedura, è possibile usare Windows per immettere una riga di comando simile alla seguente, in ogni server di amministrazione e monitoraggio:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Nota**  
   Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di ripristino.



**Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ogni server che sta usando la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM, che si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Spostamento della funzionalità di database di conformità e controllo


Se si vuole trasferire il database di controllo e conformità di MBAM da un computer a un altro (ovvero, trasferire il database dal server a al server B), usare la procedura seguente. Il processo include i passaggi di alto livello seguenti:

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio.

2.  Eseguire la configurazione di MBAM sul server B.

3.  Eseguire il backup del database nel server A.

4.  Trasferire il database dal server da A a B.

5.  Ripristinare il database nel server B.

6.  Configurare l'accesso al database nel server B.

7.  Aggiornare i dati di connessione al database nei server di amministrazione e monitoraggio di MBAM.

8.  Aggiornare la stringa di connessione all'origine dati di report SSRS con la nuova posizione del database di conformità e controllo.

9.  Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio.

**Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio**

1.  In ogni server che sta usando la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Per eseguire questa riga di comando, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell. È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.



**Eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare solo il **database di conformità e controllo** per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **Nota**  
    Nota: Sostituisci i valori seguenti nell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà spostato il database di conformità e controllo.

    -   $DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e server di ogni server di amministrazione e monitoraggio di MBAM che contatterà il database di conformità e controllo. Usare un punto e virgola per separare ogni coppia di domini e server nell'elenco, ad esempio $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $). Ogni nome del server deve essere seguito da un simbolo "$", come illustrato nell'esempio (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di conformità e controllo.

    -   $X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.



**Eseguire il backup del database di conformità e controllo nel server A**

1.  Per eseguire il backup del database di conformità e controllo nel server A, usare SQL Server Management Studio e l'attività denominata **backup**. Per impostazione predefinita, il nome del database è **mbam compliance database status**.

2.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

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

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Eseguire il file SQL usando una riga di comando di Windows PowerShell simile alla seguente:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà eseguito il backup del database di conformità e controllo.



**Trasferire il database di conformità e controllo dal server a alla B**

1.  È necessario trasferire i file seguenti dal server a al server B usando Esplora risorse.

    -   Informazioni sul database dello stato di conformità MBAM. bak

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $-immettere il nome del server in cui verranno copiati i file.

    -   $DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.



**Ripristinare il database di conformità e controllo nel server B**

1.  Ripristinare il database di conformità e controllo nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database**.

2.  Dopo aver completato l'attività, selezionare il file di backup del database selezionando l'opzione **da dispositivo** e quindi usando il comando **Aggiungi** per selezionare il file Data. bak del database di stato della conformità di mbam. Selezionare **OK** per completare il processo di ripristino.

3.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Eseguire il file SQL usando una riga di comando di Windows PowerShell simile alla seguente:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà ripristinato il database di conformità e controllo.



**Configurare l'accesso al database di conformità e controllo nel server B**

1.  Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Compliance status DB Access**.

2.  Verificare che l'accesso a SQL **Access mbam Compliance controllo DB** per il database ripristinato sia mappato al nome di accesso **$machineName $ \ \ mbam compliance audit DB Access**. Se non è mappato come descritto, crea un altro account di accesso con l'appartenenza a un gruppo simile e associalo al nome di accesso **$machineName $ \ \ mbam compliance audit DB Access**.

3.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando nel server B simile alla seguente:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM. Il nome del server deve essere seguito da un "$", come illustrato nell'esempio. (ad esempio, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server**

1.  In ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.

3.  Selezionare l'opzione **configurationStrings** dal controllo **elenco sezioni** .

4.  Selezionare la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.

5.  Nell' **Editor della raccolta**selezionare la riga denominata **ComplianceStatusConnectionString** durante l'aggiornamento della configurazione per l'applicazione MBAMAdministrationService o la riga denominata **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** durante l'aggiornamento della configurazione per il MBAMComplianceStatusService.

6.  Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome del server e dell'istanza, ad esempio $SERVERNAME $ \ \ $SqlInstanceName, a cui è stato spostato il database di ripristino.

7.  Per automatizzare questa procedura, è possibile usare Windows per immettere una riga di comando in ogni server di amministrazione e monitoraggio simile al seguente:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di ripristino.



**Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ogni server che sta usando la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Spostamento dei report di conformità e controllo


Se si vuole trasferire i report di controllo e conformità di MBAM da un computer a un altro (ovvero, trasferire i report dal server a al server B), usare la procedura seguente, che include i passaggi di alto livello seguenti:

1.  Eseguire la configurazione di MBAM sul server B.

2.  Configurare l'accesso ai report di conformità e controllo nel server B.

3.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.

4.  Aggiornare i dati di connessione dei report nei server di amministrazione e monitoraggio di MBAM.

5.  Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.

**Eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare solo la caratteristica **conformità e controllo rapporti** per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di conformità e controllo.

    -   $DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di conformità e controllo.

    -   $PASSWORD $-immettere la password dell'account utente che verrà usato per connettersi al database di conformità e controllo.

    -   $X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.



**Configurare l'accesso ai report di conformità e controllo sul server B**

1.  Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account utente che avranno accesso ai report di conformità e controllo. Aggiungere gli account utente al gruppo locale denominato MBAM report Users.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando nel server B simile alla seguente:

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ogni server che sta usando la funzionalità MBAM Administration e Monitoring Server usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Aggiornare i dati di connessione al database nei server di amministrazione e monitoraggio di MBAM**

1. In ogni server che sta usando la funzionalità MBAM Administration e Monitoring Server usare la console di gestione di Internet Information Services (IIS) per aggiornare l'URL dei report di conformità e controllo.

2. Selezionare il sito Web di **amministrazione e monitoraggio di Microsoft BitLocker** e usare la caratteristica **editor di configurazione** che è la posizione nella sezione **gestione** della **visualizzazione funzionalità**.

3. Selezionare l'opzione **appSettings** dal controllo **elenco sezioni** .

4. Selezionare la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.

5. Nell' **Editor della raccolta**selezionare la riga denominata **Microsoft. mbam. Reports. URL**.

6. Aggiorna il valore per **Microsoft. mbam. Reports. URL** per riflettere il nome del server per il server B. Se la caratteristica conformità e rapporti di controllo è stata installata in un'istanza di SQL Reporting Services denominata, assicurarsi di aggiungere o aggiornare il nome dell'istanza all'URL, ad esempio http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....)

7. Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando in ogni server di amministrazione e monitoraggio simile al seguente:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **Nota**  
   Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

   -   $SERVERNAME $-immettere il nome del nome del server a cui sono stati installati i report di conformità e controllo.

   -   $SRSINSTANCENAME $-immettere il nome dell'istanza di SQL Reporting Services a cui sono stati installati i report di conformità e controllo.



**Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ogni server che sta usando la funzionalità MBAM Administration e Monitoring Server usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Per eseguire questa riga di comando, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell. È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.



## Spostamento della funzionalità di amministrazione e monitoraggio


Se si vuole trasferire la caratteristica di amministrazione e monitoraggio dei report di MBAM da un computer a un altro (ovvero, trasferire la caratteristica dal server a al server B), usare la procedura seguente, che include i passaggi di alto livello seguenti:

1.  Eseguire la configurazione di MBAM sul server B.

2.  Configurare l'accesso al database nel server B.

**Eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare solo la funzionalità **amministrazione e monitoraggio server** per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-per il parametro COMPLIDB \ _SQLINSTANCE immettere il nome del server e l'istanza in cui si trova il database di conformità e controllo. Per il parametro RECOVERYANDHWDB \ _SQLINSTANCE immettere il nome del server e l'istanza in cui si trova il database di ripristino.

    -   $DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di conformità e controllo.

    -   $ REPORTSSERVERURL $-immettere l'URL per la posizione Home del sito Web del servizio SQL Reporting. Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL avrà il formato "http://$SERVERNAME $/ReportServer". Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL avrà il formato "http://$SERVERNAME $/ReportServer\_ $ SqlInstanceName $".

    -   $X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.



**Configurare l'accesso ai database**

1.  Nel server o nei server in cui sono distribuiti il database di ripristino e la conformità e il database di controllo, usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità MBAM Administration and Monitoring Server nei gruppi locali denominati **mbam Recovery and hardware DB Access** (Recovery DB Server) e **mbam Compliance status DB Access**

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente, nel server in cui è stato distribuito il database di conformità e controllo.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  Nel server in cui è stato distribuito il database di ripristino, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Sostituire il valore seguente nell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio. Il nome del server deve essere seguito da un simbolo "$", come illustrato nell'esempio, ad esempio MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Argomenti correlati


[Manutenzione di MBAM 2.0](maintaining-mbam-20-mbam-2.md)









