---
title: Come configurare le applicazioni Web di MBAM 2.5
description: Come configurare le applicazioni Web di MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824496"
---
# <span data-ttu-id="c0148-103">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0148-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="c0148-104">Questo argomento spiega come configurare le applicazioni Web di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 per l' [architettura di alto livello consigliata per MBAM 2,5](high-level-architecture-for-mbam-25.md) usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0148-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="c0148-105">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0148-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="c0148-106">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="c0148-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="c0148-107">Le applicazioni Web includono i siti Web seguenti e i relativi servizi Web:</span><span class="sxs-lookup"><span data-stu-id="c0148-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0148-108">Website</span><span class="sxs-lookup"><span data-stu-id="c0148-108">Website</span></span></th>
<th align="left"><span data-ttu-id="c0148-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0148-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0148-110">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="c0148-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0148-111">Sito Web in cui gli utenti specificati possono visualizzare i report e aiutare gli utenti finali a recuperare i propri computer quando dimenticano il PIN o la password</span><span class="sxs-lookup"><span data-stu-id="c0148-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0148-112">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="c0148-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0148-113">Sito Web a cui gli utenti finali possono accedere per ottenere l'accesso in modo indipendente ai propri computer se dimenticano il PIN o la password</span><span class="sxs-lookup"><span data-stu-id="c0148-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c0148-114">Prima di iniziare la configurazione:</span><span class="sxs-lookup"><span data-stu-id="c0148-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0148-115">Passaggio</span><span class="sxs-lookup"><span data-stu-id="c0148-115">Step</span></span></th>
<th align="left"><span data-ttu-id="c0148-116">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="c0148-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0148-117">Esaminare l'architettura consigliata per MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0148-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="c0148-118">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0148-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0148-119">Esaminare le configurazioni supportate per MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0148-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="c0148-120">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0148-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0148-121">Completare i prerequisiti necessari per ogni server.</span><span class="sxs-lookup"><span data-stu-id="c0148-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c0148-122">Nota</span><span class="sxs-lookup"><span data-stu-id="c0148-122">Note</span></span></strong><br/><p><span data-ttu-id="c0148-123">Verificare di aver configurato SQL ServerReporting Services (SSRS) in modo da usare il Secure Sockets Layer (SSL) prima di configurare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c0148-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="c0148-124">In caso contrario, la caratteristica report utilizzerà HTTP anziché HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c0148-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="c0148-125">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0148-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="c0148-126">Prerequisiti di MBAM 2,5 server che si applicano solo alla topologia di integrazione di Configuration Manager </a> (se applicabile)</span><span class="sxs-lookup"><span data-stu-id="c0148-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0148-127">Registrare nomi di entità servizio (SPN) per l'account del pool di applicazioni per i siti Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="c0148-128">È necessario eseguire questa procedura solo se non si hanno diritti di dominio amministrativi in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0148-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="c0148-129">Se si hanno questi diritti in servizi di dominio Active Directory, MBAM creerà i nomi SPN per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c0148-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="c0148-130">Pianificazione di come proteggere i siti Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="c0148-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0148-131">Installare il software MBAM server su ogni server in cui verrà configurata una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0148-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c0148-132">Nota</span><span class="sxs-lookup"><span data-stu-id="c0148-132">Note</span></span></strong><br/><p><span data-ttu-id="c0148-133">Se si prevede di installare i siti Web in un server e i servizi Web in un altro, sarà possibile configurarli solo usando il <strong> cmdlet Enable-MbamWebApplication di </strong> Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0148-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="c0148-134">La configurazione guidata di MBAM server non supporta la configurazione di questi elementi in server distinti.</span><span class="sxs-lookup"><span data-stu-id="c0148-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="c0148-135">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0148-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0148-136">Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet per configurare le caratteristiche del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0148-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="c0148-137">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0148-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c0148-138">Per configurare le applicazioni Web tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0148-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c0148-139">Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0148-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="c0148-140">Usare il cmdlet **Enable-MbamWebApplication** per configurare le applicazioni Web tramite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0148-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="c0148-141">Per ottenere informazioni su questo cmdlet, digitare **Get-Help Enable-MbamWebApplication**.</span><span class="sxs-lookup"><span data-stu-id="c0148-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="c0148-142">Per configurare le impostazioni per tutte le applicazioni Web tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="c0148-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="c0148-143">Nel server in cui si vogliono configurare le applicazioni Web, avviare la configurazione guidata del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0148-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="c0148-144">È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="c0148-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="c0148-145">Fare clic su **Aggiungi nuove funzionalità**, selezionare **amministrazione e monitoraggio del sito Web** e **portale self-service**, quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c0148-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="c0148-146">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="c0148-147">Se il controllo dei prerequisiti è riuscito, fare clic su **Avanti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="c0148-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="c0148-148">In caso contrario, risolvere i prerequisiti mancanti e quindi fare di **nuovo clic su Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="c0148-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="c0148-149">Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="c0148-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="c0148-150">Campo</span><span class="sxs-lookup"><span data-stu-id="c0148-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="c0148-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0148-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-152">Certificato di sicurezza</span><span class="sxs-lookup"><span data-stu-id="c0148-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-153">Selezionare un certificato creato in precedenza per crittografare facoltativamente la comunicazione tra i servizi Web e il server in cui si configurano i siti Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="c0148-154">Se si sceglie <strong> di non usare un certificato </strong> , la comunicazione web potrebbe non essere sicura.</span><span class="sxs-lookup"><span data-stu-id="c0148-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c0148-155">Nome dell'host</span><span class="sxs-lookup"><span data-stu-id="c0148-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-156">Nome del computer host in cui si configurano i siti Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-157">Percorso di installazione</span><span class="sxs-lookup"><span data-stu-id="c0148-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-158">Percorso in cui si installano i siti Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c0148-159">Port</span><span class="sxs-lookup"><span data-stu-id="c0148-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-160">Numero di porta da usare per la comunicazione tramite sito Web e servizi.</span><span class="sxs-lookup"><span data-stu-id="c0148-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="c0148-161">Nota</span><span class="sxs-lookup"><span data-stu-id="c0148-161">Note</span></span></strong><br/><p><span data-ttu-id="c0148-162">Per abilitare le comunicazioni tramite la porta specificata, è necessario impostare un'eccezione del firewall.</span><span class="sxs-lookup"><span data-stu-id="c0148-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-163">Account di dominio e password del pool di applicazioni Web Service</span><span class="sxs-lookup"><span data-stu-id="c0148-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-164">Account utente di dominio e password per il pool di applicazioni del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="c0148-165">Se si immette un nome utente nel <strong> campo utente o gruppo di dominio di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , è necessario immettere lo stesso valore in questo campo.</span><span class="sxs-lookup"><span data-stu-id="c0148-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="c0148-166">Se si immette un nome di gruppo nel <strong> campo utente o gruppo di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , il valore immesso in questo campo deve essere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="c0148-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="c0148-167">Se non specifichi le credenziali, verranno usate le credenziali specificate per qualsiasi applicazione Web abilitata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c0148-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="c0148-168">Tutte le applicazioni Web devono usare le stesse credenziali del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c0148-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="c0148-169">Se si specificano credenziali diverse per diverse applicazioni Web, verrà usato il valore specificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="c0148-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="c0148-170">Importante</span><span class="sxs-lookup"><span data-stu-id="c0148-170">Important</span></span></strong><br/><p><span data-ttu-id="c0148-171">Per una maggiore sicurezza, imposta l'account specificato nelle credenziali per avere diritti utente limitati.</span><span class="sxs-lookup"><span data-stu-id="c0148-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="c0148-172">Imposta inoltre la password dell'account su non scadono mai.</span><span class="sxs-lookup"><span data-stu-id="c0148-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="c0148-173">Verificare che l'account predefinito di IIS \ _IUSRS o l'account del pool di applicazioni sia stato aggiunto al **client** di rappresentanza dopo l'autenticazione e le impostazioni di sicurezza locali del **processo di accesso come batch** .</span><span class="sxs-lookup"><span data-stu-id="c0148-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="c0148-174">Per verificare se è stata aggiunta alle impostazioni di sicurezza locali, aprire l' **Editor criteri di sicurezza locali**, espandere il **nodo Criteri locali** , fare clic sul nodo **assegnazione diritti utente** e quindi fare doppio clic su **rappresenta un client dopo l'autenticazione** e **accedere come criteri processo batch** nel riquadro destro.</span><span class="sxs-lookup"><span data-stu-id="c0148-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="c0148-175">Per configurare le informazioni di connessione per i database tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="c0148-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="c0148-176">Usare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="c0148-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c0148-177">Campo</span><span class="sxs-lookup"><span data-stu-id="c0148-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="c0148-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0148-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c0148-179">Nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0148-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="c0148-180">Nome del server in cui è configurato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="c0148-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="c0148-181">Istanza di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0148-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="c0148-182">Nome dell'istanza di SQL Server in cui è configurato il database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="c0148-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c0148-183">Nome database</span><span class="sxs-lookup"><span data-stu-id="c0148-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="c0148-184">Nome del database di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="c0148-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="c0148-185">Usare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c0148-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c0148-186">Campo</span><span class="sxs-lookup"><span data-stu-id="c0148-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="c0148-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0148-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c0148-188">Nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0148-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="c0148-189">Nome del server in cui è configurato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c0148-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="c0148-190">Istanza di database di SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0148-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="c0148-191">Nome dell'istanza di SQL Server in cui è configurato il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c0148-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c0148-192">Nome database</span><span class="sxs-lookup"><span data-stu-id="c0148-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="c0148-193">Nome del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c0148-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="c0148-194">Per configurare le applicazioni Web tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="c0148-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="c0148-195">Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata per configurare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c0148-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c0148-196">Campo</span><span class="sxs-lookup"><span data-stu-id="c0148-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="c0148-197">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0148-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-198">Gruppo di domini del ruolo Advanced helpdesk</span><span class="sxs-lookup"><span data-stu-id="c0148-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-199">Gruppo di utenti del dominio i cui membri hanno accesso a tutte le aree del sito Web di amministrazione e monitoraggio eccetto l'area report.</span><span class="sxs-lookup"><span data-stu-id="c0148-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c0148-200">Gruppo di domini del ruolo helpdesk</span><span class="sxs-lookup"><span data-stu-id="c0148-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-201">Gruppo di utenti del dominio i cui membri hanno accesso alle <strong> </strong> aree di gestione TPM e <strong> recupero unità </strong> del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c0148-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-202">Usare l'integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0148-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-203">Selezionare questa casella di controllo se si sta configurando MBAM con la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0148-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="c0148-204">Selezionando questa casella di controllo tutti i report, eccetto il rapporto di controllo del ripristino, verranno visualizzati in Configuration Manager invece che nel sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c0148-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c0148-205">Gruppo di Domain Role Reporting</span><span class="sxs-lookup"><span data-stu-id="c0148-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-206">Gruppo di utenti del dominio i cui membri hanno accesso in sola lettura all'area report del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c0148-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-207">URL di SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="c0148-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-208">URL per il server SSRS in cui sono configurati i report MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0148-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="c0148-209">Esempi di URL del report:</span><span class="sxs-lookup"><span data-stu-id="c0148-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c0148-210">Tipo di nome host</span><span class="sxs-lookup"><span data-stu-id="c0148-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="c0148-211">Esempio</span><span class="sxs-lookup"><span data-stu-id="c0148-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c0148-212">Esempio con un nome di dominio completo</span><span class="sxs-lookup"><span data-stu-id="c0148-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="c0148-213">Esempio con un nome host personalizzato</span><span class="sxs-lookup"><span data-stu-id="c0148-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="c0148-214">Directory virtuale</span><span class="sxs-lookup"><span data-stu-id="c0148-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-215">Directory virtuale del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c0148-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="c0148-216">Questo nome corrisponde alla directory fisica del sito Web del server e viene accodato al nome host del sito Web, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c0148-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="c0148-217">http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> porta </em> &gt; /helpdesk/</span><span class="sxs-lookup"><span data-stu-id="c0148-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="c0148-218">Se non si specifica una directory virtuale, verrà usato l'helpdesk per il valore <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="c0148-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-219">Gruppo di dominio del ruolo di migrazione dei dati </strong> (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="c0148-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c0148-220">Gruppo di utenti di dominio i cui membri hanno accesso per usare i cmdlet di informazioni di scrittura-mbam \* per scrivere le informazioni di ripristino tramite questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="c0148-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="c0148-221">Usare la descrizione seguente per immettere i valori dei campi nella procedura guidata per configurare il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0148-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c0148-222">Campo</span><span class="sxs-lookup"><span data-stu-id="c0148-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="c0148-223">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0148-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="c0148-224">Directory virtuale</span><span class="sxs-lookup"><span data-stu-id="c0148-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="c0148-225">Directory virtuale dell'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-225">Virtual directory of the web application.</span></span> <span data-ttu-id="c0148-226">Questo nome corrisponde alla directory fisica del sito Web del server e viene accodato al nome host del sito Web, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c0148-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="c0148-227">http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> porta </em> &gt; /selfservice/</span><span class="sxs-lookup"><span data-stu-id="c0148-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="c0148-228">Se non specifichi una directory virtuale, verrà usato il valore <strong> selfservice </strong> .</span><span class="sxs-lookup"><span data-stu-id="c0148-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="c0148-229">Nome azienda</span><span class="sxs-lookup"><span data-stu-id="c0148-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c0148-230">Specificare il nome di una società per il portale self-service, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c0148-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="c0148-231">Contoso IT</span><span class="sxs-lookup"><span data-stu-id="c0148-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="c0148-232">Il nome della società viene visualizzato da tutti gli utenti del portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0148-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c0148-233">Testo dell'URL dell'helpdesk</span><span class="sxs-lookup"><span data-stu-id="c0148-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c0148-234">Specificare un'istruzione di testo che indirizzi gli utenti al sito Web dell'helpdesk dell'organizzazione, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c0148-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="c0148-235">Contattare l'helpdesk o il reparto IT</span><span class="sxs-lookup"><span data-stu-id="c0148-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="c0148-236">URL dell'helpdesk</span><span class="sxs-lookup"><span data-stu-id="c0148-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c0148-237">Specificare l'URL del sito Web dell'helpdesk dell'organizzazione, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c0148-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="c0148-238">http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="c0148-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="c0148-239">File di testo di avviso</span><span class="sxs-lookup"><span data-stu-id="c0148-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c0148-240">Selezionare un file contenente l'avviso che si vuole visualizzare agli utenti nella pagina di destinazione del portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0148-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="c0148-241">Non visualizzare il testo dell'avviso per gli utenti</span><span class="sxs-lookup"><span data-stu-id="c0148-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="c0148-242">Selezionare questa casella di controllo per specificare che il testo dell'avviso non viene visualizzato agli utenti.</span><span class="sxs-lookup"><span data-stu-id="c0148-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="c0148-243">Dopo aver completato le voci, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c0148-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="c0148-244">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="c0148-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="c0148-245">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="c0148-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="c0148-246">Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.</span><span class="sxs-lookup"><span data-stu-id="c0148-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="c0148-247">Nota</span><span class="sxs-lookup"><span data-stu-id="c0148-247">Note</span></span>**  
   <span data-ttu-id="c0148-248">Per creare uno script di Windows PowerShell per le voci effettuate, fare clic su **Esporta script di PowerShell** e salvare lo script.</span><span class="sxs-lookup"><span data-stu-id="c0148-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="c0148-249">Fare clic su **Aggiungi** per aggiungere le applicazioni Web al server e quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="c0148-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="c0148-250">Per personalizzare il portale self-service con l'aggiunta di testo di avviso personalizzato, il nome della società, i puntatori a altre informazioni e così via, vedere [personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="c0148-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="c0148-251">Per configurare il portale self-service se i computer client non riescono ad accedere alla rete CDN</span><span class="sxs-lookup"><span data-stu-id="c0148-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="c0148-252">Determinare se è in uso Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0148-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="c0148-253">In caso affermativo, non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="c0148-253">If so, do nothing.</span></span> <span data-ttu-id="c0148-254">La configurazione del portale self-service è completa.</span><span class="sxs-lookup"><span data-stu-id="c0148-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="c0148-255">Nota</span><span class="sxs-lookup"><span data-stu-id="c0148-255">Note</span></span>**  
    <span data-ttu-id="c0148-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 installa i file JavaScript in configurazione e non deve quindi essere connesso alla rete di distribuzione del contenuto Microsoft AJAX per configurare il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0148-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="c0148-257">I passaggi seguenti sono necessari solo se si usa una versione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 precedente a SP1.</span><span class="sxs-lookup"><span data-stu-id="c0148-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="c0148-258">Determinare se i computer client hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="c0148-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="c0148-259">La rete CDN offre al portale self-service l'accesso necessario a determinati file JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0148-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="c0148-260">Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, verranno visualizzati solo il nome della società e l'account in cui l'utente finale ha effettuato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="c0148-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="c0148-261">Nessun messaggio di errore verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c0148-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="c0148-262">Effettua una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="c0148-262">Do one of the following:</span></span>

    -   <span data-ttu-id="c0148-263">Se i computer client hanno accesso alla rete CDN, non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="c0148-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="c0148-264">La configurazione del portale self-service è completa.</span><span class="sxs-lookup"><span data-stu-id="c0148-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="c0148-265">Se i computer client non hanno accesso alla rete CDN, completare la procedura descritta in [come configurare il portale self-service quando i computer client non riescono ad accedere a Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="c0148-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="c0148-266">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0148-266">Related topics</span></span>


[<span data-ttu-id="c0148-267">Registri eventi del server</span><span class="sxs-lookup"><span data-stu-id="c0148-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="c0148-268">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0148-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="c0148-269">Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft</span><span class="sxs-lookup"><span data-stu-id="c0148-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="c0148-270">Personalizzazione del portale self-service per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="c0148-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="c0148-271">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c0148-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="c0148-272">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="c0148-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c0148-273">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c0148-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c0148-274">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c0148-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





