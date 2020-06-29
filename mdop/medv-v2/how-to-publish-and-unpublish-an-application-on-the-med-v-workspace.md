---
title: Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V
description: Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826925"
---
# <span data-ttu-id="5674d-103">Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="5674d-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="5674d-104">Anche se un'applicazione viene installata in un'area di lavoro MED-V, potrebbe essere necessario pubblicare l'applicazione anche prima che diventi disponibile per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="5674d-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="5674d-105">Per impostazione predefinita, la maggior parte delle applicazioni viene pubblicata nel momento in cui sono installate e i tasti di scelta rapida vengono creati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="5674d-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="5674d-106">In alcuni casi, è possibile installare le applicazioni nell'area di lavoro MED-V senza renderle disponibili per l'utente finale, ad esempio software per la ricerca di virus.</span><span class="sxs-lookup"><span data-stu-id="5674d-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="5674d-107">Allo stesso modo, ci sono occasioni in cui vuoi pubblicare un'applicazione installata nell'area di lavoro MED-V che in precedenza non era disponibile per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="5674d-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="5674d-108">Ad esempio, potrebbe essere necessario pubblicare un'applicazione installata se l'installazione non crea automaticamente un collegamento nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="5674d-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="5674d-109">**Importante**  Se pubblichi un'applicazione che non supporta percorsi UNC, ti consigliamo di eseguire il mapping dell'applicazione a un'unità.</span><span class="sxs-lookup"><span data-stu-id="5674d-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="5674d-110">È possibile pubblicare o annullare la pubblicazione di applicazioni in un'area di lavoro MED-V distribuita eseguendo una delle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="5674d-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="5674d-111">Per pubblicare o annullare la pubblicazione di un'applicazione installata</span><span class="sxs-lookup"><span data-stu-id="5674d-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="5674d-112">Per pubblicare un'applicazione in un'area di lavoro MED-V distribuita, copiare un collegamento per l'applicazione nella cartella seguente della macchina virtuale:</span><span class="sxs-lookup"><span data-stu-id="5674d-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="5674d-113">Menu di C:\\Documents and e Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="5674d-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="5674d-114">Se necessario, usare criteri di gruppo o un sistema ESD per distribuire uno script che copia il collegamento per l'applicazione nella cartella tutti i menu di Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="5674d-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="5674d-115">Per annullare la pubblicazione di un'applicazione in un'area di lavoro MED-V distribuita, eliminare il collegamento per l'applicazione dalla cartella seguente nella macchina virtuale:</span><span class="sxs-lookup"><span data-stu-id="5674d-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="5674d-116">Menu di C:\\Documents and e Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="5674d-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="5674d-117">Se necessario, usare criteri di gruppo o un sistema ESD per distribuire uno script che elimina il collegamento per tale applicazione dalla cartella tutti i menu di Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="5674d-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="5674d-118">**Nota**  Spesso, quando si disinstalla l'applicazione, il collegamento viene eliminato automaticamente dal menu **Start** del computer host.</span><span class="sxs-lookup"><span data-stu-id="5674d-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="5674d-119">Tuttavia, in alcuni casi, ad esempio per un'area di lavoro MED-V configurata per tutti gli utenti di un computer condiviso, potrebbe essere necessario eliminare manualmente il collegamento nel menu **Start** dopo la disinstallazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5674d-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="5674d-120">L'utente finale può eseguire questa operazione facendo clic con il pulsante destro del mouse sul collegamento e scegliendo **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="5674d-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="5674d-121">Per verificare che l'applicazione sia stata pubblicata o non pubblicata, verifica nell'area di lavoro MED-V se il collegamento corrispondente è disponibile o meno.</span><span class="sxs-lookup"><span data-stu-id="5674d-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="5674d-122">**Nota**  Le applicazioni incluse in Windows XP SP3 e si trovano nella cartella del menu Start della macchina virtuale non vengono pubblicate automaticamente nell'host.</span><span class="sxs-lookup"><span data-stu-id="5674d-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="5674d-123">Sono controllate dalle impostazioni del registro di sistema che bloccano la pubblicazione automatica.</span><span class="sxs-lookup"><span data-stu-id="5674d-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="5674d-124">Per altre informazioni, Vedi [elenco esclusioni applicazioni di Windows Virtual PC](windows-virtual-pc-application-exclude-list.md).</span><span class="sxs-lookup"><span data-stu-id="5674d-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="5674d-125">Per pubblicare gli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5674d-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="5674d-126">Creare un collegamento nella macchina virtuale in cui la destinazione è il nome dell'elemento, ad esempio C:\\WINDOWS\\system32\\appwiz.cpl.</span><span class="sxs-lookup"><span data-stu-id="5674d-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="5674d-127">Il collegamento deve essere creato in o spostato nella cartella "%ALLUSERSPROFILE%\\Start Menu\\" o in una delle relative sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="5674d-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="5674d-128">L'elemento verrà pubblicato nel computer host nella posizione corrispondente nella cartella del menu di avvio dell'host.</span><span class="sxs-lookup"><span data-stu-id="5674d-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="5674d-129">Avviare il collegamento per l'elemento nell'host.</span><span class="sxs-lookup"><span data-stu-id="5674d-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="5674d-130">**Attenzione**  Quando si crea il collegamento, non specificare% SystemRoot% \\control.exe.</span><span class="sxs-lookup"><span data-stu-id="5674d-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="5674d-131">Questa applicazione non verrà pubblicata perché è contenuta nelle impostazioni del registro di sistema che bloccano la pubblicazione automatica.</span><span class="sxs-lookup"><span data-stu-id="5674d-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="5674d-132">Come MED-V gestisce la pubblicazione automatica delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="5674d-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="5674d-133">Durante la pubblicazione dell'applicazione, MED-V copia i tasti di scelta rapida dalla macchina virtuale Guest al computer host provando a corrispondere alla gerarchia delle cartelle esistente nel guest.</span><span class="sxs-lookup"><span data-stu-id="5674d-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="5674d-134">In questo modo, MED-V copia i tasti di scelta rapida dal Guest all'host eseguendo la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="5674d-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="5674d-135">MED-V cerca di individuare una cartella in Start Menu\\Programs nel computer host denominata uguale alla cartella nel guest in cui si trova il collegamento.</span><span class="sxs-lookup"><span data-stu-id="5674d-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="5674d-136">Se non è presente alcuna cartella corrispondente, MED-V cerca quindi di individuare una cartella nella cartella del menu Start dell'host denominata uguale alla cartella dell'ospite in cui si trova il collegamento.</span><span class="sxs-lookup"><span data-stu-id="5674d-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="5674d-137">Se non è presente alcuna cartella corrispondente, MED-V copia il collegamento alla cartella predefinita dell'host, la cartella Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="5674d-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="5674d-138">Esempio di processo di pubblicazione delle applicazioni:</span><span class="sxs-lookup"><span data-stu-id="5674d-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="5674d-139">Se un collegamento a un'applicazione viene pubblicato nella cartella Start Menu\\Programs\\AppShortcuts nel guest, MED-V Cerca nel computer host una cartella Start Menu\\Programs\\ AppShortcuts e, se trovata, copia il collegamento a tale cartella.</span><span class="sxs-lookup"><span data-stu-id="5674d-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="5674d-140">Se la cartella non viene trovata, MED-V Cerca nel computer host una cartella Start Menu\\AppShortcuts e, se trovata, copia il collegamento a tale cartella.</span><span class="sxs-lookup"><span data-stu-id="5674d-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="5674d-141">Se la cartella non viene trovata, MED-V copia il collegamento alla cartella Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="5674d-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="5674d-142">**Nota**  Una cartella deve esistere già nella cartella del menu Start del computer host per MED-V per copiare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="5674d-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="5674d-143">MED-V non crea la cartella se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="5674d-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="5674d-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5674d-144">Related topics</span></span>


[<span data-ttu-id="5674d-145">Installazione e rimozione di un'applicazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="5674d-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="5674d-146">Gestione degli aggiornamenti software per le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="5674d-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="5674d-147">Elenco esclusioni dell'applicazione Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5674d-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 





