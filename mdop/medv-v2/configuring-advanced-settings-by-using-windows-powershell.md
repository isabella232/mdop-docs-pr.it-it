---
title: Configurazione delle impostazioni avanzate con Windows PowerShell
description: Configurazione delle impostazioni avanzate con Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827395"
---
# <span data-ttu-id="08016-103">Configurazione delle impostazioni avanzate con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="08016-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="08016-104">Il pacchetto dell'area di lavoro MED-V creato include un file di script di Windows PowerShell (con estensione ps1) che è possibile modificare prima di testare e distribuire il pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="08016-105">Questa sezione fornisce informazioni e indicazioni utili per gestire le impostazioni di configurazione di MED-V tramite Windows PowerShell prima di distribuire le aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="08016-106">Usare i cmdlet di Windows PowerShell in MED-V</span><span class="sxs-lookup"><span data-stu-id="08016-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="08016-107">I cmdlet di Windows PowerShell seguenti sono disponibili in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="08016-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="08016-108">New-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="08016-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="08016-109">Export-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="08016-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="08016-110">New-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="08016-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="08016-111">Export-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="08016-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="08016-112">Per accedere ai cmdlet di Windows PowerShell per MED-V, aprire Windows PowerShell e digitare il comando seguente per importare i moduli MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="08016-113">Dopo aver importato i moduli, è possibile accedere alla Guida in linea per i cmdlet usando i comandi della Guida di Windows PowerShell standard, **Man** o **Get-Help**.</span><span class="sxs-lookup"><span data-stu-id="08016-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="08016-114">Ad esempio, per accedere a una descrizione del cmdlet **New-MedvConfiguration** , incluso un elenco completo dei parametri disponibili, digitare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="08016-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="08016-115">È anche possibile visualizzare la guida per parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="08016-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="08016-116">Ad esempio, per visualizzare la guida per il parametro VmMemory, digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="08016-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="08016-117">Per visualizzare un elenco di tutte le impostazioni di configurazione di MED-V e i relativi valori predefiniti, digitare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="08016-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="08016-118">Per visualizzare un elenco di tutte le impostazioni di configurazione di MED-V e i relativi valori correnti, digitare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="08016-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="08016-119">Creazione di un'area di lavoro MED-V con impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="08016-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="08016-120">Dopo aver creato un pacchetto di area di lavoro MED-V usando il Packager area di lavoro MED-V, viene generato uno script di Windows PowerShell nella cartella specificata per il salvataggio dei file di Packager.</span><span class="sxs-lookup"><span data-stu-id="08016-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="08016-121">Il contenuto di questo script Mostra alcune delle impostazioni di configurazione di MED-V disponibili che è possibile modificare.</span><span class="sxs-lookup"><span data-stu-id="08016-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="08016-122">Seguendo questa procedura, è possibile personalizzare lo script e quindi eseguirlo in Windows PowerShell per creare un'area di lavoro MED-V con le nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="08016-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="08016-123">**Importante**  Eseguire Windows PowerShell con le credenziali amministrative e verificare che i criteri di esecuzione di Windows PowerShell consentano l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="08016-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="08016-124">Modificare lo script di Windows PowerShell generato dal Packager area di lavoro MED-V oppure creare un nuovo script con le impostazioni di configurazione desiderate.</span><span class="sxs-lookup"><span data-stu-id="08016-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="08016-125">Eseguire Windows PowerShell con le credenziali amministrative e al prompt dei comandi digitare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="08016-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="08016-126">Questo comando esegue lo script di Windows PowerShell e esegue il cmdlet **New-MedvWorkspace** per generare un nuovo pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="08016-127">I nuovi file di Packager vengono salvati nella cartella specificata in origine per l'archiviazione dei file di Packager dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="08016-128">Per altre informazioni su questo cmdlet, vedere la Guida di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08016-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="08016-129">Esportazione di una configurazione MED-V in un file del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="08016-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="08016-130">È possibile aggiornare le impostazioni di configurazione di MED-V dopo l'installazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="08016-131">Utilizzare il cmdlet **New-MedvConfiguration** per specificare i parametri che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="08016-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="08016-132">Ad esempio, per creare un file del registro di sistema che modifichi l'impostazione della memoria della macchina virtuale, digitare i comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="08016-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="08016-133">Per applicare le nuove impostazioni di configurazione, è possibile importare il file del registro di sistema risultante dal computer host a un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="08016-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="08016-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08016-134">Related topics</span></span>


[<span data-ttu-id="08016-135">Gestione delle impostazioni di configurazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="08016-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="08016-136">Testare e distribuire il pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="08016-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





