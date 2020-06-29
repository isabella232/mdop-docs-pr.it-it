---
title: Come generare report
description: Come generare report
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826995"
---
# <span data-ttu-id="15df8-103">Come generare report</span><span class="sxs-lookup"><span data-stu-id="15df8-103">How to Generate Reports</span></span>


<span data-ttu-id="15df8-104">I tipi di report seguenti possono essere creati dagli amministratori in MED-V:</span><span class="sxs-lookup"><span data-stu-id="15df8-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="15df8-105">[Stato](#bkmk-generatingastatusreport): usa il rapporto sullo stato per esaminare lo stato corrente di tutti gli utenti attivi e tutte le aree di lavoro MED-V di ogni utente in base a un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="15df8-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="15df8-106">Ciò include la visualizzazione di computer attualmente connessi al server o, se non sono attualmente connessi, la data e l'ora in cui sono stati connessi per ultimo al server, lo stato di ogni computer e altre informazioni rilevanti.</span><span class="sxs-lookup"><span data-stu-id="15df8-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="15df8-107">[Log attività](#bkmk-generatinganactivitylogreport): usare questo report per esaminare gli eventi originati da un utente o un host specifico in un intervallo di date definito.</span><span class="sxs-lookup"><span data-stu-id="15df8-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="15df8-108">[Log errori](#bkmk-generatinganerrorlogreport): usare questo report per visualizzare gli errori originati da un utente o un host specifico in un intervallo di date definito.</span><span class="sxs-lookup"><span data-stu-id="15df8-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="15df8-109">I risultati del report possono essere ordinati in base a qualsiasi colonna facendo clic sul nome della colonna appropriata.</span><span class="sxs-lookup"><span data-stu-id="15df8-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="15df8-110">I risultati del report possono essere raggruppati trascinando un'intestazione di colonna nella parte superiore del report.</span><span class="sxs-lookup"><span data-stu-id="15df8-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="15df8-111">Trascinare più intestazioni di colonna per raggruppare una colonna dopo l'altra.</span><span class="sxs-lookup"><span data-stu-id="15df8-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="15df8-112">Come generare un report sullo stato</span><span class="sxs-lookup"><span data-stu-id="15df8-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="15df8-113">Per generare un report sullo stato</span><span class="sxs-lookup"><span data-stu-id="15df8-113">To generate a status report</span></span>**

