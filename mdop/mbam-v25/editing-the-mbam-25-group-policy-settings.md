---
title: Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5
description: Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804347"
---
# <span data-ttu-id="3f5f6-103">Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3f5f6-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="3f5f6-104">Per distribuire correttamente Microsoft BitLocker Administration and Monitoring (MBAM), è necessario:</span><span class="sxs-lookup"><span data-stu-id="3f5f6-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f5f6-105">Attività</span><span class="sxs-lookup"><span data-stu-id="3f5f6-105">Task</span></span></th>
<th align="left"><span data-ttu-id="3f5f6-106">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="3f5f6-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f5f6-107">Copiare i modelli dei criteri di gruppo di MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="3f5f6-108">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3f5f6-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f5f6-109">Determinare gli oggetti Criteri di gruppo che si desidera utilizzare nell'implementazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="3f5f6-110">In base alle esigenze dell'organizzazione, potrebbe essere necessario configurare altre impostazioni di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="3f5f6-111">Pianificazione per i requisiti di criteri di gruppo di MBAM 2,5 </a> -contiene le descrizioni dei GPO</span><span class="sxs-lookup"><span data-stu-id="3f5f6-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f5f6-112">Impostare le impostazioni dei criteri di gruppo per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3f5f6-113">**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="3f5f6-114">Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="3f5f6-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="3f5f6-115">Per modificare le impostazioni dei criteri di gruppo di MBAM client</span><span class="sxs-lookup"><span data-stu-id="3f5f6-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="3f5f6-116">In un computer in cui sono installati i modelli di criteri di gruppo di MBAM verificare che i servizi MBAM siano abilitati.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="3f5f6-117">Usando la console Gestione criteri di gruppo (GPMC. msc) o il prodotto Microsoft Advanced Group Policy Management MDOP in un computer con i modelli di criteri di gruppo di mbam installati, selezionare criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (Gestione BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="3f5f6-118">Modificare le impostazioni dei criteri di gruppo necessarie per abilitare i servizi client di MBAM nei computer client.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="3f5f6-119">Per ogni criterio nella tabella seguente selezionare **gruppo criteri**, fare clic sul **criterio** desiderato e quindi configurare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="3f5f6-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="3f5f6-120">Gruppo criteri</span><span class="sxs-lookup"><span data-stu-id="3f5f6-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="3f5f6-121">Criterio</span><span class="sxs-lookup"><span data-stu-id="3f5f6-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3f5f6-122">Gestione dei client</span><span class="sxs-lookup"><span data-stu-id="3f5f6-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3f5f6-123">Configurare i servizi MBAM</span><span class="sxs-lookup"><span data-stu-id="3f5f6-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3f5f6-124">Unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3f5f6-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3f5f6-125">Impostazioni di crittografia unità del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3f5f6-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3f5f6-126">Unità rimovibile</span><span class="sxs-lookup"><span data-stu-id="3f5f6-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3f5f6-127">Controllare l'uso di BitLocker su unità rimovibili</span><span class="sxs-lookup"><span data-stu-id="3f5f6-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3f5f6-128">Unità fissa</span><span class="sxs-lookup"><span data-stu-id="3f5f6-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3f5f6-129">Controllare l'uso di BitLocker su unità fisse</span><span class="sxs-lookup"><span data-stu-id="3f5f6-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="3f5f6-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f5f6-130">Related topics</span></span>


[<span data-ttu-id="3f5f6-131">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3f5f6-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="3f5f6-132">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3f5f6-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="3f5f6-133">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="3f5f6-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3f5f6-134">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3f5f6-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3f5f6-135">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3f5f6-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





