---
title: Procedure consigliate MED-V 2.0
description: Procedure consigliate MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826115"
---
# <span data-ttu-id="4a941-103">Procedure consigliate MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="4a941-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="4a941-104">Durante la pianificazione, la distribuzione e la gestione di MED-V nell'organizzazione, è possibile che siano utili le procedure consigliate.</span><span class="sxs-lookup"><span data-stu-id="4a941-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="4a941-105">Configurare la configurazione per la prima volta per l'esecuzione automatica</span><span class="sxs-lookup"><span data-stu-id="4a941-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="4a941-106">Anche se è possibile specificare le impostazioni preferite, è consigliabile creare il file Sysprep. inf in modo che sia possibile eseguire la configurazione per la prima volta in modalità **automatica** .</span><span class="sxs-lookup"><span data-stu-id="4a941-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="4a941-107">In questo modo è necessario specificare tutte le informazioni sulle impostazioni necessarie mentre si continua con la procedura guidata di **Setup Manager** .</span><span class="sxs-lookup"><span data-stu-id="4a941-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="4a941-108">Per altre informazioni su come configurare l'immagine MED-V, vedere [configurazione di un'immagine di PC virtuale Windows per MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="4a941-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="4a941-109">Disabilitare i punti di ripristino nella macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="4a941-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="4a941-110">Prima di creare il pacchetto dell'area di lavoro MED-V, è consigliabile disabilitare i punti di ripristino nella macchina virtuale per evitare che il disco differenze cresca in modo non associato.</span><span class="sxs-lookup"><span data-stu-id="4a941-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="4a941-111">Per altre informazioni, vedere [come disattivare e attivare Ripristino configurazione di sistema in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="4a941-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="4a941-112">Configurare l'immagine MED-V per usare i profili locali</span><span class="sxs-lookup"><span data-stu-id="4a941-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="4a941-113">È consigliabile applicare solo i criteri che hanno senso in un ambiente di compatibilità delle applicazioni per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a941-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="4a941-114">I criteri di personalizzazione desktop, ad esempio, in genere non devono essere applicati e devono essere disabilitati.</span><span class="sxs-lookup"><span data-stu-id="4a941-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="4a941-115">Per altre informazioni su come consentire solo i profili locali, vedere [impostazioni di criteri di gruppo per i profili utente mobili](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="4a941-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="4a941-116">Configurare un aggiornamento delle prestazioni di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="4a941-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="4a941-117">Per impostazione predefinita, i criteri di gruppo vengono scaricati in un computer un byte alla volta.</span><span class="sxs-lookup"><span data-stu-id="4a941-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="4a941-118">Ciò causa ritardi quando MED-V viene aggiunto al dominio.</span><span class="sxs-lookup"><span data-stu-id="4a941-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="4a941-119">Per aumentare le prestazioni dei criteri di gruppo, è consigliabile impostare il valore della chiave del registro di sistema seguente nel registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="4a941-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="4a941-120">Sottochiave del registro di sistema: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="4a941-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="4a941-121">Voce: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="4a941-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="4a941-122">Digitare: DWORD</span><span class="sxs-lookup"><span data-stu-id="4a941-122">Type: DWORD</span></span>

<span data-ttu-id="4a941-123">Valore: 1</span><span class="sxs-lookup"><span data-stu-id="4a941-123">Value: 1</span></span>

