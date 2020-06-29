---
title: Note sulla versione di MBAM 2.0 SP1
description: Note sulla versione di MBAM 2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825585"
---
# <span data-ttu-id="6eeb3-103">Note sulla versione di MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="6eeb3-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="6eeb3-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="6eeb3-105">Leggere queste note sulla versione accuratamente prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="6eeb3-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente l'amministrazione e il monitoraggio di BitLocker di 2,0 SP1 e contengono informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="6eeb3-107">Se c'è una differenza tra queste note sulla versione e altre documentazioni di MBAM 2,0 SP1, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="6eeb3-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="6eeb3-109">Problemi noti di MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6eeb3-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="6eeb3-110">Questa sezione contiene problemi noti per MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="6eeb3-111">L'aggiornamento di MBAM con la topologia integrata di Configuration Manager per MBAM 2,0 SP1 richiede la rimozione manuale degli oggetti di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6eeb3-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="6eeb3-112">Se si usa MBAM con Configuration Manager e si vuole eseguire l'aggiornamento a MBAM 2,0 SP1, è necessario rimuovere manualmente tutti gli oggetti di Configuration Manager installati in Configuration Manager come parte dell'installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="6eeb3-113">Gli oggetti che è necessario rimuovere manualmente sono i report di MBAM, la raccolta di computer supportati MBAM e la previsione di configurazione della protezione BitLocker e gli elementi di configurazione associati.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="6eeb3-114">**Soluzione alternativa**: aggiornare gli oggetti di Configuration Manager completando i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6eeb3-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="6eeb3-115">Eseguire il backup dei dati di conformità esistenti in un file esterno, come descritto nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="6eeb3-116">**Nota**  Tutti i dati di conformità di BitLocker esistenti verranno eliminati quando si elimina la previsione esistente in Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="6eeb3-117">I dati verranno rigenerati nel tempo, ma è consigliabile salvare una copia dei dati nel caso siano necessari i dati di conformità per un determinato computer prima che i dati di conformità vengano rigenerati.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="6eeb3-118">Per salvare i dati cronologici relativi alla conformità di BitLocker, aprire il report **Dettagli conformità di BitLocker Enterprise** .</span><span class="sxs-lookup"><span data-stu-id="6eeb3-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="6eeb3-119">Fare clic sull'icona **Salva** nel report e selezionare **Excel**.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="6eeb3-120">Il report salvato conterrà dati come il nome del computer, il nome di dominio, lo stato di conformità, l'esenzione, gli utenti del dispositivo, i dettagli dello stato di conformità e la data/ora dell'ultimo contatto.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="6eeb3-121">Alcune informazioni, ad esempio informazioni dettagliate sul volume e forza di crittografia, non vengono salvate.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="6eeb3-122">Disinstallare **mbam** dal server tramite il programma di installazione di **mbam** .</span><span class="sxs-lookup"><span data-stu-id="6eeb3-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="6eeb3-123">Eliminare manualmente gli oggetti seguenti da Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="6eeb3-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="6eeb3-124">Raccolta di computer supportati MBAM</span><span class="sxs-lookup"><span data-stu-id="6eeb3-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="6eeb3-125">Previsione protezione BitLocker</span><span class="sxs-lookup"><span data-stu-id="6eeb3-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="6eeb3-126">Elemento di configurazione protezione unità sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="6eeb3-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="6eeb3-127">Elemento di configurazione della protezione delle unità dati fisse di BitLocker</span><span class="sxs-lookup"><span data-stu-id="6eeb3-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="6eeb3-128">Eliminare manualmente la cartella di MBAM Reports nel sito di SQL Server Reporting Services di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="6eeb3-129">A tale scopo, effettua le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="6eeb3-129">To do this:</span></span>

    1.  <span data-ttu-id="6eeb3-130">Usare Internet Explorer per passare al punto di Reporting Services, ad esempio http:// &lt; yourcmserver &gt; /Reports.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="6eeb3-131">Fare clic sul collegamento codice sito di Configuration Manager appropriato.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="6eeb3-132">Eliminare la cartella MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="6eeb3-133">Usare il programma di installazione di MBAM server per reinstallare gli oggetti di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="6eeb3-134">I computer client inizieranno a caricare di nuovo i dati di conformità di BitLocker nel tempo.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="6eeb3-135">Il pulsante Invia in Self-Service Portal non funziona in Internet Explorer10</span><span class="sxs-lookup"><span data-stu-id="6eeb3-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="6eeb3-136">Quando si usa Internet Explorer10 per accedere al sito Web di amministrazione e monitoraggio, il pulsante **Invia** nel sito Web non funziona.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="6eeb3-137">**Soluzione alternativa**: nel server in cui è stato installato il sito Web di amministrazione e monitoraggio installare l' [hotfix per i file di definizione del browser ASP.NET](https://go.microsoft.com/fwlink/?LinkId=317798).</span><span class="sxs-lookup"><span data-stu-id="6eeb3-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="6eeb3-138">I nomi di dominio internazionali non sono supportati</span><span class="sxs-lookup"><span data-stu-id="6eeb3-138">International domain names are not supported</span></span>

