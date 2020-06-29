---
title: Applicazione di hotfix su MBAM 2.5 SP1
description: Applicazione di hotfix su MBAM 2.5 SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824186"
---
# <span data-ttu-id="735a6-103">Applicazione di hotfix su MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="735a6-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="735a6-104">Questo argomento descrive il processo per l'applicazione degli hotfix per Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="735a6-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="735a6-105">Prima di iniziare, scaricare l'hotfix più recente di Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="735a6-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="735a6-106">Pacchetto di ottimizzazione desktop</span><span class="sxs-lookup"><span data-stu-id="735a6-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="735a6-107">Per altre informazioni sulle versioni di hotfix, vedere il [grafico mbam Version](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span><span class="sxs-lookup"><span data-stu-id="735a6-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="735a6-108">Procedura per aggiornare il server MBAM per l'ambiente attuale MBAM</span><span class="sxs-lookup"><span data-stu-id="735a6-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="735a6-109">Rimuovere la caratteristica del server MBAM (eseguire questa operazione aprendo lo strumento di configurazione del server MBAM, quindi selezionando Rimuovi funzionalità).</span><span class="sxs-lookup"><span data-stu-id="735a6-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="735a6-110">Rimuovere MDOP MBAM dal pannello di controllo | Programmi e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="735a6-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="735a6-111">Installare i componenti del server di MBAM 2,5 SP1 RTM.</span><span class="sxs-lookup"><span data-stu-id="735a6-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="735a6-112">Installare l'ultimo aggiornamento cumulativo di MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="735a6-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="735a6-113">Configurare le caratteristiche di MBAM con MBAM Server Configurator.</span><span class="sxs-lookup"><span data-stu-id="735a6-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="735a6-114">Procedura per installare il nuovo hotfix per il server MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="735a6-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="735a6-115">Fare riferimento al documento per l'installazione di un [nuovo server](deploying-the-mbam-25-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="735a6-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
