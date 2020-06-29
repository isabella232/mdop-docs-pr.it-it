---
title: Gestione di BitLocker con MBAM
description: Gestione di BitLocker con MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825895"
---
# <span data-ttu-id="178d2-103">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="178d2-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="178d2-104">Dopo la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurare e usare MBAM per gestire la crittografia BitLocker aziendale.</span><span class="sxs-lookup"><span data-stu-id="178d2-104">After you deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="178d2-105">In questa sezione vengono illustrate le attività di gestione delle crittografazioni post-installazione, quotidiane, che possono essere eseguite tramite MBAM.</span><span class="sxs-lookup"><span data-stu-id="178d2-105">This section describes post-installation, day-to-day BitLocker encryption management tasks that can be accomplished by using MBAM.</span></span>

## <span data-ttu-id="178d2-106">Reimpostare un blocco TPM con MBAM</span><span class="sxs-lookup"><span data-stu-id="178d2-106">Reset a TPM Lockout with MBAM</span></span>


<span data-ttu-id="178d2-107">Un microchip TPM (Trusted Platform Module) offre funzioni di base relative alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="178d2-107">A Trusted Platform Module (TPM) microchip provides basic security-related functions.</span></span> <span data-ttu-id="178d2-108">Queste funzioni vengono eseguite principalmente dall'uso di chiavi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="178d2-108">These functions are accomplished primarily by the use of encryption keys.</span></span> <span data-ttu-id="178d2-109">Il TPM viene in genere installato sulla scheda madre di un computer o un portatile e comunica con il resto del sistema usando un bus hardware.</span><span class="sxs-lookup"><span data-stu-id="178d2-109">The TPM is typically installed on the motherboard of a computer or laptop and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="178d2-110">I computer che incorporano un TPM possono creare chiavi crittografiche che possono essere decrittografate solo dal TPM.</span><span class="sxs-lookup"><span data-stu-id="178d2-110">Computers that incorporate a TPM can create cryptographic keys that can be decrypted only by the TPM.</span></span> <span data-ttu-id="178d2-111">Se un utente immette un PIN errato troppo spesso, può verificarsi un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="178d2-111">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="178d2-112">Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore.</span><span class="sxs-lookup"><span data-stu-id="178d2-112">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="178d2-113">Il sistema di dati di ripristino chiave nel sito Web di amministrazione di MBAM consente di ottenere un file di password del proprietario del TPM reimpostato.</span><span class="sxs-lookup"><span data-stu-id="178d2-113">The Key Recovery data system on the MBAM administration website enables you to obtain a reset TPM owner password file.</span></span>

[<span data-ttu-id="178d2-114">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="178d2-114">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-1.md)

## <span data-ttu-id="178d2-115">Recuperare le unità con MBAM</span><span class="sxs-lookup"><span data-stu-id="178d2-115">Recover drives with MBAM</span></span>


<span data-ttu-id="178d2-116">Verificare di essere in grado di provare il recupero di dati da unità crittografate in caso di errori hardware, modifiche al personale o altre situazioni in cui le chiavi di crittografia andranno perse.</span><span class="sxs-lookup"><span data-stu-id="178d2-116">Make sure that you know how to attempt data recovery from encrypted drives in the event of hardware failure, changes in personnel, or other situations in which encryption keys are lost.</span></span> <span data-ttu-id="178d2-117">Le caratteristiche di ripristino delle unità crittografate di MBAM consentono di acquisire e archiviare i dati e la disponibilità di strumenti necessari per accedere a un volume protetto da BitLocker quando il volume entra in modalità di ripristino, viene spostato o viene danneggiato.</span><span class="sxs-lookup"><span data-stu-id="178d2-117">The Encrypted Drive Recovery features of MBAM provide the capture and storage of data and availability of tools required to access a BitLocker-protected volume when the volume goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="178d2-118">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="178d2-118">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[<span data-ttu-id="178d2-119">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="178d2-119">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-1.md)

[<span data-ttu-id="178d2-120">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="178d2-120">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-1.md)

## <span data-ttu-id="178d2-121">Determinare lo stato di crittografia di BitLocker dei computer persi usando MBAM</span><span class="sxs-lookup"><span data-stu-id="178d2-121">Determine BitLocker Encryption State of lost computers by Using MBAM</span></span>


<span data-ttu-id="178d2-122">Quando si usa MBAM, è possibile determinare l'ultimo stato di crittografia di BitLocker noto dei computer persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="178d2-122">When you use MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="178d2-123">Come determinare lo stato di crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="178d2-123">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## <span data-ttu-id="178d2-124">Altre risorse per eseguire la gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="178d2-124">Other resources for performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="178d2-125">Operazioni relative a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="178d2-125">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





