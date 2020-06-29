---
title: Riquadro Risultati del nodo Licenze applicazione
description: Riquadro Risultati del nodo Licenze applicazione
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819506"
---
# <span data-ttu-id="8bf9d-103">Riquadro Risultati del nodo Licenze applicazione</span><span class="sxs-lookup"><span data-stu-id="8bf9d-103">Applications Licenses Results Pane</span></span>


<span data-ttu-id="8bf9d-104">Il riquadro dei **risultati delle licenze** per le applicazioni nella console di gestione del server Application Virtualization consente di visualizzare un elenco di gruppi di licenze e applicazioni disponibili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-104">The **Applications Licenses Results** pane in the Application Virtualization Server Management Console displays a list of the available application license groups and application licenses.</span></span>

<span data-ttu-id="8bf9d-105">Fare clic con il pulsante destro del mouse su un gruppo di licenze per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-105">Right-click any application license group to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="8bf9d-106">Nuova licenza illimitata</span><span class="sxs-lookup"><span data-stu-id="8bf9d-106">New Unlimited License</span></span>**  
<span data-ttu-id="8bf9d-107">Visualizza la procedura guidata nuova licenza illimitata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-107">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="8bf9d-108">Questa opzione è disponibile solo se il gruppo di licenze non ha licenze.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-108">This option is available only when the license group has no licenses.</span></span> <span data-ttu-id="8bf9d-109">Questa procedura guidata è costituita da tre pagine:</span><span class="sxs-lookup"><span data-stu-id="8bf9d-109">This wizard consists of three pages:</span></span>

1.  <span data-ttu-id="8bf9d-110">Immettere il nome di un gruppo nel campo **nome del gruppo di licenze** per le applicazioni e un valore (in minuti) nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-110">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="8bf9d-111">È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-111">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="8bf9d-112">Immettere un breve testo descrittivo nel campo **Descrizione licenza** e selezionare la casella di controllo **abilitata** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-112">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box.</span></span> <span data-ttu-id="8bf9d-113">Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-113">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="8bf9d-114">È possibile selezionare la casella di controllo predefinita o usare l'utilità calendario per passare alla data di scadenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-114">You can select the default check box or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="8bf9d-115">Fare clic su **fine** per aggiungere la nuova licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-115">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="8bf9d-116">Nuova licenza concorrente</span><span class="sxs-lookup"><span data-stu-id="8bf9d-116">New Concurrent License</span></span>**  
<span data-ttu-id="8bf9d-117">Visualizza la creazione guidata nuova licenza simultanea.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-117">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="8bf9d-118">Questa opzione è disponibile solo se il gruppo di licenze non ha licenze illimitate.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-118">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="8bf9d-119">Questa procedura guidata è costituita dalle pagine seguenti ed è quasi identica alla nuova procedura guidata licenza illimitata:</span><span class="sxs-lookup"><span data-stu-id="8bf9d-119">This wizard consists of the following pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="8bf9d-120">Immettere il nome di un gruppo nel campo **nome del gruppo di licenze** per le applicazioni e un valore (in minuti) nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-120">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="8bf9d-121">È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-121">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="8bf9d-122">Immettere un breve testo descrittivo nel campo **Descrizione licenza** e immettere un valore nel campo **quantità licenza simultanea** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-122">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span> <span data-ttu-id="8bf9d-123">È anche possibile usare le frecce su e giù per specificare il numero di licenze simultanee.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-123">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="8bf9d-124">Selezionare la casella di controllo **abilitata** per abilitare la licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-124">Select the **Enabled** check box to enable the license.</span></span> <span data-ttu-id="8bf9d-125">Facoltativamente, è possibile usare il campo **Data di scadenza** per selezionare una data di scadenza per la licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-125">Optionally, you can use the **Expiration Date** field to select an expiration date for the license.</span></span> <span data-ttu-id="8bf9d-126">È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-126">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="8bf9d-127">Fare clic su **fine** per aggiungere le nuove licenze.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-127">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="8bf9d-128">Nuova licenza denominata</span><span class="sxs-lookup"><span data-stu-id="8bf9d-128">New Named License</span></span>**  
<span data-ttu-id="8bf9d-129">Visualizza la procedura guidata nuova licenza denominata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-129">Displays the New Named License Wizard.</span></span> <span data-ttu-id="8bf9d-130">Questa opzione è disponibile solo se il gruppo di licenze non ha licenze illimitate.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-130">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="8bf9d-131">Questa procedura guidata è composta dalle pagine seguenti:</span><span class="sxs-lookup"><span data-stu-id="8bf9d-131">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="8bf9d-132">Immettere il nome di un gruppo nel campo **nome del gruppo di licenze** per le applicazioni e un valore (in minuti) nel campo **Avviso scadenza licenza** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-132">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="8bf9d-133">È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-133">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="8bf9d-134">Immettere un breve testo descrittivo nella **Descrizione della licenza**e selezionare la casella di controllo **abilitata** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-134">Enter brief descriptive text in the **License Description**, and select the **Enabled** check box.</span></span> <span data-ttu-id="8bf9d-135">Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-135">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="8bf9d-136">È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-136">You can select the check box to use the displayed expiration date, or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="8bf9d-137">Fare clic su **Aggiungi**, **modifica**o **Rimuovi** utenti denominati.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-137">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="8bf9d-138">Fare clic su **fine** per aggiungere la nuova licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-138">Click **Finish** to add the new license.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="8bf9d-139">Nuova finestra da qui</span><span class="sxs-lookup"><span data-stu-id="8bf9d-139">New Window from Here</span></span>**  
<span data-ttu-id="8bf9d-140">Apre una nuova console di gestione con il nodo selezionato come nodo radice.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-140">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="8bf9d-141">Delete</span><span class="sxs-lookup"><span data-stu-id="8bf9d-141">Delete</span></span>**  
<span data-ttu-id="8bf9d-142">Elimina il gruppo di licenze dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-142">Deletes the license group from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="8bf9d-143">Rename</span><span class="sxs-lookup"><span data-stu-id="8bf9d-143">Rename</span></span>**  
<span data-ttu-id="8bf9d-144">Modifica il nome del gruppo di licenze per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-144">Changes the name of the applications license group.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="8bf9d-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bf9d-145">Properties</span></span>**  
<span data-ttu-id="8bf9d-146">Visualizza la finestra di dialogo **Proprietà** per i gruppi di licenze dell'applicazione selezionati.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-146">Displays the **Properties** dialog box for the selected application license groups.</span></span> <span data-ttu-id="8bf9d-147">Questa finestra di dialogo include le schede seguenti:</span><span class="sxs-lookup"><span data-stu-id="8bf9d-147">This dialog box has the following tabs:</span></span>

