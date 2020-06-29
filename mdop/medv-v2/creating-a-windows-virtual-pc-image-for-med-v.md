---
title: Creazione di un'immagine di Windows Virtual PC per MED-V
description: Creazione di un'immagine di Windows Virtual PC per MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804413"
---
# <span data-ttu-id="55f6e-103">Creazione di un'immagine di Windows Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="55f6e-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="55f6e-104">Prima di poter consegnare un'area di lavoro MED-V agli utenti, è necessario prima di tutto preparare un disco rigido virtuale che si usa per creare il pacchetto di installazione dell'area di lavoro MED-V per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="55f6e-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="55f6e-105">Per preparare il disco rigido virtuale necessario, è necessario creare un'immagine di PC virtuale Windows che contiene il sistema operativo, gli aggiornamenti e il software necessari per consentire di distribuire in seguito le informazioni di reindirizzamento degli URL e delle applicazioni agli utenti.</span><span class="sxs-lookup"><span data-stu-id="55f6e-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="55f6e-106">In questa sezione vengono fornite indicazioni su come creare il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="55f6e-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="55f6e-107">Per creare un'immagine virtuale per MED-V, è necessario seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="55f6e-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="55f6e-108">Creare un'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55f6e-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="55f6e-109">Installare Windows XP nell'immagine</span><span class="sxs-lookup"><span data-stu-id="55f6e-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="55f6e-110">Installare .NET Framework nell'immagine</span><span class="sxs-lookup"><span data-stu-id="55f6e-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="55f6e-111">Applicare gli aggiornamenti all'immagine</span><span class="sxs-lookup"><span data-stu-id="55f6e-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="55f6e-112">Installare i componenti di integrazione</span><span class="sxs-lookup"><span data-stu-id="55f6e-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="55f6e-113">Creazione di un'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55f6e-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="55f6e-114">Per creare un'immagine di Windows Virtual PC, vedere la documentazione di Windows Virtual PC:</span><span class="sxs-lookup"><span data-stu-id="55f6e-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="55f6e-115">[Home page di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="55f6e-116">[Guida di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="55f6e-117">In alternativa, se si ha già un file Windows Imaging (WIM) che si vuole usare come base per l'immagine virtuale, è possibile convertirlo in un VHD che si usa per creare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="55f6e-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="55f6e-118">Per altre informazioni su come convertire un WIM in un disco rigido virtuale, vedere [supporto del VHD nativo in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="55f6e-119">**Importante**  MED-V supporta solo un disco rigido virtuale per ogni macchina virtuale e una sola partizione in ogni disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="55f6e-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="55f6e-120">Dopo aver creato il disco rigido virtuale, installare Windows XP nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="55f6e-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="55f6e-121">Installazione di Windows XP in un'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55f6e-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="55f6e-122">MED-V richiede che Windows XP SP3 sia installato nell'immagine PC virtuale Windows prima di creare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="55f6e-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="55f6e-123">Per altre informazioni su come installare Windows XP, vedere [creare una macchina virtuale e installare un sistema operativo guest](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="55f6e-124">Installazione di .NET Framework 3,5 SP1 in un'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55f6e-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="55f6e-125">È necessario installare manualmente .NET Framework 3,5 SP1 e l'aggiornamento di KB959209 nell'immagine di Windows Virtual PC preparata per l'uso con MED-V.</span><span class="sxs-lookup"><span data-stu-id="55f6e-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="55f6e-126">L'aggiornamento [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) affronta diversi problemi noti di compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="55f6e-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="55f6e-127">Applicazione degli aggiornamenti all'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55f6e-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="55f6e-128">Dopo aver installato Windows XP nella propria macchina virtuale, installare gli aggiornamenti necessari di Windows XP nell'immagine, ad esempio SP3.</span><span class="sxs-lookup"><span data-stu-id="55f6e-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="55f6e-129">È anche possibile installare alcuni aggiornamenti facoltativi per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="55f6e-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="55f6e-130">**Importante**  MED-V richiede che Windows XP SP3 sia in uso nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="55f6e-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="55f6e-131">**Avviso**  Quando si installano gli aggiornamenti in Windows XP, assicurarsi di rimanere nella versione di Internet Explorer nell'ospite che si intende usare nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="55f6e-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="55f6e-132">Ad esempio, se si intende eseguire Internet Explorer 6 nell'area di lavoro MED-V, verificare che gli eventuali aggiornamenti installati non includano Internet Explorer 7 o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="55f6e-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="55f6e-133">Inoltre, è consigliabile configurare il registro di sistema per evitare aggiornamenti automatici dall'aggiornamento di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="55f6e-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="55f6e-134">Installazione di un aggiornamento delle prestazioni facoltativo</span><span class="sxs-lookup"><span data-stu-id="55f6e-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="55f6e-135">Anche se è facoltativo, è consigliabile installare il seguente aggiornamento per l' [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="55f6e-136">Questo aggiornamento aumenta le prestazioni delle cartelle condivise in una sessione di Servizi terminal:</span><span class="sxs-lookup"><span data-stu-id="55f6e-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="55f6e-137">**Nota**  L'aggiornamento è pubblicamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="55f6e-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="55f6e-138">Tuttavia, potrebbe essere richiesto di accettare un contratto per i servizi Microsoft.</span><span class="sxs-lookup"><span data-stu-id="55f6e-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="55f6e-139">Seguire le istruzioni sulle pagine Web successive per recuperare questo hotfix.</span><span class="sxs-lookup"><span data-stu-id="55f6e-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="55f6e-140">Configurazione di un aggiornamento delle prestazioni di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="55f6e-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="55f6e-141">Per impostazione predefinita, i criteri di gruppo vengono scaricati in un computer un byte alla volta.</span><span class="sxs-lookup"><span data-stu-id="55f6e-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="55f6e-142">Ciò causa ritardi durante l'aggiunta di MED-V al dominio.</span><span class="sxs-lookup"><span data-stu-id="55f6e-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="55f6e-143">Per aumentare le prestazioni dei criteri di gruppo, impostare il valore della chiave del registro di sistema seguente nel registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="55f6e-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="55f6e-144">Sottochiave del registro di sistema: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="55f6e-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="55f6e-145">Voce: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="55f6e-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="55f6e-146">Digitare: DWORD</span><span class="sxs-lookup"><span data-stu-id="55f6e-146">Type: DWORD</span></span>

