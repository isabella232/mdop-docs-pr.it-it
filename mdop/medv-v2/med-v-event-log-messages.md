---
title: Messaggi del registro eventi MED-V
description: Messaggi del registro eventi MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823076"
---
# <span data-ttu-id="dca64-103">Messaggi del registro eventi MED-V</span><span class="sxs-lookup"><span data-stu-id="dca64-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="dca64-104">I file di log per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 offrono informazioni dettagliate su come distribuire e gestire MED-V nell'organizzazione e consentire la verifica della funzionalità o la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="dca64-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="dca64-105">ID evento</span><span class="sxs-lookup"><span data-stu-id="dca64-105">Event IDs</span></span>


<span data-ttu-id="dca64-106">Di seguito è riportato un elenco di ID evento MED-V per risolvere i problemi che possono verificarsi durante la distribuzione o la gestione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="dca64-107">FTS</span><span class="sxs-lookup"><span data-stu-id="dca64-107">Fts</span></span>

<span data-ttu-id="dca64-108">Mostra gli ID evento per la configurazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="dca64-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="dca64-109">ID evento 3066</span><span class="sxs-lookup"><span data-stu-id="dca64-109">Event ID 3066</span></span>

<span data-ttu-id="dca64-110">Avviare l'operazione macchina virtuale non riuscita.</span><span class="sxs-lookup"><span data-stu-id="dca64-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-111">Description</span></span>**  
<span data-ttu-id="dca64-112">Esiste un potenziale problema con il disco rigido virtuale (VHD) usato per creare un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-113">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-113">Solution</span></span>**  
<span data-ttu-id="dca64-114">Verificare che sia possibile creare una macchina virtuale con il VHD per MED-V e che possa essere avviata.</span><span class="sxs-lookup"><span data-stu-id="dca64-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="dca64-115">ID evento 3071</span><span class="sxs-lookup"><span data-stu-id="dca64-115">Event ID 3071</span></span>

<span data-ttu-id="dca64-116">La preparazione della macchina virtuale non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="dca64-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-117">Description</span></span>**  
<span data-ttu-id="dca64-118">Si è verificato un problema con la configurazione per la prima volta che potrebbe essere stata causata da molti problemi diversi.</span><span class="sxs-lookup"><span data-stu-id="dca64-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="dca64-119">Questi includono problemi di connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="dca64-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-120">Solution</span></span>**  
<span data-ttu-id="dca64-121">Riavviare l'agente host MED-V per eseguire nuovamente la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="dca64-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="dca64-122">ID evento 3078</span><span class="sxs-lookup"><span data-stu-id="dca64-122">Event ID 3078</span></span>

<span data-ttu-id="dca64-123">La preparazione della macchina virtuale non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="dca64-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-124">Description</span></span>**  
<span data-ttu-id="dca64-125">Un problema potenziale esiste con il VHD usato per creare un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-126">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-126">Solution</span></span>**  
<span data-ttu-id="dca64-127">Verificare che sia possibile creare una macchina virtuale con il VHD per MED-V e che possa essere avviata.</span><span class="sxs-lookup"><span data-stu-id="dca64-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="dca64-128">ID evento 3079</span><span class="sxs-lookup"><span data-stu-id="dca64-128">Event ID 3079</span></span>

<span data-ttu-id="dca64-129">Riprovare la preparazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-130">Description</span></span>**  
<span data-ttu-id="dca64-131">MED-V sta provando a preparare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-132">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-132">Solution</span></span>**  
<span data-ttu-id="dca64-133">Non è richiesta alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="dca64-133">No action is required.</span></span> <span data-ttu-id="dca64-134">Consentire la configurazione del primo tempo.</span><span class="sxs-lookup"><span data-stu-id="dca64-134">Let first time setup finish.</span></span>

### <span data-ttu-id="dca64-135">ID evento 3080</span><span class="sxs-lookup"><span data-stu-id="dca64-135">Event ID 3080</span></span>

<span data-ttu-id="dca64-136">Il client è stato interrotto durante la preparazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-137">Description</span></span>**  
<span data-ttu-id="dca64-138">MED-V si arresta in modo imprevisto quando tenta di preparare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-139">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-139">Solution</span></span>**  
<span data-ttu-id="dca64-140">Avviare l'agente host MED-V e consentire il completamento della configurazione per la prima volta</span><span class="sxs-lookup"><span data-stu-id="dca64-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="dca64-141">ID evento 3084</span><span class="sxs-lookup"><span data-stu-id="dca64-141">Event ID 3084</span></span>

