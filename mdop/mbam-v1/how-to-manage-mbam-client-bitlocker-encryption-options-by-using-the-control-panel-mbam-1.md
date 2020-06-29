---
title: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
description: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804617"
---
# <span data-ttu-id="4f985-103">Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="4f985-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="4f985-104">Un'applicazione per il pannello di controllo di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, denominata opzioni di crittografia BitLocker, sarà disponibile in **sistema e sicurezza** quando il client mbam è installato.</span><span class="sxs-lookup"><span data-stu-id="4f985-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the MBAM Client is installed.</span></span> <span data-ttu-id="4f985-105">Questo pannello di controllo di MBAM personalizzato sostituisce il pannello di controllo predefinito di Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4f985-105">This customized MBAM control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="4f985-106">Il pannello di controllo di MBAM consente di sbloccare le unità crittografate (fisse e rimovibili) e consente anche di gestire il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="4f985-106">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span> <span data-ttu-id="4f985-107">Per altre informazioni su come abilitare il pannello di controllo di MBAM, vedere [come nascondere la crittografia BitLocker predefinita nel pannello di controllo di Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="4f985-107">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in The Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span></span>

<span data-ttu-id="4f985-108">**Nota**  Per il client BitLocker, i file di registro dell'amministratore e dell'operativo si trovano nel Visualizzatore eventi, in **applicazione e servizi vengono registrati**  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="4f985-108">**Note** For the BitLocker client, the Admin and Operational log files are located in Event Viewer, under **Application and Services Logs** / **Microsoft** / **Windows** / **BitLockerManagement**.</span></span>

 

**<span data-ttu-id="4f985-109">Per usare il pannello di controllo del client MBAM</span><span class="sxs-lookup"><span data-stu-id="4f985-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="4f985-110">Per aprire le opzioni di crittografia BitLocker, fare clic sul pulsante **Start**e quindi selezionare **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="4f985-110">To open BitLocker Encryption Options, click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="4f985-111">Quando si apre il **Pannello di controllo** , selezionare **sistema e sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="4f985-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="4f985-112">Fare doppio clic sulle **Opzioni di crittografia BitLocker** per aprire il pannello di controllo di mbam personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4f985-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="4f985-113">Verrà visualizzato un elenco di tutte le unità disco rigido nel computer e il relativo stato di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4f985-113">You will see a list of all the hard disk drives on the computer and their encryption status.</span></span> <span data-ttu-id="4f985-114">Verrà visualizzata anche un'opzione per gestire il PIN o le password.</span><span class="sxs-lookup"><span data-stu-id="4f985-114">You will also see an option to manage your PIN or passwords.</span></span>

3.  <span data-ttu-id="4f985-115">Usare l'elenco di unità disco rigido nel computer per verificare lo stato di crittografia, sbloccare un'unità o richiedere un'esenzione per la protezione da BitLocker se sono stati distribuiti i criteri di esenzione dall'utente e dal computer.</span><span class="sxs-lookup"><span data-stu-id="4f985-115">Use the list of hard disk drives on the computer to verify the encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

4.  <span data-ttu-id="4f985-116">Gli utenti non amministratori possono usare il pannello di controllo opzioni di crittografia BitLocker per gestire i pin o le password.</span><span class="sxs-lookup"><span data-stu-id="4f985-116">Non-administrators can use the BitLocker Encryption Options control panel to manage PINs or passwords.</span></span> <span data-ttu-id="4f985-117">Un utente può selezionare **Gestisci pin** e quindi immettere sia un PIN corrente che un nuovo PIN.</span><span class="sxs-lookup"><span data-stu-id="4f985-117">A user can select **Manage PIN,** and then enter both a current PIN and a new PIN.</span></span> <span data-ttu-id="4f985-118">Gli utenti possono anche confermare il nuovo PIN.</span><span class="sxs-lookup"><span data-stu-id="4f985-118">Users can also confirm their new PIN.</span></span> <span data-ttu-id="4f985-119">La funzione **Aggiorna pin** Reimposta il pin su quello nuovo selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4f985-119">The **Update PIN** function will reset the PIN to the new one that the user selects.</span></span>

5.  <span data-ttu-id="4f985-120">Per gestire la password, selezionare **Sblocca unità** e immettere la password corrente.</span><span class="sxs-lookup"><span data-stu-id="4f985-120">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="4f985-121">Non appena l'unità è sbloccata, selezionare **Reimposta password** per cambiare la password corrente.</span><span class="sxs-lookup"><span data-stu-id="4f985-121">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="4f985-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f985-122">Related topics</span></span>


[<span data-ttu-id="4f985-123">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4f985-123">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





