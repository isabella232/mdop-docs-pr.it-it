---
title: Configurare i prerequisiti di installazione
description: Configurare i prerequisiti di installazione
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819306"
---
# <span data-ttu-id="a1a7f-103">Configurare i prerequisiti di installazione</span><span class="sxs-lookup"><span data-stu-id="a1a7f-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="a1a7f-104">Le istruzioni seguenti sono prerequisiti per l'installazione e l'uso di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="a1a7f-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="a1a7f-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="a1a7f-106">Aggiornamento di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="a1a7f-107">Configurazione software antivirus/backup</span><span class="sxs-lookup"><span data-stu-id="a1a7f-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="a1a7f-108">Come installare e configurare Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="a1a7f-109">**Importante**  Se nel computer host esiste già una versione di Virtual PC per Windows, è necessario disinstallarla prima di installare Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="a1a7f-110">Per installare Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="a1a7f-111">Scaricare [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) dall'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .</span><span class="sxs-lookup"><span data-stu-id="a1a7f-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="a1a7f-112">Eseguire il file di installazione nel computer host e seguire i passaggi della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="a1a7f-113">**Importante**  Windows Virtual PC include il pacchetto componenti integrativi, che offre funzionalità che migliorano l'interazione tra l'ambiente virtuale e il computer fisico.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="a1a7f-114">Ad esempio, consente di passare al mouse tra l'host e i computer guest.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="a1a7f-115">MED-V richiede l'installazione del pacchetto componenti integrativi.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="a1a7f-116">Come installare e configurare l'aggiornamento di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="a1a7f-117">L'aggiornamento Microsoft associato all'articolo KB977206 Abilita la modalità Windows XP per i computer senza tecnologia HAV (hardware-Assisted Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a1a7f-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="a1a7f-118">È consigliabile installare questo aggiornamento perché alcune funzionalità di integrazione potrebbero non funzionare correttamente se il pacchetto componenti integrativi nel sistema operativo guest non corrisponde alla versione di Windows Virtual PC installata nel computer host.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="a1a7f-119">**Importante**  Non è necessario installare questo aggiornamento quando si installa MED-V nei computer host che eseguono Windows 7 con Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="a1a7f-120">**Suggerimento**  Oltre all'aggiornamento elencato in questo articolo, è consigliabile rivedere tutti gli aggiornamenti di Windows Virtual PC disponibili e applicare gli aggiornamenti appropriati o necessari per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="a1a7f-121">Per installare l'aggiornamento di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="a1a7f-122">Scaricare l'aggiornamento di Windows Virtual PC richiesto dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="a1a7f-123">[aggiornamento a 32 bit](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="a1a7f-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="a1a7f-124">[aggiornamento a 64 bit](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="a1a7f-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="a1a7f-125">Eseguire il file di installazione nel computer host in modalità elevata e seguire i passaggi della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="a1a7f-126">Per altre informazioni sul pacchetto di hotfix per Windows Virtual PC, vedere l' [articolo 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="a1a7f-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="a1a7f-127">Come configurare il software antivirus/backup</span><span class="sxs-lookup"><span data-stu-id="a1a7f-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="a1a7f-128">Per evitare che l'attività antivirus incida sulle prestazioni del desktop virtuale, è consigliabile, dove è possibile, escludere i tipi di file della macchina virtuale seguenti da qualsiasi processo antivirus o di backup in esecuzione nel computer host:</span><span class="sxs-lookup"><span data-stu-id="a1a7f-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="a1a7f-129">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="a1a7f-129">\*.VMC</span></span>

-   <span data-ttu-id="a1a7f-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="a1a7f-130">\*.VUD</span></span>

-   <span data-ttu-id="a1a7f-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="a1a7f-131">\*.VSV</span></span>

-   <span data-ttu-id="a1a7f-132">\*. VHD</span><span class="sxs-lookup"><span data-stu-id="a1a7f-132">\*.VHD</span></span>

## <span data-ttu-id="a1a7f-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1a7f-133">Related topics</span></span>


[<span data-ttu-id="a1a7f-134">Configurare i prerequisiti di ambiente</span><span class="sxs-lookup"><span data-stu-id="a1a7f-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="a1a7f-135">Architettura di alto livello</span><span class="sxs-lookup"><span data-stu-id="a1a7f-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="a1a7f-136">Configurazioni supportate di MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="a1a7f-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





