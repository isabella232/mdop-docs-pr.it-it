---
title: Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0
description: Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804516"
---
# <span data-ttu-id="1d4ee-103">Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1d4ee-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="1d4ee-104">Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 Language release è un aggiornamento di MBAM che include il supporto di nuove lingue.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="1d4ee-105">Le nuove lingue sono:</span><span class="sxs-lookup"><span data-stu-id="1d4ee-105">The new languages are:</span></span>

-   <span data-ttu-id="1d4ee-106">Inglese (en-US)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-106">English (en-us)</span></span>

-   <span data-ttu-id="1d4ee-107">Francese (FR)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-107">French (fr)</span></span>

-   <span data-ttu-id="1d4ee-108">Italiano (it)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-108">Italian (it)</span></span>

-   <span data-ttu-id="1d4ee-109">Tedesco (de)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-109">German (de)</span></span>

-   <span data-ttu-id="1d4ee-110">Spagnolo (es)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-110">Spanish (es)</span></span>

-   <span data-ttu-id="1d4ee-111">Coreano (KO)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-111">Korean (ko)</span></span>

-   <span data-ttu-id="1d4ee-112">Giapponese (ja)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-112">Japanese (ja)</span></span>

-   <span data-ttu-id="1d4ee-113">Portoghese brasiliano (PT-BR)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="1d4ee-114">Russo (RU)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-114">Russian (ru)</span></span>

-   <span data-ttu-id="1d4ee-115">Cinese tradizionale (ZH-TW)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="1d4ee-116">Cinese semplificato (zh-CN)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="1d4ee-117">L'aggiornamento della lingua MBAM 1.0 cambierà il numero di versione da MBAM 1.0.1237.1 a MBAM 1.0.2001.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="1d4ee-118">Non è necessario reinstallare tutte le funzionalità di MBAM per aggiungere altre lingue.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="1d4ee-119">Questo argomento definisce i passaggi necessari per aggiungere le lingue appena supportate.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="1d4ee-120">Distribuire la versione di MBAM International per le funzionalità del server MBAM</span><span class="sxs-lookup"><span data-stu-id="1d4ee-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="1d4ee-121">Per iniziare, è necessario aggiornare le caratteristiche seguenti del server MBAM:</span><span class="sxs-lookup"><span data-stu-id="1d4ee-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="1d4ee-122">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="1d4ee-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="1d4ee-123">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="1d4ee-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="1d4ee-124">Modelli di criteri</span><span class="sxs-lookup"><span data-stu-id="1d4ee-124">Policy Templates</span></span>

<span data-ttu-id="1d4ee-125">Devi quindi eseguire **MbamSetup.exe** per aggiornare le funzionalità di mbam eseguite nello stesso server contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="1d4ee-126">Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="1d4ee-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="1d4ee-127">Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti</span><span class="sxs-lookup"><span data-stu-id="1d4ee-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="1d4ee-128">Installare l'aggiornamento della lingua MBAM per i criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="1d4ee-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="1d4ee-129">I modelli di criteri di gruppo di MBAM possono essere installati in ogni workstation di gestione oppure possono essere copiati nell'archivio centrale di criteri di gruppo, in modo da rendere disponibili i modelli per tutti gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="1d4ee-130">I modelli di criteri non possono essere installati direttamente in un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="1d4ee-131">Se non si usa un archivio centrale di criteri di gruppo, è necessario copiare i criteri manualmente in ogni controller di dominio che gestisce i criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="1d4ee-132">Per aggiungere i modelli dei criteri di linguaggio di MBAM, copiare i file di lingua dei criteri di gruppo da%SystemRoot%\\PolicyDefinitions nel computer in cui è stato installato il ruolo "modelli di criteri" nella stessa posizione nel computer della workstation.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="1d4ee-133">Ecco alcuni esempi di file di criteri di gruppo:</span><span class="sxs-lookup"><span data-stu-id="1d4ee-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="1d4ee-134">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="1d4ee-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="1d4ee-135">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="1d4ee-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="1d4ee-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="1d4ee-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="1d4ee-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="1d4ee-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="1d4ee-138">fr-fr\\ BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="1d4ee-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="1d4ee-139">fr-fr\\ BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="1d4ee-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="1d4ee-140">(e similmente per ogni lingua supportata)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="1d4ee-141">Problemi noti della versione di MBAM International</span><span class="sxs-lookup"><span data-stu-id="1d4ee-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="1d4ee-142">Questo argomento contiene problemi noti per l'amministrazione e il monitoraggio delle versioni internazionali di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="1d4ee-143">Problemi noti nella versione internazionale di MBAM</span><span class="sxs-lookup"><span data-stu-id="1d4ee-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="1d4ee-144">Altre risorse per la distribuzione dell'aggiornamento della lingua MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="1d4ee-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="1d4ee-145">Distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1d4ee-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





