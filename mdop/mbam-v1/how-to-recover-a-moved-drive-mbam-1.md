---
title: Come recuperare un'unità spostata
description: Come recuperare un'unità spostata
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804594"
---
# <span data-ttu-id="e87b7-103">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="e87b7-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="e87b7-104">Quando si trasferisce un'unità del sistema operativo crittografata in precedenza con Microsoft BitLocker Administration and Monitoring (MBAM), è necessario risolvere alcuni problemi.</span><span class="sxs-lookup"><span data-stu-id="e87b7-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="e87b7-105">Dopo aver allegato un PIN al nuovo computer, l'unità non accetterà il PIN di avvio usato nel computer precedente.</span><span class="sxs-lookup"><span data-stu-id="e87b7-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="e87b7-106">Il sistema considera non valido il PIN a causa della modifica del chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="e87b7-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="e87b7-107">È necessario ottenere un ID chiave di ripristino per recuperare la password di ripristino per poter usare l'unità spostata.</span><span class="sxs-lookup"><span data-stu-id="e87b7-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="e87b7-108">Per eseguire questa operazione, usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="e87b7-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="e87b7-109">Per recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="e87b7-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="e87b7-110">Nel computer che contiene l'unità spostata, iniziare in modalità ambiente ripristino Windows (WinRE) o avviare il computer usando il set di strumenti di diagnostica e ripristino Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e87b7-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="e87b7-111">Dopo aver avviato il computer con WinRE o DaRT, MBAM tratterà l'unità di sistema operativo spostata come unità dati.</span><span class="sxs-lookup"><span data-stu-id="e87b7-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="e87b7-112">MBAM visualizzerà quindi l'ID password di ripristino dell'unità e chiederà la password di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e87b7-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="e87b7-113">**Nota**  In alcuni casi, potresti essere in grado di fare clic su **dimentica il pin** durante il processo di avvio per accedere alla modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e87b7-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="e87b7-114">In questo articolo viene visualizzato anche l'ID chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e87b7-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="e87b7-115">Nel sito Web Amministrazione MBAM usare l'ID chiave di ripristino per recuperare la password di ripristino e sbloccare l'unità.</span><span class="sxs-lookup"><span data-stu-id="e87b7-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="e87b7-116">Se l'unità spostata è stata configurata per l'uso di un chip TPM nel computer originale, è necessario eseguire ulteriori passaggi dopo l'apertura dell'unità e completare il processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="e87b7-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="e87b7-117">In modalità WinRE aprire un prompt dei comandi e usare lo strumento **Manage-bde** per decrittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="e87b7-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="e87b7-118">L'uso di questo strumento è l'unico modo per rimuovere la protezione TPM-Plus-PIN senza il chip TPM originale.</span><span class="sxs-lookup"><span data-stu-id="e87b7-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="e87b7-119">Al termine della rimozione, avviare il sistema in genere.</span><span class="sxs-lookup"><span data-stu-id="e87b7-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="e87b7-120">L'agente MBAM procederà per applicare il criterio per crittografare l'unità con il PIN TPM Plus del nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="e87b7-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="e87b7-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e87b7-121">Related topics</span></span>


[<span data-ttu-id="e87b7-122">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="e87b7-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





