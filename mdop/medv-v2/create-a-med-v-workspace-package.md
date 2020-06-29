---
title: Creare un pacchetto nell'area di lavoro MED-V
description: Creare un pacchetto nell'area di lavoro MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823265"
---
# <span data-ttu-id="7f862-103">Creare un pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-103">Create a MED-V Workspace Package</span></span>


<span data-ttu-id="7f862-104">Un'area di lavoro MED-V è l'ambiente desktop Windows XP in cui gli utenti finali interagiscono con la macchina virtuale fornita da MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-104">A MED-V workspace is the Windows XP desktop environment where end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="7f862-105">L'amministratore crea e Personalizza l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-105">The administrator creates and customizes the MED-V workspace.</span></span> <span data-ttu-id="7f862-106">L'area di lavoro è costituita da un'immagine e da criteri di gruppo che definiscono le regole e le funzionalità dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-106">The workspace consists of an image and the Group Policy that defines the rules and functionality of the MED-V workspace.</span></span>

<span data-ttu-id="7f862-107">È possibile creare più aree di lavoro MED-V, ognuna personalizzata con la propria configurazione, le impostazioni e le regole.</span><span class="sxs-lookup"><span data-stu-id="7f862-107">You can create multiple MED-V workspaces, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="7f862-108">Un utente, un gruppo o più utenti o gruppi può essere associato a ogni area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-108">A user, group, or multiple users or groups can be associated with each MED-V workspace.</span></span> <span data-ttu-id="7f862-109">La personalizzazione rende disponibile l'area di lavoro MED-V solo per l'utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="7f862-109">The customization makes that MED-V workspace available only for that user or group.</span></span>

<span data-ttu-id="7f862-110">USA **Packager area di lavoro MED-v** per creare aree di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="7f862-110">Use the **MED-V Workspace Packager** to create MED-V workspaces.</span></span> <span data-ttu-id="7f862-111">Il **Packager area di lavoro MED-V** è suddiviso in due sezioni principali:</span><span class="sxs-lookup"><span data-stu-id="7f862-111">The **MED-V Workspace Packager** is divided into two main sections:</span></span>

-   <span data-ttu-id="7f862-112">Pannello principale che include tre pulsanti che si usano per creare e gestire aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-112">A main panel that includes three buttons that you use to create and manage MED-V workspaces.</span></span> <span data-ttu-id="7f862-113">Il pulsante **Crea un pacchetto di area di lavoro MED-v** apre la **procedura guidata Crea pacchetto area di lavoro MED-v** che si usa per creare le aree di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="7f862-113">The **Create a MED-V Workspace Package** button opens the **Create MED-V Workspace Package Wizard** that you use to create your MED-V workspaces.</span></span>

-   <span data-ttu-id="7f862-114">**Centro assistenza** sul lato destro della finestra che fornisce informazioni e indicazioni utili per creare, testare e gestire le aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-114">A **Help Center** on the right-hand side of the window that provides information and guidance to help you create, test, and manage your MED-V workspaces.</span></span>

**<span data-ttu-id="7f862-115">Importante</span><span class="sxs-lookup"><span data-stu-id="7f862-115">Important</span></span>**  
<span data-ttu-id="7f862-116">Prima di poter usare **Packager area di lavoro MED-V**, devi prima di tutto verificare che il criterio di esecuzione di Windows PowerShell sia impostato su senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="7f862-116">Before you can use the **MED-V Workspace Packager**, you must first make sure that the Windows PowerShell execution policy is set to Unrestricted.</span></span>

`Set-ExecutionPolicy Unrestricted`

<span data-ttu-id="7f862-117">Inoltre, il criterio SAN per il computer in cui viene eseguito il **Packager area di lavoro MED-V** deve essere impostato su "online All".</span><span class="sxs-lookup"><span data-stu-id="7f862-117">In addition, the SAN policy for the computer on which the **MED-V Workspace Packager** is run must be set to “Online All”.</span></span> <span data-ttu-id="7f862-118">Per controllare l'impostazione del criterio SAN, eseguire i comandi seguenti in un prompt dei comandi con credenziali amministrative:</span><span class="sxs-lookup"><span data-stu-id="7f862-118">To check the setting of the SAN policy, run the following commands at a command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

