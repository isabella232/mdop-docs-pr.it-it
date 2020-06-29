---
title: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
description: Come ripristinare i computer locali usando l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822586"
---
# <span data-ttu-id="5f1b6-103">Come ripristinare i computer locali usando l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="5f1b6-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="5f1b6-104">Seguire queste istruzioni per recuperare un computer quando si è fisicamente presenti presso il computer dell'utente finale in cui si verificano problemi.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="5f1b6-105">Come recuperare un computer locale usando l'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="5f1b6-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="5f1b6-106">Avviare il computer dell'utente finale usando l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

    <span data-ttu-id="5f1b6-107">Man mano che il computer si avvia nell'immagine di ripristino di DaRT 10, viene visualizzata la finestra di dialogo **netstart** .</span><span class="sxs-lookup"><span data-stu-id="5f1b6-107">As the computer is booting into the DaRT 10 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="5f1b6-108">Quando viene chiesto se si vuole inizializzare i servizi di rete, selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f1b6-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="5f1b6-109">**Sì** -si presuppone che sia presente un server DHCP nella rete e si tenti di ottenere un indirizzo IP dal server.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="5f1b6-110">Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="5f1b6-111">**No** -ignorare il processo di inizializzazione della rete.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="5f1b6-112">Indicare se si vuole riassociare le lettere dell'unità.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="5f1b6-113">Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="5f1b6-114">Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="5f1b6-115">Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="5f1b6-116">Nella finestra di dialogo **Opzioni ripristino** configurazione di sistema selezionare un layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="5f1b6-117">Controllare la directory radice di sistema visualizzata, il tipo di sistema operativo installato e le dimensioni della partizione.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="5f1b6-118">Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti e quindi inserire il supporto di installazione per il dispositivo e selezionare il driver.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="5f1b6-119">Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="5f1b6-120">Nota</span><span class="sxs-lookup"><span data-stu-id="5f1b6-120">Note</span></span>**  
    <span data-ttu-id="5f1b6-121">Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 10 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="5f1b6-122">Nella finestra **Opzioni ripristino sistema** fare clic su **strumenti di diagnostica e ripristino Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="5f1b6-123">Verrà visualizzata la finestra del **set di strumenti di diagnostica e ripristino** .</span><span class="sxs-lookup"><span data-stu-id="5f1b6-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="5f1b6-124">È ora possibile eseguire tutti i singoli strumenti o procedure guidate inclusi quando è stata creata l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="5f1b6-125">È possibile fare clic su **Guida** nella finestra del **set di strumenti di diagnostica e ripristino** per aprire il file della Guida client che fornisce istruzioni dettagliate e informazioni necessarie per eseguire i singoli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="5f1b6-126">È anche possibile fare clic sulla **procedura guidata della soluzione** nella finestra del **set di strumenti di diagnostica e ripristino** per scegliere lo strumento migliore per la situazione, in base a una breve intervista fornita dalla procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="5f1b6-127">Per informazioni generali su qualsiasi strumento DaRT, Vedi [Panoramica degli strumenti in DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="5f1b6-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

**<span data-ttu-id="5f1b6-128">Come eseguire dardo al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="5f1b6-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="5f1b6-129">Per eseguire dardo al prompt dei comandi, specificare il comando **netstart.exe** quindi usare uno dei parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f1b6-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="5f1b6-130">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f1b6-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="5f1b6-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f1b6-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="5f1b6-132">-rete</span><span class="sxs-lookup"><span data-stu-id="5f1b6-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="5f1b6-133">Inizializza i servizi di rete.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="5f1b6-134">-Rimontare</span><span class="sxs-lookup"><span data-stu-id="5f1b6-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="5f1b6-135">Rimappa le lettere dell'unità.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="5f1b6-136">-prompt</span><span class="sxs-lookup"><span data-stu-id="5f1b6-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="5f1b6-137">Visualizza i messaggi che chiedono all'utente finale di specificare se inizializzare la rete e rimappare le unità.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="5f1b6-138">Warning</span><span class="sxs-lookup"><span data-stu-id="5f1b6-138">Warning</span></span></strong><br/><p><span data-ttu-id="5f1b6-139">La risposta dell'utente finale alla richiesta sostituisce gli interruttori-network e-rimontare.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="5f1b6-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f1b6-140">Related topics</span></span>


[<span data-ttu-id="5f1b6-141">Operazioni relative a DaRT 10</span><span class="sxs-lookup"><span data-stu-id="5f1b6-141">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="5f1b6-142">Ripristino dei computer con DaRT 10</span><span class="sxs-lookup"><span data-stu-id="5f1b6-142">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









