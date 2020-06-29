---
title: Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI
description: Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819296"
---
# <span data-ttu-id="63aad-103">Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="63aad-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="63aad-104">È possibile usare WMI e PowerShell per gestire il comportamento della configurazione e della sincronizzazione dell'agente Microsoft Experience (UE-V).</span><span class="sxs-lookup"><span data-stu-id="63aad-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="63aad-105">Come distribuire l'agente UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aad-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="63aad-106">Organizzare il file del programma di installazione di UE-V in una condivisione di rete accessibile.</span><span class="sxs-lookup"><span data-stu-id="63aad-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="63aad-107">Nota</span><span class="sxs-lookup"><span data-stu-id="63aad-107">Note</span></span>**  
    <span data-ttu-id="63aad-108">USA AgentSetup.exe per distribuire versioni a 32 bit e a 64 bit dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="63aad-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="63aad-109">Le versioni dei file di Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, sono disponibili per ogni architettura.</span><span class="sxs-lookup"><span data-stu-id="63aad-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="63aad-110">Per disinstallare l'agente UE-V in un secondo momento usando il file di installazione, è necessario usare lo stesso tipo di file.</span><span class="sxs-lookup"><span data-stu-id="63aad-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="63aad-111">Usare uno dei comandi di PowerShell seguenti per installare l'agente.</span><span class="sxs-lookup"><span data-stu-id="63aad-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="63aad-112">Come configurare l'agente UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aad-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="63aad-113">Usare un account con diritti di amministratore per aprire una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63aad-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="63aad-114">Importare il modulo di PowerShell UE-V usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="63aad-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="63aad-115">Usare i comandi di PowerShell seguenti per configurare l'agente.</span><span class="sxs-lookup"><span data-stu-id="63aad-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="63aad-116">Comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aad-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="63aad-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63aad-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-118">Get-UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="63aad-119">Visualizzare le impostazioni effettive dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="63aad-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="63aad-120">Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-121">Get-UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="63aad-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="63aad-122">Visualizzare i valori delle impostazioni dell'agente UE-V solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="63aad-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-123">Get-UevConfiguration-computer</span><span class="sxs-lookup"><span data-stu-id="63aad-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-124">Visualizzare i valori delle impostazioni di configurazione dell'agente UE-V per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-125">Set-UevConfiguration-computer- &lt; percorso di SettingsStoragePath per _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-126">Definire una posizione di archiviazione delle impostazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-127">Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; path to _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-128">Definire una posizione di archiviazione delle impostazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="63aad-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-129">Set-UevConfiguration-computer- &lt; timeout di SyncTimeoutInMilliseconds in millisecondi&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-130">Impostare il timeout della sincronizzazione in millisecondi</span><span class="sxs-lookup"><span data-stu-id="63aad-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-131">Set-UevConfiguration-CurrentComputerUser- &lt; timeout di SyncTimeoutInMilliseconds in millisecondi&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-132">Impostare il timeout della sincronizzazione per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="63aad-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-133">Set-UevConfiguration-computer- &lt; dimensione MaxPackageSizeInBytes in byte&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-134">Configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</span><span class="sxs-lookup"><span data-stu-id="63aad-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="63aad-135">Impostare la dimensione del pacchetto soglia in byte.</span><span class="sxs-lookup"><span data-stu-id="63aad-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-136">Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; dimensione in byte&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-137">Impostare la soglia di avviso dimensione pacchetto per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="63aad-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-138">Set-UevConfiguration-computer- &lt; percorso di SettingsTemplateCatalogPath per il catalogo&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-139">Impostare il percorso del catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="63aad-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-140">Set-UevConfiguration-computer-metodo di sincronizzazione di SyncMethod &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-141">Impostare il metodo di sincronizzazione: OfflineFiles o None.</span><span class="sxs-lookup"><span data-stu-id="63aad-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-142">Set-UevConfiguration-CurrentComputerUser-metodo di sincronizzazione di SyncMethod &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-143">Imposta il metodo di sincronizzazione per l'utente corrente: OfflineFiles o None.</span><span class="sxs-lookup"><span data-stu-id="63aad-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-144">Set-UEVConfiguration-computer-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="63aad-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-145">Abilitare la notifica in caso di ritardo dell'importazione delle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="63aad-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="63aad-146">Usare-DisableSettingsImportNotify per disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="63aad-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-147">Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="63aad-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-148">Abilitare la notifica per l'utente corrente quando l'importazione delle impostazioni utente viene ritardata.</span><span class="sxs-lookup"><span data-stu-id="63aad-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="63aad-149">Usare-DisableSettingsImportNotify per disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="63aad-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-150">Set-UEVConfiguration-computer-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="63aad-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-151">Specificare l'ora in secondi prima della notifica dell'utente</span><span class="sxs-lookup"><span data-stu-id="63aad-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-152">Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="63aad-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-153">Specificare l'ora in secondi prima della notifica per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="63aad-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-154">Set-UevConfiguration-computer-DisableSync</span><span class="sxs-lookup"><span data-stu-id="63aad-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-155">Disabilitare UE-V per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="63aad-156">Usare-EnableSync per abilitare o riattivare.</span><span class="sxs-lookup"><span data-stu-id="63aad-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-157">Set-UevConfiguration-CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="63aad-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-158">Disabilitare UE-V per l'utente corrente nel computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="63aad-159">Usare-EnableSync per abilitare o riattivare.</span><span class="sxs-lookup"><span data-stu-id="63aad-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-160">Clear-UevConfiguration- &lt; Nome impostazione computer&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-161">Deselezionare un'impostazione specifica per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-162">Clear-UevConfiguration-CurrentComputerUser- &lt; Nome impostazione&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-163">Deselezionare un'impostazione specifica per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="63aad-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-164">&lt;File di migrazione delle impostazioni di Export-UevConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-165">Esportare la configurazione del computer UE-V in un file di migrazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="63aad-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="63aad-166">L'estensione del file deve essere ". UEV".</span><span class="sxs-lookup"><span data-stu-id="63aad-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="63aad-167">Il cmdlet Export Esporta tutte le impostazioni dell'agente UE-V che possono essere configurate con il parametro-computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-168">&lt;File di migrazione delle impostazioni di import-UevConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-169">Importare la configurazione di computer UE-V da un file di migrazione delle impostazioni (file con estensione UEV).</span><span class="sxs-lookup"><span data-stu-id="63aad-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="63aad-170">Come esportare le impostazioni del pacchetto UE-V e ripristinare i modelli UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aad-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="63aad-171">Aprire una finestra di PowerShell come amministratore.</span><span class="sxs-lookup"><span data-stu-id="63aad-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="63aad-172">Importare il modulo di PowerShell UE-V con il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="63aad-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="63aad-173">Usare i comandi di PowerShell seguenti per configurare l'agente.</span><span class="sxs-lookup"><span data-stu-id="63aad-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="63aad-174">Comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aad-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="63aad-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63aad-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-176">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="63aad-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-177">Estrae le impostazioni da un file di pacchetto del calcolatore Microsoft e le converte in un formato leggibile in XML.</span><span class="sxs-lookup"><span data-stu-id="63aad-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-178">Repair-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="63aad-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-179">Ripristina l'indice dei modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="63aad-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="63aad-180">Come configurare l'agente UE-V con WMI</span><span class="sxs-lookup"><span data-stu-id="63aad-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="63aad-181">La virtualizzazione dell'esperienza utente fornisce il set di comandi WMI seguente.</span><span class="sxs-lookup"><span data-stu-id="63aad-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="63aad-182">Gli amministratori possono usare questa interfaccia per configurare l'agente UE-V dalla riga di comando e automatizzare le attività di configurazione tipiche.</span><span class="sxs-lookup"><span data-stu-id="63aad-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="63aad-183">Usare un account con diritti di amministratore per aprire una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63aad-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="63aad-184">Usare i comandi WMI seguenti per configurare l'agente.</span><span class="sxs-lookup"><span data-stu-id="63aad-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="63aad-185">Comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aad-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="63aad-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63aad-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-187">Get-WmiObject-configurazione dello spazio dei nomi root\Microsoft\UEV</span><span class="sxs-lookup"><span data-stu-id="63aad-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="63aad-188">Visualizzare le impostazioni attive dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="63aad-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="63aad-189">Le impostazioni specifiche dell'utente hanno la precedenza sulle impostazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-190">Get-WmiObject-spazio dei nomi root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-191">Visualizzare la configurazione dell'agente UE-V definita per l'utente.</span><span class="sxs-lookup"><span data-stu-id="63aad-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-192">Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-193">Visualizzare la configurazione dell'agente UE-V definita per il computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-194">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="63aad-196">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-197">Definire una posizione di archiviazione delle impostazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-198">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="63aad-200">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-201">Definire una posizione di archiviazione delle impostazioni per utente.</span><span class="sxs-lookup"><span data-stu-id="63aad-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-202">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="63aad-204">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-205">Impostare il timeout della sincronizzazione in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="63aad-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-206">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="63aad-208">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-209">Configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</span><span class="sxs-lookup"><span data-stu-id="63aad-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="63aad-210">Impostare la dimensione del file del pacchetto soglia in byte.</span><span class="sxs-lookup"><span data-stu-id="63aad-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-211">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-212">$config. SyncMethod = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="63aad-213">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-214">Impostare il metodo di sincronizzazione: OfflineFiles o None.</span><span class="sxs-lookup"><span data-stu-id="63aad-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63aad-215">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-216">$config. &lt; impostazione del &gt;  =  &lt; valore dell'impostazione del nome&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="63aad-217">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-218">Aggiornare una specifica impostazione per computer.</span><span class="sxs-lookup"><span data-stu-id="63aad-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="63aad-219">Per cancellare l'impostazione, usare $null come valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="63aad-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63aad-220">$config = Get-WmiObject-spazio dei nomi root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="63aad-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="63aad-221">$config. &lt; impostazione del &gt;  =  &lt; valore dell'impostazione del nome&gt;</span><span class="sxs-lookup"><span data-stu-id="63aad-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="63aad-222">$config. Inserire ()</span><span class="sxs-lookup"><span data-stu-id="63aad-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63aad-223">Aggiornare una specifica impostazione per utente.</span><span class="sxs-lookup"><span data-stu-id="63aad-223">Update a specific per-user setting.</span></span> <span data-ttu-id="63aad-224">Per cancellare l'impostazione, usare $null come valore dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="63aad-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="63aad-225">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63aad-225">Related topics</span></span>


[<span data-ttu-id="63aad-226">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="63aad-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="63aad-227">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="63aad-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









