---
title: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
description: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824506"
---
# <span data-ttu-id="1abf5-103">Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="1abf5-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="1abf5-104">Microsoft BitLocker Administration and Monitoring (MBAM) offre un pannello di controllo personalizzato per i computer client di MBAM denominato opzioni di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1abf5-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="1abf5-105">Questo pannello di controllo personalizzato può sostituire il pannello di controllo BitLocker predefinito di Windows denominato crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1abf5-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="1abf5-106">Il pannello di controllo opzioni di crittografia BitLocker, che si trova in sistema e sicurezza nel pannello di controllo di Windows, consente agli utenti di gestire il PIN e le password, sbloccare le unità e nascondere l'interfaccia che consente agli amministratori di decrittografare un'unità o di sospendere o riprendere la crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1abf5-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="1abf5-107">Per nascondere la crittografia BitLocker predefinita nel pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="1abf5-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="1abf5-108">Passare alla **Configurazione utente** usando la console Gestione criteri di gruppo, la gestione avanzata Criteri di gruppo o l'Editor criteri di gruppo locali nel computer criteri di gruppo di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1abf5-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="1abf5-109">Fare clic su **criteri**, selezionare **modelli amministrativi**e quindi fare clic su **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="1abf5-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="1abf5-110">Nel riquadro dei **Dettagli** fare doppio clic su **Nascondi elementi del pannello di controllo specificati**e quindi selezionare **abilitato**.</span><span class="sxs-lookup"><span data-stu-id="1abf5-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="1abf5-111">Fare clic su **Mostra**, **su Aggiungi...** e quindi digitare Microsoft. BitLockerDriveEncryption.</span><span class="sxs-lookup"><span data-stu-id="1abf5-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="1abf5-112">Questo criterio nasconde lo strumento di Gestione BitLocker predefinito di Windows dal pannello di controllo di Windows e consente all'utente di aprire lo strumento per la crittografia di BitLocker aggiornato MBAM dal pannello di controllo di Windows.</span><span class="sxs-lookup"><span data-stu-id="1abf5-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="1abf5-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1abf5-113">Related topics</span></span>


[<span data-ttu-id="1abf5-114">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1abf5-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





