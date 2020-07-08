---
title: Come spostare le funzionalità di MBAM 1.0 in un altro computer
description: Come spostare le funzionalità di MBAM 1.0 in un altro computer
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804611"
---
# Come spostare le funzionalità di MBAM 1.0 in un altro computer


In questo argomento vengono illustrati i passaggi da eseguire per trasferire una o più funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in un altro computer. Quando si spostano più funzionalità di MBAM in un altro computer, è consigliabile spostarle nell'ordine seguente:

1.  Database di ripristino e hardware

2.  Database di conformità e controllo

3.  Report di conformità e controllo

4.  Amministrazione e monitoraggio

## Per trasferire il database di ripristino e hardware


È possibile usare la procedura seguente per trasferire il database di MBAM Recovery e hardware da un computer a un altro (è possibile trasferire questa caratteristica del server MBAM dal server a al server B):

****

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.

2.  Eseguire la configurazione di MBAM sul server B.

3.  Eseguire il backup del database di MBAM Recovery e hardware nel server A.

4.  Database di ripristino e hardware di MBAM dal server a alla B

5.  Ripristinare il database di MBAM Recovery e hardware nel server B

6.  Configurare l'accesso al database di MBAM Recovery e hardware nel server B

7.  Aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server

8.  Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

**Per arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  Usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM in ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM. Il sito Web di MBAM si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare un comando al prompt dei comandi simile al seguente, usando Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Per eseguire il prompt dei comandi di PowerShell, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell. È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.



**Per eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare il database di ripristino e hardware per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare un comando al prompt dei comandi simile al seguente, usando Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza in cui verrà spostato il database di ripristino e hardware.

    -   $DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e server di ogni applicazione MBAM e server di monitoraggio che contatteranno il database di ripristino e hardware. Se sono presenti più nomi di dominio e server, usare un punto e virgola per separare ognuno di essi nell'elenco. Ad esempio, $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $. Inoltre, ogni nome del server deve essere seguito da a **$** . Ad esempio, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.



**Per eseguire il backup del database nel server A**

1.  Per eseguire il backup del database di ripristino e hardware nel server A, usare SQL Server Management Studio e l'attività denominata **backup...**. Per impostazione predefinita, il nome del database è **mbam Recovery and hardware database**.

