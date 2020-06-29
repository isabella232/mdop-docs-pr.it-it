---
title: Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell
description: Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805338"
---
# <span data-ttu-id="cbc97-103">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbc97-103">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="cbc97-104">Le sezioni seguenti spiegano come eseguire varie attività di gestione in un computer client autonomo usando PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cbc97-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="cbc97-105">Per restituire un elenco di pacchetti</span><span class="sxs-lookup"><span data-stu-id="cbc97-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="cbc97-106">Per aggiungere un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbc97-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="cbc97-107">Per pubblicare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbc97-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="cbc97-108">Per pubblicare un pacchetto in un utente specifico</span><span class="sxs-lookup"><span data-stu-id="cbc97-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="cbc97-109">Per aggiungere e pubblicare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbc97-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="cbc97-110">Per annullare la pubblicazione di un pacchetto esistente</span><span class="sxs-lookup"><span data-stu-id="cbc97-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="cbc97-111">Per annullare la pubblicazione di un pacchetto per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="cbc97-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="cbc97-112">Per rimuovere un pacchetto esistente</span><span class="sxs-lookup"><span data-stu-id="cbc97-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="cbc97-113">Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="cbc97-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="cbc97-114">Informazioni sui pacchetti in sospeso (UserPending e GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="cbc97-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="cbc97-115">Per restituire un elenco di pacchetti</span><span class="sxs-lookup"><span data-stu-id="cbc97-115">To return a list of packages</span></span>


<span data-ttu-id="cbc97-116">Usare le informazioni seguenti per restituire un elenco di pacchetti aventi diritto a un utente specifico:</span><span class="sxs-lookup"><span data-stu-id="cbc97-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="cbc97-117">**Cmdlet**: Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-118">**Parametri**:-name-version-PackageID-VersionId</span><span class="sxs-lookup"><span data-stu-id="cbc97-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="cbc97-119">**Esempio**: Get-AppvClientPackage-Name "ContosoApplication"-versione 2</span><span class="sxs-lookup"><span data-stu-id="cbc97-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="cbc97-120">Per aggiungere un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbc97-120">To add a package</span></span>


<span data-ttu-id="cbc97-121">Usare le informazioni seguenti per aggiungere un pacchetto a un computer.</span><span class="sxs-lookup"><span data-stu-id="cbc97-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="cbc97-122">**Importante**  Questo esempio aggiunge solo un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cbc97-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="cbc97-123">Il pacchetto non viene pubblicato nell'utente o nel computer.</span><span class="sxs-lookup"><span data-stu-id="cbc97-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="cbc97-124">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-125">**Esempio**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV</span><span class="sxs-lookup"><span data-stu-id="cbc97-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="cbc97-126">Per pubblicare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbc97-126">To publish a package</span></span>


<span data-ttu-id="cbc97-127">Usare le informazioni seguenti per pubblicare un pacchetto aggiunto a un utente specifico o a livello globale a qualsiasi utente nel computer.</span><span class="sxs-lookup"><span data-stu-id="cbc97-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbc97-128">Metodo di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="cbc97-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="cbc97-129">Cmdlet ed esempio</span><span class="sxs-lookup"><span data-stu-id="cbc97-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbc97-130">Pubblicazione per l'utente</span><span class="sxs-lookup"><span data-stu-id="cbc97-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="cbc97-131">Cmdlet </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="cbc97-132">Esempio </strong> : Publish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="cbc97-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbc97-133">Pubblicazione globale</span><span class="sxs-lookup"><span data-stu-id="cbc97-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="cbc97-134">Cmdlet </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="cbc97-135">Esempio </strong> : Publish-AppvClientPackage "ContosoApplication"-Global</span><span class="sxs-lookup"><span data-stu-id="cbc97-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="cbc97-136">Per pubblicare un pacchetto in un utente specifico</span><span class="sxs-lookup"><span data-stu-id="cbc97-136">To publish a package to a specific user</span></span>


<span data-ttu-id="cbc97-137">**Nota**  Per usare questo parametro è necessario usare il pacchetto hotfix 5 o versioni successive di App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="cbc97-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="cbc97-138">Un amministratore può pubblicare un pacchetto in un utente specifico specificando il parametro facoltativa- **UserSID** con il cmdlet **Publish-AppvClientPackage** , dove **-UserSID** rappresenta l'identificatore di sicurezza (SID) dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cbc97-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="cbc97-139">Per usare questo parametro:</span><span class="sxs-lookup"><span data-stu-id="cbc97-139">To use this parameter:</span></span>