<span data-ttu-id="dca64-142">La macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="dca64-142">Virtual machine is not valid.</span></span> <span data-ttu-id="dca64-143">È necessario eseguire di nuovo la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="dca64-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-144">Description</span></span>**  
<span data-ttu-id="dca64-145">L'agente host MED-V ha rilevato un problema con la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-146">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-146">Solution</span></span>**  
<span data-ttu-id="dca64-147">Non è richiesta alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="dca64-147">No action is required.</span></span> <span data-ttu-id="dca64-148">Consentire la configurazione del primo tempo.</span><span class="sxs-lookup"><span data-stu-id="dca64-148">Let first time setup finish.</span></span>

### <span data-ttu-id="dca64-149">ID evento 3099</span><span class="sxs-lookup"><span data-stu-id="dca64-149">Event ID 3099</span></span>

<span data-ttu-id="dca64-150">Chiamata per avviare la macchina virtuale non riuscita.</span><span class="sxs-lookup"><span data-stu-id="dca64-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-151">Description</span></span>**  
<span data-ttu-id="dca64-152">Esiste un potenziale problema con il VHD in uso per creare un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-153">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-153">Solution</span></span>**  
<span data-ttu-id="dca64-154">Verificare che sia possibile creare una macchina virtuale con il VHD per MED-V e che sia possibile aprirla.</span><span class="sxs-lookup"><span data-stu-id="dca64-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="dca64-155">Gestione VM</span><span class="sxs-lookup"><span data-stu-id="dca64-155">VM Management</span></span>

### <span data-ttu-id="dca64-156">ID evento 4022</span><span class="sxs-lookup"><span data-stu-id="dca64-156">Event ID 4022</span></span>

<span data-ttu-id="dca64-157">Errore irreversibile VMManagerException durante l'esecuzione del comando su VM.</span><span class="sxs-lookup"><span data-stu-id="dca64-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-158">Description</span></span>**  
<span data-ttu-id="dca64-159">L'utente finale ha provato a uscire da MED-V disconnettendosi o chiudendo l'host MED-V e l'impostazione di configurazione di VMTaskTimeout è stata superata.</span><span class="sxs-lookup"><span data-stu-id="dca64-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-160">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-160">Solution</span></span>**  
<span data-ttu-id="dca64-161">Riavviare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-161">Restart MED-V.</span></span>

### <span data-ttu-id="dca64-162">ID evento 4028</span><span class="sxs-lookup"><span data-stu-id="dca64-162">Event ID 4028</span></span>

<span data-ttu-id="dca64-163">Operazione VM scaduta.</span><span class="sxs-lookup"><span data-stu-id="dca64-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-164">Description</span></span>**  
<span data-ttu-id="dca64-165">L'utente finale ha provato a uscire da MED-V disconnettendosi o chiudendo l'host e l'impostazione di configurazione VMTaskTimeout è stata superata.</span><span class="sxs-lookup"><span data-stu-id="dca64-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-166">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-166">Solution</span></span>**  
<span data-ttu-id="dca64-167">Riavviare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-167">Restart MED-V.</span></span>

### <span data-ttu-id="dca64-168">ID evento 4038</span><span class="sxs-lookup"><span data-stu-id="dca64-168">Event ID 4038</span></span>

<span data-ttu-id="dca64-169">Vmsal ha pubblicato un messaggio di errore per l'utente.</span><span class="sxs-lookup"><span data-stu-id="dca64-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-170">Description</span></span>**  
<span data-ttu-id="dca64-171">Viene visualizzato un messaggio di errore per l'utente finale che indica che MED-V non ha potuto avviare l'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-172">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-172">Solution</span></span>**  
<span data-ttu-id="dca64-173">Se l'errore viene registrato due o più volte in una riga, arrestare MED-V e connettersi alla macchina virtuale tramite Windows Virtual PC console e provare ad avviare l'applicazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="dca64-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="dca64-174">ID evento 4040</span><span class="sxs-lookup"><span data-stu-id="dca64-174">Event ID 4040</span></span>

<span data-ttu-id="dca64-175">Riciclo delle aggiunte perché TerminalServices non viene inizializzato nel guest.</span><span class="sxs-lookup"><span data-stu-id="dca64-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-176">Description</span></span>**  
<span data-ttu-id="dca64-177">MED-V ha riavviato la macchina virtuale perché i Servizi Desktop remoto non sono stati inizializzati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-178">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-178">Solution</span></span>**  
<span data-ttu-id="dca64-179">Se l'errore viene registrato due o più volte in una riga, arrestare MED-V e connettersi alla macchina virtuale tramite Windows Virtual PC Console.</span><span class="sxs-lookup"><span data-stu-id="dca64-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="dca64-180">ID evento 4042</span><span class="sxs-lookup"><span data-stu-id="dca64-180">Event ID 4042</span></span>

