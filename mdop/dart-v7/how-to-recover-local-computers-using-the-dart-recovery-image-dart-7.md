---
title: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
description: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823765"
---
# <span data-ttu-id="450e5-103">Come ripristinare i computer locali usando l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="450e5-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="450e5-104">Per recuperare un computer locale usando Microsoft Diagnostics and Recovery Toolset (DaRT) 7, è necessario essere fisicamente presenti nel computer dell'utente finale che sta riscontrando problemi che richiedono dardo.</span><span class="sxs-lookup"><span data-stu-id="450e5-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="450e5-105">È anche possibile eseguire le freccette in remoto seguendo le istruzioni su [come recuperare i computer remoti usando l'immagine di ripristino DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="450e5-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="450e5-106">Per recuperare un computer locale usando dardo</span><span class="sxs-lookup"><span data-stu-id="450e5-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="450e5-107">Man mano che il computer si avvia nell'immagine di ripristino DaRT, viene visualizzata la finestra di dialogo **netstart** .</span><span class="sxs-lookup"><span data-stu-id="450e5-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="450e5-108">Viene chiesto se si desidera inizializzare i servizi di rete.</span><span class="sxs-lookup"><span data-stu-id="450e5-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="450e5-109">Se si fa clic su **Sì**, si presuppone che in rete sia presente un server DHCP e si tenti di ottenere un indirizzo IP dal server.</span><span class="sxs-lookup"><span data-stu-id="450e5-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="450e5-110">Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="450e5-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="450e5-111">Per ignorare il processo di inizializzazione della rete, fare clic su **No**.</span><span class="sxs-lookup"><span data-stu-id="450e5-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="450e5-112">Dopo la finestra di dialogo di inizializzazione della rete, viene chiesto se si vuole rimappare le lettere dell'unità.</span><span class="sxs-lookup"><span data-stu-id="450e5-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="450e5-113">Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione.</span><span class="sxs-lookup"><span data-stu-id="450e5-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="450e5-114">Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online.</span><span class="sxs-lookup"><span data-stu-id="450e5-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="450e5-115">Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="450e5-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="450e5-116">Dopo la finestra di dialogo rimappatura viene visualizzata la finestra di dialogo **Opzioni di ripristino del sistema** e viene chiesto di selezionare un layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="450e5-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="450e5-117">Visualizza quindi la directory radice di sistema, il tipo di sistema operativo installato e le dimensioni della partizione.</span><span class="sxs-lookup"><span data-stu-id="450e5-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="450e5-118">Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti.</span><span class="sxs-lookup"><span data-stu-id="450e5-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="450e5-119">Verrà richiesto di inserire il supporto di installazione per il dispositivo e di selezionare il driver.</span><span class="sxs-lookup"><span data-stu-id="450e5-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="450e5-120">Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="450e5-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="450e5-121">Nota</span><span class="sxs-lookup"><span data-stu-id="450e5-121">Note</span></span>**  
    <span data-ttu-id="450e5-122">Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 7 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="450e5-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="450e5-123">Nella finestra **Opzioni ripristino sistema** fare clic su **strumenti di diagnostica e ripristino Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="450e5-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="450e5-124">Verrà visualizzata la finestra del **set di strumenti di diagnostica e ripristino** .</span><span class="sxs-lookup"><span data-stu-id="450e5-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="450e5-125">È ora possibile eseguire tutti i singoli strumenti o procedure guidate inclusi quando è stata creata l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="450e5-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="450e5-126">È possibile fare clic su **Guida** nella finestra del **set di strumenti di diagnostica e ripristino** per aprire il file della Guida client che fornisce istruzioni dettagliate e informazioni necessarie per eseguire i singoli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="450e5-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="450e5-127">È anche possibile fare clic sulla **procedura guidata della soluzione** nella finestra del **set di strumenti di diagnostica e ripristino** per scegliere lo strumento migliore per la situazione, in base a una breve intervista fornita dalla procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="450e5-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="450e5-128">Per informazioni generali su qualsiasi strumento DaRT, Vedi [Panoramica degli strumenti in dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="450e5-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="450e5-129">Per eseguire dardo al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="450e5-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="450e5-130">Puoi eseguire freccetta al prompt dei comandi specificando il comando **netstart.exe** e usando uno dei parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="450e5-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="450e5-131">Parametro</span><span class="sxs-lookup"><span data-stu-id="450e5-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="450e5-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="450e5-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="450e5-133">-rete</span><span class="sxs-lookup"><span data-stu-id="450e5-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="450e5-134">Inizializza i servizi di rete.</span><span class="sxs-lookup"><span data-stu-id="450e5-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="450e5-135">-Rimontare</span><span class="sxs-lookup"><span data-stu-id="450e5-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="450e5-136">Rimappa le lettere dell'unità.</span><span class="sxs-lookup"><span data-stu-id="450e5-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="450e5-137">-prompt</span><span class="sxs-lookup"><span data-stu-id="450e5-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="450e5-138">Visualizza i messaggi che chiedono all'utente finale di specificare se inizializzare la rete e rimappare le unità.</span><span class="sxs-lookup"><span data-stu-id="450e5-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="450e5-139">Importante</span><span class="sxs-lookup"><span data-stu-id="450e5-139">Important</span></span></strong><br/><p><span data-ttu-id="450e5-140">La risposta dell'utente finale alle richieste esegue l'override degli switch-Network e-remount.</span><span class="sxs-lookup"><span data-stu-id="450e5-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="450e5-141">Puoi personalizzare il dardo in modo che un computer che si avvia in dardo apra automaticamente lo strumento di **connessione remota** usato per stabilire una connessione remota con l'help desk.</span><span class="sxs-lookup"><span data-stu-id="450e5-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="450e5-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="450e5-142">Related topics</span></span>


[<span data-ttu-id="450e5-143">Ripristino dei computer con DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="450e5-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