-   <span data-ttu-id="8bf9d-148">Scheda **generale** : Visualizza informazioni generali sul gruppo di licenze.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-148">**General** tab—Displays general information about the license group.</span></span> <span data-ttu-id="8bf9d-149">In questa scheda è possibile modificare il valore dell'ora (in minuti) nel campo di avviso per la **scadenza della licenza** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-149">From this tab, you can change the time value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="8bf9d-150">È possibile immettere qualsiasi valore compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-150">You can enter any value from 0–100.</span></span>

-   <span data-ttu-id="8bf9d-151">Scheda **applicazioni** : Visualizza l'elenco delle applicazioni associate al gruppo di licenze.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-151">**Applications** tab—Displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="8bf9d-152">Help</span><span class="sxs-lookup"><span data-stu-id="8bf9d-152">Help</span></span>**  
<span data-ttu-id="8bf9d-153">Visualizza il sistema della Guida di Application Virtualization Server Management Console.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-153">Displays the Application Virtualization Server Management Console help system.</span></span>

<span data-ttu-id="8bf9d-154">Quando nel riquadro **dei risultati** vengono visualizzati i gruppi di licenze dell'applicazione, fare clic con il pulsante destro del mouse in un punto qualsiasi del riquadro **dei risultati** , ad eccezione di un gruppo di licenze, per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-154">When the **Results** pane displays application license groups, right-click anywhere in the **Results** pane, except on a license group, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="8bf9d-155">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="8bf9d-155">Refresh</span></span>**  
<span data-ttu-id="8bf9d-156">Aggiorna la visualizzazione del server.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-156">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="8bf9d-157">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="8bf9d-157">Export List</span></span>**  
<span data-ttu-id="8bf9d-158">Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-158">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="8bf9d-159">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-159">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="8bf9d-160">Visualizza</span><span class="sxs-lookup"><span data-stu-id="8bf9d-160">View</span></span>**  
<span data-ttu-id="8bf9d-161">Modifica l'aspetto e il contenuto del riquadro dei **risultati** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-161">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="8bf9d-162">Icone disponi/allineati</span><span class="sxs-lookup"><span data-stu-id="8bf9d-162">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="8bf9d-163">Modifica la modalità di visualizzazione delle icone nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-163">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="8bf9d-164">Help</span><span class="sxs-lookup"><span data-stu-id="8bf9d-164">Help</span></span>**  
<span data-ttu-id="8bf9d-165">Visualizza il sistema della Guida per Application Virtualization Server Management Console.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-165">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="8bf9d-166">Quando nel riquadro **dei risultati** vengono visualizzate le licenze, fare clic con il pulsante destro del mouse su qualsiasi licenza dell'applicazione per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-166">When the **Results** pane displays licenses, right-click any application license to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="8bf9d-167">Delete</span><span class="sxs-lookup"><span data-stu-id="8bf9d-167">Delete</span></span>**  
<span data-ttu-id="8bf9d-168">Elimina la licenza dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-168">Deletes the license from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="8bf9d-169">Rename</span><span class="sxs-lookup"><span data-stu-id="8bf9d-169">Rename</span></span>**  
<span data-ttu-id="8bf9d-170">Modifica il nome della licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-170">Changes the name of the license.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="8bf9d-171">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bf9d-171">Properties</span></span>**  
<span data-ttu-id="8bf9d-172">Visualizza la finestra di dialogo **Proprietà** relativa alla licenza per l'applicazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-172">Displays the **Properties** dialog box for the selected application license.</span></span>