<span data-ttu-id="dca64-181">Non è riuscito a riciclare le aggiunte nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="dca64-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-182">Description</span></span>**  
<span data-ttu-id="dca64-183">MED-V non è riuscito a riciclare le aggiunte della macchina virtuale nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-184">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-184">Solution</span></span>**  
<span data-ttu-id="dca64-185">Se l'errore viene registrato due o più volte in una riga, arrestare MED-V e connettersi alla macchina virtuale tramite Windows Virtual PC Console.</span><span class="sxs-lookup"><span data-stu-id="dca64-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="dca64-186">ID evento 4043</span><span class="sxs-lookup"><span data-stu-id="dca64-186">Event ID 4043</span></span>

<span data-ttu-id="dca64-187">Non è possibile reimpostare la password scaduta nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-188">Description</span></span>**  
<span data-ttu-id="dca64-189">L'utente finale non ha reimpostato la password nella macchina virtuale prima di essere scaduta.</span><span class="sxs-lookup"><span data-stu-id="dca64-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="dca64-190">Di conseguenza, l'utente potrebbe non essere in grado di accedere alle risorse di rete o di salvare il lavoro.</span><span class="sxs-lookup"><span data-stu-id="dca64-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-191">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-191">Solution</span></span>**  
<span data-ttu-id="dca64-192">Arrestare l'ospite MED-V e riavviarlo.</span><span class="sxs-lookup"><span data-stu-id="dca64-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="dca64-193">Reindirizzamento URL</span><span class="sxs-lookup"><span data-stu-id="dca64-193">URL Redirection</span></span>

### <span data-ttu-id="dca64-194">ID evento 5005</span><span class="sxs-lookup"><span data-stu-id="dca64-194">Event ID 5005</span></span>

<span data-ttu-id="dca64-195">Impossibile ottenere il nome VM dalla configurazione; non è possibile avviare il browser Guest.</span><span class="sxs-lookup"><span data-stu-id="dca64-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-196">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-196">Description</span></span>**  
<span data-ttu-id="dca64-197">Il reindirizzamento degli URL non ha potuto ottenere il nome dell'area di lavoro MED-V dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="dca64-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="dca64-198">Di conseguenza, non può informare Windows Virtual PC per aprire l'URL reindirizzato nel browser dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-199">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-199">Solution</span></span>**  
<span data-ttu-id="dca64-200">Assicurarsi che il nome dell'area di lavoro MED-V sia impostato e che corrisponda a un nome di macchina virtuale nella &lt; *user* &gt; directory dei computer \\Virtual utente di C:\\Users\\.</span><span class="sxs-lookup"><span data-stu-id="dca64-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="dca64-201">Il nome dell'area di lavoro MED-V si trova in HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="dca64-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="dca64-202">Ad esempio, se l'utente è "Matt" e il nome dell'area di lavoro è "mattsworkspace", il valore di HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve essere "mattsworkspace" e dovrebbe essere presente un file denominato C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="dca64-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="dca64-203">ID evento 5006</span><span class="sxs-lookup"><span data-stu-id="dca64-203">Event ID 5006</span></span>

<span data-ttu-id="dca64-204">Impossibile creare il server pipe.</span><span class="sxs-lookup"><span data-stu-id="dca64-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-205">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-205">Description</span></span>**  
<span data-ttu-id="dca64-206">Il servizio di reindirizzamento degli URL non può creare il server pipe per comunicare con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dca64-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-207">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-207">Solution</span></span>**  
<span data-ttu-id="dca64-208">Controllare i registri degli eventi di sistema per tentare di creare un file o una risorsa il cui percorso inizia in modo simile al seguente: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" e termina con il nome utente e il nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dca64-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="dca64-209">Se non è presente nel log eventi, riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="dca64-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="dca64-210">ConfigMgr (ospite)</span><span class="sxs-lookup"><span data-stu-id="dca64-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="dca64-211">ID evento 7001</span><span class="sxs-lookup"><span data-stu-id="dca64-211">Event ID 7001</span></span>

