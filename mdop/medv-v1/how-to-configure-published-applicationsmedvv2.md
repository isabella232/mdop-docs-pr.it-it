---
title: Come configurare le applicazioni pubblicate
description: Come configurare le applicazioni pubblicate
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824315"
---
# <span data-ttu-id="f0ab9-103">Come configurare le applicazioni pubblicate</span><span class="sxs-lookup"><span data-stu-id="f0ab9-103">How to Configure Published Applications</span></span>


<span data-ttu-id="f0ab9-104">Le applicazioni che non sono compatibili con il sistema operativo host possono essere eseguite all'interno dell'area di lavoro MED-V e avviate dall'area di lavoro MED-V nello stesso modo in cui vengono avviate dal desktop, dal menu Start o da un collegamento a un host locale.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-104">Applications that are not compatible with the host operating system can be run within the MED-V workspace and initiated from within the MED-V workspace the same way they are initiated from the desktop—from the Start menu or from a local host shortcut.</span></span> <span data-ttu-id="f0ab9-105">Le applicazioni selezionate e definite sono denominate applicazioni pubblicate.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-105">Applications selected and defined are called published applications.</span></span> <span data-ttu-id="f0ab9-106">Le procedure descritte in questa sezione illustrano come aggiungere e rimuovere le applicazioni pubblicate.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-106">The procedures in this section describe how to add and remove published applications.</span></span>

<span data-ttu-id="f0ab9-107">Un'applicazione può essere pubblicata in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0ab9-107">An application can be published in one of the following ways:</span></span>

-   <span data-ttu-id="f0ab9-108">Come applicazione: selezionare un'applicazione specifica digitando la riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-108">As an application—Select a specific application by typing in the command line for the application.</span></span> <span data-ttu-id="f0ab9-109">Viene pubblicata solo l'applicazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-109">Only the application selected is published.</span></span>

-   <span data-ttu-id="f0ab9-110">Come menu: selezionare una cartella contenente più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-110">As a menu—Select a folder that contains multiple applications.</span></span> <span data-ttu-id="f0ab9-111">Tutte le applicazioni all'interno della cartella vengono pubblicate e visualizzate come menu.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-111">All applications within the folder are published and displayed as a menu.</span></span>

## <a href="" id="bkmk-addingapublishedapplication"></a><span data-ttu-id="f0ab9-112">Come aggiungere un'applicazione pubblicata a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-112">How to Add a Published Application to a MED-V Workspace</span></span>


**<span data-ttu-id="f0ab9-113">Per aggiungere un'applicazione all'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-113">To add an application to the MED-V workspace</span></span>**

1.  <span data-ttu-id="f0ab9-114">Fare clic sull'area di lavoro MED-V per configurare.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-114">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="f0ab9-115">Nella sezione **applicazioni pubblicate** del riquadro **applicazioni** fare clic su **Aggiungi** per aggiungere una nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-115">In the **Applications** pane, in the **Published Applications** section, click **Add** to add a new application.</span></span>

3.  <span data-ttu-id="f0ab9-116">Configurare le proprietà dell'applicazione come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-116">Configure the application properties as described in the following table.</span></span>

4.  <span data-ttu-id="f0ab9-117">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-117">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="f0ab9-118">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-118">Note</span></span>**  
    <span data-ttu-id="f0ab9-119">Se si imposta Internet Explorer come applicazione pubblicata per verificare che il reindirizzamento del Web funzioni correttamente, verificare che i parametri non siano racchiusi tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-119">If you are setting Internet Explorer as a published application to ensure that Web redirection works properly, make certain that any parameters are not in parentheses.</span></span>



