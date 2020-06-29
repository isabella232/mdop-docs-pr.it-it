---
title: Come recuperare un'unità spostata
description: Come recuperare un'unità spostata
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823345"
---
# <span data-ttu-id="cc9d7-103">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="cc9d7-103">How to Recover a Moved Drive</span></span>
<span data-ttu-id="cc9d7-104">Questo argomento spiega come usare il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per recuperare un'unità del sistema operativo che è stata spostata dopo essere stata crittografata da Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to recover an operating system drive that was moved after being encrypted by Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="cc9d7-105">Quando un'unità viene spostata, non accetta più il PIN usato nel computer precedente perché è stato modificato il chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-105">When a drive is moved, it no longer accepts the PIN that was used in the previous computer because the Trusted Platform Module (TPM) chip has changed.</span></span> <span data-ttu-id="cc9d7-106">Per recuperare l'unità spostata, è necessario ottenere l'ID chiave di ripristino per recuperare la password di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-106">To recover the moved drive, you must obtain the recovery key ID to retrieve the recovery password.</span></span>

<span data-ttu-id="cc9d7-107">Per recuperare un'unità spostata, è necessario usare l'area di **recupero unità** del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-107">To recover a moved drive, you must use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="cc9d7-108">Per accedere all'area di **ripristino dell'unità** , è necessario essere assegnati al ruolo degli utenti di mbam helpdesk o al ruolo di utenti avanzati helpdesk di mbam.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-108">To access the **Drive Recovery** area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="cc9d7-109">Per altre informazioni su questi ruoli, vedere [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-109">For more information about these roles, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

**<span data-ttu-id="cc9d7-110">Per recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="cc9d7-110">To recover a moved drive</span></span>**
1.  <span data-ttu-id="cc9d7-111">Nel computer che contiene l'unità spostata, avviare il computer in modalità ambiente ripristino Windows (WinRE) o avviare il computer usando il set di strumenti di diagnostica e ripristino Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-111">On the computer that contains the moved drive, start the computer in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="cc9d7-112">Dopo aver avviato il computer con WinRE o DaRT, MBAM tratterà l'unità di sistema operativo spostata come unità dati fissa.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-112">After the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a fixed data drive.</span></span> <span data-ttu-id="cc9d7-113">MBAM visualizzerà quindi l'ID password di ripristino dell'unità e chiederà la password di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-113">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="cc9d7-114">**Nota**  In alcuni casi, è possibile fare clic su **ho dimenticato il pin** durante il processo di avvio e quindi immettere la modalità di ripristino per visualizzare l'ID chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-114">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="cc9d7-115">Usare l'ID chiave di ripristino per recuperare la password di ripristino e sbloccare l'unità dal sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-115">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring Website.</span></span> <span data-ttu-id="cc9d7-116">Per istruzioni, vedere [come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-116">For instructions, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span></span>

    <span data-ttu-id="cc9d7-117">Se l'unità spostata è stata configurata per l'uso di un chip TPM nel computer originale, completare i passaggi aggiuntivi seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-117">If the moved drive was configured to use a TPM chip on the original computer, complete the following additional steps.</span></span> <span data-ttu-id="cc9d7-118">In caso contrario, il processo di ripristino è completo.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-118">Otherwise, the recovery process is complete.</span></span>

4.  <span data-ttu-id="cc9d7-119">Dopo avere sbloccato l'unità e aver completato il processo di avvio, aprire un prompt dei comandi in modalità WinRE e usare il `manage-bde` comando per decrittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-119">After unlocking the drive and completing the start process, open a command prompt in WinRE mode and use the `manage-bde` command to decrypt the drive.</span></span> <span data-ttu-id="cc9d7-120">L'uso di questo strumento è l'unico modo per rimuovere il TPM più il PIN Protector senza il chip TPM originale.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-120">Using this tool is the only way to remove the TPM plus the PIN protector without the original TPM chip.</span></span> <span data-ttu-id="cc9d7-121">Per informazioni sul `manage-bde` comando, vedere [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-121">For information about the `manage-bde` command, see [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span></span>

5.  <span data-ttu-id="cc9d7-122">Al termine della rimozione, avviare il computer in genere.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-122">When the removal is completed, start the computer normally.</span></span> <span data-ttu-id="cc9d7-123">L'agente MBAM implicherà ora il criterio per crittografare l'unità con il TPM del nuovo computer più il PIN.</span><span class="sxs-lookup"><span data-stu-id="cc9d7-123">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus the PIN.</span></span>



## <span data-ttu-id="cc9d7-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc9d7-124">Related topics</span></span>


[<span data-ttu-id="cc9d7-125">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc9d7-125">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="cc9d7-126">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="cc9d7-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="cc9d7-127">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="cc9d7-128">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="cc9d7-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





