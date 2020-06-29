---
title: Prerequisiti per i client di MBAM 2.5
description: Prerequisiti per i client di MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826966"
---
# <span data-ttu-id="bbabe-103">Prerequisiti per i client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bbabe-103">Prerequisites for MBAM 2.5 Clients</span></span>


<span data-ttu-id="bbabe-104">Prima di installare il software del client MBAM nei computer degli utenti finali, verificare che l'ambiente e i computer client soddisfino i prerequisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="bbabe-104">Before you install the MBAM Client software on end users' computers, ensure that your environment and the client computers meet the following prerequisites.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bbabe-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="bbabe-105">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="bbabe-106">Dettagli</span><span class="sxs-lookup"><span data-stu-id="bbabe-106">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbabe-107">Il dominio aziendale deve contenere almeno un controller di dominio di Windows Server 2008 (o versioni successive).</span><span class="sxs-lookup"><span data-stu-id="bbabe-107">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbabe-108">Il computer client deve essere connesso alla rete Intranet aziendale.</span><span class="sxs-lookup"><span data-stu-id="bbabe-108">The client computer must be logged on to the enterprise intranet.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbabe-109">Solo per i computer client Windows 7: ogni client deve avere funzionalità TPM (Trusted Platform Module) (TPM 1,2 o successiva).</span><span class="sxs-lookup"><span data-stu-id="bbabe-109">For Windows 7 client computers only: Each client must have Trusted Platform Module (TPM) capability (TPM 1.2 or later).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbabe-110">Solo per i computer client Windows 8,1, Windows 10 RTM o Windows 10 versione 1511: se si vuole che MBAM sia in grado di archiviare e gestire le chiavi di ripristino del TPM, il provisioning automatico TPM deve essere disattivato e MBAM deve essere impostato come proprietario del TPM prima di distribuire MBAM.</span><span class="sxs-lookup"><span data-stu-id="bbabe-110">For Windows 8.1, Windows 10 RTM or Windows 10 version 1511 client computers only: If you want MBAM to be able to store and manage the TPM recovery keys, TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p>
<p><span data-ttu-id="bbabe-111">In MBAM 2,5 SP1 solo non è più necessario disattivare il provisioning automatico del TPM, ma è necessario assicurarsi che gli oggetti Criteri di gruppo TPM siano impostati su Active Directory con il TPM non OwnerAuth.</span><span class="sxs-lookup"><span data-stu-id="bbabe-111">In MBAM 2.5 SP1 only, you no longer need to turn off TPM auto-provisioning, but you must make sure that the TPM Group Policy Objects are set to not escrow TPM OwnerAuth to Active Directory.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)"><span data-ttu-id="bbabe-112">Considerazioni sulla sicurezza per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bbabe-112">MBAM 2.5 Security Considerations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbabe-113">Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM.</span><span class="sxs-lookup"><span data-stu-id="bbabe-113">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="bbabe-114">In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM.</span><span class="sxs-lookup"><span data-stu-id="bbabe-114">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span></p>
<p><span data-ttu-id="bbabe-115">In MBAM 2,5 SP1 è necessario attivare il provisioning automatico.</span><span class="sxs-lookup"><span data-stu-id="bbabe-115">In MBAM 2.5 SP1, you must turn on auto-provisioning.</span></span></p>
</p></td>
<td align="left"><p><span data-ttu-id="bbabe-116"><a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> </a> Per ulteriori informazioni, vedere password del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="bbabe-116">See <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)">TPM owner password</a> for further details.</span></span>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbabe-117">Il chip TPM deve essere attivato nel BIOS e può essere ripristinato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bbabe-117">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bbabe-118">Per altre informazioni, vedere la documentazione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="bbabe-118">See the BIOS documentation for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bbabe-119">Il disco rigido del computer deve avere almeno due partizioni e deve essere formattato con il file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="bbabe-119">The computer’s hard disk must have at least two partitions and must be formatted with the NTFS file system.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbabe-120">Il disco rigido del computer deve avere un BIOS compatibile con TPM e che supporta i dispositivi USB durante l'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="bbabe-120">The computer’s hard disk must have a BIOS that is compatible with TPM and that supports USB devices during computer startup.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="bbabe-121">Nota</span><span class="sxs-lookup"><span data-stu-id="bbabe-121">Note</span></span></strong><br/><p><span data-ttu-id="bbabe-122">Verificare che la tastiera, il video o il mouse siano direttamente connessi e non gestiti tramite una tastiera, un video o un interruttore del mouse (KVM).</span><span class="sxs-lookup"><span data-stu-id="bbabe-122">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="bbabe-123">Uno switch KVM può interferire con la capacità del computer di rilevare la presenza fisica dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="bbabe-123">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bbabe-124">Se si usa un proxy, deve essere visibile nel contesto di sistema.</span><span class="sxs-lookup"><span data-stu-id="bbabe-124">If you use a proxy, it must be visible in the system context.</span></span> <span data-ttu-id="bbabe-125">MBAM viene eseguito nel contesto di sistema, non nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bbabe-125">MBAM runs under the system context, not the user context.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bbabe-126">Importante</span><span class="sxs-lookup"><span data-stu-id="bbabe-126">Important</span></span>**  
<span data-ttu-id="bbabe-127">Se BitLocker è stato usato senza MBAM, MBAM può essere installato e utilizzare le informazioni esistenti sul TPM.</span><span class="sxs-lookup"><span data-stu-id="bbabe-127">If BitLocker was used without MBAM, MBAM can be installed and utilize the existing TPM information.</span></span>




## <span data-ttu-id="bbabe-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbabe-128">Related topics</span></span>


[<span data-ttu-id="bbabe-129">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bbabe-129">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="bbabe-130">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bbabe-130">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)


## <span data-ttu-id="bbabe-131">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="bbabe-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bbabe-132">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="bbabe-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="bbabe-133">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bbabe-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