**<span data-ttu-id="f0ab9-120">Proprietà delle applicazioni pubblicate</span><span class="sxs-lookup"><span data-stu-id="f0ab9-120">Published Application Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ab9-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0ab9-121">Property</span></span></th>
<th align="left"><span data-ttu-id="f0ab9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ab9-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ab9-123">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f0ab9-123">Enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-124">Selezionare questa casella di controllo per abilitare l'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-124">Select this check box to enable the published application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ab9-125">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="f0ab9-125">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-126">Il nome del collegamento nel menu Start di Windows dell'utente&#39;.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-126">The name of the shortcut in the user&#39;s Windows Start menu.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ab9-127">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-127">Note</span></span></strong><br/><p><span data-ttu-id="f0ab9-128">Il nome visualizzato non è distinzione tra maiuscole e <strong> </strong> minuscole.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-128">The display name is <strong>not</strong> case sensitive.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ab9-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ab9-129">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-130">Descrizione dell'applicazione pubblicata, che viene visualizzata come descrizione comando quando l'utente&#39;il puntatore del mouse sul collegamento.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-130">A description of the published application, which appears as a tooltip when the user&#39;s mouse hovers over the shortcut.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ab9-131">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="f0ab9-131">Command line</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-132">Comando usato per eseguire l'applicazione dall'interno dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-132">The command used to run the application from within the MED-V workspace.</span></span> <span data-ttu-id="f0ab9-133">Il percorso completo è obbligatorio e i parametri possono essere passati all'applicazione in modo simile a qualsiasi altro comando Windows.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-133">The full path is required, and the parameters can be passed to the application in a similar fashion as in any other Windows command.</span></span></p>
<p><span data-ttu-id="f0ab9-134">In un'area di lavoro di revertible MED-V è possibile eseguire il mapping di un'unità di rete con la sintassi MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; drive &gt; &lt; path, &gt; </em> &quot; ad esempio &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="f0ab9-134">In a revertible MED-V workspace, you can map a network drive with MapNetworkDrive syntax: &quot;<em>MapNetworkDrive &lt;drive&gt; &lt;path&gt;</em>&quot;—for example, &quot;<em>MapNetworkDrive t: \tux\date</em>&quot;.</span></span></p>
<p><span data-ttu-id="f0ab9-135">Ad esempio, per pubblicare Esplora risorse, usare la sintassi seguente: &quot; <em> c: &lt; /em &gt; &quot; o &quot; <em> c:\Windows </em> .&quot;</span><span class="sxs-lookup"><span data-stu-id="f0ab9-135">For example, to publish Windows Explorer, use the following syntax: &quot;<em>c:&lt;/em&gt;&quot; or &quot;<em>c:\windows</em>.&quot;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ab9-136">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-136">Note</span></span></strong><br/><p><span data-ttu-id="f0ab9-137">Per avere una risoluzione del nome, è necessario eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0ab9-137">To have a name resolution, you need to perform one of the following:</span></span></p>
</div>
<div>

</div>
<ul>
<li><p><span data-ttu-id="f0ab9-138">Configurare il DNS nell'immagine dell'area di lavoro base MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-138">Configure the DNS in the base MED-V workspace image.</span></span></p></li>
<li><p><span data-ttu-id="f0ab9-139">Verificare che la risoluzione DNS sia definita nell'host e configurarla per l'uso dell'host DNS.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-139">Verify the DNS resolution is defined in the host, and configure it to use the host DNS.</span></span></p></li>
<li><p><span data-ttu-id="f0ab9-140">Usare l'IP per definire l'unità di rete.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-140">Use the IP for defining the network drive.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="f0ab9-141">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-141">Note</span></span></strong><br/><p><span data-ttu-id="f0ab9-142">Se il percorso include spazi, l'intero percorso deve essere racchiuso tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-142">If the path includes spaces, the entire path must be inside quotation marks.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="f0ab9-143">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-143">Note</span></span></strong><br/><p><span data-ttu-id="f0ab9-144">Il percorso non deve terminare con una barra rovesciata ().</span><span class="sxs-lookup"><span data-stu-id="f0ab9-144">The path should not end with a backslash ().</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ab9-145">Menu Start</span><span class="sxs-lookup"><span data-stu-id="f0ab9-145">Start menu</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-146">Selezionare questa casella di controllo per creare un collegamento per l'applicazione nel menu Start di Windows dell'utente&#39;.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-146">Select this check box to create a shortcut for the application in the user&#39;s Windows Start menu.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f0ab9-147">Tutte le applicazioni pubblicate vengono visualizzate come tasti di scelta rapida nel menu **Start** di Windows (**Start &gt; All &gt; Applications programs MED-V**).</span><span class="sxs-lookup"><span data-stu-id="f0ab9-147">All published applications appear as shortcuts in the Windows **Start** menu (**Start &gt;All Programs&gt; MED-V Applications**).</span></span>