<span data-ttu-id="dca64-212">I dati di configurazione della rete host non sono formattati correttamente.</span><span class="sxs-lookup"><span data-stu-id="dca64-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-213">Description</span></span>**  
<span data-ttu-id="dca64-214">La configurazione di rete ricevuta dall'host è una stringa XML formattata in modo non corretto o le informazioni di rete restituite dall'host non possono essere scritte in un documento XML.</span><span class="sxs-lookup"><span data-stu-id="dca64-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-215">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-215">Solution</span></span>**  
<span data-ttu-id="dca64-216">Riavviare il computer host e la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="dca64-217">ID evento 7005</span><span class="sxs-lookup"><span data-stu-id="dca64-217">Event ID 7005</span></span>

<span data-ttu-id="dca64-218">È stata rilevata una modifica alla configurazione della rete host, ma non è stato possibile applicarla perché i dati di configurazione della rete host non sono stati formattati correttamente.</span><span class="sxs-lookup"><span data-stu-id="dca64-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-219">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-219">Description</span></span>**  
<span data-ttu-id="dca64-220">Una modifica alla configurazione della rete host è stata comunicata alla macchina virtuale, ma non è stato possibile elaborarla nella macchina virtuale a causa di un errore.</span><span class="sxs-lookup"><span data-stu-id="dca64-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="dca64-221">Questo errore potrebbe essere causato da dati formattati in modo non corretto o dall'impossibilità di impostare le informazioni nell'istanza di CCMNetworkAdapter di Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dca64-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-222">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-222">Solution</span></span>**  
<span data-ttu-id="dca64-223">Riavviare l'host e la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="dca64-224">ConfigMgr (host)</span><span class="sxs-lookup"><span data-stu-id="dca64-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="dca64-225">ID evento 8006</span><span class="sxs-lookup"><span data-stu-id="dca64-225">Event ID 8006</span></span>

<span data-ttu-id="dca64-226">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-227">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-227">Description</span></span>**  
<span data-ttu-id="dca64-228">Windows Virtual PC 7 non è in grado di individuare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="dca64-229">La macchina virtuale potrebbe essere stata eliminata, spostata, rimossa o l'accesso è stato negato.</span><span class="sxs-lookup"><span data-stu-id="dca64-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-230">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-230">Solution</span></span>**  
<span data-ttu-id="dca64-231">Reinstallare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="dca64-232">ID evento 8008</span><span class="sxs-lookup"><span data-stu-id="dca64-232">Event ID 8008</span></span>

<span data-ttu-id="dca64-233">Non è stato possibile recuperare le informazioni di configurazione della rete della workstation.</span><span class="sxs-lookup"><span data-stu-id="dca64-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-234">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-234">Description</span></span>**  
<span data-ttu-id="dca64-235">Non è stato possibile raccogliere informazioni di configurazione della rete dall'host MED-V, probabilmente a causa di un errore di chiamata di sistema in .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dca64-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="dca64-236">Questo errore può verificarsi anche se le informazioni di rete restituite dall'host MED-V non possono essere scritte in un documento XML.</span><span class="sxs-lookup"><span data-stu-id="dca64-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-237">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-237">Solution</span></span>**  
<span data-ttu-id="dca64-238">Riavviare la workstation host.</span><span class="sxs-lookup"><span data-stu-id="dca64-238">Restart the host workstation.</span></span>

### <span data-ttu-id="dca64-239">ID evento 8010</span><span class="sxs-lookup"><span data-stu-id="dca64-239">Event ID 8010</span></span>

<span data-ttu-id="dca64-240">I dati di configurazione della rete non possono essere impostati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-241">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-241">Description</span></span>**  
<span data-ttu-id="dca64-242">Non è stato possibile comunicare l'indirizzo NAT (MED-V hostnetwork Address Translation) alla macchina virtuale, probabilmente perché la macchina virtuale è in uno stato difettoso o le aggiunte di Windows Virtual PC non sono state installate o abilitate.</span><span class="sxs-lookup"><span data-stu-id="dca64-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-243">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-243">Solution</span></span>**  
<span data-ttu-id="dca64-244">Arrestare e riavviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="dca64-245">Inoltre, potrebbe essere necessario reinstallare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="dca64-246">ID evento 8011</span><span class="sxs-lookup"><span data-stu-id="dca64-246">Event ID 8011</span></span>

