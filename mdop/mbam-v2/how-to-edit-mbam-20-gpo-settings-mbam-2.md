---
title: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0
description: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824086"
---
# <span data-ttu-id="a8805-103">Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a8805-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="a8805-104">Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è necessario prima di tutto determinare i criteri di gruppo che verranno usati nell'implementazione dell'amministrazione e del monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a8805-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="a8805-105">Per altre informazioni sui diversi criteri disponibili, vedere [pianificazione dei requisiti di criteri di gruppo per MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) .</span><span class="sxs-lookup"><span data-stu-id="a8805-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="a8805-106">Dopo aver determinato i criteri che si intende usare, è necessario modificare uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri per MBAM.</span><span class="sxs-lookup"><span data-stu-id="a8805-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="a8805-107">È possibile usare la procedura seguente per configurare le impostazioni di GPO di base consigliate per consentire a MBAM di gestire la crittografia BitLocker per i computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a8805-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="a8805-108">Per modificare le impostazioni del GPO client MBAM</span><span class="sxs-lookup"><span data-stu-id="a8805-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="a8805-109">In un computer in cui è installato il modello di criteri di gruppo di MBAM verificare che i servizi MBAM siano abilitati.</span><span class="sxs-lookup"><span data-stu-id="a8805-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="a8805-110">Usando la console Gestione criteri di gruppo (GPMC. msc) o il prodotto MDOP Advanced Group Policy Management in un computer in cui è installato il modello di criteri di gruppo di MBAM, selezionare **Configurazione computer**, scegliere **criteri**, **modelli amministrativi**, **componenti di Windows**e quindi fare clic su **MDOP mbam (Gestione BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="a8805-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="a8805-111">Modificare le impostazioni degli oggetti Criteri di gruppo necessarie per abilitare i servizi client di MBAM nei computer client.</span><span class="sxs-lookup"><span data-stu-id="a8805-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="a8805-112">Per ogni criterio nella tabella seguente selezionare **gruppo criteri**, fare clic sul **criterio**e quindi configurare l' **impostazione**:</span><span class="sxs-lookup"><span data-stu-id="a8805-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a8805-113">Gruppo criteri</span><span class="sxs-lookup"><span data-stu-id="a8805-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="a8805-114">Criterio</span><span class="sxs-lookup"><span data-stu-id="a8805-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="a8805-115">Impostazione</span><span class="sxs-lookup"><span data-stu-id="a8805-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a8805-116">Gestione dei client</span><span class="sxs-lookup"><span data-stu-id="a8805-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-117">Configurare i servizi MBAM</span><span class="sxs-lookup"><span data-stu-id="a8805-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-118">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8805-118">Enabled.</span></span> <span data-ttu-id="a8805-119">Impostare l' <strong> endpoint del servizio hardware e ripristino </strong> di mbam e <strong> selezionare informazioni di ripristino di BitLocker da archiviare </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8805-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="a8805-120">Impostare l' <strong> endpoint del servizio </strong> di conformità mbam e immettere la frequenza del rapporto di stato in (minuti).</span><span class="sxs-lookup"><span data-stu-id="a8805-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a8805-121">Unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a8805-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-122">Impostazioni di crittografia unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a8805-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-123">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8805-123">Enabled.</span></span> <span data-ttu-id="a8805-124">Impostare <strong> Seleziona protezione per l'unità del sistema operativo </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8805-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="a8805-125">Necessario per salvare i dati dell'unità del sistema operativo nel server di ripristino MBAMKey.</span><span class="sxs-lookup"><span data-stu-id="a8805-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a8805-126">Unità rimovibile</span><span class="sxs-lookup"><span data-stu-id="a8805-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-127">Controllare l'uso di BitLocker su unità rimovibili</span><span class="sxs-lookup"><span data-stu-id="a8805-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-128">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8805-128">Enabled.</span></span> <span data-ttu-id="a8805-129">Obbligatorio se MBAM Salva i dati dell'unità rimovibili nel server di ripristino di chiave di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a8805-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a8805-130">Unità fissa</span><span class="sxs-lookup"><span data-stu-id="a8805-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-131">Controllare l'uso di BitLocker su unità fisse</span><span class="sxs-lookup"><span data-stu-id="a8805-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a8805-132">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="a8805-132">Enabled.</span></span> <span data-ttu-id="a8805-133">Obbligatorio se MBAM Salva i dati di unità fissati nel server di ripristino della chiave di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a8805-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="a8805-134">Impostare <strong> scegliere il modo in cui le unità protette da BitLocker possono essere recuperate </strong> e <strong> consentire l'agente di recupero dati </strong> .</span><span class="sxs-lookup"><span data-stu-id="a8805-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="a8805-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8805-135">Related topics</span></span>


[<span data-ttu-id="a8805-136">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a8805-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)









