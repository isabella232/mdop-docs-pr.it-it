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
# <span data-ttu-id="9eabc-103">Come spostare le funzionalità di MBAM 1.0 in un altro computer</span><span class="sxs-lookup"><span data-stu-id="9eabc-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="9eabc-104">In questo argomento vengono illustrati i passaggi da eseguire per trasferire una o più funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="9eabc-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="9eabc-105">Quando si spostano più funzionalità di MBAM in un altro computer, è consigliabile spostarle nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="9eabc-106">Database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="9eabc-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="9eabc-107">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9eabc-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="9eabc-108">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9eabc-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="9eabc-109">Amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="9eabc-109">Administration and Monitoring</span></span>

## <span data-ttu-id="9eabc-110">Per trasferire il database di ripristino e hardware</span><span class="sxs-lookup"><span data-stu-id="9eabc-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="9eabc-111">È possibile usare la procedura seguente per trasferire il database di MBAM Recovery e hardware da un computer a un altro (è possibile trasferire questa caratteristica del server MBAM dal server a al server B):</span><span class="sxs-lookup"><span data-stu-id="9eabc-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="9eabc-112">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="9eabc-113">Eseguire la configurazione di MBAM sul server B.</span><span class="sxs-lookup"><span data-stu-id="9eabc-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="9eabc-114">Eseguire il backup del database di MBAM Recovery e hardware nel server A.</span><span class="sxs-lookup"><span data-stu-id="9eabc-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="9eabc-115">Database di ripristino e hardware di MBAM dal server a alla B</span><span class="sxs-lookup"><span data-stu-id="9eabc-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="9eabc-116">Ripristinare il database di MBAM Recovery e hardware nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="9eabc-117">Configurare l'accesso al database di MBAM Recovery e hardware nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="9eabc-118">Aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server</span><span class="sxs-lookup"><span data-stu-id="9eabc-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="9eabc-119">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="9eabc-120">Per arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9eabc-121">Usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM in ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="9eabc-122">Il sito Web di MBAM si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9eabc-123">Per automatizzare questa procedura, è possibile usare un comando al prompt dei comandi simile al seguente, usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9eabc-124">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-124">Note</span></span>**  
    <span data-ttu-id="9eabc-125">Per eseguire il prompt dei comandi di PowerShell, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9eabc-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="9eabc-126">È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="9eabc-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="9eabc-127">Per eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="9eabc-128">Eseguire la configurazione di MBAM sul server B e selezionare il database di ripristino e hardware per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9eabc-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="9eabc-129">Per automatizzare questa procedura, è possibile usare un comando al prompt dei comandi simile al seguente, usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9eabc-130">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-130">Note</span></span>**  
    <span data-ttu-id="9eabc-131">Sostituire i valori seguenti nell'esempio precedente con quelli corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-132">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e dell'istanza in cui verrà spostato il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="9eabc-133">$DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e server di ogni applicazione MBAM e server di monitoraggio che contatteranno il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="9eabc-134">Se sono presenti più nomi di dominio e server, usare un punto e virgola per separare ognuno di essi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="9eabc-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="9eabc-135">Ad esempio, $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="9eabc-136">Inoltre, ogni nome del server deve essere seguito da a **$** .</span><span class="sxs-lookup"><span data-stu-id="9eabc-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="9eabc-137">Ad esempio, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="9eabc-138">Per eseguire il backup del database nel server A</span><span class="sxs-lookup"><span data-stu-id="9eabc-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="9eabc-139">Per eseguire il backup del database di ripristino e hardware nel server A, usare SQL Server Management Studio e l'attività denominata **backup...**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="9eabc-140">Per impostazione predefinita, il nome del database è **mbam Recovery and hardware database**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="9eabc-141">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="9eabc-142">Modificare il database di MBAM Recovery e hardware per usare la modalità di recupero completo.</span><span class="sxs-lookup"><span data-stu-id="9eabc-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="9eabc-143">Creare MBAM Recovery e dati di database hardware e dispositivi di backup logici di ripristino MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="9eabc-144">Eseguire il backup del database completo di MBAM Recovery e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-144">Back up the full MBAM Recovery and Hardware database.</span></span>

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

    **<span data-ttu-id="9eabc-145">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-145">Note</span></span>**  
    <span data-ttu-id="9eabc-146">Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-147">$PASSWORD $-immettere una password che verrà usata per crittografare il file della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="9eabc-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="9eabc-148">Eseguire il file SQL con SQL Server PowerShell e un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9eabc-149">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-149">Note</span></span>**  
    <span data-ttu-id="9eabc-150">Sostituire il valore nell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-151">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza da cui eseguire il backup del database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="9eabc-152">Per trasferire il database e il certificato dal server a alla B</span><span class="sxs-lookup"><span data-stu-id="9eabc-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="9eabc-153">Consente di trasferire i dati di MBAM Recovery e database hardware dal server a al server B usando Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="9eabc-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="9eabc-154">Per trasferire il certificato per il database crittografato, è necessario usare la procedura di automazione seguente.</span><span class="sxs-lookup"><span data-stu-id="9eabc-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="9eabc-155">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="9eabc-156">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-156">Note</span></span>**  
    <span data-ttu-id="9eabc-157">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-158">$SERVERNAME $-immettere il nome del server in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9eabc-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="9eabc-159">$DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9eabc-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="9eabc-160">Per ripristinare il database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="9eabc-161">Ripristinare il database di ripristino e hardware nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="9eabc-162">Dopo aver eseguito l'attività, scegliere il file di backup del database selezionando l'opzione **da dispositivo** e quindi usare il comando **Aggiungi** per scegliere il file **Data. bak** per il recupero e il database hardware di mbam.</span><span class="sxs-lookup"><span data-stu-id="9eabc-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="9eabc-163">Selezionare **OK** per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9eabc-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="9eabc-164">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="9eabc-165">Eliminare il certificato creato da MBAM Setup.</span><span class="sxs-lookup"><span data-stu-id="9eabc-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="9eabc-166">Aggiungi certificato</span><span class="sxs-lookup"><span data-stu-id="9eabc-166">Add certificate</span></span>

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

    <span data-ttu-id="9eabc-167">Ripristinare i dati di database hardware e ripristino di MBAM e i file di log.</span><span class="sxs-lookup"><span data-stu-id="9eabc-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="9eabc-168">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-168">Note</span></span>**  
    <span data-ttu-id="9eabc-169">Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-170">$PASSWORD $-immettere la password usata per crittografare il file della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="9eabc-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="9eabc-171">Usare Windows PowerShell per immettere una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9eabc-172">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-172">Note</span></span>**  
    <span data-ttu-id="9eabc-173">Sostituisci il valore dell'esempio che sfugge con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-174">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà ripristinato il ripristino e il database hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="9eabc-175">Configurare l'accesso al database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="9eabc-176">Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Recovery and hardware DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="9eabc-177">Per automatizzare questa procedura, è possibile usare Windows PowerShell sul server B per immettere un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="9eabc-178">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-178">Note</span></span>**  
    <span data-ttu-id="9eabc-179">Sostituire i valori dell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9eabc-180">$DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome di dominio e il nome del computer del server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9eabc-181">Il nome del server deve essere seguito da un **$** , ad esempio MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="9eabc-182">Per aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server</span><span class="sxs-lookup"><span data-stu-id="9eabc-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="9eabc-183">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio di Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="9eabc-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="9eabc-184">Servizio di amministrazione MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="9eabc-185">Servizio di ripristino e hardware di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="9eabc-186">Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="9eabc-187">Selezionare l'opzione **configurationStrings** dal controllo elenco sezioni.</span><span class="sxs-lookup"><span data-stu-id="9eabc-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="9eabc-188">Scegliere la riga denominata **(raccolta)** e aprire l' **Editor della raccolta** selezionando il pulsante sul lato destro della riga.</span><span class="sxs-lookup"><span data-stu-id="9eabc-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="9eabc-189">Nell' **Editor della raccolta**scegliere la riga denominata **KeyRecoveryConnectionString** quando è stata aggiornata la configurazione per l'applicazione "MBAMAdministrationService" oppure scegliere la riga denominata <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString, quando si aggiorna la configurazione per "MBAMRecoveryAndHardwareService".</span><span class="sxs-lookup"><span data-stu-id="9eabc-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="9eabc-190">Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome del server e l'istanza in cui è stato spostato il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="9eabc-191">Ad esempio, $SERVERNAME $ \ \ $SQLINSTANCENAME $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="9eabc-192">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell in ogni server di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="9eabc-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="9eabc-193">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-193">Note</span></span>**  
   <span data-ttu-id="9eabc-194">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="9eabc-195">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="9eabc-196">Per riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9eabc-197">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM, denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9eabc-198">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="9eabc-199">Per cambiare la funzionalità del database dello stato di conformità</span><span class="sxs-lookup"><span data-stu-id="9eabc-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="9eabc-200">Se si sceglie di trasferire la funzionalità di database di stato di conformità di MBAM da un computer a un altro, ad esempio dal server a al server B, è consigliabile usare la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="9eabc-201">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="9eabc-202">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="9eabc-203">Eseguire il backup del database nel server A</span><span class="sxs-lookup"><span data-stu-id="9eabc-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="9eabc-204">Trasferire il database dal server a alla B</span><span class="sxs-lookup"><span data-stu-id="9eabc-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="9eabc-205">Ripristinare il database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="9eabc-206">Configurare l'accesso al database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="9eabc-207">Aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server</span><span class="sxs-lookup"><span data-stu-id="9eabc-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="9eabc-208">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="9eabc-209">Per arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9eabc-210">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM, che si chiama **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9eabc-211">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9eabc-212">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-212">Note</span></span>**  
    <span data-ttu-id="9eabc-213">Per eseguire questo comando, è necessario aggiungere il modulo IIS per PowerShell all'istanza corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9eabc-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="9eabc-214">È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per consentire l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="9eabc-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="9eabc-215">Per eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="9eabc-216">Eseguire la configurazione di MBAM sul server B e selezionare la caratteristica di database dello stato di conformità per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9eabc-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="9eabc-217">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="9eabc-218">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-218">Note</span></span>**  
    <span data-ttu-id="9eabc-219">Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-220">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà spostato il database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="9eabc-221">$DOMAIN $ \ \ $SERVERNAME $-immettere i nomi di dominio e i nomi dei server di ogni applicazione MBAM e server di monitoraggio che contatteranno il database di stato conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="9eabc-222">Se sono presenti più nomi di dominio e nomi di server, usare un punto e virgola per separare ognuno di essi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="9eabc-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="9eabc-223">Ad esempio, $DOMAIN \\NOMESERVER $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="9eabc-224">Ogni nome del server deve essere seguito da un **$** come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9eabc-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="9eabc-225">Ad esempio, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="9eabc-226">$DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di stato della conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="9eabc-227">Per eseguire il backup del database di conformità nel server A</span><span class="sxs-lookup"><span data-stu-id="9eabc-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="9eabc-228">Per eseguire il backup del database di conformità nel server A, usare SQL Server Management Studio e l'attività denominata **backup...**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="9eabc-229">Per impostazione predefinita, il nome del database è **mbam compliance database status**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="9eabc-230">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:</span><span class="sxs-lookup"><span data-stu-id="9eabc-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="9eabc-231">Eseguire il file SQL con un comando simile a quello seguente usando la PowerShell per SQL Server:</span><span class="sxs-lookup"><span data-stu-id="9eabc-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9eabc-232">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-232">Note</span></span>**  
    <span data-ttu-id="9eabc-233">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-234">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza da cui verrà eseguito il backup del database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="9eabc-235">Per trasferire il database dal server a alla B</span><span class="sxs-lookup"><span data-stu-id="9eabc-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="9eabc-236">Per trasferire i file seguenti dal server a al server B, usare Esplora risorse:</span><span class="sxs-lookup"><span data-stu-id="9eabc-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="9eabc-237">Informazioni sul database dello stato di conformità MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="9eabc-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="9eabc-238">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="9eabc-239">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-239">Note</span></span>**  
    <span data-ttu-id="9eabc-240">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-241">$SERVERNAME $-immettere il nome del server in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9eabc-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="9eabc-242">$DESTINATIONSHARE $-immettere il nome della condivisione e del percorso in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="9eabc-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="9eabc-243">Per ripristinare il database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="9eabc-244">Ripristinare il database dello stato di conformità nel server B tramite SQL Server Management Studio e l'attività denominata **Ripristina database.**...</span><span class="sxs-lookup"><span data-stu-id="9eabc-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="9eabc-245">Dopo l'esecuzione dell'attività, selezionare il file di backup del database selezionando l'opzione da dispositivo e quindi usare il comando Aggiungi per scegliere il file Data. bak del database di stato della conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="9eabc-246">Fare clic su OK per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9eabc-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="9eabc-247">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script seguente-SQL:</span><span class="sxs-lookup"><span data-stu-id="9eabc-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="9eabc-248">Eseguire il file SQL con un comando simile a quello seguente usando la PowerShell per SQL Server:</span><span class="sxs-lookup"><span data-stu-id="9eabc-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="9eabc-249">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-249">Note</span></span>**  
    <span data-ttu-id="9eabc-250">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-251">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui verrà ripristinato il database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="9eabc-252">Per configurare l'accesso al database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="9eabc-253">Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nel gruppo locale denominato **mbam Compliance status DB Access**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="9eabc-254">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell sul server B:</span><span class="sxs-lookup"><span data-stu-id="9eabc-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="9eabc-255">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-255">Note</span></span>**  
    <span data-ttu-id="9eabc-256">Sostituire il valore dell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9eabc-257">$DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9eabc-258">Il nome del server deve essere seguito da a **$** . Ad esempio, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="9eabc-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="9eabc-259">$DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9eabc-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="9eabc-260">Per aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server</span><span class="sxs-lookup"><span data-stu-id="9eabc-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="9eabc-261">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per le applicazioni seguenti, ospitate nel sito Web di amministrazione e monitoraggio di Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="9eabc-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="9eabc-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="9eabc-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="9eabc-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="9eabc-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="9eabc-264">Selezionare ogni applicazione e usare la caratteristica **editor di configurazione** , che si trova nella sezione **gestione** della **visualizzazione funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="9eabc-265">Selezionare l'opzione **configurationStrings** dal controllo elenco sezioni.</span><span class="sxs-lookup"><span data-stu-id="9eabc-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="9eabc-266">Selezionare la riga denominata **(raccolta)** e aprire l'editor della raccolta selezionando il pulsante sul lato destro della riga.</span><span class="sxs-lookup"><span data-stu-id="9eabc-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="9eabc-267">Nell' **Editor della raccolta**selezionare la riga denominata **ComplianceStatusConnectionString**, quando si aggiorna la configurazione per l'applicazione MBAMAdministrationService o la riga denominata **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, quando si aggiorna la configurazione per MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="9eabc-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="9eabc-268">Aggiornare l' **origine dati =** valore per la proprietà **configurationStrings** per elencare il nome del server e il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9eabc-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="9eabc-269">Ad esempio, $SERVERNAME $ \ \ $SQLINSTANCENAME, a cui è stato spostato il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="9eabc-270">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile a quello seguente in ogni server di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="9eabc-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="9eabc-271">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-271">Note</span></span>**  
    <span data-ttu-id="9eabc-272">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-273">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e il nome dell'istanza in cui si trova il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="9eabc-274">Per riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9eabc-275">In ognuno dei server che gestiscono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9eabc-276">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="9eabc-277">PS C:\\ &gt; Start-sito Web "amministrazione e monitoraggio di Microsoft BitLocker"</span><span class="sxs-lookup"><span data-stu-id="9eabc-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="9eabc-278">Per spostare i report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9eabc-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="9eabc-279">Se si sceglie di trasferire i report di controllo e conformità di MBAM da un computer a un altro (in particolare, se si trasferisce la caratteristica dal server a al server B), è consigliabile usare la procedura e i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9eabc-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="9eabc-280">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="9eabc-281">Configurare l'accesso ai report di conformità e controllo sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="9eabc-282">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="9eabc-283">Aggiornare i dati di connessione dei report sui server di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="9eabc-284">Riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="9eabc-285">Per eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="9eabc-286">Eseguire la configurazione di MBAM sul server B e selezionare solo la funzionalità di conformità e controllo per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9eabc-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="9eabc-287">Per automatizzare questa procedura, è possibile usare un comando simile al seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="9eabc-288">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-288">Note</span></span>**  
    <span data-ttu-id="9eabc-289">Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-290">$SERVERNAME $ \ \ $SQLINSTANCENAME $-immettere il nome del server e l'istanza in cui si trova il database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="9eabc-291">$DOMAIN $ \ \ $USERNAME $-immettere il nome di dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di stato della conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="9eabc-292">$PASSWORD $-immettere la password dell'account utente che verrà usato per connettersi al database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="9eabc-293">Per configurare l'accesso ai report di conformità e controllo nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="9eabc-294">Nel server B usare lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account utente che avranno accesso ai report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9eabc-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="9eabc-295">Aggiungere gli account utente al gruppo locale denominato "utenti report MBAM".</span><span class="sxs-lookup"><span data-stu-id="9eabc-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="9eabc-296">Per automatizzare questa procedura, è possibile usare un comando simile al seguente usando Windows PowerShell nel server B.</span><span class="sxs-lookup"><span data-stu-id="9eabc-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="9eabc-297">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-297">Note</span></span>**  
    <span data-ttu-id="9eabc-298">Sostituire il valore seguente dell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9eabc-299">$DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="9eabc-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="9eabc-300">Per arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9eabc-301">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9eabc-302">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="9eabc-303">Per aggiornare i dati di connessione al database in amministrazione e monitoraggio di MBAM server</span><span class="sxs-lookup"><span data-stu-id="9eabc-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="9eabc-304">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per aggiornare l'URL dei report di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="9eabc-305">Selezionare il sito Web di **amministrazione e monitoraggio di Microsoft BitLocker** e usare la caratteristica **editor di configurazione** che si trova nella sezione **gestione** della **visualizzazione funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="9eabc-306">Selezionare l'opzione **appSettings** dal controllo elenco sezioni.</span><span class="sxs-lookup"><span data-stu-id="9eabc-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="9eabc-307">Da qui selezionare la riga denominata **(raccolta)** e aprire l'editor della **raccolta** selezionando il pulsante sul lato destro della riga.</span><span class="sxs-lookup"><span data-stu-id="9eabc-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="9eabc-308">Nell' **Editor della raccolta**selezionare la riga denominata "Microsoft. mbam. Reports. URL".</span><span class="sxs-lookup"><span data-stu-id="9eabc-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="9eabc-309">Aggiorna il valore per Microsoft. mbam. Reports. URL per riflettere il nome del server per il server B. Se la caratteristica conformità e rapporti di controllo è stata installata in un'istanza di SQL Reporting Services denominata, verificare di aggiungere o aggiornare il nome dell'istanza all'URL.</span><span class="sxs-lookup"><span data-stu-id="9eabc-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="9eabc-310">Ad esempio, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....</span><span class="sxs-lookup"><span data-stu-id="9eabc-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="9eabc-311">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile a quello seguente in ogni server di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="9eabc-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="9eabc-312">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-312">Note</span></span>**  
   <span data-ttu-id="9eabc-313">Sostituire il valore dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="9eabc-314">$SERVERNAME $-immettere il nome del server a cui sono stati installati i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9eabc-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="9eabc-315">$SRSINSTANCENAME $-immettere il nome dell'istanza di SQL Reporting Services a cui sono stati installati i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9eabc-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="9eabc-316">Per riprendere tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="9eabc-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="9eabc-317">In ognuno dei server che eseguono la funzionalità di amministrazione e monitoraggio di MBAM, usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web MBAM denominato **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="9eabc-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="9eabc-318">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="9eabc-319">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-319">Note</span></span>**  
    <span data-ttu-id="9eabc-320">Per eseguire questo comando, il modulo IIS per PowerShell deve essere aggiunto all'istanza corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9eabc-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="9eabc-321">È inoltre necessario aggiornare i criteri di esecuzione di PowerShell per abilitare l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="9eabc-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="9eabc-322">Per trasferire la funzionalità di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="9eabc-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="9eabc-323">Se si sceglie di trasferire la caratteristica di amministrazione e monitoraggio di MBAM da un computer a un altro, se si trasferisce la caratteristica dal server a al server B, è consigliabile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="9eabc-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="9eabc-324">Il processo include i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9eabc-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="9eabc-325">Eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="9eabc-326">Configurare l'accesso al database nel server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="9eabc-327">Per eseguire la configurazione di MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="9eabc-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="9eabc-328">Eseguire la configurazione di MBAM sul server B e selezionare solo la caratteristica di amministrazione per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9eabc-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="9eabc-329">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9eabc-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="9eabc-330">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-330">Note</span></span>**  
    <span data-ttu-id="9eabc-331">Sostituire i valori dell'esempio precedente con quelli che corrispondono all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="9eabc-332">$SERVERNAME $ \ \ $SQLINSTANCENAME $-per il parametro COMPLIDB \ _SQLINSTANCE, immettere il nome del server e l'istanza in cui si trova il database dello stato di conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="9eabc-333">Per il parametro RECOVERYANDHWDB \ _SQLINSTANCE, immettere il nome del server e l'istanza in cui si trova il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="9eabc-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="9eabc-334">$DOMAIN $ \ \ $USERNAME $-immettere il dominio e il nome utente che verranno usati dalla funzionalità di report di conformità e controllo per connettersi al database di stato della conformità.</span><span class="sxs-lookup"><span data-stu-id="9eabc-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="9eabc-335">$ REPORTSSERVERURL $-immettere l'URL per la posizione Home del sito Web del servizio SQL Reporting.</span><span class="sxs-lookup"><span data-stu-id="9eabc-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="9eabc-336">Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL verrà formattato come "http://$SERVERNAME $/ReportServer".</span><span class="sxs-lookup"><span data-stu-id="9eabc-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="9eabc-337">Se i report sono stati installati in un'istanza di SRS predefinita, il formato dell'URL verrà formattato in "http://$SERVERNAME $/ReportServer\_ $ SqlInstanceName $".</span><span class="sxs-lookup"><span data-stu-id="9eabc-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="9eabc-338">Per configurare l'accesso ai database</span><span class="sxs-lookup"><span data-stu-id="9eabc-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="9eabc-339">In server o server in cui il ripristino e l'hardware e i database di conformità e controllo vengono distribuiti, USA lo snap-in utenti e gruppi locali di Server Manager per aggiungere gli account del computer da ogni server che esegue la funzionalità di amministrazione e monitoraggio di MBAM nei gruppi locali denominati "MBAM Recovery and hardware DB Access" (Recovery and hardware DB Server) e "MBAM Compliance status DB Access" (conformità e audit DB Server).</span><span class="sxs-lookup"><span data-stu-id="9eabc-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="9eabc-340">Per automatizzare questa procedura, è possibile usare un comando simile a quello seguente usando Windows PowerShell nel server in cui sono stati distribuiti i database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9eabc-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="9eabc-341">Nel server in cui sono stati distribuiti i database di ripristino e hardware eseguire un comando simile a quello seguente usando Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9eabc-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="9eabc-342">Nota</span><span class="sxs-lookup"><span data-stu-id="9eabc-342">Note</span></span>**  
    <span data-ttu-id="9eabc-343">Sostituire il valore dell'esempio precedente con i valori applicabili per l'ambiente:</span><span class="sxs-lookup"><span data-stu-id="9eabc-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="9eabc-344">$DOMAIN $ \ \ $SERVERNAME $ $-immettere il nome del dominio e del computer del server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="9eabc-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="9eabc-345">Il nome del server deve essere seguito da a **$** .</span><span class="sxs-lookup"><span data-stu-id="9eabc-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="9eabc-346">Ad esempio, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="9eabc-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="9eabc-347">$DOMAIN $ \ \ $REPORTSUSERNAME $-immettere il nome dell'account utente usato per configurare l'origine dati per i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="9eabc-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="9eabc-348">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eabc-348">Related topics</span></span>


[<span data-ttu-id="9eabc-349">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="9eabc-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









