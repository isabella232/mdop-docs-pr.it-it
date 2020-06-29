---
title: Come creare un gruppo di connessione
description: Come creare un gruppo di connessione
author: dansimp
ms.assetid: 221e2eed-7ebb-42e3-b3d6-11c37c0578e6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f20b3e71c7c0b72d66700bbad945860112ffd03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805649"
---
# <span data-ttu-id="47e7c-103">Come creare un gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="47e7c-103">How to Create a Connection Group</span></span>


<span data-ttu-id="47e7c-104">Seguire questa procedura per creare un gruppo di connessioni usando la console di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="47e7c-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="47e7c-105">Per usare PowerShell per creare gruppi di connessioni, vedere [come gestire i gruppi di connessioni in un computer autonomo usando PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="47e7c-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md).</span></span>

<span data-ttu-id="47e7c-106">Quando si inseriscono i pacchetti in un gruppo di connessioni, i percorsi radice del pacchetto vengono uniti.</span><span class="sxs-lookup"><span data-stu-id="47e7c-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="47e7c-107">Se si rimuovono i pacchetti, solo i pacchetti rimanenti manterranno la radice unita.</span><span class="sxs-lookup"><span data-stu-id="47e7c-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="47e7c-108">Per creare un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="47e7c-108">To create a connection group</span></span>**

1.  <span data-ttu-id="47e7c-109">Nella console di gestione di App-V 5,1 selezionare **gruppi di connessioni** per visualizzare la raccolta gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="47e7c-109">In the App-V 5.1 Management Console, select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

2.  <span data-ttu-id="47e7c-110">Selezionare **Aggiungi gruppo di connessioni** per creare un nuovo gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="47e7c-110">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

3.  <span data-ttu-id="47e7c-111">Nel riquadro **nuovo gruppo di connessioni** Digitare una descrizione per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="47e7c-111">In the **New Connection Group** pane, type a description for the group.</span></span>

4.  <span data-ttu-id="47e7c-112">Fare clic su **modifica** nel riquadro **pacchetti connessi** per aggiungere una nuova applicazione al gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="47e7c-112">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

5.  <span data-ttu-id="47e7c-113">Nell' **intero riquadro Raccolta pacchetti** selezionare l'applicazione da aggiungere e fare clic sulla freccia per aggiungere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47e7c-113">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="47e7c-114">Per rimuovere un'applicazione, selezionare l'applicazione da rimuovere nel riquadro **pacchetti in** e fare clic sulla freccia.</span><span class="sxs-lookup"><span data-stu-id="47e7c-114">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="47e7c-115">Per riassegnare le priorità alle applicazioni nel gruppo di connessioni, usare le frecce nel riquadro **pacchetti in** .</span><span class="sxs-lookup"><span data-stu-id="47e7c-115">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="47e7c-116">**Importante**  Per impostazione predefinita, le configurazioni di accesso ai servizi di dominio Active Directory associate a un'applicazione specifica non vengono aggiunte al gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="47e7c-116">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="47e7c-117">Per trasferire la configurazione di Access in Active Directory, selezionare **Aggiungi accesso a un pacchetto all'accesso al gruppo**, che si trova nel riquadro **pacchetti in** .</span><span class="sxs-lookup"><span data-stu-id="47e7c-117">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

6.  <span data-ttu-id="47e7c-118">Dopo aver aggiunto tutte le applicazioni e aver configurato l'accesso a Active Directory, fare clic su **applica**.</span><span class="sxs-lookup"><span data-stu-id="47e7c-118">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="47e7c-119">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="47e7c-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="47e7c-120">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="47e7c-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="47e7c-121">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="47e7c-121">Got an App-V issue?</span></span>** <span data-ttu-id="47e7c-122">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="47e7c-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="47e7c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47e7c-123">Related topics</span></span>


[<span data-ttu-id="47e7c-124">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="47e7c-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="47e7c-125">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="47e7c-125">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