<span data-ttu-id="6eeb3-139">MBAM 2,0 SP1 non supporta i nomi di dominio internazionali.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="6eeb3-140">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-140">**Workaround**: None.</span></span>

### <span data-ttu-id="6eeb3-141">I report nel sito Web amministrazione e monitoraggio visualizzano un avviso se SSL non è configurato in SSRS</span><span class="sxs-lookup"><span data-stu-id="6eeb3-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="6eeb3-142">Se SQLServer Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL per i report verrà impostato su HTTP invece che su HTTPS quando si installa il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="6eeb3-143">Se si passa al sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto".</span><span class="sxs-lookup"><span data-stu-id="6eeb3-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="6eeb3-144">**Soluzione alternativa**: per risolvere il problema, configurare SSL in **Gestione configurazione di Reporting Services** nel server mbam in cui è installato SqlServer Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="6eeb3-145">Disinstallare e quindi reinstallare il sito Web di amministrazione e monitoraggio Server.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="6eeb3-146">Se si fa clic di nuovo nel report di riepilogo conformità, potrebbe essere visualizzato un errore</span><span class="sxs-lookup"><span data-stu-id="6eeb3-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="6eeb3-147">Se si esegue il drill-down in un report di riepilogo conformità e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe verificarsi un errore.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="6eeb3-148">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-148">**Workaround**: None.</span></span>

### <span data-ttu-id="6eeb3-149">Solo spazio usato la crittografia non funziona correttamente</span><span class="sxs-lookup"><span data-stu-id="6eeb3-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="6eeb3-150">Se si crittografa un computer per la prima volta dopo l'installazione del client MBAM e si imposta un oggetto Criteri di gruppo per implementare la crittografia solo spazio usato, MBAM crittografa erroneamente l'intero disco invece di crittografare solo lo spazio usato del disco.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="6eeb3-151">Se un computer è già crittografato con la crittografia solo spazio usato prima di installare il client MBAM ed è stato impostato lo stesso oggetto Criteri di gruppo crittografia solo spazio usato, MBAM riconosce l'impostazione e segnala correttamente la crittografia nei report di conformità.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="6eeb3-152">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-152">**Workaround**: None.</span></span>

