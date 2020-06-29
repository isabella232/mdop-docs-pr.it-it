---
title: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5
description: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824386"
---
# <span data-ttu-id="ad942-103">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ad942-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="ad942-104">Per distribuire MBAM, è necessario impostare le impostazioni dei criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ad942-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="ad942-105">Per completare questa attività, è necessario copiare i modelli di criteri di gruppo di MBAM in un server o una workstation in grado di eseguire la console Gestione criteri di gruppo o gestione avanzata Criteri di gruppo e quindi modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ad942-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="ad942-106">**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="ad942-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="ad942-107">Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="ad942-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="ad942-108">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ad942-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="ad942-109">Prima di installare il client MBAM, devi copiare oggetti Criteri di gruppo specifici per MBAM nella workstation di gestione.</span><span class="sxs-lookup"><span data-stu-id="ad942-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="ad942-110">Questi GPO definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ad942-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="ad942-111">È possibile copiare i modelli di criteri di gruppo in qualsiasi server o workstation supportato da un computer Windows Server o client e che sia in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ad942-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="ad942-112">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ad942-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="ad942-113">Modifica delle impostazioni GPO di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="ad942-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="ad942-114">Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ad942-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="ad942-115">Per visualizzare e creare oggetti Criteri di gruppo, è necessario che sia installata la console di gestione dei criteri di raggruppamento o Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="ad942-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="ad942-116">Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ad942-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="ad942-117">Visualizzare o nascondere il pannello di controllo di MBAM nel pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="ad942-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="ad942-118">Dato che MBAM offre un pannello di controllo di MBAM personalizzato che può sostituire il pannello di controllo predefinito di Windows BitLocker, puoi anche scegliere di mostrare o nascondere il pannello di controllo predefinito di BitLocker dagli utenti finali usando le impostazioni dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="ad942-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="ad942-119">Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="ad942-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="ad942-120">Altre risorse per la distribuzione di oggetti Criteri di gruppo di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="ad942-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="ad942-121">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ad942-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="ad942-122">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="ad942-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ad942-123">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ad942-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ad942-124">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ad942-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





