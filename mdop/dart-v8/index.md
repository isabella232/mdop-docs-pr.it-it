---
title: Guida dell'amministratore di Diagnostics and Recovery Toolset 8
description: Guida dell'amministratore di Diagnostics and Recovery Toolset 8
author: dansimp
ms.assetid: 33685dd7-844f-4864-b504-3ef384ef01de
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2017
ms.openlocfilehash: c4f4e7cb49b89759acc4c3c738ff74a4a197b120
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795740"
---
# <span data-ttu-id="e5fcf-103">Guida dell'amministratore di Diagnostics and Recovery Toolset 8</span><span class="sxs-lookup"><span data-stu-id="e5fcf-103">Diagnostics and Recovery Toolset 8 Administrator's Guide</span></span>


<span data-ttu-id="e5fcf-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 consente di diagnosticare e ripristinare un computer che non può essere avviato o che ha problemi di avvio come previsto.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you diagnose and repair a computer that cannot be started or that has problems starting as expected.</span></span> <span data-ttu-id="e5fcf-105">Usando DaRT 8,0, puoi recuperare i computer degli utenti finali che sono diventati inutilizzabili, diagnosticare probabili cause di problemi e ripristinare rapidamente i computer non avviabili o bloccati.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-105">By using DaRT 8.0, you can recover end-user computers that have become unusable, diagnose probable causes of issues, and quickly repair unbootable or locked-out computers.</span></span> <span data-ttu-id="e5fcf-106">Quando necessario, è anche possibile ripristinare rapidamente i file persi importanti e rilevare e rimuovere il malware, anche quando il computer non è online.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-106">When it is necessary, you can also quickly restore important lost files and detect and remove malware, even when the computer is not online.</span></span>

<span data-ttu-id="e5fcf-107">DaRT 8,0 consente di creare un'immagine di ripristino DaRT nei formati di file ISO (International Organization for Standardizzation) e Windows Imaging (WIM) e di masterizzare l'immagine in un CD, un DVD o un USB.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-107">DaRT 8.0 lets you create a DaRT recovery image in International Organization for Standardization (ISO) and Windows Imaging (WIM) file formats and burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="e5fcf-108">È quindi possibile usare i file di immagine di ripristino e distribuirli localmente o in una partizione remota o in una partizione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-108">You can then use the recovery image files and deploy them locally or to a remote partition or a recovery partition.</span></span>

<span data-ttu-id="e5fcf-109">DaRT 8,0 è una parte importante di Microsoft Desktop Optimization Pack (MDOP), una soluzione dinamica disponibile per i clienti di Software Assurance che consente di ridurre i costi di installazione del software, consente il recapito delle applicazioni come servizi e consente di gestire e controllare gli ambienti desktop aziendali.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-109">DaRT 8.0 is an important part of the Microsoft Desktop Optimization Pack (MDOP), a dynamic solution available to Software Assurance customers that helps reduce software installation costs, enables delivery of applications as services, and helps manage and control enterprise desktop environments.</span></span>

