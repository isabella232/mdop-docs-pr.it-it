---
title: Informazioni su Microsoft Application Virtualization 4.6 SP2
description: Informazioni su Microsoft Application Virtualization 4.6 SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820016"
---
# <span data-ttu-id="bee1c-103">Informazioni su Microsoft Application Virtualization 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="bee1c-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="bee1c-104">Microsoft Application Virtualization (App-V) 4.6 SP2 offre diversi miglioramenti e nuove funzionalità, descritti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="bee1c-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="bee1c-105">**Attenzione**  Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bee1c-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="bee1c-106">Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="bee1c-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="bee1c-107">Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat).</span><span class="sxs-lookup"><span data-stu-id="bee1c-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="bee1c-108">Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="bee1c-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="bee1c-109">Cambiare il registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="bee1c-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="bee1c-110">Supporto per Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bee1c-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="bee1c-111">App-V 4.6 SP2 aggiunge il supporto per i Servizi Desktop remoto di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bee1c-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="bee1c-112">Supporto per la coesistenza con client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="bee1c-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="bee1c-113">App-V 4.6 SP2 offre il supporto per la coesistenza con il client Microsoft Application Virtualization 5,0.</span><span class="sxs-lookup"><span data-stu-id="bee1c-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="bee1c-114">Esaminare la documentazione di App-V 5,0 per istruzioni su come configurare il client App-V 5,0 per la coesistenza con il client App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="bee1c-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="bee1c-115">Per altre informazioni su App-V 5,0, vedere [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) in TechNet.</span><span class="sxs-lookup"><span data-stu-id="bee1c-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="bee1c-116">Possibilità di virtualizzare Adobe Reader X con la modalità protetta</span><span class="sxs-lookup"><span data-stu-id="bee1c-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="bee1c-117">È possibile virtualizzare Adobe Reader X con la funzionalità modalità protetta attivata usando le procedure seguenti.</span><span class="sxs-lookup"><span data-stu-id="bee1c-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="bee1c-118">In precedenza è stata necessario disabilitare la modalità protetta per virtualizzare Adobe Reader X.</span><span class="sxs-lookup"><span data-stu-id="bee1c-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="bee1c-119">Prima di avviare l'App-V Sequencer, creare il seguente valore del registro di sistema in HKEY \ _LOCAL \ _MACHINE directory \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span><span class="sxs-lookup"><span data-stu-id="bee1c-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee1c-120">Nome</span><span class="sxs-lookup"><span data-stu-id="bee1c-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee1c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="bee1c-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee1c-122">Dati</span><span class="sxs-lookup"><span data-stu-id="bee1c-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee1c-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bee1c-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee1c-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="bee1c-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee1c-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="bee1c-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee1c-126">1</span><span class="sxs-lookup"><span data-stu-id="bee1c-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee1c-127">Impostare questo valore su <strong> 1 per </strong> avviare Adobe Reader X in modalità protetta durante la fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="bee1c-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="bee1c-128">**Nota**  In un computer che gestisce un sistema operativo a 64 bit, creare il valore di registro in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span><span class="sxs-lookup"><span data-stu-id="bee1c-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="bee1c-129">Per ogni file OSD nel pacchetto di Adobe Reader X, aggiungere gli elementi seguenti nell' &lt; &gt; elemento policy:</span><span class="sxs-lookup"><span data-stu-id="bee1c-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="bee1c-130">Nuovo parametro della riga di comando sequencer</span><span class="sxs-lookup"><span data-stu-id="bee1c-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="bee1c-131">Quando si crea un Acceleratore pacchetto (PA) tramite la GUI sequencer, è possibile selezionare un file RTF o TXT che fornisca indicazioni per il packaging e la distribuzione agli amministratori che applicano l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bee1c-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="bee1c-132">Questa funzionalità è ora disponibile usando la CLI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="bee1c-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="bee1c-133">Specificare un percorso di un file RTF o TXT che fornisca indicazioni per il packaging e la distribuzione durante la creazione di un Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="bee1c-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="bee1c-134">La segnalazione degli errori delle applicazioni Microsoft non deve più essere installata</span><span class="sxs-lookup"><span data-stu-id="bee1c-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="bee1c-135">Quando si installa il client App-V 4.6 SP2 usando setup.msi, non è più necessario installare segnalazione errori applicazioni Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="bee1c-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="bee1c-136">App-V 4.6 SP2 ora usa la segnalazione degli errori Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bee1c-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="bee1c-137">Per altre informazioni, vedere [come installare il client App-V usando Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span><span class="sxs-lookup"><span data-stu-id="bee1c-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="bee1c-138">Feedback dei clienti e aggiornamento cumulativo</span><span class="sxs-lookup"><span data-stu-id="bee1c-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="bee1c-139">App-V 4.6 SP2 include un rollup di correzioni per risolvere i problemi rilevati dalla versione App-V 4,6 SP1.</span><span class="sxs-lookup"><span data-stu-id="bee1c-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="bee1c-140">App-V 4.6 SP2 contiene le correzioni più recenti fino a Microsoft Application Virtualization 4,6 SP1 hotfix 6.</span><span class="sxs-lookup"><span data-stu-id="bee1c-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="bee1c-141">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="bee1c-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="bee1c-142">Note sulla versione di App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="bee1c-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="bee1c-143">Fornisce le informazioni più aggiornate sui problemi noti di App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="bee1c-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