<span data-ttu-id="55f6e-147">Valore: 1</span><span class="sxs-lookup"><span data-stu-id="55f6e-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="55f6e-148">Installazione di componenti di integrazione</span><span class="sxs-lookup"><span data-stu-id="55f6e-148">Installing Integration Components</span></span>


<span data-ttu-id="55f6e-149">Windows Virtual PC include il pacchetto componenti integrativi.</span><span class="sxs-lookup"><span data-stu-id="55f6e-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="55f6e-150">In questo articolo vengono fornite caratteristiche che migliorano l'interazione tra l'ambiente virtuale e il computer fisico.</span><span class="sxs-lookup"><span data-stu-id="55f6e-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="55f6e-151">Ad esempio, il pacchetto componenti integrativi consente di passare al mouse tra l'host e i computer guest.</span><span class="sxs-lookup"><span data-stu-id="55f6e-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="55f6e-152">**Importante**  MED-V richiede l'installazione del pacchetto componenti integrativi.</span><span class="sxs-lookup"><span data-stu-id="55f6e-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="55f6e-153">Quando si configura l'immagine virtuale per l'uso con MED-V, è necessario installare manualmente il pacchetto componenti integrativi nel sistema operativo guest per rendere disponibili le caratteristiche di integrazione.</span><span class="sxs-lookup"><span data-stu-id="55f6e-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="55f6e-154">Per altre informazioni su come installare e usare il pacchetto componenti integrativi, vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="55f6e-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="55f6e-155">[Installare o aggiornare il pacchetto componenti integrativi](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="55f6e-156">[Informazioni sulle caratteristiche di integrazione](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="55f6e-157">Installazione di aggiornamento RemoteApp</span><span class="sxs-lookup"><span data-stu-id="55f6e-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="55f6e-158">Dopo aver installato il pacchetto componenti integrativi, viene chiesto di installare l'aggiornamento seguente: "aggiornamento per Windows XP SP3 per abilitare RemoteApp".</span><span class="sxs-lookup"><span data-stu-id="55f6e-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="55f6e-159">Questo è un componente obbligatorio per MED-V.</span><span class="sxs-lookup"><span data-stu-id="55f6e-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="55f6e-160">**Importante**  Se non viene chiesto di installare l'aggiornamento RemoteApp, è necessario scaricarlo e installarlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="55f6e-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="55f6e-161">Per altre informazioni e istruzioni su come scaricare questo aggiornamento, vedere [aggiornamento per Windows XP SP3 per abilitare RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="55f6e-162">Abilitazione del desktop remoto</span><span class="sxs-lookup"><span data-stu-id="55f6e-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="55f6e-163">Per impostazione predefinita, il desktop remoto è abilitato dopo l'installazione del pacchetto componenti integrativi.</span><span class="sxs-lookup"><span data-stu-id="55f6e-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="55f6e-164">Affinché MED-V sia operativo, verificare che desktop remoto sia abilitato e non distribuire criteri di gruppo che la disabilitano.</span><span class="sxs-lookup"><span data-stu-id="55f6e-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="55f6e-165">Per informazioni su come abilitare Desktop remoto, vedere [abilitare o disabilitare Desktop remoto](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="55f6e-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="55f6e-166">Personalizzazione di Internet Explorer tramite il kit di amministrazione di Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="55f6e-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="55f6e-167">Se si vuole, è possibile usare Internet Explorer Administration Kit per personalizzare Internet Explorer nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="55f6e-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="55f6e-168">Per altre informazioni, vedere il [Kit di amministrazione e la guida alla distribuzione di Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).</span><span class="sxs-lookup"><span data-stu-id="55f6e-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="55f6e-169">**Avviso**  È consigliabile considerare i problemi di sicurezza associati alla personalizzazione di Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="55f6e-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="55f6e-170">Per altre informazioni, vedere [procedure consigliate per la sicurezza per le operazioni MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="55f6e-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="55f6e-171">Dopo aver installato il disco rigido virtuale con un sistema operativo guest aggiornato, è possibile installare le applicazioni nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="55f6e-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="55f6e-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55f6e-172">Related topics</span></span>


[<span data-ttu-id="55f6e-173">Installazione di applicazioni in un'immagine di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55f6e-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="55f6e-174">Configurazione di un'immagine di Windows Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="55f6e-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