<span data-ttu-id="8bf9d-173">La scheda **generale** della finestra di dialogo **Proprietà** Visualizza le informazioni sulla licenza e consente di modificare lo stato abilitato, la data di scadenza della licenza e le informazioni sulla chiave di licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-173">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="8bf9d-174">Help</span><span class="sxs-lookup"><span data-stu-id="8bf9d-174">Help</span></span>**  
<span data-ttu-id="8bf9d-175">Visualizza il sistema della guida della console di gestione server.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-175">Displays the server management console help system.</span></span>

<span data-ttu-id="8bf9d-176">Quando nel riquadro **dei risultati** vengono visualizzate le licenze, fare clic con il pulsante destro del mouse in un punto qualsiasi del riquadro **dei risultati** , ad eccezione di una licenza, per visualizzare un menu a comparsa contenente gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-176">When the **Results** pane displays licenses, right-click anywhere in the **Results** pane, except on a license, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="8bf9d-177">Esporta elenco</span><span class="sxs-lookup"><span data-stu-id="8bf9d-177">Export List</span></span>**  
<span data-ttu-id="8bf9d-178">Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-178">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="8bf9d-179">Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-179">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="8bf9d-180">Visualizza</span><span class="sxs-lookup"><span data-stu-id="8bf9d-180">View</span></span>**  
<span data-ttu-id="8bf9d-181">Modifica l'aspetto e il contenuto del riquadro dei **risultati** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-181">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="8bf9d-182">Icone disponi/allineati</span><span class="sxs-lookup"><span data-stu-id="8bf9d-182">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="8bf9d-183">Modifica la modalità di visualizzazione delle icone nel riquadro **dei risultati** .</span><span class="sxs-lookup"><span data-stu-id="8bf9d-183">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="8bf9d-184">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8bf9d-184">Properties</span></span>**  
<span data-ttu-id="8bf9d-185">Visualizza la finestra di dialogo **Proprietà** relativa alla licenza selezionata.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-185">Displays the **Properties** dialog box for the selected license.</span></span>

<span data-ttu-id="8bf9d-186">La scheda **generale** della finestra di dialogo **Proprietà** Visualizza le informazioni sulla licenza e consente di modificare lo stato abilitato, la data di scadenza della licenza e le informazioni sulla chiave di licenza.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-186">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="8bf9d-187">Help</span><span class="sxs-lookup"><span data-stu-id="8bf9d-187">Help</span></span>**  
<span data-ttu-id="8bf9d-188">Visualizza il sistema della Guida per Application Virtualization Server Management Console.</span><span class="sxs-lookup"><span data-stu-id="8bf9d-188">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="8bf9d-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8bf9d-189">Related topics</span></span>


[<span data-ttu-id="8bf9d-190">Informazioni sulle licenze dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="8bf9d-190">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="8bf9d-191">Come gestire le licenze dell'applicazione in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="8bf9d-191">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="8bf9d-192">Server Management Console: Nodo Licenze applicazione</span><span class="sxs-lookup"><span data-stu-id="8bf9d-192">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





