---
title: Come gestire manualmente le applicazioni virtuali
description: Come gestire manualmente le applicazioni virtuali
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817115"
---
# <span data-ttu-id="cb48a-103">Come gestire manualmente le applicazioni virtuali</span><span class="sxs-lookup"><span data-stu-id="cb48a-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="cb48a-104">Puoi usare la console di gestione client Application Virtualization (App-V) per gestire le applicazioni virtuali nel client Desktop App-V o nel client App-V per Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="cb48a-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="cb48a-105">Gli amministratori di App-V possono usare eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb48a-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="cb48a-106">Come caricare o scaricare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="cb48a-107">Puoi usare le procedure seguenti per caricare o scaricare un'applicazione dalla cache, direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione dei client di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb48a-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="cb48a-108">Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cb48a-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="cb48a-109">**Nota**  Quando carichi o scarichi un pacchetto, tutte le applicazioni nel pacchetto vengono caricate o rimosse dalla cache.</span><span class="sxs-lookup"><span data-stu-id="cb48a-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="cb48a-110">Quando si carica un pacchetto, se non si dispone di spazio sufficiente nella cache per caricare le applicazioni, aumentare le dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="cb48a-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="cb48a-111">Per altre informazioni sulle dimensioni della cache, vedere [come modificare le dimensioni della cache e la denominazione della lettera dell'unità](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span><span class="sxs-lookup"><span data-stu-id="cb48a-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="cb48a-112">Per caricare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="cb48a-113">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **carica** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-114">L'applicazione viene caricata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cb48a-114">The application is automatically loaded.</span></span> <span data-ttu-id="cb48a-115">Lo stato di avanzamento viene registrato nella colonna contrassegnata come **stato del pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="cb48a-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="cb48a-116">È necessario aggiornare la visualizzazione per verificare che il caricamento sia completo o per visualizzare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="cb48a-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="cb48a-117">Per scaricare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="cb48a-118">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Scarica** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-119">L'applicazione viene scaricata automaticamente e la colonna **stato del pacchetto** viene aggiornata per riflettere la modifica.</span><span class="sxs-lookup"><span data-stu-id="cb48a-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="cb48a-120">Come cancellare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-120">How to clear an App-V application</span></span>


<span data-ttu-id="cb48a-121">È possibile cancellare un'applicazione dalla console direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="cb48a-122">Quando si deseleziona un'applicazione, il sistema rimuove le impostazioni, i tasti di scelta rapida e le associazioni di tipi di file che corrispondono all'applicazione e rimuove anche l'applicazione dall'elenco di applicazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cb48a-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="cb48a-123">**Nota**  Quando si deseleziona un'applicazione dalla console, non è più possibile usare tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb48a-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="cb48a-124">Tuttavia, l'applicazione rimane nella cache ed è ancora disponibile per altri utenti nello stesso sistema.</span><span class="sxs-lookup"><span data-stu-id="cb48a-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="cb48a-125">Dopo un aggiornamento della pubblicazione, le applicazioni deselezionate diventeranno di nuovo disponibili.</span><span class="sxs-lookup"><span data-stu-id="cb48a-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="cb48a-126">Se sono presenti più applicazioni in un pacchetto, le impostazioni dell'utente non vengono rimosse finché tutte le applicazioni non vengono cancellate.</span><span class="sxs-lookup"><span data-stu-id="cb48a-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="cb48a-127">Per cancellare un'applicazione dalla console</span><span class="sxs-lookup"><span data-stu-id="cb48a-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="cb48a-128">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Cancella** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-129">Alla richiesta di conferma fare clic su **Sì** per rimuovere l'applicazione o fare clic su **No** per annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb48a-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="cb48a-130">Come ripristinare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-130">How to Repair an App-V application</span></span>


<span data-ttu-id="cb48a-131">Per ripristinare un'applicazione selezionata, è possibile eseguire la procedura seguente direttamente dal riquadro dei **risultati** del nodo **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="cb48a-132">Quando si ripristina un'applicazione, si rimuovono le impostazioni utente personalizzate e si ripristinano le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="cb48a-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="cb48a-133">Questa azione non modifica né elimina i collegamenti o le associazioni di tipi di file e non rimuove l'applicazione dalla cache.</span><span class="sxs-lookup"><span data-stu-id="cb48a-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="cb48a-134">Per ripristinare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="cb48a-135">Posizionare il cursore nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="cb48a-136">Fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Ripristina** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="cb48a-137">Alla richiesta di conferma fare clic su **Sì** per ripristinare l'applicazione o **No** per annullare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="cb48a-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="cb48a-138">Come importare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-138">How to import an App-V application</span></span>