## <span data-ttu-id="f0ab9-148">Come rimuovere un'applicazione pubblicata da un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-148">How to Remove a Published Application from a MED-V Workspace</span></span>


**<span data-ttu-id="f0ab9-149">Per rimuovere un'applicazione dall'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-149">To remove an application from the MED-V workspace</span></span>**

1.  <span data-ttu-id="f0ab9-150">Fare clic su un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-150">Click a MED-V workspace.</span></span>

2.  <span data-ttu-id="f0ab9-151">Nella sezione **applicazioni pubblicate** del riquadro **applicazioni** selezionare un'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-151">In the **Applications** pane, in the **Published Applications** section, select an application to remove.</span></span>

3.  <span data-ttu-id="f0ab9-152">Fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-152">Click **Remove**.</span></span>

    <span data-ttu-id="f0ab9-153">L'applicazione viene rimossa dall'elenco delle applicazioni pubblicate.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-153">The application is removed from the list of published applications.</span></span>

4.  <span data-ttu-id="f0ab9-154">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-154">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="f0ab9-155">Come aggiungere un menu pubblicato a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-155">How to Add a Published Menu to a MED-V Workspace</span></span>


**<span data-ttu-id="f0ab9-156">Per aggiungere un menu pubblicato all'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-156">To add a published menu to the MED-V workspace</span></span>**

1.  <span data-ttu-id="f0ab9-157">Fare clic sull'area di lavoro MED-V per configurare.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-157">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="f0ab9-158">Nella sezione **menu pubblicati** del riquadro **applicazioni** fare clic su **Aggiungi** per aggiungere un nuovo menu.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-158">In the **Applications** pane, in the **Published Menus** section, click **Add** to add a new menu.</span></span>

3.  <span data-ttu-id="f0ab9-159">Configurare le proprietà del menu come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-159">Configure the menu properties as described in the following table.</span></span>

4.  <span data-ttu-id="f0ab9-160">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-160">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="f0ab9-161">Proprietà del menu pubblicato</span><span class="sxs-lookup"><span data-stu-id="f0ab9-161">Published Menu Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ab9-162">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0ab9-162">Property</span></span></th>
<th align="left"><span data-ttu-id="f0ab9-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ab9-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ab9-164">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f0ab9-164">Enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-165">Selezionare questa casella di controllo per abilitare il menu pubblicato.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-165">Select this check box to enable the published menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ab9-166">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="f0ab9-166">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-167">Il nome del collegamento nel menu Start di Windows dell'utente&#39;.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-167">The name of the shortcut in the user&#39;s Windows Start menu.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ab9-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0ab9-168">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-169">Descrizione, che viene visualizzata come descrizione comando quando l'utente&#39;il puntatore del mouse sul collegamento.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-169">The description, which appears as a tooltip when the user&#39;s mouse hovers over the shortcut.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ab9-170">Cartella nell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="f0ab9-170">Folder in workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ab9-171">Selezionare la cartella da pubblicare come menu contenente tutte le applicazioni all'interno della cartella.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-171">Select the folder to publish as a menu containing all the applications within the folder.</span></span></p>
<p><span data-ttu-id="f0ab9-172">Il testo visualizzato è un percorso relativo dalla cartella programmi.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-172">The text displayed is a relative path from the Programs folder.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f0ab9-173">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-173">Note</span></span></strong><br/><p><span data-ttu-id="f0ab9-174">Se lasciato vuoto, tutti i programmi nell'host verranno pubblicati come menu.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-174">If left blank, all programs on the host will be published as a menu.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f0ab9-175">Tutti i menu pubblicati vengono visualizzati come tasti di scelta rapida nel menu **Start** di Windows (**avviare &gt; tutte &gt; le applicazioni programmi MED-V**).</span><span class="sxs-lookup"><span data-stu-id="f0ab9-175">All published menus appear as shortcuts in the Windows **Start** menu (**Start &gt;All Programs&gt; MED-V Applications**).</span></span> <span data-ttu-id="f0ab9-176">È possibile modificare il nome del collegamento nel campo della **cartella scelte rapide dal menu Start** .</span><span class="sxs-lookup"><span data-stu-id="f0ab9-176">You can change the name of the shortcut in the **Start-menu shortcuts folder** field.</span></span>