### <span data-ttu-id="4a941-124">Distribuire l'avviso legale tramite criteri di gruppo anziché nell'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="4a941-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="4a941-125">Se si vuole che gli utenti finali vedano un contratto di servizio (SLA) prima di accedere a MED-V, è consigliabile applicare lo SLA tramite criteri di gruppo in un secondo momento in modo che l'SLA venga visualizzato all'utente finale al termine della prima configurazione.</span><span class="sxs-lookup"><span data-stu-id="4a941-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="4a941-126">**Attenzione**  Anche se è consigliabile eseguire la configurazione per la prima volta in modalità **automatica** , se si decide di impostare il criterio locale o la voce del registro di sistema per includere un contratto di SLA nell'immagine (disco rigido virtuale), è necessario specificare anche che la configurazione per la prima volta viene eseguita in modalità **assistita** oppure la configurazione iniziale può non riuscire.</span><span class="sxs-lookup"><span data-stu-id="4a941-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="4a941-127">Compattare il disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="4a941-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="4a941-128">È consigliabile compattare il disco rigido virtuale per recuperare spazio su disco vuoto e ridurre le dimensioni del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a941-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="4a941-129">Per altre informazioni su come compattare il disco rigido virtuale, vedere [compattazione del disco rigido virtuale MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="4a941-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="4a941-130">Configurare la macchina virtuale per riavviare l'arresto anomalo della schermata blu</span><span class="sxs-lookup"><span data-stu-id="4a941-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="4a941-131">È consigliabile configurare la macchina virtuale dell'area di lavoro MED-V per riavviare automaticamente quando incontra un arresto anomalo della schermata blu.</span><span class="sxs-lookup"><span data-stu-id="4a941-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="4a941-132">Per configurare questa impostazione nel guest, imposta il valore di riavvio autoboot nella HKEY \ _LOCAL \ _MACHINE chiave \\SYSTEM\\CurrentControlSet\\Control\\CrashControl su "1".</span><span class="sxs-lookup"><span data-stu-id="4a941-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="4a941-133">Per configurare questa impostazione, è anche possibile fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **sistema**.</span><span class="sxs-lookup"><span data-stu-id="4a941-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="4a941-134">Quindi, nell'area **avvio e ripristino** della scheda **Avanzate** , fare clic su **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="4a941-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="4a941-135">Selezionare la casella di controllo **Riavvia automaticamente** e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a941-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="4a941-136">Eseguire il backup dell'immagine MED-V prima di sigillarla</span><span class="sxs-lookup"><span data-stu-id="4a941-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="4a941-137">È consigliabile creare una copia di backup dell'immagine MED-V prima di chiuderla.</span><span class="sxs-lookup"><span data-stu-id="4a941-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="4a941-138">Per altre informazioni sulla chiusura dell'immagine MED-V, vedere [configurazione di un'immagine di PC virtuale Windows per MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="4a941-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="4a941-139">Installare Windows Virtual PC per ultimo durante l'installazione da un file batch</span><span class="sxs-lookup"><span data-stu-id="4a941-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="4a941-140">Quando si installano i componenti MED-V usando un file batch, specificare che Windows Virtual PC e Windows Virtual PC hotfix vengono installati dopo l'agente host MED-V e i file del pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="4a941-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="4a941-141">Questo garantisce che Windows Update non causi interferenze con il processo di installazione richiedendo un riavvio.</span><span class="sxs-lookup"><span data-stu-id="4a941-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="4a941-142">Installare l'area di lavoro MED-V dalla cartella locale</span><span class="sxs-lookup"><span data-stu-id="4a941-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="4a941-143">A causa di problemi che possono verificarsi durante l'installazione di MED-V da un percorso di rete, è consigliabile copiare i file di configurazione dell'area di lavoro MED-V localmente e quindi eseguire setup.exe.</span><span class="sxs-lookup"><span data-stu-id="4a941-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="4a941-144">Gestire il reindirizzamento della stampante in un solo modo</span><span class="sxs-lookup"><span data-stu-id="4a941-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="4a941-145">Se una stampante è installata manualmente nella macchina virtuale guest MED-V e la stessa stampante viene installata in seguito nel computer host, il risultato è che viene installata due volte nel guest.</span><span class="sxs-lookup"><span data-stu-id="4a941-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="4a941-146">Per evitare questa situazione, è consigliabile usare le procedure consigliate per MED-V per gestire il reindirizzamento della stampante in un solo modo: disabilitare il reindirizzamento e installare le stampanti manualmente nell'ospite oppure abilitare il reindirizzamento e non installare le stampanti manualmente nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="4a941-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="4a941-147">Configurare le impostazioni per le patch guest MED-V</span><span class="sxs-lookup"><span data-stu-id="4a941-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="4a941-148">È possibile controllare quando e per quanto tempo la macchina virtuale MED-V si risveglia per ricevere gli aggiornamenti automatici definendo i valori di configurazione rilevanti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4a941-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="4a941-149">Una procedura consigliata per MED-V consiste nell'impostare l'intervallo di riattivazione in modo che corrisponda al momento in cui sono stati pianificati aggiornamenti regolari per le macchine virtuali MED-V.</span><span class="sxs-lookup"><span data-stu-id="4a941-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="4a941-150">Inoltre, ti consigliamo di configurare queste impostazioni per assomigliare al comportamento del computer host.</span><span class="sxs-lookup"><span data-stu-id="4a941-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="4a941-151">Per altre informazioni su come configurare le impostazioni per le patch guest MED-V, vedere [gestire gli aggiornamenti automatici per le aree di lavoro MED-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="4a941-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="4a941-152">Configurare il software antivirus/backup</span><span class="sxs-lookup"><span data-stu-id="4a941-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="4a941-153">Per evitare che l'attività antivirus incida sulle prestazioni del desktop virtuale, è consigliabile escludere i tipi di file della macchina virtuale seguenti da qualsiasi processo antivirus o di backup in esecuzione nel computer host MED-V:</span><span class="sxs-lookup"><span data-stu-id="4a941-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="4a941-154">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="4a941-154">\*.VMC</span></span>

-   <span data-ttu-id="4a941-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="4a941-155">\*.VUD</span></span>

-   <span data-ttu-id="4a941-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="4a941-156">\*.VSV</span></span>

-   <span data-ttu-id="4a941-157">\*. VHD</span><span class="sxs-lookup"><span data-stu-id="4a941-157">\*.VHD</span></span>

## <span data-ttu-id="4a941-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a941-158">Related topics</span></span>


[<span data-ttu-id="4a941-159">Sicurezza e protezione per MED-V</span><span class="sxs-lookup"><span data-stu-id="4a941-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





