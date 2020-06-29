---
title: Come distribuire il client MBAM a computer desktop o portatili
description: Come distribuire il client MBAM a computer desktop o portatili
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825545"
---
# <span data-ttu-id="a4332-103">Come distribuire il client MBAM a computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="a4332-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="a4332-104">Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a4332-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="a4332-105">Il client MBAM può essere integrato in un'organizzazione distribuendo il client tramite strumenti, ad esempio servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale, ad esempio MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="a4332-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="a4332-106">**Nota**  Per esaminare i requisiti di sistema client di MBAM, vedere [configurazioni supportate di mbam 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a4332-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="a4332-107">Per distribuire il client MBAM in computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="a4332-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="a4332-108">Individuare i file di installazione del client MBAM forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="a4332-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="a4332-109">Distribuire il pacchetto di Windows Installer in computer di destinazione usando servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale, ad esempio MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="a4332-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="a4332-110">**Nota**  Non usare criteri di gruppo per distribuire il pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a4332-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="a4332-111">Configurare le impostazioni di distribuzione o criteri di gruppo per eseguire il file di installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="a4332-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="a4332-112">Dopo aver completato l'installazione, il client MBAM applica le impostazioni dei criteri di gruppo ricevute da un controller di dominio per avviare le funzioni di crittografia e gestione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a4332-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="a4332-113">Per altre informazioni sulle impostazioni dei criteri di gruppo di MBAM, vedere [pianificazione per i requisiti di criteri di gruppo di mbam 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4332-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="a4332-114">**Importante**  Il client MBAM non avvierà le azioni di crittografia BitLocker se è attiva una connessione di protocollo desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a4332-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="a4332-115">Tutte le connessioni della console remota devono essere chiuse prima che venga avviata la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a4332-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="a4332-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4332-116">Related topics</span></span>


[<span data-ttu-id="a4332-117">Distribuzione del client MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a4332-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





