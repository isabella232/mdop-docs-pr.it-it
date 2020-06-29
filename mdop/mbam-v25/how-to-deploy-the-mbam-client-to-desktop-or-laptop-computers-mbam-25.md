---
title: Come distribuire il client MBAM a computer desktop o portatili
description: Come distribuire il client MBAM a computer desktop o portatili
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824476"
---
# <span data-ttu-id="5d0e2-103">Come distribuire il client MBAM a computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="5d0e2-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="5d0e2-104">Questo argomento spiega come distribuire il client MBAM in modo che i computer degli utenti finiscano.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="5d0e2-105">È possibile distribuire il client MBAM tramite un sistema di distribuzione elettronica del software, ad esempio Active Directory Domain Services o MicrosoftSystemCenterConfiguration Manager.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="5d0e2-106">Per distribuire il client MBAM come parte di una distribuzione di Windows, vedere [come abilitare BitLocker tramite mbam come parte di una distribuzione di Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="5d0e2-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="5d0e2-107">Prima di avviare la distribuzione di MBAM client, esaminare le [configurazioni supportate di mbam 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="5d0e2-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="5d0e2-108">Per distribuire il client MBAM in computer desktop o portatili</span><span class="sxs-lookup"><span data-stu-id="5d0e2-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="5d0e2-109">Individuare i file di installazione del client MBAM forniti con il software MBAM.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="5d0e2-110">Usare servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale come MicrosoftSystemCenterConfiguration Manager per distribuire il pacchetto di Windows Installer in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="5d0e2-111">Configurare le impostazioni di distribuzione o di criteri di gruppo per eseguire il file di installazione del client MBAM.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="5d0e2-112">Dopo aver completato l'installazione, il client MBAM applica le impostazioni dei criteri di gruppo ricevute da un controller di dominio per avviare le funzioni di crittografia e gestione unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="5d0e2-113">**Importante**  Il client MBAM non avvia le azioni di crittografia unità BitLocker se è attiva una connessione di protocollo desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="5d0e2-114">Tutte le connessioni della console remota devono essere chiuse e un utente deve avere effettuato l'accesso a una sessione di console fisica prima dell'inizio della crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5d0e2-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="5d0e2-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d0e2-115">Related topics</span></span>
[<span data-ttu-id="5d0e2-116">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5d0e2-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="5d0e2-117">Pianificazione della distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5d0e2-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="5d0e2-118">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="5d0e2-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5d0e2-119">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="5d0e2-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5d0e2-120">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5d0e2-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





