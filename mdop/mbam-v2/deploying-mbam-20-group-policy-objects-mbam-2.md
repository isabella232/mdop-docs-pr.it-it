---
title: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0
description: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823495"
---
# <span data-ttu-id="96eef-103">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="96eef-103">Deploying MBAM 2.0 Group Policy Objects</span></span>


<span data-ttu-id="96eef-104">Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è necessario prima di tutto determinare i criteri di gruppo che verranno usati nell'implementazione dell'amministrazione e del monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="96eef-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="96eef-105">Per altre informazioni sui diversi criteri disponibili, vedere [pianificazione dei requisiti di criteri di gruppo per MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="96eef-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="96eef-106">Dopo aver determinato i criteri da usare, è necessario creare e distribuire uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri per MBAM tramite il modello di criteri di gruppo di MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="96eef-106">When you have determined the policies that you are going to use, you then must create and deploy one or more Group Policy Objects (GPO) that include the policy settings for MBAM by using the MBAM 2.0 Group Policy template.</span></span>

## <span data-ttu-id="96eef-107">Installare il modello MBAM 2,0 criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="96eef-107">Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="96eef-108">Oltre alle funzionalità di amministrazione e monitoraggio di Microsoft BitLocker correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="96eef-108">In addition to the server-related Microsoft BitLocker Administration and Monitoring features, the server setup application includes a MBAM Group Policy template.</span></span> <span data-ttu-id="96eef-109">Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="96eef-109">This template can be installed on any computer able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="96eef-110">Come installare il modello Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="96eef-110">How to Install the MBAM 2.0 Group Policy Template</span></span>](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## <span data-ttu-id="96eef-111">Distribuire le impostazioni dei criteri di gruppo di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="96eef-111">Deploy MBAM 2.0 Group Policy Settings</span></span>


<span data-ttu-id="96eef-112">Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="96eef-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="96eef-113">Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="96eef-113">How to Edit MBAM 2.0 GPO Settings</span></span>](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## <span data-ttu-id="96eef-114">Visualizzare il pannello di controllo di MBAM in Windows</span><span class="sxs-lookup"><span data-stu-id="96eef-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="96eef-115">Dato che MBAM offre un pannello di controllo di MBAM personalizzato che può sostituire il pannello di controllo predefinito di Windows BitLocker, puoi anche scegliere di nascondere il pannello di controllo predefinito di BitLocker dagli utenti finali usando criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="96eef-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="96eef-116">Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="96eef-116">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## <span data-ttu-id="96eef-117">Altre risorse per la distribuzione di oggetti Criteri di gruppo di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="96eef-117">Other Resources for Deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="96eef-118">Distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="96eef-118">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





