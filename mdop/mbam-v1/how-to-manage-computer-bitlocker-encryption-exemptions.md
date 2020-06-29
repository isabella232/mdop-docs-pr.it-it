---
title: Come gestire le esenzioni della crittografia BitLocker del computer
description: Come gestire le esenzioni della crittografia BitLocker del computer
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825676"
---
# <span data-ttu-id="8445e-103">Come gestire le esenzioni della crittografia BitLocker del computer</span><span class="sxs-lookup"><span data-stu-id="8445e-103">How to Manage Computer BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="8445e-104">Microsoft BitLocker Administration and Monitoring (MBAM) può essere usato per esentare determinati computer dalla protezione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8445e-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to exempt certain computers from BitLocker protection.</span></span> <span data-ttu-id="8445e-105">Ad esempio, un'organizzazione può decidere di controllare l'esenzione da BitLocker in base al computer.</span><span class="sxs-lookup"><span data-stu-id="8445e-105">For example, an organization may decide to control BitLocker exemption on a computer-by-computer basis.</span></span>

<span data-ttu-id="8445e-106">Per esonerare un computer dalla crittografia BitLocker, è necessario aggiungere il computer a un gruppo di sicurezza in ActiveDirectoryDomainServices per aggirare le regole di protezione di BitLocker basate su computer.</span><span class="sxs-lookup"><span data-stu-id="8445e-106">To exempt a computer from BitLocker encryption, you must add the computer to a security group in ActiveDirectoryDomainServices in order to bypass any computer-based BitLocker protection rules.</span></span>

<span data-ttu-id="8445e-107">**Nota**  Se il computer è già protetto da BitLocker, i criteri di esenzione dal computer non hanno effetto.</span><span class="sxs-lookup"><span data-stu-id="8445e-107">**Note** If the computer is already BitLocker-protected, the computer exemption policy has no effect.</span></span>

 

**<span data-ttu-id="8445e-108">Per esonerare un computer dalla crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="8445e-108">To exempt a computer from BitLocker encryption</span></span>**

1.  <span data-ttu-id="8445e-109">Aggiungere l'account del computer che si vuole esentare da un gruppo di sicurezza in ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="8445e-109">Add the computer account that you want to be exempted to a security group in ActiveDirectoryDomainServices.</span></span> <span data-ttu-id="8445e-110">In questo modo è possibile ignorare le regole di protezione di BitLocker basate su computer.</span><span class="sxs-lookup"><span data-stu-id="8445e-110">This allows you to bypass any computer-based BitLocker protection rules.</span></span>

2.  <span data-ttu-id="8445e-111">Creare un oggetto Criteri di gruppo usando il modello di criteri di gruppo di MBAM, quindi associare l'oggetto Criteri di gruppo al gruppo Active Directory creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="8445e-111">Create a Group Policy Object by using the MBAM Group Policy template, then associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="8445e-112">Per altre informazioni sulla creazione degli oggetti Criteri di gruppo necessari, vedere [distribuzione di oggetti Criteri di gruppo di MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8445e-112">For more information about creating the necessary Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

3.  <span data-ttu-id="8445e-113">Quando viene avviato un computer esentato, il client MBAM controlla l'impostazione dei criteri di esenzione del computer e sospende la protezione in base al fatto che il computer faccia parte del gruppo di sicurezza per l'esenzione da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8445e-113">When an exempted computer starts, the MBAM client checks the Computer Exemption Policy setting and suspends protection based on whether the computer is part of the BitLocker exemption security group.</span></span>

## <span data-ttu-id="8445e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8445e-114">Related topics</span></span>


[<span data-ttu-id="8445e-115">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8445e-115">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





