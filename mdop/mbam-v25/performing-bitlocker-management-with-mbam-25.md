---
title: Gestione di BitLocker con MBAM 2.5
description: Gestione di BitLocker con MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826006"
---
# <span data-ttu-id="0673f-103">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0673f-103">Performing BitLocker Management with MBAM 2.5</span></span>


<span data-ttu-id="0673f-104">Dopo aver pianificato e quindi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurarlo e usarlo per gestire la crittografia unità BitLocker in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0673f-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker Drive Encryption across your enterprise.</span></span> <span data-ttu-id="0673f-105">Le informazioni in questa sezione illustrano le attività di gestione della crittografia di BitLocker che si verificano dopo l'installazione e che vengono eseguite con l'amministrazione e il monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0673f-105">The information in this section describes post-installation, day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="0673f-106">Reimpostare un blocco TPM</span><span class="sxs-lookup"><span data-stu-id="0673f-106">Reset a TPM lockout</span></span>


<span data-ttu-id="0673f-107">Un modulo TPM (Trusted Platform Module) è un microchip progettato per ottenere funzioni di base relative alla sicurezza, che coinvolgono principalmente le chiavi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0673f-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="0673f-108">Il TPM viene in genere installato sulla scheda madre di un computer e comunica con il resto del sistema usando una scheda bus host.</span><span class="sxs-lookup"><span data-stu-id="0673f-108">The TPM is usually installed on the motherboard of a computer, and it communicates with the rest of the system by using a host bus adapter.</span></span> <span data-ttu-id="0673f-109">Nei computer che incorporano un TPM è possibile creare chiavi crittografiche e crittografarle in modo che possano essere decrittografate solo dal TPM.</span><span class="sxs-lookup"><span data-stu-id="0673f-109">On computers that incorporate a TPM, you can create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="0673f-110">Se un utente immette il PIN errato troppe volte, può verificarsi un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="0673f-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="0673f-111">Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino per il produttore.</span><span class="sxs-lookup"><span data-stu-id="0673f-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies by manufacturer.</span></span> <span data-ttu-id="0673f-112">Puoi usare MBAM per accedere al sistema di dati di ripristino centralizzato delle chiavi nel sito Web di amministrazione e monitoraggio, in cui puoi recuperare un file di password del proprietario del TPM quando fornisci un ID computer e un Identificativo utente associato.</span><span class="sxs-lookup"><span data-stu-id="0673f-112">You can use MBAM to access the centralized key recovery data system on the Administration and Monitoring Website, where you can retrieve a TPM owner password file when you supply a computer ID and an associated user identifier.</span></span>

[<span data-ttu-id="0673f-113">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="0673f-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-25.md)

## <span data-ttu-id="0673f-114">Recuperare le unità</span><span class="sxs-lookup"><span data-stu-id="0673f-114">Recover drives</span></span>


<span data-ttu-id="0673f-115">Quando si ha a che fare con la crittografia dei dati, in particolare in un ambiente aziendale, valutare il modo in cui i dati possono essere recuperati in caso di errori hardware, modifiche al personale o altre situazioni in cui le chiavi di crittografia possono essere perse.</span><span class="sxs-lookup"><span data-stu-id="0673f-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="0673f-116">Le funzionalità di ripristino delle unità crittografate in MBAM garantiscono che i dati possano essere acquisiti e archiviati e che gli strumenti necessari siano disponibili per accedere a un volume protetto da BitLocker quando BitLocker entra in modalità di ripristino, viene spostato o viene danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0673f-116">The encrypted drive recovery features in MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="0673f-117">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="0673f-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[<span data-ttu-id="0673f-118">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="0673f-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-25.md)

[<span data-ttu-id="0673f-119">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="0673f-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-25.md)

## <span data-ttu-id="0673f-120">Determinare lo stato di crittografia di BitLocker dei computer persi</span><span class="sxs-lookup"><span data-stu-id="0673f-120">Determine BitLocker encryption state of lost computers</span></span>


<span data-ttu-id="0673f-121">Con MBAM puoi determinare l'ultimo stato di crittografia di BitLocker noto dei computer che sono stati persi o rubati.</span><span class="sxs-lookup"><span data-stu-id="0673f-121">By using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="0673f-122">Come determinare lo stato della crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="0673f-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## <span data-ttu-id="0673f-123">Usare il portale self-service per ottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="0673f-123">Use the Self-Service Portal to regain access to a computer</span></span>


<span data-ttu-id="0673f-124">Se gli utenti finali si bloccano in Windows da BitLocker, possono usare le istruzioni in questa sezione per ottenere una chiave di ripristino di BitLocker per riottenere l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="0673f-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="0673f-125">Come usare il portale self-service per riottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="0673f-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## <span data-ttu-id="0673f-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0673f-126">Related topics</span></span>


[<span data-ttu-id="0673f-127">Operazioni relative a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0673f-127">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

 

## <span data-ttu-id="0673f-128">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="0673f-128">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0673f-129">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="0673f-129">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0673f-130">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0673f-130">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





