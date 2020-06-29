---
title: Risoluzione dei problemi di installazione di MBAM 2.5
description: Introduzione alla risoluzione dei problemi di installazione di MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804546"
---
# <span data-ttu-id="dd160-103">Risoluzione dei problemi di installazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dd160-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="dd160-104">Questo articolo illustra come risolvere i problemi di installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 in una configurazione autonoma.</span><span class="sxs-lookup"><span data-stu-id="dd160-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="dd160-105">Riferimenti ai file di log di MBAM per la risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="dd160-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="dd160-106">MBAM include la registrazione per l'installazione del server, l'installazione del client e gli eventi.</span><span class="sxs-lookup"><span data-stu-id="dd160-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="dd160-107">Questa registrazione deve essere definita per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="dd160-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="dd160-108">File di log di installazione di MBAM server</span><span class="sxs-lookup"><span data-stu-id="dd160-108">MBAM server installation log files</span></span>

<span data-ttu-id="dd160-109">MBAMServerSetup.exe genera i file di log seguenti nella cartella% Temp% dell'utente durante l'installazione di MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd160-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="dd160-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numeri>. log</span><span class="sxs-lookup"><span data-stu-id="dd160-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="dd160-111">MBAMServerSetup.exe registra le azioni intraprese durante l'installazione di MBAM Setup e MBAM server:</span><span class="sxs-lookup"><span data-stu-id="dd160-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="dd160-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="dd160-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="dd160-113">MBAMServerSetup.exe registra altre azioni acquisite durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dd160-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="dd160-114">File di log di installazione del client MBAM</span><span class="sxs-lookup"><span data-stu-id="dd160-114">MBAM client installation log file</span></span>

<span data-ttu-id="dd160-115">L'installazione del client viene registrata nel file di log seguente nella cartella% Temp% (o in una posizione personalizzata, a seconda del modo in cui il client è stato installato):</span><span class="sxs-lookup"><span data-stu-id="dd160-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="dd160-116">MSI \<five random characters\> . log</span><span class="sxs-lookup"><span data-stu-id="dd160-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="dd160-117">Questo log contiene le azioni che vengono eseguite durante l'installazione di MBAM client.</span><span class="sxs-lookup"><span data-stu-id="dd160-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="dd160-118">Evento client MBAM-canale di registrazione</span><span class="sxs-lookup"><span data-stu-id="dd160-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="dd160-119">MBAM include canali di registrazione eventi distinti.</span><span class="sxs-lookup"><span data-stu-id="dd160-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="dd160-120">I file di log amministratore, analitico e operativo si trovano nel Visualizzatore eventi, in **applicazioni e servizi**di  >  **Microsoft**  >  **Windows**  >  **mbam**.</span><span class="sxs-lookup"><span data-stu-id="dd160-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="dd160-121">La tabella seguente fornisce una breve descrizione di ogni log eventi.</span><span class="sxs-lookup"><span data-stu-id="dd160-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="dd160-122">Registro eventi</span><span class="sxs-lookup"><span data-stu-id="dd160-122">Event log</span></span>| <span data-ttu-id="dd160-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd160-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="dd160-124">Microsoft-Windows-MBAM/admin</span><span class="sxs-lookup"><span data-stu-id="dd160-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="dd160-125">Contiene messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="dd160-125">Contains error messages</span></span>|
|<span data-ttu-id="dd160-126">Microsoft-Windows-MBAM/analitica</span><span class="sxs-lookup"><span data-stu-id="dd160-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="dd160-127">Contiene informazioni di registrazione avanzate</span><span class="sxs-lookup"><span data-stu-id="dd160-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="dd160-128">Microsoft-Windows-MBAM/Operational</span><span class="sxs-lookup"><span data-stu-id="dd160-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="dd160-129">Contiene messaggi di successo</span><span class="sxs-lookup"><span data-stu-id="dd160-129">Contains success messages</span></span>|

### <span data-ttu-id="dd160-130">Evento server MBAM-canale di registrazione</span><span class="sxs-lookup"><span data-stu-id="dd160-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="dd160-131">I file di log si trovano nel Visualizzatore eventi, in **Application and Services logs**di  >  **Microsoft**  >  **Windows**  >  **mbam**.</span><span class="sxs-lookup"><span data-stu-id="dd160-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="dd160-132">La tabella seguente include i registri eventi del server introdotti in MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="dd160-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="dd160-133">Registro eventi</span><span class="sxs-lookup"><span data-stu-id="dd160-133">Event log</span></span>| <span data-ttu-id="dd160-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd160-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="dd160-135">Microsoft-Windows-MBAM/admin</span><span class="sxs-lookup"><span data-stu-id="dd160-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="dd160-136">Contiene messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="dd160-136">Contains error messages</span></span>|
|<span data-ttu-id="dd160-137">Microsoft-Windows-MBAM/analitica</span><span class="sxs-lookup"><span data-stu-id="dd160-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="dd160-138">Contiene informazioni di registrazione avanzate</span><span class="sxs-lookup"><span data-stu-id="dd160-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="dd160-139">Microsoft-Windows-MBAM/Operational</span><span class="sxs-lookup"><span data-stu-id="dd160-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="dd160-140">Contiene messaggi di successo</span><span class="sxs-lookup"><span data-stu-id="dd160-140">Contains success messages</span></span>|

