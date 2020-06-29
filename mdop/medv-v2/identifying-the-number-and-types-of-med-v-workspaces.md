---
title: Identificazione del numero e dei tipi di aree di lavoro MED-V
description: Identificazione del numero e dei tipi di aree di lavoro MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827265"
---
# <span data-ttu-id="2614b-103">Identificazione del numero e dei tipi di aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2614b-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="2614b-104">MED-V crea un ambiente virtuale per l'esecuzione di applicazioni che richiedono Windows XP o che richiedono una versione di Internet Explorer diversa dalla versione nel computer host.</span><span class="sxs-lookup"><span data-stu-id="2614b-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="2614b-105">Questo ambiente virtuale è noto come area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="2614b-106">A seconda dei requisiti di compatibilità delle applicazioni incontrati dall'organizzazione mentre si esegue la migrazione a Windows 7, solo determinati utenti o reparti potrebbero richiedere aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="2614b-107">Quando si pianifica la distribuzione, è necessario determinare il numero di aree di lavoro MED-V necessarie nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2614b-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="2614b-108">È inoltre necessario definire i requisiti di ogni area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="2614b-109">Identificare il numero e i tipi di aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2614b-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="2614b-110">Identificare i computer e i gruppi dell'organizzazione per i quali verranno create aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="2614b-111">In genere, questi sono gli utenti che richiedono l'accesso alle applicazioni di cui non è possibile eseguire la migrazione in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2614b-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="2614b-112">Identificare le applicazioni di cui non è possibile eseguire la migrazione e gli utenti che necessitano di un'area di lavoro MED-V per eseguire queste applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2614b-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="2614b-113">Potresti anche avere indirizzi Intranet che non sono ancora stati ottimizzati per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2614b-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="2614b-114">L'area di lavoro MED-V offre un browser Internet Explorer in cui gli utenti finali possono accedere meglio agli indirizzi Web non ancora pronti per la migrazione a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2614b-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="2614b-115">Durante la preparazione e la pianificazione della distribuzione di MED-V, sarà necessario identificare e compilare un elenco degli indirizzi URL da reindirizzare da Internet Explorer nel computer host a Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="2614b-116">Infine, è necessario valutare i requisiti di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="2614b-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="2614b-117">La maggior parte delle aree di lavoro MED-V è di 2 gigabyte (GB) o più grande.</span><span class="sxs-lookup"><span data-stu-id="2614b-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="2614b-118">Lo spazio disponibile su disco in un sistema può essere consumato rapidamente, a seconda del numero di utenti e della configurazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="2614b-119">Inoltre, il metodo di distribuzione preferito della società può richiedere spazio aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="2614b-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="2614b-120">In genere, è consigliabile liberare un minimo di 10 GB di spazio su disco per un'area di lavoro MED-V, ma questo è molto diverso, a seconda delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2614b-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="2614b-121">Calcolare i requisiti di spazio su disco per le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2614b-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="2614b-122">Un'area di lavoro MED-V richiede memoria e spazio su disco dal computer host in cui è installato.</span><span class="sxs-lookup"><span data-stu-id="2614b-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="2614b-123">Nell'host è necessario un minimo di 2 GB di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="2614b-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="2614b-124">Lo spazio su disco è variabile e dipende dal numero di applicazioni e dai dati nell'area di lavoro MED-V di un utente.</span><span class="sxs-lookup"><span data-stu-id="2614b-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="2614b-125">È consigliabile un minimo di 10 GB di spazio su disco per MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="2614b-126">Questo importo consente l'utilizzo di un'area di lavoro di base di Windows XP e alcune applicazioni e il reindirizzamento Web installati di base.</span><span class="sxs-lookup"><span data-stu-id="2614b-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="2614b-127">Offre anche spazio disponibile per l'unità di scambio host.</span><span class="sxs-lookup"><span data-stu-id="2614b-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="2614b-128">In una configurazione di base, MED-V e una singola area di lavoro MED-V distribuita consumano fino a 6-8 GB.</span><span class="sxs-lookup"><span data-stu-id="2614b-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="2614b-129">Se si includono molte applicazioni nell'area di lavoro MED-V o si hanno più utenti per computer, è possibile usare il calcolo seguente per determinare in modo più accurato lo spazio su disco richiesto dall'area di lavoro MED-V:</span><span class="sxs-lookup"><span data-stu-id="2614b-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="2614b-130">VHD di base + (utente per computer x (differenza di disco + stato salvato))</span><span class="sxs-lookup"><span data-stu-id="2614b-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="2614b-131">Per calcolare lo spazio su disco richiesto, determinare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2614b-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="2614b-132">**Dimensioni del VHD di base** : il disco rigido virtuale usato per creare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="2614b-133">**Importante**  Non usare la dimensione del file con estensione MEDV per il calcolo perché il file con estensione MEDV è compresso.</span><span class="sxs-lookup"><span data-stu-id="2614b-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="2614b-134">**Utenti per computer** : Med-v crea un'area di lavoro MED-v per ogni utente in un computer; l'area di lavoro MED-V usa lo spazio su disco quando ogni utente accede e viene creata l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="2614b-135">**Dimensioni del disco differenze** , usato per tenere traccia della differenza dal VHD di base.</span><span class="sxs-lookup"><span data-stu-id="2614b-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="2614b-136">Questa dimensione varia man mano che si aggiungono applicazioni e aggiornamenti software al disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="2614b-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="2614b-137">Viene creato un disco differenze per ogni utente MED-V quando avviano MED-V per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="2614b-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="2614b-138">**Dimensioni del file di stato salvato** , usato per mantenere lo stato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2614b-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="2614b-139">In genere, questo è solo un po' più grande della RAM allocata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2614b-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="2614b-140">Ad esempio, 1 GB di RAM allocata crea un file di 1.081.000 KB.</span><span class="sxs-lookup"><span data-stu-id="2614b-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="2614b-141">L'esempio seguente mostra un calcolo basato su tre utenti di un'area di lavoro MED-V con un disco rigido virtuale di 2,6 GB:</span><span class="sxs-lookup"><span data-stu-id="2614b-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="2614b-142">2.6 GB + (3 x (1.5 GB + 1GB)) = 10.1 GB</span><span class="sxs-lookup"><span data-stu-id="2614b-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="2614b-143">**Nota**  Una procedura consigliata per MED-V consiste nel calcolare lo spazio richiesto usando una distribuzione di Lab per convalidare i requisiti.</span><span class="sxs-lookup"><span data-stu-id="2614b-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="2614b-144">Individuare i file per determinare le dimensioni del file</span><span class="sxs-lookup"><span data-stu-id="2614b-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="2614b-145">Le posizioni seguenti contengono i file per il computer e le impostazioni utente:</span><span class="sxs-lookup"><span data-stu-id="2614b-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2614b-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="2614b-146">Type</span></span></th>
<th align="left"><span data-ttu-id="2614b-147">Posizione</span><span class="sxs-lookup"><span data-stu-id="2614b-147">Location</span></span></th>
<th align="left"><span data-ttu-id="2614b-148">File</span><span class="sxs-lookup"><span data-stu-id="2614b-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2614b-149">VHD di base</span><span class="sxs-lookup"><span data-stu-id="2614b-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="2614b-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="2614b-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="2614b-151">InternalName </em> . vhd-Where <em> internalname </em> è il nome del disco rigido virtuale selezionato nel Packager area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2614b-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2614b-152">Disco differenze</span><span class="sxs-lookup"><span data-stu-id="2614b-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="2614b-153">Macchine%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="2614b-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="2614b-154">Workspacename </em> . vhd</span><span class="sxs-lookup"><span data-stu-id="2614b-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2614b-155">File di stato salvato</span><span class="sxs-lookup"><span data-stu-id="2614b-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="2614b-156">Macchine%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="2614b-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="2614b-157">Workspacename </em> . VSV</span><span class="sxs-lookup"><span data-stu-id="2614b-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2614b-158">Calcolare i requisiti di spazio su disco per le aree di lavoro MED-V condivise</span><span class="sxs-lookup"><span data-stu-id="2614b-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="2614b-159">Se si sta calcolando la distribuzione di un'area di lavoro MED-V condivisa in un singolo computer, il numero di utenti per computer nel calcolo è sempre "1" perché MED-V configura solo un singolo disco differenze per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="2614b-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="2614b-160">È possibile trovare il disco differenze e il file di stato salvato per le aree di lavoro MED-V condivise in%ProgramData%\\Microsoft\\Medv\\AllUsers.</span><span class="sxs-lookup"><span data-stu-id="2614b-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="2614b-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2614b-161">Related topics</span></span>


[<span data-ttu-id="2614b-162">Definire e pianificare la distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="2614b-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="2614b-163">Pianificazione di MED-V</span><span class="sxs-lookup"><span data-stu-id="2614b-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





