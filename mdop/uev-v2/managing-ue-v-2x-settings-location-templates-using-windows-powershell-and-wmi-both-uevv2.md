---
title: Gestione dei modelli di posizione delle impostazioni di UE-V 2. x con Windows PowerShell e WMI
description: Gestione dei modelli di posizione delle impostazioni di UE-V 2. x con Windows PowerShell e WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804558"
---
# <span data-ttu-id="38753-103">Gestione dei modelli di posizione delle impostazioni di UE-V 2. x con Windows PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="38753-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="38753-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usano i modelli di posizione delle impostazioni XML per definire le impostazioni che l'utente ha acquisito e si applica alla virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="38753-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="38753-105">UE-V include un set di modelli di posizione standard per le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="38753-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="38753-106">Include anche lo strumento generatore di UE-V che consente di creare modelli di posizione delle impostazioni personalizzati.</span><span class="sxs-lookup"><span data-stu-id="38753-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="38753-107">Dopo aver creato e distribuito i modelli di posizione delle impostazioni, è possibile gestire questi modelli usando Windows PowerShell e Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="38753-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="38753-108">Per un elenco completo dei cmdlet di PowerShell di UE-V, Vedi informazioni di [riferimento sui cmdlet di UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="38753-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="38753-109">Gestire i modelli di posizione delle impostazioni di UE-V 2 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38753-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="38753-110">Le caratteristiche di WMI e Windows PowerShell di UE-V includono la possibilità di abilitare, disabilitare, registrare, aggiornare e annullare la registrazione dei modelli di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="38753-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="38753-111">Usando queste funzionalità, puoi automatizzare il processo di registrazione, aggiornamento o annullamento della registrazione dei modelli con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="38753-112">È anche possibile registrare manualmente i modelli usando i comandi WMI e Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38753-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="38753-113">Usando queste funzionalità in combinazione con una soluzione elettronica di distribuzione del software, criteri di gruppo o un altro metodo di distribuzione automatizzato, ad esempio uno script, puoi automatizzare ulteriormente questo processo.</span><span class="sxs-lookup"><span data-stu-id="38753-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="38753-114">Per aggiornare, registrare o annullare la registrazione di un modello di posizione delle impostazioni, è necessario disporre delle autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="38753-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="38753-115">Le autorizzazioni di amministratore non sono necessarie per abilitare, disabilitare o elencare i modelli.</span><span class="sxs-lookup"><span data-stu-id="38753-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="38753-116">Per gestire i modelli di posizione delle impostazioni tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38753-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="38753-117">Usare un account con diritti di amministratore per aprire un prompt dei comandi di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38753-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="38753-118">Usare i cmdlet di Windows PowerShell seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="38753-119">Comando di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38753-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="38753-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38753-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-121">Elenca tutti i modelli di posizione delle impostazioni registrati nel computer.</span><span class="sxs-lookup"><span data-stu-id="38753-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-122">Elenca tutti i modelli di posizione delle impostazioni registrati nel computer in cui il nome dell'applicazione o il nome del modello contiene una &lt; stringa &gt; .</span><span class="sxs-lookup"><span data-stu-id="38753-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-123">Elenca tutti i modelli di posizione delle impostazioni registrati nel computer in cui l'ID modello contiene una &lt; stringa &gt; .</span><span class="sxs-lookup"><span data-stu-id="38753-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-124">Elenca tutti i modelli di posizione delle impostazioni registrati nel computer in cui il nome dell'applicazione o del modello o l'ID modello contiene una &lt; stringa &gt; .</span><span class="sxs-lookup"><span data-stu-id="38753-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-125">Ottiene il nome delle informazioni sul programma e sulla versione, che dipendono dall'ID modello.</span><span class="sxs-lookup"><span data-stu-id="38753-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-126">Ottiene l'elenco effettivo delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="38753-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-127">Ottiene l'elenco delle app di Windows configurate per il computer.</span><span class="sxs-lookup"><span data-stu-id="38753-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-128">Ottiene l'elenco delle app di Windows configurate per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-129">Registra uno o più modelli di posizione delle impostazioni con UE-V usando percorsi relativi e/o caratteri jolly nei percorsi di file.</span><span class="sxs-lookup"><span data-stu-id="38753-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="38753-130">Dopo aver registrato un modello, l'UE-V sincronizza le impostazioni definite nel modello tra i computer con il modello registrato.</span><span class="sxs-lookup"><span data-stu-id="38753-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-131">Registra uno o più modelli di posizione delle impostazioni con UE-V usando i percorsi letterali, in cui nessun carattere può essere interpretato come caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="38753-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="38753-132">Dopo aver registrato un modello, l'UE-V sincronizza le impostazioni definite nel modello tra i computer con il modello registrato.</span><span class="sxs-lookup"><span data-stu-id="38753-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-133">Annulla la registrazione di un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="38753-134">Quando un modello non viene registrato, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</span><span class="sxs-lookup"><span data-stu-id="38753-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-135">Annulla la registrazione di tutti i modelli di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="38753-136">Quando un modello non viene registrato, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</span><span class="sxs-lookup"><span data-stu-id="38753-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-137">Aggiorna uno o più modelli di posizione delle impostazioni con una versione più recente del modello.</span><span class="sxs-lookup"><span data-stu-id="38753-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="38753-138">Usare percorsi relativi e/o caratteri jolly nei percorsi di file.</span><span class="sxs-lookup"><span data-stu-id="38753-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="38753-139">Il nuovo modello deve essere una versione più recente rispetto al modello esistente.</span><span class="sxs-lookup"><span data-stu-id="38753-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-140">Aggiorna uno o più modelli di posizione delle impostazioni con una versione più recente del modello.</span><span class="sxs-lookup"><span data-stu-id="38753-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="38753-141">Usare percorsi completi per i file modello, in cui nessun carattere può essere interpretato come caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="38753-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="38753-142">Il nuovo modello deve essere una versione più recente rispetto al modello esistente.</span><span class="sxs-lookup"><span data-stu-id="38753-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-143">Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-144">Rimuove l'app di Windows dall'elenco delle app di Windows utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-145">Rimuove tutte le app di Windows dall'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-146">Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-147">Rimuove tutte le app di Windows dall'elenco delle app di Windows utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-148">Disabilita un modello di posizione delle impostazioni per l'utente corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="38753-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-149">Disabilita una o più app di Windows nell'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-150">Disabilita una o più app di Windows nell'elenco app utente corrente di Windows.</span><span class="sxs-lookup"><span data-stu-id="38753-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-151">Abilita un modello di posizione delle impostazioni per l'utente corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="38753-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-152">Consente di abilitare una o più app di Windows nell'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-153">Consente di abilitare una o più app di Windows nell'elenco app utente corrente di Windows.</span><span class="sxs-lookup"><span data-stu-id="38753-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-154">Determina se uno o più modelli di posizione delle impostazioni sono conformi allo schema XML.</span><span class="sxs-lookup"><span data-stu-id="38753-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="38753-155">Può usare percorsi relativi e caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="38753-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-156">Determina se uno o più modelli di posizione delle impostazioni sono conformi allo schema XML.</span><span class="sxs-lookup"><span data-stu-id="38753-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="38753-157">Il percorso deve essere un percorso completo del file del modello, ma non include caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="38753-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="38753-158">Le funzionalità di Windows PowerShell UE-V consentono di gestire un gruppo di modelli di impostazioni distribuiti nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="38753-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="38753-159">Usare la procedura seguente per gestire un gruppo di modelli tramite Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38753-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="38753-160">Per gestire un gruppo di modelli di posizione delle impostazioni tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38753-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="38753-161">Modificare o aggiornare i modelli di posizione delle impostazioni desiderati.</span><span class="sxs-lookup"><span data-stu-id="38753-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="38753-162">Se si vogliono modificare o aggiornare i modelli di posizione delle impostazioni, distribuire i modelli di posizione delle impostazioni in una cartella accessibile al computer locale.</span><span class="sxs-lookup"><span data-stu-id="38753-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="38753-163">Nel computer locale aprire una finestra di Windows PowerShell con i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="38753-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="38753-164">Annulla la registrazione di tutte le versioni precedentemente registrate dei modelli digitando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="38753-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="38753-165">Questo comando Annulla la registrazione di tutti i modelli attivi nel computer.</span><span class="sxs-lookup"><span data-stu-id="38753-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="38753-166">Registrare i modelli aggiornati digitando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="38753-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="38753-167">Questo comando registra tutti i modelli di posizione delle impostazioni che si trovano nella cartella modello specificata.</span><span class="sxs-lookup"><span data-stu-id="38753-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="38753-168">Elenco delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="38753-168">Windows app list</span></span>