1.  <span data-ttu-id="15df8-114">Fare clic sul pulsante Gestione **report** .</span><span class="sxs-lookup"><span data-stu-id="15df8-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="15df8-115">Nel modulo **report** scegliere **stato**dal menu **tipi di report** e fare clic su **genera**.</span><span class="sxs-lookup"><span data-stu-id="15df8-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="15df8-116">Verrà visualizzata la finestra di dialogo parametri rapporto.</span><span class="sxs-lookup"><span data-stu-id="15df8-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="15df8-117">Nella finestra di dialogo **parametri rapporto** , nel campo **numero di giorni** , immettere un numero o usare le frecce per selezionare il numero di giorni da includere nel report di stato e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="15df8-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="15df8-118">Viene generato un report di stato.</span><span class="sxs-lookup"><span data-stu-id="15df8-118">A status report is generated.</span></span> <span data-ttu-id="15df8-119">I parametri del report sono definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="15df8-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="15df8-120">Proprietà area di lavoro client MED-V</span><span class="sxs-lookup"><span data-stu-id="15df8-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15df8-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15df8-121">Property</span></span></th>
<th align="left"><span data-ttu-id="15df8-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15df8-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-123">Tempo</span><span class="sxs-lookup"><span data-stu-id="15df8-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-124">Data e ora in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15df8-125">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-125">Note</span></span></strong><br/><p><span data-ttu-id="15df8-126">Per impostazione predefinita, gli eventi vengono visualizzati in ordine di data decrescente.</span><span class="sxs-lookup"><span data-stu-id="15df8-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="15df8-127">Tuttavia, può essere modificato facendo clic sulla colonna data/ora ricevuta.</span><span class="sxs-lookup"><span data-stu-id="15df8-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-128">Nome utente</span><span class="sxs-lookup"><span data-stu-id="15df8-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-129">L'utente che ha avviato l'evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15df8-130">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-130">Note</span></span></strong><br/><p><span data-ttu-id="15df8-131">Se l'evento si è verificato prima che un utente abbia effettuato l'accesso, il nome utente è SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="15df8-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-132">Nome host</span><span class="sxs-lookup"><span data-stu-id="15df8-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-133">Il nome del computer host.</span><span class="sxs-lookup"><span data-stu-id="15df8-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-134">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="15df8-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-135">Nome dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15df8-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-136">Nome computer area di lavoro</span><span class="sxs-lookup"><span data-stu-id="15df8-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-137">Nome del computer in cui è in uso l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15df8-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-138">Online</span><span class="sxs-lookup"><span data-stu-id="15df8-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-139">Lo stato corrente del computer client:</span><span class="sxs-lookup"><span data-stu-id="15df8-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="15df8-140">Ha smesso</span><span class="sxs-lookup"><span data-stu-id="15df8-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="15df8-141">Iniziato alla &lt; data e ora in cui è stata avviata l'area di lavoro&gt;</span><span class="sxs-lookup"><span data-stu-id="15df8-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-142">Versione client</span><span class="sxs-lookup"><span data-stu-id="15df8-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-143">Numero di versione del client.</span><span class="sxs-lookup"><span data-stu-id="15df8-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-144">Versione dei criteri</span><span class="sxs-lookup"><span data-stu-id="15df8-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-145">La versione del criterio attualmente utilizzata dall'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15df8-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-146">Nome immagine</span><span class="sxs-lookup"><span data-stu-id="15df8-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-147">Nome dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="15df8-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-148">Versione immagine</span><span class="sxs-lookup"><span data-stu-id="15df8-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-149">Versione dell'immagine che l'area di lavoro MED-V sta attualmente usando.</span><span class="sxs-lookup"><span data-stu-id="15df8-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15df8-150">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-150">Note</span></span></strong><br/><p><span data-ttu-id="15df8-151">La versione dell'area di lavoro MED-V può essere sconosciuta se non è stata ancora scaricata nel computer.</span><span class="sxs-lookup"><span data-stu-id="15df8-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="15df8-152">Come generare un report del log attività</span><span class="sxs-lookup"><span data-stu-id="15df8-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="15df8-153">Per generare un report del log attività</span><span class="sxs-lookup"><span data-stu-id="15df8-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="15df8-154">Fare clic sul pulsante Gestione **report** .</span><span class="sxs-lookup"><span data-stu-id="15df8-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="15df8-155">Viene visualizzato il modulo report.</span><span class="sxs-lookup"><span data-stu-id="15df8-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="15df8-156">Nel modulo **report** selezionare **log attività**dal menu **tipi di report** e fare clic su **genera**.</span><span class="sxs-lookup"><span data-stu-id="15df8-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="15df8-157">Nella finestra di dialogo **parametri report** configurare uno o più dei parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="15df8-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="15df8-158">**Numero di giorni**: il numero di giorni da visualizzare nel report.</span><span class="sxs-lookup"><span data-stu-id="15df8-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="15df8-159">**Nome utente contiene**: ogni evento in cui il nome utente contiene il testo immesso è incluso nel report.</span><span class="sxs-lookup"><span data-stu-id="15df8-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="15df8-160">**Host Name Contains**: ogni evento in cui il nome host contiene il testo immesso è incluso nel report.</span><span class="sxs-lookup"><span data-stu-id="15df8-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="15df8-161">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="15df8-161">Click **OK**.</span></span>

    <span data-ttu-id="15df8-162">Viene generato un report con gli eventi e le date selezionati.</span><span class="sxs-lookup"><span data-stu-id="15df8-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="15df8-163">I parametri del report sono definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="15df8-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="15df8-164">Proprietà del report del log attività</span><span class="sxs-lookup"><span data-stu-id="15df8-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15df8-165">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15df8-165">Property</span></span></th>
