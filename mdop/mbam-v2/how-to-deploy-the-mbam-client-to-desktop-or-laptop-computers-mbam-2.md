---
title: Come distribuire il client MBAM a computer desktop o portatili
description: Come distribuire il client MBAM a computer desktop o portatili
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804654"
---
# <span data-ttu-id="7056a-103">Come distribuire il client MBAM a computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="7056a-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="7056a-104">Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7056a-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="7056a-105">Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione elettronica del software, ad esempio servizi di dominio Active Directory o MicrosoftSystemCenterConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="7056a-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="7056a-106">**Nota**  Per esaminare i requisiti di sistema per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="7056a-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="7056a-107">Per distribuire il client MBAM in computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="7056a-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="7056a-108">Individuare i file di installazione del client MBAM forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="7056a-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="7056a-109">Usare servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale, come MicrosoftSystemCenterConfigurationManager, per distribuire il pacchetto di Windows Installer in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7056a-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="7056a-110">Configurare le impostazioni di distribuzione o criteri di gruppo per eseguire il file di installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="7056a-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="7056a-111">Dopo aver completato l'installazione, il client MBAM applica le impostazioni dei criteri di gruppo ricevute da un controller di dominio per avviare le funzioni di crittografia e gestione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7056a-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="7056a-112">Per altre informazioni sulle impostazioni dei criteri di gruppo di MBAM, vedere [pianificazione per i requisiti di criteri di gruppo di mbam 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="7056a-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="7056a-113">**Importante**  Il client MBAM non avvierà le azioni di crittografia BitLocker se è attiva una connessione di protocollo desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="7056a-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="7056a-114">Tutte le connessioni della console remota devono essere chiuse prima che venga avviata la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7056a-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="7056a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7056a-115">Related topics</span></span>


[<span data-ttu-id="7056a-116">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7056a-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





