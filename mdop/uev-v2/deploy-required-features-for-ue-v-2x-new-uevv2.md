---
title: Distribuire le funzionalità necessarie per UE-V 2.x
description: Distribuire le funzionalità necessarie per UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824666"
---
# <span data-ttu-id="741a9-103">Distribuire le funzionalità necessarie per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="741a9-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="741a9-104">Tutte le distribuzioni Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 richiedono queste funzionalità</span><span class="sxs-lookup"><span data-stu-id="741a9-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="741a9-105">[Distribuire una posizione di archiviazione delle impostazioni](#ssl) accessibile agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="741a9-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="741a9-106">Si tratta di una condivisione di rete standard che consente di archiviare e recuperare le impostazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="741a9-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="741a9-107">Scegliere il metodo di configurazione per UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="741a9-108">La versione UE-V può essere distribuita e configurata usando strumenti di gestione comuni, tra cui criteri di gruppo, Configuration Manager o infrastruttura di gestione di Windows e PowerShell.</span><span class="sxs-lookup"><span data-stu-id="741a9-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="741a9-109">[Distribuire un agente UE-V](#agent) da installare in tutti i computer che sincronizzano le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="741a9-110">Questo monitora le applicazioni registrate e il sistema operativo per tutte le modifiche delle impostazioni e sincronizza le impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="741a9-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="741a9-111">Gli argomenti in questa sezione illustrano come distribuire queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="741a9-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="741a9-112">Distribuire una posizione di archiviazione delle impostazioni di UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="741a9-113">UE-V richiede una posizione in cui archiviare le impostazioni utente nei file di pacchetto delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="741a9-114">È possibile configurare la posizione di archiviazione delle impostazioni in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="741a9-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="741a9-115">Creare un percorso di archiviazione delle impostazioni personalizzato</span><span class="sxs-lookup"><span data-stu-id="741a9-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="741a9-116">Usare Active Directory esistente per la posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="741a9-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="741a9-117">Se non si crea una posizione di archiviazione delle impostazioni, l'agente UE-V utilizzerà Active Directory (AD) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="741a9-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="741a9-118">Nota</span><span class="sxs-lookup"><span data-stu-id="741a9-118">Note</span></span>**  
<span data-ttu-id="741a9-119">Per quanto riguarda la [pianificazione delle prestazioni e della capacità](https://technet.microsoft.com/library/dn458932.aspx#capacity) e per ridurre i problemi di latenza della rete, creare posizioni di archiviazione delle impostazioni nelle stesse reti locali in cui risiedono i computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="741a9-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="741a9-120">È consigliabile 20 MB di spazio su disco per ogni utente per la posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="741a9-121">Creare una posizione di archiviazione delle impostazioni di UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="741a9-122">Prima di definire la posizione di archiviazione delle impostazioni, è necessario creare una directory radice con autorizzazioni di lettura/scrittura per gli utenti che archiviano le impostazioni della condivisione.</span><span class="sxs-lookup"><span data-stu-id="741a9-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="741a9-123">L'agente UE-V crea cartelle specifiche dell'utente nella directory radice.</span><span class="sxs-lookup"><span data-stu-id="741a9-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="741a9-124">La posizione di archiviazione delle impostazioni viene definita impostando l'opzione di configurazione SettingsStoragePath, che può essere configurata utilizzando uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="741a9-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="741a9-125">Quando si [distribuisce l'agente UE-V](#agent) tramite un parametro della riga di comando o in uno script batch</span><span class="sxs-lookup"><span data-stu-id="741a9-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="741a9-126">Impostazioni di [criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="741a9-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="741a9-127">Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) per UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="741a9-128">Dopo l'installazione dell'agente UE-V, usare [Windows PowerShell o Strumentazione gestione Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="741a9-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="741a9-129">Il percorso deve trovarsi in un percorso UNC (Universal Naming Convention) del server e condividere.</span><span class="sxs-lookup"><span data-stu-id="741a9-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="741a9-130">Ad esempio, **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="741a9-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="741a9-131">Questa opzione di configurazione supporta l'uso di variabili per abilitare scenari di sincronizzazione specifici.</span><span class="sxs-lookup"><span data-stu-id="741a9-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="741a9-132">Ad esempio, puoi usare le `%username%\%computername%` variabili per mantenere l'esperienza delle impostazioni degli utenti finali in questi scenari:</span><span class="sxs-lookup"><span data-stu-id="741a9-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="741a9-133">Utenti finali che usano più computer fisici nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="741a9-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="741a9-134">Computer aziendali usati da più utenti finali</span><span class="sxs-lookup"><span data-stu-id="741a9-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="741a9-135">L'agente UE-V crea in modo dinamico un percorso di archiviazione delle impostazioni specifico dell'utente, con una cartella di sistema nascosta denominata `SettingsPackages` , in base all'impostazione di configurazione di **SettingsStoragePath**.</span><span class="sxs-lookup"><span data-stu-id="741a9-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="741a9-136">L'agente legge e scrive le impostazioni in questa posizione, come definito dai modelli di posizione delle impostazioni UE-V registrati.</span><span class="sxs-lookup"><span data-stu-id="741a9-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="741a9-137">**Le impostazioni di UE-V sono determinate dalla regola "ultima scrittura WINS":** Se la posizione di archiviazione delle impostazioni è uguale per l'utente con più computer gestiti, un agente UE-V legge e scrive nella posizione delle impostazioni in modo indipendente dagli agenti in uso in altri computer.</span><span class="sxs-lookup"><span data-stu-id="741a9-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="741a9-138">Le ultime impostazioni e i valori scritti sono quelli applicati quando l'agente successivo legge il percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="741a9-139">**Distribuire il percorso di archiviazione delle impostazioni:** Seguire questa procedura per definire la posizione di archiviazione delle impostazioni invece di usare il servizio Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="741a9-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="741a9-140">È consigliabile limitare l'accesso alla condivisione di archiviazione delle impostazioni agli utenti che lo richiedono, come illustrato nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="741a9-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="741a9-141">Per distribuire la condivisione di rete UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="741a9-142">Creare un nuovo gruppo di sicurezza per gli utenti di UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="741a9-143">Creare una nuova cartella nel computer situato in posizione centrale in cui sono archiviati i pacchetti di impostazioni UE-V e quindi concedere agli utenti di UE-V l'accesso con le autorizzazioni di gruppo alla cartella.</span><span class="sxs-lookup"><span data-stu-id="741a9-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="741a9-144">L'amministratore che supporta UE-V deve disporre delle autorizzazioni per questa cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="741a9-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="741a9-145">Impostare le autorizzazioni SMB (Server Message Block) di livello di condivisione seguenti per la cartella della posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="741a9-146">Account utente</span><span class="sxs-lookup"><span data-stu-id="741a9-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="741a9-147">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="741a9-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="741a9-148">Tutti</span><span class="sxs-lookup"><span data-stu-id="741a9-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="741a9-149">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="741a9-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="741a9-150">Gruppo di sicurezza degli utenti di UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="741a9-151">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="741a9-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="741a9-152">Impostare le autorizzazioni di file system NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="741a9-153">Account utente</span><span class="sxs-lookup"><span data-stu-id="741a9-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="741a9-154">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="741a9-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="741a9-155">Cartella</span><span class="sxs-lookup"><span data-stu-id="741a9-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="741a9-156">Creatore/proprietario</span><span class="sxs-lookup"><span data-stu-id="741a9-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="741a9-157">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="741a9-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="741a9-158">Solo sottocartelle e file</span><span class="sxs-lookup"><span data-stu-id="741a9-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="741a9-159">Gruppo di sicurezza degli utenti di UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="741a9-160">Cartella di elenco/dati letti, creare cartelle/accodare dati</span><span class="sxs-lookup"><span data-stu-id="741a9-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="741a9-161">Solo questa cartella</span><span class="sxs-lookup"><span data-stu-id="741a9-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="741a9-162">Con questa configurazione, l'agente UE-V crea e protegge una cartella Settingspackage mentre viene eseguita nel contesto dell'utente e concede a ogni utente l'autorizzazione per creare cartelle per l'archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="741a9-163">Gli utenti ricevono il controllo completo nella cartella Settingspackage, mentre altri utenti non possono accedervi.</span><span class="sxs-lookup"><span data-stu-id="741a9-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="741a9-164">Nota</span><span class="sxs-lookup"><span data-stu-id="741a9-164">Note</span></span>**  
<span data-ttu-id="741a9-165">Se si crea la condivisione di archiviazione delle impostazioni in un computer che esegue un sistema operativo Windows Server, configurare UE-V per verificare che il gruppo Administrators locale o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="741a9-166">Per abilitare questa ulteriore sicurezza, specificare questa impostazione nell'editor del registro di sistema di Windows Server:</span><span class="sxs-lookup"><span data-stu-id="741a9-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="741a9-167">Aggiungere una chiave **reg \ _DWORD** del registro di sistema denominata **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="741a9-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="741a9-168">Impostare il valore della chiave del registro di sistema su *1*.</span><span class="sxs-lookup"><span data-stu-id="741a9-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="741a9-169">Usare Active Directory con UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="741a9-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="741a9-170">L'agente UE-V usa Active Directory (AD) per impostazione predefinita se una posizione di archiviazione delle impostazioni non è altrimenti definita.</span><span class="sxs-lookup"><span data-stu-id="741a9-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="741a9-171">In questi casi, l'agente UE-V crea dinamicamente la cartella di archiviazione delle impostazioni sotto la radice della Home directory di ogni utente.</span><span class="sxs-lookup"><span data-stu-id="741a9-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="741a9-172">Tuttavia, se è stata configurata un'impostazione di directory personalizzata in AD, viene usata invece quella directory.</span><span class="sxs-lookup"><span data-stu-id="741a9-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="741a9-173">Scegliere il metodo di configurazione per UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="741a9-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="741a9-174">Si vuole individuare il metodo di configurazione che verrà usato per gestire la versione UE-V dopo la distribuzione, poiché questo sarà il metodo di configurazione usato per distribuire l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="741a9-175">In genere, si tratta del metodo di configurazione già usato nell'ambiente, ad esempio Windows PowerShell o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="741a9-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="741a9-176">Puoi configurare la versione UE-V prima, durante o dopo l'installazione dell'agente UE-V, a seconda del metodo di configurazione che usi.</span><span class="sxs-lookup"><span data-stu-id="741a9-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="741a9-177">[Criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)**:** è possibile usare l'infrastruttura di criteri di gruppo esistente per configurare UE-v prima o dopo la distribuzione di agenti UE-v.</span><span class="sxs-lookup"><span data-stu-id="741a9-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="741a9-178">Il modello ADMX di criteri di gruppo di UE-V consente la gestione centralizzata delle opzioni di configurazione dell'agente UE-V comuni e include le impostazioni per la configurazione della sincronizzazione UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="741a9-179">**Installazione dei modelli ADMX di criteri di gruppo di UE-V:** I modelli ADMX di criteri di gruppo per la versione UE-V configurano le impostazioni di sincronizzazione per l'agente UE-V e consentono la gestione centralizzata delle impostazioni di configurazione dell'agente UE-V comuni usando un'infrastruttura di criteri di gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="741a9-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="741a9-180">I sistemi operativi supportati per il controller di dominio che distribuisce gli oggetti Criteri di gruppo includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="741a9-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="741a9-181">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="741a9-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="741a9-182">Windows Server 2012 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="741a9-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="741a9-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** il pacchetto di configurazione UE-v consente di usare la caratteristica Impostazioni conformità di System Center Configuration Manager 2012 SP1 o versioni successive per applicare configurazioni coerenti tra i siti in cui sono installati i sistemi UE-v e Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="741a9-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="741a9-184">[Windows PowerShell e WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** è possibile usare comandi con script per Windows PowerShell e Strumentazione gestione Windows (WMI) per modificare le configurazioni dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="741a9-185">Nota</span><span class="sxs-lookup"><span data-stu-id="741a9-185">Note</span></span>**  
    <span data-ttu-id="741a9-186">La modifica del registro di sistema può causare la perdita di dati o il computer non risponde.</span><span class="sxs-lookup"><span data-stu-id="741a9-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="741a9-187">Ti consigliamo di usare altri metodi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="741a9-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="741a9-188">**Installazione da riga di comando o da script batch:** I parametri usati quando si [distribuisce l'agente UE-v](#agent) configurano molte impostazioni UE-v.</span><span class="sxs-lookup"><span data-stu-id="741a9-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="741a9-189">I sistemi di distribuzione elettronica del software, ad esempio System Center 2012 Configuration Manager, usano questi parametri per configurare i loro client quando distribuiscono e installano il software dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="741a9-190">Distribuire l'agente UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="741a9-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="741a9-191">L'agente UE-V è il nucleo di una distribuzione UE-V e deve essere eseguito in ogni computer che USA UE-V per sincronizzare le impostazioni dell'applicazione e di Windows.</span><span class="sxs-lookup"><span data-stu-id="741a9-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="741a9-192">**File di installazione dell'agente UE-V:** Un singolo file di installazione, AgentSetup.exe, installa l'agente UE-V nei sistemi operativi 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="741a9-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="741a9-193">Vengono inoltre forniti AgentSetupx86.msi o AgentSetupx64.msi file di Windows Installer specifici dell'architettura e, poiché sono più piccoli, potrebbero semplificare le distribuzioni di agente.</span><span class="sxs-lookup"><span data-stu-id="741a9-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="741a9-194">I [parametri della riga di comando per il programma di installazione di AgentSetup.exe](#params) sono supportati anche per l'installazione di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="741a9-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="741a9-195">Importante</span><span class="sxs-lookup"><span data-stu-id="741a9-195">Important</span></span>**  
<span data-ttu-id="741a9-196">Durante l'installazione o la disinstallazione dell'agente UE-V, è possibile usare il file AgentSetup.exe o il &lt; &gt; file Arch. msi di AgentSetup, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="741a9-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="741a9-197">Lo stesso file deve essere usato per disinstallare l'agente UE-V usato per installare l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="741a9-198">Per distribuire l'agente UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="741a9-199">Puoi usare i metodi seguenti per distribuire l'agente UE-V:</span><span class="sxs-lookup"><span data-stu-id="741a9-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="741a9-200">Un sistema di soluzioni Electronic Software Distribution (ESD), ad esempio Configuration Manager, che può installare un file di Windows Installer (con estensione msi).</span><span class="sxs-lookup"><span data-stu-id="741a9-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="741a9-201">Uno script di installazione che fa riferimento al file di Windows Installer (con estensione msi) archiviato centralmente in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="741a9-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="741a9-202">Programma di installazione eseguito manualmente nel computer.</span><span class="sxs-lookup"><span data-stu-id="741a9-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="741a9-203">Usare la procedura seguente per distribuire l'agente UE-V da una condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="741a9-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="741a9-204">Per installare e configurare l'agente UE-V da una condivisione di rete</span><span class="sxs-lookup"><span data-stu-id="741a9-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="741a9-205">Eseguire il file di installazione dell'agente UE-V AgentSetup.exe in una condivisione di rete a cui gli utenti hanno l'autorizzazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="741a9-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="741a9-206">Distribuire uno script nei computer degli utenti che installano l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="741a9-207">Lo script deve specificare la posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="741a9-208">**Opzioni di distribuzione:** Assicurarsi di usare il formato di variabile corretto quando si installa l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="741a9-209">La tabella seguente contiene esempi di opzioni di distribuzione per l'uso dei file AgentSetup.exe o Windows Installer (con estensione msi).</span><span class="sxs-lookup"><span data-stu-id="741a9-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="741a9-210">Tipo di distribuzione</span><span class="sxs-lookup"><span data-stu-id="741a9-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="741a9-211">Descrizione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="741a9-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="741a9-212">Esempio</span><span class="sxs-lookup"><span data-stu-id="741a9-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-213">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="741a9-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-214">Quando si installa l'agente UE-V al prompt dei comandi, usare il <em> formato di variabile% ^ nomeutente% </em> .</span><span class="sxs-lookup"><span data-stu-id="741a9-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="741a9-215">Se sono necessarie le virgolette a causa di spazi nel percorso di archiviazione delle impostazioni, usare un file di script batch per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="741a9-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-216">Script batch</span><span class="sxs-lookup"><span data-stu-id="741a9-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-217">Quando si installa l'agente UE-V da un file di script batch, usare il formato di variabile%% <em> nomeutente%% </em> .</span><span class="sxs-lookup"><span data-stu-id="741a9-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="741a9-218">Se si usa questo metodo di installazione, è necessario sfuggire alla variabile con i caratteri%%.</span><span class="sxs-lookup"><span data-stu-id="741a9-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="741a9-219">Senza questo carattere, lo script espande la <em> variabile username </em> al momento dell'installazione, invece che in fase di esecuzione, che causa l'uso di una singola posizione di archiviazione delle impostazioni per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="741a9-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-220">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="741a9-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-221">Quando si installa l'agente UE-V da un prompt di Windows PowerShell o uno script di Windows PowerShell, usare il <em> formato variabile% nomeutente% </em> .</span><span class="sxs-lookup"><span data-stu-id="741a9-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-222">Distribuzione elettronica del software, ad esempio distribuzione della distribuzione del software di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="741a9-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-223">Quando si installa l'agente UE-V tramite Configuration Manager, usare il <em> formato di variabile ^% nomeutente ^% </em> .</span><span class="sxs-lookup"><span data-stu-id="741a9-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="741a9-224">Nota</span><span class="sxs-lookup"><span data-stu-id="741a9-224">Note</span></span>**  
<span data-ttu-id="741a9-225">L'installazione dell'agente UE-V richiede i diritti di amministratore e il computer richiede un riavvio prima che l'agente UE-V possa essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="741a9-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="741a9-226">Parametri della riga di comando per la distribuzione di agenti UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="741a9-227">I parametri della riga di comando dell'agente UE-V sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="741a9-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="741a9-228">Parametro della riga di comando</span><span class="sxs-lookup"><span data-stu-id="741a9-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="741a9-229">Definizione</span><span class="sxs-lookup"><span data-stu-id="741a9-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="741a9-230">Note</span><span class="sxs-lookup"><span data-stu-id="741a9-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-231">/Help o/h o/?</span><span class="sxs-lookup"><span data-stu-id="741a9-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-232">Visualizza la finestra di dialogo utilizzo AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="741a9-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="741a9-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-234">Indica il percorso UNC (Universal Naming Convention) che definisce la posizione in cui sono archiviate le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="741a9-235">Importante</span><span class="sxs-lookup"><span data-stu-id="741a9-235">Important</span></span></strong><br/><p><span data-ttu-id="741a9-236">È necessario specificare un SettingsStoragePath in UE-V 2,1 e in UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="741a9-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="741a9-237">Puoi impostare la stringa AdHomePath per specificare che viene usato il percorso Home dell'utente&#39;s Active Directory.</span><span class="sxs-lookup"><span data-stu-id="741a9-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="741a9-238">Ad esempio: <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span><span class="sxs-lookup"><span data-stu-id="741a9-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="741a9-239">In UE-V 2,0 è possibile abbandonare SettingsStoragePath blank per usare invece il percorso Home di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="741a9-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="741a9-240">vengono accettate le variabili di ambiente% nomeutente% o% nomecomputer%.</span><span class="sxs-lookup"><span data-stu-id="741a9-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="741a9-241">Gli script possono richiedere variabili di escape.</span><span class="sxs-lookup"><span data-stu-id="741a9-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="741a9-242">Impostazione predefinita </strong> : &lt; None&gt;</span><span class="sxs-lookup"><span data-stu-id="741a9-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="741a9-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-244">Ottiene il valore SettingsStoragePath dal registro di sistema durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="741a9-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-245">Al prompt dei comandi digitare l'esempio seguente per imporre a UE-V di usare il percorso Home di Active Directory invece di un UNC specifico.</span><span class="sxs-lookup"><span data-stu-id="741a9-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="741a9-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-247">Indica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-248">Obbligatorio solo per i modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="741a9-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="741a9-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-250">Specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="741a9-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-251">True | False</span><span class="sxs-lookup"><span data-stu-id="741a9-251">True | False</span></span></p>
<p><strong><span data-ttu-id="741a9-252">Impostazione predefinita </strong> : vero</span><span class="sxs-lookup"><span data-stu-id="741a9-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-253">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="741a9-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-254">Specifica il metodo di sincronizzazione da usare.</span><span class="sxs-lookup"><span data-stu-id="741a9-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-255">SyncProvider | Nessuno</span><span class="sxs-lookup"><span data-stu-id="741a9-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="741a9-256">Impostazione predefinita </strong> : SyncProvider</span><span class="sxs-lookup"><span data-stu-id="741a9-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="741a9-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-258">Specifica il numero di millisecondi che il computer attende prima del timeout quando recupera le impostazioni utente dalla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="741a9-259">Impostazione predefinita </strong> : 2000 millisecondi</span><span class="sxs-lookup"><span data-stu-id="741a9-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="741a9-260">(attendere fino a 2 secondi)</span><span class="sxs-lookup"><span data-stu-id="741a9-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="741a9-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-262">Specifica se la sincronizzazione UE-V è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="741a9-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-263">True | False</span><span class="sxs-lookup"><span data-stu-id="741a9-263">True | False</span></span></p>
<p><strong><span data-ttu-id="741a9-264">Impostazione predefinita </strong> : vero</span><span class="sxs-lookup"><span data-stu-id="741a9-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="741a9-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-266">Specifica una dimensione del file del pacchetto di impostazioni in byte quando l'agente UE-V segnala che i file superano la soglia.</span><span class="sxs-lookup"><span data-stu-id="741a9-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-267">&lt;dimensioni&gt;</span><span class="sxs-lookup"><span data-stu-id="741a9-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="741a9-268">Default </strong> : None (nessuna soglia di avviso)</span><span class="sxs-lookup"><span data-stu-id="741a9-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="741a9-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-270">Specifica l'impostazione per la partecipazione al programma Analisi utilizzo software.</span><span class="sxs-lookup"><span data-stu-id="741a9-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="741a9-271">Se impostato su <strong> true </strong> , le informazioni sul programma di installazione vengono caricate nel sito Microsoft Customer Experience Improvement Program.</span><span class="sxs-lookup"><span data-stu-id="741a9-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="741a9-272">Se impostato su <strong> false </strong> , non vengono caricate informazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-273">True | False</span><span class="sxs-lookup"><span data-stu-id="741a9-273">True | False</span></span></p>
<p><strong><span data-ttu-id="741a9-274">Impostazione predefinita </strong> : false</span><span class="sxs-lookup"><span data-stu-id="741a9-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-275">NoRestart</span><span class="sxs-lookup"><span data-stu-id="741a9-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-276">Supporta il differimento del riavvio del computer dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="741a9-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-278">Consente di impostare una cartella di installazione diversa per l'agente UE-V o per il generatore di UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="741a9-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-280">Consente alla configurazione di accettare l'opzione da includere nel programma Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="741a9-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="741a9-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="741a9-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-282">Consente l'installazione di UE-V in modo invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="741a9-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="741a9-283">Questa operazione deve essere impostata su <strong> true </strong> per installare la versione UE-v in modo silenzioso e ignorare il requisito che l'utente accetti le condizioni di licenza UE-v.</span><span class="sxs-lookup"><span data-stu-id="741a9-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="741a9-284">Se impostato su <strong> false </strong> o Left Empty, l'utente riceverà un messaggio di errore e non verrà installato UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="741a9-285">Importante</span><span class="sxs-lookup"><span data-stu-id="741a9-285">Important</span></span></strong><br/><p><span data-ttu-id="741a9-286">Questo parametro è obbligatorio per l'installazione di UE-V in modo invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="741a9-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="741a9-287">NORESTART</span><span class="sxs-lookup"><span data-stu-id="741a9-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="741a9-288">Impedisce un riavvio obbligatorio dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="741a9-289">Aggiornare l'agente UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-289">Update the UE-V Agent</span></span>

<span data-ttu-id="741a9-290">Gli aggiornamenti per il software dell'agente UE-V vengono forniti tramite Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="741a9-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="741a9-291">Puoi distribuire gli aggiornamenti di agente UE-V tramite sistemi di infrastruttura ESD (Enterprise Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="741a9-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="741a9-292">Durante l'aggiornamento di un agente UE-V, è possibile aggiornare il gruppo predefinito dei modelli di posizione delle impostazioni per le applicazioni Microsoft comuni e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="741a9-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="741a9-293">Aggiornare l'agente UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="741a9-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="741a9-294">L'agente UE-V 2. x introduce molte nuove funzionalità e modifica la modalità e il momento in cui l'agente carica il contenuto nella condivisione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="741a9-295">Il processo di aggiornamento automatizza queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="741a9-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="741a9-296">Per aggiornare l'agente UE-V, eseguire il pacchetto di installazione dell'agente UE-V (AgentSetup.exe, AgentSetupx86.msi o AgentSetupx64.msi) nei computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="741a9-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="741a9-297">Nota</span><span class="sxs-lookup"><span data-stu-id="741a9-297">Note</span></span>**  
<span data-ttu-id="741a9-298">Quando si esegue l'aggiornamento dell'agente UE-V, è necessario usare lo stesso tipo di programma di installazione (file exe o pacchetto MSI) che ha installato il precedente agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="741a9-299">Ad esempio, usa la AgentSetup.exe UE-V 2 per aggiornare gli agenti UE-V 1,0 installati tramite AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="741a9-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="741a9-300">Le configurazioni seguenti vengono mantenute quando viene eseguito il programma di installazione dell'agente:</span><span class="sxs-lookup"><span data-stu-id="741a9-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="741a9-301">Percorso di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="741a9-301">Settings storage path</span></span>

-   <span data-ttu-id="741a9-302">Impostazioni del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="741a9-302">Registry settings</span></span>

-   <span data-ttu-id="741a9-303">Attività pianificate (le impostazioni di intervallo vengono reimpostate sui valori predefiniti)</span><span class="sxs-lookup"><span data-stu-id="741a9-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="741a9-304">Nota</span><span class="sxs-lookup"><span data-stu-id="741a9-304">Note</span></span>**  
<span data-ttu-id="741a9-305">Un computer con i modelli di posizione delle impostazioni di UE-V 2. x registrati negli errori di registrazione dell'agente UE-V 1,0 nel registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="741a9-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="741a9-306">È possibile usare Microsoft System Center 2012 Configuration Manager o un altro strumento di distribuzione del software aziendale per automatizzare e distribuire l'aggiornamento dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="741a9-307">**Raccomandazioni:** È consigliabile aggiornare tutti gli agenti UE-V 1,0 in un ambiente di elaborazione, ma non è necessario.</span><span class="sxs-lookup"><span data-stu-id="741a9-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="741a9-308">I modelli di posizione delle impostazioni di UE-V 2. x possono interagire con un agente UE-V 1,0 perché condividono solo le impostazioni dal percorso di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="741a9-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="741a9-309">È tuttavia consigliabile trasferire le distribuzioni a una versione di un singolo agente per semplificare la gestione e supportare UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="741a9-310">Ripristinare l'agente UE-V dopo un aggiornamento non riuscito</span><span class="sxs-lookup"><span data-stu-id="741a9-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="741a9-311">Dopo aver tentato una delle operazioni seguenti, potrebbe verificarsi un errore:</span><span class="sxs-lookup"><span data-stu-id="741a9-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="741a9-312">Eseguire l'aggiornamento da UE-V 1,0 a UE-V 2</span><span class="sxs-lookup"><span data-stu-id="741a9-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="741a9-313">Eseguire l'aggiornamento a una versione più recente di Windows, ad esempio da Windows 7 a Windows 8 o da Windows 8 a Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="741a9-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="741a9-314">Disinstallare l'agente dopo l'aggiornamento dell'agente UE-V</span><span class="sxs-lookup"><span data-stu-id="741a9-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="741a9-315">Per risolvere eventuali problemi, provare a ripristinare l'agente UE-V immettendo questo comando al prompt dei comandi nel computer in cui è installato l'agente.</span><span class="sxs-lookup"><span data-stu-id="741a9-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="741a9-316">Puoi quindi riprovare il processo di disinstallazione o l'aggiornamento installando la versione più recente dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="741a9-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="741a9-317">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="741a9-317">Related topics</span></span>


[<span data-ttu-id="741a9-318">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="741a9-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="741a9-319">Distribuire UE-V 2. x per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="741a9-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









