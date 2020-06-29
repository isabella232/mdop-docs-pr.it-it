---
title: Amministrazione di App-V 5.1 con PowerShell
description: Amministrazione di App-V 5.1 con PowerShell
author: dansimp
ms.assetid: 9e10ff07-2cd9-4dc1-9e99-582f90c36081
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0c64d7e0330ff5d737dfa02d87f156cc3236b04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806052"
---
# <span data-ttu-id="d6995-103">Amministrazione di App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-103">Administering App-V 5.1 by Using PowerShell</span></span>


<span data-ttu-id="d6995-104">Microsoft Application Virtualization (App-V) 5,1 offre i cmdlet di Windows PowerShell, che consentono agli amministratori di eseguire varie attività di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d6995-104">Microsoft Application Virtualization (App-V) 5.1 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.1 tasks.</span></span> <span data-ttu-id="d6995-105">Nelle sezioni seguenti sono disponibili altre informazioni sull'uso di PowerShell con App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d6995-105">The following sections provide more information about using PowerShell with App-V 5.1.</span></span>

## <span data-ttu-id="d6995-106">Come amministrare App-V 5,1 tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-106">How to administer App-V 5.1 by using PowerShell</span></span>


<span data-ttu-id="d6995-107">Usare le procedure di PowerShell seguenti per eseguire varie attività di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d6995-107">Use the following PowerShell procedures to perform various App-V 5.1 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6995-108">Nome</span><span class="sxs-lookup"><span data-stu-id="d6995-108">Name</span></span></th>
<th align="left"><span data-ttu-id="d6995-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6995-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)"><span data-ttu-id="d6995-110">Come caricare i cmdlet di PowerShell e ottenere informazioni sui cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6995-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-111">Descrive come installare i cmdlet di PowerShell e trovare la guida e gli esempi di cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6995-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="d6995-112">Come gestire i pacchetti App-V 5.1 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-112">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-113">Descrive come gestire il ciclo di vita del pacchetto client in un computer autonomo con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md)"><span data-ttu-id="d6995-114">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-115">Descrive come gestire i gruppi di connessioni tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell51.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md)"><span data-ttu-id="d6995-116">Come modificare la configurazione client con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-117">Descrive come modificare il client usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)"><span data-ttu-id="d6995-118">Come applicare il file di configurazione utente con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-119">Descrive come applicare un file di configurazione utente usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)"><span data-ttu-id="d6995-120">Come applicare il file di configurazione della distribuzione con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-121">Descrive come applicare un file di configurazione della distribuzione usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-51.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-51.md)"><span data-ttu-id="d6995-122">Come sequenziare un pacchetto usando PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-123">Descrive come creare un nuovo pacchetto usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell51.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md)"><span data-ttu-id="d6995-124">Come creare un acceleratore pacchetto con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-125">Descrive come creare un Acceleratore pacchetto usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="d6995-126">Puoi usare gli acceleratori pacchetto per sequenziare automaticamente applicazioni di grandi dimensioni e complesse.</span><span class="sxs-lookup"><span data-stu-id="d6995-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)"><span data-ttu-id="d6995-127">Come abilitare la creazione di report nel client App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-127">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-128">Descrive come abilitare il computer che gestisce l'App-V 5,1 per l'invio di informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="d6995-128">Describes how to enable the computer running the App-V 5.1 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md)"><span data-ttu-id="d6995-129">Come installare i database di App-V e convertire gli identificatori di sicurezza associati tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="d6995-130">Descrive come usare una matrice di nomi di account e per convertirli nel SID corrispondente in formati standard ed esadecimali.</span><span class="sxs-lookup"><span data-stu-id="d6995-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d6995-131">**Importante**  Verificare che gli script eseguiti con i pacchetti App-V corrispondano ai criteri di esecuzione configurati per PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6995-131">**Important** Make sure that any script you execute with your App-V packages matches the execution policy that you have configured for PowerShell.</span></span>

 

## <span data-ttu-id="d6995-132">Gestione degli errori di PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6995-132">PowerShell Error Handling</span></span>


<span data-ttu-id="d6995-133">Usare la tabella seguente per informazioni sulla gestione degli errori di PowerShell in App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="d6995-133">Use the following table for information about App-V 5.1 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6995-134">Evento</span><span class="sxs-lookup"><span data-stu-id="d6995-134">Event</span></span></th>
<th align="left"><span data-ttu-id="d6995-135">Azione</span><span class="sxs-lookup"><span data-stu-id="d6995-135">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6995-136">Uso dell'attributo RollbackOnError con gli script incorporati</span><span class="sxs-lookup"><span data-stu-id="d6995-136">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6995-137">Quando usi l' <strong> attributo RollbackOnError </strong> con gli script incorporati, l'attributo viene ignorato per gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6995-137">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="d6995-138">Rimozione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="d6995-138">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="d6995-139">Annullamento della pubblicazione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="d6995-139">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="d6995-140">Chiusura di un ambiente virtuale</span><span class="sxs-lookup"><span data-stu-id="d6995-140">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="d6995-141">Chiusura di un processo</span><span class="sxs-lookup"><span data-stu-id="d6995-141">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6995-142">Il nome del pacchetto contiene<strong>$</span><span class="sxs-lookup"><span data-stu-id="d6995-142">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d6995-143">Se il nome di un pacchetto contiene il carattere ( <strong> $ </strong> ), è necessario usare una virgoletta singola ( <strong> ' </strong> ), ad esempio</span><span class="sxs-lookup"><span data-stu-id="d6995-143">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="d6995-144">Add-AppvClientPackage ' Contoso $ App. AppV '</span><span class="sxs-lookup"><span data-stu-id="d6995-144">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="d6995-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6995-145">Related topics</span></span>


[<span data-ttu-id="d6995-146">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="d6995-146">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





