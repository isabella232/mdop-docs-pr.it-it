---
title: Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto
description: Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805368"
---
# <span data-ttu-id="11e38-103">Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="11e38-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="11e38-104">Microsoft Application Virtualization (App-V) 5,0 SP3 consente di configurare un gruppo di connessioni per l'uso di una versione qualsiasi di un pacchetto, semplificando gli aggiornamenti dei pacchetti e riducendo il numero di gruppi di connessione che è necessario creare.</span><span class="sxs-lookup"><span data-stu-id="11e38-104">Microsoft Application Virtualization (App-V) 5.0 SP3 enables you to configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="11e38-105">Per aggiornare un pacchetto nelle versioni precedenti di App-V, è necessario eseguire diversi passaggi, tra cui la disabilitazione del gruppo di connessioni e la modifica del file di definizione XML del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="11e38-105">To upgrade a package in earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11e38-106">Descrizione delle attività con App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="11e38-106">Task description with App-V 5.0 SP3</span></span></th>
<th align="left"><span data-ttu-id="11e38-107">Come eseguire l'attività con App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="11e38-107">How to perform the task with App-V 5.0 SP3</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11e38-108">Puoi configurare un gruppo di connessioni per accettare qualsiasi versione di un pacchetto, che ti consente di aggiornare il pacchetto senza dover disabilitare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="11e38-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="11e38-109">Funzionamento della caratteristica:</span><span class="sxs-lookup"><span data-stu-id="11e38-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="11e38-110">Se il gruppo di connessioni ha accesso a più versioni di un pacchetto, viene usata la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="11e38-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="11e38-111">Se il gruppo di connessioni contiene un pacchetto facoltativo con una versione non corretta, il pacchetto viene ignorato e non bloccherà l'ambiente virtuale del gruppo di connessioni da creare.</span><span class="sxs-lookup"><span data-stu-id="11e38-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="11e38-112">Se il gruppo di connessioni contiene un pacchetto non facoltativo con una versione non corretta, non è possibile creare l'ambiente virtuale del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="11e38-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11e38-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="11e38-113">Method</span></span></th>
<th align="left"><span data-ttu-id="11e38-114">Passaggi</span><span class="sxs-lookup"><span data-stu-id="11e38-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11e38-115">App-V Server-Console di gestione</span><span class="sxs-lookup"><span data-stu-id="11e38-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="11e38-116">Nella console di gestione selezionare <strong> pacchetti di </strong> &gt; <strong> connessione gruppi </strong> .</span><span class="sxs-lookup"><span data-stu-id="11e38-116">In the Management Console, select <strong>PACKAGES</strong> &gt; <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="11e38-117">Selezionare il gruppo di connessioni corretto dalla raccolta gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="11e38-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="11e38-118">Fare clic su <strong> modifica </strong> nel riquadro pacchetti connessi.</span><span class="sxs-lookup"><span data-stu-id="11e38-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="11e38-119">Selezionare <strong> </strong> la casella di controllo Usa qualsiasi versione accanto al nome del pacchetto e fare clic su <strong> Applica </strong> .</span><span class="sxs-lookup"><span data-stu-id="11e38-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="11e38-120">Per altre informazioni sull'aggiunta o l'aggiornamento di pacchetti, vedere <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> come aggiungere o aggiornare pacchetti tramite la console di gestione </a> .</span><span class="sxs-lookup"><span data-stu-id="11e38-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11e38-121">Client App-V in un computer autonomo</span><span class="sxs-lookup"><span data-stu-id="11e38-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="11e38-122">Creare il documento XML del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="11e38-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="11e38-123">Per aggiornare il pacchetto, imposta l' <strong> </strong> attributo di tag del pacchetto <strong> VersionId </strong> su un asterisco ( <strong>\*</strong> ).</span><span class="sxs-lookup"><span data-stu-id="11e38-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="11e38-124">Utilizzare il cmdlet seguente per aggiungere il gruppo di connessioni e includere il percorso del documento XML del gruppo di connessioni:</span><span class="sxs-lookup"><span data-stu-id="11e38-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="11e38-125">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="11e38-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="11e38-126">Quando si aggiorna un pacchetto, usare i cmdlet seguenti per rimuovere il pacchetto precedente, aggiungere il pacchetto aggiornato e pubblicare il pacchetto aggiornato:</span><span class="sxs-lookup"><span data-stu-id="11e38-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="11e38-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="11e38-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="11e38-128">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="11e38-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="11e38-129">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="11e38-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="11e38-130">Per altre informazioni, vedi:</span><span class="sxs-lookup"><span data-stu-id="11e38-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="11e38-131">File XML di esempio, <strong> file XML del gruppo di connessioni con pacchetti facoltativi </strong> , in questa sezione: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> come usare i pacchetti facoltativi nei gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="11e38-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="11e38-132">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="11e38-132">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="11e38-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11e38-133">Related topics</span></span>


[<span data-ttu-id="11e38-134">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="11e38-134">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