-   <span data-ttu-id="cbc97-140">Puoi eseguire questo cmdlet dalla sessione utente o amministratore.</span><span class="sxs-lookup"><span data-stu-id="cbc97-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="cbc97-141">Per usare il parametro è necessario avere effettuato l'accesso con le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="cbc97-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="cbc97-142">L'utente finale deve essere connesso.</span><span class="sxs-lookup"><span data-stu-id="cbc97-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="cbc97-143">Devi specificare l'identificatore di sicurezza (SID) dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cbc97-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="cbc97-144">**Cmdlet**: Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-145">**Esempio**: Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="cbc97-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="cbc97-146">Per aggiungere e pubblicare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbc97-146">To add and publish a package</span></span>


<span data-ttu-id="cbc97-147">Usare le informazioni seguenti per aggiungere un pacchetto a un computer e pubblicarlo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="cbc97-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="cbc97-148">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-149">**Esempio**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="cbc97-150">Per annullare la pubblicazione di un pacchetto esistente</span><span class="sxs-lookup"><span data-stu-id="cbc97-150">To unpublish an existing package</span></span>


<span data-ttu-id="cbc97-151">Usare le informazioni seguenti per annullare la pubblicazione di un pacchetto autorizzato a un utente, ma non rimuovere il pacchetto dal computer.</span><span class="sxs-lookup"><span data-stu-id="cbc97-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="cbc97-152">**Cmdlet**: annullamento della pubblicazione-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-153">**Esempio**: Unpublish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="cbc97-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="cbc97-154">Per annullare la pubblicazione di un pacchetto per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="cbc97-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="cbc97-155">**Nota**  Per usare questo parametro è necessario usare il pacchetto hotfix 5 o versioni successive di App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="cbc97-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="cbc97-156">Un amministratore può annullare la pubblicazione di un pacchetto per un utente specifico usando il parametro facoltativo **-UserSID** con il cmdlet **Unpublish-AppvClientPackage** , dove **-UserSID** rappresenta l'identificatore di sicurezza (SID) dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cbc97-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="cbc97-157">Per usare questo parametro:</span><span class="sxs-lookup"><span data-stu-id="cbc97-157">To use this parameter:</span></span>

-   <span data-ttu-id="cbc97-158">Puoi eseguire questo cmdlet dalla sessione utente o amministratore.</span><span class="sxs-lookup"><span data-stu-id="cbc97-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="cbc97-159">Per usare il parametro è necessario avere effettuato l'accesso con le credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="cbc97-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="cbc97-160">L'utente finale deve essere connesso.</span><span class="sxs-lookup"><span data-stu-id="cbc97-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="cbc97-161">Devi specificare l'identificatore di sicurezza (SID) dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cbc97-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="cbc97-162">**Cmdlet**: annullamento della pubblicazione-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-163">**Esempio**: Unpublish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="cbc97-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="cbc97-164">Per rimuovere un pacchetto esistente</span><span class="sxs-lookup"><span data-stu-id="cbc97-164">To remove an existing package</span></span>


