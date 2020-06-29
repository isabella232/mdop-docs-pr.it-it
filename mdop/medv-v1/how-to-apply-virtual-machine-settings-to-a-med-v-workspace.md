---
title: Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V
description: Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825975"
---
# <span data-ttu-id="81e06-103">Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="81e06-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="81e06-104">Ogni area di lavoro MED-V deve avere un'immagine di Microsoft Virtual PC associata.</span><span class="sxs-lookup"><span data-stu-id="81e06-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="81e06-105">Le impostazioni della macchina virtuale consentono di assegnare un'immagine Virtual PC e di impostare altre proprietà della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81e06-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="81e06-106">Tutte le impostazioni della macchina virtuale sono configurate nel modulo **criteri** , nella scheda **Impostazioni macchina virtuale** .</span><span class="sxs-lookup"><span data-stu-id="81e06-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="81e06-107">Per applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="81e06-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="81e06-108">Fare clic sull'area di lavoro MED-V per configurare.</span><span class="sxs-lookup"><span data-stu-id="81e06-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="81e06-109">Configurare le proprietà della macchina virtuale come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="81e06-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="81e06-110">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="81e06-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="81e06-111">Proprietà della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="81e06-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="81e06-112">Impostazioni della *macchina virtuale* della descrizione della proprietà</span><span class="sxs-lookup"><span data-stu-id="81e06-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="81e06-113">Immagine assegnata</span><span class="sxs-lookup"><span data-stu-id="81e06-113">Assigned Image</span></span>

<span data-ttu-id="81e06-114">Immagine effettiva di Microsoft Virtual PC assegnata all'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="81e06-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="81e06-115">Il menu contiene un elenco di tutte le immagini di Virtual PC disponibili.</span><span class="sxs-lookup"><span data-stu-id="81e06-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="81e06-116">I tipi di immagine seguenti si trovano nell'elenco delle immagini **attive** :</span><span class="sxs-lookup"><span data-stu-id="81e06-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="81e06-117">**Immagini di test locali**: immagini nel computer locale non ancora imballate.</span><span class="sxs-lookup"><span data-stu-id="81e06-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="81e06-118">Questi nomi di immagine sono seguiti dalla parola "test" tra parentesi (test) e sono solo per scopi di test.</span><span class="sxs-lookup"><span data-stu-id="81e06-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="81e06-119">**Immagini**imballate locali: immagini confezionate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="81e06-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="81e06-120">Queste immagini sono seguite dalla parola "local" tra parentesi (local) e non possono essere scaricate dai client finché l'amministratore non le carica nel server.</span><span class="sxs-lookup"><span data-stu-id="81e06-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="81e06-121">È possibile selezionare un'immagine locale se si sta creando un pacchetto che verrà distribuito al client tramite elementi multimediali rimovibili, ad esempio USB o DVD.</span><span class="sxs-lookup"><span data-stu-id="81e06-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="81e06-122">**Immagini imballate sul server**: immagini presenti nel server e disponibili per il download dai client.</span><span class="sxs-lookup"><span data-stu-id="81e06-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="81e06-123">Fare clic su Aggiorna per aggiornare l'elenco immagini.</span><span class="sxs-lookup"><span data-stu-id="81e06-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="81e06-124">**Nota**  Ogni immagine dell'area di lavoro MED-V può essere usata solo da un utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="81e06-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="81e06-125">L'area di lavoro è persistente</span><span class="sxs-lookup"><span data-stu-id="81e06-125">Workspace is persistent</span></span>

<span data-ttu-id="81e06-126">Selezionare questa casella di controllo per configurare l'area di lavoro MED-V come persistente.</span><span class="sxs-lookup"><span data-stu-id="81e06-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="81e06-127">In un'area di lavoro MED-V persistente, quando l'area di lavoro MED-V viene interrotta, le modifiche e le aggiunte all'area di lavoro MED-v vengono salvate nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="81e06-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="81e06-128">Per un'area di lavoro di dominio MED-V, questa opzione deve essere selezionata.</span><span class="sxs-lookup"><span data-stu-id="81e06-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="81e06-129">**Nota**  Questa impostazione non deve essere modificata dopo la distribuzione di un'area di lavoro MED-V agli utenti.</span><span class="sxs-lookup"><span data-stu-id="81e06-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="81e06-130">Arrestare la VM quando si arresta l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="81e06-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="81e06-131">Selezionare questa casella di controllo per arrestare la macchina virtuale quando si arresta l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="81e06-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="81e06-132">Se questa casella di controllo è deselezionata, al termine di ogni sessione la macchina virtuale non viene arrestata, ma accetta invece uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81e06-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="81e06-133">Dopo l'avvio di una nuova sessione, Windows viene avviato dallo snapshot, ovvero Windows non viene riavviato e non è necessario alcun accesso.</span><span class="sxs-lookup"><span data-stu-id="81e06-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="81e06-134">**Nota**  Questa proprietà è abilitata solo se l' **area di lavoro è permanente** selezionata.</span><span class="sxs-lookup"><span data-stu-id="81e06-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="81e06-135">Accedere a Windows in VM usando le credenziali MED-V (SSO)</span><span class="sxs-lookup"><span data-stu-id="81e06-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="81e06-136">Selezionare questa casella di controllo per accedere a Windows nella macchina virtuale usando le credenziali MED-V immesse durante l'accesso al client MED-V.</span><span class="sxs-lookup"><span data-stu-id="81e06-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="81e06-137">**Nota**  Questa proprietà è abilitata solo quando è selezionata l' **area di lavoro persistente** .</span><span class="sxs-lookup"><span data-stu-id="81e06-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="81e06-138">Area di lavoro è revertible</span><span class="sxs-lookup"><span data-stu-id="81e06-138">Workspace is revertible</span></span>

