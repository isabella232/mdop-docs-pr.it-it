---
title: Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V
description: Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817935"
---
# <span data-ttu-id="1f505-103">Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V</span><span class="sxs-lookup"><span data-stu-id="1f505-103">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>


<span data-ttu-id="1f505-104">È possibile usare la procedura seguente per configurare l'ambiente Microsoft Application Virtualization (App-V) in modo da usare il mirroring del database di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f505-104">You can use the following procedure to configure your Microsoft Application Virtualization (App-V) environment to use Microsoft SQL Server database mirroring.</span></span> <span data-ttu-id="1f505-105">La configurazione del mirroring del database può essere utile per scenari di failover e ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="1f505-105">Configuring database mirroring can help with disaster recovery and failover scenarios.</span></span> <span data-ttu-id="1f505-106">App-V 4,5 SP2 supporta tutte le modalità di mirroring del database attualmente disponibili per Microsoft SQL Server 2005 e SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1f505-106">App-V 4.5 SP2 supports all modes of database mirroring currently available for Microsoft SQL Server 2005 and SQL Server 2008.</span></span>

**<span data-ttu-id="1f505-107">Nota</span><span class="sxs-lookup"><span data-stu-id="1f505-107">Note</span></span>**  
<span data-ttu-id="1f505-108">Questa procedura viene scritta per gli amministratori che hanno familiarità con l'impostazione e la configurazione dei database di SQL Server e del mirroring del database con Microsoft SQL Server e quindi copre solo le impostazioni di configurazione specifiche univoche per App-V.</span><span class="sxs-lookup"><span data-stu-id="1f505-108">This procedure is written for administrators who are familiar with setting up and configuring SQL Server databases and database mirroring with Microsoft SQL Server, and therefore covers only the specific configuration settings that are unique to App-V.</span></span>



**<span data-ttu-id="1f505-109">Per configurare l'ambiente App-V in modo da usare il mirroring del database di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="1f505-109">To configure your App-V environment to use Microsoft SQL Server database mirroring</span></span>**

