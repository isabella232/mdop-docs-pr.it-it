---
title: Come distribuire pacchetti App-V 5.0 usando una soluzione di distribuzione elettronica del software
description: Come distribuire pacchetti App-V 5.0 usando una soluzione di distribuzione elettronica del software
author: dansimp
ms.assetid: 08e5e05b-dbb8-4be7-b2d8-721ef627da81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 33af02c5e9fad7408f9719ecd1a7fa90eacfeb29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805541"
---
# <span data-ttu-id="88d2c-103">Come distribuire pacchetti App-V 5.0 usando una soluzione di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="88d2c-103">How to deploy App-V 5.0 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="88d2c-104">Puoi usare un sistema ESD (Electronic Software Distribution) per distribuire le applicazioni virtuali App-V 5,0 ai client App-V.</span><span class="sxs-lookup"><span data-stu-id="88d2c-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.0 virtual applications to App-V clients.</span></span> <span data-ttu-id="88d2c-105">Per informazioni dettagliate, vedere la documentazione disponibile con l'ESD in uso.</span><span class="sxs-lookup"><span data-stu-id="88d2c-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="88d2c-106">Per i requisiti e le opzioni per i componenti per l'uso di un ESD per distribuire pacchetti App-V, vedere Pianificazione della distribuzione [di App-v 5,0 con un sistema di distribuzione elettronica del software](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="88d2c-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.0 with an Electronic Software Distribution System](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="88d2c-107">Usa uno dei metodi seguenti per pubblicare i pacchetti in computer client App-V con un ESD:</span><span class="sxs-lookup"><span data-stu-id="88d2c-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="88d2c-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="88d2c-108">Method</span></span></th>
<th align="left"><span data-ttu-id="88d2c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88d2c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="88d2c-110">Funzionalità fornite da un ESD di terze parti</span><span class="sxs-lookup"><span data-stu-id="88d2c-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="88d2c-111">Usare la funzionalità in un ESD di terze parti.</span><span class="sxs-lookup"><span data-stu-id="88d2c-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="88d2c-112">Windows Installer autonomo</span><span class="sxs-lookup"><span data-stu-id="88d2c-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="88d2c-113">Installare l'applicazione nel computer client di destinazione usando il file di Windows Installer (MSI) associato creato quando si sequenzia inizialmente un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="88d2c-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="88d2c-114">Il file di Windows Installer contiene le informazioni relative ai file del pacchetto App-V 5,0 usate per configurare un pacchetto e copia i file di pacchetto necessari nel client.</span><span class="sxs-lookup"><span data-stu-id="88d2c-114">The Windows Installer file contains the associated App-V 5.0 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="88d2c-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="88d2c-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="88d2c-116">Usare i cmdlet di PowerShell per distribuire applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="88d2c-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="88d2c-117">Per altre informazioni sull'uso di PowerShell e App-V 5,0, vedere <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)"> amministrazione di App-v tramite PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="88d2c-117">For more information about using PowerShell and App-V 5.0, see <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)">Administering App-V by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="88d2c-118">Per distribuire i pacchetti App-V 5,0 usando un ESD</span><span class="sxs-lookup"><span data-stu-id="88d2c-118">To deploy App-V 5.0 packages by using an ESD</span></span>**

1.  <span data-ttu-id="88d2c-119">Installare il sequencer App-V 5,0 in un computer nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="88d2c-119">Install the App-V 5.0 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="88d2c-120">Per altre informazioni sull'installazione del sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="88d2c-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="88d2c-121">Usare il sequencer App-V 5,0 per creare un'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="88d2c-121">Use the App-V 5.0 Sequencer to create virtual application.</span></span> <span data-ttu-id="88d2c-122">Per informazioni sulla creazione di un'applicazione virtuale, vedere [creazione e gestione di applicazioni virtualizzate App-V 5,0](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="88d2c-122">For information about creating a virtual application, see [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="88d2c-123">Dopo aver creato l'applicazione virtuale, distribuire il pacchetto usando la soluzione ESD.</span><span class="sxs-lookup"><span data-stu-id="88d2c-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="88d2c-124">Se si usa System Center Configuration Manager, iniziare rivedendo [Introduzione alla gestione delle applicazioni in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) per informazioni sull'uso di App-V 5,0 e System Center2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="88d2c-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.0 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="88d2c-125">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="88d2c-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="88d2c-126">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="88d2c-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="88d2c-127">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="88d2c-127">Got an App-V issue?</span></span>** <span data-ttu-id="88d2c-128">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="88d2c-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="88d2c-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88d2c-129">Related topics</span></span>


[<span data-ttu-id="88d2c-130">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="88d2c-130">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