<span data-ttu-id="cb48a-139">È possibile usare la procedura seguente per importare un'applicazione nella cache direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="cb48a-140">Per importare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="cb48a-141">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Importa** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-142">Nella finestra **Sfoglia** passare al percorso del file del pacchetto per l'applicazione desiderata e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb48a-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="cb48a-143">**Nota**  Se è già stato configurato un percorso di ricerca di importazione o se il file SFT si trova nello stesso percorso dell'ultima importazione riuscita, il passaggio 2 non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cb48a-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="cb48a-144">Come bloccare o sbloccare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="cb48a-145">È possibile usare le procedure seguenti per bloccare o sbloccare qualsiasi applicazione nella cache del client Desktop Application Virtualization o nel client per la cache dei Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="cb48a-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="cb48a-146">Non è possibile rimuovere un'applicazione bloccata dalla cache per creare spazio per le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cb48a-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="cb48a-147">Per rimuovere un'applicazione bloccata dalla cache client Desktop Application Virtualization o dal client per la cache dei Servizi Desktop remoto, è necessario prima di tutto sbloccarla.</span><span class="sxs-lookup"><span data-stu-id="cb48a-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="cb48a-148">Per bloccare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="cb48a-148">To lock an application</span></span>**

1.  <span data-ttu-id="cb48a-149">Posizionare il cursore nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="cb48a-150">Fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **blocca** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="cb48a-151">L'applicazione selezionata è bloccata nella cache.</span><span class="sxs-lookup"><span data-stu-id="cb48a-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="cb48a-152">Per sbloccare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="cb48a-152">To unlock an application</span></span>**

1.  <span data-ttu-id="cb48a-153">Posizionare il cursore nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="cb48a-154">Fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Sblocca** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="cb48a-155">L'applicazione selezionata viene sbloccata nella cache e può essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="cb48a-156">Come eliminare un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-156">How to delete an App-V application</span></span>


<span data-ttu-id="cb48a-157">Quando si seleziona il nodo **dell'applicazione** nella console di gestione client Application Virtualization, nel riquadro dei **risultati** viene visualizzato un elenco di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cb48a-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="cb48a-158">Puoi usare la procedura seguente per eliminare un'applicazione dal riquadro dei **risultati** , che rimuove anche l'applicazione dalla cache.</span><span class="sxs-lookup"><span data-stu-id="cb48a-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="cb48a-159">**Nota**  Quando si elimina un'applicazione, l'applicazione selezionata non sarà più disponibile per gli utenti di tale client.</span><span class="sxs-lookup"><span data-stu-id="cb48a-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="cb48a-160">I tasti di scelta rapida e le associazioni di tipi di file sono nascosti e l'applicazione viene eliminata dalla cache.</span><span class="sxs-lookup"><span data-stu-id="cb48a-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="cb48a-161">Tuttavia, se un'altra applicazione fa riferimento ai dati nei dati della cache del file System per l'applicazione selezionata, questi elementi non verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="cb48a-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="cb48a-162">Dopo un aggiornamento della pubblicazione, le applicazioni eliminate diventeranno di nuovo disponibili.</span><span class="sxs-lookup"><span data-stu-id="cb48a-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="cb48a-163">Per eliminare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="cb48a-163">To delete an application</span></span>**

1.  <span data-ttu-id="cb48a-164">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **Elimina** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-165">Alla richiesta di conferma fare clic su **Sì** per rimuovere l'applicazione o fare clic su **No** per annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb48a-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="cb48a-166">Come modificare un'icona dell'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-166">How to change an App-V application icon</span></span>


<span data-ttu-id="cb48a-167">È possibile usare la procedura seguente per modificare un'icona associata all'applicazione selezionata direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="cb48a-168">Per modificare un'icona dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="cb48a-168">To change an application icon</span></span>**

1.  <span data-ttu-id="cb48a-169">Posizionare il cursore nel riquadro **dei risultati** e fare clic con il pulsante destro del mouse sull'applicazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="cb48a-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="cb48a-170">Selezionare **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="cb48a-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="cb48a-171">Nella scheda **generale** fare clic su **Cambia icona**.</span><span class="sxs-lookup"><span data-stu-id="cb48a-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="cb48a-172">Selezionare l'icona desiderata oppure passare a un'altra posizione per selezionare l'icona.</span><span class="sxs-lookup"><span data-stu-id="cb48a-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="cb48a-173">Dopo aver selezionato l'icona, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb48a-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="cb48a-174">La nuova icona viene visualizzata nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="cb48a-175">Come aggiungere un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-175">How to add an App-V application</span></span>


