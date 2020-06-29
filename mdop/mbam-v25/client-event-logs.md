---
title: Registri eventi del client
description: Registri eventi del client
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824195"
---
# <span data-ttu-id="79f3b-103">Registri eventi del client</span><span class="sxs-lookup"><span data-stu-id="79f3b-103">Client Event Logs</span></span>

<span data-ttu-id="79f3b-104">I log eventi del client MBAM si trovano nel Visualizzatore eventi-log delle applicazioni e dei servizi-Microsoft-Windows-MBAM-Operational Path.</span><span class="sxs-lookup"><span data-stu-id="79f3b-104">MBAM Client event logs are located in Event Viewer – Applications and Services Logs – Microsoft – Windows – MBAM - Operational path.</span></span>
<span data-ttu-id="79f3b-105">La tabella seguente contiene gli ID evento che possono verificarsi nel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-105">The following table contains event IDs that can occur on the MBAM Client.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79f3b-106">ID evento</span><span class="sxs-lookup"><span data-stu-id="79f3b-106">Event ID</span></span></th>
<th align="left"><span data-ttu-id="79f3b-107">Canale</span><span class="sxs-lookup"><span data-stu-id="79f3b-107">Channel</span></span></th>
<th align="left"><span data-ttu-id="79f3b-108">Simbolo dell'evento</span><span class="sxs-lookup"><span data-stu-id="79f3b-108">Event symbol</span></span></th>
<th align="left"><span data-ttu-id="79f3b-109">Messaggio</span><span class="sxs-lookup"><span data-stu-id="79f3b-109">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-110">1</span><span class="sxs-lookup"><span data-stu-id="79f3b-110">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-111">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-111">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-112">VolumeEnactmentSuccessful</span><span class="sxs-lookup"><span data-stu-id="79f3b-112">VolumeEnactmentSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-113">I criteri di MBAM sono stati applicati correttamente.</span><span class="sxs-lookup"><span data-stu-id="79f3b-113">The MBAM policies were applied successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-114">2</span><span class="sxs-lookup"><span data-stu-id="79f3b-114">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-115">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-115">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-116">VolumeEnactmentFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-116">VolumeEnactmentFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-117">Si è verificato un errore durante l'applicazione di criteri MBAM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-117">An error occurred while applying MBAM policies.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-118">3</span><span class="sxs-lookup"><span data-stu-id="79f3b-118">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-119">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-119">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-120">TransferStatusDataSuccessful</span><span class="sxs-lookup"><span data-stu-id="79f3b-120">TransferStatusDataSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-121">I dati di stato della crittografia sono stati inviati correttamente.</span><span class="sxs-lookup"><span data-stu-id="79f3b-121">The encryption status data was sent successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-122">4</span><span class="sxs-lookup"><span data-stu-id="79f3b-122">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-123">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-123">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-124">TransferStatusDataFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-124">TransferStatusDataFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-125">Si è verificato un errore durante l'invio di dati sullo stato di crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-125">An error occurred while sending encryption status data.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-126">8</span><span class="sxs-lookup"><span data-stu-id="79f3b-126">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-127">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-127">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-128">SystemVolumeNotFound</span><span class="sxs-lookup"><span data-stu-id="79f3b-128">SystemVolumeNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-129">Il volume di sistema non è presente.</span><span class="sxs-lookup"><span data-stu-id="79f3b-129">The system volume is missing.</span></span> <span data-ttu-id="79f3b-130">SystemVolume è necessario per crittografare l'unità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="79f3b-130">SystemVolume is needed to encrypt the operating system drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-131">9</span><span class="sxs-lookup"><span data-stu-id="79f3b-131">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-132">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-132">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-133">TPMNotFound</span><span class="sxs-lookup"><span data-stu-id="79f3b-133">TPMNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-134">L'hardware TPM manca.</span><span class="sxs-lookup"><span data-stu-id="79f3b-134">The TPM hardware is missing.</span></span> <span data-ttu-id="79f3b-135">TPM è necessario per crittografare l'unità del sistema operativo con qualsiasi protezione TPM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-135">TPM is needed to encrypt the operating system drive with any TPM protector.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-136">10</span><span class="sxs-lookup"><span data-stu-id="79f3b-136">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-137">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-137">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-138">MachineHWExempted</span><span class="sxs-lookup"><span data-stu-id="79f3b-138">MachineHWExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-139">Il computer è esentato dalla crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-139">The computer is exempted from Encryption.</span></span> <span data-ttu-id="79f3b-140">Stato hardware della macchina: esentato</span><span class="sxs-lookup"><span data-stu-id="79f3b-140">Machine’s hardware status: Exempted</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-141">11</span><span class="sxs-lookup"><span data-stu-id="79f3b-141">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-142">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-142">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-143">MachineHWUnknown</span><span class="sxs-lookup"><span data-stu-id="79f3b-143">MachineHWUnknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-144">Il computer è esentato dalla crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-144">The computer is exempted from encryption.</span></span> <span data-ttu-id="79f3b-145">Stato hardware della macchina: sconosciuto</span><span class="sxs-lookup"><span data-stu-id="79f3b-145">Machine’s hardware status: Unknown</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-146">12</span><span class="sxs-lookup"><span data-stu-id="79f3b-146">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-147">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-147">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-148">HWCheckFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-148">HWCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-149">Controllo esenzione hardware non riuscito.</span><span class="sxs-lookup"><span data-stu-id="79f3b-149">Hardware exemption check failed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-150">13</span><span class="sxs-lookup"><span data-stu-id="79f3b-150">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-151">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-151">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-152">UserIsExempted</span><span class="sxs-lookup"><span data-stu-id="79f3b-152">UserIsExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-153">L'utente è esonerato dalla crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-153">The user is exempt from encryption.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-154">14</span><span class="sxs-lookup"><span data-stu-id="79f3b-154">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-155">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-155">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-156">UserIsWaiting</span><span class="sxs-lookup"><span data-stu-id="79f3b-156">UserIsWaiting</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-157">L'utente ha richiesto un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="79f3b-157">The user requested an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-158">15</span><span class="sxs-lookup"><span data-stu-id="79f3b-158">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-159">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-159">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-160">UserExemptionCheckFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-160">UserExemptionCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-161">Controllo di esenzione dall'utente non riuscito.</span><span class="sxs-lookup"><span data-stu-id="79f3b-161">User exemption check failed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-162">16</span><span class="sxs-lookup"><span data-stu-id="79f3b-162">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-163">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-163">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-164">UserPostponed</span><span class="sxs-lookup"><span data-stu-id="79f3b-164">UserPostponed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-165">L'utente ha rinviato il processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-165">The user postponed the encryption process.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-166">17</span><span class="sxs-lookup"><span data-stu-id="79f3b-166">17</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-167">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-167">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-168">TPMInitializationFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-168">TPMInitializationFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-169">L'inizializzazione del TPM non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="79f3b-169">TPM initialization failed.</span></span> <span data-ttu-id="79f3b-170">L'utente ha rifiutato le modifiche del BIOS.</span><span class="sxs-lookup"><span data-stu-id="79f3b-170">The user rejected the BIOS changes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-171">18</span><span class="sxs-lookup"><span data-stu-id="79f3b-171">18</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-172">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-172">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-173">CoreServiceDown</span><span class="sxs-lookup"><span data-stu-id="79f3b-173">CoreServiceDown</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-174">Non è possibile connettersi al servizio di ripristino e hardware di MBAM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-174">Unable to connect to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-175">19</span><span class="sxs-lookup"><span data-stu-id="79f3b-175">19</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-176">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-176">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-177">CoreServiceUp</span><span class="sxs-lookup"><span data-stu-id="79f3b-177">CoreServiceUp</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-178">Connesso correttamente al servizio di ripristino e hardware di MBAM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-178">Successfully connected to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-179">20</span><span class="sxs-lookup"><span data-stu-id="79f3b-179">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-180">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-180">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-181">PolicyMismatch</span><span class="sxs-lookup"><span data-stu-id="79f3b-181">PolicyMismatch</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-182">I criteri di MBAM sono in conflitto o corrotti.</span><span class="sxs-lookup"><span data-stu-id="79f3b-182">The MBAM policy is in conflict or corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-183">21</span><span class="sxs-lookup"><span data-stu-id="79f3b-183">21</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-184">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-184">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-185">ConflictingOSVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="79f3b-185">ConflictingOSVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-186">Rilevato conflitto tra i criteri di crittografia del volume OS.</span><span class="sxs-lookup"><span data-stu-id="79f3b-186">Detected OS volume encryption policies conflict.</span></span> <span data-ttu-id="79f3b-187">Controlla i criteri di BitLocker e MBAM relativi alle protezioni unità OS.</span><span class="sxs-lookup"><span data-stu-id="79f3b-187">Check BitLocker and MBAM policies related to OS drive protectors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-188">22</span><span class="sxs-lookup"><span data-stu-id="79f3b-188">22</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-189">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-189">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-190">ConflictingFDDVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="79f3b-190">ConflictingFDDVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-191">Rilevato conflitto di criteri di crittografia del volume delle unità dati fisse.</span><span class="sxs-lookup"><span data-stu-id="79f3b-191">Detected Fixed Data Drive volume encryption policies conflict.</span></span> <span data-ttu-id="79f3b-192">Controlla i criteri di BitLocker e MBAM relativi alle protezioni unità FDD.</span><span class="sxs-lookup"><span data-stu-id="79f3b-192">Check BitLocker and MBAM policies related to FDD drive protectors.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-193">27</span><span class="sxs-lookup"><span data-stu-id="79f3b-193">27</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-194">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-194">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-195">EncryptionFailedNoDra</span><span class="sxs-lookup"><span data-stu-id="79f3b-195">EncryptionFailedNoDra</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-196">Si è verificato un errore durante la crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-196">An error occurred while encrypting.</span></span> <span data-ttu-id="79f3b-197">Una protezione DRA (Data Recovery Agent) è necessaria in modalità FIPS per i computer pre-Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="79f3b-197">A Data Recovery Agent (DRA) protector is required in FIPS mode for pre-Windows 8.1 machines.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-198">28</span><span class="sxs-lookup"><span data-stu-id="79f3b-198">28</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-199">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-199">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-200">TpmOwnerAuthEscrowed</span><span class="sxs-lookup"><span data-stu-id="79f3b-200">TpmOwnerAuthEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-201">Il TPM OwnerAuth è stato escrowed.</span><span class="sxs-lookup"><span data-stu-id="79f3b-201">The TPM OwnerAuth has been escrowed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-202">29</span><span class="sxs-lookup"><span data-stu-id="79f3b-202">29</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-203">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-203">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-204">RecoveryKeyEscrowed</span><span class="sxs-lookup"><span data-stu-id="79f3b-204">RecoveryKeyEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-205">La chiave di ripristino di BitLocker per il volume è stata escrowed.</span><span class="sxs-lookup"><span data-stu-id="79f3b-205">The BitLocker recovery key for the volume has been escrowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-206">30</span><span class="sxs-lookup"><span data-stu-id="79f3b-206">30</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-207">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-207">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-208">RecoveryKeyReset</span><span class="sxs-lookup"><span data-stu-id="79f3b-208">RecoveryKeyReset</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-209">La chiave di ripristino di BitLocker per il volume è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="79f3b-209">The BitLocker recovery key for the volume has been updated.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-210">31</span><span class="sxs-lookup"><span data-stu-id="79f3b-210">31</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-211">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-211">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-212">EnforcePolicyDateSet</span><span class="sxs-lookup"><span data-stu-id="79f3b-212">EnforcePolicyDateSet</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-213">La data di applicazione dei criteri, <em> &lt; data &gt; </em> , è stata impostata per il volume</span><span class="sxs-lookup"><span data-stu-id="79f3b-213">The enforce policy date, <em>&lt;date&gt;</em>, has been set for the volume</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-214">32</span><span class="sxs-lookup"><span data-stu-id="79f3b-214">32</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-215">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-215">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-216">EnforcePolicyDateCleared</span><span class="sxs-lookup"><span data-stu-id="79f3b-216">EnforcePolicyDateCleared</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-217">La data di applicazione dei criteri, <em> &lt; data &gt; </em> , è stata deselezionata per il volume.</span><span class="sxs-lookup"><span data-stu-id="79f3b-217">The enforce policy date, <em>&lt;date&gt;</em>, has been cleared for the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-218">33</span><span class="sxs-lookup"><span data-stu-id="79f3b-218">33</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-219">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-219">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-220">TpmLockOutResetSucceeded</span><span class="sxs-lookup"><span data-stu-id="79f3b-220">TpmLockOutResetSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-221">Reimpostare correttamente il blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-221">Successfully reset TPM lockout.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-222">34</span><span class="sxs-lookup"><span data-stu-id="79f3b-222">34</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-223">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-223">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-224">TpmLockOutResetFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-224">TpmLockOutResetFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-225">Non è possibile reimpostare il blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-225">Failed to reset TPM lockout.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-226">35</span><span class="sxs-lookup"><span data-stu-id="79f3b-226">35</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-227">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-227">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-228">TpmOwnerAuthRetrievalSucceeded</span><span class="sxs-lookup"><span data-stu-id="79f3b-228">TpmOwnerAuthRetrievalSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-229">È stato recuperato correttamente TPM OwnerAuth da MBAM Services.</span><span class="sxs-lookup"><span data-stu-id="79f3b-229">Successfully retrieved TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-230">36</span><span class="sxs-lookup"><span data-stu-id="79f3b-230">36</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-231">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-231">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-232">TpmOwnerAuthRetrievalFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-232">TpmOwnerAuthRetrievalFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-233">Impossibile recuperare il TPM OwnerAuth da servizi MBAM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-233">Failed to retrieve TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-234">37</span><span class="sxs-lookup"><span data-stu-id="79f3b-234">37</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-235">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-235">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-236">WmiProviderDllSearchPathUpdateFailed</span><span class="sxs-lookup"><span data-stu-id="79f3b-236">WmiProviderDllSearchPathUpdateFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-237">Non è possibile aggiornare il percorso di ricerca della DLL per il provider WMI.</span><span class="sxs-lookup"><span data-stu-id="79f3b-237">Failed to update the DLL search path for WMI provider.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-238">38</span><span class="sxs-lookup"><span data-stu-id="79f3b-238">38</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-239">Admin</span><span class="sxs-lookup"><span data-stu-id="79f3b-239">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-240">TimedOutWaitingForWmiProvider</span><span class="sxs-lookup"><span data-stu-id="79f3b-240">TimedOutWaitingForWmiProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-241">Interruzione dell'agente-timeout in attesa per l'istanza del provider WMI MBAM.</span><span class="sxs-lookup"><span data-stu-id="79f3b-241">Agent Stopping - Timed-out waiting for MBAM WMI Provider Instance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-242">39</span><span class="sxs-lookup"><span data-stu-id="79f3b-242">39</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-243">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-243">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-244">RemovableDriveMounted</span><span class="sxs-lookup"><span data-stu-id="79f3b-244">RemovableDriveMounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-245">È stato montato un drive rimovibile.</span><span class="sxs-lookup"><span data-stu-id="79f3b-245">Removable drive was mounted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-246">40</span><span class="sxs-lookup"><span data-stu-id="79f3b-246">40</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-247">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-247">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-248">RemovableDriveDismounted</span><span class="sxs-lookup"><span data-stu-id="79f3b-248">RemovableDriveDismounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-249">L'unità rimovibile è stata smontata.</span><span class="sxs-lookup"><span data-stu-id="79f3b-249">Removable drive was unmounted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-250">41</span><span class="sxs-lookup"><span data-stu-id="79f3b-250">41</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-251">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-251">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-252">FailedToEnactEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="79f3b-252">FailedToEnactEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-253">L'errore di connettersi al servizio di ripristino e hardware di MBAM ha impedito che i criteri di MBAM venissero applicati correttamente al volume.</span><span class="sxs-lookup"><span data-stu-id="79f3b-253">Failure to connect to the MBAM Recovery and Hardware service prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f3b-254">42</span><span class="sxs-lookup"><span data-stu-id="79f3b-254">42</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-255">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-255">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-256">FailedToEnactLockedVolume</span><span class="sxs-lookup"><span data-stu-id="79f3b-256">FailedToEnactLockedVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-257">Lo stato del volume bloccato ha impedito che i criteri di MBAM venissero applicati correttamente al volume.</span><span class="sxs-lookup"><span data-stu-id="79f3b-257">Locked volume state prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f3b-258">43</span><span class="sxs-lookup"><span data-stu-id="79f3b-258">43</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-259">Operativo</span><span class="sxs-lookup"><span data-stu-id="79f3b-259">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-260">TransferStatusDataFailedEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="79f3b-260">TransferStatusDataFailedEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f3b-261">L'omissione di connettersi al servizio di stato e conformità di MBAM ha impedito il trasferimento dei dati di stato della crittografia.</span><span class="sxs-lookup"><span data-stu-id="79f3b-261">Failure to connect to the MBAM Compliance and Status service prevented the transfer of encryption status data.</span></span></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="79f3b-262">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79f3b-262">Related topics</span></span>
[<span data-ttu-id="79f3b-263">Documentazione tecnica per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="79f3b-263">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="79f3b-264">Registri eventi del server</span><span class="sxs-lookup"><span data-stu-id="79f3b-264">Server Event Logs</span></span>](server-event-logs.md)

 


## <span data-ttu-id="79f3b-265">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="79f3b-265">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="79f3b-266">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="79f3b-266">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="79f3b-267">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="79f3b-267">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





