---
title: Opzioni della riga di comando per i file di installazione MED-V
description: Opzioni della riga di comando per i file di installazione MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826466"
---
# <span data-ttu-id="99d07-103">Opzioni della riga di comando per i file di installazione MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-103">Command-Line Options for MED-V Installation Files</span></span>


<span data-ttu-id="99d07-104">Quando si installa o si disinstalla Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, è possibile eseguire i file di installazione al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="99d07-104">When you install or uninstall Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="99d07-105">Questa sezione descrive diverse opzioni che è possibile specificare quando si installa o si disinstalla MED-V al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="99d07-105">This section describes different options that you can specify when you install or uninstall MED-V at the command prompt.</span></span>

### <span data-ttu-id="99d07-106">Argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="99d07-106">Command-Line Arguments</span></span>

<span data-ttu-id="99d07-107">Puoi usare gli argomenti della riga di comando seguenti insieme ai rispettivi file di installazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="99d07-107">You can use the following command-line arguments together with their respective MED-V installation files.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="99d07-108">File di installazione</span><span class="sxs-lookup"><span data-stu-id="99d07-108">Installation File</span></span></th>
<th align="left"><span data-ttu-id="99d07-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="99d07-109">Argument</span></span></th>
<th align="left"><span data-ttu-id="99d07-110">Valori accettati</span><span class="sxs-lookup"><span data-stu-id="99d07-110">Accepted Values</span></span></th>
<th align="left"><span data-ttu-id="99d07-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="99d07-111">Type</span></span></th>
<th align="left"><span data-ttu-id="99d07-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99d07-112">Description</span></span></th>
<th align="left"><span data-ttu-id="99d07-113">Default</span><span class="sxs-lookup"><span data-stu-id="99d07-113">Default</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99d07-114">Agente host</span><span class="sxs-lookup"><span data-stu-id="99d07-114">Host Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-115">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="99d07-115">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-116">&lt;percorso di installazione&gt;</span><span class="sxs-lookup"><span data-stu-id="99d07-116">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-117">Installazione</span><span class="sxs-lookup"><span data-stu-id="99d07-117">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-118">Modificare la directory installata</span><span class="sxs-lookup"><span data-stu-id="99d07-118">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-119">L'installazione passa a Programmi\Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="99d07-119">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="99d07-120">Packager area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-120">MED-V Workspace Packager</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-121">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="99d07-121">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-122">&lt;percorso di installazione&gt;</span><span class="sxs-lookup"><span data-stu-id="99d07-122">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-123">Installazione</span><span class="sxs-lookup"><span data-stu-id="99d07-123">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-124">Modificare la directory installata</span><span class="sxs-lookup"><span data-stu-id="99d07-124">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-125">L'installazione passa a Programmi\Microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="99d07-125">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99d07-126">Area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-126">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-127">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="99d07-127">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-128">&lt;percorso di installazione&gt;</span><span class="sxs-lookup"><span data-stu-id="99d07-128">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-129">Installazione</span><span class="sxs-lookup"><span data-stu-id="99d07-129">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-130">Modificare la directory installata</span><span class="sxs-lookup"><span data-stu-id="99d07-130">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-131">L'installazione passa a ProgramData\Microsoft\Medv\Workspace.</span><span class="sxs-lookup"><span data-stu-id="99d07-131">Installation goes to ProgramData\Microsoft\Medv\Workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="99d07-132">Area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-132">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-133">SOVRASCRIVERE VHD</span><span class="sxs-lookup"><span data-stu-id="99d07-133">OVERWRITE VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-134">0 o 1</span><span class="sxs-lookup"><span data-stu-id="99d07-134">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-135">Installazione</span><span class="sxs-lookup"><span data-stu-id="99d07-135">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-136">Errore di installazione se il VHD esiste (0) o sovrascrive il VHD esistente (1).</span><span class="sxs-lookup"><span data-stu-id="99d07-136">Fail installation if VHD exists(0) or overwrite existing VHD(1).</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-137">La sovrascrittura non si verifica e l'installazione non riesce se esiste già un disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="99d07-137">Overwrite does not occur and installation fails if a virtual hard disk (VHD) already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="99d07-138">Area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-138">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-139">SUPPRESSMEDVLAUNCH</span><span class="sxs-lookup"><span data-stu-id="99d07-139">SUPPRESSMEDVLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-140">0 o 1</span><span class="sxs-lookup"><span data-stu-id="99d07-140">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-141">Installazione</span><span class="sxs-lookup"><span data-stu-id="99d07-141">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-142">Avviare (0) o non avviare (1) MED-V dopo l'installazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="99d07-142">Start(0) or do not start(1) MED-V after MED-V workspace is installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-143">Se l'area di lavoro MED-V è stata installata con l'interfaccia utente, una casella di controllo nella <strong> </strong> pagina fine controlla se avviare MED-v.</span><span class="sxs-lookup"><span data-stu-id="99d07-143">If the MED-V workspace was installed with the user interface (UI), a check box on the <strong>Finish</strong> page controls whether to start MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="99d07-144">Area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-144">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-145">DELETEDIFFDISKS</span><span class="sxs-lookup"><span data-stu-id="99d07-145">DELETEDIFFDISKS</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-146">0 o 1</span><span class="sxs-lookup"><span data-stu-id="99d07-146">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-147">Disinstallazione</span><span class="sxs-lookup"><span data-stu-id="99d07-147">Uninstallation</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-148">Mantieni (0) o Elimina (1) VHD creati da MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-148">Keep(0) or delete(1) VHDs created by MED-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="99d07-149">Nessun VHD viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="99d07-149">No VHDs are deleted.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="99d07-150">Esempi di argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="99d07-150">Examples of Command-Line Arguments</span></span>

<span data-ttu-id="99d07-151">Nell'esempio seguente viene installata l'area di lavoro MED-V creata dal Packager area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="99d07-151">The following example installs the MED-V workspace created by the MED-V workspace Packager.</span></span> <span data-ttu-id="99d07-152">Il file di installazione crea un file di log nella directory Temp ed esegue il file di installazione in modalità non interattiva, ma non avvia il completamento dell'agente host MED-V.</span><span class="sxs-lookup"><span data-stu-id="99d07-152">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode, but does not start the MED-V Host Agent on completion.</span></span> <span data-ttu-id="99d07-153">Il file di installazione sovrascrive qualsiasi VHD lasciato da un'installazione precedente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="99d07-153">The installation file overwrites any VHD left behind by a previous installation that has the same name.</span></span>

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

<span data-ttu-id="99d07-154">Nell'esempio seguente viene disinstallata l'area di lavoro MED-V installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="99d07-154">The following example uninstalls the MED-V workspace that was previously installed.</span></span> <span data-ttu-id="99d07-155">Il file di installazione crea un file di log nella directory Temp ed esegue il file di installazione in modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="99d07-155">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode.</span></span> <span data-ttu-id="99d07-156">Il file di installazione Elimina i file di disco rigido virtuali rimanenti dal file System.</span><span class="sxs-lookup"><span data-stu-id="99d07-156">The installation file deletes any remaining virtual hard disk files from the file system.</span></span>

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## <span data-ttu-id="99d07-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99d07-157">Related topics</span></span>


[<span data-ttu-id="99d07-158">Distribuire i componenti MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-158">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

[<span data-ttu-id="99d07-159">Documentazione tecnica su MED-V</span><span class="sxs-lookup"><span data-stu-id="99d07-159">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





