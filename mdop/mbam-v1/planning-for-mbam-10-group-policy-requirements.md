---
title: Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0
description: Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804227"
---
# <span data-ttu-id="c6b64-103">Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c6b64-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="c6b64-104">La gestione dei client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker richiede l'applicazione di impostazioni di criteri di gruppo personalizzate.</span><span class="sxs-lookup"><span data-stu-id="c6b64-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="c6b64-105">In questo argomento vengono illustrate le opzioni dei criteri disponibili per l'oggetto Criteri di gruppo quando si usa MBAM per gestire la crittografia unità BitLocker nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c6b64-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="c6b64-106">Importante</span><span class="sxs-lookup"><span data-stu-id="c6b64-106">Important</span></span>**  
<span data-ttu-id="c6b64-107">MBAM non usa le impostazioni GPO predefinite per la crittografia unità BitLocker di Windows.</span><span class="sxs-lookup"><span data-stu-id="c6b64-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="c6b64-108">Se le impostazioni predefinite sono abilitate, possono causare un comportamento conflittuale.</span><span class="sxs-lookup"><span data-stu-id="c6b64-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="c6b64-109">Per abilitare MBAM per la gestione di BitLocker, è necessario definire le impostazioni dei criteri GPO dopo l'installazione del modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c6b64-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="c6b64-110">Dopo aver installato il modello dei criteri di gruppo di MBAM, è possibile visualizzare e modificare le impostazioni dei criteri GPO personalizzati di MBAM che consentono a MBAM di gestire la crittografia BitLocker dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c6b64-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="c6b64-111">Il modello di criteri di gruppo di MBAM deve essere installato in un computer in grado di eseguire la console Gestione criteri di gruppo o la tecnologia MDOP avanzata per la gestione dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="c6b64-112">Per modificare quindi il GPO applicabile, aprire GPMC o Advanced Group Policy Management e quindi passare al nodo GPO seguente: **Configurazione computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="c6b64-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="c6b64-113">Il nodo GPO MDOP MBAM (BitLocker Management) contiene rispettivamente quattro impostazioni di criteri globali e quattro nodi di impostazione GPO figlio.</span><span class="sxs-lookup"><span data-stu-id="c6b64-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="c6b64-114">Le quattro impostazioni dei criteri globali del GPO sono: gestione client, unità fisse, unità del sistema operativo e unità rimovibile.</span><span class="sxs-lookup"><span data-stu-id="c6b64-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="c6b64-115">Le sezioni seguenti includono definizioni di criteri e impostazioni dei criteri suggerite per pianificare i requisiti per l'impostazione di criteri GPO di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c6b64-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="c6b64-116">Nota</span><span class="sxs-lookup"><span data-stu-id="c6b64-116">Note</span></span>**  
<span data-ttu-id="c6b64-117">Per altre informazioni sulla configurazione delle impostazioni GPO minime consigliate per consentire a MBAM di gestire la crittografia BitLocker, vedere [come modificare le impostazioni del GPO di mbam 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c6b64-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="c6b64-118">Definizioni di criteri globali</span><span class="sxs-lookup"><span data-stu-id="c6b64-118">Global policy definitions</span></span>


<span data-ttu-id="c6b64-119">Questa sezione descrive le definizioni dei criteri globali di mbam, che possono essere trovate nel nodo GPO seguente: **configurazione di computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="c6b64-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6b64-120">Nome criterio</span><span class="sxs-lookup"><span data-stu-id="c6b64-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="c6b64-121">Panoramica e impostazione di criteri suggeriti</span><span class="sxs-lookup"><span data-stu-id="c6b64-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-122">Scegliere il metodo di crittografia unità e la forza di cifratura</span><span class="sxs-lookup"><span data-stu-id="c6b64-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-123">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-124">Configura questo criterio per usare un metodo di crittografia specifico e un livello di codifica.</span><span class="sxs-lookup"><span data-stu-id="c6b64-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="c6b64-125">Quando questo criterio non è configurato, BitLocker usa il metodo di crittografia predefinito di AES 128 bit con il diffusore o il metodo di crittografia specificato dallo script di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c6b64-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-126">Impedire la sovrascrittura della memoria al riavvio</span><span class="sxs-lookup"><span data-stu-id="c6b64-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-127">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-128">Configurare questo criterio per migliorare le prestazioni di riavvio senza sovrascrivere i segreti di BitLocker in memoria al riavvio.</span><span class="sxs-lookup"><span data-stu-id="c6b64-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="c6b64-129">Quando questo criterio non è configurato, i segreti di BitLocker vengono rimossi dalla memoria quando il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="c6b64-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-130">Convalidare la regola di utilizzo del certificato smart card</span><span class="sxs-lookup"><span data-stu-id="c6b64-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-131">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-132">Configurare questo criterio per l'uso della protezione BitLocker basata su certificati smartcard.</span><span class="sxs-lookup"><span data-stu-id="c6b64-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="c6b64-133">Quando questo criterio non è configurato, per specificare un certificato viene usato un identificatore di oggetto predefinito 1.3.6.1.4.1.311.67.1.1.</span><span class="sxs-lookup"><span data-stu-id="c6b64-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-134">Specificare gli identificatori univoci per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="c6b64-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-135">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-136">Configurare questo criterio per l'uso di un agente di recupero dati basato su certificati o del lettore BitLocker to go.</span><span class="sxs-lookup"><span data-stu-id="c6b64-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="c6b64-137">Quando questo criterio non è configurato, il <strong> campo di identificazione </strong> non viene usato.</span><span class="sxs-lookup"><span data-stu-id="c6b64-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="c6b64-138">Se la società richiede misure di sicurezza più elevate, è consigliabile configurare <strong> il </strong> campo di identificazione per assicurarsi che tutti i dispositivi USB dispongano di questo set di campi e che siano allineati con questa impostazione di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c6b64-139">Definizioni dei criteri di gestione client</span><span class="sxs-lookup"><span data-stu-id="c6b64-139">Client Management policy definitions</span></span>


<span data-ttu-id="c6b64-140">In questa sezione vengono illustrate le definizioni dei criteri di gestione dei client per mbam, disponibile nel nodo GPO seguente: **configurazione di computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **Client Management**.</span><span class="sxs-lookup"><span data-stu-id="c6b64-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6b64-141">Nome criterio</span><span class="sxs-lookup"><span data-stu-id="c6b64-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="c6b64-142">Panoramica e impostazioni dei criteri suggerite</span><span class="sxs-lookup"><span data-stu-id="c6b64-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-143">Configurare i servizi MBAM</span><span class="sxs-lookup"><span data-stu-id="c6b64-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-144">Configurazione consigliata: <strong> abilitata</span><span class="sxs-lookup"><span data-stu-id="c6b64-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="c6b64-145">Endpoint del servizio di recupero e hardware di MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="c6b64-146">Questa è la prima impostazione di criteri che è necessario configurare per abilitare la gestione della crittografia BitLocker client di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c6b64-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="c6b64-147">Per questa impostazione, immettere la posizione dell'endpoint simile all'esempio seguente: <strong> http:// </strong><em> &lt; mbam Administration e Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port il servizio Web è associato a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="c6b64-148">Selezionare informazioni di ripristino di BitLocker da archiviare </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="c6b64-149">Questa impostazione dei criteri consente di configurare il servizio di recupero chiavi per eseguire il backup delle informazioni di ripristino di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="c6b64-150">Consente inoltre di configurare il servizio di segnalazione dello stato per la raccolta dei report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="c6b64-151">Il criterio fornisce un metodo amministrativo per il recupero dei dati crittografati da BitLocker per evitare perdite di dati dovute alla mancanza di informazioni chiave.</span><span class="sxs-lookup"><span data-stu-id="c6b64-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="c6b64-152">Il rapporto di stato e l'attività di ripristino delle chiavi verranno inviate automaticamente e silenziosamente alla posizione del server di report configurata.</span><span class="sxs-lookup"><span data-stu-id="c6b64-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="c6b64-153">Se non si configura o se si disabilita questa impostazione, le informazioni relative al ripristino della chiave non verranno salvate e il rapporto di stato e l'attività di ripristino delle chiavi non verranno segnalate al server.</span><span class="sxs-lookup"><span data-stu-id="c6b64-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="c6b64-154">Quando questa impostazione è impostata su <strong> password di ripristino e pacchetto di tasti </strong> , la password di ripristino e il pacchetto di chiave verranno automaticamente e silenziosamente configurati nel percorso del server di recupero chiavi configurato.</span><span class="sxs-lookup"><span data-stu-id="c6b64-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="c6b64-155">Immettere il client che controlla la frequenza dello stato in minuti </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="c6b64-156">Questa impostazione del criterio gestisce la frequenza con cui il client controlla i criteri di protezione di BitLocker e lo stato nel computer client.</span><span class="sxs-lookup"><span data-stu-id="c6b64-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="c6b64-157">Questo criterio gestisce anche la frequenza con cui lo stato di conformità del client viene salvato nel server.</span><span class="sxs-lookup"><span data-stu-id="c6b64-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="c6b64-158">Il client controlla i criteri e lo stato di protezione di BitLocker nel computer client e esegue anche il backup della chiave di ripristino client in corrispondenza della frequenza configurata.</span><span class="sxs-lookup"><span data-stu-id="c6b64-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="c6b64-159">Imposta questa frequenza in base al requisito stabilito dalla tua società per verificare con quante volte si controlla lo stato di conformità del computer e con quale frequenza eseguire il backup della chiave di ripristino del client.</span><span class="sxs-lookup"><span data-stu-id="c6b64-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="c6b64-160">Endpoint del servizio Segnalazione stato di MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="c6b64-161">Questa è la seconda impostazione di criteri che è necessario configurare per abilitare la gestione della crittografia BitLocker client di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c6b64-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="c6b64-162">Per questa impostazione, immettere la posizione dell'endpoint usando l'esempio seguente: <strong> http:// </strong><em> &lt; mbam Administration and Monitoring Server Name &gt; </em><strong> : </strong><em> &lt; Port il servizio Web è associato a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.</span><span class="sxs-lookup"><span data-stu-id="c6b64-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="c6b64-163">SVC </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-164">Consentire il controllo della compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="c6b64-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-165">Configurazione consigliata: <strong> abilitata</span><span class="sxs-lookup"><span data-stu-id="c6b64-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="c6b64-166">Questa impostazione consente di gestire la verifica della compatibilità hardware prima di abilitare la protezione BitLocker sulle unità dei computer client MBAM.</span><span class="sxs-lookup"><span data-stu-id="c6b64-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="c6b64-167">È consigliabile abilitare questa opzione per i criteri se l'organizzazione ha hardware o computer meno recenti che non supportano il TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="c6b64-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="c6b64-168">Se uno di questi criteri è vero, abilitare la verifica della compatibilità hardware per verificare che MBAM venga applicato solo ai modelli di computer che supportano BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="c6b64-169">Se tutti i computer dell'organizzazione supportano BitLocker, non è necessario distribuire la compatibilità hardware ed è possibile impostare questo criterio su <strong> non configurato </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="c6b64-170">Se si abilita questa impostazione, il modello del computer viene convalidato con l'elenco compatibilità hardware una volta ogni 24 ore, prima che il criterio consenta la protezione di BitLocker in un'unità del computer.</span><span class="sxs-lookup"><span data-stu-id="c6b64-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c6b64-171">Nota</span><span class="sxs-lookup"><span data-stu-id="c6b64-171">Note</span></span></strong><br/><p><span data-ttu-id="c6b64-172">Prima di abilitare questa impostazione, verificare di avere configurato l'impostazione dell' <strong> endpoint di servizio hardware e ripristino </strong> di mbam nelle <strong> Opzioni di configurazione dei criteri di servizi mbam </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="c6b64-173">Se si disattiva o non si configura l'impostazione di questo criterio, il modello di computer non viene convalidato rispetto all'elenco compatibilità hardware.</span><span class="sxs-lookup"><span data-stu-id="c6b64-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-174">Configurare i criteri di esenzione dall'utente</span><span class="sxs-lookup"><span data-stu-id="c6b64-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-175">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-176">Questa impostazione dei criteri consente di configurare un indirizzo di sito Web, un indirizzo di posta elettronica o un numero di telefono che indicherà a un utente di richiedere un'esenzione dalla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="c6b64-177">Se si abilita questa impostazione per i criteri e si specifica un indirizzo di sito Web, un indirizzo di posta elettronica o un numero di telefono, gli utenti vedranno una finestra di dialogo con le istruzioni su come richiedere un'esenzione dalla protezione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="c6b64-178">Per altre informazioni su come abilitare le esenzioni per la crittografia BitLocker per gli utenti, vedere <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> come gestire le esenzioni di crittografia di BitLocker dell'utente </a> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="c6b64-179">Se si disattiva o non si configura l'impostazione di questo criterio, le istruzioni su come applicare una richiesta di esenzione non verranno presentate agli utenti.</span><span class="sxs-lookup"><span data-stu-id="c6b64-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c6b64-180">Nota</span><span class="sxs-lookup"><span data-stu-id="c6b64-180">Note</span></span></strong><br/><p><span data-ttu-id="c6b64-181">L'esenzione dall'utente è gestita per utente, non per computer.</span><span class="sxs-lookup"><span data-stu-id="c6b64-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="c6b64-182">Se più utenti accedono allo stesso computer e un utente non è esonerato, il computer verrà crittografato.</span><span class="sxs-lookup"><span data-stu-id="c6b64-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c6b64-183">Definizioni di criteri di unità fisse</span><span class="sxs-lookup"><span data-stu-id="c6b64-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="c6b64-184">Questa sezione descrive le definizioni dei criteri di unità fisse per mbam, che si trova nel nodo GPO seguente: **configurazione di computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (Gestione BitLocker)**  \\  **unità fissa**.</span><span class="sxs-lookup"><span data-stu-id="c6b64-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6b64-185">Nome criterio</span><span class="sxs-lookup"><span data-stu-id="c6b64-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="c6b64-186">Panoramica e impostazione di criteri suggeriti</span><span class="sxs-lookup"><span data-stu-id="c6b64-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-187">Impostazioni di crittografia unità dati fisse</span><span class="sxs-lookup"><span data-stu-id="c6b64-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-188">Configurazione consigliata: <strong> abilitata </strong> e selezionare la <strong> casella di controllo Attiva unità dati fisse di sblocco automatico </strong> se è necessario crittografare il volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="c6b64-189">Questa impostazione consente di controllare se crittografare o meno le unità fisse.</span><span class="sxs-lookup"><span data-stu-id="c6b64-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="c6b64-190">Quando si Abilita questo criterio, non disabilitare la <strong> configurazione dell'uso della password per i criteri delle unità dati fisse </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="c6b64-191">Se la <strong> casella di controllo Abilita l'auto-sblocco dei dati fissi </strong> è selezionata, il volume del sistema operativo deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="c6b64-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="c6b64-192">Se si abilita questa impostazione, gli utenti devono inserire tutte le unità fisse in protezione BitLocker, in modo da crittografare le unità.</span><span class="sxs-lookup"><span data-stu-id="c6b64-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="c6b64-193">Se non si configura questo criterio o se si disabilita questo criterio, gli utenti non sono tenuti a inserire unità fisse in protezione BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="c6b64-194">Se si disattiva questo criterio, l'agente MBAM decrittografa eventuali unità fisse crittografate.</span><span class="sxs-lookup"><span data-stu-id="c6b64-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="c6b64-195">Se non è necessario crittografare il volume del sistema operativo, deselezionare la <strong> casella di controllo attiva l'unità dati fissa di sblocco automatico </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-196">Negare l'autorizzazione "Scrivi" alle unità fisse che non sono protette da BitLocker</span><span class="sxs-lookup"><span data-stu-id="c6b64-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-197">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-198">Questa impostazione dei criteri determina se la protezione di BitLocker è necessaria per le unità fisse in un computer in modo che siano scrivibili.</span><span class="sxs-lookup"><span data-stu-id="c6b64-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="c6b64-199">Questa impostazione dei criteri viene applicata quando si attiva BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="c6b64-200">Quando il criterio non è configurato, tutte le unità fisse nel computer vengono montate con le autorizzazioni di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6b64-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-201">Consentire l'accesso a dischi fissi protetti da BitLocker da versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="c6b64-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-202">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-203">Abilitare questo criterio per sbloccare e visualizzare le unità fisse formattate con il file system FAT (file allocation table) nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="c6b64-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="c6b64-204">Questi sistemi operativi hanno le autorizzazioni di sola lettura per le unità protette da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="c6b64-205">Quando il criterio è disabilitato, le unità fisse formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="c6b64-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-206">Configurare l'uso della password per le unità fisse</span><span class="sxs-lookup"><span data-stu-id="c6b64-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-207">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-208">Abilitare questo criterio per configurare la protezione con password in unità fisse.</span><span class="sxs-lookup"><span data-stu-id="c6b64-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="c6b64-209">Quando il criterio non è configurato, le password saranno supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e richiedono solo otto caratteri.</span><span class="sxs-lookup"><span data-stu-id="c6b64-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="c6b64-210">Per una maggiore sicurezza, abilitare questo criterio e selezionare <strong> Richiedi password per l'unità dati fissa </strong> , selezionare <strong> Richiedi complessità password </strong> e impostare la <strong> lunghezza minima della password desiderata </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-211">Scegliere il modo in cui possono essere recuperati i dischi fissi protetti da BitLocker</span><span class="sxs-lookup"><span data-stu-id="c6b64-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-212">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-213">Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="c6b64-214">Quando questo criterio non è configurato, l'agente di recupero dati di BitLocker è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="c6b64-215">MBAM non richiede le informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c6b64-216">Definizioni dei criteri unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6b64-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="c6b64-217">Questa sezione descrive le definizioni dei criteri di unità del sistema operativo per mbam, disponibile nel nodo GPO seguente: **configurazione del computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **drive del sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="c6b64-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6b64-218">Nome criterio</span><span class="sxs-lookup"><span data-stu-id="c6b64-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="c6b64-219">Panoramica e impostazione di criteri suggeriti</span><span class="sxs-lookup"><span data-stu-id="c6b64-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-220">Impostazioni di crittografia unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6b64-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-221">Configurazione consigliata: <strong> abilitata</span><span class="sxs-lookup"><span data-stu-id="c6b64-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="c6b64-222">Questa impostazione dei criteri determina se l'unità del sistema operativo verrà crittografata.</span><span class="sxs-lookup"><span data-stu-id="c6b64-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="c6b64-223">Configurare questo criterio per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6b64-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c6b64-224">Applicare la protezione BitLocker per l'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="c6b64-225">Configurare l'utilizzo del PIN per usare un PIN TPM (Trusted Platform Module) per la protezione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="c6b64-226">Configurare i pin di avvio avanzati per consentire caratteri come lettere maiuscole e minuscole e numeri.</span><span class="sxs-lookup"><span data-stu-id="c6b64-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="c6b64-227">MBAM non supporta l'uso di simboli e spazi per i PIN avanzati, anche se BitLocker supporta simboli e spazi.</span><span class="sxs-lookup"><span data-stu-id="c6b64-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="c6b64-228">Se si abilita questa impostazione, è necessario che gli utenti proteggano l'unità del sistema operativo tramite BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="c6b64-229">Se non si configura o se si disattiva l'impostazione, gli utenti non sono tenuti a proteggere l'unità del sistema operativo tramite BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="c6b64-230">Se si disattiva questo criterio, l'agente MBAM decrittografa il volume del sistema operativo se è crittografato.</span><span class="sxs-lookup"><span data-stu-id="c6b64-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="c6b64-231">Quando è abilitata, questa impostazione del criterio richiede agli utenti di proteggere il sistema operativo tramite la protezione BitLocker e l'unità è crittografata.</span><span class="sxs-lookup"><span data-stu-id="c6b64-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="c6b64-232">In base ai requisiti di crittografia, è possibile selezionare il metodo di protezione per l'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c6b64-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="c6b64-233">Per i requisiti di sicurezza più elevati, usare TPM + PIN, consentire i PIN avanzati e impostare la lunghezza minima del PIN su otto caratteri.</span><span class="sxs-lookup"><span data-stu-id="c6b64-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="c6b64-234">Quando questo criterio è abilitato con TPM + PIN Protector, è possibile considerare la possibilità di disabilitare i criteri seguenti in <strong> </strong>  /  <strong> </strong>  /  <strong> Impostazioni Sleep di Power Management </strong> :</span><span class="sxs-lookup"><span data-stu-id="c6b64-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="c6b64-235">Consentire stati di standby (S1-S3) durante il sonno (collegato)</span><span class="sxs-lookup"><span data-stu-id="c6b64-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="c6b64-236">Consentire stati di standby (S1-S3) durante il sonno (sulla batteria)</span><span class="sxs-lookup"><span data-stu-id="c6b64-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-237">Configurare il profilo di convalida della piattaforma TPM</span><span class="sxs-lookup"><span data-stu-id="c6b64-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-238">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-239">Questa impostazione consente di configurare il modo in cui l'hardware di sicurezza TPM in un computer protegge la chiave di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="c6b64-240">Questa impostazione non si applica se il computer non ha un TPM compatibile o se BitLocker ha già abilitato la protezione TPM.</span><span class="sxs-lookup"><span data-stu-id="c6b64-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="c6b64-241">Quando questo criterio non è configurato, il TPM usa il profilo di convalida della piattaforma predefinito o il profilo di convalida della piattaforma specificato dallo script di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c6b64-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-242">Scegliere come recuperare le unità del sistema operativo protette da BitLocker</span><span class="sxs-lookup"><span data-stu-id="c6b64-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-243">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-244">Configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="c6b64-245">Quando questo criterio non è configurato, l'agente di recupero dati è consentita e le informazioni di ripristino non vengono sostenute in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="c6b64-246">L'operazione MBAM non richiede le informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c6b64-247">Definizioni dei criteri unità rimovibili</span><span class="sxs-lookup"><span data-stu-id="c6b64-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="c6b64-248">Questa sezione descrive le definizioni dei criteri di unità rimovibili per mbam, disponibile nel nodo GPO seguente: **configurazione del computer** \\ **modelli amministrativi**di \\ **Windows Components** \\ **MDOP mbam (BitLocker Management)**  \\  **drive rimovibile**.</span><span class="sxs-lookup"><span data-stu-id="c6b64-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c6b64-249">Nome criterio</span><span class="sxs-lookup"><span data-stu-id="c6b64-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="c6b64-250">Panoramica e impostazione di criteri suggeriti</span><span class="sxs-lookup"><span data-stu-id="c6b64-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-251">Controllare l'uso di BitLocker su unità rimovibili</span><span class="sxs-lookup"><span data-stu-id="c6b64-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-252">Configurazione consigliata: <strong> abilitata</span><span class="sxs-lookup"><span data-stu-id="c6b64-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="c6b64-253">Questo criterio Controlla l'uso di BitLocker su unità dati rimovibili.</span><span class="sxs-lookup"><span data-stu-id="c6b64-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="c6b64-254">Abilitare l' <strong> opzione Consenti agli utenti di applicare la protezione BitLocker su unità dati rimovibili </strong> per consentire agli utenti di eseguire la configurazione guidata di BitLocker in un'unità dati rimovibile.</span><span class="sxs-lookup"><span data-stu-id="c6b64-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="c6b64-255">Consentire agli <strong> utenti di sospendere e decrittografare l'opzione BitLocker in unità dati rimovibili </strong> per consentire agli utenti di rimuovere la crittografia unità BitLocker dall'unità o di sospendere la crittografia durante l'esecuzione della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="c6b64-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="c6b64-256">Quando questo criterio è abilitato e l' <strong> opzione Consenti agli utenti di applicare la protezione BitLocker su unità dati rimovibili </strong> è selezionata, il client mbam Salva le informazioni di ripristino sulle unità rimovibili nel server di ripristino di mbam Key e consente agli utenti di recuperare l'unità se la password è perduta.</span><span class="sxs-lookup"><span data-stu-id="c6b64-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-257">Rifiutare le autorizzazioni di scrittura per le unità rimovibili non protette da BitLocker</span><span class="sxs-lookup"><span data-stu-id="c6b64-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-258">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-259">Abilitare questo criterio per consentire le autorizzazioni di sola scrittura per le unità protette da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="c6b64-260">Quando questo criterio è abilitato, tutte le unità dati rimovibili nel computer richiedono la crittografia prima che siano consentite le autorizzazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6b64-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-261">Consentire l'accesso alle unità rimovibili protette da BitLocker dalle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="c6b64-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-262">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-263">Abilitare questo criterio per sbloccare e visualizzare le unità fisse formattate con il file System (FAT) nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="c6b64-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="c6b64-264">Questi sistemi operativi hanno le autorizzazioni di sola lettura per le unità protette da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6b64-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="c6b64-265">Quando il criterio è disabilitato, le unità rimovibili formattate con il file system FAT non possono essere sbloccate e il loro contenuto non può essere visualizzato nei computer che eseguono Windows Server 2008, Windows Vista, Windows XP con SP3 o Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="c6b64-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6b64-266">Configurare l'uso della password per le unità dati rimovibili</span><span class="sxs-lookup"><span data-stu-id="c6b64-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-267">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-268">Abilitare questo criterio per configurare la protezione con password sulle unità dati rimovibili.</span><span class="sxs-lookup"><span data-stu-id="c6b64-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="c6b64-269">Quando questo criterio non è configurato, le password sono supportate con le impostazioni predefinite, che non includono requisiti di complessità delle password e richiedono solo otto caratteri.</span><span class="sxs-lookup"><span data-stu-id="c6b64-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="c6b64-270">Per una maggiore sicurezza, è possibile abilitare questo criterio e selezionare <strong> Richiedi password per l'unità dati rimovibili </strong> , selezionare <strong> Richiedi complessità password </strong> e quindi impostare la <strong> lunghezza minima della password preferita </strong> .</span><span class="sxs-lookup"><span data-stu-id="c6b64-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6b64-271">Scegliere il modo in cui possono essere recuperate le unità rimovibili protette da BitLocker</span><span class="sxs-lookup"><span data-stu-id="c6b64-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6b64-272">Configurazione consigliata: <strong> non configurata</span><span class="sxs-lookup"><span data-stu-id="c6b64-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="c6b64-273">È possibile configurare questo criterio per abilitare l'agente recupero dati di BitLocker o per salvare le informazioni di ripristino di BitLocker in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="c6b64-274">Quando il criterio è impostato su <strong> non configurato </strong> , l'agente di recupero dati è consentita e non viene eseguito il backup delle informazioni di ripristino in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="c6b64-275">L'operazione MBAM non richiede le informazioni di ripristino di cui eseguire il backup in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6b64-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c6b64-276">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6b64-276">Related topics</span></span>


[<span data-ttu-id="c6b64-277">Preparazione dell'ambiente per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c6b64-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









