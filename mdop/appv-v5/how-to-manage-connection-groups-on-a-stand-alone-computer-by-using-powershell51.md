---
title: Come gestire i gruppi di connessione in un computer autonomo con PowerShell
description: Come gestire i gruppi di connessione in un computer autonomo con PowerShell
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805314"
---
# <span data-ttu-id="2aa79-103">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="2aa79-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="2aa79-104">Un gruppo di connessioni App-V consente di eseguire tutte le applicazioni virtuali come set di pacchetti definiti in un unico ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aa79-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="2aa79-105">Ad esempio, puoi virtualizzare un'applicazione e i relativi plug-in usando pacchetti distinti, ma eseguirli insieme in un singolo gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="2aa79-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="2aa79-106">Un file XML del gruppo di connessioni definisce il gruppo di connessioni eseguito nel computer in cui è stato installato il client App-V.</span><span class="sxs-lookup"><span data-stu-id="2aa79-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="2aa79-107">Per informazioni sul file XML del gruppo di connessioni e su come configurarlo, vedere [informazioni sul file del gruppo di connessioni](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="2aa79-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

<span data-ttu-id="2aa79-108">In questo argomento vengono illustrate le procedure seguenti:</span><span class="sxs-lookup"><span data-stu-id="2aa79-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="2aa79-109">Per aggiungere e pubblicare i pacchetti App-V nel gruppo connessione</span><span class="sxs-lookup"><span data-stu-id="2aa79-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="2aa79-110">Per aggiungere e abilitare il gruppo di connessioni nel client App-V</span><span class="sxs-lookup"><span data-stu-id="2aa79-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="2aa79-111">Per abilitare o disabilitare un gruppo di connessioni per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="2aa79-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="2aa79-112">Per consentire solo agli amministratori di abilitare i gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="2aa79-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a><span data-ttu-id="2aa79-113">*Per aggiungere e pubblicare i pacchetti App-V nel gruppo connessione*\*</span><span class="sxs-lookup"><span data-stu-id="2aa79-113">*To add and publish the App-V packages in the connection group*\*</span></span>

1.  <span data-ttu-id="2aa79-114">Per aggiungere e pubblicare i pacchetti App-V 5,1 nel computer che gestisce il client App-V, digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2aa79-114">To add and publish the App-V 5.1 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="2aa79-115">Add-AppvClientPackage – path c:\\tmpstore\\quartfin.AppV | Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="2aa79-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="2aa79-116">Ripetere il **passaggio 1** di questa procedura per ogni pacchetto nel gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="2aa79-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="2aa79-117">Per aggiungere e abilitare il gruppo di connessioni nel client App-V</span><span class="sxs-lookup"><span data-stu-id="2aa79-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="2aa79-118">Aggiungere il gruppo di connessioni digitando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2aa79-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="2aa79-119">Add-AppvClientConnectionGroup – Path c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="2aa79-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="2aa79-120">Abilitare il gruppo di connessioni digitando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2aa79-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="2aa79-121">Enable-AppvClientConnectionGroup-Name "applicazioni finanziarie"</span><span class="sxs-lookup"><span data-stu-id="2aa79-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="2aa79-122">Quando nel computer di destinazione vengono eseguite tutte le applicazioni virtuali che si trovano nei pacchetti di membri, verranno eseguite all'interno dell'ambiente virtuale del gruppo di connessioni e saranno disponibili per tutte le applicazioni virtuali degli altri pacchetti del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="2aa79-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="2aa79-123">Per abilitare o disabilitare un gruppo di connessioni per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="2aa79-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="2aa79-124">Esaminare la descrizione e i requisiti dei parametri:</span><span class="sxs-lookup"><span data-stu-id="2aa79-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="2aa79-125">Il parametro consente a un amministratore di abilitare o disabilitare un gruppo di connessioni per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="2aa79-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="2aa79-126">Per usare questo parametro è necessario usare il pacchetto hotfix 5 o versioni successive di App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="2aa79-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="2aa79-127">Puoi eseguire questo cmdlet dalla sessione utente o amministratore.</span><span class="sxs-lookup"><span data-stu-id="2aa79-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="2aa79-128">Per usare il parametro è necessario avere effettuato l'accesso con le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="2aa79-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="2aa79-129">L'utente finale deve essere connesso.</span><span class="sxs-lookup"><span data-stu-id="2aa79-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="2aa79-130">Devi specificare l'identificatore di sicurezza (SID) dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="2aa79-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="2aa79-131">USA i cmdlet seguenti e Aggiungi il parametro facoltativo **-UserSID** , dove **-UserSID** rappresenta l'identificatore di sicurezza dell'utente finale (SID):</span><span class="sxs-lookup"><span data-stu-id="2aa79-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2aa79-132">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2aa79-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="2aa79-133">Esempi</span><span class="sxs-lookup"><span data-stu-id="2aa79-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2aa79-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="2aa79-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aa79-135">Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="2aa79-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2aa79-136">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="2aa79-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aa79-137">Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="2aa79-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="2aa79-138">Per consentire solo agli amministratori di abilitare i gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="2aa79-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="2aa79-139">Esaminare la descrizione e il requisito per l'uso di questo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2aa79-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="2aa79-140">Usa questo cmdlet e il parametro per configurare il client App-V per consentire solo agli amministratori (non agli utenti finali) di abilitare o disabilitare i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="2aa79-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="2aa79-141">Per usare questo cmdlet, è necessario utilizzare almeno App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="2aa79-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="2aa79-142">Eseguire il cmdlet e il parametro seguenti:</span><span class="sxs-lookup"><span data-stu-id="2aa79-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2aa79-143">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2aa79-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="2aa79-144">Parametro e valori</span><span class="sxs-lookup"><span data-stu-id="2aa79-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="2aa79-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="2aa79-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2aa79-146">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="2aa79-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2aa79-147">–RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="2aa79-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2aa79-148">0-falso</span><span class="sxs-lookup"><span data-stu-id="2aa79-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="2aa79-149">1-vero</span><span class="sxs-lookup"><span data-stu-id="2aa79-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="2aa79-150">Set-AppvClientConfiguration-RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="2aa79-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="2aa79-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2aa79-151">Related topics</span></span>


[<span data-ttu-id="2aa79-152">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2aa79-152">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="2aa79-153">Amministrazione di App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="2aa79-153">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