1.  <span data-ttu-id="1f505-110">Configurare il mirroring del database di SQL Server del database App-V seguendo le normali procedure aziendali per il mirroring del database.</span><span class="sxs-lookup"><span data-stu-id="1f505-110">Set up SQL Server database mirroring of the App-V database following your standard business practices for database mirroring.</span></span> <span data-ttu-id="1f505-111">Usare i collegamenti seguenti per informazioni generali sull'implementazione del mirroring del database di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="1f505-111">Use the following links for general information about implementing Microsoft SQL Server database mirroring:</span></span>

    -   <span data-ttu-id="1f505-112">**Microsoft SQL 2005**—[configurazione del mirroring del database](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span><span class="sxs-lookup"><span data-stu-id="1f505-112">**Microsoft SQL 2005**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span></span>

    -   <span data-ttu-id="1f505-113">**Microsoft SQL 2008**—[configurazione del mirroring del database](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span><span class="sxs-lookup"><span data-stu-id="1f505-113">**Microsoft SQL 2008**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span></span>

    <span data-ttu-id="1f505-114">Inoltre, è possibile trovare informazioni sulle procedure consigliate nelle procedure consigliate per il [mirroring del database e le considerazioni sulle prestazioni](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .</span><span class="sxs-lookup"><span data-stu-id="1f505-114">In addition, you can find Best Practices information in [Database Mirroring Best Practices and Performance Considerations](https://go.microsoft.com/fwlink/?LinkId=190270) (https://go.microsoft.com/fwlink/?LinkId=190270).</span></span>

2.  <span data-ttu-id="1f505-115">Dopo aver configurato il mirroring, verificare che il database App-V indichi uno stato **(Principal, synchronized)** e che il database con mirroring visualizzi lo stato **(mirror, synchronized/Restoring)**.</span><span class="sxs-lookup"><span data-stu-id="1f505-115">After mirroring has been set up, verify that the App-V database shows a status of **(Principal, Synchronized)**, and the mirrored database shows a status of **(Mirror, Synchronized / Restoring)**.</span></span> <span data-ttu-id="1f505-116">Risolvere i problemi di mirroring prima di procedere con il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="1f505-116">Resolve any mirroring issues before proceeding to the next step.</span></span> <span data-ttu-id="1f505-117">Per altre informazioni sul monitoraggio dello stato, vedere [monitoraggio dello stato del mirroring](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .</span><span class="sxs-lookup"><span data-stu-id="1f505-117">For additional information about monitoring the status, see [Monitoring Mirroring Status](https://go.microsoft.com/fwlink/?LinkId=190279) (https://go.microsoft.com/fwlink/?LinkId=190279).</span></span>

3.  <span data-ttu-id="1f505-118">Nel computer SQL Server che ospita lo specchio del database di App-v creare l'account di accesso di SQL Server per il servizio di rete dell'app-v Management Server usando il nome del dominio di account \*\* &lt; &gt; \\ &lt; ManagementServerHostName &gt; $ \*\*.</span><span class="sxs-lookup"><span data-stu-id="1f505-118">On the SQL Server computer that hosts the mirror of the App-V database, create the SQL Server Login for the network service account of the App-V Management Server by using the account name **&lt;domain&gt;\\&lt;ManagementServerHostName&gt;$**.</span></span>

4.  <span data-ttu-id="1f505-119">Installare Microsoft SQL Server Native client in App-V Management Server e nel computer in cui è in uso l'App-V Management Web Service se installato in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="1f505-119">Install the Microsoft SQL Server Native Client on the App-V Management Server, and on the computer running the App-V Management Web Service if installed on a different computer.</span></span> <span data-ttu-id="1f505-120">Se si prevede di connettere altri server di gestione di App-V al database SQL con mirroring per il bilanciamento del carico, è necessario installare anche Microsoft SQL Server Native client in tali computer.</span><span class="sxs-lookup"><span data-stu-id="1f505-120">If you plan to have additional App-V Management Servers connect to the mirrored SQL database for load balancing, you must install the Microsoft SQL Server Native Client on those computers as well.</span></span> <span data-ttu-id="1f505-121">È possibile scaricare Microsoft SQL Server Native Client dalla pagina [Microsoft SQL server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) nell'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .</span><span class="sxs-lookup"><span data-stu-id="1f505-121">You can download the Microsoft SQL Server Native Client from the [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) page in the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=187479).</span></span>

5.  <span data-ttu-id="1f505-122">Selezionare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** e verificare che contenga solo il nome host di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f505-122">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerName** and make sure that it contains only the host name of the SQL Server.</span></span> <span data-ttu-id="1f505-123">Se include un nome di istanza, ad esempio *serverhostname\\instancename*, il nome dell'istanza deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="1f505-123">If it includes an instance name, for example *serverhostname\\instancename*, the instance name must be removed.</span></span>

    **<span data-ttu-id="1f505-124">Importante</span><span class="sxs-lookup"><span data-stu-id="1f505-124">Important</span></span>**  
    <span data-ttu-id="1f505-125">App-V Management Server usa la libreria di rete TCP/IP per comunicare con il server SQL quando è abilitato il mirroring del database e quindi non è possibile usare i nomi di istanza.</span><span class="sxs-lookup"><span data-stu-id="1f505-125">The App-V Management Server uses the TCP/IP networking library to communicate with the SQL Server when database mirroring is enabled, and therefore instance names cannot be used.</span></span> <span data-ttu-id="1f505-126">I numeri di porta devono essere specificati nelle chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1f505-126">The port numbers must be specified in the registry keys instead.</span></span>



6.  <span data-ttu-id="1f505-127">Selezionare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** e verificare che contenga il numero di porta usato per SQL nel computer SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f505-127">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerPort** and make sure that it contains the port number that is used for SQL on the SQL Server computer.</span></span> <span data-ttu-id="1f505-128">Se si usa un'istanza denominata, il valore della chiave deve essere impostato sulla porta utilizzata per l'istanza denominata.</span><span class="sxs-lookup"><span data-stu-id="1f505-128">If you are using a named instance this key value must be set to the port that is used for the named instance.</span></span>

7.  <span data-ttu-id="1f505-129">Creare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** come REG \ _SZ e quindi impostare il valore sul nome host di SQL Server che ospita il mirror.</span><span class="sxs-lookup"><span data-stu-id="1f505-129">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerName** as REG\_SZ and then set the value to the host name of the SQL Server that hosts the mirror.</span></span>

8.  <span data-ttu-id="1f505-130">Creare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** come DWORD e quindi impostare il valore sul numero di porta usato per SQL nel computer in cui è in uso SQL Server per ospitare il mirror.</span><span class="sxs-lookup"><span data-stu-id="1f505-130">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerPort** as DWORD and then set the value to the port number that is used for SQL on the computer that is running SQL Server to host the mirror.</span></span> <span data-ttu-id="1f505-131">Se si usa un'istanza denominata per il mirror, il valore della chiave deve essere impostato sul numero di porta usato per l'istanza denominata.</span><span class="sxs-lookup"><span data-stu-id="1f505-131">If you are using a named instance for the mirror this key value must be set to the port number that is used for the named instance.</span></span>

9.  <span data-ttu-id="1f505-132">Nel computer che sta usando il servizio Web di gestione App-V configurare il file di testo UDL (Universal Data Link).</span><span class="sxs-lookup"><span data-stu-id="1f505-132">On the computer that is running the App-V Management Web Service, configure the Universal Data Link (UDL) text file.</span></span> <span data-ttu-id="1f505-133">Nella directory in cui è installato App-V fare doppio clic su **SftMgmt. UDL** e specificare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f505-133">In the directory where App-V is installed, double-click **SftMgmt.udl** and specify the following values:</span></span>

    -   <span data-ttu-id="1f505-134">Nella scheda **provider** selezionare il provider OLE DB **SQL Server Native Client 10,0**.</span><span class="sxs-lookup"><span data-stu-id="1f505-134">On the **Provider** tab, select the OLE DB provider **SQL Server Native Client 10.0**.</span></span>

    -   <span data-ttu-id="1f505-135">Fare clic su **Avanti** per selezionare la scheda **connessione** . Nella casella **nome server** immettere il nome del server di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f505-135">Click **Next** to select the **Connection** tab. In the **Server Name** box, enter the server name of the SQL Server.</span></span> <span data-ttu-id="1f505-136">Selezionare quindi **Usa sicurezza integrata di Windows NT**.</span><span class="sxs-lookup"><span data-stu-id="1f505-136">Next, select **Use Windows NT Integrated Security**.</span></span> <span data-ttu-id="1f505-137">Infine, fare clic sull'elenco **selezionare il database**e quindi selezionare il nome del database App-V.</span><span class="sxs-lookup"><span data-stu-id="1f505-137">Finally, click the list **Select the database**, and then select the App-V database name.</span></span>

    -   <span data-ttu-id="1f505-138">Fare clic sulla scheda **tutte** e quindi selezionare il partner per il **failover**delle voci.</span><span class="sxs-lookup"><span data-stu-id="1f505-138">Click the **All** tab, and then select the entry **Failover Partner**.</span></span> <span data-ttu-id="1f505-139">Fare clic su **Modifica valore**e quindi immettere il nome del server di SQL Server di failover.</span><span class="sxs-lookup"><span data-stu-id="1f505-139">Click **Edit Value**, and then enter the server name of the failover SQL Server.</span></span> <span data-ttu-id="1f505-140">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f505-140">Click **OK**.</span></span>

    **<span data-ttu-id="1f505-141">Importante</span><span class="sxs-lookup"><span data-stu-id="1f505-141">Important</span></span>**  
    <span data-ttu-id="1f505-142">Il sistema App-V usa l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1f505-142">The App-V system uses Kerberos authentication.</span></span> <span data-ttu-id="1f505-143">Di conseguenza, quando si configura il mirroring SQL in cui l'autenticazione Kerberos è abilitata in SQL Server e il servizio SQL Server viene eseguito in un account utente di dominio, è necessario configurare manualmente un nome SPN.</span><span class="sxs-lookup"><span data-stu-id="1f505-143">Therefore, when you configure SQL mirroring where Kerberos Authentication is enabled on the SQL Server and the SQL Server service runs under a domain user account, you must manually configure an SPN.</span></span> <span data-ttu-id="1f505-144">Per altre informazioni, vedere "quando il servizio SQL usa un account basato su dominio" nell'articolo [configurazione dell'amministrazione di App-V per un ambiente distribuito](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .</span><span class="sxs-lookup"><span data-stu-id="1f505-144">For more information, see “When SQL Service Uses Domain-Based Account” in the article [Configuring App-V Administration for a Distributed Environment](https://go.microsoft.com/fwlink/?LinkId=203186) (https://go.microsoft.com/fwlink/?LinkId=203186).</span></span>



10. <span data-ttu-id="1f505-145">Per verificare che il mirroring del database sia in corso correttamente, verificare il failover e verificare che l'App-V Management Server continui a funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="1f505-145">To verify that database mirroring is running correctly, test the failover and confirm that the App-V Management Server continues to function correctly.</span></span>

    **<span data-ttu-id="1f505-146">Importante</span><span class="sxs-lookup"><span data-stu-id="1f505-146">Important</span></span>**  
    <span data-ttu-id="1f505-147">Procedere con attenzione e seguire le procedure aziendali standard per verificare che le operazioni di sistema non vengano interrotte in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="1f505-147">Proceed with care, and follow your standard business practices to ensure that system operations are not disrupted in the event of a failure.</span></span>



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## <span data-ttu-id="1f505-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f505-148">Related topics</span></span>


[<span data-ttu-id="1f505-149">Come eseguire attività amministrative in Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="1f505-149">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









