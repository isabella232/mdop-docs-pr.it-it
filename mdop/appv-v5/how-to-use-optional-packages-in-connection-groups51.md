---
title: Come usare i pacchetti facoltativi nei gruppi di connessione
description: Come usare i pacchetti facoltativi nei gruppi di connessione
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805121"
---
# <span data-ttu-id="46e13-103">Come usare i pacchetti facoltativi nei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="46e13-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="46e13-104">A partire da Microsoft Application Virtualization (App-V) 5,0 SP3, è possibile aggiungere pacchetti facoltativi ai gruppi di connessioni per semplificare la gestione dei gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="46e13-105">La tabella seguente riepiloga le attività che è possibile completare più facilmente con i pacchetti facoltativi e fornisce collegamenti alle istruzioni per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="46e13-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="46e13-106">**Nota** 
 **I pacchetti facoltativi non sono supportati nelle versioni precedenti a App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="46e13-106">**Note**
**Optional packages are not supported in releases prior to App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="46e13-107">Prima di usare pacchetti facoltativi, vedere [requisiti per l'uso di pacchetti facoltativi nei gruppi di connessioni](#bkmk-reqs-using-cg).</span><span class="sxs-lookup"><span data-stu-id="46e13-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46e13-108">Collegamento alle istruzioni</span><span class="sxs-lookup"><span data-stu-id="46e13-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="46e13-109">Attività</span><span class="sxs-lookup"><span data-stu-id="46e13-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="46e13-110">Usare un gruppo di connessioni, con pacchetti facoltativi, per più utenti con pacchetti diversi a cui hanno diritto</span><span class="sxs-lookup"><span data-stu-id="46e13-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="46e13-111">Usa un singolo gruppo di connessioni per creare diversi gruppi di applicazioni e plug-in disponibili per diversi utenti finali.</span><span class="sxs-lookup"><span data-stu-id="46e13-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="46e13-112">Ad esempio, si vuole distribuire Microsoft Office a tutti gli utenti finali, ma distribuire plug-in diversi a diversi sottoinsiemi di utenti.</span><span class="sxs-lookup"><span data-stu-id="46e13-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="46e13-113">Annullare la pubblicazione o eliminare un pacchetto facoltativo oppure annullare la pubblicazione di un pacchetto facoltativo e ripubblicarlo in un secondo momento senza modificare il gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="46e13-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="46e13-114">Annullare la pubblicazione, eliminare o ripubblicare un pacchetto facoltativo senza dover disabilitare, rimuovere, modificare, aggiungere e riattivare il gruppo di connessioni nel client App-V.</span><span class="sxs-lookup"><span data-stu-id="46e13-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="46e13-115">È anche possibile annullare la pubblicazione del pacchetto facoltativo e ripubblicarlo in un secondo momento senza dover disabilitare o ripubblicare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="46e13-116">Usare un gruppo di connessioni, con pacchetti facoltativi, per più utenti con pacchetti diversi a cui hanno diritto</span><span class="sxs-lookup"><span data-stu-id="46e13-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46e13-117">Descrizione attività</span><span class="sxs-lookup"><span data-stu-id="46e13-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="46e13-118">Come eseguire l'attività</span><span class="sxs-lookup"><span data-stu-id="46e13-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="46e13-119">Con App-V 5,0 SP3 e App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="46e13-119">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="46e13-120">È possibile aggiungere pacchetti facoltativi ai gruppi di connessioni, che consente di specificare combinazioni diverse di applicazioni e plug-in per diversi utenti finali.</span><span class="sxs-lookup"><span data-stu-id="46e13-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="46e13-121">Esempio </strong> : si vuole distribuire Microsoft Office agli utenti finali, ma abilitare un determinato plug-in solo per un sottoinsieme di utenti.</span><span class="sxs-lookup"><span data-stu-id="46e13-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="46e13-122">A questo scopo, crea un gruppo di connessioni che contiene un pacchetto con Office e un altro pacchetto con plug-in di Office e quindi rendi facoltativo il pacchetto plug-in.</span><span class="sxs-lookup"><span data-stu-id="46e13-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="46e13-123">Gli utenti finali che non hanno diritto al pacchetto di plug-in saranno comunque in grado di eseguire Office.</span><span class="sxs-lookup"><span data-stu-id="46e13-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46e13-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="46e13-124">Method</span></span></th>
<th align="left"><span data-ttu-id="46e13-125">Passaggi</span><span class="sxs-lookup"><span data-stu-id="46e13-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46e13-126">App-V Server-Console di gestione</span><span class="sxs-lookup"><span data-stu-id="46e13-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="46e13-127">Nella console di gestione selezionare <strong> gruppi di connessioni </strong> per visualizzare la raccolta gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-127">In the Management Console, select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="46e13-128">Selezionare il gruppo di connessioni corretto dalla raccolta gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-128">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="46e13-129">Fare clic su <strong> modifica </strong> nel riquadro pacchetti connessi.</span><span class="sxs-lookup"><span data-stu-id="46e13-129">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="46e13-130">Selezionare <strong> facoltativo </strong> accanto al nome del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="46e13-130">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="46e13-131">Selezionare la <strong> casella di controllo Aggiungi pacchetto Access to Group Access </strong> .</span><span class="sxs-lookup"><span data-stu-id="46e13-131">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="46e13-132">Questo passaggio necessario aggiunge al gruppo di connessioni i diritti di pacchetto configurati in precedenza quando si assegnavano pacchetti a gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46e13-132">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46e13-133">App-V Server-cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="46e13-133">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="46e13-134">Usa il cmdlet seguente e specifica il <strong> parametro-Optional </strong> :</span><span class="sxs-lookup"><span data-stu-id="46e13-134">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="46e13-135">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="46e13-135">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="46e13-136">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46e13-136">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="46e13-137">Esempio:</span><span class="sxs-lookup"><span data-stu-id="46e13-137">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46e13-138">Client App-V in un computer autonomo</span><span class="sxs-lookup"><span data-stu-id="46e13-138">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="46e13-139">Creare il documento XML del gruppo di connessioni e impostare <strong> l' </strong> attributo di tag del pacchetto <strong> </strong> su <strong> "true".</span><span class="sxs-lookup"><span data-stu-id="46e13-139">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="46e13-140">Usare i cmdlet seguenti per aggiungere e abilitare il gruppo di connessioni:</span><span class="sxs-lookup"><span data-stu-id="46e13-140">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="46e13-141">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="46e13-141">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="46e13-142">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="46e13-142">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="46e13-143">Esempio di documento XML del gruppo di connessioni con pacchetti facoltativi:</span><span class="sxs-lookup"><span data-stu-id="46e13-143">Example connection group XML document with optional packages:</span></span></strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="46e13-144">Versioni precedenti all'App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="46e13-144">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="46e13-145">È stato necessario creare molti gruppi di connessioni per rendere disponibili le combinazioni di applicazioni e plug-in specifiche per gli utenti specifici.</span><span class="sxs-lookup"><span data-stu-id="46e13-145">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="46e13-146">Annullare la pubblicazione o eliminare un pacchetto facoltativo oppure annullare la pubblicazione di un pacchetto facoltativo e ripubblicarlo in un secondo momento senza modificare il gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="46e13-146">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46e13-147">Descrizione attività</span><span class="sxs-lookup"><span data-stu-id="46e13-147">Task description</span></span></th>
<th align="left"><span data-ttu-id="46e13-148">Come eseguire l'attività</span><span class="sxs-lookup"><span data-stu-id="46e13-148">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="46e13-149">Con App-V 5,0 SP3 e App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="46e13-149">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="46e13-150">È possibile annullare la pubblicazione, eliminare o ripubblicare un pacchetto facoltativo, che si trova in un gruppo di connessioni, senza dover disabilitare o riabilitare il gruppo di connessioni nel client App-V.</span><span class="sxs-lookup"><span data-stu-id="46e13-150">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="46e13-151">È anche possibile annullare la pubblicazione di un pacchetto facoltativo e ripubblicarlo in un secondo momento senza dover disabilitare o ripubblicare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-151">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="46e13-152">Esempio </strong> : se si pubblica un pacchetto facoltativo che contiene un plug-in di Microsoft Office e si vuole rimuovere il plug-in, è possibile annullare la pubblicazione del pacchetto senza dover disabilitare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-152">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46e13-153">Metodo</span><span class="sxs-lookup"><span data-stu-id="46e13-153">Method</span></span></th>
<th align="left"><span data-ttu-id="46e13-154">Passaggi</span><span class="sxs-lookup"><span data-stu-id="46e13-154">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46e13-155">App-V Server-Console di gestione</span><span class="sxs-lookup"><span data-stu-id="46e13-155">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="46e13-156">Per annullare la pubblicazione del pacchetto: nella console di gestione selezionare elegge la <strong> </strong> pagina pacchetti, fare clic o fare clic con il pulsante destro del mouse sul pacchetto che si vuole annullare la pubblicazione e quindi fare clic su <strong> Annulla pubblicazione </strong> .</span><span class="sxs-lookup"><span data-stu-id="46e13-156">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, click or right-click the package that you want to unpublish, and click <strong>Unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="46e13-157">Per rimuovere un pacchetto facoltativo da un gruppo di connessioni: nella <strong> pagina gruppi di connessioni </strong> selezionare il pacchetto che si vuole rimuovere e fare clic sulla freccia destra per rimuovere il pacchetto dal riquadro del gruppo di connessioni in basso a sinistra.</span><span class="sxs-lookup"><span data-stu-id="46e13-157">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46e13-158">Client App-V in un computer autonomo</span><span class="sxs-lookup"><span data-stu-id="46e13-158">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="46e13-159">Usare i cmdlet esistenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="46e13-159">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="46e13-160">Annulla pubblicazione-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="46e13-160">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="46e13-161">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="46e13-161">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="46e13-162">Per altre informazioni, vedere <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> come gestire i pacchetti App-V 5,1 in uso in un computer autonomo usando PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="46e13-162">For more information, see <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="46e13-163">Versioni precedenti all'App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="46e13-163">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="46e13-164">È necessario:</span><span class="sxs-lookup"><span data-stu-id="46e13-164">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="46e13-165">Rimuovere il gruppo di connessioni da ogni computer client App-V in cui è stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="46e13-165">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="46e13-166">Annullare la pubblicazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="46e13-166">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="46e13-167">Rimuovere il pacchetto dalla definizione del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-167">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="46e13-168">Ripubblicare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-168">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="46e13-169">Requisiti per l'uso di pacchetti facoltativi nei gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="46e13-169">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="46e13-170">Verificare i requisiti seguenti prima di usare pacchetti facoltativi nei gruppi di connessioni:</span><span class="sxs-lookup"><span data-stu-id="46e13-170">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46e13-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e13-171">Requirement</span></span></th>
<th align="left"><span data-ttu-id="46e13-172">Dettagli</span><span class="sxs-lookup"><span data-stu-id="46e13-172">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46e13-173">I gruppi di connessioni devono contenere almeno un pacchetto non facoltativo.</span><span class="sxs-lookup"><span data-stu-id="46e13-173">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="46e13-174">Verificare attentamente che soddisfi questo requisito, poiché il server App-V e il cmdlet di PowerShell non convalidano che il requisito sia stato soddisfatto.</span><span class="sxs-lookup"><span data-stu-id="46e13-174">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="46e13-175">Se si crea accidentalmente un gruppo di connessioni che non contiene almeno un pacchetto non facoltativo e l'utente finale prova ad aprire un'applicazione di pacchetto in tale gruppo di connessioni, il gruppo di connessioni non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="46e13-175">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="46e13-176">I gruppi di connessioni pubblicati dall'utente possono contenere pacchetti pubblicati a livello globale o per l'utente.</span><span class="sxs-lookup"><span data-stu-id="46e13-176">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="46e13-177">I gruppi di connessioni pubblicati globalmente devono contenere solo pacchetti pubblicati globalmente.</span><span class="sxs-lookup"><span data-stu-id="46e13-177">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="46e13-178">I gruppi di connessioni pubblicati globalmente devono contenere pacchetti pubblicati globalmente per verificare che i pacchetti siano disponibili all'avvio dell'ambiente virtuale del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="46e13-178">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="46e13-179">Se si tenta di aggiungere o abilitare gruppi di connessioni pubblicati a livello globale che contengono pacchetti pubblicati dall'utente, il gruppo di connessioni non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="46e13-179">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46e13-180">È necessario pubblicare tutti i pacchetti non facoltativi prima di pubblicare il gruppo di connessioni che contiene questi pacchetti.</span><span class="sxs-lookup"><span data-stu-id="46e13-180">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="46e13-181">L'ambiente virtuale di un gruppo di connessioni non può essere avviato se mancano pacchetti non facoltativi.</span><span class="sxs-lookup"><span data-stu-id="46e13-181">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="46e13-182">Il client App-V non riesce ad aggiungere o abilitare un gruppo di connessioni se i pacchetti non facoltativi non sono stati pubblicati.</span><span class="sxs-lookup"><span data-stu-id="46e13-182">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46e13-183">Prima di annullare la pubblicazione di un pacchetto pubblicato a livello globale, verificare che i gruppi di connessioni che hanno diritto a tutti gli utenti del computer non richiedano più il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="46e13-183">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="46e13-184">Il sistema non controlla se il pacchetto fa parte del gruppo di connessioni di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="46e13-184">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="46e13-185">L'annullamento della pubblicazione di un pacchetto globale lo rende non disponibile per tutti gli utenti del computer, quindi assicurati che i gruppi di connessioni di ogni utente non contengano più il pacchetto o in alternativa Rendi il pacchetto facoltativo.</span><span class="sxs-lookup"><span data-stu-id="46e13-185">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="46e13-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46e13-186">Related topics</span></span>


[<span data-ttu-id="46e13-187">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="46e13-187">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





