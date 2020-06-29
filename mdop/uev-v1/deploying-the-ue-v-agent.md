---
title: Distribuzione dell'agente di UE-V
description: Distribuzione dell'agente di UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827185"
---
# <span data-ttu-id="50802-103">Distribuzione dell'agente di UE-V</span><span class="sxs-lookup"><span data-stu-id="50802-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="50802-104">L'agente Microsoft User Experience Virtualization (UE-V) deve essere eseguito in ogni computer che USA UE-V per aggirare le impostazioni dell'applicazione e di Windows.</span><span class="sxs-lookup"><span data-stu-id="50802-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="50802-105">Un singolo file del programma di installazione, AgentSetup.exe, installa l'agente UE-V nei sistemi operativi 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="50802-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="50802-106">I parametri della riga di comando dell'agente UE-V sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="50802-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="50802-107">AgentSetup.exe parametri della riga di comando</span><span class="sxs-lookup"><span data-stu-id="50802-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="50802-108">Parametro della riga di comando</span><span class="sxs-lookup"><span data-stu-id="50802-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="50802-109">Definizione</span><span class="sxs-lookup"><span data-stu-id="50802-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="50802-110">Note</span><span class="sxs-lookup"><span data-stu-id="50802-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-111">/Help o/h o/?</span><span class="sxs-lookup"><span data-stu-id="50802-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-112">Visualizza la finestra di dialogo AgentSetup.exe utilizzo.</span><span class="sxs-lookup"><span data-stu-id="50802-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50802-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="50802-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-114">Indica il percorso UNC (Universal Naming Convention) che definisce la posizione in cui sono archiviate le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-115">vengono accettate le variabili di ambiente% nomeutente% o% nomecomputer%.</span><span class="sxs-lookup"><span data-stu-id="50802-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="50802-116">Gli script possono richiedere variabili di escape.</span><span class="sxs-lookup"><span data-stu-id="50802-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="50802-117">Impostazione predefinita </strong> : &lt; None &gt; (Home utente di Active Directory)</span><span class="sxs-lookup"><span data-stu-id="50802-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="50802-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-119">Indica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-120">Obbligatorio solo per i modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="50802-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50802-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="50802-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-122">Specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="50802-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-123">True | False</span><span class="sxs-lookup"><span data-stu-id="50802-123">True | False</span></span></p>
<p><strong><span data-ttu-id="50802-124">Impostazione predefinita </strong> : vero</span><span class="sxs-lookup"><span data-stu-id="50802-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-125">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="50802-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-126">Specifica il metodo di sincronizzazione da usare.</span><span class="sxs-lookup"><span data-stu-id="50802-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-127">OfflineFiles | Nessuno</span><span class="sxs-lookup"><span data-stu-id="50802-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="50802-128">Impostazione predefinita </strong> : offlinefiles</span><span class="sxs-lookup"><span data-stu-id="50802-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50802-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="50802-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-130">Specifica il numero di millisecondi che il computer attende prima del timeout quando recupera le impostazioni utente dalla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="50802-131">Impostazione predefinita </strong> : 2000 millisecondi</span><span class="sxs-lookup"><span data-stu-id="50802-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="50802-132">(attendere fino a 2 secondi)</span><span class="sxs-lookup"><span data-stu-id="50802-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="50802-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-134">Specifica se la sincronizzazione UE-V è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="50802-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-135">True | False</span><span class="sxs-lookup"><span data-stu-id="50802-135">True | False</span></span></p>
<p><strong><span data-ttu-id="50802-136">Impostazione predefinita </strong> : vero</span><span class="sxs-lookup"><span data-stu-id="50802-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50802-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="50802-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-138">Specifica una dimensione del file del pacchetto di impostazioni in byte quando l'agente UE-V segnala che i file superano la soglia.</span><span class="sxs-lookup"><span data-stu-id="50802-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-139">&lt;dimensioni&gt;</span><span class="sxs-lookup"><span data-stu-id="50802-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="50802-140">Default </strong> : None (nessuna soglia di avviso)</span><span class="sxs-lookup"><span data-stu-id="50802-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="50802-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-142">Specifica l'impostazione per la partecipazione al programma Analisi utilizzo software.</span><span class="sxs-lookup"><span data-stu-id="50802-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="50802-143">Se impostato su true, le informazioni sul programma di installazione vengono caricate nel sito Microsoft Customer Experience Improvement Program.</span><span class="sxs-lookup"><span data-stu-id="50802-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="50802-144">Se impostato su false, non vengono caricate informazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-145">True | False</span><span class="sxs-lookup"><span data-stu-id="50802-145">True | False</span></span></p>
<p><strong><span data-ttu-id="50802-146">Impostazione predefinita </strong> : false</span><span class="sxs-lookup"><span data-stu-id="50802-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="50802-147">In Windows 7 </strong> : vero</span><span class="sxs-lookup"><span data-stu-id="50802-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="50802-148">Durante l'installazione, il parametro della riga di comando SettingsStoragePath specifica la posizione di archiviazione delle impostazioni per i valori delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="50802-149">Una posizione di archiviazione delle impostazioni può essere definita prima della distribuzione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="50802-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="50802-150">Se non è stata definita la posizione di archiviazione delle impostazioni, quindi UE-V usa la directory Home dell'utente di Active Directory come posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="50802-151">Quando si specifica la configurazione di SettingsStoragePath durante l'installazione e si usa% username% come parte del valore, la stessa esperienza delle impostazioni utente verrà aggirata in tutti i computer o le sessioni in cui un utente accede.</span><span class="sxs-lookup"><span data-stu-id="50802-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="50802-152">Se specifichi le variabili%UserName%\\%ComputerName% come parte del valore SettingsStoragePath, questo consentirà di mantenere l'esperienza delle impostazioni per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="50802-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="50802-153">I file di Windows Installer (MSI) specifici dell'architettura vengono forniti per l'installazione dell'agente UE-V oltre al programma di installazione combinato a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="50802-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="50802-154">I file di installazione AgentSetupx86.msi o AgentSetupx64.msi sono più piccoli del file AgentSetup.exe e potrebbero semplificare le distribuzioni degli agenti.</span><span class="sxs-lookup"><span data-stu-id="50802-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="50802-155">I parametri della riga di comando per il programma di installazione di AgentSetup.exe sono supportati per l'installazione di Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="50802-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="50802-156">**Nota**  Durante l'installazione o la disinstallazione dell'agente UE-V è possibile usare il file AgentSetup.exe o il &lt; &gt; file Arch. msi di AgentSetup, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="50802-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="50802-157">Lo stesso file deve essere usato per disinstallare l'agente UE-V quando è stato usato per installare l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="50802-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="50802-158">Assicurarsi di usare il formato di variabile corretto quando si installa l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="50802-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="50802-159">La tabella seguente contiene esempi di opzioni di distribuzione per l'uso dei file di installazione AgentSetup.exe o Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="50802-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="50802-160">Tipo di distribuzione</span><span class="sxs-lookup"><span data-stu-id="50802-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="50802-161">Descrizione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="50802-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="50802-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="50802-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-163">Prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="50802-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-164">Quando si installa l'agente UE-V da un prompt dei comandi, usare il formato di variabile% ^ nomeutente%.</span><span class="sxs-lookup"><span data-stu-id="50802-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="50802-165">Se sono necessarie le virgolette a causa di spazi nel percorso di archiviazione delle impostazioni, usare un file di script batch per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="50802-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50802-166">Script batch</span><span class="sxs-lookup"><span data-stu-id="50802-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-167">Quando si installa l'agente UE-V da un file di script batch, usare il formato di variabile%% nomeutente%%.</span><span class="sxs-lookup"><span data-stu-id="50802-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="50802-168">Se si usa questo metodo di installazione, è necessario sfuggire alla variabile con i caratteri%%.</span><span class="sxs-lookup"><span data-stu-id="50802-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="50802-169">Senza questo carattere, lo script espande la variabile username al momento dell'installazione, invece che in fase di esecuzione, causando l'uso di una singola posizione di archiviazione delle impostazioni per tutti gli utenti con UE-V.</span><span class="sxs-lookup"><span data-stu-id="50802-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50802-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="50802-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-171">Quando si installa l'agente UE-V da un prompt di PowerShell o da uno script di PowerShell, usare il formato variabile% nomeutente%.</span><span class="sxs-lookup"><span data-stu-id="50802-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50802-172">Distribuzione elettronica del software, ad esempio distribuzione della distribuzione del software di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="50802-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="50802-173">Quando si installa l'agente UE-V con Configuration Manager, usare il formato di variabile ^% nomeutente ^%.</span><span class="sxs-lookup"><span data-stu-id="50802-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="50802-174">**Nota**  L'installazione dell'agente U-EV richiede i diritti di amministratore e il computer richiederà un riavvio prima che l'agente UE-V possa essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="50802-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="50802-175">Metodi di distribuzione di agenti UE-V da una condivisione di rete</span><span class="sxs-lookup"><span data-stu-id="50802-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="50802-176">Puoi usare i metodi seguenti per distribuire l'agente UE-V:</span><span class="sxs-lookup"><span data-stu-id="50802-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="50802-177">Soluzione ESD (Electronic Software Distribution) che può installare un file di Windows Installer (con estensione msi).</span><span class="sxs-lookup"><span data-stu-id="50802-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="50802-178">Uno script di installazione che fa riferimento al file di Windows Installer (con estensione msi) archiviato centralmente in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="50802-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="50802-179">Eseguire manualmente il programma di installazione nel computer.</span><span class="sxs-lookup"><span data-stu-id="50802-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="50802-180">Per distribuire l'agente UE-V da una condivisione di rete, eseguire la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="50802-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="50802-181">Per installare e configurare l'agente UE-V da una condivisione di rete</span><span class="sxs-lookup"><span data-stu-id="50802-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="50802-182">Eseguire il file di installazione dell'agente UE-V (AgentSetup.exe) in una condivisione di rete a cui gli utenti hanno l'autorizzazione "Leggi".</span><span class="sxs-lookup"><span data-stu-id="50802-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="50802-183">Distribuire uno script nei computer degli utenti che installano l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="50802-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="50802-184">Lo script deve specificare la posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="50802-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="50802-185">Aggiornare l'agente UE-V</span><span class="sxs-lookup"><span data-stu-id="50802-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="50802-186">Gli aggiornamenti per il software dell'agente UE-V verranno forniti tramite Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="50802-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="50802-187">Durante l'aggiornamento dell'agente UE-V, il gruppo predefinito dei modelli di posizione delle impostazioni per le comuni applicazioni Microsoft e le impostazioni di Windows può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="50802-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="50802-188">Gli aggiornamenti dell'agente UE-V possono essere distribuiti usando l'infrastruttura ESD (Enterprise Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="50802-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="50802-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50802-189">Related topics</span></span>


[<span data-ttu-id="50802-190">Distribuzione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="50802-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="50802-191">Configurazioni supportate per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="50802-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="50802-192">Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0</span><span class="sxs-lookup"><span data-stu-id="50802-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="50802-193">Installazione di Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="50802-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="50802-194">Distribuire l'agente di virtualizzazione dell'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="50802-194">Deploy the User Experience Virtualization Agent</span></span>
 

 





