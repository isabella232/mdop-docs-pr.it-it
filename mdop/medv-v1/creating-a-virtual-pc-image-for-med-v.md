---
title: Creazione di un'immagine Virtual PC per MED-V
description: Creazione di un'immagine Virtual PC per MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823665"
---
# <span data-ttu-id="0baee-103">Creazione di un'immagine Virtual PC per MED-V</span><span class="sxs-lookup"><span data-stu-id="0baee-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="0baee-104">Per creare un'immagine di un PC virtuale (VPC) per MED-V, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0baee-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="0baee-105">[Creare un'immagine VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="0baee-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="0baee-106">[Installare il pacchetto di Workspace. msi MED-V nell'immagine VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).</span><span class="sxs-lookup"><span data-stu-id="0baee-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="0baee-107">[Eseguire lo strumento di prerequisiti della macchina virtuale MED-V nell'immagine VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).</span><span class="sxs-lookup"><span data-stu-id="0baee-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="0baee-108">[Configurare manualmente i prerequisiti della macchina virtuale nell'immagine VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span><span class="sxs-lookup"><span data-stu-id="0baee-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="0baee-109">[Configurare Sysprep per le immagini MED-V](#bkmk-howtoconfiguresysprepformedvimages) (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="0baee-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="0baee-110">[Disattivare Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="0baee-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="0baee-111">Creazione di un'immagine PC virtuale tramite Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0baee-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="0baee-112">Per creare un'immagine di Virtual PC con Microsoft Virtual PC, vedere la documentazione di Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="0baee-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="0baee-113">Per ulteriori informazioni, vedere le pagine seguenti:</span><span class="sxs-lookup"><span data-stu-id="0baee-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="0baee-114">Guida di Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0baee-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="0baee-115">Creare una macchina virtuale e installare un sistema operativo guest</span><span class="sxs-lookup"><span data-stu-id="0baee-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="0baee-116">Come installare il pacchetto di area di lavoro MED-V. msi</span><span class="sxs-lookup"><span data-stu-id="0baee-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="0baee-117">Dopo aver creato l'immagine di Virtual PC, installare il pacchetto MED-V Workspace. msi nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0baee-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="0baee-118">Per installare l'immagine dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="0baee-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="0baee-119">Avviare la macchina virtuale e copiare il pacchetto Workspace. msi MED-V.</span><span class="sxs-lookup"><span data-stu-id="0baee-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="0baee-120">Il pacchetto MSI di area di lavoro MED-V si chiama *MED-V\_workspace\_x.msi*, dove *x* è il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="0baee-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="0baee-121">Ad esempio, *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="0baee-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="0baee-122">Fare doppio clic sul pacchetto Workspace. msi MED-V e seguire le istruzioni per l'installazione guidata.</span><span class="sxs-lookup"><span data-stu-id="0baee-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="0baee-123">Nota</span><span class="sxs-lookup"><span data-stu-id="0baee-123">Note</span></span>**  
    <span data-ttu-id="0baee-124">Quando viene rilasciata una nuova versione di MED-V e viene aggiornata un'immagine del PC virtuale esistente, disinstallare il pacchetto esistente di area di lavoro MED-V. msi, riavviare il computer e installare il nuovo pacchetto di Workspace. msi di MED-V.</span><span class="sxs-lookup"><span data-stu-id="0baee-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="0baee-125">Come eseguire lo strumento prerequisiti macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0baee-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="0baee-126">Lo strumento dei prerequisiti della macchina virtuale (VM) è una procedura guidata che automatizza diversi dei prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="0baee-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="0baee-127">Nota</span><span class="sxs-lookup"><span data-stu-id="0baee-127">Note</span></span>**  