<span data-ttu-id="dca64-247">I dati di configurazione della rete non possono essere reimpostati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-248">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-248">Description</span></span>**  
<span data-ttu-id="dca64-249">La configurazione di hostnetwork MED-V (BRIDGEd) non può essere comunicata alla macchina virtuale, probabilmente perché la macchina virtuale è in uno stato difettoso o le aggiunte di Windows Virtual PC non sono state installate o abilitate.</span><span class="sxs-lookup"><span data-stu-id="dca64-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-250">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-250">Solution</span></span>**  
<span data-ttu-id="dca64-251">Arrestare e riavviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="dca64-252">Inoltre, potrebbe essere necessario reinstallare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dca64-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="dca64-253">Reindirizzamento della stampante</span><span class="sxs-lookup"><span data-stu-id="dca64-253">Printer Redirection</span></span>

### <span data-ttu-id="dca64-254">ID evento 9001</span><span class="sxs-lookup"><span data-stu-id="dca64-254">Event ID 9001</span></span>

<span data-ttu-id="dca64-255">Errore di autorizzazione file.</span><span class="sxs-lookup"><span data-stu-id="dca64-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-256">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-256">Description</span></span>**  
<span data-ttu-id="dca64-257">L'utente finale non è autorizzato ad accedere alla cartella richiesta per aprire o creare il file della stampante MED-V per la lettura.</span><span class="sxs-lookup"><span data-stu-id="dca64-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-258">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-258">Solution</span></span>**  
<span data-ttu-id="dca64-259">Verificare che sia possibile accedere al percorso di User\\AppData\\ e che l'utente disponga delle autorizzazioni per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="dca64-260">Ad esempio, se l'utente è "Matt", il percorso C:\\Users\\Matt\\AppData\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="dca64-261">E se esiste, il percorso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="dca64-262">ID evento 9002</span><span class="sxs-lookup"><span data-stu-id="dca64-262">Event ID 9002</span></span>

<span data-ttu-id="dca64-263">Errore di autorizzazione file.</span><span class="sxs-lookup"><span data-stu-id="dca64-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-264">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-264">Description</span></span>**  
<span data-ttu-id="dca64-265">L'utente finale non è autorizzato ad accedere alla cartella richiesta per aprire o creare il file della stampante MED-V per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-266">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-266">Solution</span></span>**  
<span data-ttu-id="dca64-267">Verificare che sia possibile accedere al percorso di User\\AppData\\ e che l'utente disponga delle autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="dca64-268">Ad esempio, se l'utente è "Matt", il percorso C:\\Users\\Matt\\AppData\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="dca64-269">E se esiste, il percorso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="dca64-270">ID evento 9004</span><span class="sxs-lookup"><span data-stu-id="dca64-270">Event ID 9004</span></span>

<span data-ttu-id="dca64-271">Impossibile creare il percorso per l'archiviazione dei file della stampante MEDV.</span><span class="sxs-lookup"><span data-stu-id="dca64-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-272">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-272">Description</span></span>**  
<span data-ttu-id="dca64-273">Il servizio di reindirizzamento della stampante non può accedere ai file o creare directory necessarie per archiviare le informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="dca64-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-274">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-274">Solution</span></span>**  
<span data-ttu-id="dca64-275">Verificare che sia possibile accedere al percorso di User\\AppData\\ e che l'utente disponga delle autorizzazioni per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="dca64-276">Ad esempio, se l'utente è "Matt", il percorso C:\\Users\\Matt\\AppData\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="dca64-277">E se esiste, il percorso C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e tutti i file in essa contenuti devono avere le autorizzazioni di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="dca64-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="dca64-278">ID evento 9005</span><span class="sxs-lookup"><span data-stu-id="dca64-278">Event ID 9005</span></span>

<span data-ttu-id="dca64-279">Impossibile ottenere il nome VM dalla configurazione; non è possibile avviare il programma di installazione Guest.</span><span class="sxs-lookup"><span data-stu-id="dca64-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="dca64-280">Non è possibile aggiornare MED-V: non è stato rilevato alcun network host.</span><span class="sxs-lookup"><span data-stu-id="dca64-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-281">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-281">Description</span></span>**  
<span data-ttu-id="dca64-282">Il servizio di reindirizzamento della stampante non è stato in grado di ottenere il nome dell'area di lavoro MED-V dalla configurazione MED-V e non può informare Windows Virtual PC di avviare il programma di installazione nell'guest MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-283">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-283">Solution</span></span>**  
<span data-ttu-id="dca64-284">Assicurarsi che il nome dell'area di lavoro MED-V sia impostato e che corrisponda a un nome di macchina virtuale nella &lt; *user* &gt; directory dei computer \\Virtual utente di C:\\Users\\.</span><span class="sxs-lookup"><span data-stu-id="dca64-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="dca64-285">Il nome dell'area di lavoro MED-V si trova in HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="dca64-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="dca64-286">Ad esempio, se l'utente è "Matt" e il nome dell'area di lavoro è "mattsworkspace", il valore di HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve essere "mattsworkspace" e dovrebbe essere presente un file denominato C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="dca64-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="dca64-287">Pubblicazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="dca64-287">Application Publishing</span></span>

