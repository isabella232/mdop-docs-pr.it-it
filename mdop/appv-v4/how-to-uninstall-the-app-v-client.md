---
title: Come disinstallare il client App-V
description: Come disinstallare il client App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816525"
---
# <span data-ttu-id="b1d32-103">Come disinstallare il client App-V</span><span class="sxs-lookup"><span data-stu-id="b1d32-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="b1d32-104">Usare la procedura seguente per disinstallare il client di virtualizzazione dell'applicazione dal computer.</span><span class="sxs-lookup"><span data-stu-id="b1d32-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="b1d32-105">Per disinstallare il client Desktop Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b1d32-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="b1d32-106">Nel pannello di controllo fare doppio clic su **installazione** applicazioni o in Windows Vista, **programmi e funzionalità**e quindi fare doppio clic su **client desktop Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="b1d32-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="b1d32-107">Nella finestra di dialogo visualizzata fare clic su **Sì** per continuare con il processo di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="b1d32-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="b1d32-108">**Importante**  Il processo di disinstallazione non può essere annullato o interrotto.</span><span class="sxs-lookup"><span data-stu-id="b1d32-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="b1d32-109">Quando viene visualizzato un messaggio che indica che l'applicazione vassoio di Microsoft Application Virtualization Client deve essere chiusa prima di continuare a essere visualizzata, fare clic con il pulsante destro del mouse sull'icona dell'App-V nell'area di notifica e scegliere **Exit** per chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1d32-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="b1d32-110">Quindi fare clic su **Riprova** per continuare con il processo di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="b1d32-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="b1d32-111">**Importante**  Potrebbe essere visualizzato un messaggio che indica che sono in uso una o più applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="b1d32-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="b1d32-112">Chiudere tutte le applicazioni aperte e salvare i dati prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="b1d32-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="b1d32-113">Quindi fare clic su **OK** per continuare con il processo di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="b1d32-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="b1d32-114">Una barra di stato indica il tempo rimanente.</span><span class="sxs-lookup"><span data-stu-id="b1d32-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="b1d32-115">Al termine di questo passaggio, è necessario riavviare il computer in modo che tutti i driver associati possano essere fermati per completare il processo di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="b1d32-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="b1d32-116">**Nota**  Le chiavi del registro di sistema seguenti restano al termine del processo di disinstallazione:</span><span class="sxs-lookup"><span data-stu-id="b1d32-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="b1d32-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="b1d32-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="b1d32-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="b1d32-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="b1d32-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "client" = DWORD: 00000000</span><span class="sxs-lookup"><span data-stu-id="b1d32-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="b1d32-120">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span><span class="sxs-lookup"><span data-stu-id="b1d32-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="b1d32-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1d32-121">Related topics</span></span>


[<span data-ttu-id="b1d32-122">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="b1d32-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="b1d32-123">Come installare manualmente Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="b1d32-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="b1d32-124">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="b1d32-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





