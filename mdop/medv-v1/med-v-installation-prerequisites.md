---
title: Prerequisiti per l'installazione di MED-V
description: Prerequisiti per l'installazione di MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824966"
---
# <span data-ttu-id="1da7a-103">Prerequisiti per l'installazione di MED-V</span><span class="sxs-lookup"><span data-stu-id="1da7a-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="1da7a-104">Di seguito sono riportati i prerequisiti per l'installazione di MED-V:</span><span class="sxs-lookup"><span data-stu-id="1da7a-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="1da7a-105">Requisiti di Active Directory</span><span class="sxs-lookup"><span data-stu-id="1da7a-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="1da7a-106">Database report</span><span class="sxs-lookup"><span data-stu-id="1da7a-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="1da7a-107">Configurazione software antivirus/backup</span><span class="sxs-lookup"><span data-stu-id="1da7a-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="1da7a-108">Microsoft Virtual PC 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="1da7a-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="1da7a-109">Requisiti di Active Directory</span><span class="sxs-lookup"><span data-stu-id="1da7a-109">Active Directory Requirements</span></span>


<span data-ttu-id="1da7a-110">Quando si configura il server MED-V, se gli utenti non fanno parte dello stesso dominio a cui appartiene il server, è necessario impostare un trust tra i domini.</span><span class="sxs-lookup"><span data-stu-id="1da7a-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="1da7a-111">Come installare il database del report</span><span class="sxs-lookup"><span data-stu-id="1da7a-111">How to Install the Report Database</span></span>


<span data-ttu-id="1da7a-112">Il database del report è necessario per archiviare tutti i registri dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="1da7a-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="1da7a-113">Il database del log viene quindi usato per generare report MED-V.</span><span class="sxs-lookup"><span data-stu-id="1da7a-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="1da7a-114">Per informazioni sui report, vedere [report di MED-V](med-v-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="1da7a-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="1da7a-115">SQL Server può essere installato nello stesso server del server MED-V o in un server remoto.</span><span class="sxs-lookup"><span data-stu-id="1da7a-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="1da7a-116">Se si esegue l'installazione in un server remoto, vedere [installazione di SQL Server in un server remoto](#bkmk-installingsqlserveronaremoteserver).</span><span class="sxs-lookup"><span data-stu-id="1da7a-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="1da7a-117">Installazione di SQL Server in un server remoto</span><span class="sxs-lookup"><span data-stu-id="1da7a-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="1da7a-118">Per installare SQL Server in un server remoto</span><span class="sxs-lookup"><span data-stu-id="1da7a-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="1da7a-119">Configurare le operazioni seguenti nel server remoto:</span><span class="sxs-lookup"><span data-stu-id="1da7a-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="1da7a-120">Nome istanza: istanza predefinita</span><span class="sxs-lookup"><span data-stu-id="1da7a-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="1da7a-121">Modalità di autenticazione: modalità mista</span><span class="sxs-lookup"><span data-stu-id="1da7a-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="1da7a-122">Utente: l'utente predefinito creato è "sa"</span><span class="sxs-lookup"><span data-stu-id="1da7a-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="1da7a-123">Password: password desiderata</span><span class="sxs-lookup"><span data-stu-id="1da7a-123">Password—Desired password</span></span>

    -   <span data-ttu-id="1da7a-124">Impostazioni regole di confronto: impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="1da7a-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="1da7a-125">Errore nelle impostazioni del report utilizzo: impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="1da7a-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="1da7a-126">Installare i file seguenti nel server MED-V:</span><span class="sxs-lookup"><span data-stu-id="1da7a-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="1da7a-127">Per installare i prerequisiti per la raccolta di oggetti Management Pack per Microsoft SQL Server2008, scaricare [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1da7a-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="1da7a-128">Per installare i prerequisiti per la raccolta di oggetti Management Pack per Microsoft SQL Server2005, scaricare [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1da7a-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="1da7a-129">Per installare i file dll necessari per Microsoft SQL Server2008, scaricare [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1da7a-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="1da7a-130">Per installare i file dll necessari per Microsoft SQL Server2005, scaricare [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1da7a-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="1da7a-131">Per installare i pacchetti di installazione autonomi che offrono un valore aggiuntivo per SQL Server2008, scaricare il [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1da7a-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="1da7a-132">Per installare i pacchetti di installazione autonomi che offrono un valore aggiuntivo per SQL Server2005, scaricare il [Feature Pack per Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1da7a-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="1da7a-133">Per altre informazioni su questi file, vedere [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) nell'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) o [Feature Pack per Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) nell'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="1da7a-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="1da7a-134">Configurazione software antivirus/backup</span><span class="sxs-lookup"><span data-stu-id="1da7a-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="1da7a-135">Per evitare che l'attività antivirus incida sulle prestazioni del desktop virtuale, è consigliabile escludere i tipi di file della macchina virtuale seguenti da qualsiasi elaborazione di antivirus o backup in esecuzione nell'host:</span><span class="sxs-lookup"><span data-stu-id="1da7a-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="1da7a-136">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="1da7a-136">\*.VMC</span></span>

-   <span data-ttu-id="1da7a-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="1da7a-137">\*.VUD</span></span>

-   <span data-ttu-id="1da7a-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="1da7a-138">\*.VSV</span></span>

-   <span data-ttu-id="1da7a-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="1da7a-139">\*.CKM</span></span>

-   <span data-ttu-id="1da7a-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="1da7a-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="1da7a-141">Come installare e configurare Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="1da7a-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="1da7a-142">**Importante**  Se nel computer host è presente Virtual PC per Windows, disinstallarlo prima di installare Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1da7a-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="1da7a-143">Per installare Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="1da7a-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="1da7a-144">Scaricare Virtual PC2007 SP1 dall'area download Microsoft [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span><span class="sxs-lookup"><span data-stu-id="1da7a-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="1da7a-145">Eseguire il file di installazione nel computer host e seguire la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="1da7a-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="1da7a-146">Installare l'aggiornamento di Virtual PC2007 SP1 nel computer host in modalità elevata.</span><span class="sxs-lookup"><span data-stu-id="1da7a-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="1da7a-147">Per altre informazioni, vedere [la descrizione del pacchetto di hotfix per Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span><span class="sxs-lookup"><span data-stu-id="1da7a-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="1da7a-148">**Nota**  È necessario l'aggiornamento virtuale di PC2007 SP1 per l'uso di Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="1da7a-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="1da7a-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1da7a-149">Related topics</span></span>


[<span data-ttu-id="1da7a-150">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="1da7a-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