### <span data-ttu-id="dca64-288">ID evento 10015</span><span class="sxs-lookup"><span data-stu-id="dca64-288">Event ID 10015</span></span>

<span data-ttu-id="dca64-289">Si è verificato un errore di file System durante il processo di riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="dca64-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="dca64-290">Il processo di riconciliazione non elaborerà il &lt; *nome* del file &gt; , ma continuerà a elaborare qualsiasi altra modifica.</span><span class="sxs-lookup"><span data-stu-id="dca64-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-291">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-291">Description</span></span>**  
<span data-ttu-id="dca64-292">Si è verificato un errore di I/O di accesso non autorizzato quando è stato creato o eliminato un collegamento.</span><span class="sxs-lookup"><span data-stu-id="dca64-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-293">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-293">Solution</span></span>**  
<span data-ttu-id="dca64-294">Verificare che sia possibile accedere al percorso del file e che l'utente disponga delle autorizzazioni per creare o eliminare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="dca64-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="dca64-295">ID evento 10021</span><span class="sxs-lookup"><span data-stu-id="dca64-295">Event ID 10021</span></span>

<span data-ttu-id="dca64-296">&lt; *Errore di errore \ _information* &gt; per l'operazione operazione file &lt; *\ _name* &gt; il nome del file &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-297">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-297">Description</span></span>**  
<span data-ttu-id="dca64-298">Si è verificato un errore di I/O di accesso non autorizzato quando è stato creato o eliminato un collegamento.</span><span class="sxs-lookup"><span data-stu-id="dca64-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-299">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-299">Solution</span></span>**  
<span data-ttu-id="dca64-300">Verificare che sia possibile accedere al percorso del file e che l'utente disponga delle autorizzazioni per creare o eliminare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="dca64-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="dca64-301">Patch Guest</span><span class="sxs-lookup"><span data-stu-id="dca64-301">Guest Patching</span></span>

### <span data-ttu-id="dca64-302">ID evento 11001</span><span class="sxs-lookup"><span data-stu-id="dca64-302">Event ID 11001</span></span>

<span data-ttu-id="dca64-303">Messaggio di utilizzo delle attività di risveglio Guest.</span><span class="sxs-lookup"><span data-stu-id="dca64-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-304">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-304">Description</span></span>**  
<span data-ttu-id="dca64-305">MedvHost.exe con l'opzione/GuestWakeup è stata eseguita in modo non corretto oppure il comando è formattato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="dca64-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-306">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-306">Solution</span></span>**  
<span data-ttu-id="dca64-307">Verificare che il comando venga eseguito con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="dca64-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="dca64-308">Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *area di lavoro \ _name* &gt; " dove</span><span class="sxs-lookup"><span data-stu-id="dca64-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="dca64-309">&lt;*durata \ _in \ _minutes* &gt; è il numero di minuti che la macchina virtuale deve rimanere svegli (il valore predefinito è 240) e</span><span class="sxs-lookup"><span data-stu-id="dca64-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="dca64-310">&lt;*area di lavoro \ _name* &gt; è il nome della macchina virtuale che deve essere riattivata.</span><span class="sxs-lookup"><span data-stu-id="dca64-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="dca64-311">ID evento 11002</span><span class="sxs-lookup"><span data-stu-id="dca64-311">Event ID 11002</span></span>

<span data-ttu-id="dca64-312">Non è possibile aggiornare MED-V: non è stato rilevato alcun network host.</span><span class="sxs-lookup"><span data-stu-id="dca64-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-313">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-313">Description</span></span>**  
<span data-ttu-id="dca64-314">Non è stato possibile completare la patch Guest perché non è stata rilevata una connessione di rete host.</span><span class="sxs-lookup"><span data-stu-id="dca64-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-315">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-315">Solution</span></span>**  
<span data-ttu-id="dca64-316">Connettere l'host MED-V a una connessione di rete attiva prima di eseguire le patch Guest.</span><span class="sxs-lookup"><span data-stu-id="dca64-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="dca64-317">ID evento 11003</span><span class="sxs-lookup"><span data-stu-id="dca64-317">Event ID 11003</span></span>

