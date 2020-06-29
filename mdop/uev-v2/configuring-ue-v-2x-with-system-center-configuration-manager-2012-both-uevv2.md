---
title: Configurazione di UE-V 2. x con System Center Configuration Manager 2012
description: Configurazione di UE-V 2. x con System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824406"
---
# <span data-ttu-id="63cbe-103">Configurazione di UE-V 2. x con System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="63cbe-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="63cbe-104">Dopo l'installazione di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1 e le relative caratteristiche necessarie, è necessario configurare UE-V.</span><span class="sxs-lookup"><span data-stu-id="63cbe-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="63cbe-105">Il pacchetto di configurazione UE-V consente agli amministratori di usare la caratteristica Impostazioni conformità di System Center Configuration Manager 2012 SP1 o versioni successive per applicare configurazioni coerenti tra i siti in cui sono installati i sistemi UE-V e Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="63cbe-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="63cbe-106">Funzionalità supportate di Configuration Pack di UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="63cbe-107">Il pacchetto di configurazione UE-V include strumenti per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="63cbe-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="63cbe-108">Creare o aggiornare le previsioni di distribuzione del modello di posizione delle impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="63cbe-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="63cbe-109">Definire i modelli UE-V da registrare o annullare la registrazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="63cbe-110">Aggiornare gli elementi di configurazione e le previsioni del modello UE-V come vengono aggiunti o aggiornati i modelli</span><span class="sxs-lookup"><span data-stu-id="63cbe-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="63cbe-111">Distribuire e registrare modelli UE-V usando la correzione standard degli elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="63cbe-112">Creare o aggiornare un elemento della configurazione dei criteri dell'agente UE-V per impostare o deselezionare queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="63cbe-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63cbe-113">Dimensione massima del pacchetto</span><span class="sxs-lookup"><span data-stu-id="63cbe-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-114">Abilitare/disabilitare la sincronizzazione delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="63cbe-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-115">Attendere la sincronizzazione all'avvio dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63cbe-116">Impostazione del ritardo di importazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-117">Sincronizzare le app di Windows non in elenco</span><span class="sxs-lookup"><span data-stu-id="63cbe-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-118">Attendere la sincronizzazione all'accesso</span><span class="sxs-lookup"><span data-stu-id="63cbe-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63cbe-119">Notifica di importazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="63cbe-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-120">URL del contatto IT</span><span class="sxs-lookup"><span data-stu-id="63cbe-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-121">Attendere il timeout della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63cbe-122">Percorso di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="63cbe-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-123">Contattare il testo descrittivo</span><span class="sxs-lookup"><span data-stu-id="63cbe-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-124">Percorso catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="63cbe-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63cbe-125">Attivazione della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-126">Icona del vassoio abilitata</span><span class="sxs-lookup"><span data-stu-id="63cbe-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-127">Start/Stop UE-servizio agente V</span><span class="sxs-lookup"><span data-stu-id="63cbe-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="63cbe-128">Metodo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-129">Notifica primo utilizzo</span><span class="sxs-lookup"><span data-stu-id="63cbe-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="63cbe-130">Definire le app di Windows che andranno in roaming</span><span class="sxs-lookup"><span data-stu-id="63cbe-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="63cbe-131">Timeout sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="63cbe-132">Verificare la conformità confermando che UE-V è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="63cbe-133">Generare un elemento di configurazione dei criteri dell'agente UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="63cbe-134">Tutti i criteri e la configurazione dell'agente UE-V vengono distribuiti tramite un singolo elemento di configurazione generato tramite lo strumento UevAgentPolicyGenerator.exe.</span><span class="sxs-lookup"><span data-stu-id="63cbe-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="63cbe-135">Questo strumento legge la configurazione desiderata da un file di configurazione XML e crea un IC contenente le impostazioni di individuazione e correzione necessarie per conferire al computer la conformità.</span><span class="sxs-lookup"><span data-stu-id="63cbe-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="63cbe-136">Il file CAB dell'elemento di configurazione dei criteri dell'agente UE-V viene creato usando lo strumento della riga di comando UevTemplateBaselineGenerator.exe, che contiene questi parametri:</span><span class="sxs-lookup"><span data-stu-id="63cbe-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="63cbe-137">&lt;Codice sito sito&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="63cbe-138">PolicyName &lt; Name &gt; facoltativo: impostazione predefinita "criteri agente UE-V" se non è presente</span><span class="sxs-lookup"><span data-stu-id="63cbe-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="63cbe-139">&lt;Descrizione PolicyDescription &gt; facoltativa: se non è presente, viene fornita una descrizione</span><span class="sxs-lookup"><span data-stu-id="63cbe-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="63cbe-140">&lt;Percorso completo di CabFilePath per l'elemento di configurazione. File CAB&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="63cbe-141">&lt;Percorso completo di ConfigurationFile al file XML di configurazione dell'agente&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="63cbe-142">**Nota**  Potrebbe essere necessario modificare i criteri di esecuzione di PowerShell per consentire l'esecuzione di questi script nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="63cbe-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="63cbe-143">Eseguire questi passaggi nella console di Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="63cbe-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="63cbe-144">Selezionare \*\* &gt; le &gt; proprietà delle impostazioni del client di amministrazione\*\*</span><span class="sxs-lookup"><span data-stu-id="63cbe-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="63cbe-145">Nella scheda **agente utente** impostare i criteri di **esecuzione di PowerShell** su **Ignora**</span><span class="sxs-lookup"><span data-stu-id="63cbe-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="63cbe-146">Creare il primo elemento di configurazione dei criteri UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="63cbe-147">Copiare il file di configurazione delle impostazioni predefinite dalla directory di installazione di UE-V config Pack in una posizione visibile alla console di amministrazione di ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="63cbe-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="63cbe-148">Il file di configurazione predefinito contiene cinque sezioni:</span><span class="sxs-lookup"><span data-stu-id="63cbe-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="63cbe-149">Criteri computer</span><span class="sxs-lookup"><span data-stu-id="63cbe-149">Computer Policy</span></span>**  
    <span data-ttu-id="63cbe-150">Tutte le impostazioni di livello computer UE-V.</span><span class="sxs-lookup"><span data-stu-id="63cbe-150">All UE-V machine level settings.</span></span> <span data-ttu-id="63cbe-151">L'attributo DesiredState può essere</span><span class="sxs-lookup"><span data-stu-id="63cbe-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="63cbe-152">**Impostare** il valore assegnato nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="63cbe-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="63cbe-153">**Deselezionare** per rimuovere l'impostazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="63cbe-154">**Non gestito** per avere l'elemento di configurazione lasciato allo stato corrente</span><span class="sxs-lookup"><span data-stu-id="63cbe-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="63cbe-155">Non rimuovere le righe da questa sezione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-155">Do not remove lines from this section.</span></span> <span data-ttu-id="63cbe-156">Imposta invece la DesiredState su "non gestito" se non vuoi che Configuration Manager modifichi i valori correnti o predefiniti.</span><span class="sxs-lookup"><span data-stu-id="63cbe-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="63cbe-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="63cbe-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="63cbe-158">Tutte le impostazioni di livello utente di UE-V.</span><span class="sxs-lookup"><span data-stu-id="63cbe-158">All UE-V user level settings.</span></span> <span data-ttu-id="63cbe-159">Queste voci eseguono l'override delle impostazioni del computer per un utente.</span><span class="sxs-lookup"><span data-stu-id="63cbe-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="63cbe-160">L'attributo DesiredState può essere</span><span class="sxs-lookup"><span data-stu-id="63cbe-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="63cbe-161">**Impostare** il valore assegnato nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="63cbe-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="63cbe-162">**Deselezionare** per rimuovere l'impostazione</span><span class="sxs-lookup"><span data-stu-id="63cbe-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="63cbe-163">**Non gestito** per avere l'elemento di configurazione lasciato allo stato corrente</span><span class="sxs-lookup"><span data-stu-id="63cbe-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="63cbe-164">Non rimuovere le righe da questa sezione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-164">Do not remove lines from this section.</span></span> <span data-ttu-id="63cbe-165">Imposta invece la DesiredState su "non gestito" se non vuoi che Configuration Manager modifichi i valori correnti o predefiniti.</span><span class="sxs-lookup"><span data-stu-id="63cbe-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="63cbe-166">Servizi</span><span class="sxs-lookup"><span data-stu-id="63cbe-166">Services</span></span>**  
    <span data-ttu-id="63cbe-167">Le voci in questa sezione controllano l'operazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="63cbe-167">Entries in this section control service operation.</span></span> <span data-ttu-id="63cbe-168">Il file di configurazione predefinito contiene una singola voce per UevAgentService.</span><span class="sxs-lookup"><span data-stu-id="63cbe-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="63cbe-169">L'attributo DesiredState può essere impostato su **in corso** o **interrotto**.</span><span class="sxs-lookup"><span data-stu-id="63cbe-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="63cbe-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="63cbe-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="63cbe-171">Tutte le impostazioni di sincronizzazione delle app di Windows a livello di computer.</span><span class="sxs-lookup"><span data-stu-id="63cbe-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="63cbe-172">Ogni PackageFamilyName elencato in questa sezione può essere assegnato un DesiredState di</span><span class="sxs-lookup"><span data-stu-id="63cbe-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="63cbe-173">**Abilitato** per il roaming delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="63cbe-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="63cbe-174">**Disabilitata** per impedire il roaming delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="63cbe-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="63cbe-175">**Deselezionata** per rimuovere la voce dal controllo UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="63cbe-176">È possibile aggiungere altre righe a questa sezione in base all'elenco delle app di Windows installate che possono essere visualizzate usando il cmdlet di GetAppxPackage.</span><span class="sxs-lookup"><span data-stu-id="63cbe-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="63cbe-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="63cbe-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="63cbe-178">Identico a Windows8AppsComputerPolicy con le impostazioni che eseguono l'override delle impostazioni del computer per un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="63cbe-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="63cbe-179">Modificare il file di configurazione modificando i campi stato e valore desiderati.</span><span class="sxs-lookup"><span data-stu-id="63cbe-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="63cbe-180">Eseguire questo comando in un computer che esegue la console di amministrazione di ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="63cbe-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="63cbe-181">Importare il file CAB usando la console ConfigMgr o l'importazione di PowerShell-CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="63cbe-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="63cbe-182">Aggiornare un elemento di configurazione dei criteri UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="63cbe-183">Modificare il file di configurazione modificando i campi stato e valore desiderati.</span><span class="sxs-lookup"><span data-stu-id="63cbe-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="63cbe-184">Eseguire il comando del passaggio 3 in [creare il primo elemento di configurazione dei criteri UE-V](#create).</span><span class="sxs-lookup"><span data-stu-id="63cbe-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="63cbe-185">Se il nome è stato modificato con il parametro PolicyName, verificare di aver immesso lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="63cbe-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="63cbe-186">Reimportare il file CAB.</span><span class="sxs-lookup"><span data-stu-id="63cbe-186">Reimport the CAB file.</span></span> <span data-ttu-id="63cbe-187">La versione in ConfigMgr verrà aggiornata.</span><span class="sxs-lookup"><span data-stu-id="63cbe-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="63cbe-188">Generare un modello di previsione UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="63cbe-189">I modelli UE-V vengono distribuiti usando una previsione contenente più elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="63cbe-190">Ogni elemento di configurazione contiene gli script di individuazione e correzione necessari per installare un modello UE-V.</span><span class="sxs-lookup"><span data-stu-id="63cbe-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="63cbe-191">L'effettivo modello UE-V è incorporato nello script di correzione per la distribuzione tramite la funzionalità degli elementi di configurazione standard.</span><span class="sxs-lookup"><span data-stu-id="63cbe-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="63cbe-192">Il modello di previsione UE-V viene creato usando lo strumento della riga di comando UevTemplateBaselineGenerator.exe, che contiene questi parametri:</span><span class="sxs-lookup"><span data-stu-id="63cbe-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="63cbe-193">&lt;Codice sito sito&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="63cbe-194">&lt;Nome BaselineName &gt; (facoltativo: impostazione predefinita "linea di base distribuzione modello UE-V" se non presente)</span><span class="sxs-lookup"><span data-stu-id="63cbe-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="63cbe-195">&lt;Descrizione &gt; di BaselineDescription (facoltativo: viene fornita una descrizione se non è presente)</span><span class="sxs-lookup"><span data-stu-id="63cbe-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="63cbe-196">&lt;Cartella modello TemplateFolder UE-V&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="63cbe-197">Registrare l' &lt; elenco dei file di modello separati da virgola&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="63cbe-198">Annullamento della registrazione di un &lt; elenco di modelli separati da virgola&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="63cbe-199">CabFilePath &lt; percorso completo del file CAB previsto per la generazione&gt;</span><span class="sxs-lookup"><span data-stu-id="63cbe-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="63cbe-200">Il risultato è un file CAB previsto pronto per l'importazione in Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="63cbe-201">Se in una data futura si aggiorna o si aggiunge un modello, è possibile rieseguire il comando usando lo stesso nome previsto.</span><span class="sxs-lookup"><span data-stu-id="63cbe-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="63cbe-202">L'importazione del CAB restituisce gli aggiornamenti della versione CI nei modelli modificati.</span><span class="sxs-lookup"><span data-stu-id="63cbe-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="63cbe-203">Creare la prima previsione del modello UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="63cbe-204">Creare un set "Master" di modelli UE-V in una posizione di cartella stabile visibile al computer in cui è in uso la console di amministrazione di ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="63cbe-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="63cbe-205">Quando si aggiungono o si aggiornano i modelli, questa cartella è la posizione in cui vengono estratte per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="63cbe-206">L'elenco iniziale dei modelli può essere copiato da un computer con l'installazione di UE-V.</span><span class="sxs-lookup"><span data-stu-id="63cbe-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="63cbe-207">Il percorso predefinito del modello è C:\\Programmi \\Programmi\\microsoft User Experience Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="63cbe-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="63cbe-208">Creare un file di text.bat in cui è possibile aggiungere il comando generatore di modelli.</span><span class="sxs-lookup"><span data-stu-id="63cbe-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="63cbe-209">Questa opzione è facoltativa, ma rende più semplice la rigenerazione se si salvano i parametri del comando.</span><span class="sxs-lookup"><span data-stu-id="63cbe-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="63cbe-210">Aggiungere il comando e i parametri al file con estensione bat che genererà la linea di base.</span><span class="sxs-lookup"><span data-stu-id="63cbe-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="63cbe-211">L'esempio seguente crea una previsione che distribuisce il blocco note e la calcolatrice:</span><span class="sxs-lookup"><span data-stu-id="63cbe-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="63cbe-212">Eseguire il file bat per creare UevTemplateBaseline.cab pronto per l'importazione in Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="63cbe-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="63cbe-213">Aggiornare una previsione del modello UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="63cbe-214">Il generatore di modelli USA la versione modello per determinare se un modello deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="63cbe-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="63cbe-215">Se si apporta una modifica al modello e si aggiorna la versione, il generatore di previsione confronta il modello nella cartella master con il modello contenuto nel server di ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="63cbe-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="63cbe-216">Se viene rilevata una differenza, vengono aggiornate le versioni di previsione generate e di CI modificate.</span><span class="sxs-lookup"><span data-stu-id="63cbe-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="63cbe-217">Per distribuire un nuovo modello di blocco note, eseguire la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="63cbe-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="63cbe-218">Aggiornare il modello e la versione del modello presenti &lt; nell' &gt; elemento Version del modello.</span><span class="sxs-lookup"><span data-stu-id="63cbe-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="63cbe-219">Copiare il modello nella directory del modello master.</span><span class="sxs-lookup"><span data-stu-id="63cbe-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="63cbe-220">Eseguire il comando nel file con estensione bat creato nel passaggio 3 in [creare la prima previsione del modello UE-V](#create2).</span><span class="sxs-lookup"><span data-stu-id="63cbe-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="63cbe-221">Importare il file CAB generato in ConfigMgr usando la console o Import-CMBaseline di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63cbe-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="63cbe-222">Ottenere il pacchetto di configurazione UE-V</span><span class="sxs-lookup"><span data-stu-id="63cbe-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="63cbe-223">Il pacchetto di configurazione UE-V per Configuration Manager 2012 SP1 o versioni successive può essere scaricato [qui](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="63cbe-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="63cbe-224">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63cbe-224">Related topics</span></span>


[<span data-ttu-id="63cbe-225">Gestire le configurazioni per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="63cbe-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