<th align="left"><span data-ttu-id="15df8-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15df8-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-167">ID evento</span><span class="sxs-lookup"><span data-stu-id="15df8-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-168">ID evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-169">Gravità</span><span class="sxs-lookup"><span data-stu-id="15df8-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="15df8-170">Informazioni, errore, avviso</span><span class="sxs-lookup"><span data-stu-id="15df8-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-171">Categoria</span><span class="sxs-lookup"><span data-stu-id="15df8-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-172">Il modulo a cui fa riferimento il report.</span><span class="sxs-lookup"><span data-stu-id="15df8-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15df8-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-174">Descrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-175">Tempo ricevuto</span><span class="sxs-lookup"><span data-stu-id="15df8-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-176">Data e ora in cui l'evento è stato ricevuto nel server.</span><span class="sxs-lookup"><span data-stu-id="15df8-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15df8-177">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-177">Note</span></span></strong><br/><p><span data-ttu-id="15df8-178">Se il client sta lavorando offline, il server riceve i report quando il client è online.</span><span class="sxs-lookup"><span data-stu-id="15df8-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="15df8-179">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-179">Note</span></span></strong><br/><p><span data-ttu-id="15df8-180">Per impostazione predefinita, gli eventi vengono visualizzati in ordine di data decrescente.</span><span class="sxs-lookup"><span data-stu-id="15df8-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="15df8-181">Tuttavia, può essere modificato facendo clic sulla <strong> colonna data/ora ricevuta </strong> .</span><span class="sxs-lookup"><span data-stu-id="15df8-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-182">Ora client</span><span class="sxs-lookup"><span data-stu-id="15df8-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-183">La data e l'ora in cui si è verificato l'evento in base all'orologio client.</span><span class="sxs-lookup"><span data-stu-id="15df8-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-184">Nome host</span><span class="sxs-lookup"><span data-stu-id="15df8-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-185">Il nome del computer host.</span><span class="sxs-lookup"><span data-stu-id="15df8-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-186">Nome utente</span><span class="sxs-lookup"><span data-stu-id="15df8-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-187">L'utente che ha avviato l'evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-188">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="15df8-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-189">Nome dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15df8-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-190">Nome computer area di lavoro</span><span class="sxs-lookup"><span data-stu-id="15df8-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-191">Nome del computer in cui è in uso l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15df8-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="15df8-192">Come generare un report del log degli errori</span><span class="sxs-lookup"><span data-stu-id="15df8-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="15df8-193">Per generare un report del log degli errori</span><span class="sxs-lookup"><span data-stu-id="15df8-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="15df8-194">Fare clic sul pulsante Gestione **report** .</span><span class="sxs-lookup"><span data-stu-id="15df8-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="15df8-195">Nel menu **tipi di report** del modulo **report** selezionare **log degli errori**e quindi fare clic su **genera**.</span><span class="sxs-lookup"><span data-stu-id="15df8-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="15df8-196">Nella finestra di dialogo **parametri report** configurare uno o più dei parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="15df8-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="15df8-197">**Numero di giorni**: il numero di giorni da visualizzare nel report.</span><span class="sxs-lookup"><span data-stu-id="15df8-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="15df8-198">**Nome utente contiene**: ogni evento in cui il nome utente contiene il testo immesso è incluso nel report.</span><span class="sxs-lookup"><span data-stu-id="15df8-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="15df8-199">**Host Name Contains**: ogni evento in cui il nome host contiene il testo immesso è incluso nel report.</span><span class="sxs-lookup"><span data-stu-id="15df8-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="15df8-200">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="15df8-200">Click **OK**.</span></span>

    <span data-ttu-id="15df8-201">Viene generato un report con gli eventi e le date selezionati.</span><span class="sxs-lookup"><span data-stu-id="15df8-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="15df8-202">I parametri del report sono definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="15df8-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="15df8-203">Proprietà del report log errori</span><span class="sxs-lookup"><span data-stu-id="15df8-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15df8-204">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15df8-204">Property</span></span></th>
<th align="left"><span data-ttu-id="15df8-205">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15df8-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-206">ID evento</span><span class="sxs-lookup"><span data-stu-id="15df8-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-207">ID evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-208">Categoria</span><span class="sxs-lookup"><span data-stu-id="15df8-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-209">Il modulo a cui fa riferimento il report.</span><span class="sxs-lookup"><span data-stu-id="15df8-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15df8-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-211">Descrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-212">Tempo ricevuto</span><span class="sxs-lookup"><span data-stu-id="15df8-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-213">Data e ora in cui l'evento è stato ricevuto nel server.</span><span class="sxs-lookup"><span data-stu-id="15df8-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="15df8-214">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-214">Note</span></span></strong><br/><p><span data-ttu-id="15df8-215">Se il client sta lavorando offline, il server riceve i report quando il client è online.</span><span class="sxs-lookup"><span data-stu-id="15df8-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="15df8-216">Nota</span><span class="sxs-lookup"><span data-stu-id="15df8-216">Note</span></span></strong><br/><p><span data-ttu-id="15df8-217">Per impostazione predefinita, gli eventi vengono visualizzati in ordine di data decrescente.</span><span class="sxs-lookup"><span data-stu-id="15df8-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="15df8-218">Tuttavia, può essere modificato facendo clic sulla <strong> colonna data/ora ricevuta </strong> .</span><span class="sxs-lookup"><span data-stu-id="15df8-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-219">Ora client</span><span class="sxs-lookup"><span data-stu-id="15df8-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-220">La data e l'ora in cui si è verificato l'evento in base all'orologio client.</span><span class="sxs-lookup"><span data-stu-id="15df8-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-221">Nome host</span><span class="sxs-lookup"><span data-stu-id="15df8-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-222">Il nome del computer host.</span><span class="sxs-lookup"><span data-stu-id="15df8-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15df8-223">Nome utente</span><span class="sxs-lookup"><span data-stu-id="15df8-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-224">L'utente che ha avviato l'evento.</span><span class="sxs-lookup"><span data-stu-id="15df8-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15df8-225">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="15df8-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="15df8-226">Nome dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15df8-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











