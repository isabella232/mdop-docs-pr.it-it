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
# <span data-ttu-id="b9edf-103">Come spostare i database di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b9edf-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="b9edf-104">Usare queste procedure per trasferire i database seguenti da un computer a un altro; dal server a al server B, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b9edf-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="b9edf-105">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="b9edf-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="b9edf-106">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="b9edf-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="b9edf-107">È importante che i database vengano ripristinati nel computer B prima di eseguire la configurazione guidata di MBAM per aggiornarli/configurarli.</span><span class="sxs-lookup"><span data-stu-id="b9edf-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="b9edf-108">Se i database non sono presenti, la configurazione guidata crea nuovi database vuoti.</span><span class="sxs-lookup"><span data-stu-id="b9edf-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="b9edf-109">Quando i database esistenti vengono ripristinati, questo processo interrompe la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9edf-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="b9edf-110">Ripristinare prima i database, quindi eseguire la configurazione guidata di MBAM, scegliere l'opzione database e la configurazione guidata verrà "connessa" ai database ripristinati. aggiornarli, se necessario, come parte del processo.</span><span class="sxs-lookup"><span data-stu-id="b9edf-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="b9edf-111">Se si stanno spostando più funzionalità, spostarle nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="b9edf-112">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="b9edf-112">Recovery Database</span></span>

2.  <span data-ttu-id="b9edf-113">Database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="b9edf-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="b9edf-114">Rapporti</span><span class="sxs-lookup"><span data-stu-id="b9edf-114">Reports</span></span>