<span data-ttu-id="7f862-119">Se necessario, modificare i criteri di SAN in "online All" digitando i comandi seguenti al prompt dei comandi con le credenziali amministrative:</span><span class="sxs-lookup"><span data-stu-id="7f862-119">If it is necessary, change the SAN policy to "Online All" by typing the following commands at the command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**<span data-ttu-id="7f862-120">Importante</span><span class="sxs-lookup"><span data-stu-id="7f862-120">Important</span></span>**  
<span data-ttu-id="7f862-121">Se nel computer che si usa per montare il disco rigido virtuale e creare il pacchetto di area di lavoro MED-V è installato il software di crittografia automatica del disco, è necessario disabilitare il software prima di iniziare.</span><span class="sxs-lookup"><span data-stu-id="7f862-121">If automatic disk encryption software is installed on the computer that you use to mount the virtual hard disk and build the MED-V workspace package, you must disable the software before you start.</span></span> <span data-ttu-id="7f862-122">In caso contrario, non è possibile usare l'area di lavoro MED-V in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="7f862-122">Otherwise, you cannot use the MED-V workspace on any other computer.</span></span>



<span data-ttu-id="7f862-123">Le informazioni fornite in questo articolo consentono di creare il pacchetto di distribuzione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-123">The information we provide here can help you create your MED-V workspace deployment package.</span></span>

## <a href="" id="bkmk-prereq"></a><span data-ttu-id="7f862-124">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7f862-124">Prerequisites</span></span>


<span data-ttu-id="7f862-125">Prima di iniziare a creare il pacchetto di distribuzione dell'area di lavoro MED-V, verificare di avere accesso agli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f862-125">Before you start to build your MED-V workspace deployment package, verify that you have access to the following items:</span></span>

