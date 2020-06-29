---
title: Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager
description: Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804233"
---
# <span data-ttu-id="792a7-103">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="792a7-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="792a7-104">Questo argomento spiega come configurare l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) per usare la topologia di integrazione di System Center Configuration Manager, che si integra con MBAM con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="792a7-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="792a7-105">Le istruzioni spiegano come configurare l'integrazione di Configuration Manager usando:</span><span class="sxs-lookup"><span data-stu-id="792a7-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="792a7-106">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="792a7-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="792a7-107">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="792a7-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="792a7-108">Le istruzioni si basano sull'architettura consigliata nell' [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="792a7-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="792a7-109">Prima di iniziare la configurazione:</span><span class="sxs-lookup"><span data-stu-id="792a7-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="792a7-110">Passaggio</span><span class="sxs-lookup"><span data-stu-id="792a7-110">Step</span></span></th>
<th align="left"><span data-ttu-id="792a7-111">Dove ottenere le istruzioni</span><span class="sxs-lookup"><span data-stu-id="792a7-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="792a7-112">Esaminare l'architettura consigliata per MBAM.</span><span class="sxs-lookup"><span data-stu-id="792a7-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="792a7-113">Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="792a7-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="792a7-114">Esaminare le configurazioni supportate per MBAM.</span><span class="sxs-lookup"><span data-stu-id="792a7-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="792a7-115">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="792a7-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="792a7-116">Completare i prerequisiti necessari per ogni server.</span><span class="sxs-lookup"><span data-stu-id="792a7-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="792a7-117">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="792a7-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="792a7-118">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="792a7-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="792a7-119">Installare il software MBAM server su ogni server in cui verrà configurata una caratteristica del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="792a7-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="792a7-120">Nota</span><span class="sxs-lookup"><span data-stu-id="792a7-120">Note</span></span></strong><br/><p><span data-ttu-id="792a7-121">Per questa topologia, è necessario installare la console di Configuration Manager nel computer in cui si sta installando il software del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="792a7-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="792a7-122">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="792a7-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="792a7-123">Rivedere i prerequisiti di Windows PowerShell (applicabile solo se si intende usare i cmdlet di Windows PowerShell per configurare MBAM).</span><span class="sxs-lookup"><span data-stu-id="792a7-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="792a7-124">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="792a7-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="792a7-125">Per configurare l'integrazione di Configuration Manager con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="792a7-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="792a7-126">Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="792a7-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="792a7-127">Usare il cmdlet **Enable-MbamCMIntegration** di Windows PowerShell per configurare i report.</span><span class="sxs-lookup"><span data-stu-id="792a7-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="792a7-128">Per ottenere informazioni su questo cmdlet, digitare **Get-Help Enable-MbamCMIntegration**.</span><span class="sxs-lookup"><span data-stu-id="792a7-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="792a7-129">Per configurare l'integrazione di System Center Configuration Manager tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="792a7-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="792a7-130">Nel server in cui si vuole configurare la funzionalità di integrazione di System Center Configuration Manager, avviare la configurazione guidata di MBAM server.</span><span class="sxs-lookup"><span data-stu-id="792a7-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="792a7-131">È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="792a7-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="792a7-132">Fare clic su **Aggiungi nuove funzionalità**, selezionare **integrazione di System Center Configuration Manager**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="792a7-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="792a7-133">La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per l'integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="792a7-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="792a7-134">Se il controllo dei prerequisiti è riuscito, fare clic su **Avanti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="792a7-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="792a7-135">In caso contrario, risolvere i prerequisiti mancanti e quindi fare di **nuovo clic su Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="792a7-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="792a7-136">Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata:</span><span class="sxs-lookup"><span data-stu-id="792a7-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="792a7-137">Campo</span><span class="sxs-lookup"><span data-stu-id="792a7-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="792a7-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="792a7-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="792a7-139">Server di SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="792a7-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="792a7-140">Nome di dominio completo (FQDN) del server con il ruolo del punto di servizio Reporting.</span><span class="sxs-lookup"><span data-stu-id="792a7-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="792a7-141">Questo è il server a cui sono distribuiti i report di MBAM Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="792a7-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="792a7-142">Se non specifichi un server, i report di Configuration Manager verranno distribuiti nel server locale.</span><span class="sxs-lookup"><span data-stu-id="792a7-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="792a7-143">Istanza di SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="792a7-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="792a7-144">Nome dell'istanza di SQL Server Reporting Services (SSRS) in cui vengono distribuiti i report di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="792a7-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="792a7-145">Se non specifichi un'istanza, i report di Configuration Manager verranno distribuiti nel nome dell'istanza di SSRS predefinita.</span><span class="sxs-lookup"><span data-stu-id="792a7-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="792a7-146">Il valore immesso viene ignorato se nel server è installato System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="792a7-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="792a7-147">Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.</span><span class="sxs-lookup"><span data-stu-id="792a7-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="792a7-148">Nota</span><span class="sxs-lookup"><span data-stu-id="792a7-148">Note</span></span>**  
    <span data-ttu-id="792a7-149">Per creare uno script di Windows PowerShell delle voci appena apportate, fare clic su **Esporta script di PowerShell** e salvare lo script.</span><span class="sxs-lookup"><span data-stu-id="792a7-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="792a7-150">Fare clic su **Aggiungi** per aggiungere la funzionalità di integrazione di Configuration Manager al server e quindi fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="792a7-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="792a7-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="792a7-151">Related topics</span></span>


[<span data-ttu-id="792a7-152">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="792a7-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="792a7-153">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="792a7-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="792a7-154">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="792a7-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="792a7-155">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="792a7-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="792a7-156">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="792a7-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






