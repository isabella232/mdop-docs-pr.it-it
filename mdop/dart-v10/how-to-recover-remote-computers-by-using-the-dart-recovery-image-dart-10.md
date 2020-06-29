---
title: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
description: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: c0062208-39cd-4e01-adf8-36a11386e2ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 42d49c6c5c494da866785764e1c93a6bda2d667e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822595"
---
# <span data-ttu-id="1e013-103">Come ripristinare i computer remoti con l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="1e013-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="1e013-104">Usare la caratteristica connessione remota in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 per eseguire gli strumenti DaRT in remoto in un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1e013-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="1e013-105">Dopo che l'utente finale fornisce all'amministratore o all'addetto al supporto tecnico informazioni specifiche, l'amministratore IT o il lavoratore dell'help desk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.</span><span class="sxs-lookup"><span data-stu-id="1e013-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="1e013-106">Se gli strumenti DaRT sono stati disabilitati quando è stata creata l'immagine di ripristino, è comunque possibile accedere a tutti gli strumenti.</span><span class="sxs-lookup"><span data-stu-id="1e013-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="1e013-107">Tutti gli strumenti, ad eccezione della connessione remota, non sono disponibili per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="1e013-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="1e013-108">Per recuperare un computer remoto usando l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="1e013-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="1e013-109">Avviare un computer dell'utente finale usando l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="1e013-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="1e013-110">Si utilizzerà in genere uno dei metodi seguenti per avviare il dardo per recuperare un computer remoto, a seconda di come si distribuisce l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="1e013-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="1e013-111">Per altre informazioni sulla distribuzione dell'immagine di ripristino delle freccette, vedere [distribuzione di Dart 10](deploying-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="1e013-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 10](deploying-dart-10.md).</span></span>

    -   <span data-ttu-id="1e013-112">Avviare il dardo da una partizione di ripristino nel computer del problema.</span><span class="sxs-lookup"><span data-stu-id="1e013-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="1e013-113">Avviare il dardo da una partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="1e013-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="1e013-114">Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di Dart 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="1e013-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

    <span data-ttu-id="1e013-115">Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1e013-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="1e013-116">Nota</span><span class="sxs-lookup"><span data-stu-id="1e013-116">Note</span></span>**  
    <span data-ttu-id="1e013-117">La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="1e013-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="1e013-118">Quando viene chiesto se si vuole inizializzare i servizi di rete, selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e013-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="1e013-119">**Sì** -si presuppone che sia presente un server DHCP nella rete e si tenti di ottenere un indirizzo IP dal server.</span><span class="sxs-lookup"><span data-stu-id="1e013-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="1e013-120">Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="1e013-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="1e013-121">**No** -ignorare il processo di inizializzazione della rete.</span><span class="sxs-lookup"><span data-stu-id="1e013-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="1e013-122">Indicare se si vuole riassociare le lettere dell'unità.</span><span class="sxs-lookup"><span data-stu-id="1e013-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="1e013-123">Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione.</span><span class="sxs-lookup"><span data-stu-id="1e013-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="1e013-124">Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online.</span><span class="sxs-lookup"><span data-stu-id="1e013-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="1e013-125">Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="1e013-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="1e013-126">Nella finestra di dialogo **Opzioni ripristino** configurazione di sistema selezionare un layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="1e013-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="1e013-127">Controllare la directory radice di sistema visualizzata, il tipo di sistema operativo installato e le dimensioni della partizione.</span><span class="sxs-lookup"><span data-stu-id="1e013-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="1e013-128">Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti e quindi inserire il supporto di installazione per il dispositivo e selezionare il driver.</span><span class="sxs-lookup"><span data-stu-id="1e013-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="1e013-129">Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="1e013-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="1e013-130">Nota</span><span class="sxs-lookup"><span data-stu-id="1e013-130">Note</span></span>**  
   <span data-ttu-id="1e013-131">Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 10 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e013-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="1e013-132">Per informazioni su come risolvere il problema, vedere [risoluzione dei problemi relativi a Dart 10](troubleshooting-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="1e013-132">For information about how to resolve this issue, see [Troubleshooting DaRT 10](troubleshooting-dart-10.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="1e013-133">Nella finestra **Opzioni ripristino sistema** fare clic su **strumenti di diagnostica e ripristino di Microsoft** per aprire il **set di strumenti di diagnostica e ripristino**.</span><span class="sxs-lookup"><span data-stu-id="1e013-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="1e013-134">Nella finestra del **set di strumenti di diagnostica e ripristino** fare clic su **connessione remota** per aprire la finestra di **connessione remota Dart** .</span><span class="sxs-lookup"><span data-stu-id="1e013-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="1e013-135">Se viene richiesto di fornire l'accesso remoto all'help desk, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e013-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="1e013-136">Viene visualizzata la finestra di connessione remota dardo e viene visualizzato un numero di biglietto, un indirizzo IP e le informazioni sulla porta.</span><span class="sxs-lookup"><span data-stu-id="1e013-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="1e013-137">Nel computer dell'help desk aprire il **Visualizzatore di connessione remota Dart**.</span><span class="sxs-lookup"><span data-stu-id="1e013-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="1e013-138">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Microsoft DaRT 10**e quindi fare clic su **Visualizzatore connessione remota dardo**.</span><span class="sxs-lookup"><span data-stu-id="1e013-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 10**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="1e013-139">Nella finestra di **connessione remota Dart** immettere il ticket, l'indirizzo IP e le informazioni sulla porta necessari.</span><span class="sxs-lookup"><span data-stu-id="1e013-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="1e013-140">Nota</span><span class="sxs-lookup"><span data-stu-id="1e013-140">Note</span></span>**  
   <span data-ttu-id="1e013-141">Queste informazioni vengono create nel computer dell'utente finale e devono essere fornite dall'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1e013-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="1e013-142">Potrebbe essere possibile scegliere tra più indirizzi IP, a seconda del numero di utenti disponibili nel computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1e013-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="1e013-143">Fai clic su **Connetti**.</span><span class="sxs-lookup"><span data-stu-id="1e013-143">Click **Connect**.</span></span>

<span data-ttu-id="1e013-144">L'amministratore IT assume ora il controllo del computer dell'utente finale e può eseguire gli strumenti DaRT in remoto.</span><span class="sxs-lookup"><span data-stu-id="1e013-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="1e013-145">Nota</span><span class="sxs-lookup"><span data-stu-id="1e013-145">Note</span></span>**  
<span data-ttu-id="1e013-146">Viene fornito un file denominato inv32.xml che contiene le informazioni di connessione remota, ad esempio il numero di porta e l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="1e013-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="1e013-147">Per impostazione predefinita, il file si trova in genere in%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="1e013-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="1e013-148">Per personalizzare il processo di connessione remota</span><span class="sxs-lookup"><span data-stu-id="1e013-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="1e013-149">È possibile personalizzare il processo di connessione remota modificando il file winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="1e013-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="1e013-150">Per altre informazioni su come modificare il file di winpeshl.ini, vedere [Winpeshl.ini file](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="1e013-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="1e013-151">Specificare i comandi e i parametri seguenti per personalizzare il modo in cui viene stabilita una connessione remota con un computer dell'utente finale:</span><span class="sxs-lookup"><span data-stu-id="1e013-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="1e013-152">Comando</span><span class="sxs-lookup"><span data-stu-id="1e013-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="1e013-153">Parametro</span><span class="sxs-lookup"><span data-stu-id="1e013-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="1e013-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e013-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="1e013-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="1e013-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1e013-156">-nomessage</span><span class="sxs-lookup"><span data-stu-id="1e013-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1e013-157">Specifica che la richiesta di conferma non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="1e013-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="1e013-158">La connessione remota </strong> continua proprio come se l'utente finale avesse risposto &quot; Sì &quot; alla richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="1e013-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="1e013-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="1e013-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="1e013-160">nessuno</span><span class="sxs-lookup"><span data-stu-id="1e013-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="1e013-161">Impedisce che uno script personalizzato continui fino a quando <strong> </strong> non è in esecuzione una connessione remota o non viene stabilita una connessione valida con il computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1e013-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="1e013-162">Importante</span><span class="sxs-lookup"><span data-stu-id="1e013-162">Important</span></span></strong><br/><p><span data-ttu-id="1e013-163">Questo comando non serve alcuna funzione se specificato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="1e013-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="1e013-164">Deve essere specificato in uno script per funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="1e013-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="1e013-165">Di seguito è riportato un esempio di file di winpeshl.ini personalizzato per aprire lo strumento di **connessione remota** non appena viene eseguito un tentativo di avvio in dardo:</span><span class="sxs-lookup"><span data-stu-id="1e013-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="1e013-166">Quando si avvia dardo, crea il file inv32.xml in \\Windows\\System32\\ sul disco RAM.</span><span class="sxs-lookup"><span data-stu-id="1e013-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="1e013-167">Questo file contiene informazioni sulla connessione: indirizzo IP, porta e numero di biglietto.</span><span class="sxs-lookup"><span data-stu-id="1e013-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="1e013-168">È possibile copiare il file in una condivisione di rete per attivare un flusso di lavoro Help desk.</span><span class="sxs-lookup"><span data-stu-id="1e013-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="1e013-169">Ad esempio, un programma personalizzato può controllare la condivisione di rete per i file di connessione e quindi creare un ticket di supporto o inviare notifiche tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="1e013-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="1e013-170">Per eseguire il Visualizzatore di connessione remota al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="1e013-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="1e013-171">Per eseguire il **Visualizzatore di connessioni remote di Dart** al prompt dei comandi, specificare il comando **DartRemoteViewer.exe** e usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e013-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="1e013-172">Parametro</span><span class="sxs-lookup"><span data-stu-id="1e013-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="1e013-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e013-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1e013-174">-Ticket = &lt; <em> numero ticket</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="1e013-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1e013-175">Dove &lt; <em> numero ticket </em> &gt; è il numero del biglietto, inclusi i trattini generati da una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="1e013-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1e013-176">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="1e013-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1e013-177">Dove &lt; <em> IPAddress </em> &gt; è l'indirizzo IP generato dalla connessione remota.</span><span class="sxs-lookup"><span data-stu-id="1e013-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1e013-178">-porta = &lt; <em> porta</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="1e013-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1e013-179">Dove &lt; <em> porta </em> &gt; è la porta che corrisponde all'indirizzo IP specificato.</span><span class="sxs-lookup"><span data-stu-id="1e013-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="1e013-180">Se si specificano tutti e tre i parametri e i dati sono validi, viene eseguita immediatamente una connessione all'avvio del programma.</span><span class="sxs-lookup"><span data-stu-id="1e013-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="1e013-181">Se un parametro qualsiasi non è valido, il programma viene avviato come se non fossero stati specificati parametri.</span><span class="sxs-lookup"><span data-stu-id="1e013-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="1e013-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e013-182">Related topics</span></span>


[<span data-ttu-id="1e013-183">Operazioni relative a DaRT 10</span><span class="sxs-lookup"><span data-stu-id="1e013-183">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="1e013-184">Ripristino dei computer con DaRT 10</span><span class="sxs-lookup"><span data-stu-id="1e013-184">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









