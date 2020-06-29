---
title: Come avviare, arrestare e riavviare un'area di lavoro MED-V
description: Come avviare, arrestare e riavviare un'area di lavoro MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825725"
---
# <span data-ttu-id="b891c-103">Come avviare, arrestare e riavviare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b891c-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="b891c-104">Per avviare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b891c-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="b891c-105">Nell'area di notifica fare clic con il pulsante destro del mouse sull'icona MED-V.</span><span class="sxs-lookup"><span data-stu-id="b891c-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="b891c-106">Nel sottomenu fare clic su **Avvia area di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="b891c-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="b891c-107">Se nel computer sono in uso più aree di lavoro MED-V, viene visualizzata la finestra di **selezione dell'area di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="b891c-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="b891c-108">Selezionare un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b891c-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="b891c-109">Selezionare la casella di controllo **Avvia l'area di lavoro selezionata senza chiedermi** di ignorare questa finestra al successivo avvio del client e per aprire automaticamente l'area di lavoro MED-V selezionata.</span><span class="sxs-lookup"><span data-stu-id="b891c-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="b891c-110">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b891c-110">Click **OK**.</span></span>

    <span data-ttu-id="b891c-111">Verrà visualizzata la finestra di **autenticazione avvia area di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="b891c-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="b891c-112">Se nel computer sono presenti diverse aree di lavoro MED-V e si è scelto di usare un'area di lavoro MED-V specificata, viene visualizzata la finestra visualizzata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b891c-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="b891c-113">Se nel computer è presente una sola area di lavoro MED-V, l'opzione "Start last used Workspace" non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b891c-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="b891c-114">Digitare le credenziali utente del dominio.</span><span class="sxs-lookup"><span data-stu-id="b891c-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="b891c-115">**Nota**  La prima volta che viene avviata un'area di lavoro MED-V, il nome utente deve avere il formato seguente: &lt; Domain Name &gt; \\ &lt; User Name &gt; .</span><span class="sxs-lookup"><span data-stu-id="b891c-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="b891c-116">Selezionare **Salva la password** per salvare la password tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="b891c-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="b891c-117">**Nota**  Per abilitare la caratteristica Salva password, l'attributo EnableSavePassword deve essere impostato su true nel file ClientSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="b891c-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="b891c-118">Il file si trova nella cartella *Servers\\Configuration Server\\*</span><span class="sxs-lookup"><span data-stu-id="b891c-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="b891c-119">Deselezionare la casella di controllo **Avvia ultima area di lavoro usata** per scegliere un'area di lavoro MED-V diversa.</span><span class="sxs-lookup"><span data-stu-id="b891c-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="b891c-120">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b891c-120">Click **OK**.</span></span>

    <span data-ttu-id="b891c-121">Diverse schermate di stato vengono visualizzate a seconda della configurazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b891c-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="b891c-122">Viene visualizzata la schermata **Avvia area di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="b891c-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="b891c-123">Per riavviare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b891c-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="b891c-124">Quando il client è in funzione, nell'area di notifica fare clic con il pulsante destro del mouse sull'icona MED-V.</span><span class="sxs-lookup"><span data-stu-id="b891c-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="b891c-125">Nel sottomenu fare clic su **Riavvia area di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="b891c-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="b891c-126">L'area di lavoro MED-V viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="b891c-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="b891c-127">In un'area di lavoro MED-V persistente, la macchina virtuale viene arrestata e quindi riavviata.</span><span class="sxs-lookup"><span data-stu-id="b891c-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="b891c-128">In un'area di lavoro di revertible MED-V la macchina virtuale non viene effettivamente chiusa; Restituisce invece lo stato originale.</span><span class="sxs-lookup"><span data-stu-id="b891c-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="b891c-129">Per arrestare un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b891c-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="b891c-130">Nell'area di notifica fare clic con il pulsante destro del mouse sull'icona MED-V.</span><span class="sxs-lookup"><span data-stu-id="b891c-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="b891c-131">Nel sottomenu fare clic su **Interrompi area di lavoro**.</span><span class="sxs-lookup"><span data-stu-id="b891c-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="b891c-132">L'area di lavoro MED-V viene interrotta.</span><span class="sxs-lookup"><span data-stu-id="b891c-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="b891c-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b891c-133">Related topics</span></span>


[<span data-ttu-id="b891c-134">Come avviare e chiudere il client MED-V</span><span class="sxs-lookup"><span data-stu-id="b891c-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 