<span data-ttu-id="0baee-128">Anche se molti parametri sono configurabili nella procedura guidata, le proprietà necessarie per il corretto funzionamento di MED-V non sono configurabili.</span><span class="sxs-lookup"><span data-stu-id="0baee-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="0baee-129">Per eseguire lo strumento prerequisiti macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0baee-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="0baee-130">Dopo aver installato il pacchetto di area di lavoro MED-V. msi, nel menu **Start** di Windows selezionare **tutti i programmi &gt; Med-v &gt; VM prerequisiti Tool**.</span><span class="sxs-lookup"><span data-stu-id="0baee-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="0baee-131">Nota</span><span class="sxs-lookup"><span data-stu-id="0baee-131">Note</span></span>**  
    <span data-ttu-id="0baee-132">L'utente che ha eseguito lo strumento prerequisiti della macchina virtuale deve avere diritti di amministratore locale e deve essere l'unico utente connesso.</span><span class="sxs-lookup"><span data-stu-id="0baee-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="0baee-133">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="0baee-133">Click **Next**.</span></span>

3. <span data-ttu-id="0baee-134">Nella pagina **impostazioni di Windows** , dalle proprietà configurabili seguenti selezionare quelle da configurare:</span><span class="sxs-lookup"><span data-stu-id="0baee-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="0baee-135">Cancellare le informazioni sulla cronologia personale degli utenti</span><span class="sxs-lookup"><span data-stu-id="0baee-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="0baee-136">Cancellare la directory Temp dei profili locali</span><span class="sxs-lookup"><span data-stu-id="0baee-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="0baee-137">Disabilitare i suoni negli eventi di Windows seguenti: Start, Logon, disconnessione</span><span class="sxs-lookup"><span data-stu-id="0baee-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="0baee-138">Nota</span><span class="sxs-lookup"><span data-stu-id="0baee-138">Note</span></span>**  
   <span data-ttu-id="0baee-139">Non abilitare Windows Page Saver in un criterio di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0baee-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="0baee-140">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="0baee-140">Click **Next**.</span></span>

5. <span data-ttu-id="0baee-141">Nella pagina **impostazioni di Internet Explorer** , dalle proprietà configurabili seguenti, selezionare quelle da configurare:</span><span class="sxs-lookup"><span data-stu-id="0baee-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="0baee-142">Non usare le caratteristiche di completamento automatico</span><span class="sxs-lookup"><span data-stu-id="0baee-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="0baee-143">Disabilitare il riutilizzo di Windows per l'avvio dei collegamenti</span><span class="sxs-lookup"><span data-stu-id="0baee-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="0baee-144">Cancellare la cronologia esplorazioni</span><span class="sxs-lookup"><span data-stu-id="0baee-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="0baee-145">Abilitare l'esplorazione a schede in Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="0baee-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="0baee-146">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="0baee-146">Click **Next**.</span></span>

7. <span data-ttu-id="0baee-147">Nella pagina **Servizi Windows** , dalle proprietà configurabili seguenti selezionare quelle da configurare:</span><span class="sxs-lookup"><span data-stu-id="0baee-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="0baee-148">Servizio Centro sicurezza</span><span class="sxs-lookup"><span data-stu-id="0baee-148">Security center service</span></span>**

   -   **<span data-ttu-id="0baee-149">Servizio Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0baee-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="0baee-150">Servizio Aggiornamenti automatici</span><span class="sxs-lookup"><span data-stu-id="0baee-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="0baee-151">Servizio Ripristino configurazione di sistema</span><span class="sxs-lookup"><span data-stu-id="0baee-151">System restore service</span></span>**

   -   **<span data-ttu-id="0baee-152">Servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="0baee-152">Indexing service</span></span>**

   -   **<span data-ttu-id="0baee-153">Configurazione wireless zero</span><span class="sxs-lookup"><span data-stu-id="0baee-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="0baee-154">Compatibilità con il cambio rapido degli utenti</span><span class="sxs-lookup"><span data-stu-id="0baee-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="0baee-155">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="0baee-155">Click **Next**.</span></span>