<span data-ttu-id="cbc97-165">Usare le informazioni seguenti per rimuovere un pacchetto dal computer.</span><span class="sxs-lookup"><span data-stu-id="cbc97-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="cbc97-166">**Cmdlet**: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="cbc97-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="cbc97-167">**Esempio**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="cbc97-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="cbc97-168">**Nota**  I cmdlet App-V sono stati assegnati alle variabili per gli esempi precedenti solo per motivi di chiarezza; l'assegnazione non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="cbc97-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="cbc97-169">La maggior parte dei cmdlet può essere combinata come visualizzata in [per aggiungere e pubblicare un pacchetto](#bkmk-add-pub-pkg-standalone-posh).</span><span class="sxs-lookup"><span data-stu-id="cbc97-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="cbc97-170">Per un'esercitazione dettagliata, vedere [App-V 5,0 client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span><span class="sxs-lookup"><span data-stu-id="cbc97-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="cbc97-171">Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="cbc97-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="cbc97-172">**Nota** 
 **Questa funzionalità è supportata a partire da App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="cbc97-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="cbc97-173">Usa il cmdlet e il parametro seguenti per consentire solo agli amministratori (non agli utenti finali) di pubblicare o annullare la pubblicazione di pacchetti:</span><span class="sxs-lookup"><span data-stu-id="cbc97-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cbc97-174">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbc97-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cbc97-175">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbc97-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cbc97-176">Parametro</span><span class="sxs-lookup"><span data-stu-id="cbc97-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cbc97-177">-RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="cbc97-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="cbc97-178">Valori dei parametri:</span><span class="sxs-lookup"><span data-stu-id="cbc97-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="cbc97-179">0-falso</span><span class="sxs-lookup"><span data-stu-id="cbc97-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="cbc97-180">1-vero</span><span class="sxs-lookup"><span data-stu-id="cbc97-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="cbc97-181">Esempio: </strong> : set-AppvClientConfiguration-RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="cbc97-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cbc97-182">Per usare la console di gestione di App-V per impostare questa configurazione, vedere [come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="cbc97-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="cbc97-183">Informazioni sui pacchetti in sospeso (UserPending e GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="cbc97-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="cbc97-184">A **partire da App-V 5,0 SP2**: se si esegue un cmdlet di PowerShell che influisce su un pacchetto attualmente in uso, l'attività che si sta provando a eseguire viene inserita in uno stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="cbc97-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="cbc97-185">Se ad esempio si prova a pubblicare un pacchetto quando si usa un'applicazione in tale pacchetto e quindi si esegue **Get-AppvClientPackage**, lo stato in sospeso verrà visualizzato nell'output del cmdlet come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="cbc97-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbc97-186">Elemento di output cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbc97-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="cbc97-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbc97-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbc97-188">UserPending</span><span class="sxs-lookup"><span data-stu-id="cbc97-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbc97-189">Indica se il pacchetto elencato ha un'attività in sospeso che viene applicata all'utente:</span><span class="sxs-lookup"><span data-stu-id="cbc97-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="cbc97-190">True</span><span class="sxs-lookup"><span data-stu-id="cbc97-190">True</span></span></p></li>
<li><p><span data-ttu-id="cbc97-191">False</span><span class="sxs-lookup"><span data-stu-id="cbc97-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbc97-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="cbc97-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbc97-193">Indica se il pacchetto elencato ha un'attività in sospeso applicata globalmente al computer:</span><span class="sxs-lookup"><span data-stu-id="cbc97-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="cbc97-194">True</span><span class="sxs-lookup"><span data-stu-id="cbc97-194">True</span></span></p></li>
<li><p><span data-ttu-id="cbc97-195">False</span><span class="sxs-lookup"><span data-stu-id="cbc97-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cbc97-196">L'attività in sospeso verrà eseguita in un secondo momento, in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbc97-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbc97-197">Tipo di attività</span><span class="sxs-lookup"><span data-stu-id="cbc97-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="cbc97-198">Regola applicabile</span><span class="sxs-lookup"><span data-stu-id="cbc97-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbc97-199">Attività basata su utenti, ad esempio, pubblicazione di un pacchetto in un utente</span><span class="sxs-lookup"><span data-stu-id="cbc97-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbc97-200">L'attività in sospeso verrà eseguita dopo la disattivazione dell'utente e quindi il log di nuovo.</span><span class="sxs-lookup"><span data-stu-id="cbc97-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbc97-201">Attività basata su base globale, ad esempio, che consente a un gruppo di connessioni a livello globale</span><span class="sxs-lookup"><span data-stu-id="cbc97-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbc97-202">L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</span><span class="sxs-lookup"><span data-stu-id="cbc97-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cbc97-203">Per altre informazioni sulle attività in sospeso, vedere [informazioni su App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span><span class="sxs-lookup"><span data-stu-id="cbc97-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="cbc97-204">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="cbc97-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cbc97-205">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="cbc97-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cbc97-206">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="cbc97-206">Got an App-V issue?</span></span>** <span data-ttu-id="cbc97-207">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cbc97-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cbc97-208">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbc97-208">Related topics</span></span>


[<span data-ttu-id="cbc97-209">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="cbc97-209">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="cbc97-210">Amministrazione di App-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbc97-210">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