<a href="" id="getting-started-with-dart-8-0"></a>[<span data-ttu-id="e5fcf-110">Attività iniziali di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-110">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)  

<span data-ttu-id="e5fcf-111">[Informazioni su DaRT 8,0](about-dart-80-dart-8.md) **|** [Note sulla versione di DaRT 8,0](release-notes-for-dart-80--dart-8.md) **|** [Informazioni su DaRT 8,0 SP1](about-dart-80-sp1.md) **|** [Note sulla versione per DaRT 8,0 SP1](release-notes-for-dart-80-sp1.md) **|** [Informazioni su DaRT 8,1](about-dart-81.md) **|** [Note sulla versione di DaRT 8,1](release-notes-for-dart-81.md) **|** [Panoramica degli strumenti in DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md) **|** [Accessibilità per DaRT 8,0](accessibility-for-dart-80-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="e5fcf-111">[About DaRT 8.0](about-dart-80-dart-8.md)**|**[Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md)**|**[About DaRT 8.0 SP1](about-dart-80-sp1.md)**|**[Release Notes for DaRT 8.0 SP1](release-notes-for-dart-80-sp1.md)**|**[About DaRT 8.1](about-dart-81.md)**|**[Release Notes for DaRT 8.1](release-notes-for-dart-81.md)**|**[Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md)**|**[Accessibility for DaRT 8.0](accessibility-for-dart-80-dart-8.md)</span></span>

<a href="" id="planning-for-dart-8-0"></a>[<span data-ttu-id="e5fcf-112">Pianificazione di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-112">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)  

<span data-ttu-id="e5fcf-113">[Pianificazione della distribuzione di DaRT 8,0](planning-to-deploy-dart-80-dart-8.md) **|** Configurazioni supportate di [DaRT 8,0](dart-80-supported-configurations-dart-8.md) **|** [Pianificazione della creazione dell'immagine di ripristino di DaRT 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md) **|** [Pianificare come salvare e distribuire l'immagine](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md) **|** di ripristino di Dart 8,0 [Elenco di controllo della pianificazione di DaRT 8,0](dart-80-planning-checklist-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="e5fcf-113">[Planning to Deploy DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)**|**[DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md)**|**[Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md)**|**[Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md)**|**[DaRT 8.0 Planning Checklist](dart-80-planning-checklist-dart-8.md)</span></span>

<a href="" id="deploying-dart-8-0"></a>[<span data-ttu-id="e5fcf-114">Distribuzione di DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-114">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)  

<span data-ttu-id="e5fcf-115">[Distribuzione di DaRT 8,0 ai computer](deploying-dart-80-to-administrator-computers-dart-8.md) **|** dell'amministratore [Creazione dell'immagine](creating-the-dart-80-recovery-image-dart-8.md) **|** di ripristino di Dart 8,0 [Distribuzione dell'immagine](deploying-the-dart-recovery-image-dart-8.md) **|** di ripristino delle freccette [Elenco di controllo della distribuzione di DaRT 8,0](dart-80-deployment-checklist-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="e5fcf-115">[Deploying DaRT 8.0 to Administrator Computers](deploying-dart-80-to-administrator-computers-dart-8.md)**|**[Creating the DaRT 8.0 Recovery Image](creating-the-dart-80-recovery-image-dart-8.md)**|**[Deploying the DaRT Recovery Image](deploying-the-dart-recovery-image-dart-8.md)**|**[DaRT 8.0 Deployment Checklist](dart-80-deployment-checklist-dart-8.md)</span></span>

<a href="" id="operations-for-dart-8-0"></a>[<span data-ttu-id="e5fcf-116">Operazioni relative a DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-116">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)  

<span data-ttu-id="e5fcf-117">[Recupero di computer con dardo 8,0](recovering-computers-using-dart-80-dart-8.md) **|** [Diagnostica degli errori di sistema con Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md) **|** [Sicurezza e privacy per DaRT 8,0](security-and-privacy-for-dart-80-dart-8.md) **|** [Amministrazione di DaRT 8,0 tramite PowerShell](administering-dart-80-using-powershell-dart-8.md)</span><span class="sxs-lookup"><span data-stu-id="e5fcf-117">[Recovering Computers Using DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)**|**[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)**|**[Security and Privacy for DaRT 8.0](security-and-privacy-for-dart-80-dart-8.md)**|**[Administering DaRT 8.0 Using PowerShell](administering-dart-80-using-powershell-dart-8.md)</span></span>

<a href="" id="technical-reference-for-dart-8-0"></a>[<span data-ttu-id="e5fcf-118">Riferimento tecnico per DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-118">Technical Reference for DaRT 8.0</span></span>](technical-reference-for-dart-80-new-ia.md)  

[<span data-ttu-id="e5fcf-119">Microsoft Diagnostics and Recovery Toolset (DaRT) gli utenti devono usare Microsoft Defender offline (WDO) per il rilevamento di malware-></span><span class="sxs-lookup"><span data-stu-id="e5fcf-119">Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection--></span></span>](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md)

<a href="" id="troubleshooting-dart-8-0"></a>[<span data-ttu-id="e5fcf-120">Risoluzione dei problemi relativi a DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-120">Troubleshooting DaRT 8.0</span></span>](troubleshooting-dart-80-dart-8.md)  

### <span data-ttu-id="e5fcf-121">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="e5fcf-121">More Information</span></span>

<a href="" id="how-do-i-get-mdop"></a>[<span data-ttu-id="e5fcf-122">Come si ottiene MDOP</span><span class="sxs-lookup"><span data-stu-id="e5fcf-122">How Do I Get MDOP</span></span>](https://go.microsoft.com/fwlink/?LinkId=322049)  
<span data-ttu-id="e5fcf-123">Ottenere informazioni su come scaricare dardo.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-123">Get information about how to download DaRT.</span></span>

<a href="" id="release-notes-for-dart-8-0"></a>[<span data-ttu-id="e5fcf-124">Note sulla versione per DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="e5fcf-124">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)  
<span data-ttu-id="e5fcf-125">Visualizzare le informazioni aggiornate sui prodotti e i problemi noti per DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-125">View updated product information and known issues for DaRT 8.0.</span></span>

<a href="" id="mdop-techcenter-page"></a>[<span data-ttu-id="e5fcf-126">Pagina TechCenter di MDOP</span><span class="sxs-lookup"><span data-stu-id="e5fcf-126">MDOP TechCenter Page</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=225286)  
<span data-ttu-id="e5fcf-127">Scopri le informazioni e le risorse più recenti di MDOP.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-127">Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a>[<span data-ttu-id="e5fcf-128">Esperienza di informazioni su MDOP</span><span class="sxs-lookup"><span data-stu-id="e5fcf-128">MDOP Information Experience</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=236032)  
<span data-ttu-id="e5fcf-129">Trovare documentazione, video e altre risorse per le tecnologie MDOP.</span><span class="sxs-lookup"><span data-stu-id="e5fcf-129">Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="e5fcf-130">È anche possibile [inviare commenti e suggerimenti](mailto:MDOPDocs@microsoft.com)o informazioni sugli aggiornamenti seguendoli su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="e5fcf-130">You can also [send us feedback](mailto:MDOPDocs@microsoft.com), or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

 

 