<span data-ttu-id="dca64-318">Non è possibile aggiornare MED-V-host non in uso in un/C powerFailed per creare server pipe.</span><span class="sxs-lookup"><span data-stu-id="dca64-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-319">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-319">Description</span></span>**  
<span data-ttu-id="dca64-320">L'aggiornamento delle patch Guest non può essere completato perché l'host sembra essere in funzione a batteria invece che da un cavo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="dca64-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-321">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-321">Solution</span></span>**  
<span data-ttu-id="dca64-322">Connettere il computer host a un cavo di alimentazione prima di eseguire le patch Guest.</span><span class="sxs-lookup"><span data-stu-id="dca64-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="dca64-323">Client UX</span><span class="sxs-lookup"><span data-stu-id="dca64-323">Client UX</span></span>

### <span data-ttu-id="dca64-324">ID evento 14003</span><span class="sxs-lookup"><span data-stu-id="dca64-324">Event ID 14003</span></span>

<span data-ttu-id="dca64-325">Il messaggio di stato del vassoio seguente è stato troppo lungo e non è stato possibile visualizzarlo: &lt; *tray \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="dca64-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-326">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-326">Description</span></span>**  
<span data-ttu-id="dca64-327">In MED-V è stata creata una stringa non prevista troppo lunga per la descrizione comando vassoio o il messaggio Balloon.</span><span class="sxs-lookup"><span data-stu-id="dca64-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="dca64-328">Di conseguenza, il messaggio visualizzato è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="dca64-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-329">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-329">Solution</span></span>**  
<span data-ttu-id="dca64-330">Si tratta di un errore raro che può verificarsi quando MED-V crea in modo casuale il testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="dca64-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="dca64-331">Non esiste una soluzione.</span><span class="sxs-lookup"><span data-stu-id="dca64-331">There is no solution.</span></span>

### <span data-ttu-id="dca64-332">ID evento 14004</span><span class="sxs-lookup"><span data-stu-id="dca64-332">Event ID 14004</span></span>

<span data-ttu-id="dca64-333">MED-V è stato interrotto a causa di un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="dca64-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-334">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-334">Description</span></span>**  
<span data-ttu-id="dca64-335">Un'eccezione non gestita ha causato l'arresto imprevisto di MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-336">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-336">Solution</span></span>**  
<span data-ttu-id="dca64-337">Riavviare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-337">Restart MED-V.</span></span>

### <span data-ttu-id="dca64-338">ID evento 14005</span><span class="sxs-lookup"><span data-stu-id="dca64-338">Event ID 14005</span></span>

<span data-ttu-id="dca64-339">Il server ha tentato di creare mutex ma esiste già.</span><span class="sxs-lookup"><span data-stu-id="dca64-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-340">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-340">Description</span></span>**  
<span data-ttu-id="dca64-341">Una seconda istanza di MedvHost.exe è bloccata in memoria.</span><span class="sxs-lookup"><span data-stu-id="dca64-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-342">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-342">Solution</span></span>**  
<span data-ttu-id="dca64-343">Aprire TaskManager e terminare tutti i processi di MedvHost.exe.</span><span class="sxs-lookup"><span data-stu-id="dca64-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="dca64-344">ID evento 14006</span><span class="sxs-lookup"><span data-stu-id="dca64-344">Event ID 14006</span></span>

<span data-ttu-id="dca64-345">Errore durante la modifica o l'eliminazione del registro di valori del registro di sistema &lt; *_value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-346">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-346">Description</span></span>**  
<span data-ttu-id="dca64-347">MED-V non è in grado di modificare la voce specificata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dca64-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-348">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-348">Solution</span></span>**  
<span data-ttu-id="dca64-349">Assicurarsi di installare o disinstallare MED-V con credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="dca64-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="dca64-350">ID evento 14007</span><span class="sxs-lookup"><span data-stu-id="dca64-350">Event ID 14007</span></span>

<span data-ttu-id="dca64-351">Il file specificato ( &lt; *nomefile* &gt; ) non è valido.</span><span class="sxs-lookup"><span data-stu-id="dca64-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-352">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-352">Description</span></span>**  
<span data-ttu-id="dca64-353">Durante l'installazione o la disinstallazione, un file temporaneo danneggiato è stato passato all'host MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-354">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-354">Solution</span></span>**  
<span data-ttu-id="dca64-355">Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="dca64-356">ID evento 14008</span><span class="sxs-lookup"><span data-stu-id="dca64-356">Event ID 14008</span></span>

