---
title: Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente
description: Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente
author: dansimp
ms.assetid: 851b8742-0283-4aa6-b3a3-f7f6289824c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 230e687360920c05a214624750eba54dc84b5731
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805673"
---
# <span data-ttu-id="9a6f3-103">Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente</span><span class="sxs-lookup"><span data-stu-id="9a6f3-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>


<span data-ttu-id="9a6f3-104">È possibile creare gruppi di connessioni autorizzati dall'utente che contengono sia i pacchetti pubblicati dall'utente che quelli pubblicati a livello globale, usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a6f3-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="9a6f3-105">Come usare i cmdlet di PowerShell per creare i gruppi di connessioni autorizzati dall'utente</span><span class="sxs-lookup"><span data-stu-id="9a6f3-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="9a6f3-106">Come usare app-V Server per creare i gruppi di connessioni autorizzati dall'utente</span><span class="sxs-lookup"><span data-stu-id="9a6f3-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="9a6f3-107">Informazioni da conoscere prima di iniziare:</span><span class="sxs-lookup"><span data-stu-id="9a6f3-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a6f3-108">Scenari non supportati e potenziali problemi</span><span class="sxs-lookup"><span data-stu-id="9a6f3-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="9a6f3-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="9a6f3-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a6f3-110">Non è possibile includere pacchetti pubblicati dall'utente in gruppi di connessioni autorizzati a livello globale.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a6f3-111">Il gruppo di connessioni avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a6f3-112">Se si pubblica un pacchetto a livello globale e quindi si crea un gruppo di connessioni pubblicato dall'utente in cui è stato reso non facoltativo il pacchetto, è comunque possibile eseguire <strong> il pacchetto Unpublish-AppvClientPackage &lt; &gt; -Global </strong> per annullare la pubblicazione del pacchetto, anche quando il pacchetto viene usato in un altro gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a6f3-113">Se un altro gruppo di connessioni usa il pacchetto, il pacchetto non riuscirà in questi gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="9a6f3-114">Per evitare di non pubblicare inavvertitamente un pacchetto non facoltativo usato in un altro gruppo di connessioni, è consigliabile tenere traccia dei gruppi di connessioni in cui è stato usato un pacchetto non facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="9a6f3-115">Come usare i cmdlet di PowerShell per creare gruppi di connessioni autorizzati dall'utente</span><span class="sxs-lookup"><span data-stu-id="9a6f3-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="9a6f3-116">Aggiungere e pubblicare pacchetti usando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a6f3-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="9a6f3-117">Add-AppvClientPackage package1 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="9a6f3-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="9a6f3-118">Add-AppvClientPackage Package2 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="9a6f3-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="9a6f3-119">Publish-AppvClientPackage-PackageId package1 \ _ID-VersionId package1 \ _Version ID-globale</span><span class="sxs-lookup"><span data-stu-id="9a6f3-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="9a6f3-120">Publish-AppvClientPackage-PackageId Package2 \ _ID-VersionIdPackage2 \ _ID</span><span class="sxs-lookup"><span data-stu-id="9a6f3-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="9a6f3-121">Creare il file XML del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-121">Create the connection group XML file.</span></span> <span data-ttu-id="9a6f3-122">Per altre informazioni, vedere [informazioni sul file del gruppo di connessioni](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="9a6f3-122">For more information, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

3.  <span data-ttu-id="9a6f3-123">Aggiungere e pubblicare il gruppo di connessioni usando i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a6f3-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="9a6f3-124">Connessione Add-AppvClientConnectionGroup \ _Group \ _XML \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="9a6f3-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="9a6f3-125">Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="9a6f3-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="9a6f3-126">Come usare app-V Server per creare gruppi di connessioni autorizzati dall'utente</span><span class="sxs-lookup"><span data-stu-id="9a6f3-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="9a6f3-127">Aprire la console di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-127">Open the App-V 5.1 Management Console.</span></span>

2.  <span data-ttu-id="9a6f3-128">Seguire le istruzioni fornite in [come pubblicare un pacchetto usando la console di gestione](how-to-publish-a-package-by-using-the-management-console-51.md) per pubblicare i pacchetti a livello globale e per l'utente.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="9a6f3-129">Seguire le istruzioni fornite in [come creare un gruppo di connessioni](how-to-create-a-connection-group51.md) per creare il gruppo di connessioni e aggiungere i pacchetti pubblicati dall'utente e a livello globale.</span><span class="sxs-lookup"><span data-stu-id="9a6f3-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group51.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="9a6f3-130">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="9a6f3-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9a6f3-131">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9a6f3-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9a6f3-132">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="9a6f3-132">Got an App-V issue?</span></span>** <span data-ttu-id="9a6f3-133">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9a6f3-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9a6f3-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a6f3-134">Related topics</span></span>


[<span data-ttu-id="9a6f3-135">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="9a6f3-135">Managing Connection Groups</span></span>](managing-connection-groups51.md)

[<span data-ttu-id="9a6f3-136">Come usare i pacchetti facoltativi nei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="9a6f3-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups51.md)

 

 





