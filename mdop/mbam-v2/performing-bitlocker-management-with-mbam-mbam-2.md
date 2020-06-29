---
title: Gestione di BitLocker con MBAM
description: Gestione di BitLocker con MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826496"
---
# <span data-ttu-id="c1179-103">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="c1179-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="c1179-104">Dopo aver pianificato e quindi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurarlo e usarlo per gestire la crittografia BitLocker aziendale.</span><span class="sxs-lookup"><span data-stu-id="c1179-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="c1179-105">Le informazioni in questa sezione illustrano le attività di gestione delle crittografazioni quotidiane dopo l'installazione che vengono eseguite con l'amministrazione e il monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c1179-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="c1179-106">Reimpostare un blocco TPM tramite MBAM</span><span class="sxs-lookup"><span data-stu-id="c1179-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="c1179-107">Un modulo TPM (Trusted Platform Module) è un microchip progettato per ottenere funzioni di base relative alla sicurezza, che coinvolgono principalmente le chiavi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="c1179-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="c1179-108">Il TPM viene in genere installato sulla scheda madre di un computer o un portatile e comunica con il resto del sistema usando un bus hardware.</span><span class="sxs-lookup"><span data-stu-id="c1179-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="c1179-109">I computer che incorporano un TPM hanno la possibilità di creare chiavi crittografiche e crittografarle in modo che possano essere decrittografate solo dal TPM.</span><span class="sxs-lookup"><span data-stu-id="c1179-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="c1179-110">Se un utente immette il PIN errato troppe volte, può verificarsi un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="c1179-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="c1179-111">Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore.</span><span class="sxs-lookup"><span data-stu-id="c1179-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="c1179-112">Puoi usare MBAM per accedere al sistema di dati di ripristino centralizzato delle chiavi nel sito Web di amministrazione e monitoraggio, in cui puoi recuperare un file di password del proprietario del TPM quando fornisci un ID computer e un Identificativo utente associato.</span><span class="sxs-lookup"><span data-stu-id="c1179-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="c1179-113">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="c1179-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="c1179-114">Recuperare le unità con MBAM</span><span class="sxs-lookup"><span data-stu-id="c1179-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="c1179-115">Quando si ha a che fare con la crittografia dei dati, in particolare in un ambiente aziendale, valutare il modo in cui i dati possono essere recuperati in caso di errori hardware, modifiche al personale o altre situazioni in cui le chiavi di crittografia possono essere perse.</span><span class="sxs-lookup"><span data-stu-id="c1179-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="c1179-116">Le caratteristiche di ripristino delle unità crittografate di MBAM garantiscono che i dati possano essere acquisiti e archiviati e che gli strumenti necessari siano disponibili per accedere a un volume protetto da BitLocker quando BitLocker entra in modalità di ripristino, viene spostato o viene danneggiato.</span><span class="sxs-lookup"><span data-stu-id="c1179-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="c1179-117">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="c1179-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="c1179-118">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="c1179-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="c1179-119">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="c1179-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="c1179-120">Determinare lo stato di crittografia di BitLocker dei computer persi usando MBAM</span><span class="sxs-lookup"><span data-stu-id="c1179-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="c1179-121">Usando MBAM, puoi determinare l'ultimo stato di crittografia di BitLocker noto dei computer che sono stati persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="c1179-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="c1179-122">Come determinare lo stato della crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="c1179-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="c1179-123">Usare il portale self-service per ottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="c1179-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="c1179-124">Se gli utenti finali si bloccano in Windows da BitLocker, possono usare le istruzioni in questa sezione per ottenere una chiave di ripristino di BitLocker per riottenere l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="c1179-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="c1179-125">Come usare il portale self-service per riottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="c1179-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="c1179-126">Altre risorse per eseguire la gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="c1179-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="c1179-127">Operazioni relative a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c1179-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