<span data-ttu-id="dca64-357">File non trovato: &lt; *nomefile* &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-358">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-358">Description</span></span>**  
<span data-ttu-id="dca64-359">Durante l'installazione o la disinstallazione, non è stato trovato un percorso di un file temporaneo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dca64-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-360">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-360">Solution</span></span>**  
<span data-ttu-id="dca64-361">Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="dca64-362">ID evento 14009</span><span class="sxs-lookup"><span data-stu-id="dca64-362">Event ID 14009</span></span>

<span data-ttu-id="dca64-363">Non è possibile leggere il nome del file del parametro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-364">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-364">Description</span></span>**  
<span data-ttu-id="dca64-365">Durante il processo di installazione o disinstallazione, MED-V non è in grado di leggere un file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="dca64-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-366">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-366">Solution</span></span>**  
<span data-ttu-id="dca64-367">Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="dca64-368">Verificare inoltre che l'utente disponga dei diritti e delle autorizzazioni necessarie per la cartella Temp.</span><span class="sxs-lookup"><span data-stu-id="dca64-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="dca64-369">ID evento 14010</span><span class="sxs-lookup"><span data-stu-id="dca64-369">Event ID 14010</span></span>

<span data-ttu-id="dca64-370">Errore di deserializzazione del file di parametro &lt; *nomefile* &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-371">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-371">Description</span></span>**  
<span data-ttu-id="dca64-372">Durante il processo di installazione o disinstallazione, MED-V ha rilevato un file temporaneo danneggiato.</span><span class="sxs-lookup"><span data-stu-id="dca64-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-373">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-373">Solution</span></span>**  
<span data-ttu-id="dca64-374">Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="dca64-375">Verificare inoltre che l'utente disponga dei diritti e delle autorizzazioni necessarie per la cartella Temp.</span><span class="sxs-lookup"><span data-stu-id="dca64-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="dca64-376">ID evento 14011</span><span class="sxs-lookup"><span data-stu-id="dca64-376">Event ID 14011</span></span>

<span data-ttu-id="dca64-377">Errore imprevisto che deserializza il nome del file del parametro &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-378">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-378">Description</span></span>**  
<span data-ttu-id="dca64-379">Durante il processo di installazione o disinstallazione, MED-V ha rilevato un file temporaneo danneggiato.</span><span class="sxs-lookup"><span data-stu-id="dca64-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-380">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-380">Solution</span></span>**  
<span data-ttu-id="dca64-381">Eliminare tutti i file nella cartella Temp e reinstallare o disinstallare MED-V.</span><span class="sxs-lookup"><span data-stu-id="dca64-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="dca64-382">Verificare inoltre che l'utente disponga dei diritti e delle autorizzazioni necessarie per la cartella Temp.</span><span class="sxs-lookup"><span data-stu-id="dca64-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="dca64-383">ID evento 14012</span><span class="sxs-lookup"><span data-stu-id="dca64-383">Event ID 14012</span></span>

<span data-ttu-id="dca64-384">Errore imprevisto quando i diritti delle impostazioni nella cartella cartella &lt; *\ _name* &gt; per il &lt; *nome*utente &gt; .</span><span class="sxs-lookup"><span data-stu-id="dca64-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-385">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-385">Description</span></span>**  
<span data-ttu-id="dca64-386">Si verifica un errore quando MED-V non è in grado di impostare diritti e autorizzazioni per determinate cartelle durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dca64-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-387">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-387">Solution</span></span>**  
<span data-ttu-id="dca64-388">Verificare i diritti di amministratore per le cartelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="dca64-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="dca64-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="dca64-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="dca64-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="dca64-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="dca64-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="dca64-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="dca64-392">ID evento 14013</span><span class="sxs-lookup"><span data-stu-id="dca64-392">Event ID 14013</span></span>

<span data-ttu-id="dca64-393">Errore imprevisto durante la creazione di file di blocco.</span><span class="sxs-lookup"><span data-stu-id="dca64-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="dca64-394">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca64-394">Description</span></span>**  
<span data-ttu-id="dca64-395">Si verifica un errore quando MED-V non è in grado di creare un file nella cartella @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dca64-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="dca64-396">Soluzione</span><span class="sxs-lookup"><span data-stu-id="dca64-396">Solution</span></span>**  
<span data-ttu-id="dca64-397">Controlla i diritti di amministratore per la cartella MedvLock.</span><span class="sxs-lookup"><span data-stu-id="dca64-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="dca64-398">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dca64-398">Related topics</span></span>


[<span data-ttu-id="dca64-399">Risoluzione dei problemi di MED-V</span><span class="sxs-lookup"><span data-stu-id="dca64-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