9. <span data-ttu-id="0baee-156">Nella pagina **accesso automatico di Windows** eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0baee-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="0baee-157">Selezionare la casella di controllo **Abilita accesso automatico di Windows** .</span><span class="sxs-lookup"><span data-stu-id="0baee-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="0baee-158">Assegnare un **nome utente** e una **password**.</span><span class="sxs-lookup"><span data-stu-id="0baee-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="0baee-159">Fare clic su **applica**e quindi, nella casella di conferma visualizzata, fare clic su **Sì**.</span><span class="sxs-lookup"><span data-stu-id="0baee-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="0baee-160">Nella pagina **Riepilogo** fare clic su **fine** per chiudere la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="0baee-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="0baee-161">Nota</span><span class="sxs-lookup"><span data-stu-id="0baee-161">Note</span></span>**  
<span data-ttu-id="0baee-162">Verificare che i criteri di gruppo non sovrascrivano le impostazioni obbligatorie impostate nello strumento prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="0baee-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="0baee-163">Come configurare i prerequisiti di installazione manuale della macchina virtuale MED-V</span><span class="sxs-lookup"><span data-stu-id="0baee-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="0baee-164">Diverse configurazioni non possono essere configurate tramite lo strumento prerequisiti macchina virtuale e devono essere eseguite manualmente.</span><span class="sxs-lookup"><span data-stu-id="0baee-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="0baee-165">Impostazioni della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0baee-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="0baee-166">È consigliabile configurare le impostazioni della macchina virtuale seguenti in Microsoft Virtual PC Console:</span><span class="sxs-lookup"><span data-stu-id="0baee-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="0baee-167">Disabilitare le unità disco floppy.</span><span class="sxs-lookup"><span data-stu-id="0baee-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="0baee-168">Disabilitare Undo-Disks (**Settings &gt; Undo-disks**).</span><span class="sxs-lookup"><span data-stu-id="0baee-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="0baee-169">Verificare che l'immagine disponga di una sola CPU virtuale.</span><span class="sxs-lookup"><span data-stu-id="0baee-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="0baee-170">Eliminare le interazioni tra la macchina virtuale e l'utente, in cui non sono correlate alle applicazioni pubblicate, ad esempio i messaggi che richiedono l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0baee-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="0baee-171">Impostazioni immagine</span><span class="sxs-lookup"><span data-stu-id="0baee-171">Image Settings</span></span>

    <span data-ttu-id="0baee-172">Configurare le impostazioni manuali seguenti nell'immagine:</span><span class="sxs-lookup"><span data-stu-id="0baee-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="0baee-173">Nella finestra delle **proprietà delle opzioni risparmio energia** disattivare l'ibernazione e il sonno.</span><span class="sxs-lookup"><span data-stu-id="0baee-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="0baee-174">Applicare gli aggiornamenti di Windows più recenti.</span><span class="sxs-lookup"><span data-stu-id="0baee-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="0baee-175">Nella sezione **errore sistema** della finestra di dialogo **avvio e ripristino di Windows** deselezionare la casella di controllo **Riavvia automaticamente** .</span><span class="sxs-lookup"><span data-stu-id="0baee-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="0baee-176">Verificare che l'immagine usi una chiave di licenza di VLK.</span><span class="sxs-lookup"><span data-stu-id="0baee-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="0baee-177">Installazione delle aggiunte di VPC</span><span class="sxs-lookup"><span data-stu-id="0baee-177">Installing VPC Additions</span></span>

    <span data-ttu-id="0baee-178">Nel menu **azione** selezionare **Installa o aggiorna aggiunte macchina virtuale**.</span><span class="sxs-lookup"><span data-stu-id="0baee-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="0baee-179">Configurazione della stampa</span><span class="sxs-lookup"><span data-stu-id="0baee-179">Configuring Printing</span></span>

    <span data-ttu-id="0baee-180">È possibile configurare la stampa dall'area di lavoro MED-V in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0baee-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="0baee-181">Aggiungere una stampante alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0baee-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="0baee-182">Consentire la stampa con le stampanti configurate nel computer host.</span><span class="sxs-lookup"><span data-stu-id="0baee-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="0baee-183">Come configurare Sysprep per le immagini di MED-V</span><span class="sxs-lookup"><span data-stu-id="0baee-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="0baee-184">In un'area di lavoro MED-V è possibile configurare Sysprep per l'assegnazione di ID di sicurezza univoco (SID), in particolare quando vengono eseguite più aree di lavoro MED-V in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="0baee-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="0baee-185">Non è consigliabile usare Sysprep per partecipare a un dominio; USA invece l'azione di script Domain Join di MED-V come descritto in [come configurare le azioni di script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0baee-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="0baee-186">Nota</span><span class="sxs-lookup"><span data-stu-id="0baee-186">Note</span></span>**  
<span data-ttu-id="0baee-187">Sysprep è l'utilità per la preparazione del sistema Microsoft per il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0baee-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="0baee-188">Per configurare Sysprep in un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="0baee-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="0baee-189">Creare una directory nella radice dell'unità di sistema denominata *Sysprep*.</span><span class="sxs-lookup"><span data-stu-id="0baee-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="0baee-190">Nel CD di installazione di Windows estrarre *deploy.cab* nella radice dell'unità di sistema oppure scaricare l'aggiornamento degli strumenti di distribuzione più recenti dal sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0baee-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="0baee-191">Per Windows 2000, vedere [aggiornamento degli strumenti di distribuzione per windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span><span class="sxs-lookup"><span data-stu-id="0baee-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="0baee-192">Per Windows XP, vedere [aggiornamento degli strumenti di distribuzione per Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span><span class="sxs-lookup"><span data-stu-id="0baee-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="0baee-193">Eseguire **Setup Manager** (setupmgr.exe).</span><span class="sxs-lookup"><span data-stu-id="0baee-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="0baee-194">Seguire la configurazione guidata di Setup Manager.</span><span class="sxs-lookup"><span data-stu-id="0baee-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="0baee-195">Dopo aver configurato Sysprep e creato l'area di lavoro MED-V, è necessario eseguire Sysprep.</span><span class="sxs-lookup"><span data-stu-id="0baee-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="0baee-196">Per eseguire Sysprep</span><span class="sxs-lookup"><span data-stu-id="0baee-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="0baee-197">Nella cartella Sysprep situata nella radice dell'unità di sistema eseguire lo strumento preparazione sistema (Sysprep.exe).</span><span class="sxs-lookup"><span data-stu-id="0baee-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="0baee-198">Nella finestra di messaggio di avviso che viene visualizzata fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="0baee-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="0baee-199">Nella finestra di dialogo **Proprietà Sysprep** selezionare la casella **di controllo non reimpostare il periodo di tolleranza per l'attivazione** e **usare la configurazione minima** .</span><span class="sxs-lookup"><span data-stu-id="0baee-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="0baee-200">Fare clic su **Richiudi**.</span><span class="sxs-lookup"><span data-stu-id="0baee-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="0baee-201">Se non si è soddisfatti delle informazioni elencate nella casella del messaggio di conferma che viene visualizzata, fare clic su **Annulla** e modificare le selezioni.</span><span class="sxs-lookup"><span data-stu-id="0baee-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="0baee-202">Fare clic su **OK** per completare il processo di preparazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="0baee-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="0baee-203">Disattivazione di Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0baee-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="0baee-204">Dopo che tutti i componenti sono stati installati e configurati, chiudere Microsoft Virtual PC e selezionare **Disattiva**.</span><span class="sxs-lookup"><span data-stu-id="0baee-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="0baee-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0baee-205">Related topics</span></span>


<span data-ttu-id="0baee-206">Creazione di un'immagine MED-V [come configurare le azioni di script](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="0baee-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>









