---
title: Come installare il client MED-V
description: Come installare il client MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827195"
---
# <span data-ttu-id="697e4-103">Come installare il client MED-V</span><span class="sxs-lookup"><span data-stu-id="697e4-103">How to Install MED-V Client</span></span>


<span data-ttu-id="697e4-104">In uno scenario basato su un pacchetto di distribuzione, l'installazione del client MED-V è inclusa nel pacchetto di distribuzione e viene installata direttamente dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="697e4-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="697e4-105">Importante</span><span class="sxs-lookup"><span data-stu-id="697e4-105">Important</span></span>**  
<span data-ttu-id="697e4-106">Quando si usa un pacchetto di distribuzione che non include un'immagine, assicurarsi che l'immagine venga caricata sul Web o inserita nella cartella pre-stage prima di installare il pacchetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="697e4-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="697e4-107">Per installare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="697e4-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="697e4-108">Effettua una delle seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="697e4-108">Do one of the following:</span></span>

    -   <span data-ttu-id="697e4-109">Scaricare il pacchetto MED-V dal Web.</span><span class="sxs-lookup"><span data-stu-id="697e4-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="697e4-110">Inserire la distribuzione USB o DVD nell'unità host.</span><span class="sxs-lookup"><span data-stu-id="697e4-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="697e4-111">Se MED-V non viene avviato automaticamente, fare doppio clic su MED-VAutoInstaller.exe.</span><span class="sxs-lookup"><span data-stu-id="697e4-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="697e4-112">Verrà visualizzata una finestra di dialogo in cui sono elencati i componenti già installati e quelli attualmente installati.</span><span class="sxs-lookup"><span data-stu-id="697e4-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="697e4-113">Nota</span><span class="sxs-lookup"><span data-stu-id="697e4-113">Note</span></span>**  
    <span data-ttu-id="697e4-114">Se nel computer host è presente una versione di Microsoft Virtual PC che non è supportata, verrà visualizzato un messaggio che indica di disinstallare la versione esistente ed eseguire di nuovo il programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="697e4-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="697e4-115">Se necessario, riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="697e4-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="697e4-116">Al termine dell'installazione, viene avviato MED-V e viene visualizzato un messaggio che informa che l'installazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="697e4-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="697e4-117">Accedere a MED-V usando il nome utente e la password seguenti:</span><span class="sxs-lookup"><span data-stu-id="697e4-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="697e4-118">Digitare il nome di dominio e il nome utente seguiti dalla password dell'utente di dominio autorizzato a usare MED-V.</span><span class="sxs-lookup"><span data-stu-id="697e4-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="697e4-119">Esempio: "Domain \ _name \\user\ _name", "password"</span><span class="sxs-lookup"><span data-stu-id="697e4-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="697e4-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="697e4-120">Related topics</span></span>


[<span data-ttu-id="697e4-121">Come configurare un pacchetto di distribuzione</span><span class="sxs-lookup"><span data-stu-id="697e4-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="697e4-122">Come caricare un'immagine MED-V nel server</span><span class="sxs-lookup"><span data-stu-id="697e4-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="697e4-123">Riferimento della riga di comando dell'installazione client</span><span class="sxs-lookup"><span data-stu-id="697e4-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)









