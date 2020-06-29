---
title: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
description: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822795"
---
# <span data-ttu-id="e8045-103">Come ripristinare i computer remoti con l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="e8045-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="e8045-104">La funzionalità di connessione remota in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 consente a un amministratore IT di eseguire gli strumenti DaRT in remoto in un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e8045-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="e8045-105">Dopo che alcune informazioni sono state fornite dall'utente finale (o da un helpdesk professionale che lavora nel computer dell'utente finale), l'amministratore IT o l'agente dell'helpdesk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.</span><span class="sxs-lookup"><span data-stu-id="e8045-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="e8045-106">Importante</span><span class="sxs-lookup"><span data-stu-id="e8045-106">Important</span></span>**  
<span data-ttu-id="e8045-107">I due computer che stabiliscono una connessione remota devono far parte della stessa rete.</span><span class="sxs-lookup"><span data-stu-id="e8045-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="e8045-108">Per recuperare un computer remoto tramite dardo</span><span class="sxs-lookup"><span data-stu-id="e8045-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="e8045-109">Avviare un computer dell'utente finale usando l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8045-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="e8045-110">Si utilizzerà in genere uno dei metodi seguenti per avviare il dardo per recuperare un computer remoto, a seconda di come si distribuisce l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="e8045-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="e8045-111">Per altre informazioni sulla distribuzione dell'immagine di ripristino delle freccette, vedere [distribuzione dell'immagine di ripristino di dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="e8045-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="e8045-112">Avviare il dardo da una partizione di ripristino nel computer del problema.</span><span class="sxs-lookup"><span data-stu-id="e8045-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="e8045-113">Avviare il dardo da una partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="e8045-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="e8045-114">Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="e8045-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="e8045-115">Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e8045-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="e8045-116">Nota</span><span class="sxs-lookup"><span data-stu-id="e8045-116">Note</span></span>**  
    <span data-ttu-id="e8045-117">La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8045-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="e8045-118">Man mano che il computer si avvia nell'immagine di ripristino DaRT, viene visualizzata la finestra di dialogo **netstart** .</span><span class="sxs-lookup"><span data-stu-id="e8045-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="e8045-119">Viene chiesto se si desidera inizializzare i servizi di rete.</span><span class="sxs-lookup"><span data-stu-id="e8045-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="e8045-120">Se si fa clic su **Sì**, si presuppone che in rete sia presente un server DHCP e si tenti di ottenere un indirizzo IP dal server.</span><span class="sxs-lookup"><span data-stu-id="e8045-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="e8045-121">Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="e8045-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="e8045-122">Per ignorare il processo di inizializzazione della rete, fare clic su **No**.</span><span class="sxs-lookup"><span data-stu-id="e8045-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="e8045-123">Dopo la finestra di dialogo di inizializzazione della rete, viene chiesto se si vuole rimappare le lettere dell'unità.</span><span class="sxs-lookup"><span data-stu-id="e8045-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="e8045-124">Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione.</span><span class="sxs-lookup"><span data-stu-id="e8045-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="e8045-125">Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online.</span><span class="sxs-lookup"><span data-stu-id="e8045-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="e8045-126">Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="e8045-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="e8045-127">Dopo la finestra di dialogo rimappatura viene visualizzata la finestra di dialogo **Opzioni di ripristino del sistema** e viene chiesto di selezionare un layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="e8045-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="e8045-128">Visualizza quindi la directory radice di sistema, il tipo di sistema operativo installato e le dimensioni della partizione.</span><span class="sxs-lookup"><span data-stu-id="e8045-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="e8045-129">Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti.</span><span class="sxs-lookup"><span data-stu-id="e8045-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="e8045-130">Verrà richiesto di inserire il supporto di installazione per il dispositivo e di selezionare il driver.</span><span class="sxs-lookup"><span data-stu-id="e8045-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="e8045-131">Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e8045-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="e8045-132">Nota</span><span class="sxs-lookup"><span data-stu-id="e8045-132">Note</span></span>**  
    <span data-ttu-id="e8045-133">Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 7 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e8045-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="e8045-134">Per informazioni su questa situazione, ad esempio su come risolverlo, vedere [risoluzione dei problemi relativi a DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="e8045-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="e8045-135">Nella finestra **Opzioni ripristino sistema** selezionare strumenti di **diagnostica e ripristino di Microsoft** per aprire la finestra del **set di strumenti di diagnostica e ripristino** .</span><span class="sxs-lookup"><span data-stu-id="e8045-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="e8045-136">Nella finestra del **set di strumenti di diagnostica e ripristino** fare clic su **connessione remota** per aprire la finestra di **connessione remota Dart** .</span><span class="sxs-lookup"><span data-stu-id="e8045-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="e8045-137">Se viene richiesto di fornire l'accesso remoto all'help desk, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8045-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="e8045-138">Viene visualizzata la finestra di connessione remota dardo e viene visualizzato un numero di biglietto, un indirizzo IP e le informazioni sulla porta.</span><span class="sxs-lookup"><span data-stu-id="e8045-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="e8045-139">Nel computer dell'agente helpdesk aprire il **Visualizzatore connessioni remote di Dart**.</span><span class="sxs-lookup"><span data-stu-id="e8045-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="e8045-140">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Microsoft DaRT 7**e quindi fare clic su **Visualizzatore connessione remota dardo**.</span><span class="sxs-lookup"><span data-stu-id="e8045-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="e8045-141">Nella finestra di **connessione remota Dart** immettere il ticket, l'indirizzo IP e le informazioni sulla porta necessari.</span><span class="sxs-lookup"><span data-stu-id="e8045-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="e8045-142">Nota</span><span class="sxs-lookup"><span data-stu-id="e8045-142">Note</span></span>**  
   <span data-ttu-id="e8045-143">Queste informazioni vengono create nel computer dell'utente finale e devono essere fornite dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e8045-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="e8045-144">Potrebbe essere possibile scegliere tra più indirizzi IP, a seconda del numero di utenti disponibili nel computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e8045-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="e8045-145">Fai clic su **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="e8045-145">Click **Connect**.</span></span>

<span data-ttu-id="e8045-146">L'amministratore IT assume ora il controllo del computer dell'utente finale e può eseguire gli strumenti DaRT in remoto.</span><span class="sxs-lookup"><span data-stu-id="e8045-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="e8045-147">Nota</span><span class="sxs-lookup"><span data-stu-id="e8045-147">Note</span></span>**  
<span data-ttu-id="e8045-148">Viene fornito un file denominato inv32.xml che contiene le informazioni di connessione remota, ad esempio il numero di porta e l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="e8045-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="e8045-149">Per impostazione predefinita, il file si trova in genere in%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="e8045-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="e8045-150">Per personalizzare il processo di connessione remota</span><span class="sxs-lookup"><span data-stu-id="e8045-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="e8045-151">È possibile personalizzare il processo di connessione remota modificando il file winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="e8045-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="e8045-152">Per altre informazioni su come modificare il file di winpeshl.ini, vedere [Winpeshl.ini file](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="e8045-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="e8045-153">Specificare i comandi e i parametri seguenti per personalizzare il modo in cui viene stabilita una connessione remota con un computer dell'utente finale:</span><span class="sxs-lookup"><span data-stu-id="e8045-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="e8045-154">Comando</span><span class="sxs-lookup"><span data-stu-id="e8045-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="e8045-155">Parametro</span><span class="sxs-lookup"><span data-stu-id="e8045-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="e8045-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8045-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e8045-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="e8045-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8045-158">-nomessage</span><span class="sxs-lookup"><span data-stu-id="e8045-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="e8045-159">Specifica che la richiesta di conferma non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="e8045-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="e8045-160">La connessione remota </strong> continua proprio come se l'utente finale avesse risposto &quot; Sì &quot; alla richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="e8045-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e8045-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="e8045-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e8045-162">nessuno</span><span class="sxs-lookup"><span data-stu-id="e8045-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="e8045-163">Impedisce che uno script personalizzato continui fino a quando <strong> </strong> non è in esecuzione una connessione remota o non viene stabilita una connessione valida con il computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="e8045-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="e8045-164">Importante</span><span class="sxs-lookup"><span data-stu-id="e8045-164">Important</span></span></strong><br/><p><span data-ttu-id="e8045-165">Questo comando non serve alcuna funzione se specificato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="e8045-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="e8045-166">Deve essere specificato in uno script per funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="e8045-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="e8045-167">Di seguito è riportato un esempio di file di winpeshl.ini personalizzato per aprire lo strumento di **connessione remota** non appena viene eseguito un tentativo di avvio in dardo:</span><span class="sxs-lookup"><span data-stu-id="e8045-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="e8045-168">Per eseguire il Visualizzatore di connessione remota al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e8045-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="e8045-169">È possibile eseguire il **Visualizzatore di connessioni remote di Dart** al prompt dei comandi specificando il comando **DartRemoteViewer.exe** e usando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="e8045-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="e8045-170">Parametro</span><span class="sxs-lookup"><span data-stu-id="e8045-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="e8045-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8045-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e8045-172">-Ticket = &lt; <em> numero ticket</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="e8045-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8045-173">Dove &lt; <em> numero ticket </em> &gt; è il numero del biglietto, inclusi i trattini generati da una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e8045-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e8045-174">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="e8045-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8045-175">Dove &lt; <em> IPAddress </em> &gt; è l'indirizzo IP generato dalla connessione remota.</span><span class="sxs-lookup"><span data-stu-id="e8045-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e8045-176">-porta = &lt; <em> porta</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="e8045-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8045-177">Dove &lt; <em> porta </em> &gt; è la porta che corrisponde all'indirizzo IP specificato.</span><span class="sxs-lookup"><span data-stu-id="e8045-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="e8045-178">Se si specificano tutti e tre i parametri e i dati sono validi, viene eseguita immediatamente una connessione all'avvio del programma.</span><span class="sxs-lookup"><span data-stu-id="e8045-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="e8045-179">Se un parametro qualsiasi non è valido, il programma viene avviato come se non fossero stati specificati parametri.</span><span class="sxs-lookup"><span data-stu-id="e8045-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="e8045-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8045-180">Related topics</span></span>


[<span data-ttu-id="e8045-181">Ripristino dei computer con DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="e8045-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









