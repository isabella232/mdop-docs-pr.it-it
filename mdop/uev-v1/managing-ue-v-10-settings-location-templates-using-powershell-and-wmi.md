---
title: Gestione dei modelli percorsi impostazioni UE-V 1.0 con PowerShell e WMI
description: Gestione dei modelli percorsi impostazioni UE-V 1.0 con PowerShell e WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804269"
---
# <span data-ttu-id="95aaa-103">Gestione dei modelli percorsi impostazioni UE-V 1.0 con PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="95aaa-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="95aaa-104">Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate dalla virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="95aaa-105">UE-V include un set di modelli di posizione standard per le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="95aaa-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="95aaa-106">Include anche lo strumento generatore di UE-V che consente di creare modelli di posizione delle impostazioni personalizzati.</span><span class="sxs-lookup"><span data-stu-id="95aaa-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="95aaa-107">Dopo aver creato e distribuito i modelli di posizione delle impostazioni, è possibile gestire questi modelli usando PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="95aaa-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="95aaa-108">Gestire i modelli di posizione delle impostazioni con WMI e PowerShell</span><span class="sxs-lookup"><span data-stu-id="95aaa-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="95aaa-109">Le funzionalità WMI e PowerShell di UE-V includono la possibilità di abilitare, disabilitare, registrare, aggiornare e annullare la registrazione dei modelli di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="95aaa-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="95aaa-110">Usando queste funzionalità, puoi automatizzare il processo di registrazione, aggiornamento o annullamento della registrazione dei modelli con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="95aaa-111">È anche possibile registrare manualmente i modelli usando i comandi WMI e PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95aaa-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="95aaa-112">Usando queste funzionalità in combinazione con una soluzione elettronica di distribuzione del software, criteri di gruppo o un altro metodo di distribuzione automatizzato, ad esempio uno script, puoi automatizzare ulteriormente questo processo.</span><span class="sxs-lookup"><span data-stu-id="95aaa-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="95aaa-113">Per aggiornare, registrare o annullare la registrazione di un modello di posizione delle impostazioni, è necessario disporre delle autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="95aaa-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="95aaa-114">Le autorizzazioni di amministratore non sono necessarie per abilitare o disabilitare i modelli.</span><span class="sxs-lookup"><span data-stu-id="95aaa-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="95aaa-115">Per gestire i modelli di posizione delle impostazioni con PowerShell</span><span class="sxs-lookup"><span data-stu-id="95aaa-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="95aaa-116">Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95aaa-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="95aaa-117">Per importare il modulo **Microsoft UE-V PowerShell** , digitare il comando seguente al prompt dei comandi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95aaa-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="95aaa-118">Usare i cmdlet di PowerShell seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="95aaa-119">Comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="95aaa-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="95aaa-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95aaa-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-121">Get-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-122">Elenca tutti i modelli di posizione delle impostazioni registrati nel computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-123">Registro-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-124">Registra un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="95aaa-125">Una volta registrato un modello, UE-V sincronizza le impostazioni definite nel modello tra i computer con il modello registrato.</span><span class="sxs-lookup"><span data-stu-id="95aaa-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-126">Annullamento della registrazione-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-127">Annulla la registrazione di un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="95aaa-128">Non appena viene annullata la registrazione di un modello, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-129">Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-130">Aggiorna un modello di posizione delle impostazioni con una versione più recente del modello.</span><span class="sxs-lookup"><span data-stu-id="95aaa-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="95aaa-131">Il nuovo modello deve avere una versione successiva rispetto a quella esistente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-132">Disable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-133">Disabilita un modello di posizione delle impostazioni per l'utente corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-134">Enable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-135">Abilita un modello di posizione delle impostazioni per l'utente corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-136">Test-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95aaa-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-137">Determina se un modello di posizione di impostazioni specifico è conforme al relativo schema XML.</span><span class="sxs-lookup"><span data-stu-id="95aaa-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="95aaa-138">Le funzionalità di PowerShell UE-V consentono di gestire un gruppo di modelli di impostazioni distribuiti nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="95aaa-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="95aaa-139">Per gestire un gruppo di modelli tramite PowerShell, eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="95aaa-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="95aaa-140">Per gestire un gruppo di modelli di posizione delle impostazioni con PowerShell</span><span class="sxs-lookup"><span data-stu-id="95aaa-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="95aaa-141">Modificare o aggiornare i modelli di posizione delle impostazioni desiderati.</span><span class="sxs-lookup"><span data-stu-id="95aaa-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="95aaa-142">Distribuire i modelli di posizione delle impostazioni desiderati in una cartella accessibile al computer locale.</span><span class="sxs-lookup"><span data-stu-id="95aaa-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="95aaa-143">Nel computer locale aprire una finestra di Windows PowerShell con i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="95aaa-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="95aaa-144">Importando il modulo Microsoft UE-V PowerShell, digitando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="95aaa-145">Annulla la registrazione di tutte le versioni precedentemente registrate dei modelli digitando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="95aaa-146">Verrà annullata la registrazione di tutti i modelli attivi nel computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="95aaa-147">Registrare i modelli aggiornati digitando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="95aaa-148">Verranno registrati tutti i modelli di posizione delle impostazioni presenti nella cartella modello specificata.</span><span class="sxs-lookup"><span data-stu-id="95aaa-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="95aaa-149">La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="95aaa-150">Gli amministratori possono usare queste interfacce per gestire i modelli di posizione delle impostazioni da Windows PowerShell e automatizzare le attività amministrative del modello.</span><span class="sxs-lookup"><span data-stu-id="95aaa-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="95aaa-151">Per gestire i modelli di posizione delle impostazioni con WMI</span><span class="sxs-lookup"><span data-stu-id="95aaa-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="95aaa-152">Usare un account con diritti di amministratore per aprire una finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95aaa-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="95aaa-153">Usare i comandi WMI seguenti per registrare e gestire i modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="95aaa-154">Comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="95aaa-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="95aaa-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95aaa-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-156">Get-WmiObject-spazio dei nomi root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, templateName, TemplateVersion, Enabled | Format-tabella-AutoSize</span><span class="sxs-lookup"><span data-stu-id="95aaa-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-157">Elenca tutti i modelli di posizione delle impostazioni registrati per il computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-158">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Register-percorso modello per gli argomenti &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="95aaa-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-159">Registra un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-160">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ID modello per gli argomenti &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="95aaa-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-161">Annulla la registrazione di un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="95aaa-162">Non appena viene annullata la registrazione di un modello, UE-V non Sincronizza più le impostazioni definite nel modello tra i computer.</span><span class="sxs-lookup"><span data-stu-id="95aaa-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-163">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ID modello per gli argomenti &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="95aaa-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-164">Abilita un modello di posizione delle impostazioni con UE-V</span><span class="sxs-lookup"><span data-stu-id="95aaa-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-165">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ID modello per gli argomenti &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="95aaa-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-166">Disabilita un modello di posizione delle impostazioni con UE-V</span><span class="sxs-lookup"><span data-stu-id="95aaa-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="95aaa-167">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update-percorso del &lt; modello arguments&gt;</span><span class="sxs-lookup"><span data-stu-id="95aaa-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-168">Aggiorna un modello di posizione delle impostazioni con UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="95aaa-169">Il nuovo modello deve avere una versione superiore a quella esistente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="95aaa-170">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-percorso del &lt; modello arguments&gt;</span><span class="sxs-lookup"><span data-stu-id="95aaa-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="95aaa-171">Determina se un modello di posizione di impostazioni specifico è conforme al relativo schema XML.</span><span class="sxs-lookup"><span data-stu-id="95aaa-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="95aaa-172">Come distribuire l'agente UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="95aaa-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="95aaa-173">Organizzare il file del programma di installazione di UE-V in una condivisione di rete accessibile.</span><span class="sxs-lookup"><span data-stu-id="95aaa-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="95aaa-174">**Nota**  USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="95aaa-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="95aaa-175">Le versioni dei file di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura.</span><span class="sxs-lookup"><span data-stu-id="95aaa-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="95aaa-176">Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.</span><span class="sxs-lookup"><span data-stu-id="95aaa-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="95aaa-177">Usare uno dei comandi di PowerShell seguenti per installare l'agente.</span><span class="sxs-lookup"><span data-stu-id="95aaa-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="95aaa-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95aaa-178">Related topics</span></span>


[<span data-ttu-id="95aaa-179">Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="95aaa-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="95aaa-180">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="95aaa-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="95aaa-181">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="95aaa-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