<span data-ttu-id="81e06-139">Selezionare questa casella di controllo per configurare l'area di lavoro MED-V come revertible.</span><span class="sxs-lookup"><span data-stu-id="81e06-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="81e06-140">In un'area di lavoro di revertible MED-V, al termine di ogni sessione (ovvero quando l'utente interrompe l'area di lavoro MED-V), l'area di lavoro MED-V ripristina lo stato originale durante la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="81e06-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="81e06-141">Nessuna modifica o aggiunta che l'utente ha eseguito viene salvata nell'area di lavoro MED-V tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="81e06-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="81e06-142">**Nota**  Questa impostazione non deve essere modificata dopo la distribuzione di un'area di lavoro MED-V agli utenti.</span><span class="sxs-lookup"><span data-stu-id="81e06-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="81e06-143">Sincronizzare il fuso orario dell'area di lavoro con host</span><span class="sxs-lookup"><span data-stu-id="81e06-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="81e06-144">Selezionare questa casella di controllo per sincronizzare il fuso orario nell'area di lavoro MED-V con l'host.</span><span class="sxs-lookup"><span data-stu-id="81e06-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="81e06-145">La sincronizzazione funziona in modo diverso a seconda che l'area di lavoro MED-V sia permanente o revertible, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="81e06-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="81e06-146">In un'area di lavoro MED-V persistente, il fuso orario cerca prima di eseguire la sincronizzazione con il server.</span><span class="sxs-lookup"><span data-stu-id="81e06-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="81e06-147">Se l'operazione non riesce, viene sincronizzata con l'host.</span><span class="sxs-lookup"><span data-stu-id="81e06-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="81e06-148">In un'area di lavoro di revertible MED-V, il fuso orario viene sincronizzato con l'host.</span><span class="sxs-lookup"><span data-stu-id="81e06-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="81e06-149">Bloccare le impostazioni</span><span class="sxs-lookup"><span data-stu-id="81e06-149">Lock Settings</span></span>*

<span data-ttu-id="81e06-150">Bloccare l'area di lavoro nell'evento standby/ibernazione host</span><span class="sxs-lookup"><span data-stu-id="81e06-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="81e06-151">Selezionare questa casella di controllo per bloccare automaticamente l'area di lavoro MED-V quando il computer host entra in standby o in ibernazione.</span><span class="sxs-lookup"><span data-stu-id="81e06-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="81e06-152">Bloccare l'area di lavoro dopo</span><span class="sxs-lookup"><span data-stu-id="81e06-152">Lock the Workspace after</span></span>

<span data-ttu-id="81e06-153">Selezionare questa casella di controllo per bloccare l'area di lavoro MED-V quando l'area di lavoro MED-V è inattiva per un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="81e06-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="81e06-154">Quando l'opzione è selezionata, la casella numero è abilitata.</span><span class="sxs-lookup"><span data-stu-id="81e06-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="81e06-155">Immettere il numero di minuti di tempo di inattività prima di bloccare l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="81e06-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="81e06-156">**Nota**  Il tempo di inattività fa riferimento alle applicazioni di area di lavoro MED-V (non alle applicazioni host).</span><span class="sxs-lookup"><span data-stu-id="81e06-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="81e06-157">Impostazioni di aggiornamento delle immagini</span><span class="sxs-lookup"><span data-stu-id="81e06-157">Image Update Settings</span></span>*

<span data-ttu-id="81e06-158">Mantieni solo</span><span class="sxs-lookup"><span data-stu-id="81e06-158">Keep only</span></span>

<span data-ttu-id="81e06-159">Selezionare questa casella di controllo per limitare il numero di versioni di immagini obsolete da conservare.</span><span class="sxs-lookup"><span data-stu-id="81e06-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="81e06-160">Quando l'opzione è selezionata, la casella numero è abilitata.</span><span class="sxs-lookup"><span data-stu-id="81e06-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="81e06-161">Immettere il numero di versioni precedenti da conservare.</span><span class="sxs-lookup"><span data-stu-id="81e06-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="81e06-162">Suggerisci aggiornamento quando è disponibile una nuova versione</span><span class="sxs-lookup"><span data-stu-id="81e06-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="81e06-163">Selezionare questa casella di controllo per suggerire (ma non forzare) un aggiornamento quando è disponibile una nuova versione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="81e06-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="81e06-164">I client devono usare il trasferimento trim durante il download di immagini per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="81e06-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="81e06-165">Selezionare questa casella di controllo per abilitare il trasferimento Trim (per altre informazioni, vedere [tecnologia di trasferimento Trim Med-v](med-v-trim-transfer-technology-medvv2.md)) durante il download di immagini associate all'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="81e06-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="81e06-166">Se questa casella di controllo è deselezionata, verrà scaricata l'immagine completa.</span><span class="sxs-lookup"><span data-stu-id="81e06-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="81e06-167">**Nota**  Trim Transfer richiede l'indicizzazione del disco rigido, che può richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="81e06-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="81e06-168">È consigliabile usare il trasferimento di trim quando l'indicizzazione del disco rigido è più efficiente del download della nuova versione dell'immagine, ad esempio quando si scarica una versione di immagine simile alla versione esistente.</span><span class="sxs-lookup"><span data-stu-id="81e06-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="81e06-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81e06-169">Related topics</span></span>


[<span data-ttu-id="81e06-170">Creazione di un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="81e06-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="81e06-171">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="81e06-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="81e06-172">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="81e06-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





