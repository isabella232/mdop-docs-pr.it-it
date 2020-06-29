---
title: Come installare il client MED-V e MED-V Management Console
description: Come installare il client MED-V e MED-V Management Console
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826985"
---
# <span data-ttu-id="125a6-103">Come installare il client MED-V e MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="125a6-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="125a6-104">I componenti MED-V seguenti sono inclusi nel pacchetto client. msi:</span><span class="sxs-lookup"><span data-stu-id="125a6-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="125a6-105">Client MED-V: il software MED-V che deve essere installato nei computer client per l'uso delle aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="125a6-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="125a6-106">MED-V Management Console: lo strumento di amministrazione che gli amministratori possono usare per creare e gestire le immagini, le aree di lavoro MED-V e i criteri.</span><span class="sxs-lookup"><span data-stu-id="125a6-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="125a6-107">La console di gestione MED-V e il client MED-V sono entrambi installati dal pacchetto client. msi di MED-V.</span><span class="sxs-lookup"><span data-stu-id="125a6-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="125a6-108">Il client MED-V, tuttavia, può essere installato in modo indipendente senza la console di gestione MED-V deselezionando la casella di controllo **installa l'applicazione di gestione MED-** v durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="125a6-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="125a6-109">Nota</span><span class="sxs-lookup"><span data-stu-id="125a6-109">Note</span></span>**  
<span data-ttu-id="125a6-110">Il client MED-V e la console di gestione MED-V possono essere installati solo nei computer basati su Windows 7, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="125a6-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="125a6-111">Non è possibile installare i prodotti server.</span><span class="sxs-lookup"><span data-stu-id="125a6-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="125a6-112">Nota</span><span class="sxs-lookup"><span data-stu-id="125a6-112">Note</span></span>**  
<span data-ttu-id="125a6-113">Non installare il client MED-V usando il comando Windows **RunAs** .</span><span class="sxs-lookup"><span data-stu-id="125a6-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="125a6-114">Per installare il client MED-V</span><span class="sxs-lookup"><span data-stu-id="125a6-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="125a6-115">Accedere come utente con i diritti di amministratore locale nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="125a6-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="125a6-116">Eseguire il pacchetto MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="125a6-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="125a6-117">Il pacchetto MED-V. msi si chiama *MED-V\_x.msi*, dove *x* corrisponde al numero di versione.</span><span class="sxs-lookup"><span data-stu-id="125a6-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="125a6-118">Ad esempio, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="125a6-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="125a6-119">Quando viene visualizzata la schermata **iniziale della procedura guidata InstallShield** , fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="125a6-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="125a6-120">Nella schermata **contratto di licenza** leggere il contratto di licenza, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="125a6-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="125a6-121">Verrà visualizzata la schermata **cartella di destinazione** con la cartella di installazione predefinita visualizzata.</span><span class="sxs-lookup"><span data-stu-id="125a6-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="125a6-122">La cartella di installazione predefinita è la directory in cui è installato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="125a6-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="125a6-123">Per modificare la cartella in cui deve essere installato MED-V, fare clic su **Cambia**e selezionare una cartella esistente.</span><span class="sxs-lookup"><span data-stu-id="125a6-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="125a6-124">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="125a6-124">Click **Next**.</span></span>

6.  <span data-ttu-id="125a6-125">Nella schermata **Impostazioni Med-v** configurare l'installazione di Med-v come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="125a6-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="125a6-126">Selezionare la casella di controllo **installa l'applicazione di gestione MED-V** per includere il componente di gestione nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="125a6-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="125a6-127">Nota</span><span class="sxs-lookup"><span data-stu-id="125a6-127">Note</span></span>**  
        <span data-ttu-id="125a6-128">Gli amministratori di virtualizzazione desktop aziendale devono installare l'applicazione di gestione MED-V.</span><span class="sxs-lookup"><span data-stu-id="125a6-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="125a6-129">Questa applicazione è necessaria per la configurazione di immagini desktop e aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="125a6-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="125a6-130">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="125a6-130">Click **Next**.</span></span>

8. <span data-ttu-id="125a6-131">Nella schermata **pronto per l'installazione** fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="125a6-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="125a6-132">Viene avviata l'installazione del client MED-V.</span><span class="sxs-lookup"><span data-stu-id="125a6-132">The MED-V client installation starts.</span></span> <span data-ttu-id="125a6-133">Questo può richiedere diversi minuti e la schermata potrebbe non visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="125a6-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="125a6-134">Durante l'installazione vengono visualizzate diverse schermate di stato.</span><span class="sxs-lookup"><span data-stu-id="125a6-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="125a6-135">Se viene visualizzato un messaggio, seguire le istruzioni fornite.</span><span class="sxs-lookup"><span data-stu-id="125a6-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="125a6-136">Una volta completata l'installazione, viene visualizzata la schermata **completamento configurazione guidata InstallShield** .</span><span class="sxs-lookup"><span data-stu-id="125a6-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="125a6-137">Fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="125a6-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="125a6-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="125a6-138">Related topics</span></span>


[<span data-ttu-id="125a6-139">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="125a6-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="125a6-140">Elenchi di controllo per l'installazione e l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="125a6-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









