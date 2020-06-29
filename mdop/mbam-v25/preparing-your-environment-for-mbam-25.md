---
title: Preparazione dell'ambiente per MBAM 2.5
description: Preparazione dell'ambiente per MBAM 2.5
author: dansimp
ms.assetid: 7552ba08-9dbf-40cd-8920-203d733fd242
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b18c9853035018c2e36dd447fbf0effbf49c45cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825495"
---
# <span data-ttu-id="31620-103">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="31620-103">Preparing your Environment for MBAM 2.5</span></span>


<span data-ttu-id="31620-104">Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di avere soddisfatto i prerequisiti per installare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="31620-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="31620-105">Quando si sa quali sono i prerequisiti in anticipo, è possibile distribuire il prodotto in modo efficiente e abilitarne le funzionalità per consentire il supporto più efficace degli obiettivi aziendali dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="31620-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="31620-106">Se si distribuisce l'amministrazione e il monitoraggio di Microsoft BitLocker con Configuration Manager, verificare di soddisfare i requisiti aggiuntivi per Configuration Manager, elencati più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="31620-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Configuration Manager, ensure that you meet the additional requirements for Configuration Manager, which are listed later in this topic.</span></span>

## <span data-ttu-id="31620-107">Verificare i prerequisiti di distribuzione di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="31620-107">Review MBAM 2.5 deployment prerequisites</span></span>


<span data-ttu-id="31620-108">Per assicurarti che la distribuzione di MBAM abbia successo, assicurati di rivedere e completare i prerequisiti software necessari prima di installare il client MBAM e configurare le funzionalità del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="31620-108">To ensure that your MBAM deployment is successful, make sure that you review and complete the required software prerequisites before you install the MBAM Client and configure the MBAM Server features.</span></span>

[<span data-ttu-id="31620-109">Prerequisiti per la distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="31620-109">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)

## <span data-ttu-id="31620-110">Pianificare i requisiti di criteri di gruppo di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="31620-110">Plan for MBAM 2.5 Group Policy requirements</span></span>


<span data-ttu-id="31620-111">Prima di MBAM in grado di gestire i client nell'organizzazione, è necessario scaricare e configurare i modelli di criteri di gruppo specifici di MBAM e quindi configurare le impostazioni dei criteri di gruppo desiderate per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="31620-111">Before MBAM can manage clients in the enterprise, you must download and configure Group Policy templates that are specific to MBAM, and then configure the Group Policy settings that you want for your environment.</span></span>

[<span data-ttu-id="31620-112">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="31620-112">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

## <span data-ttu-id="31620-113">Pianificare i ruoli e gli account di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="31620-113">Plan for MBAM 2.5 roles and accounts</span></span>


<span data-ttu-id="31620-114">Come parte dei prerequisiti, devi definire determinati ruoli e account, che vengono usati in MBAM per concedere diritti di sicurezza e accesso a server e funzionalità specifici, ad esempio i database in uso in SQL Server e le applicazioni Web in uso nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="31620-114">As part of the prerequisites, you must define certain roles and accounts, which are used in MBAM to provide security and access rights to specific servers and features, such as the databases running on SQL Server and the web applications running on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="31620-115">Pianificazione di gruppi e account di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="31620-115">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)

## <span data-ttu-id="31620-116">Altre risorse per la pianificazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="31620-116">Other resources for MBAM planning</span></span>


[<span data-ttu-id="31620-117">Pianificazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="31620-117">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="31620-118">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="31620-118">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="31620-119">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="31620-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="31620-120">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="31620-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="31620-121">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="31620-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