4.  <span data-ttu-id="b9edf-115">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b9edf-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="b9edf-116">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="b9edf-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="b9edf-117">Per eseguire gli script di Windows PowerShell di esempio forniti in questo argomento, è necessario aggiornare i criteri di esecuzione di Windows PowerShell per consentire l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="b9edf-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="b9edf-118">Per istruzioni, vedere [eseguire script di Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b9edf-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="b9edf-119">Trasferire il database di ripristino</span><span class="sxs-lookup"><span data-stu-id="b9edf-119">Move the Recovery Database</span></span>

<span data-ttu-id="b9edf-120">I passaggi di alto livello per lo spostamento del database di ripristino sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9edf-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="b9edf-121">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="b9edf-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="b9edf-122">Eseguire il backup del database di ripristino nel server A</span><span class="sxs-lookup"><span data-stu-id="b9edf-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="b9edf-123">Trasferire il database di ripristino dal server a al server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="b9edf-124">Ripristinare il database di ripristino nel server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="b9edf-125">Configurare l'accesso al database nel server B e aggiornare i dati di connessione</span><span class="sxs-lookup"><span data-stu-id="b9edf-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="b9edf-126">Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="b9edf-127">Riprendere l'istanza del sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b9edf-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="b9edf-128">Come si trasferisce il database di ripristino</span><span class="sxs-lookup"><span data-stu-id="b9edf-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="b9edf-129">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9edf-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="b9edf-130">In ogni server che sta usando il sito Web di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b9edf-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="b9edf-131">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="b9edf-132">Per eseguire questo comando, è necessario aggiungere il modulo Internet Information Services (IIS) per Windows PowerShell all'istanza corrente di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9edf-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="b9edf-133">Eseguire il backup del database di ripristino nel server A</span><span class="sxs-lookup"><span data-stu-id="b9edf-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="b9edf-134">Usare l'attività di **backup** in SQL Server Management Studio per eseguire il backup del database di ripristino nel server a.  Per impostazione predefinita, il nome del database è il **database di ripristino MBAM**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="b9edf-135">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente e modificare il database di ripristino di MBAM per usare la modalità di recupero completo:</span><span class="sxs-lookup"><span data-stu-id="b9edf-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

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

3.  <span data-ttu-id="b9edf-136">Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="b9edf-137">**$Password $** -password che si usa per crittografare il file della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b9edf-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="b9edf-138">In Windows PowerShell eseguire lo script archiviato nel file e simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="b9edf-139">Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="b9edf-140">**$ServerName $ \ $SqlInstanceName $** -nome del server e istanza da cui verrà eseguito il backup del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="b9edf-141">Trasferire il database di ripristino dal server a al server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="b9edf-142">USA Esplora risorse per trasferire il file **Data. bak del database di ripristino di mbam** dal server a al server B.</span><span class="sxs-lookup"><span data-stu-id="b9edf-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="b9edf-143">Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="b9edf-144">Usare le informazioni nella tabella seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="b9edf-145">Parametro</span><span class="sxs-lookup"><span data-stu-id="b9edf-145">Parameter</span></span>**        | **<span data-ttu-id="b9edf-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9edf-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="b9edf-147">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="b9edf-147">$SERVERNAME$</span></span>       | <span data-ttu-id="b9edf-148">Nome del server in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="b9edf-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="b9edf-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="b9edf-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="b9edf-150">Nome della condivisione e del percorso in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="b9edf-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="b9edf-151">Ripristinare il database di ripristino nel server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="b9edf-152">Ripristinare il database di ripristino nel server B usando l'attività **Ripristina database** in SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b9edf-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="b9edf-153">Al termine dell'attività precedente, selezionare **da dispositivo**e quindi selezionare il file di backup del database.</span><span class="sxs-lookup"><span data-stu-id="b9edf-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="b9edf-154">Usare il comando **Aggiungi** per selezionare il file **Data. bak del database di ripristino di mbam** e fare clic su **OK** per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="b9edf-155">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

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

5.  <span data-ttu-id="b9edf-156">Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="b9edf-157">**$Password $** -password usata per crittografare il file della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b9edf-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="b9edf-158">In Windows PowerShell eseguire lo script archiviato nel file e simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="b9edf-159">Usa il valore seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="b9edf-160">**$ServerName $ \ $SqlInstanceName $** -nome del server e istanza in cui verrà ripristinato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="b9edf-161">Configurare l'accesso al database nel server B e aggiornare i dati di connessione</span><span class="sxs-lookup"><span data-stu-id="b9edf-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="b9edf-162">Verificare che l'account di accesso dell'utente di Microsoft SQL Server che consente l'accesso al database di ripristino nel database ripristinato sia mappato all'indirizzo di Access fornito durante il processo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9edf-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="b9edf-163">Se l'account di accesso non è lo stesso, creare un account di accesso tramite SQL Server Management Studio e associarlo all'utente del database esistente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="b9edf-164">Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per i siti Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9edf-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="b9edf-165">Modificare la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="b9edf-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="b9edf-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="b9edf-167">Aggiornare il valore dell' **origine dati** con il nome del server e dell'istanza, ad esempio \ $ServerName \ $ \ \ \ $SqlInstanceName, in cui è stato spostato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="b9edf-168">Aggiornare il valore del **catalogo iniziale** con il nome del database recuperato.</span><span class="sxs-lookup"><span data-stu-id="b9edf-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="b9edf-169">Per automatizzare il processo, è possibile usare il prompt dei comandi di Windows PowerShell per immettere una riga di comando nel server di amministrazione e monitoraggio simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

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
   ><span data-ttu-id="b9edf-170">Questa stringa di connessione è condivisa da tutte le applicazioni Web di MBAM locali.</span><span class="sxs-lookup"><span data-stu-id="b9edf-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="b9edf-171">Pertanto, deve essere aggiornata solo una volta per ogni server.</span><span class="sxs-lookup"><span data-stu-id="b9edf-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="b9edf-172">Usare la tabella seguente per sostituire i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="b9edf-173">Parametro</span><span class="sxs-lookup"><span data-stu-id="b9edf-173">Parameter</span></span>|<span data-ttu-id="b9edf-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9edf-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="b9edf-175">$SERVERNAME $/\ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="b9edf-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="b9edf-176">Nome server e istanza di SQL Server in cui si trova il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="b9edf-177">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="b9edf-177">$DATABASE$</span></span>|<span data-ttu-id="b9edf-178">Nome del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="b9edf-179">Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="b9edf-180">Installare il software MBAM 2,5 Server sul server B. Per informazioni dettagliate, vedere [installazione del software server MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="b9edf-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="b9edf-181">Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **database di ripristino** .</span><span class="sxs-lookup"><span data-stu-id="b9edf-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="b9edf-182">Per informazioni dettagliate su come configurare i database, vedere [come configurare i database di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="b9edf-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="b9edf-183">In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamDatabase** per configurare il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="b9edf-184">Riprendere l'istanza del sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b9edf-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="b9edf-185">Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b9edf-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="b9edf-186">Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="b9edf-187">Per eseguire questo comando, è necessario aggiungere il modulo IIS per Windows PowerShell all'istanza corrente di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9edf-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="b9edf-188">Trasferire il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="b9edf-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="b9edf-189">I passaggi di alto livello per lo spostamento del database di conformità e controllo sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9edf-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="b9edf-190">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="b9edf-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="b9edf-191">Eseguire il backup del database di conformità e controllo nel server A</span><span class="sxs-lookup"><span data-stu-id="b9edf-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="b9edf-192">Trasferire il database di conformità e controllo dal server a al server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="b9edf-193">Ripristinare il database di conformità e controllo nel server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="b9edf-194">Configurare l'accesso al database nel server B e aggiornare i dati di connessione</span><span class="sxs-lookup"><span data-stu-id="b9edf-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="b9edf-195">Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="b9edf-196">Riprendere l'istanza del sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b9edf-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="b9edf-197">Come si trasferisce il database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="b9edf-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="b9edf-198">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="b9edf-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="b9edf-199">In ogni server che sta usando il sito Web di amministrazione e monitoraggio di MBAM, usa la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b9edf-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="b9edf-200">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="b9edf-201">Per eseguire questo comando, è necessario aggiungere il modulo Internet Information Services (IIS) per Windows PowerShell all'istanza corrente di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9edf-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="b9edf-202">Eseguire il backup del database di conformità e controllo nel server A</span><span class="sxs-lookup"><span data-stu-id="b9edf-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="b9edf-203">Usare l'attività di **backup** in SQL Server Management Studio per eseguire il backup del database di conformità e controllo nel server a. Per impostazione predefinita, il nome del database è **mbam compliance database status**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="b9edf-204">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

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

3.  <span data-ttu-id="b9edf-205">Eseguire lo script archiviato nel file con estensione SQL usando un comando di Windows PowerShell simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="b9edf-206">Usando il valore seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="b9edf-207">**$ServerName $ \ $SqlInstanceName $** -nome del server e istanza da cui verrà eseguito il backup del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="b9edf-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="b9edf-208">Trasferire il database di conformità e controllo dal server a al server B \* \*</span><span class="sxs-lookup"><span data-stu-id="b9edf-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="b9edf-209">USA Esplora risorse per trasferire il file **Data. bak di database di stato della conformità di mbam** dal server a al server B.</span><span class="sxs-lookup"><span data-stu-id="b9edf-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="b9edf-210">Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="b9edf-211">Usando la tabella seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="b9edf-212">Parametro</span><span class="sxs-lookup"><span data-stu-id="b9edf-212">Parameter</span></span>**        | **<span data-ttu-id="b9edf-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9edf-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="b9edf-214">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="b9edf-214">$SERVERNAME$</span></span>       | <span data-ttu-id="b9edf-215">Nome del server in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="b9edf-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="b9edf-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="b9edf-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="b9edf-217">Nome della condivisione e del percorso in cui verranno copiati i file.</span><span class="sxs-lookup"><span data-stu-id="b9edf-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="b9edf-218">Ripristinare il database di conformità e controllo nel server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="b9edf-219">Ripristinare il database di conformità e controllo nel server B usando l'attività **Ripristina database** in SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b9edf-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="b9edf-220">Al termine dell'attività precedente, selezionare **da dispositivo**e quindi selezionare il file di backup del database.</span><span class="sxs-lookup"><span data-stu-id="b9edf-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="b9edf-221">Usare il comando **Aggiungi** per selezionare il file **Data. bak di database di stato della conformità di mbam** e fare clic su **OK** per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="b9edf-222">Per automatizzare questa procedura, creare un file SQL (con estensione SQL) che contiene lo script SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="b9edf-223">In Windows PowerShell eseguire lo script archiviato nel file e simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="b9edf-224">Usando il valore seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="b9edf-225">**$ServerName $ \ $SqlInstanceName $** -nome del server e istanza in cui verrà ripristinato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="b9edf-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="b9edf-226">Configurare l'accesso al database nel server B e aggiornare i dati di connessione</span><span class="sxs-lookup"><span data-stu-id="b9edf-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="b9edf-227">Verificare che l'account di accesso dell'utente di Microsoft SQL Server che consente l'accesso al database di conformità e di controllo nel database ripristinato sia mappato con quello specificato durante il processo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9edf-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="b9edf-228">Se l'account di accesso non è lo stesso, creare un account di accesso tramite SQL Server Management Studio e associarlo all'utente del database esistente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="b9edf-229">Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per aggiornare le informazioni della stringa di connessione per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="b9edf-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="b9edf-230">Modificare la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="b9edf-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="b9edf-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="b9edf-232">Aggiornare il valore dell' **origine dati** con il nome del server e dell'istanza, ad esempio \ $ServerName \ $ \ \ \ $SqlInstanceName, in cui è stato spostato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="b9edf-233">Aggiornare il valore del **catalogo iniziale** con il nome del database recuperato.</span><span class="sxs-lookup"><span data-stu-id="b9edf-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="b9edf-234">Per automatizzare il processo, è possibile usare il prompt dei comandi di Windows PowerShell per immettere una riga di comando nel server di amministrazione e monitoraggio simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="b9edf-235">Questa stringa di connessione è condivisa da tutte le applicazioni Web di MBAM locali.</span><span class="sxs-lookup"><span data-stu-id="b9edf-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="b9edf-236">Pertanto, deve essere aggiornata solo una volta per ogni server.</span><span class="sxs-lookup"><span data-stu-id="b9edf-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="b9edf-237">Usando la tabella seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b9edf-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="b9edf-238">Parametro</span><span class="sxs-lookup"><span data-stu-id="b9edf-238">Parameter</span></span> | <span data-ttu-id="b9edf-239">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9edf-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="b9edf-240">$SERVERNAME $ \ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="b9edf-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="b9edf-241">Nome server e istanza di SQL Server in cui si trova il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9edf-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="b9edf-242">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="b9edf-242">$DATABASE$</span></span>|<span data-ttu-id="b9edf-243">Nome del database recuperato.</span><span class="sxs-lookup"><span data-stu-id="b9edf-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="b9edf-244">Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="b9edf-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="b9edf-245">Installare il software MBAM 2,5 Server sul server B. Per informazioni dettagliate, vedere [installazione del software server MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="b9edf-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="b9edf-246">Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **di database di conformità e controllo** .</span><span class="sxs-lookup"><span data-stu-id="b9edf-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="b9edf-247">Per informazioni dettagliate su come configurare i database, vedere [come configurare i database di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="b9edf-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="b9edf-248">In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamDatabase** per configurare il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="b9edf-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="b9edf-249">Riprendere l'istanza del sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="b9edf-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="b9edf-250">Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b9edf-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="b9edf-251">Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b9edf-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="b9edf-252">Per eseguire questo comando, è necessario aggiungere il modulo IIS per Windows PowerShell all'istanza corrente di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9edf-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