<span data-ttu-id="cb48a-176">È possibile usare la procedura seguente per aggiungere un'applicazione direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="cb48a-177">Per aggiungere un'applicazione</span><span class="sxs-lookup"><span data-stu-id="cb48a-177">To add an application</span></span>**

1.  <span data-ttu-id="cb48a-178">Nel riquadro **risultati** fare clic con il pulsante destro del mouse e scegliere **nuova applicazione** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-179">Nella pagina della procedura guidata è possibile eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb48a-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="cb48a-180">**Icona cambia**: Visualizza un browser di icone standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="cb48a-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="cb48a-181">Individuare e selezionare l'icona desiderata.</span><span class="sxs-lookup"><span data-stu-id="cb48a-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="cb48a-182">**URL o percorso file OSD**: immettere un percorso assoluto locale, un percorso UNC completo (file condiviso o directory in una rete) o un URL http.</span><span class="sxs-lookup"><span data-stu-id="cb48a-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="cb48a-183">**(Pulsante Sfoglia OSD)**: Visualizza la finestra di dialogo standard di Windows **Open file** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="cb48a-184">Individuare il file desiderato.</span><span class="sxs-lookup"><span data-stu-id="cb48a-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="cb48a-185">Fare clic su **fine** per aggiungere l'applicazione al riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="cb48a-186">Come pubblicare un collegamento a un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="cb48a-187">Puoi usare la procedura seguente per pubblicare i collegamenti a un'applicazione direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="cb48a-188">Per pubblicare i collegamenti alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="cb48a-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="cb48a-189">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **nuovo collegamento** dal menu a comparsa per visualizzare la creazione guidata nuovo collegamento.</span><span class="sxs-lookup"><span data-stu-id="cb48a-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="cb48a-190">Nella prima pagina della creazione guidata nuovo collegamento selezionare un'icona e specificare un nome per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="cb48a-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="cb48a-191">**Icona cambia**: Visualizza un browser di icone standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="cb48a-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="cb48a-192">Individuare e selezionare l'icona desiderata.</span><span class="sxs-lookup"><span data-stu-id="cb48a-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="cb48a-193">**Titolo del collegamento**: immettere il nome che si vuole assegnare al collegamento.</span><span class="sxs-lookup"><span data-stu-id="cb48a-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="cb48a-194">Questo campo viene impostato come predefinito per il nome e la versione esistenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb48a-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="cb48a-195">Nella seconda pagina della procedura guidata determinare la posizione del collegamento pubblicato.</span><span class="sxs-lookup"><span data-stu-id="cb48a-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="cb48a-196">**Desktop**: selezionare questa casella di controllo per pubblicare il collegamento sul desktop.</span><span class="sxs-lookup"><span data-stu-id="cb48a-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="cb48a-197">**Barra di avvio veloce**: selezionare questa casella di controllo per pubblicare il collegamento sulla barra di avvio veloce.</span><span class="sxs-lookup"><span data-stu-id="cb48a-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="cb48a-198">**Menu Invia a**: selezionare questa casella di controllo per pubblicare il collegamento al menu **Invia a** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="cb48a-199">**Programmi nel menu Start**: quando si seleziona la casella di controllo **menu Start** , questo campo diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="cb48a-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="cb48a-200">Lascia vuoto questo campo per pubblicare il collegamento direttamente nella radice della cartella programmi oppure immetti un nome di cartella o una gerarchia, ad esempio "My \ _Computer applicazioni \\Office".</span><span class="sxs-lookup"><span data-stu-id="cb48a-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="cb48a-201">I collegamenti creati in questo modo sono disponibili solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="cb48a-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="cb48a-202">**Altro percorso** e pulsante **Sfoglia** : quando si seleziona la casella di controllo **altro percorso** , questo campo diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="cb48a-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="cb48a-203">Immettere una posizione valida nel computer o in qualsiasi percorso UNC disponibile (file condiviso o directory in una rete).</span><span class="sxs-lookup"><span data-stu-id="cb48a-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="cb48a-204">Il pulsante **Sfoglia** Visualizza una finestra di dialogo **Apri file** standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="cb48a-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="cb48a-205">Nella terza pagina della procedura guidata Immetti i parametri della riga di comando desiderati.</span><span class="sxs-lookup"><span data-stu-id="cb48a-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="cb48a-206">Fare clic su **fine** per pubblicare i tasti di scelta rapida e quindi uscire dal riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="cb48a-207">Come aggiungere un'associazione di tipi di file per un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="cb48a-208">Puoi usare la procedura seguente per aggiungere un'associazione di tipi di file, usando il nodo **associazioni di tipi di file** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cb48a-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="cb48a-209">Per aggiungere un'associazione di tipi di file</span><span class="sxs-lookup"><span data-stu-id="cb48a-209">To add a file type association</span></span>**