<span data-ttu-id="38753-169">Elencando un'app di Windows nell'elenco delle app di Windows, devi specificare se l'app è abilitata o disabilitata per la sincronizzazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="38753-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="38753-170">Le app sono identificate nell'elenco in base al nome della famiglia di pacchetti e se la sincronizzazione delle impostazioni deve essere abilitata o disabilitata per l'app.</span><span class="sxs-lookup"><span data-stu-id="38753-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="38753-171">Quando si usano queste impostazioni insieme all'impostazione predefinita per il comportamento di sincronizzazione non elencata, è possibile controllare se le app di Windows sono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="38753-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="38753-172">Per visualizzare il nome della famiglia di pacchetti delle app di Windows installate, in un prompt dei comandi di Windows PowerShell immettere:</span><span class="sxs-lookup"><span data-stu-id="38753-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="38753-173">Per visualizzare un elenco di app di Windows che possono sincronizzare le impostazioni in un computer con il nome della famiglia di pacchetti, lo stato abilitato e l'origine abilitata, al prompt dei comandi di Windows PowerShell immettere:</span><span class="sxs-lookup"><span data-stu-id="38753-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="38753-174">Definizioni delle proprietà Get-UevAppxPackage</span><span class="sxs-lookup"><span data-stu-id="38753-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="38753-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="38753-175">DisplayName</span></span>**  
<span data-ttu-id="38753-176">Nome visualizzato all'utente nell'applicazione centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="38753-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="38753-177">La `DisplayName` proprietà è derivata dalla `PackageFamilyName` Proprietà.</span><span class="sxs-lookup"><span data-stu-id="38753-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="38753-178">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="38753-178">PackageFamilyName</span></span>**  
<span data-ttu-id="38753-179">Nome del pacchetto installato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="38753-180">Abilitato</span><span class="sxs-lookup"><span data-stu-id="38753-180">Enabled</span></span>**  
<span data-ttu-id="38753-181">Definisce se le impostazioni per l'app sono configurate per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="38753-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="38753-182">EnabledSource</span><span class="sxs-lookup"><span data-stu-id="38753-182">EnabledSource</span></span>**  
<span data-ttu-id="38753-183">La posizione in cui viene impostata la configurazione che Abilita o Disabilita l'app.</span><span class="sxs-lookup"><span data-stu-id="38753-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="38753-184">I valori possibili sono: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*e *PolicyUser*.</span><span class="sxs-lookup"><span data-stu-id="38753-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="38753-185">NotSet</span><span class="sxs-lookup"><span data-stu-id="38753-185">NotSet</span></span>**  
<span data-ttu-id="38753-186">Il criterio non è configurato per sincronizzare l'app.</span><span class="sxs-lookup"><span data-stu-id="38753-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="38753-187">LocalMachine</span><span class="sxs-lookup"><span data-stu-id="38753-187">LocalMachine</span></span>**  
<span data-ttu-id="38753-188">Lo stato Enabled viene impostato nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="38753-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="38753-189">LocalUser</span><span class="sxs-lookup"><span data-stu-id="38753-189">LocalUser</span></span>**  
<span data-ttu-id="38753-190">Lo stato Enabled viene impostato nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="38753-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="38753-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="38753-191">PolicyMachine</span></span>**  
<span data-ttu-id="38753-192">Lo stato Enabled viene impostato nella sezione Policy della sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="38753-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="38753-193">Per ottenere l'elenco configurato dall'utente delle app di Windows, al prompt dei comandi di Windows PowerShell immetti:</span><span class="sxs-lookup"><span data-stu-id="38753-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="38753-194">Per ottenere l'elenco configurato dal computer delle app di Windows, al prompt dei comandi di Windows PowerShell immetti:</span><span class="sxs-lookup"><span data-stu-id="38753-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="38753-195">Per i parametri, CurrentComputerUser o computer, il cmdlet restituisce un elenco delle app di Windows configurate dall'utente o a livello di computer.</span><span class="sxs-lookup"><span data-stu-id="38753-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="38753-196">Definizioni delle proprietà</span><span class="sxs-lookup"><span data-stu-id="38753-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="38753-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="38753-197">DisplayName</span></span>**  
<span data-ttu-id="38753-198">Nome visualizzato all'utente nell'applicazione centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="38753-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="38753-199">La `DisplayName` proprietà è derivata dalla `PackageFamilyName` Proprietà.</span><span class="sxs-lookup"><span data-stu-id="38753-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="38753-200">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="38753-200">PackageFamilyName</span></span>**  
<span data-ttu-id="38753-201">Nome del pacchetto installato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="38753-202">Abilitato</span><span class="sxs-lookup"><span data-stu-id="38753-202">Enabled</span></span>**  
<span data-ttu-id="38753-203">Definisce se le impostazioni per l'app sono configurate per la sincronizzazione per l'opzione specificata, ovvero l' **utente** o il **computer**.</span><span class="sxs-lookup"><span data-stu-id="38753-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="38753-204">Installato</span><span class="sxs-lookup"><span data-stu-id="38753-204">Installed</span></span>**  
<span data-ttu-id="38753-205">True se l'app, ovvero PackageFamilyName, è installata per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="38753-206">Gestire i modelli di posizione delle impostazioni di UE-V 2 tramite WMI</span><span class="sxs-lookup"><span data-stu-id="38753-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="38753-207">La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente.</span><span class="sxs-lookup"><span data-stu-id="38753-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="38753-208">Gli amministratori possono usare queste interfacce per gestire i modelli di posizione delle impostazioni da Windows PowerShell e automatizzare le attività amministrative del modello.</span><span class="sxs-lookup"><span data-stu-id="38753-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="38753-209">Per gestire i modelli di posizione delle impostazioni tramite WMI</span><span class="sxs-lookup"><span data-stu-id="38753-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="38753-210">Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38753-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="38753-211">Usare i comandi WMI seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="38753-212">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38753-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-213">Elenca tutti i modelli di posizione delle impostazioni registrati per il computer.</span><span class="sxs-lookup"><span data-stu-id="38753-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-214">Ottiene il nome delle informazioni sul programma e sulla versione, che dipendono dal nome del modello.</span><span class="sxs-lookup"><span data-stu-id="38753-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-215">Ottiene l'elenco effettivo delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="38753-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="38753-216">Get-WmiObject-spazio dei nomi root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="38753-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="38753-217">Ottiene l'elenco delle app di Windows configurate per il computer.</span><span class="sxs-lookup"><span data-stu-id="38753-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-218">Ottiene l'elenco delle app di Windows configurate per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-219">Registra un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-220">Annulla la registrazione di un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="38753-221">Non appena viene annullata la registrazione di un modello, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</span><span class="sxs-lookup"><span data-stu-id="38753-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-222">Aggiorna un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="38753-223">Il nuovo modello deve essere una versione più recente rispetto a quella esistente.</span><span class="sxs-lookup"><span data-stu-id="38753-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-224">Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-225">Consente di rimuovere una o più app di Windows dall'elenco delle app di Windows utente corrente.</span><span class="sxs-lookup"><span data-stu-id="38753-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-226">Disabilita uno o più modelli di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-227">Disabilita una o più app di Windows nell'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-228">Disabilita una o più app di Windows nell'elenco app utente corrente di Windows.</span><span class="sxs-lookup"><span data-stu-id="38753-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-229">Abilita un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-230">Abilita le app di Windows nell'elenco delle app di Windows per computer.</span><span class="sxs-lookup"><span data-stu-id="38753-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-231">Abilita le app di Windows nell'elenco app utente corrente di Windows.</span><span class="sxs-lookup"><span data-stu-id="38753-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="38753-232">Determina se un modello di posizione di impostazioni specifico è conforme al relativo schema XML.</span><span class="sxs-lookup"><span data-stu-id="38753-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="38753-233">Distribuzione dell'agente UE-V con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38753-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="38753-234">Come distribuire l'agente UE-V tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="38753-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="38753-235">Organizzare il pacchetto di installazione dell'agente UE-V in una condivisione di rete accessibile.</span><span class="sxs-lookup"><span data-stu-id="38753-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="38753-236">Nota</span><span class="sxs-lookup"><span data-stu-id="38753-236">Note</span></span>**  
    <span data-ttu-id="38753-237">USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="38753-238">I pacchetti di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura.</span><span class="sxs-lookup"><span data-stu-id="38753-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="38753-239">Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.</span><span class="sxs-lookup"><span data-stu-id="38753-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="38753-240">Usare uno dei comandi di Windows PowerShell seguenti per installare l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="38753-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="38753-241">**Hai un suggerimento per l'UE-V**?</span><span class="sxs-lookup"><span data-stu-id="38753-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="38753-242">Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="38753-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="38753-243">**È stato ottenuto un problema UE-V**?</span><span class="sxs-lookup"><span data-stu-id="38753-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="38753-244">Utilizzare il [forum TechNet di UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="38753-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="38753-245">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38753-245">Related topics</span></span>


[<span data-ttu-id="38753-246">Amministrazione di UE-V 2. x con Windows PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="38753-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="38753-247">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="38753-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









