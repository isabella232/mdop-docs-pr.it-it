---
title: Uso di Client Management Console di App-V 5.1
description: Uso di Client Management Console di App-V 5.1
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804840"
---
# <span data-ttu-id="807af-103">Uso di Client Management Console di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="807af-103">Using the App-V 5.1 Client Management Console</span></span>


<span data-ttu-id="807af-104">Questo argomento fornisce informazioni su come configurare e gestire il client di Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="807af-104">This topic provides information about how you can configure and manage the Microsoft Application Virtualization (App-V) 5.1 client.</span></span>

## <span data-ttu-id="807af-105">Modificare la configurazione client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="807af-105">Modify App-V 5.1 client configuration</span></span>


<span data-ttu-id="807af-106">Il client App-V 5,1 ha impostazioni associate che possono essere configurate per determinare il modo in cui il client verrà eseguito nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="807af-106">The App-V 5.1 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="807af-107">È possibile gestire queste impostazioni nel computer che esegue il client o tramite PowerShell o criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="807af-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="807af-108">Per altre informazioni su come modificare il client usando PowerShell o configurazione di criteri di gruppo, vedere [come modificare la configurazione del client tramite PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="807af-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).</span></span>

## <a href="" id="the-app-v-5-1-client-management-console-"></a><span data-ttu-id="807af-109">Console di gestione client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="807af-109">The App-V 5.1 client management console</span></span>


<span data-ttu-id="807af-110">Puoi ottenere informazioni sul client App-V 5,1 o eseguire attività specifiche usando la console di gestione client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="807af-110">You can obtain information about the App-V 5.1 client or perform specific tasks by using the App-V 5.1 client management console.</span></span> <span data-ttu-id="807af-111">Molte delle attività che è possibile eseguire nella console di gestione client possono essere eseguite anche tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="807af-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="807af-112">I cmdlet di PowerShell associati per ogni azione vengono visualizzati anche nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="807af-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="807af-113">Per altre informazioni sull'uso di PowerShell, vedere [amministrazione di App-V 5,1 tramite PowerShell](administering-app-v-51-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="807af-113">For more information about how to use PowerShell, see [Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md).</span></span>

<span data-ttu-id="807af-114">La console di gestione client contiene le schede principali descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="807af-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="807af-115">TAB</span><span class="sxs-lookup"><span data-stu-id="807af-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="807af-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="807af-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="807af-117">Panoramica</span><span class="sxs-lookup"><span data-stu-id="807af-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="807af-118">La <strong> </strong> scheda Panoramica contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="807af-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="807af-119">Update: usare il <strong> </strong> riquadro Aggiorna per aggiornare un'applicazione virtualizzata o per ricevere un nuovo pacchetto virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="807af-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="807af-120">L' <strong> Ultimo aggiornamento </strong> Visualizza la versione corrente del pacchetto virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="807af-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="807af-121">Scaricare tutte le applicazioni virtuali: usare <strong> il </strong> riquadro download per scaricare tutti i pacchetti di cui è stato eseguito il provisioning per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="807af-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="807af-122">(Cmdlet di PowerShell associato: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="807af-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="807af-123">Lavorare offline: usare questo riquadro per disabilitare tutti gli aggiornamenti automatici e manuali delle applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="807af-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="807af-124">(Cmdlet di PowerShell associato: <strong> Set-AppvPublishServer-UserRefreshEnabled-GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="807af-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="807af-125">App virtuali</span><span class="sxs-lookup"><span data-stu-id="807af-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="807af-126">La <strong> scheda App virtuali </strong> Visualizza tutti i pacchetti che sono stati pubblicati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="807af-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="807af-127">È anche possibile fare clic su un pacchetto specifico e vedere tutte le applicazioni che fanno parte del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="807af-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="807af-128">In questo modo vengono visualizzate informazioni sui pacchetti attualmente in uso e sulla quantità di ogni pacchetto scaricato nel computer.</span><span class="sxs-lookup"><span data-stu-id="807af-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="807af-129">È anche possibile avviare e arrestare i download del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="807af-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="807af-130">È inoltre possibile ripristinare lo stato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="807af-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="807af-131">Un ripristino eliminerà tutti i dati utente associati a un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="807af-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="807af-132">Gruppi di connessioni app</span><span class="sxs-lookup"><span data-stu-id="807af-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="807af-133">Nella <strong> scheda gruppi di connessioni app </strong> vengono visualizzati tutti i gruppi di connessioni disponibili per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="807af-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="807af-134">Fare clic su un gruppo di connessioni specifico per visualizzare tutti i pacchetti che fanno parte del gruppo selezionato.</span><span class="sxs-lookup"><span data-stu-id="807af-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="807af-135">Vengono visualizzate informazioni sui gruppi di connessioni già in uso e sulla quantità di contenuto del gruppo di connessioni scaricate nel computer.</span><span class="sxs-lookup"><span data-stu-id="807af-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="807af-136">È inoltre possibile avviare e arrestare i download del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="807af-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="807af-137">Puoi usare questa sezione per avviare un ripristino.</span><span class="sxs-lookup"><span data-stu-id="807af-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="807af-138">Un ripristino rimuoverà tutto lo stato dell'utente associato a un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="807af-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="807af-139">(Cmdlet di PowerShell associati: download- <strong> Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="807af-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="807af-140">Repair- <strong> AppvClientConnectionGroup </strong> .)</span><span class="sxs-lookup"><span data-stu-id="807af-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="807af-141">Come accedere a Client Management Console</span><span class="sxs-lookup"><span data-stu-id="807af-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console51.md)

[<span data-ttu-id="807af-142">Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="807af-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## <span data-ttu-id="807af-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="807af-143">Related topics</span></span>


[<span data-ttu-id="807af-144">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="807af-144">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





