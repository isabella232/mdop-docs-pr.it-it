---
title: Elenco esclusioni dell'applicazione Windows Virtual PC
description: Elenco esclusioni dell'applicazione Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823695"
---
# <span data-ttu-id="e68f4-103">Elenco esclusioni dell'applicazione Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e68f4-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="e68f4-104">In alcuni casi potrebbe non essere necessario che le applicazioni installate nell'area di lavoro MED-V vengano pubblicate nel menu **Start** del computer host.</span><span class="sxs-lookup"><span data-stu-id="e68f4-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="e68f4-105">È possibile annullare la pubblicazione di queste applicazioni seguendo le istruzioni [su come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="e68f4-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="e68f4-106">Tuttavia, se il programma viene aggiornato automaticamente, potrebbe anche essere ripubblicato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e68f4-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="e68f4-107">In questo modo è necessario annullare la pubblicazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e68f4-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="e68f4-108">Windows Virtual PC include una caratteristica nota come "elenco di esclusione" che consente di specificare alcune applicazioni installate che non si desidera pubblicare nel menu **Start** dell'host.</span><span class="sxs-lookup"><span data-stu-id="e68f4-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="e68f4-109">L'"elenco esclusioni" si trova nel registro di sistema guest nella chiave HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList ed elenca le applicazioni non pubblicate nel menu **Start** dell'host.</span><span class="sxs-lookup"><span data-stu-id="e68f4-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="e68f4-110">Si può pensare all'"elenco Escludi", come se si depubblicano definitivamente le applicazioni specificate, perché gli aggiornamenti automatici delle applicazioni elencate non possono essere ripubblicati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e68f4-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="e68f4-111">Gestione delle applicazioni tramite l'elenco Escludi in Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e68f4-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="e68f4-112">Aprire l'area di lavoro MED-V a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="e68f4-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="e68f4-113">Per informazioni sull'apertura dell'area di lavoro MED-V in modalità schermo intero tramite il Toolkit di amministrazione MED-V, vedere [visualizzazione delle configurazioni dell'area di lavoro MED-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span><span class="sxs-lookup"><span data-stu-id="e68f4-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="e68f4-114">In alternativa, è possibile aprirlo manualmente a schermo intero facendo clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**, **Windows Virtual PC**e quindi fare doppio clic sull'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="e68f4-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="e68f4-115">Nell'area di lavoro MED-V Windows Virtual PC aprire l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e68f4-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="e68f4-116">Fare clic sul pulsante **Start**, scegliere **Esegui**e quindi digitare regedit.</span><span class="sxs-lookup"><span data-stu-id="e68f4-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="e68f4-117">Quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e68f4-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="e68f4-118">Nell'editor del registro di sistema individuare la chiave del registro di sistema HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="e68f4-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="e68f4-119">Creare un nuovo valore del registro di sistema per l'applicazione installata che non si vuole pubblicare nel menu **Start** del computer host.</span><span class="sxs-lookup"><span data-stu-id="e68f4-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="e68f4-120">Se ad esempio si vuole annullare la pubblicazione del programma pubblicato automaticamente in Microsoft Silverlight, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e68f4-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="e68f4-121">Con la chiave del registro di sistema VPCVAppExcludeList evidenziata, fare clic su **modifica**, su **nuovo**e quindi su **valore stringa**.</span><span class="sxs-lookup"><span data-stu-id="e68f4-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="e68f4-122">Immettere il nome del nuovo valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e68f4-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="e68f4-123">Ad esempio, per Microsoft Silverlight, è possibile immettere sllauncher.exe.</span><span class="sxs-lookup"><span data-stu-id="e68f4-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="e68f4-124">Fare doppio clic sul nuovo valore del registro di sistema e immettere i dati del valore.</span><span class="sxs-lookup"><span data-stu-id="e68f4-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="e68f4-125">I dati del valore sono il percorso completo del comando che si vuole annullare la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e68f4-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="e68f4-126">Per trovare il percorso completo, fare clic con il pulsante destro del mouse sul collegamento nel menu **Start** per l'applicazione che non si vuole pubblicare e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e68f4-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="e68f4-127">Il percorso completo è elencato nella scheda **collegamento** in **destinazione**.</span><span class="sxs-lookup"><span data-stu-id="e68f4-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="e68f4-128">Ad esempio, per il programma Microsoft Silverlight, il percorso completo potrebbe essere "C:\\Programmi \\Programmi\\microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span><span class="sxs-lookup"><span data-stu-id="e68f4-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="e68f4-129">**Importante**  Se applicabile, rimuovere le virgolette dal percorso completo quando viene immesso nel campo dati valore.</span><span class="sxs-lookup"><span data-stu-id="e68f4-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="e68f4-130">Chiudere l'editor del registro di sistema e riavviare la macchina virtuale dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="e68f4-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="e68f4-131">L'applicazione è ancora installata nell'area di lavoro MED-V, ma ora è stata rimossa dal menu **Start** del computer host.</span><span class="sxs-lookup"><span data-stu-id="e68f4-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="e68f4-132">È anche possibile ripubblicare un'applicazione esclusa nel menu **Start** dell'host eliminando il valore corrispondente dalla chiave VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="e68f4-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="e68f4-133">Ad esempio, per ripubblicare Microsoft Silverlight, fare clic con il pulsante destro del mouse sul valore del registro di sistema sllauncher.exe e scegliere **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="e68f4-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="e68f4-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e68f4-134">Related topics</span></span>


[<span data-ttu-id="e68f4-135">Documentazione tecnica su MED-V</span><span class="sxs-lookup"><span data-stu-id="e68f4-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="e68f4-136">Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="e68f4-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





