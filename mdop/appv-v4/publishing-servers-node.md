---
title: Nodo Server di pubblicazione
description: Nodo Server di pubblicazione
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815796"
---
# <span data-ttu-id="b304a-103">Nodo Server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="b304a-103">Publishing Servers Node</span></span>


<span data-ttu-id="b304a-104">Il nodo **server di pubblicazione** è un livello inferiore al nodo **Application Virtualization** nel riquadro **ambito** della console di gestione client di Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b304a-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="b304a-105">Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b304a-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="b304a-106">Fare clic con il pulsante destro del mouse sul nodo **Publishing Servers** per visualizzare un menu di scelta rapida che contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b304a-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="b304a-107">Nuovo server</span><span class="sxs-lookup"><span data-stu-id="b304a-107">New Server</span></span>**  
<span data-ttu-id="b304a-108">Questa voce di menu Visualizza la procedura guidata nuovo server.</span><span class="sxs-lookup"><span data-stu-id="b304a-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="b304a-109">Questa procedura guidata è costituita da due pagine:</span><span class="sxs-lookup"><span data-stu-id="b304a-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="b304a-110">Immettere un nome visualizzato del server e un tipo di server:</span><span class="sxs-lookup"><span data-stu-id="b304a-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="b304a-111">**Nome visualizzato**: immettere un nome che si vuole visualizzare per il server.</span><span class="sxs-lookup"><span data-stu-id="b304a-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="b304a-112">Questo campo è vuoto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b304a-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="b304a-113">**Tipo**: scegliere il tipo di server nell'elenco a discesa dei tipi di server.</span><span class="sxs-lookup"><span data-stu-id="b304a-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="b304a-114">Specificare le impostazioni di connessione per il server:</span><span class="sxs-lookup"><span data-stu-id="b304a-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="b304a-115">**Host name**: immettere il nome o l'indirizzo IP per il server.</span><span class="sxs-lookup"><span data-stu-id="b304a-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="b304a-116">**Porta**: immettere un valore numerico corrispondente al numero di porta.</span><span class="sxs-lookup"><span data-stu-id="b304a-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="b304a-117">Il valore predefinito è 554 se il tipo di server è "Application Virtualization Server" e 80 se il tipo di server è "server HTTP standard".</span><span class="sxs-lookup"><span data-stu-id="b304a-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="b304a-118">**Path**: questo campo viene impostato su "/" ed è di sola lettura quando il tipo di server è "Application Virtualization Server" o "Enhanced Security Application Virtualization Server".</span><span class="sxs-lookup"><span data-stu-id="b304a-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="b304a-119">Quando il tipo di server è "server HTTP standard" o "server HTTP di sicurezza avanzato", anche il campo **path** è modificabile.</span><span class="sxs-lookup"><span data-stu-id="b304a-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="b304a-120">Nuova finestra da qui</span><span class="sxs-lookup"><span data-stu-id="b304a-120">New Window from Here</span></span>**  
<span data-ttu-id="b304a-121">Selezionare questa voce di menu per aprire una nuova console di gestione con il nodo selezionato come nodo radice.</span><span class="sxs-lookup"><span data-stu-id="b304a-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="b304a-122">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="b304a-122">Export List</span></span>**  
<span data-ttu-id="b304a-123">Puoi usare questa voce di menu per creare un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="b304a-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="b304a-124">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="b304a-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="b304a-125">Visualizza</span><span class="sxs-lookup"><span data-stu-id="b304a-125">View</span></span>**  
<span data-ttu-id="b304a-126">Questo elenco popup di voci di menu consente di modificare l'aspetto e il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="b304a-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="b304a-127">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="b304a-127">Refresh</span></span>**  
<span data-ttu-id="b304a-128">Selezionare questa voce per aggiornare la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="b304a-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="b304a-129">Help</span><span class="sxs-lookup"><span data-stu-id="b304a-129">Help</span></span>**  
<span data-ttu-id="b304a-130">Questo elemento Visualizza il sistema della Guida per la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="b304a-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="b304a-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b304a-131">Related topics</span></span>


[<span data-ttu-id="b304a-132">Riquadro Risultati del nodo Server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="b304a-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="b304a-133">Colonne del riquadro Risultati del nodo Server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="b304a-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





