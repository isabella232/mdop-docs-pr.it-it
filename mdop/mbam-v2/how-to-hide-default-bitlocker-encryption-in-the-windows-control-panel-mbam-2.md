---
title: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
description: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824085"
---
# <span data-ttu-id="4b9f0-103">Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="4b9f0-103">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>


<span data-ttu-id="4b9f0-104">Microsoft BitLocker Administration and Monitoring (MBAM) offre un pannello di controllo personalizzato per l'amministrazione di Microsoft BitLocker e il monitoraggio dei computer client, denominati opzioni di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for Microsoft BitLocker Administration and Monitoring client computers, called BitLocker Encryption Options.</span></span> <span data-ttu-id="4b9f0-105">Questo pannello di controllo personalizzato può sostituire il pannello di controllo BitLocker predefinito di Windows, denominato crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-105">This customized control panel can replace the default Windows BitLocker control panel, which is called BitLocker Drive Encryption.</span></span> <span data-ttu-id="4b9f0-106">Il pannello di controllo personalizzato, che si trova nel pannello di controllo in sistema e sicurezza, consente agli utenti di gestire il PIN e le password e di sbloccare le unità e nasconde l'interfaccia che consente agli amministratori di decrittografare un'unità o di sospendere o riprendere la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-106">The customized control panel, which is in Control Panel under System and Security, enables users to manage their PIN and passwords and to unlock drives, and hides the interface that enables administrators to decrypt a drive or to suspend or resume BitLocker drive encryption.</span></span>

**<span data-ttu-id="4b9f0-107">Per nascondere la crittografia predefinita unità BitLocker nel pannello di controllo di Windows</span><span class="sxs-lookup"><span data-stu-id="4b9f0-107">To hide default BitLocker drive encryption in Windows Control Panel</span></span>**

1.  <span data-ttu-id="4b9f0-108">Nella console Gestione criteri di gruppo (GPMC), in Advanced Group Policy Management o nell'Editor criteri di gruppo locali nel computer criteri di gruppo di BitLocker, passare alla **Configurazione utente**.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-108">In the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer, browse to **User configuration**.</span></span>

2.  <span data-ttu-id="4b9f0-109">Fare quindi clic su **criteri**, selezionare **modelli amministrativi**e quindi fare clic su **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-109">Next, click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="4b9f0-110">Fare doppio clic su **Nascondi elementi del pannello di controllo specificati** nel riquadro dei **Dettagli** e quindi selezionare **abilitato**.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-110">Double-click **Hide specified Control Panel items** in the **Details** pane, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="4b9f0-111">Fare clic su **Mostra**, su **Aggiungi**e quindi digitare **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-111">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span> <span data-ttu-id="4b9f0-112">Questo criterio nasconde lo strumento di Gestione BitLocker predefinito di Windows dal pannello di controllo di Windows e, nel pannello di controllo, consente all'utente di aprire lo strumento per le opzioni di crittografia di BitLocker aggiornato di MBAM in sistema e sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4b9f0-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and, in Control Panel, lets the user open the updated MBAM BitLocker Encryption Options tool under System and Security.</span></span>

## <span data-ttu-id="4b9f0-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b9f0-113">Related topics</span></span>


[<span data-ttu-id="4b9f0-114">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4b9f0-114">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