2.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:

    Modificare il database di MBAM Recovery e hardware per usare la modalità di recupero completo.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    Creare MBAM Recovery e dati di database hardware e dispositivi di backup logici di ripristino MBAM.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    Eseguire il backup del database completo di MBAM Recovery e hardware.

    ```sql
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
    Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $PASSWORD $-immettere una password che verrà usata per crittografare il file della chiave privata.



3.  Eseguire il file SQL con SQL Server PowerShell e un comando simile al seguente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire il valore nell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza da cui eseguire il backup del database di ripristino e hardware.



**Per trasferire il database e il certificato dal server a alla B**

1.  Consente di trasferire i dati di MBAM Recovery e database hardware dal server a al server B usando Esplora risorse.

2.  Per trasferire il certificato per il database crittografato, è necessario usare la procedura di automazione seguente. Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $-immettere il nome del server in cui verranno copiati i file.

    -   $DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.



**Per ripristinare il database nel server B**

1.  Ripristinare il database di ripristino e hardware nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database**.

2.  Dopo aver eseguito l'attività, scegliere il file di backup del database selezionando l'opzione **da dispositivo** e quindi usare il comando **Aggiungi** per scegliere il file **Data. bak** per il recupero e il database hardware di mbam.

3.  Selezionare **OK** per completare il processo di ripristino.

4.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    Eliminare il certificato creato da MBAM Setup.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    Aggiungi certificato

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    Ripristinare i dati di database hardware e ripristino di MBAM e i file di log.

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **Nota**  
    Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $PASSWORD $-immettere la password usata per crittografare il file della chiave privata.



5.  Usare Windows PowerShell per immettere una riga di comando simile alla seguente:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituisci il valore dell'esempio che sfugge con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà ripristinato il ripristino e il database hardware.



**Configurare l'accesso al database nel server B**

1.  Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Recovery and hardware DB Access**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell sul server B per immettere un comando simile al seguente:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Sostituire i valori dell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome di dominio e il nome del computer del server di amministrazione e monitoraggio di MBAM. Il nome del server deve essere seguito da un **$** , ad esempio MyDomain\\MyServerName1 $.



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Per aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server**

1. In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio di Microsoft BitLocker:

   -   Servizio di amministrazione MBAM

   -   Servizio di ripristino e hardware di MBAM

2. Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.

3. Selezionare l'opzione **configurationStrings** dal controllo elenco sezioni.

4. Scegliere la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.

5. Nell' **Editor della raccolta**scegliere la riga denominata **KeyRecoveryConnectionString** quando è stata aggiornata la configurazione per l'applicazione "MBAMAdministrationService" oppure scegliere la riga denominata <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString, quando si aggiorna la configurazione per "MBAMRecoveryAndHardwareService".

6. Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome del server e l'istanza in cui è stato spostato il database di ripristino e hardware. Ad esempio, $SERVERNAME $ \ \ $SQLINSTANCENAME $.

7. Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell in ogni server di amministrazione e monitoraggio:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Nota**  
   Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di ripristino e hardware.



**Per riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM, denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Per cambiare la funzionalità del database dello stato di conformità


Se si sceglie di trasferire la funzionalità di database di stato di conformità di MBAM da un computer a un altro, ad esempio dal server a al server B, è consigliabile usare la procedura seguente:

1.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

2.  Eseguire la configurazione di MBAM sul server B

3.  Eseguire il backup del database nel server A

4.  Trasferire il database dal server a alla B

5.  Ripristinare il database nel server B

6.  Configurare l'accesso al database nel server B

7.  Aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server

8.  Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

**Per arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM, che si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Per eseguire questo comando, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell. È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.



**Per eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare la caratteristica di database dello stato di conformità per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **Nota**  
    Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà spostato il database dello stato di conformità.

    -   $DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e i nomi dei server di ogni applicazione MBAM e server di monitoraggio che contatteranno il database di stato conformità. Se sono presenti più nomi di dominio e nomi di server, usare un punto e virgola per separare ognuno di essi nell'elenco. Ad esempio, $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $. Ogni nome del server deve essere seguito da un **$** come illustrato nell'esempio. Ad esempio, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.

    -   $DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di stato della conformità.



**Per eseguire il backup del database di conformità nel server A**

1.  Per eseguire il backup del database di conformità nel server A, usare SQL Server Management Studio e l'attività denominata **backup...**. Per impostazione predefinita, il nome del database è **mbam compliance database status**.

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Eseguire il file SQL con un comando simile a quello seguente usando la PowerShell per SQL Server:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza da cui verrà eseguito il backup del database dello stato di conformità.



**Per trasferire il database dal server a alla B**

1.  Per trasferire i file seguenti dal server a al server B, usare Esplora risorse:

    -   Informazioni sul database dello stato di conformità MBAM. bak

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Nota**  
    Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $-immettere il nome del server in cui verranno copiati i file.

    -   $DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.



**Per ripristinare il database nel server B**

1.  Ripristinare il database dello stato di conformità nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database.**...

2.  Dopo l'esecuzione dell'attività, selezionare il file di backup del database selezionando l'opzione da dispositivo e quindi usare il comando Aggiungi per scegliere il file Data. bak del database di stato della conformità di MBAM. Fare clic su OK per completare il processo di ripristino.

3.  Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Eseguire il file SQL con un comando simile a quello seguente usando la PowerShell per SQL Server:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Nota**  
    Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà ripristinato il database dello stato di conformità.



**Per configurare l'accesso al database nel server B**

1.  Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Compliance status DB Access**.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell sul server B:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Sostituire il valore dell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM. Il nome del server deve essere seguito da a **$** . Ad esempio, MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**Per aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server**

1.  In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio di Microsoft BitLocker:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.

3.  Selezionare l'opzione **configurationStrings** dal controllo elenco sezioni.

4.  Selezionare la riga denominata **(raccolta)** e aprire l'editor della raccolta selezionando il pulsante sul lato destro della riga.

5.  Nell' **Editor della raccolta**selezionare la riga denominata **ComplianceStatusConnectionString**, quando si aggiorna la configurazione per l'applicazione MBAMAdministrationService o la riga denominata **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, quando si aggiorna la configurazione per MBAMComplianceStatusService.

6.  Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome del server e il nome dell'istanza. Ad esempio, $SERVERNAME $ \ \ $SQLINSTANCENAME, a cui è stato spostato il database di ripristino e hardware.

7.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile a quello seguente in ogni server di amministrazione e monitoraggio:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Nota**  
    Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e il nome dell'istanza in cui si trova il database di ripristino e hardware.



**Per riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ognuno dei server che gestiscono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:

    **PS C:\\ &gt; Start-sito Web "amministrazione e monitoraggio di Microsoft BitLocker"**

## Per spostare i report di conformità e controllo


Se si sceglie di trasferire i report di controllo e conformità di MBAM da un computer a un altro (in particolare, se si trasferisce la caratteristica dal server a al server B), è consigliabile usare la procedura e i passaggi seguenti:

1.  Eseguire la configurazione di MBAM sul server B

2.  Configurare l'accesso ai report di conformità e controllo sul server B

3.  Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

4.  Aggiornare i dati di connessione dei report sui server di amministrazione e monitoraggio di MBAM

5.  Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM

**Per eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare solo la funzionalità di conformità e controllo per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare un comando simile al seguente usando Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **Nota**  
    Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database dello stato di conformità.

    -   $DOMAIN $ \ \ $USERNAME $-immettere il nome di dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di stato della conformità.

    -   $PASSWORD $-immettere la password dell'account utente che verrà usato per connettersi al database dello stato di conformità.



**Per configurare l'accesso ai report di conformità e controllo nel server B**

1.  Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account utente che avranno accesso ai report di conformità e controllo. Aggiungere gli account utente al gruppo locale denominato "utenti report MBAM".

2.  Per automatizzare questa procedura, è possibile usare un comando simile al seguente usando Windows PowerShell nel server B.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Nota**  
    Sostituire il valore seguente dell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Per arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Per aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server**

1. In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare l'URL dei report di conformità.

2. Selezionare il sito Web di **amministrazione e monitoraggio di Microsoft BitLocker** e usare la caratteristica **editor di configurazione** che si trova nella sezione **gestione** della **visualizzazione funzionalità**.

3. Selezionare l'opzione **appSettings** dal controllo elenco sezioni.

4. Da qui selezionare la riga denominata **(raccolta)** e aprire l'editor della **raccolta** selezionando il pulsante sul lato destro della riga.

5. Nell' **Editor della raccolta**selezionare la riga denominata "Microsoft. mbam. Reports. URL".

6. Aggiorna il valore per Microsoft. mbam. Reports. URL per riflettere il nome del server per il server B. Se la caratteristica conformità e rapporti di controllo è stata installata in un'istanza di SQL Reporting Services denominata, verificare di aggiungere o aggiornare il nome dell'istanza all'URL. Ad esempio, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....

7. Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile a quello seguente in ogni server di amministrazione e monitoraggio:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **Nota**  
   Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:

   -   $SERVERNAME $-immettere il nome del server a cui sono stati installati i report di conformità e controllo.

   -   $SRSINSTANCENAME $-immettere il nome dell'istanza di SQL Reporting Services a cui sono stati installati i report di conformità e controllo.



**Per riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM**

1.  In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Nota**  
    Per eseguire questo comando, il modulo IIS per PowerShell deve essere aggiunto all'istanza corrente di PowerShell. È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per abilitare l'esecuzione di script.



## Per trasferire la funzionalità di amministrazione e monitoraggio


Se si sceglie di trasferire la caratteristica di amministrazione e monitoraggio di MBAM da un computer a un altro, se si trasferisce la caratteristica dal server a al server B, è consigliabile usare la procedura seguente. Il processo include i passaggi seguenti:

1.  Eseguire la configurazione di MBAM sul server B

2.  Configurare l'accesso al database nel server B

**Per eseguire la configurazione di MBAM sul server B**

1.  Eseguire la configurazione di MBAM sul server B e selezionare solo la caratteristica di amministrazione per l'installazione.

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **Nota**  
    Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-per il parametro COMPLIDB \ _SQLINSTANCE, immettere il nome del server e l'istanza in cui si trova il database dello stato di conformità. Per il parametro RECOVERYANDHWDB \ _SQLINSTANCE, immettere il nome del server e l'istanza in cui si trova il database di ripristino e hardware.

    -   $DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di stato della conformità.

    -   $ REPORTSSERVERURL $-immettere l'URL per la posizione Home del sito Web del servizio SQL Reporting. Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL verrà formattato come "http://$SERVERNAME $/ReportServer". Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL verrà formattato in "http://$SERVERNAME $/ReportServer\_ $ SqlInstanceName $".



**Per configurare l'accesso ai database**

1.  In server o server in cui il ripristino e l'hardware e i database di conformità e controllo vengono distribuiti, USA lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nei gruppi locali denominati "MBAM Recovery and hardware DB Access" (Recovery and hardware DB Server) e "MBAM Compliance status DB Access" (conformità e audit DB Server).

2.  Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell nel server in cui sono stati distribuiti i database di conformità e controllo.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  Nel server in cui sono stati distribuiti i database di ripristino e hardware eseguire un comando simile a quello seguente usando Windows PowerShell.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Nota**  
    Sostituire il valore dell'esempio precedente con i valori applicabili per l'ambiente:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM. Il nome del server deve essere seguito da a **$** . Ad esempio, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 1.0](administering-mbam-10-features.md)









