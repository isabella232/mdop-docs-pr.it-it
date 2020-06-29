---
title: Nodo Criteri dei provider
description: Nodo Criteri dei provider
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815835"
---
# <span data-ttu-id="79715-103">Nodo Criteri dei provider</span><span class="sxs-lookup"><span data-stu-id="79715-103">Provider Policies Node</span></span>


<span data-ttu-id="79715-104">Il nodo **criteri provider** è un livello inferiore al nodo Application Virtualization System nel riquadro **ambito** della console di gestione di Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="79715-104">The **Provider Policies** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="79715-105">Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di criteri per il provider.</span><span class="sxs-lookup"><span data-stu-id="79715-105">When you select this node, the **Results** pane displays a list of provider policies.</span></span> <span data-ttu-id="79715-106">Fare clic con il pulsante destro del mouse sul nodo **criteri provider** per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="79715-106">Right-click the **Provider Policies** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-provider-policy"></a>**<span data-ttu-id="79715-107">Nuovi criteri per i provider</span><span class="sxs-lookup"><span data-stu-id="79715-107">New Provider Policy</span></span>**  
<span data-ttu-id="79715-108">Visualizza la creazione guidata nuovo criterio provider.</span><span class="sxs-lookup"><span data-stu-id="79715-108">Displays the New Provider Policy Wizard.</span></span> <span data-ttu-id="79715-109">Questa procedura guidata è composta dalle pagine seguenti:</span><span class="sxs-lookup"><span data-stu-id="79715-109">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="79715-110">Immettere un nome nel campo **Nome criterio provider** .</span><span class="sxs-lookup"><span data-stu-id="79715-110">Enter a name in the **Provider Policy Name** field.</span></span> <span data-ttu-id="79715-111">Selezionare la casella di controllo **Gestisci desktop client tramite la console di gestione** se si vuole che tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="79715-111">Select the **Manage client desktop using the Management Console** check box if you want that capability.</span></span> <span data-ttu-id="79715-112">Selezionare una o entrambe le caselle di controllo seguenti se si vuole eseguire la funzionalità associata:</span><span class="sxs-lookup"><span data-stu-id="79715-112">Select one or both of the following check boxes if you want the associated functionality:</span></span>

    -   **<span data-ttu-id="79715-113">Aggiornare la configurazione di pubblicazione quando un utente accede</span><span class="sxs-lookup"><span data-stu-id="79715-113">Refresh publishing configuration when a user logs in</span></span>**

    -   <span data-ttu-id="79715-114">**Aggiornare la configurazione ogni**.</span><span class="sxs-lookup"><span data-stu-id="79715-114">**Refresh configuration every**.</span></span> <span data-ttu-id="79715-115">Dopo aver selezionato questa opzione, immettere un numero e selezionare l'unità dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="79715-115">After selecting this option, enter a number and select the unit from the drop-down menu.</span></span> <span data-ttu-id="79715-116">Le voci valide variano da un minimo di **30 minuti** a un massimo di **999 giorni**.</span><span class="sxs-lookup"><span data-stu-id="79715-116">Valid entries range from a minimum of **30 minutes** to a maximum of **999 days**.</span></span>

2.  <span data-ttu-id="79715-117">Fare clic su **Aggiungi** o **Rimuovi** per aggiungere o rimuovere un'assegnazione di gruppo.</span><span class="sxs-lookup"><span data-stu-id="79715-117">Click **Add** or **Remove** to add or remove a group assignment.</span></span> <span data-ttu-id="79715-118">Usare la finestra di dialogo Esplora **Windows** standard per trovare un gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="79715-118">Use the standard **Windows Browse** dialog box to find a user group.</span></span>

3.  <span data-ttu-id="79715-119">Selezionare una delle caselle di controllo seguenti nella finestra di dialogo **configurazione pipeline provider** per abilitare la caratteristica associata:</span><span class="sxs-lookup"><span data-stu-id="79715-119">Select one of the following check boxes on the **Provider Pipeline Configuration** dialog box to enable the associated feature:</span></span>

    -   <span data-ttu-id="79715-120">**Autenticazione**: selezionare il tipo di autenticazione nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="79715-120">**Authentication**—Select the type of authentication from the drop-down list.</span></span>

    -   **<span data-ttu-id="79715-121">Applicare le impostazioni di autorizzazione di accesso</span><span class="sxs-lookup"><span data-stu-id="79715-121">Enforce Access Permission Settings</span></span>**

    -   **<span data-ttu-id="79715-122">Informazioni sull'utilizzo del log</span><span class="sxs-lookup"><span data-stu-id="79715-122">Log Usage Information</span></span>**

    -   <span data-ttu-id="79715-123">**Licenze**: selezionare uno schema di imposizione dall'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="79715-123">**Licensing**—Select an enforcement scheme from the drop-down list.</span></span>

4.  <span data-ttu-id="79715-124">Fare clic su **fine** per aggiungere i nuovi criteri del provider.</span><span class="sxs-lookup"><span data-stu-id="79715-124">Click **Finish** to add the new provider policy.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="79715-125">Visualizza</span><span class="sxs-lookup"><span data-stu-id="79715-125">View</span></span>**  
<span data-ttu-id="79715-126">Modifica l'aspetto e il contenuto del riquadro dei **risultati** .</span><span class="sxs-lookup"><span data-stu-id="79715-126">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="79715-127">Nuova finestra da qui</span><span class="sxs-lookup"><span data-stu-id="79715-127">New Window from Here</span></span>**  
<span data-ttu-id="79715-128">Apre una nuova console di gestione con il nodo selezionato come nodo radice.</span><span class="sxs-lookup"><span data-stu-id="79715-128">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="79715-129">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="79715-129">Refresh</span></span>**  
<span data-ttu-id="79715-130">Aggiorna la visualizzazione del server.</span><span class="sxs-lookup"><span data-stu-id="79715-130">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="79715-131">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="79715-131">Export List</span></span>**  
<span data-ttu-id="79715-132">Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="79715-132">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="79715-133">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="79715-133">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="79715-134">Help</span><span class="sxs-lookup"><span data-stu-id="79715-134">Help</span></span>**  
<span data-ttu-id="79715-135">Visualizza il sistema della Guida per Application Virtualization Server Management Console.</span><span class="sxs-lookup"><span data-stu-id="79715-135">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="79715-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79715-136">Related topics</span></span>


[<span data-ttu-id="79715-137">Server Management Console: Nodo Criteri dei provider</span><span class="sxs-lookup"><span data-stu-id="79715-137">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





