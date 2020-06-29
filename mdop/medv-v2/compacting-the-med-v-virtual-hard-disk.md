---
title: Compattazione del disco rigido virtuale MED-V
description: Compattazione del disco rigido virtuale MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823276"
---
# <span data-ttu-id="93928-103">Compattazione del disco rigido virtuale MED-V</span><span class="sxs-lookup"><span data-stu-id="93928-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="93928-104">Anche se è facoltativo, puoi compattare il disco rigido virtuale (VHD) per recuperare spazio su disco vuoto e ridurre le dimensioni del VHD prima di configurare l'immagine di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="93928-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="93928-105">**Importante**  Prima di procedere, creare una copia di backup dell'immagine di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93928-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="93928-106">Preparazione del disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="93928-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="93928-107">Aprire l'immagine di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93928-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="93928-108">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**, Windows **Virtual PC**e quindi fare doppio clic sull'immagine di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93928-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="93928-109">Cancellare la cache DLL.</span><span class="sxs-lookup"><span data-stu-id="93928-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="93928-110">Al prompt dei comandi nella macchina virtuale digitare **sfc/cachesize = 1**.</span><span class="sxs-lookup"><span data-stu-id="93928-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="93928-111">Riavviare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="93928-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="93928-112">Al prompt dei comandi nella macchina virtuale digitare **sfc/purgecache**.</span><span class="sxs-lookup"><span data-stu-id="93928-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="93928-113">Eliminare i file non necessari, ad esempio i programmi di disinstallazione, i file temporanei, i file di log, i file di pagina, le cartelle condivise e così via.</span><span class="sxs-lookup"><span data-stu-id="93928-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="93928-114">Disattivare Ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="93928-114">Turn off System Restore.</span></span> <span data-ttu-id="93928-115">È anche possibile specificare questo passaggio nel file Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="93928-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="93928-116">Nel **Pannello di controllo**fare doppio clic su **sistema**e quindi selezionare la scheda **Ripristino configurazione di sistema** .</span><span class="sxs-lookup"><span data-stu-id="93928-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="93928-117">Selezionare **Disattiva Ripristino configurazione di sistema**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="93928-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="93928-118">Impostare le dimensioni massime del log eventi e cancellare tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="93928-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="93928-119">Aprire il Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="93928-119">Open the event viewer.</span></span>

        <span data-ttu-id="93928-120">Fare clic sul pulsante **Start**, scegliere **Pannello di controllo**, fare doppio clic su **strumenti di amministrazione**e quindi fare doppio clic su **Visualizzatore eventi**.</span><span class="sxs-lookup"><span data-stu-id="93928-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="93928-121">Fare clic con il pulsante destro del mouse su **applicazione**e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="93928-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="93928-122">Nell'area **dimensioni log** impostare la **dimensione massima del log** su 512KB e quindi selezionare **Sovrascrivi eventi in base alle esigenze**.</span><span class="sxs-lookup"><span data-stu-id="93928-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="93928-123">Fare clic su **Cancella log**.</span><span class="sxs-lookup"><span data-stu-id="93928-123">Click **Clear Log**.</span></span> <span data-ttu-id="93928-124">Nella finestra di dialogo **Visualizzatore eventi** che viene visualizzata fare clic su **No**.</span><span class="sxs-lookup"><span data-stu-id="93928-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="93928-125">Nella finestra **Proprietà** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="93928-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="93928-126">Ripetere i passaggi da a a e per i registri di **sicurezza** e di **sistema** .</span><span class="sxs-lookup"><span data-stu-id="93928-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="93928-127">Eseguire lo strumento di pulizia disco.</span><span class="sxs-lookup"><span data-stu-id="93928-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="93928-128">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Accessori**, **strumenti di sistema**e quindi fare clic su **pulizia disco**.</span><span class="sxs-lookup"><span data-stu-id="93928-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="93928-129">Configurare il file di pagina in base alle esigenze per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="93928-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="93928-130">Nel **Pannello di controllo**fare doppio clic su **sistema**e quindi selezionare la scheda **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="93928-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="93928-131">Nell'area **prestazioni** fare clic su **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="93928-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="93928-132">Nell'area **memoria virtuale** fare clic su **Cambia**.</span><span class="sxs-lookup"><span data-stu-id="93928-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="93928-133">Configurare le impostazioni del file di pagina.</span><span class="sxs-lookup"><span data-stu-id="93928-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="93928-134">Arrestare l'immagine di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93928-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="93928-135">Deframmentazione e pre-compattazione del disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="93928-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="93928-136">Nel **Pannello di controllo** nel computer host che sta usando Windows 7 fare clic **su strumenti di amministrazione**, fare doppio clic su **Gestione computer**e quindi su **Gestione disco**.</span><span class="sxs-lookup"><span data-stu-id="93928-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="93928-137">Usando la console Gestione disco, allegare (montare) il disco rigido virtuale e quindi deframmentare il disco.</span><span class="sxs-lookup"><span data-stu-id="93928-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="93928-138">Usando uno strumento di estrazione ISO, Estrai il precompact. ISO nella cartella componenti virtuali di PC\\Integration Files\\Windows cartella.</span><span class="sxs-lookup"><span data-stu-id="93928-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="93928-139">Usare il programma precompact.exe per comprimere il disco rigido virtuale di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93928-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="93928-140">Se si usa la console Gestione disco, scollegare il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="93928-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="93928-141">Compattazione del disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="93928-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="93928-142">Aprire Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="93928-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="93928-143">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**e quindi fare clic su **Virtual PC Windows**.</span><span class="sxs-lookup"><span data-stu-id="93928-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="93928-144">Fare clic con il pulsante destro del mouse sull'immagine di Windows XP e scegliere **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="93928-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="93928-145">Fare clic su **disco rigido** per quello corrispondente all'immagine di Windows XP e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="93928-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="93928-146">Fare clic su **disco rigido virtuale compatto**.</span><span class="sxs-lookup"><span data-stu-id="93928-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="93928-147">Fare clic su **compatta** e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="93928-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="93928-148">Creare una copia di backup del disco rigido virtuale compattato.</span><span class="sxs-lookup"><span data-stu-id="93928-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="93928-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93928-149">Related topics</span></span>


[<span data-ttu-id="93928-150">Configurazione di un'immagine di Windows Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="93928-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="93928-151">Documentazione tecnica su MED-V</span><span class="sxs-lookup"><span data-stu-id="93928-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





