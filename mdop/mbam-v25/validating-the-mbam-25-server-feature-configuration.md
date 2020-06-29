---
title: Convalida della configurazione delle funzionalità del server di MBAM 2.5
description: Convalida della configurazione delle funzionalità del server di MBAM 2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827085"
---
# <span data-ttu-id="5f0ff-103">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5f0ff-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="5f0ff-104">Al termine della distribuzione della funzionalità del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5, è consigliabile convalidare la distribuzione per verificare che tutte le funzionalità siano state configurate correttamente.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="5f0ff-105">Usare la procedura che corrisponde alla topologia (autonoma o integrazione di System Center Configuration Manager) distribuita.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="5f0ff-106">Convalida della distribuzione di MBAM server con la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="5f0ff-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="5f0ff-107">Eseguire la procedura seguente per convalidare la distribuzione di MBAM server con la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="5f0ff-108">Per convalidare una distribuzione autonoma di MBAM server</span><span class="sxs-lookup"><span data-stu-id="5f0ff-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="5f0ff-109">In ogni server in cui è distribuita una caratteristica di **Control Panel** mbam, fare clic su &gt; **Programs** &gt; **programmi e funzionalità**del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="5f0ff-110">Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="5f0ff-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="5f0ff-111">Nota</span><span class="sxs-lookup"><span data-stu-id="5f0ff-111">Note</span></span>**  
    <span data-ttu-id="5f0ff-112">Per eseguire la convalida, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="5f0ff-113">Nel server in cui è configurato il database di ripristino, aprire SQL Server Management Studio e verificare che il database **di mbam Recovery e hardware** sia configurato.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="5f0ff-114">Nel server in cui è configurato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che il **database dello stato di conformità di mbam** sia configurato.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="5f0ff-115">Nel server in cui è configurata la caratteristica report aprire un Web browser con credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="5f0ff-116">La posizione principale predefinita di un'istanza del sito di SQL Server Reporting Services è:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="5f0ff-117">http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /Reports.aspx</span><span class="sxs-lookup"><span data-stu-id="5f0ff-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="5f0ff-118">Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="5f0ff-119">Verificare che una cartella report denominata **amministrazione e monitoraggio di Microsoft BitLocker** contenga un'origine dati denominata **MaltaDataSource** e le cartelle della lingua.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="5f0ff-120">L'origine dati contiene cartelle con nomi che rappresentano le lingue, ad esempio en-US.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="5f0ff-121">I report si trovano nelle cartelle della lingua.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="5f0ff-122">Nota</span><span class="sxs-lookup"><span data-stu-id="5f0ff-122">Note</span></span>**  
    <span data-ttu-id="5f0ff-123">Se SQL Server Reporting Services (SSRS) è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="5f0ff-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="5f0ff-124">Nel server in cui è configurata la caratteristica sito Web amministrazione e monitoraggio eseguire **Server Manager**, passare a **ruoli**e quindi selezionare **Web Server (IIS)** &gt; **Gestione Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="5f0ff-125">In **connessioni**passare al \* &lt; nome &gt; del computer\* e selezionare **siti** di &gt; **amministrazione e monitoraggio di Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="5f0ff-126">Verificare che siano elencati i seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="5f0ff-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="5f0ff-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="5f0ff-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="5f0ff-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="5f0ff-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="5f0ff-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="5f0ff-130">Nel server in cui sono configurati il sito Web di amministrazione e monitoraggio e il portale self-service, aprire un Web browser con credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="5f0ff-131">Individuare i siti Web seguenti per verificare che vengano caricati correttamente:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="5f0ff-132">HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /helpdesk/-confermare tutti i collegamenti per gli spostamenti e i report</span><span class="sxs-lookup"><span data-stu-id="5f0ff-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="5f0ff-133">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /selfservice/</span><span class="sxs-lookup"><span data-stu-id="5f0ff-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="5f0ff-134">Nota</span><span class="sxs-lookup"><span data-stu-id="5f0ff-134">Note</span></span>**  
   <span data-ttu-id="5f0ff-135">Si presuppone che siano state configurate le caratteristiche del server nella porta predefinita senza crittografia di rete.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="5f0ff-136">Se sono state configurate le caratteristiche del server in una porta o una directory virtuale diversa, modificare gli URL per includere la porta appropriata, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="5f0ff-137">http (s):// &lt; *nome host* &gt; : &lt; *porta* &gt; /helpdesk/</span><span class="sxs-lookup"><span data-stu-id="5f0ff-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="5f0ff-138">http (s):// &lt; *nome host* &gt; : &lt; *porta* &gt; / &lt; *VirtualDirectory*&gt;/</span><span class="sxs-lookup"><span data-stu-id="5f0ff-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="5f0ff-139">Se le caratteristiche del server sono state configurate con crittografia di rete, cambiare http://in https://.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="5f0ff-140">Individuare i servizi Web seguenti per verificare che vengano caricati correttamente.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="5f0ff-141">Verrà visualizzata una pagina per indicare che il servizio è in corso, ma la pagina non Visualizza i metadati.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="5f0ff-142">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="5f0ff-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="5f0ff-143">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="5f0ff-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="5f0ff-144">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="5f0ff-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="5f0ff-145">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="5f0ff-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="5f0ff-146">Convalida della distribuzione di MBAM server con la topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5f0ff-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="5f0ff-147">Usare la procedura seguente per convalidare la distribuzione di MBAM con la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="5f0ff-148">Completare i passaggi di convalida che corrispondono alla versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="5f0ff-149">Convalida della distribuzione di MBAM server con System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5f0ff-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="5f0ff-150">Seguire questa procedura per convalidare la distribuzione di MBAM server quando si usa MBAM con System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="5f0ff-151">Per convalidare una distribuzione di Configuration Manager Integration MBAM Server-System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5f0ff-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="5f0ff-152">Nel server in cui è distribuito System Center 2012 Configuration Manager, aprire **programmi e funzionalità** nel **Pannello di controllo**e verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="5f0ff-153">Nota</span><span class="sxs-lookup"><span data-stu-id="5f0ff-153">Note</span></span>**  
    <span data-ttu-id="5f0ff-154">Per convalidare la configurazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="5f0ff-155">Nella console di Configuration Manager fare clic su **assets and Compliance** &gt; **Device**Workspace e verificare che venga visualizzata una nuova raccolta denominata **computer supportati mbam** .</span><span class="sxs-lookup"><span data-stu-id="5f0ff-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="5f0ff-156">Nella console di Configuration Manager fare clic su **Monitoring** &gt; **Reporting** &gt; **Reports** &gt; **mbam**report Reporting Workspace.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="5f0ff-157">Verificare che la cartella **mbam** contenga sottocartelle, con nomi che rappresentano lingue diverse e che i report seguenti siano elencati in ogni sottocartella della lingua:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="5f0ff-158">Conformità al computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="5f0ff-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="5f0ff-159">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f0ff-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="5f0ff-160">Dettagli di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f0ff-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="5f0ff-161">Riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f0ff-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="5f0ff-162">Nella console di Configuration Manager fare clic sulle previsioni di configurazione delle impostazioni di conformità per l'area **risorse e conformità** &gt; **Compliance Settings** &gt; **Configuration Baselines**e verificare che sia elencata la **protezione BitLocker** della previsione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="5f0ff-163">Nella console di Configuration Manager fare clic sugli elementi di configurazione **assets and Compliance** Workspace &gt; **Compliance Settings** &gt; **Configuration Items**e verificare che siano visualizzati i nuovi elementi di configurazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="5f0ff-164">Protezione delle unità dati fisse di BitLocker</span><span class="sxs-lookup"><span data-stu-id="5f0ff-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="5f0ff-165">Protezione unità sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="5f0ff-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="5f0ff-166">Convalida della distribuzione di MBAM server con Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="5f0ff-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="5f0ff-167">Seguire questa procedura per convalidare la distribuzione di MBAM server quando si usa MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="5f0ff-168">Per convalidare una distribuzione di Configuration Manager Integration MBAM Server-Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="5f0ff-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="5f0ff-169">Nel server in cui è distribuito Configuration Manager 2007 aprire **programmi e funzionalità** nel **Pannello di controllo** e verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="5f0ff-170">Nota</span><span class="sxs-lookup"><span data-stu-id="5f0ff-170">Note</span></span>**  
    <span data-ttu-id="5f0ff-171">Per convalidare la configurazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="5f0ff-172">Nella console di Configuration Manager fare clic su **database del sito &lt; codicesito &gt;  -  &lt; NomeServer &gt; , &lt; nomesito &gt; ), Gestione computer**e verificare che venga visualizzata una nuova raccolta denominata **computer supportati mbam** .</span><span class="sxs-lookup"><span data-stu-id="5f0ff-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="5f0ff-173">Nella console di Configuration Manager fare clic su **Reporting** &gt; **Services** &gt; \*\* \\\\ &lt; NomeServer &gt; \*\* &gt; **cartelle di report** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="5f0ff-174">Verificare che la cartella **mbam** contenga sottocartelle, con nomi che rappresentano lingue diverse e che i report seguenti siano elencati in ogni sottocartella della lingua:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="5f0ff-175">Conformità al computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="5f0ff-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="5f0ff-176">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f0ff-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="5f0ff-177">Dettagli di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f0ff-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="5f0ff-178">Riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f0ff-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="5f0ff-179">Nella console di Configuration Manager fare clic su previsioni di configurazione per la **gestione della configurazione desiderata** &gt; **Configuration Baselines**e verificare che sia elencata la **protezione BitLocker** della configurazione di base.</span><span class="sxs-lookup"><span data-stu-id="5f0ff-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="5f0ff-180">Nella console di Configuration Manager fare clic su elementi di configurazione della **gestione della configurazione desiderati** &gt; **Configuration Items**e verificare che siano visualizzati i nuovi elementi di configurazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f0ff-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="5f0ff-181">Protezione delle unità dati fisse di BitLocker</span><span class="sxs-lookup"><span data-stu-id="5f0ff-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="5f0ff-182">Protezione unità sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="5f0ff-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="5f0ff-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f0ff-183">Related topics</span></span>


[<span data-ttu-id="5f0ff-184">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5f0ff-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="5f0ff-185">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="5f0ff-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5f0ff-186">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="5f0ff-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5f0ff-187">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5f0ff-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






