---
title: Come installare Sequencer
description: Come installare Sequencer
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805362"
---
# <span data-ttu-id="26bcc-103">Come installare Sequencer</span><span class="sxs-lookup"><span data-stu-id="26bcc-103">How to Install the Sequencer</span></span>


<span data-ttu-id="26bcc-104">Usare la procedura seguente per installare il sequencer di Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="26bcc-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="26bcc-105">Il computer in cui viene eseguito il sequencer non deve eseguire alcuna versione del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="26bcc-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="26bcc-106">L'aggiornamento di un'installazione precedente di App-V Sequencer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="26bcc-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="26bcc-107">**Importante**  Per un elenco completo dei requisiti del sequencer, Vedi le sezioni sequencer dei [prerequisiti App-v 5,0](app-v-50-prerequisites.md) e delle [configurazioni supportate in app-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="26bcc-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="26bcc-108">È anche possibile usare la riga di comando per installare l'App-V 5,0 sequencer.</span><span class="sxs-lookup"><span data-stu-id="26bcc-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="26bcc-109">Nell'elenco seguente vengono visualizzate informazioni sulle opzioni per l'installazione del sequencer tramite la riga di comando e **appv\_sequencer\_setup.exe**:</span><span class="sxs-lookup"><span data-stu-id="26bcc-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26bcc-110">Comando</span><span class="sxs-lookup"><span data-stu-id="26bcc-110">Command</span></span></th>
<th align="left"><span data-ttu-id="26bcc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26bcc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26bcc-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="26bcc-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-113">Specifica la directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="26bcc-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26bcc-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="26bcc-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-115">Consente la partecipazione al programma Microsoft Customer Experience Improvement.</span><span class="sxs-lookup"><span data-stu-id="26bcc-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26bcc-116">/Log</span><span class="sxs-lookup"><span data-stu-id="26bcc-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-117">Specifica dove verrà salvato il log di installazione, la posizione predefinita è <strong> % temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="26bcc-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="26bcc-118">Ad esempio, <strong> C:\ </strong>Log log. log.</span><span class="sxs-lookup"><span data-stu-id="26bcc-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26bcc-119">/nocancel/q</span><span class="sxs-lookup"><span data-stu-id="26bcc-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-120">Specifica un'installazione silenziosa o silenziosa.</span><span class="sxs-lookup"><span data-stu-id="26bcc-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26bcc-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="26bcc-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-122">Specifica la rimozione del sequencer.</span><span class="sxs-lookup"><span data-stu-id="26bcc-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26bcc-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="26bcc-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-124">Accetta il contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="26bcc-124">Accepts the license agreement.</span></span> <span data-ttu-id="26bcc-125">Questa operazione è necessaria per un'installazione automatica.</span><span class="sxs-lookup"><span data-stu-id="26bcc-125">This is required for an unattended installation.</span></span> <span data-ttu-id="26bcc-126">Esempio di utilizzo: <strong> /AcceptEula </strong> o <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="26bcc-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26bcc-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="26bcc-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-128">Specifica l'azione di layout associata.</span><span class="sxs-lookup"><span data-stu-id="26bcc-128">Specifies the associated layout action.</span></span> <span data-ttu-id="26bcc-129">Estrae anche Windows Installer (. msi) e i file di script in una cartella senza installare App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="26bcc-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="26bcc-130">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="26bcc-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26bcc-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="26bcc-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-132">Specifica la directory del layout.</span><span class="sxs-lookup"><span data-stu-id="26bcc-132">Specifies the layout directory.</span></span> <span data-ttu-id="26bcc-133">Richiede un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="26bcc-133">Requires a string value.</span></span> <span data-ttu-id="26bcc-134">Esempio di utilizzo: <strong> /LAYOUTDIR = "client di virtualizzazione C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="26bcc-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26bcc-135">/?</span><span class="sxs-lookup"><span data-stu-id="26bcc-135">/?</span></span> <span data-ttu-id="26bcc-136">O/h o/Help</span><span class="sxs-lookup"><span data-stu-id="26bcc-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="26bcc-137">Visualizza la Guida associata.</span><span class="sxs-lookup"><span data-stu-id="26bcc-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="26bcc-138">Per installare l'App-V 5,0 sequencer</span><span class="sxs-lookup"><span data-stu-id="26bcc-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="26bcc-139">Copiare i file di installazione del sequencer App-V 5,0 nel computer in cui verrà installato.</span><span class="sxs-lookup"><span data-stu-id="26bcc-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="26bcc-140">Fare doppio clic **appv\_sequencer\_setup.exe** e quindi fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="26bcc-141">Nella pagina **condizioni di licenza software** è necessario rivedere le condizioni di licenza.</span><span class="sxs-lookup"><span data-stu-id="26bcc-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="26bcc-142">Per accettare le condizioni di licenza selezionare **Accetto le condizioni di licenza.**</span><span class="sxs-lookup"><span data-stu-id="26bcc-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="26bcc-143">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-143">Click **Next**.</span></span>

3.  <span data-ttu-id="26bcc-144">In **usare Microsoft Update per semplificare la protezione e la pagina aggiornata del computer** per consentire agli aggiornamenti Microsoft selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="26bcc-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="26bcc-145">Per disabilitare l'applicazione degli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="26bcc-146">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-146">Click **Next**.</span></span>

4.  <span data-ttu-id="26bcc-147">Nella pagina del **programma Analisi utilizzo** software per partecipare al programma selezionare **partecipa al programma Analisi utilizzo**software.</span><span class="sxs-lookup"><span data-stu-id="26bcc-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="26bcc-148">Ciò consentirà di raccogliere informazioni su come si usa l'App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="26bcc-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="26bcc-149">Se non si vuole partecipare al programma, selezionare non si **vuole partecipare al programma in questo momento**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="26bcc-150">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-150">Click **Install**.</span></span>

5.  <span data-ttu-id="26bcc-151">Per aprire il sequencer, fare clic su **Start** e quindi su **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="26bcc-152">Per risolvere i problemi relativi all'installazione di sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="26bcc-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="26bcc-153">Per altre informazioni sull'installazione di Sequencer, è possibile visualizzare il log degli errori nella cartella **% Temp%** .</span><span class="sxs-lookup"><span data-stu-id="26bcc-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="26bcc-154">Per rivedere i file di log, fare clic sul pulsante **Start**, digitare **% Temp%** e quindi cercare il **log di appv\_**.</span><span class="sxs-lookup"><span data-stu-id="26bcc-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="26bcc-155">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="26bcc-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="26bcc-156">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="26bcc-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="26bcc-157">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="26bcc-157">Got an App-V issue?</span></span>** <span data-ttu-id="26bcc-158">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="26bcc-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="26bcc-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26bcc-159">Related topics</span></span>


[<span data-ttu-id="26bcc-160">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="26bcc-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 