-   **<span data-ttu-id="7f862-126">Immagine di Windows XP preparata</span><span class="sxs-lookup"><span data-stu-id="7f862-126">A prepared Windows XP image</span></span>**

    <span data-ttu-id="7f862-127">Per altre informazioni su come creare un'immagine di Windows XP da usare con MED-V, vedere [preparare un'immagine MED-v](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="7f862-127">For more information about how to create a Windows XP image for use with MED-V, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

-   **<span data-ttu-id="7f862-128">Un file di testo o un elenco che contiene informazioni sul reindirizzamento degli URL</span><span class="sxs-lookup"><span data-stu-id="7f862-128">A text file or list that contains URL redirection information</span></span>**

    <span data-ttu-id="7f862-129">Il file di testo o l'elenco di reindirizzamento degli URL contiene gli URL che vuoi reindirizzare dal computer host a Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-129">Your URL redirection text file or list contains those URLs that you want redirected from the host computer to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="7f862-130">Quando si usa la creazione guidata pacchetti per creare l'area di lavoro MED-V, è possibile importare, digitare o copiare e incollare queste informazioni di reindirizzamento come uno dei passaggi del processo di creazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7f862-130">When you are using the packaging wizard to create your MED-V workspace, you import, type, or copy and paste this redirection information as one of the steps in the package creation process.</span></span>

    **<span data-ttu-id="7f862-131">Nota</span><span class="sxs-lookup"><span data-stu-id="7f862-131">Note</span></span>**  
    <span data-ttu-id="7f862-132">Il reindirizzamento degli URL in MED-V supporta solo i protocolli HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7f862-132">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="7f862-133">MED-V non offre il supporto per FTP o altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="7f862-133">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## <span data-ttu-id="7f862-134">Creazione di un'area di lavoro MED-V per una lingua diversa da quella del computer Packager dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-134">Packaging a MED-V Workspace for a Language Other than the Language of the MED-V Workspace Packager Computer</span></span>


<span data-ttu-id="7f862-135">Per impostazione predefinita, l'area di lavoro MED-V supporta i caratteri sia nella lingua del computer che in inglese.</span><span class="sxs-lookup"><span data-stu-id="7f862-135">By default, the MED-V workspace supports characters in both the language of the computer and in English.</span></span> <span data-ttu-id="7f862-136">Per creare un'area di lavoro MED-V per una lingua diversa da quella installata nel computer, specificare **-loc \ [locale \]** nello script di PowerShell (. ps1) dopo il nome dell'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="7f862-136">To create a MED-V workspace for a language other than the one installed on the computer, specify **-loc \[locale\]** in the PowerShell script (.ps1) after the MED-V workspace name.</span></span>

<span data-ttu-id="7f862-137">Per creare un pacchetto di area di lavoro MED-V in una lingua diversa da quella predefinita del computer Packager area di lavoro MED-V, genera uno script nella lingua predefinita eseguendo il Packager area di lavoro MED-V e quindi modificando lo script di output come richiesto per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="7f862-137">To create a MED-V workspace package in a language other than the default language of the MED-V Workspace Packager computer, generate a script in the default language by running the MED-V Workspace Packager and then modifying the output script as required for your locale.</span></span> <span data-ttu-id="7f862-138">Lo script si trova nella directory di output dell'area di lavoro MED-V specificata durante l'imballaggio.</span><span class="sxs-lookup"><span data-stu-id="7f862-138">The script is located in the MED-V workspace output directory that was specified during packaging.</span></span> <span data-ttu-id="7f862-139">I nomi delle impostazioni locali si trovano in. File di WXL nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="7f862-139">The names of the locale settings are on the .WXL files in the following directory:</span></span>

<span data-ttu-id="7f862-140">C:\\Programmi \\Programmi\\microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span><span class="sxs-lookup"><span data-stu-id="7f862-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span></span>

## <span data-ttu-id="7f862-141">Creazione di un pacchetto di area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-141">Creating a MED-V Workspace Package</span></span>


<span data-ttu-id="7f862-142">Per creare un pacchetto di area di lavoro MED-V, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f862-142">To create a MED-V workspace package, follow these steps:</span></span>

****

1.  <span data-ttu-id="7f862-143">Per aprire **Packager area di lavoro MED-v**, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="7f862-143">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="7f862-144">Nel pannello principale di Packager **area di lavoro MED-v** fare clic su **Crea un pacchetto area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="7f862-144">On the **MED-V Workspace Packager** main panel, click **Create a MED-V Workspace Package**.</span></span>

    <span data-ttu-id="7f862-145">Viene visualizzata la **creazione guidata pacchetto area di lavoro MED-v create Med-v** .</span><span class="sxs-lookup"><span data-stu-id="7f862-145">The MED-V **Create MED-V Workspace Package Wizard** appears.</span></span> <span data-ttu-id="7f862-146">La procedura guidata è composta dalle pagine seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f862-146">The wizard consists of the following pages:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7f862-147">Informazioni sul pacchetto</span><span class="sxs-lookup"><span data-stu-id="7f862-147">Package Information</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-148">Specificare un nome per l'area di lavoro MED-V e selezionare una cartella in cui vengono salvati i file del pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-148">Specify a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7f862-149">Selezionare l'immagine di Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f862-149">Select Windows XP Image</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-150">Specifica l'immagine del PC virtuale di Windows XP preparata.</span><span class="sxs-lookup"><span data-stu-id="7f862-150">Specify your prepared Windows XP Virtual PC image.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7f862-151">Configurazione per la prima volta</span><span class="sxs-lookup"><span data-stu-id="7f862-151">First Time Setup</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-152">Specificare il processo di configurazione che MED-V segue durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7f862-152">Specify the setup process that MED-V follows during first time setup.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7f862-153">Messaggi di MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-153">MED-V Messages</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-154">Specificare i messaggi e l'URL facoltativo per le informazioni della guida che l'utente finale Visualizza durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7f862-154">Specify the messages and optional URL for Help information that the end user sees during first time setup.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7f862-155">Denominazione dei computer</span><span class="sxs-lookup"><span data-stu-id="7f862-155">Naming Computers</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-156">Specificare la modalità di denominazione della macchina virtuale MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-156">Specify how the MED-V virtual machine is named.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7f862-157">Copiare le impostazioni dall'host</span><span class="sxs-lookup"><span data-stu-id="7f862-157">Copy Settings from Host</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-158">Specificare la modalità di definizione delle impostazioni per l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-158">Specify how the settings for the MED-V workspace are defined.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7f862-159">Avvio e networking</span><span class="sxs-lookup"><span data-stu-id="7f862-159">Startup and Networking</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-160">Specificare le impostazioni per l'avvio dell'area di lavoro MED-V, della rete e delle credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="7f862-160">Specify the settings for starting the MED-V workspace, networking, and user credentials.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="7f862-161">Reindirizzamento Web</span><span class="sxs-lookup"><span data-stu-id="7f862-161">Web Redirection</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-162">Specificare un file di testo o un elenco degli URL che si vuole reindirizzare a Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-162">Specify a text file or a list of the URLs you want redirected to Internet Explorer in the MED-V workspace.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="7f862-163">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="7f862-163">Summary</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="7f862-164">Verificare le impostazioni dell'area di lavoro MED-V e iniziare a creare il pacchetto di distribuzione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-164">Verify your MED-V workspace settings and start to build your MED-V workspace deployment package.</span></span></p></td>
    </tr>
    </tbody>
    </table>



3.  <span data-ttu-id="7f862-165">Nella pagina **informazioni pacchetto** immettere un nome per l'area di lavoro MED-v e selezionare una cartella in cui vengono salvati i file del pacchetto dell'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="7f862-165">On the **Package Information** page, enter a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span>

    **<span data-ttu-id="7f862-166">Warning</span><span class="sxs-lookup"><span data-stu-id="7f862-166">Warning</span></span>**  
    <span data-ttu-id="7f862-167">È necessario assegnare un nome all'area di lavoro MED-V e specificare una cartella per continuare.</span><span class="sxs-lookup"><span data-stu-id="7f862-167">You must name the MED-V workspace and specify a folder to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

4. <span data-ttu-id="7f862-168">Nella pagina **selezionare l'immagine di Windows XP** specificare la posizione dell'immagine PC virtuale di Windows XP preparata (file con estensione VHD).</span><span class="sxs-lookup"><span data-stu-id="7f862-168">On the **Select Windows XP Image** page, specify the location of your prepared MED-V Windows XP Virtual PC image (.vhd file).</span></span>

   **<span data-ttu-id="7f862-169">Warning</span><span class="sxs-lookup"><span data-stu-id="7f862-169">Warning</span></span>**  
   <span data-ttu-id="7f862-170">Per continuare, devi specificare un'immagine VHD di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7f862-170">You must specify a Windows XP VHD image to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

5. <span data-ttu-id="7f862-171">Nella pagina **configurazione per la prima volta** , selezionare se si vuole che venga eseguita la configurazione prima volta durante la fase di partecipazione o automatica e se si vuole che l'area di lavoro MED-V venga usata separatamente o usata da tutti gli utenti finali in un computer condiviso.</span><span class="sxs-lookup"><span data-stu-id="7f862-171">On the **First Time Setup** page, select whether you want first time setup to run while attended or unattended and whether you want the MED-V workspace used separately or used by all end users on a shared computer.</span></span>

   <span data-ttu-id="7f862-172">Se si seleziona **configurazione automatica, senza alcuna notifica**, l'utente finale non viene informato prima dell'esecuzione della configurazione iniziale e la macchina virtuale non viene visualizzata all'utente finale durante la configurazione del primo tempo.</span><span class="sxs-lookup"><span data-stu-id="7f862-172">If you select **Unattended setup, without any notification**, the end user is not informed before first time setup is run and the virtual machine is not shown to the end user during first time setup.</span></span> <span data-ttu-id="7f862-173">Inoltre, la pagina **messaggi MED-V** della procedura guidata è nascosta perché non è necessario alcun messaggio se la configurazione iniziale viene eseguita in modalità completamente automatica.</span><span class="sxs-lookup"><span data-stu-id="7f862-173">In addition, the **MED-V Messages** page of the wizard is hidden because no messages are required if first time setup runs in a completely unattended mode.</span></span>

   <span data-ttu-id="7f862-174">Se selezioni la **configurazione automatica, ma avvisa gli utenti finali prima che inizi la configurazione iniziale**, l'utente finale viene informato prima che venga eseguita la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7f862-174">If you select **Unattended setup, but notify end users before first time setup begins**, the end user is informed before first time setup is run.</span></span> <span data-ttu-id="7f862-175">Tuttavia, la macchina virtuale non viene visualizzata all'utente finale durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7f862-175">However, the virtual machine is not shown to the end user during first time setup.</span></span>

   <span data-ttu-id="7f862-176">Selezionare **configurazione assistita** se l'utente finale deve immettere le informazioni durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7f862-176">Select **Attended setup** if the end user must enter information during first time setup.</span></span>

   <span data-ttu-id="7f862-177">Il comportamento predefinito è la **configurazione automatica, ma avvisa gli utenti finali prima**dell'inizio della configurazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="7f862-177">The default behavior is **Unattended setup, but notify end users before first time setup begins**.</span></span>

   **<span data-ttu-id="7f862-178">Attenzione</span><span class="sxs-lookup"><span data-stu-id="7f862-178">Caution</span></span>**  
   <span data-ttu-id="7f862-179">Se è stato creato il file Sysprep. inf in modo che la configurazione minima richiedesse l'input dell'utente per il completamento, è necessario selezionare **configurazione assistita** o potrebbero verificarsi problemi durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7f862-179">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, you must select **Attended setup** or problems might occur during first time setup.</span></span>



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. <span data-ttu-id="7f862-180">Nella pagina **messaggi MED-V** specificare i messaggi seguenti che l'utente finale vedrà durante la configurazione per la prima volta:</span><span class="sxs-lookup"><span data-stu-id="7f862-180">On the **MED-V Messages** page, specify the following messages that the end user sees during first time setup:</span></span>

   -   <span data-ttu-id="7f862-181">Messaggio visualizzato dall'utente finale al momento dell'avvio della configurazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="7f862-181">The message that the end user sees when first time setup starts.</span></span>

   -   <span data-ttu-id="7f862-182">Messaggio che viene visualizzato dall'utente finale se la configurazione per la prima volta non riesce o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="7f862-182">The message that the end user sees if first time setup fails or an error occurs.</span></span>

   **<span data-ttu-id="7f862-183">Nota</span><span class="sxs-lookup"><span data-stu-id="7f862-183">Note</span></span>**  
   <span data-ttu-id="7f862-184">La pagina **messaggi MED-V** della procedura guidata è nascosta se è stata selezionata l'opzione **installazione automatica, senza alcuna notifica** nella **prima** pagina di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7f862-184">The **MED-V Messages** page of the wizard is hidden if you selected **Unattended setup, without any notification** on the **First Time Setup** page.</span></span>



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. <span data-ttu-id="7f862-185">Nella pagina **Naming Computers** è possibile specificare se la denominazione del computer è gestita da MED-V o da uno strumento di gestione del sistema, ad esempio Sysprep.</span><span class="sxs-lookup"><span data-stu-id="7f862-185">On the **Naming Computers** page, you can specify whether computer naming is managed by MED-V or by a system management tool, such as Sysprep.</span></span> <span data-ttu-id="7f862-186">L'impostazione predefinita è che la denominazione dei computer è gestita da uno strumento di gestione del sistema.</span><span class="sxs-lookup"><span data-stu-id="7f862-186">The default is that computer naming is managed by a system management tool.</span></span>

   <span data-ttu-id="7f862-187">Se specifichi che la denominazione del computer è gestita da MED-V, seleziona una convenzione di denominazione del computer (mask) predefinita nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="7f862-187">If you specify that computer naming is managed by MED-V, select a predefined computer naming convention (mask) from the drop-down list.</span></span> <span data-ttu-id="7f862-188">Verrà visualizzata un'anteprima di un nome di computer di esempio basato sul computer in uso per compilare il pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-188">A preview of a sample computer name appears that is based on the computer that you are using to build the MED-V workspace package.</span></span>

   <span data-ttu-id="7f862-189">Se si seleziona una delle convenzioni di denominazione personalizzate, i campi che è possibile specificare sono limitati ai caratteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f862-189">If you select one of the custom naming conventions, the fields you can specify are limited to the following characters:</span></span>

   -   <span data-ttu-id="7f862-190">I campi prefisso e suffisso sono limitati ai caratteri a-Z, a-z, 0-9 e ai caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="7f862-190">The prefix and suffix fields are limited to the characters A-Z, a-z, 0-9, and the special characters !</span></span> <span data-ttu-id="7f862-191">@ \ # $% ^ & ()-\ _' {}.</span><span class="sxs-lookup"><span data-stu-id="7f862-191">@ \# $ % ^ & ( ) - \_ ' { } .</span></span> <span data-ttu-id="7f862-192">e ~.</span><span class="sxs-lookup"><span data-stu-id="7f862-192">and ~.</span></span>

   -   <span data-ttu-id="7f862-193">I campi hostname e username sono limitati alle cifre da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="7f862-193">The hostname and username fields are limited to the digits 0 through 9.</span></span>

   **<span data-ttu-id="7f862-194">Importante</span><span class="sxs-lookup"><span data-stu-id="7f862-194">Important</span></span>**  
   <span data-ttu-id="7f862-195">I nomi dei computer devono essere univoci e limitati a un massimo di 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7f862-195">Computer names must be unique and are limited to a maximum of 15 characters.</span></span> <span data-ttu-id="7f862-196">Quando si decide il metodo di denominazione del computer, considerare gli utenti finali che hanno più computer o che condividono un computer ed evitare di usare maschere di nomi di computer che potrebbero causare una collisione in rete.</span><span class="sxs-lookup"><span data-stu-id="7f862-196">When you decide on your computer naming method, consider end users who have multiple computers or that share a computer, and avoid using computer name masks that could cause a collision on the network.</span></span>



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. <span data-ttu-id="7f862-197">Nella pagina **Copia impostazioni da host** è possibile selezionare le impostazioni seguenti per specificare il modo in cui è configurata l'area di lavoro MED-V:</span><span class="sxs-lookup"><span data-stu-id="7f862-197">On the **Copy Settings from Host** page, you can select the following settings to specify how the MED-V workspace is configured:</span></span>

   **<span data-ttu-id="7f862-198">Attenzione</span><span class="sxs-lookup"><span data-stu-id="7f862-198">Caution</span></span>**  
   <span data-ttu-id="7f862-199">Le impostazioni specificate in questa pagina che vengono copiate dal computer host all'area di lavoro MED-V eseguono l'override di quelle specificate nel file di risposte Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="7f862-199">The settings that you specify on this page that are copied from the host computer to the MED-V workspace override those specified in the Sysprep.inf answer file.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. <span data-ttu-id="7f862-200">Nella pagina **avvio e networking** è possibile modificare il comportamento predefinito per le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f862-200">On the **Startup and Networking** page, you can change the default behavior for the following settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7f862-201">Avviare l'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-201">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7f862-202">Scegliere se avviare l'area di lavoro MED-V all'accesso dell'utente, al primo utilizzo o per consentire all'utente finale di decidere quando viene avviata l'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="7f862-202">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="7f862-203">L'area di lavoro MED-V viene avviata in uno dei due modi seguenti: quando l'utente finale accede o quando avvia un'azione che richiede MED-V, ad esempio l'apertura di un'applicazione pubblicata o l'immissione di un URL che richiede il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="7f862-203">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first start an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="7f862-204">Puoi definire questa impostazione per l'utente finale o lasciare che l'utente finale controlli l'avvio di MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-204">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="7f862-205">Nota</span><span class="sxs-lookup"><span data-stu-id="7f862-205">Note</span></span></strong><br/><p><span data-ttu-id="7f862-206">Se specifichi che l'utente finale decide, il comportamento predefinito che provano è che l'area di lavoro MED-V viene avviata quando si collegano.</span><span class="sxs-lookup"><span data-stu-id="7f862-206">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="7f862-207">Possono modificare l'impostazione predefinita facendo clic con il pulsante destro del mouse sull'icona MED-V nell'area di notifica e selezionando <strong> impostazioni utente Med-v </strong> .</span><span class="sxs-lookup"><span data-stu-id="7f862-207">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="7f862-208">Se si definisce questa impostazione per l'utente finale, non è possibile modificare la modalità di avvio di MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-208">If you define this setting for the end user, they cannot change how MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7f862-209">Reti</span><span class="sxs-lookup"><span data-stu-id="7f862-209">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7f862-210">Selezionare <strong> condivisi </strong> o <strong> Bridged </strong> per l'impostazione di rete.</span><span class="sxs-lookup"><span data-stu-id="7f862-210">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="7f862-211">Il valore predefinito è <strong> Shared </strong> .</span><span class="sxs-lookup"><span data-stu-id="7f862-211">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="7f862-212">Condivisa </strong> - l'area di lavoro MED-V USA NAT (Network Address Translation) per condividere l'host&#39;s IP per il traffico in uscita.</span><span class="sxs-lookup"><span data-stu-id="7f862-212">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="7f862-213">Bridged </strong> - l'area di lavoro MED-V ha un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</span><span class="sxs-lookup"><span data-stu-id="7f862-213">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="7f862-214">Credenziali dello Store</span><span class="sxs-lookup"><span data-stu-id="7f862-214">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="7f862-215">Scegliere se si desidera archiviare le credenziali dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="7f862-215">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="7f862-216">Il comportamento predefinito è che l'archiviazione delle credenziali è disabilitata in modo che l'utente finale debba essere autenticato ogni volta che accede.</span><span class="sxs-lookup"><span data-stu-id="7f862-216">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="7f862-217">Importante</span><span class="sxs-lookup"><span data-stu-id="7f862-217">Important</span></span></strong><br/><p><span data-ttu-id="7f862-218">Anche se la memorizzazione nella cache delle credenziali dell'utente finale offre la migliore esperienza utente, dovresti essere consapevole dei rischi.</span><span class="sxs-lookup"><span data-stu-id="7f862-218">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="7f862-219">Le credenziali di dominio dell'utente finale sono archiviate in un formato reversibile in Gestione credenziali di Windows.</span><span class="sxs-lookup"><span data-stu-id="7f862-219">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="7f862-220">Di conseguenza, un utente malintenzionato potrebbe scrivere un programma che recupera la password e potrebbe avere accesso alle credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7f862-220">As a result, an attacker could write a program that retrieves the password and could gain access to the user’s credentials.</span></span> <span data-ttu-id="7f862-221">È possibile ridurre questo rischio solo disabilitando l'archiviazione delle credenziali degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7f862-221">You can only lessen this risk by disabling the storing of end-user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. <span data-ttu-id="7f862-222">Nella pagina di Reindirizzamento **Web** è possibile immettere, incollare o importare un elenco degli URL reindirizzati a Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-222">On the **Web Redirection** page, you can enter, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="7f862-223">Per altre informazioni su come configurare le informazioni di reindirizzamento degli URL, vedere [prerequisiti](#bkmk-prereq).</span><span class="sxs-lookup"><span data-stu-id="7f862-223">For more information about how to configure your URL redirection information, see [Prerequisites](#bkmk-prereq).</span></span>

   <span data-ttu-id="7f862-224">È anche possibile specificare la modalità di configurazione di Internet Explorer nell'area di lavoro MED-V per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7f862-224">You can also specify how Internet Explorer in the MED-V workspace is configured for end users.</span></span> <span data-ttu-id="7f862-225">Per impostazione predefinita, il livello di sicurezza dell'area Internet è impostato su elevato.</span><span class="sxs-lookup"><span data-stu-id="7f862-225">By default, the Internet zone security level is set to High.</span></span> <span data-ttu-id="7f862-226">Vengono inoltre rimosse alcune funzionalità di esplorazione predefinite, ad esempio la barra degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7f862-226">Also, certain default browsing capabilities, such as the address bar, are removed.</span></span> <span data-ttu-id="7f862-227">Questa configurazione predefinita di Internet Explorer nell'area di lavoro MED-V offre un ambiente di esplorazione più sicuro per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7f862-227">This default configuration of Internet Explorer in the MED-V workspace provides a more secure browsing environment for end users.</span></span>

   **<span data-ttu-id="7f862-228">Attenzione</span><span class="sxs-lookup"><span data-stu-id="7f862-228">Caution</span></span>**  
   <span data-ttu-id="7f862-229">Modificando le impostazioni predefinite, è possibile personalizzare Internet Explorer nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-229">By changing the default settings, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="7f862-230">Tuttavia, renditi conto che se modifichi le impostazioni predefinite per renderle meno sicure, puoi esporre l'organizzazione a questi rischi per la sicurezza presenti nelle versioni precedenti di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f862-230">However, realize that if you change the default settings so as to make them less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span> <span data-ttu-id="7f862-231">Per altre informazioni, vedere [procedure consigliate per la sicurezza per le operazioni MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7f862-231">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>



~~~
After you have finished, click **Next**.
~~~

11. <span data-ttu-id="7f862-232">Nella pagina di **Riepilogo** è possibile esaminare le impostazioni di creazione di pacchetti per l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7f862-232">On the **Summary** page, you can review the packaging settings for this MED-V workspace.</span></span> <span data-ttu-id="7f862-233">Se si vogliono modificare le impostazioni, fare clic sul pulsante **precedente** per tornare alla pagina pertinente.</span><span class="sxs-lookup"><span data-stu-id="7f862-233">If you want to change any settings, click the **Previous** button to return to the relevant page.</span></span> <span data-ttu-id="7f862-234">Dopo aver completato la revisione delle impostazioni, fare clic su **Crea**.</span><span class="sxs-lookup"><span data-stu-id="7f862-234">After you have finished reviewing the settings, click **Create**.</span></span>

   <span data-ttu-id="7f862-235">Verrà visualizzata la pagina **completamento** della **procedura guidata Crea pacchetto area di lavoro MED-V** per mostrare lo stato di avanzamento della creazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7f862-235">The **Completion** page of the **Create MED-V Workspace Package Wizard** opens to show the progress of the package creation.</span></span>

   **<span data-ttu-id="7f862-236">Nota</span><span class="sxs-lookup"><span data-stu-id="7f862-236">Note</span></span>**  
   <span data-ttu-id="7f862-237">Il processo di creazione del pacchetto dell'area di lavoro MED-V potrebbe richiedere diversi minuti per il completamento, a seconda delle dimensioni del VHD specificato.</span><span class="sxs-lookup"><span data-stu-id="7f862-237">The MED-V workspace package creation process might take several minutes to complete, depending on the size of the VHD specified.</span></span>



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. <span data-ttu-id="7f862-238">Fare clic su **Chiudi** per chiudere la creazione guidata pacchetti e tornare al **Packager area di lavoro MED-V**.</span><span class="sxs-lookup"><span data-stu-id="7f862-238">Click **Close** to close the packaging wizard and return to the **MED-V Workspace Packager**.</span></span>

<span data-ttu-id="7f862-239">Il pacchetto dell'area di lavoro MED-V è ora pronto per il test prima della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7f862-239">Your MED-V workspace package is now ready for testing before deployment.</span></span>

## <span data-ttu-id="7f862-240">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f862-240">Related topics</span></span>


[<span data-ttu-id="7f862-241">Configurazione delle impostazioni avanzate con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7f862-241">Configuring Advanced Settings by Using Windows PowerShell</span></span>](configuring-advanced-settings-by-using-windows-powershell.md)

[<span data-ttu-id="7f862-242">Test del pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-242">Testing the MED-V Workspace Package</span></span>](testing-the-med-v-workspace-package.md)

[<span data-ttu-id="7f862-243">Creare un'immagine MED-V</span><span class="sxs-lookup"><span data-stu-id="7f862-243">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









