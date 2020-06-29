---
title: Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0
description: Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821216"
---
# <span data-ttu-id="5f212-103">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5f212-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="5f212-104">Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è prima di tutto necessario determinare i criteri di gruppo che verranno usati nell'implementazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="5f212-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="5f212-105">Per altre informazioni sui vari criteri disponibili, vedere [pianificazione per i requisiti dei criteri di gruppo di MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f212-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="5f212-106">Dopo aver determinato i criteri da usare, è necessario usare il modello di criteri di gruppo MBAM 1,0 per creare e distribuire uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="5f212-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="5f212-107">Installare il modello MBAM 1,0 criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="5f212-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="5f212-108">Oltre a fornire funzionalità correlate al server di MBAM, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="5f212-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="5f212-109">Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5f212-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="5f212-110">Come installare il modello Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5f212-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="5f212-111">Distribuire le impostazioni dei criteri di gruppo di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5f212-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="5f212-112">Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5f212-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="5f212-113">Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5f212-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="5f212-114">Visualizzare il pannello di controllo di MBAM in Windows</span><span class="sxs-lookup"><span data-stu-id="5f212-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="5f212-115">Dato che MBAM offre un pannello di controllo di MBAM personalizzato che può sostituire il pannello di controllo predefinito di Windows BitLocker, puoi anche scegliere di nascondere il pannello di controllo predefinito di BitLocker dagli utenti finali usando criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5f212-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="5f212-116">Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="5f212-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="5f212-117">Altre risorse per la distribuzione di oggetti Criteri di gruppo di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="5f212-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="5f212-118">Distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5f212-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