### <span data-ttu-id="dd160-141">Registri del servizio Web MBAM</span><span class="sxs-lookup"><span data-stu-id="dd160-141">MBAM web service logs</span></span>

<span data-ttu-id="dd160-142">Ogni log del servizio Web MBAM scrive le informazioni di registrazione in un file SVCLOG.</span><span class="sxs-lookup"><span data-stu-id="dd160-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="dd160-143">Per impostazione predefinita, ogni servizio Web scrive il file di traccia in una cartella che usa il proprio nome nella cartella C:\inetpub\Microsoft di gestione di BitLocker Solution\Logs.</span><span class="sxs-lookup"><span data-stu-id="dd160-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="dd160-144">È possibile usare lo strumento Visualizzatore di tracce del servizio (parte di Microsoft Visual Studio) per esaminare le tracce di svclog.</span><span class="sxs-lookup"><span data-stu-id="dd160-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="dd160-145">Risoluzione dei problemi di crittografia e segnalazione</span><span class="sxs-lookup"><span data-stu-id="dd160-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="dd160-146">Questa sezione contiene informazioni sulla risoluzione dei problemi relativi a funzionalità server, funzionalità client, impostazioni di configurazione e problemi noti:</span><span class="sxs-lookup"><span data-stu-id="dd160-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="dd160-147">Installazione del client MBAM, impostazioni di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="dd160-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="dd160-148">Determinare se l'agente MBAM è installato nel computer client.</span><span class="sxs-lookup"><span data-stu-id="dd160-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="dd160-149">Quando MBAM è installato, crea un servizio denominato servizio client di Gestione BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd160-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="dd160-150">Questo servizio è configurato per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="dd160-150">This service is configured to start automatically.</span></span> <span data-ttu-id="dd160-151">Determinare se il servizio è in corso.</span><span class="sxs-lookup"><span data-stu-id="dd160-151">Determine whether the service is running.</span></span>

