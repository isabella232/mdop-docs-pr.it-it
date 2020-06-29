---
title: Come configurare l'accesso ai pacchetti tramite la console di gestione
description: Come configurare l'accesso ai pacchetti tramite la console di gestione
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805715"
---
# <span data-ttu-id="3a8e7-103">Come configurare l'accesso ai pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="3a8e7-103">How to Configure Access to Packages by Using the Management Console</span></span>


<span data-ttu-id="3a8e7-104">Prima di distribuire un pacchetto virtualizzato di App-V 5,0, è necessario configurare i gruppi di sicurezza di Active Directory Domain Services (AD DS) che saranno autorizzati ad accedere ed eseguire le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-104">Before you deploy an App-V 5.0 virtualized package, you must configure the Active Directory Domain Services (AD DS) security groups that will be allowed to access and run the applications.</span></span> <span data-ttu-id="3a8e7-105">I gruppi di sicurezza possono contenere computer o utenti.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-105">The security groups may contain computers or users.</span></span> <span data-ttu-id="3a8e7-106">L'intitolazione di un pacchetto a un gruppo di computer pubblica il pacchetto a livello globale in tutti i computer del gruppo.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-106">Entitling a package to a computer group publishes the package globally to all computers in the group.</span></span>

<span data-ttu-id="3a8e7-107">Usare la procedura seguente per configurare l'accesso ai pacchetti virtualizzati.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-107">Use the following procedure to configure access to virtualized packages.</span></span>

**<span data-ttu-id="3a8e7-108">Per concedere l'accesso a un pacchetto App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a8e7-108">To grant access to an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="3a8e7-109">Trovare il pacchetto che si vuole configurare:</span><span class="sxs-lookup"><span data-stu-id="3a8e7-109">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="3a8e7-110">Aprire la console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-110">Open the App-V 5.0 Management console.</span></span>

    2.  <span data-ttu-id="3a8e7-111">Per visualizzare la pagina di **accesso ad** , fare clic con il pulsante destro del mouse sul pacchetto da configurare e scegliere **modifica Active Directory Access**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-111">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="3a8e7-112">In alternativa, selezionare il pacchetto e fare clic su **modifica** nel riquadro di **accesso ad** .</span><span class="sxs-lookup"><span data-stu-id="3a8e7-112">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="3a8e7-113">Eseguire il provisioning di un gruppo di sicurezza per il pacchetto:</span><span class="sxs-lookup"><span data-stu-id="3a8e7-113">Provision a security group for the package:</span></span>

    1.  <span data-ttu-id="3a8e7-114">Accedere alla pagina **Trova nomi di Active Directory validi e Concedi accesso** .</span><span class="sxs-lookup"><span data-stu-id="3a8e7-114">Go to the **FIND VALID ACTIVE DIRECTORY NAMES AND GRANT ACCESS** page.</span></span>

    2.  <span data-ttu-id="3a8e7-115">Usando il formato del nome del **dominio**  \\  **groupname**, digitare il nome o una parte di un oggetto gruppo di Active Directory e fare clic su **Verifica**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-115">Using the format **mydomain** \\ **groupname**, type the name or part of the name of an Active Directory group object, and click **Check**.</span></span>

        <span data-ttu-id="3a8e7-116">**Nota**  Assicurati di specificare un nome di dominio associato per il gruppo che stai cercando.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-116">**Note** Ensure that you provide an associated domain name for the group that you are searching for.</span></span>

         

3.  <span data-ttu-id="3a8e7-117">Per concedere l'accesso al pacchetto, selezionare il gruppo desiderato e fare clic su **Concedi accesso**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-117">To grant access to the package, select the desired group and click **Grant Access**.</span></span> <span data-ttu-id="3a8e7-118">Il gruppo appena aggiunto viene visualizzato nel riquadro **ad entità con Access** .</span><span class="sxs-lookup"><span data-stu-id="3a8e7-118">The newly added group is displayed in the **AD ENTITIES WITH ACCESS** pane.</span></span>

4.  

    <span data-ttu-id="3a8e7-119">Per accettare le impostazioni di configurazione predefinite e chiudere la pagina di **accesso ad** , fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-119">To accept the default configuration settings and close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="3a8e7-120">Per personalizzare le configurazioni per un gruppo specifico, fare clic sull'elenco a discesa **Configurazioni assegnate** e selezionare **personalizzato**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-120">To customize configurations for a specific group, click the **ASSIGNED CONFIGURATIONS** drop-down and select **Custom**.</span></span> <span data-ttu-id="3a8e7-121">Per configurare le configurazioni personalizzate, fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-121">To configure the custom configurations, click **EDIT**.</span></span> <span data-ttu-id="3a8e7-122">Dopo aver concesso l'accesso, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-122">After you grant access, click **Close**.</span></span>

**<span data-ttu-id="3a8e7-123">Per rimuovere l'accesso a un pacchetto di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a8e7-123">To remove access to an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="3a8e7-124">Trovare il pacchetto che si vuole configurare:</span><span class="sxs-lookup"><span data-stu-id="3a8e7-124">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="3a8e7-125">Aprire la console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-125">Open the App-V 5.0 Management console.</span></span>

    2.  <span data-ttu-id="3a8e7-126">Per visualizzare la pagina di **accesso ad** , fare clic con il pulsante destro del mouse sul pacchetto da configurare e scegliere **modifica Active Directory Access**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-126">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="3a8e7-127">In alternativa, selezionare il pacchetto e fare clic su **modifica** nel riquadro di **accesso ad** .</span><span class="sxs-lookup"><span data-stu-id="3a8e7-127">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="3a8e7-128">Selezionare il gruppo che si vuole rimuovere e fare clic su **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-128">Select the group you want to remove, and click **DELETE**.</span></span>

3.  <span data-ttu-id="3a8e7-129">Per chiudere la pagina di **accesso ad** , fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="3a8e7-129">To close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="3a8e7-130">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="3a8e7-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3a8e7-131">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="3a8e7-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3a8e7-132">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="3a8e7-132">Got an App-V issue?</span></span>** <span data-ttu-id="3a8e7-133">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3a8e7-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3a8e7-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a8e7-134">Related topics</span></span>


[<span data-ttu-id="3a8e7-135">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3a8e7-135">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





