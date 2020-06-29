---
title: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
description: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825106"
---
# <span data-ttu-id="e34af-103">Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="e34af-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="e34af-104">Un'applicazione per il pannello di controllo di amministrazione e monitoraggio di Microsoft BitLocker (MBAM), denominata opzioni di crittografia BitLocker, sarà disponibile in **sistema e sicurezza** quando viene installato il client di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e34af-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the Microsoft BitLocker Administration and Monitoring Client is installed.</span></span> <span data-ttu-id="e34af-105">Questo pannello di controllo di MBAM personalizzato è un pannello di controllo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="e34af-105">This custom MBAM control panel is an additional control panel.</span></span> <span data-ttu-id="e34af-106">Non sostituisce il pannello di controllo BitLocker predefinito di Windows.</span><span class="sxs-lookup"><span data-stu-id="e34af-106">It does not replace the default Windows BitLocker control panel.</span></span> <span data-ttu-id="e34af-107">Il pannello di controllo di MBAM può essere usato per sbloccare le unità fisse e rimovibili crittografate e gestire anche il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="e34af-107">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span> <span data-ttu-id="e34af-108">Per altre informazioni su come abilitare il pannello di controllo di MBAM, vedere [come nascondere la crittografia BitLocker predefinita nel pannello di controllo di Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="e34af-108">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in the Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span></span>

**<span data-ttu-id="e34af-109">Per usare il pannello di controllo del client MBAM</span><span class="sxs-lookup"><span data-stu-id="e34af-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="e34af-110">Per aprire le opzioni di crittografia BitLocker, fare clic sul pulsante **Start** e quindi selezionare **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="e34af-110">To open BitLocker Encryption Options, click **Start** and then select **Control Panel**.</span></span> <span data-ttu-id="e34af-111">Quando si apre il **Pannello di controllo** , selezionare **sistema e sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="e34af-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="e34af-112">Fare doppio clic sulle **Opzioni di crittografia BitLocker** per aprire il pannello di controllo di mbam personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e34af-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="e34af-113">Verrà visualizzato un elenco di tutte le unità disco rigido del computer e il relativo stato di crittografia, oltre a un'opzione per gestire il PIN o le password.</span><span class="sxs-lookup"><span data-stu-id="e34af-113">You will see a list of all the hard disk drives on the computer and their encryption status, in addition to an option to manage your PIN or passwords.</span></span>

    <span data-ttu-id="e34af-114">L'elenco delle unità disco rigido nel computer può essere usato per verificare lo stato di crittografia, sbloccare un'unità o richiedere un'esenzione per la protezione da BitLocker se sono stati distribuiti i criteri di esenzione per l'utente e il computer.</span><span class="sxs-lookup"><span data-stu-id="e34af-114">The list of hard disk drives on the computer can be used to verify encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

    <span data-ttu-id="e34af-115">Il pannello di controllo opzioni di crittografia BitLocker consente inoltre agli utenti non amministratori di gestire il PIN o le password.</span><span class="sxs-lookup"><span data-stu-id="e34af-115">The BitLocker Encryption Options control panel also allows for non-administrator users to manage their PIN or passwords.</span></span> <span data-ttu-id="e34af-116">Selezionando **Gestisci pin**, viene chiesto agli utenti di immettere sia un PIN corrente che un nuovo PIN, oltre a confermare il nuovo PIN.</span><span class="sxs-lookup"><span data-stu-id="e34af-116">By selecting **Manage PIN**, users are prompted to enter both a current PIN and a new PIN (in addition to confirming the new PIN).</span></span> <span data-ttu-id="e34af-117">Selezionando **Aggiorna pin** verrà reimpostato il pin su quello nuovo selezionato dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="e34af-117">Selecting **Update PIN** will reset the PIN to the new one that the users selected.</span></span>

    <span data-ttu-id="e34af-118">Per gestire la password, selezionare **Sblocca unità** e immettere la password corrente.</span><span class="sxs-lookup"><span data-stu-id="e34af-118">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="e34af-119">Non appena l'unità è sbloccata, selezionare **Reimposta password** per cambiare la password corrente.</span><span class="sxs-lookup"><span data-stu-id="e34af-119">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="e34af-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e34af-120">Related topics</span></span>


[<span data-ttu-id="e34af-121">Amministrazione delle funzionalità di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="e34af-121">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





