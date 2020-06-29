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
# <span data-ttu-id="9d85b-103">Come spostare le funzionalità di MBAM 2.0 in un altro computer</span><span class="sxs-lookup"><span data-stu-id="9d85b-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="9d85b-104">In questo argomento vengono illustrati i passaggi da eseguire per trasferire una o più funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="9d85b-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="9d85b-105">Quando si spostano più funzionalità di amministrazione e monitoraggio di Microsoft BitLocker, è consigliabile spostarle nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="9d85b-106">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="9d85b-106">Recovery Database</span></span>

2.  <span data-ttu-id="9d85b-107">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9d85b-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="9d85b-108">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9d85b-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="9d85b-109">Amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="9d85b-109">Administration and Monitoring</span></span>

## <span data-ttu-id="9d85b-110">Spostamento del database di ripristino</span><span class="sxs-lookup"><span data-stu-id="9d85b-110">Moving the Recovery Database</span></span>


<span data-ttu-id="9d85b-111">Per trasferire il database di ripristino da un computer a un altro, ad esempio dal server a al server B, eseguire la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="9d85b-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="9d85b-112">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9d85b-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="9d85b-113">Eseguire la configurazione di MBAM sul server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="9d85b-114">Eseguire il backup del database di ripristino MBAM nel server A.</span><span class="sxs-lookup"><span data-stu-id="9d85b-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="9d85b-115">Trasferire il database di ripristino MBAM dal server da A a B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="9d85b-116">Ripristinare il database di ripristino MBAM nel server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="9d85b-117">Configurare l'accesso al database di ripristino di MBAM sul server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="9d85b-118">Aggiornare i dati di connessione al database nei server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="9d85b-119">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="9d85b-120">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9d85b-121">In ognuno dei server che gestiscono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM, che si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9d85b-122">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere la riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9d85b-123">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-123">Note</span></span>**  
    <span data-ttu-id="9d85b-124">Per eseguire questa riga di comando di PowerShell, il modulo IIS per PowerShell deve essere aggiunto all'istanza corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d85b-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="9d85b-125">È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per abilitare l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="9d85b-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="9d85b-126">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9d85b-127">Eseguire la configurazione di MBAM sul server B e selezionare solo il **database di ripristino** per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9d85b-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="9d85b-128">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere la riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="9d85b-129">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-129">Note</span></span>**  
    <span data-ttu-id="9d85b-130">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-131">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza in cui verrà spostato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="9d85b-132">$DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e server di ogni server di amministrazione e monitoraggio di MBAM che contatterà il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="9d85b-133">Usare un punto e virgola per separare le coppie di domini e server nell'elenco, ad esempio $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="9d85b-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="9d85b-134">Ogni nome del server deve essere seguito da un simbolo "$", come illustrato nell'esempio (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="9d85b-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="9d85b-135">$X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9d85b-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9d85b-136">Eseguire il backup del database di ripristino nel server A</span><span class="sxs-lookup"><span data-stu-id="9d85b-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="9d85b-137">Per eseguire il backup del database di ripristino nel server A, usare SQL Server Management Studio e l'attività denominata backup.</span><span class="sxs-lookup"><span data-stu-id="9d85b-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="9d85b-138">Per impostazione predefinita, il nome del database è il **database di ripristino MBAM**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="9d85b-139">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="9d85b-140">Modificare il database di ripristino di MBAM per usare la modalità di recupero completo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

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

    **<span data-ttu-id="9d85b-141">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-141">Note</span></span>**  
    <span data-ttu-id="9d85b-142">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-143">$PASSWORD $-immettere una password che verrà usata per crittografare il file della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="9d85b-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="9d85b-144">Eseguire il file SQL con SQL Server PowerShell e una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9d85b-145">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-145">Note</span></span>**  
    <span data-ttu-id="9d85b-146">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-147">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza da cui verrà eseguito il backup del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="9d85b-148">Trasferire il database di ripristino e il certificato dal server a al server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="9d85b-149">Trasferire il file seguente dal server a al server B usando Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9d85b-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="9d85b-150">Database di ripristino di MBAM data. bak</span><span class="sxs-lookup"><span data-stu-id="9d85b-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="9d85b-151">Per trasferire il certificato per il database crittografato, usare la procedura seguente per l'automazione.</span><span class="sxs-lookup"><span data-stu-id="9d85b-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="9d85b-152">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="9d85b-153">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-153">Note</span></span>**  
    <span data-ttu-id="9d85b-154">Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-155">$SERVERNAME $-immettere il nome del server in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9d85b-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="9d85b-156">$DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9d85b-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="9d85b-157">Ripristinare il database di ripristino nel server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="9d85b-158">Ripristinare il database di ripristino nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="9d85b-159">Dopo aver completato l'attività, selezionare il file di backup del database selezionando l'opzione **da dispositivo** e quindi usando il comando **Aggiungi** per selezionare il file **Data. bak** del database di ripristino di mbam.</span><span class="sxs-lookup"><span data-stu-id="9d85b-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="9d85b-160">Selezionare **OK** per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="9d85b-161">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:</span><span class="sxs-lookup"><span data-stu-id="9d85b-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    **<span data-ttu-id="9d85b-162">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-162">Note</span></span>**  
    <span data-ttu-id="9d85b-163">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-164">$PASSWORD $-immettere una password usata per crittografare il file della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="9d85b-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="9d85b-165">È possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9d85b-166">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-166">Note</span></span>**  
    <span data-ttu-id="9d85b-167">Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-168">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza in cui verrà ripristinato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="9d85b-169">Configurare l'accesso al database di ripristino nel server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="9d85b-170">Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Recovery and hardware DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="9d85b-171">Verificare che il ripristino di mbam dell'accesso SQL **e l'accesso DB hardware** nel database ripristinato siano mappati al nome di accesso **$machineName $ \\MBAM Recovery and hardware DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="9d85b-172">Se non è mappato come descritto, crea un altro account di accesso con l'appartenenza a un gruppo simile e associalo al nome di accesso **$machineName $ \\MBAM Recovery and hardware DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="9d85b-173">Per automatizzare questa procedura, è possibile usare Windows PowerShell sul server B per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="9d85b-174">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-174">Note</span></span>**  
    <span data-ttu-id="9d85b-175">Sostituire i valori seguenti nell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9d85b-176">$DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9d85b-177">Il nome del server deve essere seguito da un $, come illustrato nell'esempio, ad esempio MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="9d85b-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="9d85b-178">Aggiornare i dati di connessione al database di ripristino nei server di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="9d85b-179">In ognuno dei server che esegue la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="9d85b-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="9d85b-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="9d85b-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="9d85b-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="9d85b-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="9d85b-182">Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="9d85b-183">Selezionare l'opzione **configurationStrings** dal controllo **elenco sezioni** .</span><span class="sxs-lookup"><span data-stu-id="9d85b-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="9d85b-184">Selezionare la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.</span><span class="sxs-lookup"><span data-stu-id="9d85b-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="9d85b-185">Nell' **Editor della raccolta**selezionare la riga denominata **KeyRecoveryConnectionString** durante l'aggiornamento della configurazione per l'applicazione MBAMAdministrationService o la riga denominata <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString durante l'aggiornamento della configurazione per MBAMRecoveryAndHardwareService.</span><span class="sxs-lookup"><span data-stu-id="9d85b-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="9d85b-186">Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome e l'istanza del server, ad esempio $SERVERNAME $ \ \ $SqlInstanceName $) in cui è stato spostato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="9d85b-187">Per automatizzare questa procedura, è possibile usare Windows per immettere una riga di comando simile alla seguente, in ogni server di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="9d85b-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="9d85b-188">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-188">Note</span></span>**  
   <span data-ttu-id="9d85b-189">Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="9d85b-190">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="9d85b-191">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9d85b-192">In ogni server che sta usando la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM, che si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9d85b-193">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="9d85b-194">Spostamento della funzionalità di database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9d85b-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="9d85b-195">Se si vuole trasferire il database di controllo e conformità di MBAM da un computer a un altro (ovvero, trasferire il database dal server a al server B), usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="9d85b-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="9d85b-196">Il processo include i passaggi di alto livello seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d85b-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="9d85b-197">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9d85b-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="9d85b-198">Eseguire la configurazione di MBAM sul server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="9d85b-199">Eseguire il backup del database nel server A.</span><span class="sxs-lookup"><span data-stu-id="9d85b-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="9d85b-200">Trasferire il database dal server da A a B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="9d85b-201">Ripristinare il database nel server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="9d85b-202">Configurare l'accesso al database nel server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="9d85b-203">Aggiornare i dati di connessione al database nei server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="9d85b-204">Aggiornare la stringa di connessione all'origine dati di report SSRS con la nuova posizione del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="9d85b-205">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9d85b-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="9d85b-206">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="9d85b-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9d85b-207">In ogni server che sta usando la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9d85b-208">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9d85b-209">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-209">Note</span></span>**  
    <span data-ttu-id="9d85b-210">Per eseguire questa riga di comando, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d85b-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="9d85b-211">È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="9d85b-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="9d85b-212">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9d85b-213">Eseguire la configurazione di MBAM sul server B e selezionare solo il **database di conformità e controllo** per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9d85b-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="9d85b-214">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="9d85b-215">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-215">Note</span></span>**  
    <span data-ttu-id="9d85b-216">Nota: Sostituisci i valori seguenti nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-217">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà spostato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="9d85b-218">$DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e server di ogni server di amministrazione e monitoraggio di MBAM che contatterà il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="9d85b-219">Usare un punto e virgola per separare ogni coppia di domini e server nell'elenco, ad esempio $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="9d85b-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="9d85b-220">Ogni nome del server deve essere seguito da un simbolo "$", come illustrato nell'esempio (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="9d85b-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="9d85b-221">$DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9d85b-222">$X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9d85b-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9d85b-223">Eseguire il backup del database di conformità e controllo nel server A</span><span class="sxs-lookup"><span data-stu-id="9d85b-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="9d85b-224">Per eseguire il backup del database di conformità e controllo nel server A, usare SQL Server Management Studio e l'attività denominata **backup**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="9d85b-225">Per impostazione predefinita, il nome del database è **mbam compliance database status**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="9d85b-226">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:</span><span class="sxs-lookup"><span data-stu-id="9d85b-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="9d85b-227">Eseguire il file SQL usando una riga di comando di Windows PowerShell simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9d85b-228">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-228">Note</span></span>**  
    <span data-ttu-id="9d85b-229">Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-230">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà eseguito il backup del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="9d85b-231">Trasferire il database di conformità e controllo dal server a alla B</span><span class="sxs-lookup"><span data-stu-id="9d85b-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="9d85b-232">È necessario trasferire i file seguenti dal server a al server B usando Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9d85b-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="9d85b-233">Informazioni sul database dello stato di conformità MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="9d85b-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="9d85b-234">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="9d85b-235">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-235">Note</span></span>**  
    <span data-ttu-id="9d85b-236">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-237">$SERVERNAME $-immettere il nome del server in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9d85b-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="9d85b-238">$DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9d85b-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="9d85b-239">Ripristinare il database di conformità e controllo nel server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="9d85b-240">Ripristinare il database di conformità e controllo nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="9d85b-241">Dopo aver completato l'attività, selezionare il file di backup del database selezionando l'opzione **da dispositivo** e quindi usando il comando **Aggiungi** per selezionare il file Data. bak del database di stato della conformità di mbam.</span><span class="sxs-lookup"><span data-stu-id="9d85b-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="9d85b-242">Selezionare **OK** per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="9d85b-243">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:</span><span class="sxs-lookup"><span data-stu-id="9d85b-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="9d85b-244">Eseguire il file SQL usando una riga di comando di Windows PowerShell simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9d85b-245">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-245">Note</span></span>**  
    <span data-ttu-id="9d85b-246">Sostituire il valore seguente nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-247">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà ripristinato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="9d85b-248">Configurare l'accesso al database di conformità e controllo nel server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="9d85b-249">Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Compliance status DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="9d85b-250">Verificare che l'accesso a SQL **Access mbam Compliance controllo DB** per il database ripristinato sia mappato al nome di accesso **$machineName $ \ \ mbam compliance audit DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="9d85b-251">Se non è mappato come descritto, crea un altro account di accesso con l'appartenenza a un gruppo simile e associalo al nome di accesso **$machineName $ \ \ mbam compliance audit DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="9d85b-252">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando nel server B simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="9d85b-253">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-253">Note</span></span>**  
    <span data-ttu-id="9d85b-254">Sostituire i valori seguenti nell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9d85b-255">$DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9d85b-256">Il nome del server deve essere seguito da un "$", come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9d85b-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="9d85b-257">(ad esempio, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="9d85b-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="9d85b-258">$DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="9d85b-259">Aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server</span><span class="sxs-lookup"><span data-stu-id="9d85b-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="9d85b-260">In ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="9d85b-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="9d85b-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="9d85b-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="9d85b-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="9d85b-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="9d85b-263">Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="9d85b-264">Selezionare l'opzione **configurationStrings** dal controllo **elenco sezioni** .</span><span class="sxs-lookup"><span data-stu-id="9d85b-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="9d85b-265">Selezionare la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.</span><span class="sxs-lookup"><span data-stu-id="9d85b-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="9d85b-266">Nell' **Editor della raccolta**selezionare la riga denominata **ComplianceStatusConnectionString** durante l'aggiornamento della configurazione per l'applicazione MBAMAdministrationService o la riga denominata **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** durante l'aggiornamento della configurazione per il MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="9d85b-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="9d85b-267">Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome del server e dell'istanza, ad esempio $SERVERNAME $ \ \ $SqlInstanceName, a cui è stato spostato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="9d85b-268">Per automatizzare questa procedura, è possibile usare Windows per immettere una riga di comando in ogni server di amministrazione e monitoraggio simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="9d85b-269">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-269">Note</span></span>**  
    <span data-ttu-id="9d85b-270">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-271">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="9d85b-272">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9d85b-273">In ogni server che sta usando la funzionalità di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9d85b-274">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="9d85b-275">Spostamento dei report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9d85b-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="9d85b-276">Se si vuole trasferire i report di controllo e conformità di MBAM da un computer a un altro (ovvero, trasferire i report dal server a al server B), usare la procedura seguente, che include i passaggi di alto livello seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d85b-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="9d85b-277">Eseguire la configurazione di MBAM sul server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="9d85b-278">Configurare l'accesso ai report di conformità e controllo nel server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="9d85b-279">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="9d85b-280">Aggiornare i dati di connessione dei report nei server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="9d85b-281">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9d85b-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="9d85b-282">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9d85b-283">Eseguire la configurazione di MBAM sul server B e selezionare solo la caratteristica **conformità e controllo rapporti** per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9d85b-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="9d85b-284">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="9d85b-285">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-285">Note</span></span>**  
    <span data-ttu-id="9d85b-286">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-287">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="9d85b-288">$DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9d85b-289">$PASSWORD $-immettere la password dell'account utente che verrà usato per connettersi al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9d85b-290">$X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9d85b-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9d85b-291">Configurare l'accesso ai report di conformità e controllo sul server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="9d85b-292">Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account utente che avranno accesso ai report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="9d85b-293">Aggiungere gli account utente al gruppo locale denominato MBAM report Users.</span><span class="sxs-lookup"><span data-stu-id="9d85b-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="9d85b-294">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando nel server B simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="9d85b-295">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-295">Note</span></span>**  
    <span data-ttu-id="9d85b-296">Sostituire i valori seguenti nell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9d85b-297">$DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="9d85b-298">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9d85b-299">In ogni server che sta usando la funzionalità MBAM Administration e Monitoring Server usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9d85b-300">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="9d85b-301">Aggiornare i dati di connessione al database nei server di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="9d85b-302">In ogni server che sta usando la funzionalità MBAM Administration e Monitoring Server usare la console di gestione di Internet Information Services (IIS) per aggiornare l'URL dei report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="9d85b-303">Selezionare il sito Web di **amministrazione e monitoraggio di Microsoft BitLocker** e usare la caratteristica **editor di configurazione** che è la posizione nella sezione **gestione** della **visualizzazione funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="9d85b-304">Selezionare l'opzione **appSettings** dal controllo **elenco sezioni** .</span><span class="sxs-lookup"><span data-stu-id="9d85b-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="9d85b-305">Selezionare la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.</span><span class="sxs-lookup"><span data-stu-id="9d85b-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="9d85b-306">Nell' **Editor della raccolta**selezionare la riga denominata **Microsoft. mbam. Reports. URL**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="9d85b-307">Aggiorna il valore per **Microsoft. mbam. Reports. URL** per riflettere il nome del server per il server B. Se la caratteristica conformità e rapporti di controllo è stata installata in un'istanza di SQL Reporting Services denominata, assicurarsi di aggiungere o aggiornare il nome dell'istanza all'URL, ad esempio http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....)</span><span class="sxs-lookup"><span data-stu-id="9d85b-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="9d85b-308">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando in ogni server di amministrazione e monitoraggio simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="9d85b-309">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-309">Note</span></span>**  
   <span data-ttu-id="9d85b-310">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="9d85b-311">$SERVERNAME $-immettere il nome del nome del server a cui sono stati installati i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="9d85b-312">$SRSINSTANCENAME $-immettere il nome dell'istanza di SQL Reporting Services a cui sono stati installati i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="9d85b-313">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9d85b-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="9d85b-314">In ogni server che sta usando la funzionalità MBAM Administration e Monitoring Server usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9d85b-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9d85b-315">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9d85b-316">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-316">Note</span></span>**  
    <span data-ttu-id="9d85b-317">Per eseguire questa riga di comando, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d85b-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="9d85b-318">È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="9d85b-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="9d85b-319">Spostamento della funzionalità di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="9d85b-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="9d85b-320">Se si vuole trasferire la caratteristica di amministrazione e monitoraggio dei report di MBAM da un computer a un altro (ovvero, trasferire la caratteristica dal server a al server B), usare la procedura seguente, che include i passaggi di alto livello seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d85b-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="9d85b-321">Eseguire la configurazione di MBAM sul server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="9d85b-322">Configurare l'accesso al database nel server B.</span><span class="sxs-lookup"><span data-stu-id="9d85b-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="9d85b-323">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9d85b-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9d85b-324">Eseguire la configurazione di MBAM sul server B e selezionare solo la funzionalità **amministrazione e monitoraggio server** per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9d85b-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="9d85b-325">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="9d85b-326">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-326">Note</span></span>**  
    <span data-ttu-id="9d85b-327">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9d85b-328">$SERVERNAME $ \ \ $SQLINSTANCENAME $-per il parametro COMPLIDB \ _SQLINSTANCE immettere il nome del server e l'istanza in cui si trova il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="9d85b-329">Per il parametro RECOVERYANDHWDB \ _SQLINSTANCE immettere il nome del server e l'istanza in cui si trova il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d85b-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="9d85b-330">$DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="9d85b-331">$ REPORTSSERVERURL $-immettere l'URL per la posizione Home del sito Web del servizio SQL Reporting.</span><span class="sxs-lookup"><span data-stu-id="9d85b-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="9d85b-332">Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL avrà il formato "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="9d85b-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="9d85b-333">Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL avrà il formato "http://$SERVERNAME $/ReportServer\_ $ SqlInstanceName $".</span><span class="sxs-lookup"><span data-stu-id="9d85b-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="9d85b-334">$X $-immettere **0** se si sta installando la topologia di mbam autonoma oppure **1** se si sta installando la topologia di mbam Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9d85b-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="9d85b-335">Configurare l'accesso ai database</span><span class="sxs-lookup"><span data-stu-id="9d85b-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="9d85b-336">Nel server o nei server in cui sono distribuiti il database di ripristino e la conformità e il database di controllo, usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità MBAM Administration and Monitoring Server nei gruppi locali denominati **mbam Recovery and hardware DB Access** (Recovery DB Server) e **mbam Compliance status DB Access**</span><span class="sxs-lookup"><span data-stu-id="9d85b-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="9d85b-337">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente, nel server in cui è stato distribuito il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="9d85b-338">Nel server in cui è stato distribuito il database di ripristino, è possibile usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="9d85b-339">Nota</span><span class="sxs-lookup"><span data-stu-id="9d85b-339">Note</span></span>**  
    <span data-ttu-id="9d85b-340">Sostituire il valore seguente nell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9d85b-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9d85b-341">$DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="9d85b-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="9d85b-342">Il nome del server deve essere seguito da un simbolo "$", come illustrato nell'esempio, ad esempio MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="9d85b-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="9d85b-343">$DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9d85b-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="9d85b-344">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d85b-344">Related topics</span></span>


[<span data-ttu-id="9d85b-345">Manutenzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9d85b-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