### <span data-ttu-id="6eeb3-153">La forza di cifratura viene visualizzata in modo non corretto nel report conformità computer</span><span class="sxs-lookup"><span data-stu-id="6eeb3-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="6eeb3-154">Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo della forza di cifratura, il report conformità computer nella topologia integrata di Configuration Manager Visualizza sempre **sconosciuto** per il livello di cifratura, anche quando l'intensità di cifratura usa il valore predefinito della crittografia a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="6eeb3-155">Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="6eeb3-156">**Soluzione alternativa**: impostare sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di cifratura.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="6eeb3-157">La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="6eeb3-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="6eeb3-158">Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="6eeb3-159">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-159">**Workaround**: None.</span></span> <span data-ttu-id="6eeb3-160">La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="6eeb3-161">La configurazione di sicurezza avanzata può causare la visualizzazione non corretta di report</span><span class="sxs-lookup"><span data-stu-id="6eeb3-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="6eeb3-162">Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di **Access denied** quando si prova a visualizzare i report nel server mbam.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="6eeb3-163">Per impostazione predefinita, la configurazione di sicurezza avanzata viene attivata per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="6eeb3-164">**Soluzione alternativa**: se il messaggio di **accesso negato** viene visualizzato quando si prova a visualizzare i report nel server mbam, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="6eeb3-165">È anche possibile visualizzare in alternativa i report di un altro computer in cui la configurazione di sicurezza avanzata non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="6eeb3-166">L'installazione di MBAM server non riesce quando si esegue l'aggiornamento da SQLServer2008 a SQLServer2012</span><span class="sxs-lookup"><span data-stu-id="6eeb3-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="6eeb3-167">Se si esegue l'aggiornamento da SQLServer2008 a SQLServer2012 e quindi si prova a installare il database di conformità e di controllo o il database di ripristino, l'installazione non riesce e viene eseguito il rollback.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="6eeb3-168">Il problema si verifica perché il file SQLCMD.exe obbligatorio è stato rimosso durante l'aggiornamento di SQLServer e non può essere trovato dal programma di installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="6eeb3-169">Le righe del file di log MSI possono avere un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="6eeb3-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="6eeb3-170">RunDbInstallScript recupero DB CA: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript recupero DB CA: dbInstance-xxxxxx\\I01RunDbInstallScript Recovery DB CA: SqlScript-C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration e Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: defaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: PercorsoDatiPredefinito-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript recupero DB CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recupero DB CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" PercorsoDatiPredefinito = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recupero DB CA: iniziare a eseguire l'installazione del database di ripristino scriptRunDbInstallScript recupero DB CA: il file di log sqlcmd si trova in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recupero DB eccezione CA: installare l'eccezione di output della riga di comando dell'azione personalizzata del database di ripristino: il sistema non riesce a trovare il file specificato</span><span class="sxs-lookup"><span data-stu-id="6eeb3-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="6eeb3-171">Il server di Windows Installer di MBAM è hardcoded per trovare il percorso SQLCMD.exe guardando il valore della stringa Path nel registro di sistema in HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="6eeb3-172">La chiave è ancora presente durante la migrazione da SQLServer2008 a SQLServer2012, ma il percorso a cui fa riferimento il valore dei dati non contiene il file SQLCMD.exe, perché il processo SqlUpgrade ha rimosso il file.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="6eeb3-173">**Soluzione alternativa**: rinominare temporaneamente il valore stringa Path di HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup in **path \ _old**e quindi eseguire di nuovo Windows Installer sul server mbam.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="6eeb3-174">Dopo aver completato l'installazione e creato i database in SQLServer2012, rinominare **path \ _old** su **path**.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="6eeb3-175">Aggiornamenti rapidi e articoli della Knowledge base per MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6eeb3-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="6eeb3-176">Questa sezione contiene gli aggiornamenti rapidi e gli articoli della KB per MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="6eeb3-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="6eeb3-177">Articolo KB</span><span class="sxs-lookup"><span data-stu-id="6eeb3-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="6eeb3-178">Title</span><span class="sxs-lookup"><span data-stu-id="6eeb3-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="6eeb3-179">Link</span><span class="sxs-lookup"><span data-stu-id="6eeb3-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-180">2831166</span><span class="sxs-lookup"><span data-stu-id="6eeb3-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-181">L'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 non riesce con &quot; gli oggetti di System Center cm già installati&quot;</span><span class="sxs-lookup"><span data-stu-id="6eeb3-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="6eeb3-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-183">2870849</span><span class="sxs-lookup"><span data-stu-id="6eeb3-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-184">Gli utenti non possono recuperare la chiave di ripristino di BitLocker usando il portale self service di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6eeb3-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="6eeb3-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-186">2756402</span><span class="sxs-lookup"><span data-stu-id="6eeb3-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-187">Il client MBAM fallirebbe con l'ID evento 4 e il codice di errore 0x8004100E nella descrizione dell'evento</span><span class="sxs-lookup"><span data-stu-id="6eeb3-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="6eeb3-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-189">2620287</span><span class="sxs-lookup"><span data-stu-id="6eeb3-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-190">Messaggio di errore "errore del server nell'applicazione"/Reports "quando si fa clic sulla scheda report in MBAM</span><span class="sxs-lookup"><span data-stu-id="6eeb3-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="6eeb3-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-192">2639518</span><span class="sxs-lookup"><span data-stu-id="6eeb3-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-193">Errore durante l'apertura di report di conformità Enterprise o computer in MBAM</span><span class="sxs-lookup"><span data-stu-id="6eeb3-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="6eeb3-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-195">2620269</span><span class="sxs-lookup"><span data-stu-id="6eeb3-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-196">I report di MBAM Enterprise non vengono aggiornati</span><span class="sxs-lookup"><span data-stu-id="6eeb3-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="6eeb3-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-198">2712461</span><span class="sxs-lookup"><span data-stu-id="6eeb3-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-199">L'installazione di MBAM in un controller di dominio non è supportata</span><span class="sxs-lookup"><span data-stu-id="6eeb3-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="6eeb3-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-201">2876732</span><span class="sxs-lookup"><span data-stu-id="6eeb3-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-202">Viene visualizzato il codice di errore 0x80071a90 durante la configurazione dell'integrazione di MBAM 2.0 standalone o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6eeb3-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="6eeb3-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-204">2754259</span><span class="sxs-lookup"><span data-stu-id="6eeb3-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-205">MBAM e comunicazioni di rete sicure</span><span class="sxs-lookup"><span data-stu-id="6eeb3-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="6eeb3-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-207">2870842</span><span class="sxs-lookup"><span data-stu-id="6eeb3-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-208">La configurazione di MBAM 2.0 non riesce durante lo scenario di integrazione di Configuration Manager con SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eeb3-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="6eeb3-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-210">2668533</span><span class="sxs-lookup"><span data-stu-id="6eeb3-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-211">La configurazione di MBAM non riesce se SQL SSRS non è configurato correttamente</span><span class="sxs-lookup"><span data-stu-id="6eeb3-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="6eeb3-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-213">2870847</span><span class="sxs-lookup"><span data-stu-id="6eeb3-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-214">La configurazione di MBAM 2,0 non riesce con l' &quot; errore di recupero delle impostazioni del ruolo del server di Configuration Manager per &#39;ruolo&#39; del punto di Reporting Services&quot;</span><span class="sxs-lookup"><span data-stu-id="6eeb3-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="6eeb3-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-216">2870839</span><span class="sxs-lookup"><span data-stu-id="6eeb3-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-217">I report di MBAM 2.0 Enterprise non vengono aggiornati nella topologia standalone di MBAM 2.0 a causa di un errore di CreateCache processo SQL</span><span class="sxs-lookup"><span data-stu-id="6eeb3-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="6eeb3-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-219">2620269</span><span class="sxs-lookup"><span data-stu-id="6eeb3-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-220">I report di MBAM Enterprise non vengono aggiornati</span><span class="sxs-lookup"><span data-stu-id="6eeb3-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="6eeb3-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6eeb3-222">2935997</span><span class="sxs-lookup"><span data-stu-id="6eeb3-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-223">I computer supportati da MBAM Reporting di conformità non corretto include i prodotti non supportati</span><span class="sxs-lookup"><span data-stu-id="6eeb3-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="6eeb3-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6eeb3-225">2612822</span><span class="sxs-lookup"><span data-stu-id="6eeb3-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="6eeb3-226">Il record del computer viene rifiutato in MBAM</span><span class="sxs-lookup"><span data-stu-id="6eeb3-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="6eeb3-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="6eeb3-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6eeb3-228">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6eeb3-228">Related topics</span></span>


[<span data-ttu-id="6eeb3-229">Informazioni su MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="6eeb3-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 