<span data-ttu-id="dd160-152">Verificare che nel computer client vengano applicate le impostazioni dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="dd160-153">La sottochiave del registro di sistema seguente viene creata se sono state applicate le impostazioni di criteri di gruppo nel computer client: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="dd160-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="dd160-154">Verificare che questa chiave esista e venga popolata usando i valori per le impostazioni dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="dd160-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="dd160-155">Agente MBAM nel periodo di ritardo iniziale</span><span class="sxs-lookup"><span data-stu-id="dd160-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="dd160-156">Il client MBAM non avvia l'operazione immediatamente dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dd160-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="dd160-157">C'è un ritardo casuale iniziale di 1-18 minuti prima che l'agente MBAM inizi l'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd160-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="dd160-158">Oltre al ritardo iniziale, c'è un ritardo di almeno 90 minuti.</span><span class="sxs-lookup"><span data-stu-id="dd160-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="dd160-159">Il ritardo dipende dalle impostazioni dei criteri di gruppo configurate per la frequenza di controllo dello stato del client. Di conseguenza, il ritardo totale prima dell'avvio di un'operazione del client è il ritardo della frequenza di *avvio casuale*del  +  *client*.</span><span class="sxs-lookup"><span data-stu-id="dd160-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="dd160-160">Se i registri eventi operativi e amministrativi sono vuoti, il client non ha ancora avviato l'operazione e si trova nel periodo di ritardo menzionato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dd160-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="dd160-161">Se si vuole ignorare il ritardo, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd160-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="dd160-162">Arrestare il servizio di servizio client di Gestione BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd160-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="dd160-163">Nella sottochiave **HKEY_LOCAL_MACHINE \software\microsoft\mbam** del registro di sistema creare il valore del registro di sistema **NoStartupDelay** , impostarne il tipo su **REG_DWORD**e quindi impostarne il valore su **1**.</span><span class="sxs-lookup"><span data-stu-id="dd160-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="dd160-164">In **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**impostare i valori di **ClientWakeupFrequency** e **StatusReportingFrequency** su **1**.</span><span class="sxs-lookup"><span data-stu-id="dd160-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="dd160-165">Questi valori ritorneranno alle impostazioni originali dopo il computer per gli aggiornamenti dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="dd160-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="dd160-166">Avviare il servizio di servizio client di Gestione BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd160-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="dd160-167">Dopo l'avvio del servizio, se si accede localmente nel computer e non sono presenti errori, è necessario ricevere una richiesta di crittografia del computer entro un minuto.</span><span class="sxs-lookup"><span data-stu-id="dd160-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="dd160-168">Se non si riceve una richiesta, è necessario rivedere i log di amministrazione di MBAM per eventuali voci di errore.</span><span class="sxs-lookup"><span data-stu-id="dd160-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="dd160-169">Il computer non ha un dispositivo TPM o il dispositivo TPM non è abilitato nel BIOS</span><span class="sxs-lookup"><span data-stu-id="dd160-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="dd160-170">Esaminare il log eventi dell'amministratore di MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="dd160-171">Verrà visualizzata la voce di un evento simile alla seguente nel log eventi dell'amministratore di MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd160-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="dd160-172">Aprire Gestione TPM (TPM. msc) e verificare che il computer disponga di un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="dd160-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="dd160-173">Se TPM. msc non mostra un dispositivo, aprire Gestione dispositivi (devmgmt. msc) e verificare la visualizzazione di un modulo Trusted Platform in dispositivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="dd160-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="dd160-174">Se non si vede un dispositivo Trusted Platform Module, potrebbe essere vero per uno dei motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd160-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="dd160-175">Il sistema non ha un dispositivo Trusted Platform Module (TPM/sicurezza).</span><span class="sxs-lookup"><span data-stu-id="dd160-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="dd160-176">Il dispositivo TPM è disabilitato nel BIOS.</span><span class="sxs-lookup"><span data-stu-id="dd160-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="dd160-177">Il dispositivo TPM è abilitato nel BIOS, ma la gestione del dispositivo TPM dall'impostazione del sistema operativo è disabilitata nel BIOS.</span><span class="sxs-lookup"><span data-stu-id="dd160-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="dd160-178">Non si usa un driver Microsoft per il dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="dd160-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="dd160-179">Esaminare i dispositivi elencati in gestione dispositivi per identificare il driver di dispositivo TPM Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dd160-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="dd160-180">Se il dispositivo TPM non usa il driver C:\Windows\System32\tpm.sys, è necessario aggiornare il driver selezionando il file C:\Windows\Inf\tpm.inf.</span><span class="sxs-lookup"><span data-stu-id="dd160-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="dd160-181">Il computer non ha una partizione di sistema valida</span><span class="sxs-lookup"><span data-stu-id="dd160-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="dd160-182">Esaminare il log eventi dell'amministratore di MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="dd160-183">Verrà visualizzata la voce di un evento simile alla seguente nel log eventi dell'amministratore di MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd160-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="dd160-184">BitLocker richiede una partizione di sistema per abilitare la crittografia ([crittografia unità BitLocker in Windows 7: domande frequenti](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="dd160-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="dd160-185">MBAM non crea automaticamente la partizione di sistema.</span><span class="sxs-lookup"><span data-stu-id="dd160-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="dd160-186">È possibile usare l'utilità preparazione unità BitLocker (bdehdcfg.exe) per creare la partizione di sistema e trasferire i file di avvio necessari.</span><span class="sxs-lookup"><span data-stu-id="dd160-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="dd160-187">Ad esempio, puoi usare il comando **% windir% \system32\bdeHdCfg.exe-destinazione 300-dimensione predefinita-tranquilla** per preparare l'unità in modo invisibile all'utente prima di distribuire mbam per crittografare le unità.</span><span class="sxs-lookup"><span data-stu-id="dd160-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="dd160-188">Questo richiede un riavvio.</span><span class="sxs-lookup"><span data-stu-id="dd160-188">This requires a restart.</span></span> <span data-ttu-id="dd160-189">Se necessario, è anche possibile eseguire lo script dell'azione.</span><span class="sxs-lookup"><span data-stu-id="dd160-189">You can also script the action if this is required.</span></span> <span data-ttu-id="dd160-190">Il documento seguente descrive lo strumento di preparazione unità BitLocker:</span><span class="sxs-lookup"><span data-stu-id="dd160-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="dd160-191">Descrizione dello strumento di preparazione unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="dd160-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="dd160-192">Le unità non sono formattate per avere un file system compatibile</span><span class="sxs-lookup"><span data-stu-id="dd160-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="dd160-193">Vedere l' [articolo di TechNet per i requisiti di file System per BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span><span class="sxs-lookup"><span data-stu-id="dd160-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="dd160-194">Conflitto di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="dd160-194">Group Policy conflict</span></span>

<span data-ttu-id="dd160-195">Verrà visualizzata la voce di un evento simile alla seguente nel log eventi dell'amministratore di MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd160-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="dd160-196">Verificare le impostazioni di criteri di gruppo per assicurarsi di non avere un'impostazione in conflitto tra le impostazioni dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="dd160-197">È consigliabile configurare criteri di gruppo usando il modello MBAM di MDOP e non il modello di crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd160-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="dd160-198">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dd160-198">For example:</span></span>

<span data-ttu-id="dd160-199">In impostazioni di crittografia unità sistema operativo è stato selezionato TPM come Protector ed è stato selezionato Consenti anche **PIN avanzati per l'avvio**.</span><span class="sxs-lookup"><span data-stu-id="dd160-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="dd160-200">Si tratta di impostazioni in conflitto, perché la protezione solo TPM non richiede un PIN.</span><span class="sxs-lookup"><span data-stu-id="dd160-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="dd160-201">Devi quindi disabilitare l'impostazione dei PIN avanzati.</span><span class="sxs-lookup"><span data-stu-id="dd160-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="dd160-202">L'utente può richiedere un'esenzione</span><span class="sxs-lookup"><span data-stu-id="dd160-202">User may have requested an exemption</span></span>

<span data-ttu-id="dd160-203">Se è stata abilitata l'impostazione Configurazione computer\Modelli Amministrativi\componenti di Components\MDOP MBAM (BitLocker Management) \Client Management\Configure criteri di esenzione dall'utente, agli utenti verrà offerta la possibilità di richiedere un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="dd160-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="dd160-204">Per impostazione predefinita, se l'utente richiede un'esenzione, l'esenzione sarà valida per 7 giorni e l'utente non riceverà le richieste di crittografia durante questo periodo.</span><span class="sxs-lookup"><span data-stu-id="dd160-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="dd160-205">Il valore predefinito può essere aumentato o ridotto durante la configurazione dei criteri. Una volta terminato il periodo di esenzione, viene chiesto di crittografare l'utente.</span><span class="sxs-lookup"><span data-stu-id="dd160-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="dd160-206">Verrà visualizzata la voce seguente nel log eventi dell'amministratore di MBAM quando un computer è in esenzione dall'utente:</span><span class="sxs-lookup"><span data-stu-id="dd160-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="dd160-207">Se si vuole ignorare manualmente l'esenzione dall'utente per un computer, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd160-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="dd160-208">Imposta il valore AllowUserExemption su **0** nella sottochiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="dd160-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="dd160-209">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="dd160-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="dd160-210">Eliminare tutti i valori del registro di sistema sotto la sottochiave del registro di sistema seguente, ad eccezione di **AgentVersion**, **EncodedComputerName**e **installato**:</span><span class="sxs-lookup"><span data-stu-id="dd160-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="dd160-211">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM</span><span class="sxs-lookup"><span data-stu-id="dd160-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="dd160-212">**Nota** Per applicare le modifiche, è necessario riavviare l'agente MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="dd160-213">Tenere presente che dopo l'applicazione di criteri di gruppo al computer, questi valori possono tornare alle impostazioni originali.</span><span class="sxs-lookup"><span data-stu-id="dd160-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="dd160-214">Problema WMI</span><span class="sxs-lookup"><span data-stu-id="dd160-214">WMI issue</span></span>

<span data-ttu-id="dd160-215">MBAM usa i metodi della classe win32_encryptablevolume per gestire BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd160-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="dd160-216">Se questo modulo non è registrato o è corrotto, il client MBAM non funzionerà correttamente e verrà visualizzata la voce dell'evento seguente nel log eventi dell'amministratore di MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd160-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="dd160-217">Si potrebbe inoltre notare che i criteri di ripristino e hardware non si applicano con il codice di errore 0x8007007e.</span><span class="sxs-lookup"><span data-stu-id="dd160-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="dd160-218">Questo significa che non è stato possibile trovare il modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="dd160-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="dd160-219">Per risolvere il problema, è necessario registrare nuovamente la classe **Win32_EncryptableVolume** usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="dd160-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="dd160-220">Risoluzione dei problemi relativi alle comunicazioni di MBAM Agent</span><span class="sxs-lookup"><span data-stu-id="dd160-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="dd160-221">Questa sezione contiene informazioni per la risoluzione dei problemi seguenti correlate alla comunicazione tra gli agenti di MBAM:</span><span class="sxs-lookup"><span data-stu-id="dd160-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="dd160-222">URL del servizio MBAM non corretto</span><span class="sxs-lookup"><span data-stu-id="dd160-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="dd160-223">Se il valore del servizio di stato o del ripristino e del servizio hardware di MBAM Compliance non è corretto, verrà visualizzata una voce di evento simile alla seguente nel registro eventi di amministrazione di MBAM nel computer client:</span><span class="sxs-lookup"><span data-stu-id="dd160-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="dd160-224">Verificare i valori di **KeyRecoveryServiceEndPoint** e **StatusReportingServiceEndpoint** sotto la sottochiave del registro di sistema seguente nel computer client:</span><span class="sxs-lookup"><span data-stu-id="dd160-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="dd160-225">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="dd160-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="dd160-226">Per impostazione predefinita, l'URL per KeyRecoveryServiceEndPoint (MBAM Recovery and hardware service endpoint) è il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="dd160-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="dd160-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="dd160-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="dd160-228">Per impostazione predefinita, l'URL per StatusReportingServiceEndpoint (l'endpoint del servizio di segnalazione dello stato di MBAM) è il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="dd160-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="dd160-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="dd160-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="dd160-230">L'URL non deve contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="dd160-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="dd160-231">Se l'URL del servizio non è corretto, è consigliabile correggere l'URL del servizio nell'impostazione di criteri di gruppo seguente:</span><span class="sxs-lookup"><span data-stu-id="dd160-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="dd160-232">**Configurazione computer**  >  **Criteri**  >  **Modelli amministrativi**  >  **Componenti**  >  di Windows **MDOP mbam (Gestione BitLocker)**  >  **Gestione client**  >  **Configurare i servizi mbam**</span><span class="sxs-lookup"><span data-stu-id="dd160-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="dd160-233">Problema di connettività che influisce sul server di amministrazione MBAM</span><span class="sxs-lookup"><span data-stu-id="dd160-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="dd160-234">L'agente MBAM non sarà in grado di pubblicare gli aggiornamenti del database se esistono problemi di connettività tra l'agente client e il server di amministrazione MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="dd160-235">In questo caso, noterai le voci di errore di connettività nel log eventi dell'amministratore di MBAM nel computer client:</span><span class="sxs-lookup"><span data-stu-id="dd160-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="dd160-236">Controlli di base:</span><span class="sxs-lookup"><span data-stu-id="dd160-236">Basic checks:</span></span>

* <span data-ttu-id="dd160-237">Verificare la connettività di base eseguendo il ping del server di amministrazione MBAM per nome e IP.</span><span class="sxs-lookup"><span data-stu-id="dd160-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="dd160-238">Verificare se è possibile connettersi al sito Web o alla porta di servizio di MBAM Administration tramite Telnet o Portqry.</span><span class="sxs-lookup"><span data-stu-id="dd160-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="dd160-239">Verificare che il servizio IIS sia in uso nel server di amministrazione e monitoraggio di MBAM e che il servizio Web MBAM sia in ascolto sulla stessa porta configurata nel computer client MBAM ( `netstat –ano | find "portnumber"` ).</span><span class="sxs-lookup"><span data-stu-id="dd160-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="dd160-240">Verificare che il numero di porta configurato per il sito Web di MBAM usi IIS Manager (inetmgr).</span><span class="sxs-lookup"><span data-stu-id="dd160-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="dd160-241">Verificare che il numero di porta sia uguale al numero di porta in cui il client sta ascoltando.</span><span class="sxs-lookup"><span data-stu-id="dd160-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="dd160-242">Verificare che il numero di porta non sia condiviso da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="dd160-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="dd160-243">Ad esempio, un'altra applicazione sul server non deve usare la stessa porta.</span><span class="sxs-lookup"><span data-stu-id="dd160-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="dd160-244">Se è presente un firewall, verificare che la porta sia aperta nel firewall o nel server proxy.</span><span class="sxs-lookup"><span data-stu-id="dd160-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="dd160-245">Se la comunicazione tra client e server è sicura, verificare che si stia usando un certificato SSL valido.</span><span class="sxs-lookup"><span data-stu-id="dd160-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="dd160-246">Verificare la connettività di rete tra il server Web e il server di database a cui vengono inviati i dati per l'inserimento.</span><span class="sxs-lookup"><span data-stu-id="dd160-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="dd160-247">È possibile controllare la connettività del database dal server Web al server di database usando l'amministratore dell'origine dati ODBC.</span><span class="sxs-lookup"><span data-stu-id="dd160-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="dd160-248">Informazioni dettagliate sulla risoluzione dei problemi di connessione a SQL Server sono disponibili in [modalità di risoluzione dei problemi di connessione al motore di database di SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd160-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="dd160-249">Risoluzione dei problemi relativi al problema della connettività</span><span class="sxs-lookup"><span data-stu-id="dd160-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="dd160-250">Verificare che l'URL del servizio configurato nel client sia corretto.</span><span class="sxs-lookup"><span data-stu-id="dd160-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="dd160-251">Copiare il valore dell'URL per KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) dal registro di sistema e aprirlo in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dd160-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="dd160-252">Analogamente, copiare il valore dell'URL per StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) e aprirlo in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dd160-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="dd160-253">Se non è possibile passare all'URL dal computer client, è consigliabile testare la connettività di rete di base dal client al server che sta usando IIS.</span><span class="sxs-lookup"><span data-stu-id="dd160-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="dd160-254">Vedere i punti 1, 2, 3 e 4 nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="dd160-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="dd160-255">Esaminare inoltre i registri dell'applicazione nel server di amministrazione e monitoraggio per eventuali errori.</span><span class="sxs-lookup"><span data-stu-id="dd160-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="dd160-256">È possibile creare una traccia di rete simultanea tra il client e il server e rivedere la traccia per determinare la causa dell'errore di connessione tra l'agente client e il server di amministrazione MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="dd160-257">Se è possibile passare agli URL del servizio dal computer client e sono presenti voci di errore di connettività nei registri degli eventi di amministrazione di MBAM, potrebbe essere dovuto a un errore di connettività tra l'Administration Server e il server di database.</span><span class="sxs-lookup"><span data-stu-id="dd160-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="dd160-258">Se è possibile passare a entrambi gli URL del servizio e la connettività tra il client e il server in cui è in corso, IIS sta funzionando.</span><span class="sxs-lookup"><span data-stu-id="dd160-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="dd160-259">Tuttavia, potrebbe essersi verificato un problema di comunicazione tra il server che sta usando IIS e il server di database.</span><span class="sxs-lookup"><span data-stu-id="dd160-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="dd160-260">I servizi MBAM potrebbero non essere in grado di connettersi al server di database a causa di un problema di rete o di un'impostazione di stringa di connessione database non corretta.</span><span class="sxs-lookup"><span data-stu-id="dd160-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="dd160-261">Esaminare i registri dell'applicazione nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="dd160-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="dd160-262">È possibile che vengano visualizzate voci di errore o avvisi da ASP.NET di origine 2.0.50727.0 simili alla voce di log seguente:</span><span class="sxs-lookup"><span data-stu-id="dd160-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="dd160-263">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="dd160-263">Possible causes</span></span>

##### <span data-ttu-id="dd160-264">Causa 1</span><span class="sxs-lookup"><span data-stu-id="dd160-264">Cause 1</span></span>

<span data-ttu-id="dd160-265">L'amministratore potrebbe avere specificato un nome di istanza di database non valido o un cognome di database durante l'installazione di componenti server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="dd160-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="dd160-266">È possibile verificare e correggere le stringhe di connessione del database tramite la console di gestione di IIS.</span><span class="sxs-lookup"><span data-stu-id="dd160-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="dd160-267">A questo scopo, aprire Gestione IIS e passare a amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="dd160-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="dd160-268">Per ogni servizio elencato sul lato sinistro, eseguire la procedura seguente per modificare le stringhe di connessione del database:</span><span class="sxs-lookup"><span data-stu-id="dd160-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="dd160-269">In **visualizzazione funzionalità**fare doppio clic su **stringhe di connessione**.</span><span class="sxs-lookup"><span data-stu-id="dd160-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="dd160-270">Nella pagina **stringhe di connessione** selezionare la stringa di connessione che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="dd160-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="dd160-271">Nel riquadro **azioni** selezionare **modifica**.</span><span class="sxs-lookup"><span data-stu-id="dd160-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="dd160-272">Nella finestra di dialogo **Modifica stringa di connessione** modificare le proprietà che si desidera modificare e quindi scegliere **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd160-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="dd160-273">Causa 2</span><span class="sxs-lookup"><span data-stu-id="dd160-273">Cause 2</span></span>

<span data-ttu-id="dd160-274">Porta di SQL Server bloccata nel firewall.</span><span class="sxs-lookup"><span data-stu-id="dd160-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="dd160-275">Verificare il numero di porta in cui SQL Server è configurato per l'ascolto e verificare che la porta sia aperta nel firewall tra il server di amministrazione e il server di database.</span><span class="sxs-lookup"><span data-stu-id="dd160-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="dd160-276">Causa 3</span><span class="sxs-lookup"><span data-stu-id="dd160-276">Cause 3</span></span>

<span data-ttu-id="dd160-277">Binding TCP/IP non corretti di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd160-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="dd160-278">Verificare i binding TCP/IP SQL in Gestione configurazione SQL Server nel server di database.</span><span class="sxs-lookup"><span data-stu-id="dd160-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="dd160-279">MBAM richiede che i protocolli TCP/IP e named pipe siano abilitati per la connessione al database.</span><span class="sxs-lookup"><span data-stu-id="dd160-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="dd160-280">Causa 4</span><span class="sxs-lookup"><span data-stu-id="dd160-280">Cause 4</span></span>

<span data-ttu-id="dd160-281">L'account del servizio NT Authority\Network o l'account del computer del server di amministrazione MBAM non dispone delle autorizzazioni necessarie per connettersi al database SQL.</span><span class="sxs-lookup"><span data-stu-id="dd160-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="dd160-282">Durante l'installazione di componenti di database nel server di database, il programma di installazione crea due gruppi locali: controllo di conformità di MBAM per l'accesso DB e recupero di MBAM e accesso DB hardware.</span><span class="sxs-lookup"><span data-stu-id="dd160-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="dd160-283">L'account del servizio NT Authority\Network, l'account del computer di MBAM Administration Server e l'utente che installa i componenti del database vengono aggiunti automaticamente a questi gruppi.</span><span class="sxs-lookup"><span data-stu-id="dd160-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="dd160-284">A questi gruppi vengono concesse le autorizzazioni necessarie per il database durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dd160-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="dd160-285">Tutti gli utenti che fanno parte di questo gruppo ricevono automaticamente le autorizzazioni necessarie per il database.</span><span class="sxs-lookup"><span data-stu-id="dd160-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="dd160-286">Il servizio Web potrebbe non connettersi al server di database a causa di un problema di autorizzazioni se una o più delle condizioni seguenti sono vere:</span><span class="sxs-lookup"><span data-stu-id="dd160-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="dd160-287">I gruppi menzionati in precedenza vengono rimossi dai gruppi locali nel server di database.</span><span class="sxs-lookup"><span data-stu-id="dd160-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="dd160-288">L'account del servizio NT Authority\Network e l'account del computer di MBAM Administration Server non sono membri di questi gruppi.</span><span class="sxs-lookup"><span data-stu-id="dd160-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="dd160-289">Questi gruppi non dispongono delle autorizzazioni necessarie per il database.</span><span class="sxs-lookup"><span data-stu-id="dd160-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="dd160-290">Si noteranno errori relativi alle autorizzazioni nei registri dell'applicazione nel server di amministrazione e monitoraggio di MBAM se una delle condizioni precedenti è vera.</span><span class="sxs-lookup"><span data-stu-id="dd160-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="dd160-291">In questo caso, devi aggiungere manualmente l'account del servizio NT Authority\Network e l'account del computer del server di amministrazione di MBAM e concedere loro un ruolo pubblico a livello di server nel server di database SQL che usa SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dd160-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="dd160-292">Esaminare i registri del servizio Web</span><span class="sxs-lookup"><span data-stu-id="dd160-292">Review the web service logs</span></span>

<span data-ttu-id="dd160-293">Se nessun evento viene registrato nei registri dell'applicazione nel server di amministrazione MBAM, è il momento di esaminare i registri del servizio Web (con estensione svclog) del servizio Web di MBAM ospitati nel server di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="dd160-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="dd160-294">Per visualizzare il file di log, sarà necessario usare lo strumento Visualizzatore di tracce di servizio (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .</span><span class="sxs-lookup"><span data-stu-id="dd160-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="dd160-295">Dovresti studiare principalmente i log di traccia del servizio di RecoveryandHardwareService e ComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="dd160-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="dd160-296">Per impostazione predefinita, i registri dei servizi Web si trovano nella cartella di gestione di C:\inetpub\Microsoft BitLocker Solution\Logs.</span><span class="sxs-lookup"><span data-stu-id="dd160-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="dd160-297">Ogni servizio scrive il proprio file con estensione svclog nella relativa cartella.</span><span class="sxs-lookup"><span data-stu-id="dd160-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="dd160-298">Esaminare l'attività nel log di traccia dei servizi per eventuali voci di errore o di avviso.</span><span class="sxs-lookup"><span data-stu-id="dd160-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="dd160-299">Per impostazione predefinita, le voci di errore vengono evidenziate in rosso.</span><span class="sxs-lookup"><span data-stu-id="dd160-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="dd160-300">Selezionare la descrizione dell'errore nel riquadro destro del Visualizzatore di traccia per visualizzare informazioni dettagliate sulla voce di errore.</span><span class="sxs-lookup"><span data-stu-id="dd160-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="dd160-301">Di seguito è riportata una voce di errore di esempio dal log di traccia:</span><span class="sxs-lookup"><span data-stu-id="dd160-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="dd160-302">Re-installazione o riconfigurazione dell'infrastruttura MBAM</span><span class="sxs-lookup"><span data-stu-id="dd160-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="dd160-303">Per reinstallare o riconfigurare l'infrastruttura MBAM, è necessario conoscere le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd160-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="dd160-304">Account del pool di applicazioni</span><span class="sxs-lookup"><span data-stu-id="dd160-304">Application Pool account</span></span>

* <span data-ttu-id="dd160-305">Gruppi di MBAM (helpdesk, Advanced, gruppo report utenti)</span><span class="sxs-lookup"><span data-stu-id="dd160-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="dd160-306">URL report MBAM</span><span class="sxs-lookup"><span data-stu-id="dd160-306">MBAM Reports URL</span></span>

* <span data-ttu-id="dd160-307">Nomi di database e nome di SQL Server</span><span class="sxs-lookup"><span data-stu-id="dd160-307">SQL Server name and database names</span></span>

* <span data-ttu-id="dd160-308">Account di MBAM ReadWrite e ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dd160-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="dd160-309">Account del pool di applicazioni</span><span class="sxs-lookup"><span data-stu-id="dd160-309">Application Pool account</span></span>

<span data-ttu-id="dd160-310">Per trovare l'account del pool di applicazioni, accedere al server Web MBAM, aprire **Gestione Internet Information Services (IIS)** e quindi selezionare **pool di applicazioni**:</span><span class="sxs-lookup"><span data-stu-id="dd160-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![pool di applicazioni](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="dd160-312">Il nome dell'entità servizio (SPN) deve essere impostato in questo account.</span><span class="sxs-lookup"><span data-stu-id="dd160-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="dd160-313">Questa impostazione è molto importante per la funzionalità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="dd160-314">Gruppi di MBAM (helpdesk, Advanced, report Users Group e reports URL)</span><span class="sxs-lookup"><span data-stu-id="dd160-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![Gruppi di MBAM](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="dd160-316">In questo modo vengono fornite informazioni come il gruppo helpdesk, il gruppo helpdesk avanzato, il gruppo report utenti e l'URL report MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="dd160-317">L'URL di report MBAM deve essere fornito nella configurazione di MBAM e dovrebbe essere letto come: http (s)://servername/ReportServer.</span><span class="sxs-lookup"><span data-stu-id="dd160-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="dd160-318">Nomi di database e nome di SQL Server (DB)</span><span class="sxs-lookup"><span data-stu-id="dd160-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="dd160-319">Per trovare i nomi e le istanze di SQL Server che ospitano MBAM DBs, accedere al server Web MBAM (IIS) e passare alla sottochiave del registro di sistema folowing:</span><span class="sxs-lookup"><span data-stu-id="dd160-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="dd160-320">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web</span><span class="sxs-lookup"><span data-stu-id="dd160-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="dd160-322">Le parti evidenziate sono stringhe di connessione.</span><span class="sxs-lookup"><span data-stu-id="dd160-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="dd160-323">Dovrebbero avere il nome di SQL Server, i nomi di database e le istanze (se denominati).</span><span class="sxs-lookup"><span data-stu-id="dd160-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="dd160-324">Account di MBAM ReadWrite e ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dd160-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="dd160-325">Queste informazioni si trovano nel database di SQL Server, per cui è già stato trovato il nome dal server Web.</span><span class="sxs-lookup"><span data-stu-id="dd160-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="dd160-326">Account di ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dd160-326">ReadWrite account</span></span>

1. <span data-ttu-id="dd160-327">Accedere a SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="dd160-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="dd160-328">Fare clic con il pulsante destro del mouse su **mbam Recovery and hardware**, scegliere **Proprietà**e quindi selezionare **autorizzazioni**.</span><span class="sxs-lookup"><span data-stu-id="dd160-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="dd160-329">Ad esempio, il nome dell'account Lab è **MBAMWrite**.</span><span class="sxs-lookup"><span data-stu-id="dd160-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="dd160-330">Il pool di applicazioni e gli account di ReadWrite sono impostati come uguali.</span><span class="sxs-lookup"><span data-stu-id="dd160-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![Proprietà DB](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="dd160-333">Passare alla pagina **sicurezza** e quindi **accedere** a SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="dd160-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="dd160-334">Passare all'account visualizzato nella schermata precedente.</span><span class="sxs-lookup"><span data-stu-id="dd160-334">Browse to the account shown in the previous screenshot.</span></span>

![Sicurezza SQL](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="dd160-336">Fare clic con il pulsante destro del mouse sugli account, scegliere **Proprietà mapping utenti**e individuare il database di mbam Recovery and hardware:</span><span class="sxs-lookup"><span data-stu-id="dd160-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![Mapping degli utenti](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="dd160-338">Account di sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd160-338">ReadOnly account</span></span>

<span data-ttu-id="dd160-339">Aprire Gestione configurazione di SQL Server Reporting Services nel server SSRS.</span><span class="sxs-lookup"><span data-stu-id="dd160-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="dd160-340">Selezionare **URL Gestione report**e quindi esplorare gli **URL**:</span><span class="sxs-lookup"><span data-stu-id="dd160-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![Gestione report](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="dd160-342">Selezionare **amministrazione e monitoraggio di Microsoft BitLocker**:</span><span class="sxs-lookup"><span data-stu-id="dd160-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![Amministrazione e monitoraggio di BitLocker](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="dd160-344">Selezionare **MaltaDatasource**:</span><span class="sxs-lookup"><span data-stu-id="dd160-344">Select **MaltaDatasource**:</span></span>

![DBs](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="dd160-347">MaltaDataSource dovrebbe avere il nome dell'account ReadOnly e dovrebbe essere usato nella configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd160-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="dd160-348">Riferimento</span><span class="sxs-lookup"><span data-stu-id="dd160-348">Reference</span></span>

<span data-ttu-id="dd160-349">Per informazioni, vedi gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd160-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="dd160-350">Distribuzione di MBAM 2,5 in una configurazione autonoma</span><span class="sxs-lookup"><span data-stu-id="dd160-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="dd160-351">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="dd160-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
