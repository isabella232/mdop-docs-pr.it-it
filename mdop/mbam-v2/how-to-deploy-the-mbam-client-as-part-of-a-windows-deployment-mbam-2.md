---
title: Come distribuire il client MBAM come parte di una distribuzione di Windows
description: Come distribuire il client MBAM come parte di una distribuzione di Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824625"
---
# <span data-ttu-id="c5f99-103">Come distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="c5f99-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="c5f99-104">Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c5f99-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="c5f99-105">Se i computer con un chip TPM (Trusted Platform Module), il client BitLocker può essere integrato in un'organizzazione abilitando la gestione e la crittografia di BitLocker nei computer client come parte del processo di distribuzione di immagini e Windows.</span><span class="sxs-lookup"><span data-stu-id="c5f99-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="c5f99-106">Nota</span><span class="sxs-lookup"><span data-stu-id="c5f99-106">Note</span></span>**  
<span data-ttu-id="c5f99-107">Per esaminare i requisiti di sistema per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c5f99-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="c5f99-108">La crittografia dei computer client con BitLocker durante la fase di imaging iniziale di una distribuzione di Windows può ridurre il sovraccarico amministrativo necessario per l'implementazione di MBAM in un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c5f99-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="c5f99-109">Assicura inoltre che tutti i computer distribuiti abbiano già eseguito BitLocker e siano configurati correttamente.</span><span class="sxs-lookup"><span data-stu-id="c5f99-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="c5f99-110">Nota</span><span class="sxs-lookup"><span data-stu-id="c5f99-110">Note</span></span>**  
<span data-ttu-id="c5f99-111">La procedura descritta in questo argomento descrive la modifica del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="c5f99-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="c5f99-112">L'uso errato dell'editor del registro di sistema può causare seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="c5f99-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="c5f99-113">Microsoft non può garantire che i problemi causati dall'uso errato dell'editor del registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="c5f99-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="c5f99-114">Usare l'editor del registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="c5f99-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="c5f99-115">Per crittografare un computer come parte della distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="c5f99-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="c5f99-116">Se l'organizzazione prevede di usare le opzioni di protezione TPM (Trusted Platform Module) o TPM + PIN Protector in BitLocker, è necessario attivare il chip TPM prima della distribuzione iniziale di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c5f99-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="c5f99-117">Quando si attiva il chip TPM, si evita un riavvio più avanti nel processo e si assicura che i chip TPM siano configurati correttamente in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c5f99-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="c5f99-118">È necessario attivare manualmente il chip TPM nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="c5f99-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="c5f99-119">Nota</span><span class="sxs-lookup"><span data-stu-id="c5f99-119">Note</span></span>**  
    <span data-ttu-id="c5f99-120">Alcuni fornitori includono gli strumenti per attivare e attivare il chip TPM nel BIOS dall'interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c5f99-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="c5f99-121">Per altre informazioni su come configurare il chip TPM, vedere la documentazione del produttore.</span><span class="sxs-lookup"><span data-stu-id="c5f99-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="c5f99-122">Installare l'agente client di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c5f99-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="c5f99-123">Aggiungere il computer a un dominio (scelta consigliata).</span><span class="sxs-lookup"><span data-stu-id="c5f99-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="c5f99-124">Se il computer non è collegato al dominio, la password di ripristino non viene archiviata nel servizio di ripristino di chiave di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c5f99-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="c5f99-125">Per impostazione predefinita, MBAM non consente la crittografia a meno che non sia possibile archiviare la chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c5f99-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="c5f99-126">Se un computer viene avviato in modalità di ripristino prima che la chiave di ripristino sia archiviata nel server MBAM, è necessario che il computer venga rielaborato.</span><span class="sxs-lookup"><span data-stu-id="c5f99-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="c5f99-127">Non è disponibile alcun metodo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c5f99-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="c5f99-128">Eseguire il prompt dei comandi come amministratore, arrestare il servizio MBAM e quindi impostare il servizio su **manuale** o **su richiesta**e quindi iniziare digitando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5f99-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="c5f99-129">NET STOP mbamagent</span><span class="sxs-lookup"><span data-stu-id="c5f99-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="c5f99-130">sc config mbamagent start = demand</span><span class="sxs-lookup"><span data-stu-id="c5f99-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="c5f99-131">Impostare le impostazioni del registro di sistema per l'agente MBAM per ignorare i criteri di gruppo ed eseguire il TPM solo per la **crittografia dei sistemi operativi** eseguendo **Regedit**e quindi importando il modello di chiave del registro di c:\\Programmi Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="c5f99-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="c5f99-132">In regedit, passa a HKLM\\SOFTWARE\\Microsoft\\MBAM e configura le impostazioni elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c5f99-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="c5f99-133">Voce del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c5f99-133">Registry entry</span></span>

    <span data-ttu-id="c5f99-134">Impostazioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="c5f99-134">Configuration settings</span></span>

    <span data-ttu-id="c5f99-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="c5f99-135">DeploymentTime</span></span>

    <span data-ttu-id="c5f99-136">0 = DISATTIVATO</span><span class="sxs-lookup"><span data-stu-id="c5f99-136">0 = OFF</span></span>

    <span data-ttu-id="c5f99-137">1 = usare le impostazioni dei criteri per il tempo di distribuzione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5f99-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="c5f99-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="c5f99-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="c5f99-139">0 = non usare l'escrow Key (le due voci del registro di sistema successive non sono necessarie in questo caso)</span><span class="sxs-lookup"><span data-stu-id="c5f99-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="c5f99-140">1 = usare l'escrow Key nel sistema di recupero chiavi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5f99-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="c5f99-141">Consigliato: il computer deve essere in grado di comunicare con il servizio di recupero chiavi.</span><span class="sxs-lookup"><span data-stu-id="c5f99-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="c5f99-142">Verificare che il computer sia in grado di comunicare con il servizio prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="c5f99-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="c5f99-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="c5f99-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="c5f99-144">0 = carica solo il tasto di ripristino</span><span class="sxs-lookup"><span data-stu-id="c5f99-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="c5f99-145">1 = carica il tasto di ripristino e il pacchetto di ripristino della chiave (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5f99-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="c5f99-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="c5f99-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="c5f99-147">Imposta questo valore sull'URL per il server Web di ripristino chiave, ad esempio http:// &lt; nome computer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="c5f99-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="c5f99-148">L'agente MBAM riavvia il sistema durante la distribuzione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="c5f99-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="c5f99-149">Quando si è pronti per il riavvio, eseguire il comando seguente al prompt dei comandi come amministratore:</span><span class="sxs-lookup"><span data-stu-id="c5f99-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="c5f99-150">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="c5f99-150">net start mbamagent</span></span>**

8. <span data-ttu-id="c5f99-151">Quando il computer viene riavviato e il BIOS chiede di accettare una modifica del TPM, accettare la modifica.</span><span class="sxs-lookup"><span data-stu-id="c5f99-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="c5f99-152">Durante il processo di imaging del sistema operativo client Windows, quando si è pronti per avviare la crittografia, riavviare il servizio di MBAM Agent e impostare Start su **automatico** eseguendo un prompt dei comandi come amministratore e digitando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5f99-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="c5f99-153">sc config mbamagent Start = automatico</span><span class="sxs-lookup"><span data-stu-id="c5f99-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="c5f99-154">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="c5f99-154">net start mbamagent</span></span>**

10. <span data-ttu-id="c5f99-155">Rimuovere i valori di bypass del registro di sistema eseguendo regedit e passando alla voce del registro di sistema HKLM\\SOFTWARE\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5f99-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="c5f99-156">Per eliminare il nodo **mbam** , fare clic con il pulsante destro del mouse sul nodo e scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="c5f99-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="c5f99-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5f99-157">Related topics</span></span>


[<span data-ttu-id="c5f99-158">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c5f99-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









