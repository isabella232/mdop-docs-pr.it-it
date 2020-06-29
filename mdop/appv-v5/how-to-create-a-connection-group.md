---
title: Come creare un gruppo di connessione
description: Come creare un gruppo di connessione
author: dansimp
ms.assetid: 9d272052-2d28-4e41-989c-89610482a0ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 816fc3b37be056ed54a88c394ef64fa1edaf47ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805655"
---
# <span data-ttu-id="c5a35-103">Come creare un gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="c5a35-103">How to Create a Connection Group</span></span>


<span data-ttu-id="c5a35-104">Seguire questa procedura per creare un gruppo di connessioni usando la console di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="c5a35-104">Use these steps to create a connection group by using the App-V Management Console.</span></span> <span data-ttu-id="c5a35-105">Per usare PowerShell per creare gruppi di connessioni, vedere [come gestire i gruppi di connessioni in un computer autonomo usando PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c5a35-105">To use PowerShell to create connection groups, see [How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md).</span></span>

<span data-ttu-id="c5a35-106">Quando si inseriscono i pacchetti in un gruppo di connessioni, i percorsi radice del pacchetto vengono uniti.</span><span class="sxs-lookup"><span data-stu-id="c5a35-106">When you place packages in a connection group, their package root paths are merged.</span></span> <span data-ttu-id="c5a35-107">Se si rimuovono i pacchetti, solo i pacchetti rimanenti manterranno la radice unita.</span><span class="sxs-lookup"><span data-stu-id="c5a35-107">If you remove packages, only the remaining packages maintain the merged root.</span></span>

**<span data-ttu-id="c5a35-108">Per creare un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="c5a35-108">To create a connection group</span></span>**

1.  <span data-ttu-id="c5a35-109">Nella console di gestione di App-V 5,0 selezionare **pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="c5a35-109">In the App-V 5.0 Management Console, select **Packages**.</span></span>

2.  <span data-ttu-id="c5a35-110">Selezionare **gruppi di connessioni** per visualizzare la raccolta gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="c5a35-110">Select **CONNECTION GROUPS** to display the Connection Groups library.</span></span>

3.  <span data-ttu-id="c5a35-111">Selezionare **Aggiungi gruppo di connessioni** per creare un nuovo gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="c5a35-111">Select **ADD CONNECTION GROUP** to create a new connection group.</span></span>

4.  <span data-ttu-id="c5a35-112">Nel riquadro **nuovo gruppo di connessioni** Digitare una descrizione per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="c5a35-112">In the **New Connection Group** pane, type a description for the group.</span></span>

5.  <span data-ttu-id="c5a35-113">Fare clic su **modifica** nel riquadro **pacchetti connessi** per aggiungere una nuova applicazione al gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="c5a35-113">Click **EDIT** in the **CONNECTED PACKAGES** pane to add a new application to the connection group.</span></span>

6.  <span data-ttu-id="c5a35-114">Nell' **intero riquadro Raccolta pacchetti** selezionare l'applicazione da aggiungere e fare clic sulla freccia per aggiungere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5a35-114">In the **PACKAGES Entire Library** pane, select the application to be added, and click the arrow to add the application.</span></span>

    <span data-ttu-id="c5a35-115">Per rimuovere un'applicazione, selezionare l'applicazione da rimuovere nel riquadro **pacchetti in** e fare clic sulla freccia.</span><span class="sxs-lookup"><span data-stu-id="c5a35-115">To remove an application, select the application to be removed in the **PACKAGES IN** pane and click the arrow.</span></span>

    <span data-ttu-id="c5a35-116">Per riassegnare le priorità alle applicazioni nel gruppo di connessioni, usare le frecce nel riquadro **pacchetti in** .</span><span class="sxs-lookup"><span data-stu-id="c5a35-116">To reprioritize the applications in your connection group, use the arrows in the **PACKAGES IN** pane.</span></span>

    <span data-ttu-id="c5a35-117">**Importante**  Per impostazione predefinita, le configurazioni di accesso ai servizi di dominio Active Directory associate a un'applicazione specifica non vengono aggiunte al gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="c5a35-117">**Important** By default, the Active Directory Domain Services access configurations that are associated with a specific application are not added to the connection group.</span></span> <span data-ttu-id="c5a35-118">Per trasferire la configurazione di Access in Active Directory, selezionare **Aggiungi accesso a un pacchetto all'accesso al gruppo**, che si trova nel riquadro **pacchetti in** .</span><span class="sxs-lookup"><span data-stu-id="c5a35-118">To transfer the Active Directory access configuration, select **ADD PACKAGE ACCESS TO GROUP ACCESS**, which is located in the **PACKAGES IN** pane.</span></span>

     

7.  <span data-ttu-id="c5a35-119">Dopo aver aggiunto tutte le applicazioni e aver configurato l'accesso a Active Directory, fare clic su **applica**.</span><span class="sxs-lookup"><span data-stu-id="c5a35-119">After adding all the applications and configuring Active Directory access, click **Apply**.</span></span>

    <span data-ttu-id="c5a35-120">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="c5a35-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c5a35-121">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c5a35-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c5a35-122">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="c5a35-122">Got an App-V issue?</span></span>** <span data-ttu-id="c5a35-123">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c5a35-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c5a35-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5a35-124">Related topics</span></span>


[<span data-ttu-id="c5a35-125">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c5a35-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="c5a35-126">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="c5a35-126">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





