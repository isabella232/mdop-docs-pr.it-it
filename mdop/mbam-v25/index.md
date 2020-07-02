---
title: Microsoft BitLocker Administration and Monitoring 2.5
description: Microsoft BitLocker Administration and Monitoring 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795695"
---
# <span data-ttu-id="54d8f-103">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="54d8f-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 offre un'interfaccia amministrativa semplificata che è possibile usare per gestire la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="54d8f-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="54d8f-105">Si configurano i modelli di criteri di gruppo di MBAM che consentono di impostare le opzioni dei criteri di crittografia unità BitLocker appropriate per l'organizzazione e quindi di usarle per monitorare la conformità del client a tali criteri.</span><span class="sxs-lookup"><span data-stu-id="54d8f-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="54d8f-106">È anche possibile segnalare lo stato di crittografia di un singolo computer e dell'intera organizzazione.</span><span class="sxs-lookup"><span data-stu-id="54d8f-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="54d8f-107">Inoltre, è possibile accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando cambia il BIOS o il record di avvio.</span><span class="sxs-lookup"><span data-stu-id="54d8f-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="54d8f-108">Per una descrizione più dettagliata di MBAM, vedere [informazioni su mbam 2,5](about-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="54d8f-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="54d8f-109">Per ottenere MBAM, vedere [come si fa a ottenere MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span><span class="sxs-lookup"><span data-stu-id="54d8f-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="54d8f-110">Struttura</span><span class="sxs-lookup"><span data-stu-id="54d8f-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="54d8f-111">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="54d8f-112">Informazioni su MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="54d8f-113">Note sulla versione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="54d8f-114">Informazioni su MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="54d8f-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="54d8f-115">Note sulla versione di MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="54d8f-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="54d8f-116">Valutazione di MBAM 2.5 in un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="54d8f-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="54d8f-117">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="54d8f-118">Accessibilità per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="54d8f-119">Pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="54d8f-120">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="54d8f-121">Prerequisiti per la distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="54d8f-122">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="54d8f-123">Pianificazione di gruppi e account di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="54d8f-124">Pianificazione di come proteggere i siti Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="54d8f-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="54d8f-125">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="54d8f-126">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="54d8f-127">Pianificazione della disponibilità elevata per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="54d8f-128">Considerazioni sulla sicurezza per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="54d8f-129">Elenco di controllo per la pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="54d8f-130">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="54d8f-131">Distribuzione dell'infrastruttura server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="54d8f-132">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="54d8f-133">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="54d8f-134">Elenco di controllo per la distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="54d8f-135">Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="54d8f-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="54d8f-136">Rimozione di software o funzionalità del server di MBAM</span><span class="sxs-lookup"><span data-stu-id="54d8f-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="54d8f-137">Operazioni relative a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="54d8f-138">Amministrazione delle funzionalità di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="54d8f-139">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="54d8f-140">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="54d8f-141">Manutenzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="54d8f-142">Uso di Windows PowerShell per l'amministrazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="54d8f-143">Risoluzione dei problemi di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="54d8f-144">Documentazione tecnica per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54d8f-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="54d8f-145">Registri eventi del client</span><span class="sxs-lookup"><span data-stu-id="54d8f-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="54d8f-146">Registri eventi del server</span><span class="sxs-lookup"><span data-stu-id="54d8f-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="54d8f-147">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="54d8f-147">More Information</span></span>

- [<span data-ttu-id="54d8f-148">Esperienza di informazioni su MDOP</span><span class="sxs-lookup"><span data-stu-id="54d8f-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="54d8f-149">Trovare documentazione, video e altre risorse per le tecnologie MDOP.</span><span class="sxs-lookup"><span data-stu-id="54d8f-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="54d8f-150">Guida alla distribuzione di MBAM</span><span class="sxs-lookup"><span data-stu-id="54d8f-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="54d8f-151">Ottenere assistenza nella scelta di un metodo di distribuzione per MBAM, incluse le istruzioni dettagliate per ogni metodo.</span><span class="sxs-lookup"><span data-stu-id="54d8f-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="54d8f-152">Applicare gli hotfix sul server MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="54d8f-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="54d8f-153">Guida di come applicare gli hotfix del server MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="54d8f-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
