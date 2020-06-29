---
title: Gestione delle impostazioni di configurazione dell'area di lavoro MED-V
description: Gestione delle impostazioni di configurazione dell'area di lavoro MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826156"
---
# <span data-ttu-id="f0ebf-103">Gestione delle impostazioni di configurazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ebf-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="f0ebf-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 archivia le impostazioni di configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="f0ebf-105">Le informazioni che includiamo qui per il registro di sistema possono aiutare a gestire meglio i servizi MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="f0ebf-106">MED-V usa il percorso di ricerca seguente quando si cercano i valori di impostazioni risultante:</span><span class="sxs-lookup"><span data-stu-id="f0ebf-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="f0ebf-107">MED-V analizza prima di tutto i criteri del computer.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="f0ebf-108">Se il valore non viene trovato, MED-V analizza il criterio utente.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="f0ebf-109">Se il valore non viene trovato, MED-V cerca nell'hive HKEY \ _LOCAL \ _MACHINE \\System.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="f0ebf-110">Se il valore non viene trovato, MED-V cerca nell'hive del registro di sistema HKEY \ _CURRENT utente.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="f0ebf-111">Se il valore non viene ancora trovato, MED-V utilizzerà l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="f0ebf-112">Una procedura consigliata generale consiste nell'impostare il valore nell'hive HKEY \ _LOCAL \ _MACHINE \\System o nei criteri del computer.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="f0ebf-113">Ma se si vuole che l'utente finale possa configurare una determinata impostazione, è consigliabile lasciarla fuori.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="f0ebf-114">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ebf-114">Note</span></span>**  
<span data-ttu-id="f0ebf-115">Prima di distribuire le aree di lavoro MED-V, è possibile usare un editor di script per modificare lo script di Windows PowerShell (file con estensione ps1) creato dal Packager dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="f0ebf-116">Per altre informazioni, vedere [configurazione delle impostazioni avanzate tramite Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="f0ebf-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="f0ebf-117">Dopo aver distribuito le aree di lavoro MED-V, è possibile modificare alcune impostazioni di configurazione di MED-V modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="f0ebf-118">Questa sezione elenca tutte le chiavi del registro di sistema MED-V configurabili e spiega i loro usi.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="f0ebf-119">Tasto di diagnostica</span><span class="sxs-lookup"><span data-stu-id="f0ebf-119">Diagnostics Key</span></span>


<span data-ttu-id="f0ebf-120">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ebf-121">Nome</span><span class="sxs-lookup"><span data-stu-id="f0ebf-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="f0ebf-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ebf-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="f0ebf-123">Dati/impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f0ebf-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="f0ebf-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ebf-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="f0ebf-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-127">Impostazione predefinita = 3</span><span class="sxs-lookup"><span data-stu-id="f0ebf-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-128">Tipo di informazioni registrate nel log eventi.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="f0ebf-129">I livelli includono i seguenti: 0 (nessuno), 1 (errore), 2 (avviso), 3 (informazioni), 4 (debug).</span><span class="sxs-lookup"><span data-stu-id="f0ebf-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f0ebf-130">Tasto FTS</span><span class="sxs-lookup"><span data-stu-id="f0ebf-130">Fts Key</span></span>


<span data-ttu-id="f0ebf-131">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ebf-132">Nome</span><span class="sxs-lookup"><span data-stu-id="f0ebf-132">Name</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ebf-133">Type</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-134">Dati/impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f0ebf-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ebf-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-138">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-139">Configura se la configurazione per la prima volta aggiunge automaticamente l'utente finale al gruppo amministratore&#39;s.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="f0ebf-140">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-141">0 = false: la prima volta che la configurazione non aggiunge automaticamente l'utente finale al gruppo amministratore&#39;s.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-142">1 = vero: la configurazione iniziale aggiunge automaticamente l'utente finale al gruppo Administrator&#39;s.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="f0ebf-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-144">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-145">MEDV</span><span class="sxs-lookup"><span data-stu-id="f0ebf-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-146">Maschera nome computer usata per creare la macchina virtuale Guest&#39;il nome del computer s.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-147">La maschera può contenere un tag% nomeutente% per inserire il nome utente come parte del computer.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="f0ebf-148">Analogamente, il tag% hostname% inserisce il nome del computer host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="f0ebf-149">Ogni &quot; # &quot; carattere della maschera viene sostituito da una cifra casuale.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="f0ebf-150">Un carattere asterisco (\*) alla fine della maschera viene sostituito da caratteri alfanumerici casuali.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="f0ebf-151">Un numero specifico di caratteri da% hostname% e% nomeutente% può essere acquisito usando parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="f0ebf-152">Ad esempio, &quot; % nomeutente% [3] &quot; utilizzerebbe i primi tre caratteri del nome utente.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-155">Impostazione predefinita = 90</span><span class="sxs-lookup"><span data-stu-id="f0ebf-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-156">Valore di timeout, in secondi, quando la configurazione per la prima volta prova ad eliminare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="f0ebf-157">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-160">Impostazione predefinita = 120</span><span class="sxs-lookup"><span data-stu-id="f0ebf-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-161">Valore di timeout, in secondi, quando la configurazione per la prima volta prova a scollegare il disco floppy virtuale dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="f0ebf-162">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="f0ebf-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-164">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-165">URL personalizzabile che si collega alla pagina Web interna e viene visualizzato dai messaggi di dialogo configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-168">Impostazione predefinita = 900</span><span class="sxs-lookup"><span data-stu-id="f0ebf-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-169">Il valore di timeout, in secondi, che attende l'installazione per la prima volta per Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="f0ebf-170">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="f0ebf-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-173">Il messaggio si trova nel file di risorse</span><span class="sxs-lookup"><span data-stu-id="f0ebf-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-174">Messaggio personalizzabile visualizzato all'utente finale quando non è possibile completare la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="f0ebf-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-177">Impostazione predefinita = 3</span><span class="sxs-lookup"><span data-stu-id="f0ebf-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-178">Numero massimo di volte in cui MED-V cerca di assegnare diritti a un gruppo di utenti finali.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="f0ebf-179">Il superamento del valore di tentativo specificato senza la possibilità di assegnare correttamente i diritti di un gruppo di utenti finali causa probabilmente un errore di preparazione della macchina virtuale che viene quindi soggetto al valore MaxRetryCount.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="f0ebf-180">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-183">Impostazione predefinita = 300</span><span class="sxs-lookup"><span data-stu-id="f0ebf-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-184">Valore di timeout, in secondi, quando si assegnano i diritti di un gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="f0ebf-185">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="f0ebf-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-188">Elenco dei percorsi di file di log raccolti da MED-V durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="f0ebf-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-191">Impostazione predefinita = 120</span><span class="sxs-lookup"><span data-stu-id="f0ebf-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-192">Il numero massimo di ore per cui la configurazione per la prima volta può essere rinviata dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="f0ebf-193">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="f0ebf-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-196">Impostazione predefinita = 3</span><span class="sxs-lookup"><span data-stu-id="f0ebf-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-197">Numero massimo di tentativi di preparazione di una macchina virtuale da parte di MED-V se ogni tentativo termina in un errore diverso da quello di un software.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="f0ebf-198">Quando la preparazione della macchina virtuale non riesce e viene superato il numero di tentativi di configurazione per la prima volta, MED-V informa l'utente finale dell'errore e non dà l'opzione di riprovare.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="f0ebf-199">Il conteggio viene reimpostato ogni volta che viene avviato MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="f0ebf-200">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-201">Modalità</span><span class="sxs-lookup"><span data-stu-id="f0ebf-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-202">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-203">Impostazione predefinita = automatica</span><span class="sxs-lookup"><span data-stu-id="f0ebf-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-204">Configura il modo in cui la configurazione per la prima volta interagisce con l'utente.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="f0ebf-205">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0ebf-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-206">Partecipato.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-206">Attended.</span></span></strong> <span data-ttu-id="f0ebf-207">L'utente finale deve immettere le informazioni durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ebf-208">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ebf-208">Note</span></span></strong><br/><p><span data-ttu-id="f0ebf-209">Se è stato creato il file Sysprep. inf in modo che la configurazione minima richiedesse l'input dell'utente per il completamento, è necessario selezionare la <strong> modalità assistita </strong> o potrebbero verificarsi problemi durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-210">Automatica </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-210">Unattended</strong>.</span></span> <span data-ttu-id="f0ebf-211">La macchina virtuale non viene visualizzata all'utente finale durante la configurazione per la prima volta, ma l'utente finale viene richiesto prima dell'avvio della configurazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-212">Silent </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-212">Silent</strong>.</span></span> <span data-ttu-id="f0ebf-213">La macchina virtuale non viene visualizzata all'utente finale durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="f0ebf-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-216">Impostazione predefinita = 15</span><span class="sxs-lookup"><span data-stu-id="f0ebf-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-217">Il valore di timeout, in minuti, per la prima volta che la configurazione deve essere completata nella prima configurazione in modalità interattiva durante il tentativo di eseguire nuovamente la configurazione.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="f0ebf-218">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-221">Impostazione predefinita = 45</span><span class="sxs-lookup"><span data-stu-id="f0ebf-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-222">Il valore di timeout, in minuti, che la prima configurazione deve essere completata nella prima configurazione della modalità interattiva per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="f0ebf-223">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="f0ebf-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-225">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-226">Data e ora, in formato DateTime UTC, che la configurazione per la prima volta può essere rinviata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="f0ebf-227">Immettere il formato &quot; aaaa-mm-dd HH: mm &quot; con le ore specificate usando lo standard dell'orologio a 24 ore.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="f0ebf-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-230">Il messaggio si trova nel file di risorse</span><span class="sxs-lookup"><span data-stu-id="f0ebf-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-231">Messaggio personalizzabile visualizzato all'utente finale quando la configurazione per la prima volta deve ripetere il tentativo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-234">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-235">Configura se la voce nomecomputer nella sezione [UserData] del file Sysprep. inf nel guest deve essere aggiornata in base al valore di ComputerNameMask specificato.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="f0ebf-236">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-237">0 = false: la voce nomecomputer nel file Sysprep. inf non viene aggiornata in base a ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-238">1 = true: la voce nomecomputer nel file Sysprep. inf viene aggiornata in base a ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-241">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-242">Configura se l'impostazione JoinDomain nella sezione [Identification] del file Sysprep. inf nel guest deve essere aggiornata in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="f0ebf-243">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-244">0 = false: l'impostazione JoinDomain nel file Sysprep. inf non viene aggiornata in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-245">1 = true: l'impostazione JoinDomain nel file Sysprep. inf viene aggiornata in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-248">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-249">Configura se l'impostazione MachineObjectOU nella sezione [Identification] del file Sysprep. inf nel guest viene aggiornata in base all'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="f0ebf-250">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-251">0 = false: l'impostazione MachineObjectOU nel file Sysprep. inf non viene aggiornata in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-252">1 = true: l'impostazione MachineObjectOU nel file Sysprep. inf viene aggiornata in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-253">SetRegionalSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-255">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-256">Configura se le impostazioni nella sezione [RegionalSettings] del file Sysprep. inf nel guest vengono aggiornate in base all'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="f0ebf-257">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ebf-258">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ebf-258">Note</span></span></strong><br/><p><span data-ttu-id="f0ebf-259">Per impostazione predefinita, l'impostazione per il fuso orario nel Guest è sempre sincronizzata con l'impostazione TimeZone nell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-260">0 = false: le impostazioni nella sezione [RegionalSettings] del file Sysprep. inf nel guest non vengono aggiornate in base all'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-261">1 = true: le impostazioni nella sezione [RegionalSettings] del file Sysprep. inf nel guest vengono aggiornate in base all'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-264">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-265">Configura se le impostazioni FullName e OrgName nella sezione [UserData] del file Sysprep. inf nel guest vengono aggiornate in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="f0ebf-266">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-267">0 = false: le impostazioni FullName e OrgName nel file Sysprep. inf non vengono aggiornate in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-268">1 = true: le impostazioni FullName e OrgName nel file Sysprep. inf vengono aggiornate in base alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="f0ebf-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-271">Il messaggio si trova nel file di risorse</span><span class="sxs-lookup"><span data-stu-id="f0ebf-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-272">Messaggio personalizzabile visualizzato all'utente finale quando la configurazione per la prima volta è pronta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-275">Impostazione predefinita = 30</span><span class="sxs-lookup"><span data-stu-id="f0ebf-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-276">Il valore di timeout, in secondi, che la configurazione per la prima volta attende una risposta dalla macchina virtuale per un'operazione di annullamento.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="f0ebf-277">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-280">Impostazione predefinita = 60</span><span class="sxs-lookup"><span data-stu-id="f0ebf-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-281">Il valore di timeout, in secondi, che la prima volta che viene eseguita la configurazione della macchina virtuale si arresta.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="f0ebf-282">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-285">Impostazione predefinita = 600</span><span class="sxs-lookup"><span data-stu-id="f0ebf-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-286">L'ora, in secondi, prima che venga tentato l'aggiornamento del software agente guest MED-V. Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f0ebf-287">Tasto UserExperience</span><span class="sxs-lookup"><span data-stu-id="f0ebf-287">UserExperience Key</span></span>


<span data-ttu-id="f0ebf-288">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience e alla chiave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ebf-289">Nome</span><span class="sxs-lookup"><span data-stu-id="f0ebf-289">Name</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ebf-290">Type</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-291">Dati/impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f0ebf-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-292">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ebf-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-295">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-296">Configura se la pubblicazione dell'applicazione dall'ospite all'host è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="f0ebf-297">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-298">0 = false: Disabilita la pubblicazione dell'applicazione dall'ospite all'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-299">1 = true: consente la pubblicazione dell'applicazione dall'ospite all'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-302">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-303">Configura se la condivisione del dispositivo di I/O audio tra il Guest e l'host è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="f0ebf-304">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-305">0 = false: Disabilita la condivisione del dispositivo di I/O audio tra Guest e host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-306">1 = true: consente la condivisione del dispositivo i/O audio tra l'ospite e l'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-309">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-310">Configura se la condivisione degli Appunti tra l'ospite e l'host è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="f0ebf-311">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-312">0 = false: Disabilita la condivisione degli Appunti tra l'ospite e l'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-313">1 = true: consente la condivisione degli Appunti tra l'ospite e l'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-316">Impostazione predefinita = 300</span><span class="sxs-lookup"><span data-stu-id="f0ebf-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-317">L'ora, in secondi, prima della data di inizio della prima configurazione di avvio della finestra di dialogo. Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-318">HideVmTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-320">Impostazione predefinita = 30</span><span class="sxs-lookup"><span data-stu-id="f0ebf-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-321">Valore di timeout, in minuti, che la finestra della macchina virtuale a schermo intero è nascosta dall'utente finale durante un tentativo di accesso lungo.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-324">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-325">Configura se il guest deve essere avviato quando l'utente finale accede al desktop o quando viene avviata la prima applicazione Guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="f0ebf-326">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-327">0 = false: il Guest viene avviato quando viene avviata la prima applicazione Guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-328">1 = vero: l'ospite viene avviato quando l'utente finale accede al desktop.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-331">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-332">Configura se la condivisione delle stampanti tra Guest e host è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="f0ebf-333">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-334">0 = false: disattiva la condivisione delle stampanti tra Guest e host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-335">1 = true: consente la condivisione di stampanti tra Guest e host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-338">Impostazione predefinita = 1440</span><span class="sxs-lookup"><span data-stu-id="f0ebf-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-339">Valore di timeout, in minuti, che la prima volta che l'installazione attende un riavvio.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="f0ebf-340">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="f0ebf-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-343">Elenco URL specificato</span><span class="sxs-lookup"><span data-stu-id="f0ebf-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-344">Specifica un elenco di URL da reindirizzare dall'host al Guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-345">SmartCardLogonEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-347">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-348">Configura se le smart card possono essere usate per autenticare gli utenti in MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="f0ebf-349">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-350">0 = false: non consente alle smart card di eseguire l'autenticazione degli utenti finali in MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-351">1 = vero: consente alle smart card di autenticare gli utenti finali in MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ebf-352">Importante</span><span class="sxs-lookup"><span data-stu-id="f0ebf-352">Important</span></span></strong><br/><p><span data-ttu-id="f0ebf-353">Se SmartCardLogonEnabled e CredentialCacheEnabled sono entrambi abilitati, SmartCardLogonEnabled esegue l'override di CredentialCacheEnabled.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-356">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-357">Configura se la condivisione delle smart card tra l'ospite e l'host è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="f0ebf-358">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-359">0 = false: Disabilita la condivisione delle smart card tra il Guest e l'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-360">1 = true: consente la condivisione di smart card tra l'ospite e l'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-363">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-364">Configura se è abilitata la condivisione di dispositivi USB tra Guest e host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="f0ebf-365">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-366">0 = false: disattiva la condivisione dei dispositivi USB tra Guest e host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-367">1 = true: consente la condivisione di dispositivi USB tra Guest e host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f0ebf-368">Chiave VM</span><span class="sxs-lookup"><span data-stu-id="f0ebf-368">VM Key</span></span>


<span data-ttu-id="f0ebf-369">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM e alla chiave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ebf-370">Nome</span><span class="sxs-lookup"><span data-stu-id="f0ebf-370">Name</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-371">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ebf-371">Type</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-372">Dati/impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f0ebf-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="f0ebf-373">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ebf-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-374">CloseAction</span><span class="sxs-lookup"><span data-stu-id="f0ebf-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-375">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-376">Impostazione predefinita = Hibernate</span><span class="sxs-lookup"><span data-stu-id="f0ebf-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-377">L'azione eseguita dalla macchina virtuale dopo l'ultima applicazione in esecuzione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="f0ebf-378">Questa impostazione viene ignorata se il valore di LogonStartEnabled è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="f0ebf-379">Le opzioni possibili sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0ebf-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-380">Hibernate </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="f0ebf-381">Questa opzione rilascia tutte le risorse fisiche che la macchina virtuale USA, ad esempio memoria e CPU, e salva lo stato di tutte le applicazioni e le operazioni in uso.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-382">ARRESTO </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="f0ebf-383">Questa opzione arresta in modo sicuro il sistema operativo guest e rilascia tutte le risorse fisiche che la macchina virtuale USA, ad esempio memoria e CPU.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-384">disattivazione </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="f0ebf-385">Questa opzione può causare la perdita di dati perché è la stessa cosa di disattivare il pulsante di alimentazione o estrarre il cavo di alimentazione in un computer fisico.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="f0ebf-386">Usare questa opzione solo se non è possibile usare una delle altre due opzioni.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="f0ebf-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="f0ebf-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-390">Un elenco di valori di memoria (MB) per l'ospite.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="f0ebf-391">Questo valore viene usato per determinare la quantità di RAM disponibile per l'ospite.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="f0ebf-392">In combinazione con HostMemToGuestMem, viene creata una tabella di ricerca per determinare la quantità di RAM da allocare nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="f0ebf-393">I valori possibili possono essere compresi tra 128 e 3712.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="f0ebf-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-396">Impostazione predefinita = 240</span><span class="sxs-lookup"><span data-stu-id="f0ebf-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-397">Numero di minuti che MED-V deve mantenere l'ospite sveglio per l'aggiornamento automatico, a partire dall'ora specificata nel valore GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="f0ebf-398">Intervallo compreso tra 0 e 1440.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-398">Range = 0 to 1440.</span></span> <span data-ttu-id="f0ebf-399">L'impostazione di questo valore su zero (0) Disabilita la funzionalità di patch Guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="f0ebf-400">Per altre informazioni sulle patch Guest per l'aggiornamento automatico, vedere <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestione degli aggiornamenti automatici per le aree di lavoro MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="f0ebf-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-402">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-403">Impostazione predefinita = 00:00</span><span class="sxs-lookup"><span data-stu-id="f0ebf-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-404">L'ora e il minuto ogni giorno in cui MED-V deve riattivare l'ospite per l'aggiornamento automatico, usando lo standard di 24 ore.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="f0ebf-405">Specificare l'ora nel formato HH: MM</span><span class="sxs-lookup"><span data-stu-id="f0ebf-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="f0ebf-406">Per altre informazioni sulle patch Guest per l'aggiornamento automatico, vedere <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestione degli aggiornamenti automatici per le aree di lavoro MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="f0ebf-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="f0ebf-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-410">Un elenco di valori di memoria (MB) per il Guest, determinato dalla RAM disponibile nell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="f0ebf-411">In combinazione con GuestMemFromHostMem, viene creata una tabella di ricerca per determinare la quantità di RAM da allocare nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="f0ebf-412">I valori possibili possono essere compresi tra 1024 e 16384.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-415">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-416">Configura se la memoria allocata per il Guest viene calcolata dalla memoria presente nell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="f0ebf-417">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-418">0 = false: la memoria allocata per il Guest non viene calcolata dalla memoria presente nell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-419">1 = vero: la memoria allocata per il Guest viene calcolata dalla memoria presente nell'host.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-420">Memoria</span><span class="sxs-lookup"><span data-stu-id="f0ebf-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-422">Impostazione predefinita = 512</span><span class="sxs-lookup"><span data-stu-id="f0ebf-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-423">RAM (MB) che deve essere allocata per la macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="f0ebf-424">Questa impostazione viene ignorata se l'impostazione HostMemToGuestMemEnabled è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="f0ebf-425">Intervallo = 128 a 2048.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="f0ebf-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-428">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="f0ebf-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-429">Configura se più utenti condividono la stessa area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="f0ebf-430">0 = false; 1 = vero.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-431">0 = false: più utenti non condividono la stessa area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-432">1 = true: più utenti condividono la stessa area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ebf-433">NetworkingMode</span><span class="sxs-lookup"><span data-stu-id="f0ebf-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-434">SZ</span><span class="sxs-lookup"><span data-stu-id="f0ebf-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-435">Impostazione predefinita = NAT</span><span class="sxs-lookup"><span data-stu-id="f0ebf-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-436">Tipo di connessione di rete usata nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="f0ebf-437">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0ebf-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-438">Bridged </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-438">Bridged</strong>.</span></span> <span data-ttu-id="f0ebf-439">MED-V ha un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="f0ebf-440">NAT </strong> .</span><span class="sxs-lookup"><span data-stu-id="f0ebf-440">NAT</strong>.</span></span> <span data-ttu-id="f0ebf-441">MED-V USA NAT (Network Address Translation) per condividere il IP dell'host&#39;s per il traffico in uscita.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="f0ebf-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-444">Impostazione predefinita = 600</span><span class="sxs-lookup"><span data-stu-id="f0ebf-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-445">Un valore di timeout generale, in secondi, in cui MED-V attende che un'attività venga completata, ad esempio il riavvio e la chiusura.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="f0ebf-446">Intervallo compreso tra 0 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f0ebf-447">Impostazioni del registro di sistema Guest</span><span class="sxs-lookup"><span data-stu-id="f0ebf-447">Guest Registry Settings</span></span>


<span data-ttu-id="f0ebf-448">Questa sezione elenca le chiavi del registro di sistema guest MED-V configurabili e spiega i loro usi.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="f0ebf-449">V2</span><span class="sxs-lookup"><span data-stu-id="f0ebf-449">v2</span></span>

<span data-ttu-id="f0ebf-450">La tabella seguente contiene informazioni sul valore del registro di sistema guest associato alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ebf-451">Nome</span><span class="sxs-lookup"><span data-stu-id="f0ebf-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="f0ebf-452">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ebf-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="f0ebf-453">Dati/impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="f0ebf-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="f0ebf-454">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ebf-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ebf-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="f0ebf-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="f0ebf-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-457">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="f0ebf-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="f0ebf-458">Configura il modo in cui MED-V gestisce le chiavi BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f0ebf-459">Per impostazione predefinita, MED-V imposta questi tasti come segue:</span><span class="sxs-lookup"><span data-stu-id="f0ebf-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="f0ebf-460">BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="f0ebf-461">Creare la chiave EnableGPWorkarounds, se necessario, e impostare la chiave su zero se non si vuole che MED-V modifichi le impostazioni predefinite di BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ebf-462">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ebf-462">Note</span></span></strong><br/><p><span data-ttu-id="f0ebf-463">Se l'area di lavoro MED-V è in uso in modalità NAT, EnableGPWorkarounds influisce sulle chiavi del registro di sistema BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="f0ebf-464">Se l'area di lavoro MED-V è in modalità BRIDGEd, EnableGPWorkarounds interessa solo la chiave del registro di sistema BufferPolicyReads.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="f0ebf-465">1 = vero: MED-V imposta le chiavi BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0 (se in uso in modalità NAT) o solo BufferPolicyReads = 1 (se in modalità BRIDGEd).</span><span class="sxs-lookup"><span data-stu-id="f0ebf-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="f0ebf-466">0 = false: MED-V non apporta alcuna modifica alle chiavi BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="f0ebf-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f0ebf-467">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0ebf-467">Related topics</span></span>


[<span data-ttu-id="f0ebf-468">Gestire le applicazioni nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ebf-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="f0ebf-469">Gestire il reindirizzamento URL in MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ebf-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="f0ebf-470">Gestire le impostazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ebf-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









