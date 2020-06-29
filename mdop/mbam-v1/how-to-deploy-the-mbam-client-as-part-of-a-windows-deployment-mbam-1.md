---
title: Come distribuire il client MBAM come parte di una distribuzione di Windows
description: Come distribuire il client MBAM come parte di una distribuzione di Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824915"
---
# <span data-ttu-id="c1396-103">Come distribuire il client MBAM come parte di una distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="c1396-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="c1396-104">Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c1396-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="c1396-105">Il client BitLocker può essere integrato in un'organizzazione abilitando la gestione e la crittografia di BitLocker nei computer client durante il processo di distribuzione di immagini e Windows.</span><span class="sxs-lookup"><span data-stu-id="c1396-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="c1396-106">Nota</span><span class="sxs-lookup"><span data-stu-id="c1396-106">Note</span></span>**  
<span data-ttu-id="c1396-107">Per esaminare i requisiti di sistema client di MBAM, vedere [configurazioni supportate di mbam 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c1396-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="c1396-108">La crittografia dei computer client con BitLocker durante la fase di imaging iniziale di una distribuzione di Windows può ridurre il sovraccarico amministrativo per l'implementazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1396-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="c1396-109">Questo approccio assicura inoltre che tutti i computer distribuiti abbiano già eseguito BitLocker e siano configurati correttamente.</span><span class="sxs-lookup"><span data-stu-id="c1396-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="c1396-110">Warning</span><span class="sxs-lookup"><span data-stu-id="c1396-110">Warning</span></span>**  
<span data-ttu-id="c1396-111">Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c1396-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="c1396-112">Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="c1396-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="c1396-113">Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat).</span><span class="sxs-lookup"><span data-stu-id="c1396-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="c1396-114">Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="c1396-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="c1396-115">Cambiare il registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="c1396-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="c1396-116">Per crittografare un computer come parte della distribuzione di Windows</span><span class="sxs-lookup"><span data-stu-id="c1396-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="c1396-117">Se l'organizzazione prevede di usare le opzioni di protezione TPM (Trusted Platform Module) o TPM + PIN Protector in BitLocker, è necessario attivare il chip TPM prima della distribuzione iniziale di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1396-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="c1396-118">Quando si attiva il chip TPM, si evita un riavvio più avanti nel processo e si assicura che i chip TPM siano configurati correttamente in base ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c1396-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="c1396-119">È necessario attivare manualmente il chip TPM nel BIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="c1396-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="c1396-120">Per altre informazioni su come configurare il chip TPM, vedere la documentazione del produttore.</span><span class="sxs-lookup"><span data-stu-id="c1396-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="c1396-121">Installare l'agente client MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1396-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="c1396-122">Ti consigliamo di aggiungere il computer a un dominio...</span><span class="sxs-lookup"><span data-stu-id="c1396-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="c1396-123">Se il computer non è collegato a un dominio, la password di ripristino non viene archiviata nel servizio di ripristino di chiave MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1396-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="c1396-124">Per impostazione predefinita, MBAM non consente la crittografia a meno che non sia possibile archiviare la chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c1396-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="c1396-125">Se un computer viene avviato in modalità di ripristino prima che la chiave di ripristino sia archiviata nel server MBAM, è necessario che il computer venga rielaborato.</span><span class="sxs-lookup"><span data-stu-id="c1396-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="c1396-126">Non è disponibile alcun metodo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c1396-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="c1396-127">Aprire un prompt dei comandi come amministratore, arrestare il servizio MBAM e quindi impostare il servizio su **manuale** o **su richiesta**.</span><span class="sxs-lookup"><span data-stu-id="c1396-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="c1396-128">Esegui quindi i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1396-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="c1396-129">NET STOP mbamagent</span><span class="sxs-lookup"><span data-stu-id="c1396-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="c1396-130">sc config mbamagent start = demand</span><span class="sxs-lookup"><span data-stu-id="c1396-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="c1396-131">Impostare le impostazioni del registro di sistema per l'agente di MBAM per ignorare i criteri di gruppo ed eseguire il TPM per la **crittografia solo per i sistemi operativi** , eseguire **Regedit**e quindi importare il modello della chiave del registro di c:\\Programmi Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="c1396-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="c1396-132">In regedit, passa a HKLM\\SOFTWARE\\Microsoft\\MBAM e configura le impostazioni elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c1396-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="c1396-133">Voce del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c1396-133">Registry entry</span></span>

    <span data-ttu-id="c1396-134">Impostazioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="c1396-134">Configuration settings</span></span>

    <span data-ttu-id="c1396-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="c1396-135">DeploymentTime</span></span>

    <span data-ttu-id="c1396-136">0 = DISATTIVATO</span><span class="sxs-lookup"><span data-stu-id="c1396-136">0 = OFF</span></span>

    <span data-ttu-id="c1396-137">1 = usare le impostazioni dei criteri per il tempo di distribuzione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1396-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="c1396-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="c1396-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="c1396-139">0 = non usare l'escrow Key (le due voci del registro di sistema successive non sono necessarie in questo caso).</span><span class="sxs-lookup"><span data-stu-id="c1396-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="c1396-140">1 = usare l'escrow Key nel sistema di recupero chiavi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1396-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="c1396-141">Consigliato: il computer deve essere in grado di comunicare con il servizio di recupero chiavi.</span><span class="sxs-lookup"><span data-stu-id="c1396-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="c1396-142">Verificare che il computer sia in grado di comunicare con il servizio prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="c1396-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="c1396-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="c1396-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="c1396-144">0 = solo chiave di ripristino upload</span><span class="sxs-lookup"><span data-stu-id="c1396-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="c1396-145">1 = carica chiave di ripristino e pacchetto di recupero tasti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1396-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="c1396-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="c1396-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="c1396-147">Imposta questo valore sull'URL del server Web di ripristino della chiave.</span><span class="sxs-lookup"><span data-stu-id="c1396-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="c1396-148">Esempio: http:// &lt; nome computer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="c1396-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="c1396-149">L'agente MBAM riavvia il sistema durante la distribuzione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="c1396-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="c1396-150">Quando si è pronti per il riavvio, eseguire il comando seguente al prompt dei comandi come amministratore:</span><span class="sxs-lookup"><span data-stu-id="c1396-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="c1396-151">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="c1396-151">net start mbamagent</span></span>**

8. <span data-ttu-id="c1396-152">Quando il computer viene riavviato e il BIOS chiede di accettare una modifica del TPM, accettare la modifica.</span><span class="sxs-lookup"><span data-stu-id="c1396-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="c1396-153">Durante il processo di imaging del sistema operativo client Windows, quando si è pronti per avviare la crittografia, riavviare il servizio di MBAM Agent.</span><span class="sxs-lookup"><span data-stu-id="c1396-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="c1396-154">Per impostare l'avvio **automatico**, aprire un prompt dei comandi come amministratore ed eseguire i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1396-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="c1396-155">sc config mbamagent Start = automatico</span><span class="sxs-lookup"><span data-stu-id="c1396-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="c1396-156">NET Start mbamagent</span><span class="sxs-lookup"><span data-stu-id="c1396-156">net start mbamagent</span></span>**

10. <span data-ttu-id="c1396-157">Rimuovere i valori di bypass del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c1396-157">Remove the bypass registry values.</span></span> <span data-ttu-id="c1396-158">A tale scopo, eseguire regedit, passare alla voce del registro di sistema HKLM\\SOFTWARE\\Microsoft, fare clic con il pulsante destro del mouse sul nodo **mbam** e quindi scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="c1396-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="c1396-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1396-159">Related topics</span></span>


[<span data-ttu-id="c1396-160">Distribuzione del client MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c1396-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









