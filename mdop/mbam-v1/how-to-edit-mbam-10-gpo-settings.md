---
title: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0
description: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824285"
---
# <span data-ttu-id="46025-103">Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="46025-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="46025-104">Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker, è prima di tutto necessario determinare i criteri di gruppo che verranno usati nell'implementazione dell'amministrazione e del monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="46025-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="46025-105">Per altre informazioni sui vari criteri disponibili, vedere [pianificazione per i requisiti dei criteri di gruppo di MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46025-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="46025-106">Dopo aver determinato i criteri che si intende usare, è necessario modificare uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="46025-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="46025-107">I passaggi seguenti descrivono come configurare le impostazioni di base degli oggetti Criteri di gruppo (GPO) consigliate per consentire a MBAM di gestire la crittografia BitLocker per i computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="46025-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="46025-108">Per modificare le impostazioni del GPO client MBAM</span><span class="sxs-lookup"><span data-stu-id="46025-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="46025-109">In un computer in cui è installato il modello di criteri di gruppo di MBAM verificare che i servizi MBAM siano abilitati.</span><span class="sxs-lookup"><span data-stu-id="46025-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="46025-110">Usare la console Gestione criteri di gruppo (GPMC. msc) o il prodotto MDOP Advanced Group Policy Management per queste azioni: selezionare **Configurazione computer**, scegliere **criteri**, **modelli amministrativi**, selezionare **componenti di Windows**e quindi fare clic su **MDOP mbam (Gestione BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="46025-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="46025-111">Modificare le impostazioni degli oggetti Criteri di gruppo necessarie per abilitare i servizi client di MBAM nei computer client.</span><span class="sxs-lookup"><span data-stu-id="46025-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="46025-112">Per ogni criterio nella tabella seguente selezionare **gruppo criteri**, fare clic sul **criterio**e quindi configurare l' **impostazione**.</span><span class="sxs-lookup"><span data-stu-id="46025-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="46025-113">Gruppo criteri</span><span class="sxs-lookup"><span data-stu-id="46025-113">Policy Group</span></span>

    <span data-ttu-id="46025-114">Criterio</span><span class="sxs-lookup"><span data-stu-id="46025-114">Policy</span></span>

    <span data-ttu-id="46025-115">Impostazione</span><span class="sxs-lookup"><span data-stu-id="46025-115">Setting</span></span>

    <span data-ttu-id="46025-116">Gestione dei client</span><span class="sxs-lookup"><span data-stu-id="46025-116">Client Management</span></span>

    <span data-ttu-id="46025-117">Configurare i servizi MBAM</span><span class="sxs-lookup"><span data-stu-id="46025-117">Configure MBAM Services</span></span>

    <span data-ttu-id="46025-118">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="46025-118">Enabled.</span></span> <span data-ttu-id="46025-119">Impostare l' **endpoint del servizio hardware e ripristino di mbam** e **selezionare informazioni di ripristino di BitLocker da archiviare**.</span><span class="sxs-lookup"><span data-stu-id="46025-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="46025-120">Impostare l' **endpoint del servizio di conformità mbam** e **immettere la frequenza del rapporto di stato in (minuti)**.</span><span class="sxs-lookup"><span data-stu-id="46025-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="46025-121">Consentire il controllo della compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="46025-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="46025-122">Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="46025-122">Disabled.</span></span> <span data-ttu-id="46025-123">Questo criterio è abilitato per impostazione predefinita, ma non è necessario per un'implementazione di MBAM di base.</span><span class="sxs-lookup"><span data-stu-id="46025-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="46025-124">Unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="46025-124">Operating System Drive</span></span>

    <span data-ttu-id="46025-125">Impostazioni di crittografia unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="46025-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="46025-126">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="46025-126">Enabled.</span></span> <span data-ttu-id="46025-127">Impostare **Seleziona protezione per l'unità del sistema operativo**.</span><span class="sxs-lookup"><span data-stu-id="46025-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="46025-128">Questo è necessario per salvare i dati dell'unità del sistema operativo nel server di ripristino di MBAM Key.</span><span class="sxs-lookup"><span data-stu-id="46025-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="46025-129">Unità rimovibile</span><span class="sxs-lookup"><span data-stu-id="46025-129">Removable Drive</span></span>

    <span data-ttu-id="46025-130">Controllare l'uso di BitLocker su unità rimovibili</span><span class="sxs-lookup"><span data-stu-id="46025-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="46025-131">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="46025-131">Enabled.</span></span> <span data-ttu-id="46025-132">Questo è necessario se MBAM Salva i dati di unità rimovibili nel server di ripristino di chiave di MBAM.</span><span class="sxs-lookup"><span data-stu-id="46025-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="46025-133">Unità fissa</span><span class="sxs-lookup"><span data-stu-id="46025-133">Fixed Drive</span></span>

    <span data-ttu-id="46025-134">Controllare l'uso di BitLocker su unità fisse</span><span class="sxs-lookup"><span data-stu-id="46025-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="46025-135">Abilitata.</span><span class="sxs-lookup"><span data-stu-id="46025-135">Enabled.</span></span> <span data-ttu-id="46025-136">Questo è necessario se MBAM salverà i dati fissi delle unità nel server di ripristino di chiave di MBAM.</span><span class="sxs-lookup"><span data-stu-id="46025-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="46025-137">Impostare **scegliere il modo in cui le unità protette da BitLocker possono essere recuperate** e **consentire l'agente di recupero dati**.</span><span class="sxs-lookup"><span data-stu-id="46025-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="46025-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46025-138">Related topics</span></span>


[<span data-ttu-id="46025-139">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="46025-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)









