---
title: Come importare un'applicazione
description: Come importare un'applicazione
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817405"
---
# <span data-ttu-id="81319-103">Come importare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="81319-103">How to Import an Application</span></span>


<span data-ttu-id="81319-104">In genere si importano le applicazioni per renderle disponibili per lo streaming da un Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="81319-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="81319-105">È anche possibile aggiungere manualmente un'applicazione, ma è necessario specificare informazioni precise e dettagliate sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="81319-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="81319-106">Per altre informazioni, vedere [come aggiungere manualmente un'applicazione](how-to-manually-add-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="81319-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="81319-107">**Nota**  Per importare un'applicazione, è necessario che il file OSD (Open Software Descriptor) sequenziato o il file di progetto sequencer (SPRJ) sia disponibile nel server.</span><span class="sxs-lookup"><span data-stu-id="81319-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="81319-108">Quando si importa un'applicazione, è necessario assicurarsi che il server sia configurato con un valore nel campo **percorso di contenuto predefinito** nella scheda **generale** della finestra di dialogo **Opzioni di sistema** (accessibile facendo clic con il pulsante destro del mouse sul nodo **Application Virtualization System** nella console App-V Server).</span><span class="sxs-lookup"><span data-stu-id="81319-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="81319-109">Il valore predefinito del percorso di contenuto definisce la posizione in cui verranno importate le applicazioni e durante il processo di importazione questo valore viene usato per modificare i percorsi definiti nel file OSD per il file SFT e per le scelte rapide da icona.</span><span class="sxs-lookup"><span data-stu-id="81319-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="81319-110">Nel file OSD, il percorso del file SFT viene specificato nella voce CODEBASE HREF e il percorso per le icone viene specificato nella voce di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="81319-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="81319-111">Durante il processo di importazione, il protocollo, il server e, se presente, la porta specificata in questi due percorsi nel file OSD verranno sostituiti con il valore del percorso di contenuto predefinito.</span><span class="sxs-lookup"><span data-stu-id="81319-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="81319-112">La tabella seguente contiene un esempio di come verrà influenzato il percorso di importazione.</span><span class="sxs-lookup"><span data-stu-id="81319-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81319-113">Percorso di contenuto predefinito</span><span class="sxs-lookup"><span data-stu-id="81319-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="81319-114">File OSD CODEBASE HREF</span><span class="sxs-lookup"><span data-stu-id="81319-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="81319-115">Valore risultante</span><span class="sxs-lookup"><span data-stu-id="81319-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81319-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="81319-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="81319-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="81319-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="81319-118">Per importare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="81319-118">To import an application</span></span>**

1.  <span data-ttu-id="81319-119">Fare clic con il pulsante destro del mouse sul nodo **applicazioni** nel riquadro sinistro e scegliere **Importa applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="81319-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="81319-120">Nella finestra di dialogo **Apri** passare al file SPRJ o OSD dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="81319-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="81319-121">Evidenziare il file e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="81319-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="81319-122">Nella **creazione guidata nuova applicazione**verificare che la casella **abilitato** sia selezionata per le applicazioni che si desidera eseguire il flusso.</span><span class="sxs-lookup"><span data-stu-id="81319-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="81319-123">È anche possibile immettere una descrizione e verificare il server e i percorsi dei file.</span><span class="sxs-lookup"><span data-stu-id="81319-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="81319-124">Inoltre, se è stata configurata la licenza e i gruppi di server, è possibile selezionarli.</span><span class="sxs-lookup"><span data-stu-id="81319-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="81319-125">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="81319-125">Click **Next**.</span></span>

5.  <span data-ttu-id="81319-126">Nella schermata **collegamenti pubblicati** selezionare le caselle relative alle posizioni in cui si desidera visualizzare i tasti di scelta rapida dell'applicazione nei computer client.</span><span class="sxs-lookup"><span data-stu-id="81319-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="81319-127">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="81319-127">Click **Next**.</span></span>

7.  <span data-ttu-id="81319-128">Nella schermata **associazioni di file** è possibile aggiungere nuove associazioni di file a questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="81319-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="81319-129">A tale scopo, fare clic su **Aggiungi**, immettere l'estensione (senza un punto precedente), immettere una descrizione e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="81319-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="81319-130">**Nota**  Le applicazioni sequenziate con sequencer 4,0 popolano la finestra di dialogo **associazioni di file** quando vengono importate o create tramite la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="81319-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="81319-131">Le applicazioni con i pacchetti di versioni precedenti di Sequencer non lo fanno.</span><span class="sxs-lookup"><span data-stu-id="81319-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="81319-132">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="81319-132">Click **Next**.</span></span>

9.  <span data-ttu-id="81319-133">Nella schermata **autorizzazioni di accesso** fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="81319-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="81319-134">Completare la finestra di dialogo **Seleziona gruppi** .</span><span class="sxs-lookup"><span data-stu-id="81319-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="81319-135">Al termine, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="81319-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="81319-136">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="81319-136">Click **Next**.</span></span>

12. <span data-ttu-id="81319-137">Nella schermata **Riepilogo** è possibile rivedere le impostazioni di importazione.</span><span class="sxs-lookup"><span data-stu-id="81319-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="81319-138">Fare clic su **fine**oppure su **Torna** per cambiare l'importazione o fare clic su **Annulla** per annullare l'importazione.</span><span class="sxs-lookup"><span data-stu-id="81319-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="81319-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81319-139">Related topics</span></span>


[<span data-ttu-id="81319-140">Come gestire i gruppi di applicazioni in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="81319-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="81319-141">Come gestire le applicazioni in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="81319-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="81319-142">Come aggiungere manualmente un'applicazione</span><span class="sxs-lookup"><span data-stu-id="81319-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





