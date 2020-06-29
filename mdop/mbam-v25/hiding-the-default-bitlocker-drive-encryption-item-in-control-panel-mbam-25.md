---
title: Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo
description: Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823096"
---
# <span data-ttu-id="50685-103">Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="50685-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="50685-104">Questo argomento descrive come nascondere la voce del pannello di controllo **crittografia unità BitLocker** , che viene visualizzata per impostazione predefinita nel pannello di controllo come parte del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="50685-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="50685-105">**Nota**  Microsoft BitLocker Administration and Monitoring (MBAM) crea un'altra voce del pannello di controllo personalizzata, denominata **Opzioni di crittografia BitLocker**, che consente agli utenti finali di gestire il PIN e la password, attivare BitLocker per un'unità e verificare la crittografia.</span><span class="sxs-lookup"><span data-stu-id="50685-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="50685-106">Vedere informazioni sulle [Opzioni di crittografia BitLocker e sugli elementi di crittografia unità BitLocker nel pannello di controllo per la](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) lettura:</span><span class="sxs-lookup"><span data-stu-id="50685-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="50685-107">Differenze tra MBAM e gli elementi del pannello di controllo predefiniti</span><span class="sxs-lookup"><span data-stu-id="50685-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="50685-108">**Gestire** il menu di scelta rapida BitLocker visualizzato quando si fa clic con il pulsante destro del mouse su un'unità in Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="50685-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="50685-109">**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="50685-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="50685-110">In caso contrario, MBAM non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="50685-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="50685-111">Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="50685-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="50685-112">Per nascondere l'elemento di crittografia unità BitLocker predefinito nel pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="50685-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="50685-113">Nella console di gestione di criteri di gruppo o in Gestione criteri di gruppo avanzati individuare il pannello **User configuration** di controllo dei &gt; **Policies** &gt; **modelli amministrativi** &gt; **Control Panel**di criteri di configurazione utente.</span><span class="sxs-lookup"><span data-stu-id="50685-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="50685-114">Nel riquadro dei **Dettagli** fare doppio clic su **Nascondi elementi del pannello di controllo specificati**e quindi fare clic su **abilitato**.</span><span class="sxs-lookup"><span data-stu-id="50685-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="50685-115">Fare clic su **Mostra**, su **Aggiungi**e quindi digitare **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="50685-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="50685-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50685-116">Related topics</span></span>


[<span data-ttu-id="50685-117">Comprendere le opzioni di crittografia BitLocker e gli elementi di Crittografia unità BitLocker nel Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="50685-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="50685-118">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="50685-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="50685-119">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="50685-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="50685-120">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="50685-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="50685-121">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="50685-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