1.  <span data-ttu-id="cb48a-210">Fare clic con il pulsante destro del mouse sul nodo **associazioni tipo file** e scegliere **nuova associazione** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cb48a-211">Completare il primo passaggio della finestra di dialogo completando le informazioni seguenti e quindi fare clic su **Avanti**:</span><span class="sxs-lookup"><span data-stu-id="cb48a-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="cb48a-212">**Estensione**: immettere una nuova estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="cb48a-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="cb48a-213">Questo campo è vuoto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb48a-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="cb48a-214">**Creare un nuovo tipo di file con questa descrizione**: selezionare questo pulsante di opzione per immettere una nuova descrizione del tipo di file nel campo attivo.</span><span class="sxs-lookup"><span data-stu-id="cb48a-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="cb48a-215">Questo pulsante è selezionato per impostazione predefinita e il campo attivo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="cb48a-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="cb48a-216">**Applica questo tipo di file a tutti gli utenti**: selezionare questa casella di controllo quando si vuole che l'associazione sia globale per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="cb48a-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="cb48a-217">Per impostazione predefinita, questa casella è deselezionata.</span><span class="sxs-lookup"><span data-stu-id="cb48a-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="cb48a-218">**Collegare questa estensione a un tipo di file esistente**: selezionare questo pulsante di opzione per associare l'estensione a un tipo di file esistente.</span><span class="sxs-lookup"><span data-stu-id="cb48a-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="cb48a-219">Selezionare un tipo di file nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="cb48a-220">Quando si sceglie questa opzione, il **successivo** viene modificato in **fine**.</span><span class="sxs-lookup"><span data-stu-id="cb48a-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="cb48a-221">Completare il secondo passaggio della finestra di dialogo completando le informazioni seguenti e quindi fare clic su **fine** per tornare alla console di gestione client:</span><span class="sxs-lookup"><span data-stu-id="cb48a-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="cb48a-222">**Icona cambia**: fare clic su questo pulsante per modificare l'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb48a-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="cb48a-223">Selezionare una delle icone disponibili oppure passare a una nuova posizione e selezionare un'icona.</span><span class="sxs-lookup"><span data-stu-id="cb48a-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="cb48a-224">**Aprire i file con l'applicazione selezionata**: selezionare questo pulsante di opzione per aprire il file con un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cb48a-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="cb48a-225">Scegliere un'applicazione nell'elenco a discesa delle applicazioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="cb48a-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="cb48a-226">**Aprire il file con l'associazione descritta in questo file OSD**: selezionare questo pulsante di opzione per specificare un file OSD (Open Software Descriptor) che determina l'applicazione usata per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="cb48a-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="cb48a-227">Usare il pulsante Sfoglia per selezionare una posizione esistente oppure immettere un percorso o un URL in formato HTTP in questo campo.</span><span class="sxs-lookup"><span data-stu-id="cb48a-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="cb48a-228">Come eliminare un'associazione di tipi di file per un'applicazione App-V</span><span class="sxs-lookup"><span data-stu-id="cb48a-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="cb48a-229">Per eliminare un'associazione di tipi di file, è possibile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="cb48a-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="cb48a-230">Il nodo **associazioni tipo di file** è un livello sotto il nodo **Application Virtualization** nel riquadro **ambito** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="cb48a-231">Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="cb48a-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="cb48a-232">Per rimuovere un'associazione di tipi di file</span><span class="sxs-lookup"><span data-stu-id="cb48a-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="cb48a-233">Nel riquadro **risultati** fare clic con il pulsante destro del mouse sull'estensione dell'associazione del tipo di file che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="cb48a-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="cb48a-234">Selezionare **Elimina** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="cb48a-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="cb48a-235">Fare clic su **Sì** per eliminare l'associazione oppure fare clic su **No** per tornare al riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="cb48a-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="cb48a-236">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb48a-236">Related topics</span></span>


[<span data-ttu-id="cb48a-237">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="cb48a-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





