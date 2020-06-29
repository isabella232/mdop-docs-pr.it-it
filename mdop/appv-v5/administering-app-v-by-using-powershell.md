---
title: Amministrazione di App-V con PowerShell
description: Amministrazione di App-V con PowerShell
author: dansimp
ms.assetid: 1ff4686a-1e19-4eff-b648-ada091281094
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e7f9171e0ac5589d8f1935e715dfdb9c349192d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806045"
---
# <span data-ttu-id="33780-103">Amministrazione di App-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-103">Administering App-V by Using PowerShell</span></span>


<span data-ttu-id="33780-104">Microsoft Application Virtualization (App-V) 5,0 offre i cmdlet di Windows PowerShell, che consentono agli amministratori di eseguire varie attività di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="33780-104">Microsoft Application Virtualization (App-V) 5.0 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.0 tasks.</span></span> <span data-ttu-id="33780-105">Nelle sezioni seguenti sono disponibili altre informazioni sull'uso di PowerShell con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="33780-105">The following sections provide more information about using PowerShell with App-V 5.0.</span></span>

## <span data-ttu-id="33780-106">Come amministrare App-V 5,0 tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-106">How to administer App-V 5.0 by using PowerShell</span></span>


<span data-ttu-id="33780-107">Usare le procedure di PowerShell seguenti per eseguire varie attività di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="33780-107">Use the following PowerShell procedures to perform various App-V 5.0 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33780-108">Nome</span><span class="sxs-lookup"><span data-stu-id="33780-108">Name</span></span></th>
<th align="left"><span data-ttu-id="33780-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33780-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md)"><span data-ttu-id="33780-110">Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet</span><span class="sxs-lookup"><span data-stu-id="33780-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-111">Descrive come installare i cmdlet di PowerShell e trovare la guida e gli esempi di cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33780-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="33780-112">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-112">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-113">Descrive come gestire il ciclo di vita del pacchetto client in un computer autonomo con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="33780-114">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-115">Descrive come gestire i gruppi di connessioni tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md)"><span data-ttu-id="33780-116">Come modificare la configurazione client con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-117">Descrive come modificare il client usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)"><span data-ttu-id="33780-118">Come applicare il file di configurazione utente con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-119">Descrive come applicare un file di configurazione utente usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)"><span data-ttu-id="33780-120">Come applicare il file di configurazione della distribuzione con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-121">Descrive come applicare un file di configurazione della distribuzione usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-50.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-50.md)"><span data-ttu-id="33780-122">Come sequenziare un pacchetto usando PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-123">Descrive come creare un nuovo pacchetto usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md)"><span data-ttu-id="33780-124">Come creare un acceleratore pacchetto con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-125">Descrive come creare un Acceleratore pacchetto usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33780-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="33780-126">Puoi usare gli acceleratori pacchetto per sequenziare automaticamente applicazioni di grandi dimensioni e complesse.</span><span class="sxs-lookup"><span data-stu-id="33780-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)"><span data-ttu-id="33780-127">Come abilitare la creazione di report nel client App-V 5.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-127">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-128">Descrive come abilitare il computer che gestisce l'App-V 5,0 per l'invio di informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="33780-128">Describes how to enable the computer running the App-V 5.0 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md)"><span data-ttu-id="33780-129">Come installare i database di App-V e convertire gli identificatori di sicurezza associati tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="33780-130">Descrive come usare una matrice di nomi di account e per convertirli nel SID corrispondente in formati standard ed esadecimali.</span><span class="sxs-lookup"><span data-stu-id="33780-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="33780-131">Gestione degli errori di PowerShell</span><span class="sxs-lookup"><span data-stu-id="33780-131">PowerShell Error Handling</span></span>


<span data-ttu-id="33780-132">Usare la tabella seguente per informazioni sulla gestione degli errori di PowerShell in App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="33780-132">Use the following table for information about App-V 5.0 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="33780-133">Evento</span><span class="sxs-lookup"><span data-stu-id="33780-133">Event</span></span></th>
<th align="left"><span data-ttu-id="33780-134">Azione</span><span class="sxs-lookup"><span data-stu-id="33780-134">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="33780-135">Uso dell'attributo RollbackOnError con gli script incorporati</span><span class="sxs-lookup"><span data-stu-id="33780-135">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="33780-136">Quando usi l' <strong> attributo RollbackOnError </strong> con gli script incorporati, l'attributo viene ignorato per gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="33780-136">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="33780-137">Rimozione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="33780-137">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="33780-138">Annullamento della pubblicazione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="33780-138">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="33780-139">Chiusura di un ambiente virtuale</span><span class="sxs-lookup"><span data-stu-id="33780-139">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="33780-140">Chiusura di un processo</span><span class="sxs-lookup"><span data-stu-id="33780-140">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="33780-141">Il nome del pacchetto contiene<strong>$</span><span class="sxs-lookup"><span data-stu-id="33780-141">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="33780-142">Se il nome di un pacchetto contiene il carattere ( <strong> $ </strong> ), è necessario usare una virgoletta singola ( <strong> ' </strong> ), ad esempio</span><span class="sxs-lookup"><span data-stu-id="33780-142">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="33780-143">Add-AppvClientPackage ' Contoso $ App. AppV '</span><span class="sxs-lookup"><span data-stu-id="33780-143">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="33780-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33780-144">Related topics</span></span>


[<span data-ttu-id="33780-145">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="33780-145">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





