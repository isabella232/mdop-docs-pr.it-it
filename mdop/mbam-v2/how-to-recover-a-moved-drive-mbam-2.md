---
title: Come recuperare un'unità spostata
description: Come recuperare un'unità spostata
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825065"
---
# <span data-ttu-id="89134-103">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="89134-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="89134-104">Quando si trasferisce un'unità del sistema operativo crittografata tramite Microsoft BitLocker Administration and Monitoring (MBAM), l'unità non accetterà il PIN usato in un computer precedente a causa della modifica del chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="89134-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="89134-105">Per usare l'unità spostata, è necessario un modo per ottenere l'ID chiave di ripristino per recuperare la password di ripristino.</span><span class="sxs-lookup"><span data-stu-id="89134-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="89134-106">Usare la procedura seguente per recuperare un'unità spostata.</span><span class="sxs-lookup"><span data-stu-id="89134-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="89134-107">Per recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="89134-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="89134-108">Nel computer che contiene l'unità spostata, avviare il computer in modalità ambiente ripristino Windows (WinRE) o avviare il computer usando il set di strumenti di diagnostica e ripristino Microsoft (DaRT).</span><span class="sxs-lookup"><span data-stu-id="89134-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="89134-109">Dopo aver avviato il computer con WinRE o DaRT, l'amministrazione e il monitoraggio di Microsoft BitLocker considereranno l'unità di sistema operativo spostata come unità dati.</span><span class="sxs-lookup"><span data-stu-id="89134-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="89134-110">MBAM visualizzerà quindi l'ID password di ripristino dell'unità e chiederà la password di ripristino.</span><span class="sxs-lookup"><span data-stu-id="89134-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="89134-111">**Nota**  In alcuni casi, è possibile fare clic su **ho dimenticato il pin** durante il processo di avvio e quindi immettere la modalità di ripristino per visualizzare l'ID chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="89134-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="89134-112">Usare l'ID chiave di ripristino per recuperare la password di ripristino e sbloccare l'unità dal sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="89134-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="89134-113">Se l'unità spostata è stata configurata per l'uso di un chip TPM nel computer originale, è necessario eseguire ulteriori operazioni dopo lo sblocco dell'unità e il completamento del processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="89134-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="89134-114">In modalità WinRE aprire un prompt dei comandi e usare lo strumento **Manage-bde** per decrittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="89134-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="89134-115">L'uso di questo strumento è l'unico modo per rimuovere la protezione del PIN TPM Plus senza il chip TPM originale.</span><span class="sxs-lookup"><span data-stu-id="89134-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="89134-116">Una volta completata la rimozione, avviare il computer in genere.</span><span class="sxs-lookup"><span data-stu-id="89134-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="89134-117">L'agente MBAM implicherà ora il criterio per crittografare l'unità con il PIN TPM Plus del nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="89134-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="89134-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89134-118">Related topics</span></span>


[<span data-ttu-id="89134-119">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="89134-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





