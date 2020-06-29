---
title: Nodo Licenze applicazione
description: Nodo Licenze applicazione
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819515"
---
# <span data-ttu-id="286cd-103">Nodo Licenze applicazione</span><span class="sxs-lookup"><span data-stu-id="286cd-103">Applications Licenses Node</span></span>


<span data-ttu-id="286cd-104">Il nodo **licenze per le applicazioni** è un livello inferiore al nodo Application Virtualization System nel riquadro **ambito** della console di gestione di Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="286cd-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="286cd-105">Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di licenze e gruppi di licenze.</span><span class="sxs-lookup"><span data-stu-id="286cd-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="286cd-106">Sono disponibili i tipi di licenza seguenti:</span><span class="sxs-lookup"><span data-stu-id="286cd-106">The following license types are available:</span></span>

-   <span data-ttu-id="286cd-107">**Licenza illimitata**: consente di accedere a qualsiasi numero di utenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="286cd-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="286cd-108">Questo metodo di gestione delle licenze è appropriato quando si vuole associare una licenza a livello aziendale a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="286cd-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="286cd-109">**Licenza simultanea**: consente di definire il numero massimo di utenti simultanei autorizzati a usare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="286cd-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="286cd-110">**Licenza denominata**: consente di assegnare una licenza a un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="286cd-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="286cd-111">Una licenza denominata può essere usata per garantire che un determinato utente sia sempre in grado di eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="286cd-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="286cd-112">**Nota**  Puoi combinare licenze simultanee e denominate per la stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="286cd-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="286cd-113">Fare clic con il pulsante destro del mouse sul nodo **licenze applicazioni** per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="286cd-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="286cd-114">Nuova licenza illimitata</span><span class="sxs-lookup"><span data-stu-id="286cd-114">New Unlimited License</span></span>**  
<span data-ttu-id="286cd-115">Visualizza la procedura guidata nuova licenza illimitata.</span><span class="sxs-lookup"><span data-stu-id="286cd-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="286cd-116">Questa procedura guidata è composta dalle pagine seguenti:</span><span class="sxs-lookup"><span data-stu-id="286cd-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="286cd-117">Immettere il nome del gruppo di licenze nel campo **nome del gruppo di licenze** per le applicazioni e immettere un valore (in minuti) nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="286cd-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="286cd-118">È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="286cd-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="286cd-119">Immettere un breve testo descrittivo nel campo **Descrizione licenza** e selezionare la casella di controllo **abilitata** per abilitare la licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="286cd-120">Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="286cd-121">È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="286cd-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="286cd-122">Fare clic su **fine** per aggiungere la nuova licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="286cd-123">Nuova licenza concorrente</span><span class="sxs-lookup"><span data-stu-id="286cd-123">New Concurrent License</span></span>**  
<span data-ttu-id="286cd-124">Visualizza la creazione guidata nuova licenza simultanea.</span><span class="sxs-lookup"><span data-stu-id="286cd-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="286cd-125">Questa procedura guidata è composta dalle tre pagine seguenti ed è quasi identica alla nuova procedura guidata licenza illimitata:</span><span class="sxs-lookup"><span data-stu-id="286cd-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="286cd-126">Immettere il nome del gruppo di licenze nel campo **nome del gruppo di licenze** per le applicazioni e immettere un valore (in minuti) nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="286cd-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="286cd-127">È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="286cd-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="286cd-128">Immettere un breve testo descrittivo nel campo **Descrizione licenza** e immettere un valore nel campo **quantità licenza simultanea** .</span><span class="sxs-lookup"><span data-stu-id="286cd-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="286cd-129">È anche possibile usare le frecce su e giù per specificare il numero di licenze simultanee.</span><span class="sxs-lookup"><span data-stu-id="286cd-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="286cd-130">Selezionare la casella di controllo **abilitata** per abilitare la licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="286cd-131">Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="286cd-132">È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="286cd-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="286cd-133">Fare clic su **fine** per aggiungere le nuove licenze.</span><span class="sxs-lookup"><span data-stu-id="286cd-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="286cd-134">Nuova licenza denominata</span><span class="sxs-lookup"><span data-stu-id="286cd-134">New Named License</span></span>**  
<span data-ttu-id="286cd-135">Visualizza la procedura guidata nuova licenza denominata.</span><span class="sxs-lookup"><span data-stu-id="286cd-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="286cd-136">Questa procedura guidata è composta dalle quattro pagine seguenti:</span><span class="sxs-lookup"><span data-stu-id="286cd-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="286cd-137">Immettere il nome del gruppo di licenze nel campo **nome del gruppo di licenze** per le applicazioni e immettere un valore (in minuti) nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="286cd-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="286cd-138">È possibile immettere qualsiasi valore compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="286cd-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="286cd-139">È anche possibile usare le frecce su e giù per selezionare il numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="286cd-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="286cd-140">Immettere un breve testo descrittivo nel campo **Descrizione licenza** e selezionare la casella di controllo **abilitata** per abilitare la licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="286cd-141">Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="286cd-142">È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="286cd-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="286cd-143">Fare clic su **Aggiungi**, **modifica**o **Rimuovi** utenti denominati.</span><span class="sxs-lookup"><span data-stu-id="286cd-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="286cd-144">Fare clic su **fine** per aggiungere la nuova licenza.</span><span class="sxs-lookup"><span data-stu-id="286cd-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="286cd-145">Visualizza</span><span class="sxs-lookup"><span data-stu-id="286cd-145">View</span></span>**  
<span data-ttu-id="286cd-146">Modifica l'aspetto e il contenuto del riquadro dei **risultati** .</span><span class="sxs-lookup"><span data-stu-id="286cd-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="286cd-147">Nuova finestra da qui</span><span class="sxs-lookup"><span data-stu-id="286cd-147">New Window from Here</span></span>**  
<span data-ttu-id="286cd-148">Apre una nuova console di gestione con il nodo selezionato come nodo radice.</span><span class="sxs-lookup"><span data-stu-id="286cd-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="286cd-149">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="286cd-149">Refresh</span></span>**  
<span data-ttu-id="286cd-150">Aggiorna la visualizzazione del server.</span><span class="sxs-lookup"><span data-stu-id="286cd-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="286cd-151">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="286cd-151">Export List</span></span>**  
<span data-ttu-id="286cd-152">Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="286cd-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="286cd-153">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="286cd-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="286cd-154">Help</span><span class="sxs-lookup"><span data-stu-id="286cd-154">Help</span></span>**  
<span data-ttu-id="286cd-155">Visualizza il sistema della Guida per Application Virtualization Server Management Console.</span><span class="sxs-lookup"><span data-stu-id="286cd-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="286cd-156">Se si fa clic su un gruppo di licenze o una licenza visualizzata sotto il nodo **licenze applicazione** nel riquadro **ambito** , sono disponibili gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="286cd-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="286cd-157">Visualizza</span><span class="sxs-lookup"><span data-stu-id="286cd-157">View</span></span>**  
<span data-ttu-id="286cd-158">Modifica l'aspetto e il contenuto del riquadro dei **risultati** .</span><span class="sxs-lookup"><span data-stu-id="286cd-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="286cd-159">Nuova finestra da qui</span><span class="sxs-lookup"><span data-stu-id="286cd-159">New Window from Here</span></span>**  
<span data-ttu-id="286cd-160">Apre una nuova console di gestione con il nodo selezionato come nodo radice.</span><span class="sxs-lookup"><span data-stu-id="286cd-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="286cd-161">Delete</span><span class="sxs-lookup"><span data-stu-id="286cd-161">Delete</span></span>**  
<span data-ttu-id="286cd-162">Elimina un pacchetto dal riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="286cd-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="286cd-163">Rename</span><span class="sxs-lookup"><span data-stu-id="286cd-163">Rename</span></span>**  
<span data-ttu-id="286cd-164">Modifica il nome di un pacchetto nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="286cd-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="286cd-165">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="286cd-165">Export List</span></span>**  
<span data-ttu-id="286cd-166">Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="286cd-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="286cd-167">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="286cd-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="286cd-168">Proprietà</span><span class="sxs-lookup"><span data-stu-id="286cd-168">Properties</span></span>**  
<span data-ttu-id="286cd-169">Visualizza la finestra di dialogo **Proprietà** per il gruppo di licenze selezionato.</span><span class="sxs-lookup"><span data-stu-id="286cd-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="286cd-170">La scheda **generale** della finestra di dialogo **Proprietà** consente di visualizzare le informazioni sul gruppo di licenze e di modificare il valore dell'ora nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="286cd-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="286cd-171">Nella scheda **applicazioni** viene visualizzato l'elenco delle applicazioni associate al gruppo di licenze.</span><span class="sxs-lookup"><span data-stu-id="286cd-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="286cd-172">Help</span><span class="sxs-lookup"><span data-stu-id="286cd-172">Help</span></span>**  
<span data-ttu-id="286cd-173">Visualizza il sistema della Guida per Application Virtualization Server Management Console.</span><span class="sxs-lookup"><span data-stu-id="286cd-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="286cd-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="286cd-174">Related topics</span></span>


[<span data-ttu-id="286cd-175">Informazioni sulle licenze dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="286cd-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="286cd-176">Come gestire le licenze dell'applicazione in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="286cd-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="286cd-177">Server Management Console: Nodo Licenze applicazione</span><span class="sxs-lookup"><span data-stu-id="286cd-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