**<span data-ttu-id="f0ab9-177">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-177">Note</span></span>**  
<span data-ttu-id="f0ab9-178">Quando si configurano due aree di lavoro MED-V, è consigliabile configurare un nome diverso per la cartella collegamenti al menu Start.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-178">When configuring two MED-V workspaces, it is recommended to configure a different name for the Start menu shortcuts folder.</span></span>



## <span data-ttu-id="f0ab9-179">Come rimuovere un menu pubblicato da un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-179">How to Remove a Published Menu from a MED-V Workspace</span></span>


**<span data-ttu-id="f0ab9-180">Per rimuovere un menu pubblicato da un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-180">To remove a published menu from a MED-V workspace</span></span>**

1.  <span data-ttu-id="f0ab9-181">Fare clic su un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-181">Click a MED-V workspace.</span></span>

2.  <span data-ttu-id="f0ab9-182">Nella sezione **menu pubblicati** del riquadro **applicazioni** selezionare un menu da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-182">In the **Applications** pane, in the **Published Menus** section, select a menu to remove.</span></span>

3.  <span data-ttu-id="f0ab9-183">Fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-183">Click **Remove**.</span></span>

    <span data-ttu-id="f0ab9-184">Il menu viene rimosso dall'elenco dei menu pubblicati.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-184">The menu is removed from the list of published menus.</span></span>

4.  <span data-ttu-id="f0ab9-185">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-185">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="f0ab9-186">Eseguire un'applicazione pubblicata da una riga di comando nel client</span><span class="sxs-lookup"><span data-stu-id="f0ab9-186">Running a Published Application from a Command Line on the Client</span></span>


<span data-ttu-id="f0ab9-187">L'amministratore può eseguire le applicazioni pubblicate da qualsiasi posizione, ad esempio un collegamento sul desktop, usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f0ab9-187">The administrator can run published applications from any location, such as a desktop shortcut, using the following command:</span></span>

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**<span data-ttu-id="f0ab9-188">Nota</span><span class="sxs-lookup"><span data-stu-id="f0ab9-188">Note</span></span>**  
<span data-ttu-id="f0ab9-189">L'area di lavoro MED-V in cui è definita l'applicazione pubblicata deve essere in corso.</span><span class="sxs-lookup"><span data-stu-id="f0ab9-189">The MED-V workspace in which the published application is defined must be running.</span></span>



## <span data-ttu-id="f0ab9-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0ab9-190">Related topics</span></span>


[<span data-ttu-id="f0ab9-191">Come modificare un'applicazione pubblicata con le impostazioni avanzate</span><span class="sxs-lookup"><span data-stu-id="f0ab9-191">How to Edit a Published Application with Advanced Settings</span></span>](how-to-edit-a-published-application-with-advanced-settings.md)

[<span data-ttu-id="f0ab9-192">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="f0ab9-192">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="f0ab9-193">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="f0ab9-193">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









