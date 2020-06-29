---
title: Come installare il client App-V con Setup.exe
description: Come installare il client App-V con Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817336"
---
# <span data-ttu-id="1e11e-103">Come installare il client App-V con Setup.exe</span><span class="sxs-lookup"><span data-stu-id="1e11e-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="1e11e-104">Questo argomento descrive come installare il client App-V usando il programma setup.exe.</span><span class="sxs-lookup"><span data-stu-id="1e11e-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="1e11e-105">Quando si installa il client App-V usando il programma setup.exe, il installatore determina il software prerequisito necessario e lo installa automaticamente prima di installare il client.</span><span class="sxs-lookup"><span data-stu-id="1e11e-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="1e11e-106">Per installare il client di virtualizzazione dell'applicazione usando Setup.exe</span><span class="sxs-lookup"><span data-stu-id="1e11e-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="1e11e-107">Verificare di avere effettuato l'accesso con un account che disponga dei diritti di amministratore nel computer.</span><span class="sxs-lookup"><span data-stu-id="1e11e-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="1e11e-108">Aprire una finestra del prompt dei comandi e quindi cambiare la directory nella cartella che contiene i file di installazione.</span><span class="sxs-lookup"><span data-stu-id="1e11e-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="1e11e-109">Quando si installa la versione 4.6 o una versione successiva del client App-V, è necessario usare il programma di installazione corretto per il sistema operativo del computer, 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1e11e-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="1e11e-110">L'installazione non riesce e verrà visualizzato un messaggio di errore se si usa il programma di installazione errato.</span><span class="sxs-lookup"><span data-stu-id="1e11e-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="1e11e-111">Immettere la stringa di comando installa al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1e11e-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="1e11e-112">In alternativa, è possibile creare un file di comando ed eseguirlo dal prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1e11e-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="1e11e-113">Puoi anche usare un linguaggio di scripting come VBScript o Windows PowerShell per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="1e11e-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="1e11e-114">Nell'esempio della riga di comando seguente viene illustrato il modo in cui setup.exe può essere usato con una serie di parametri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="1e11e-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="1e11e-115">Per altre informazioni su questi parametri, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e11e-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="1e11e-116">"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" produzione System\\ "SWIPUBSVRTYPE = \ \"/secure\\ HTTP "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""</span><span class="sxs-lookup"><span data-stu-id="1e11e-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="1e11e-117">Importante</span><span class="sxs-lookup"><span data-stu-id="1e11e-117">Important</span></span>**  
    -   <span data-ttu-id="1e11e-118">Le virgolette che compaiono nella sezione "**/v**" devono essere considerate caratteri speciali e immesse con un " **\\** ".</span><span class="sxs-lookup"><span data-stu-id="1e11e-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="1e11e-119">Le virgolette sono obbligatorie solo quando il valore contiene uno spazio; Tuttavia, per coerenza, tutte le istanze nell'esempio precedente vengono visualizzate come virgolette.</span><span class="sxs-lookup"><span data-stu-id="1e11e-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="1e11e-120">I **%** caratteri "" in "**% HOMEDRIVE%**" devono essere preceduti dal carattere di **^** escape "".</span><span class="sxs-lookup"><span data-stu-id="1e11e-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="1e11e-121">In caso contrario, la shell dei comandi di Windows imposta il valore su quello dell'utente che sta eseguendo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1e11e-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="1e11e-122">Gli switch di **InstallShield** **/s** e **/qn** sono necessari per creare un'installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="1e11e-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="1e11e-123">L'opzione **/qn** deve seguire l'opzione **/v** , separata solo da un carattere di virgoletta senza spazi intermedi.</span><span class="sxs-lookup"><span data-stu-id="1e11e-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="1e11e-124">La cartella specificata nel valore **SWIGLOBALDATA** deve esistere già.</span><span class="sxs-lookup"><span data-stu-id="1e11e-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="1e11e-125">Al termine dell'installazione, è consigliabile eseguire un'analisi di Microsoft Update per verificare che siano installati gli aggiornamenti più recenti.</span><span class="sxs-lookup"><span data-stu-id="1e11e-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="1e11e-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e11e-126">Related topics</span></span>


[<span data-ttu-id="1e11e-127">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="1e11e-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





