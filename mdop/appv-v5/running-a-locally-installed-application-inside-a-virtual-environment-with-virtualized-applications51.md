---
title: Esecuzione di un'applicazione installata in locale all'interno di un ambiente virtuale con applicazioni virtualizzate
description: Esecuzione di un'applicazione installata in locale all'interno di un ambiente virtuale con applicazioni virtualizzate
author: dansimp
ms.assetid: 71baf193-a9e8-4ffa-aa7f-e0bffed2e4b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 384a1325b2f363595971f70f25fe0a25cade448d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804870"
---
# <span data-ttu-id="19de2-103">Esecuzione di un'applicazione installata in locale all'interno di un ambiente virtuale con applicazioni virtualizzate</span><span class="sxs-lookup"><span data-stu-id="19de2-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="19de2-104">È possibile eseguire un'applicazione installata localmente in un ambiente virtuale, insieme alle applicazioni virtualizzate tramite Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="19de2-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="19de2-105">Se si vuole eseguire questa operazione, è possibile:</span><span class="sxs-lookup"><span data-stu-id="19de2-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="19de2-106">Si vuole installare ed eseguire un'applicazione localmente nei computer client, ma si vuole virtualizzare ed eseguire plug-in specifici che funzionano con quell'applicazione locale.</span><span class="sxs-lookup"><span data-stu-id="19de2-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="19de2-107">Risoluzione dei problemi relativi a un pacchetto client App-V e si vuole aprire un'applicazione locale nell'ambiente virtuale App-V.</span><span class="sxs-lookup"><span data-stu-id="19de2-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="19de2-108">Usa uno dei metodi seguenti per aprire un'applicazione locale all'interno dell'ambiente virtuale App-V:</span><span class="sxs-lookup"><span data-stu-id="19de2-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="19de2-109">Chiave del registro di sistema RunVirtual</span><span class="sxs-lookup"><span data-stu-id="19de2-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="19de2-110">Cmdlet di PowerShell Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="19de2-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="19de2-111">Opzione della riga di comando/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="19de2-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="19de2-112">Opzione hook della riga di comando/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="19de2-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="19de2-113">Ogni metodo compie essenzialmente la stessa attività, ma alcuni metodi possono essere più adatti per alcune applicazioni rispetto ad altri, a seconda che l'applicazione virtualizzata sia già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="19de2-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="19de2-114">Chiave del registro di sistema RunVirtual</span><span class="sxs-lookup"><span data-stu-id="19de2-114">RunVirtual registry key</span></span>


<span data-ttu-id="19de2-115">Per aggiungere un'applicazione installata localmente a un pacchetto o a un ambiente virtuale di un gruppo di connessioni, è possibile aggiungere una sottochiave alla chiave del registro di sistema `RunVirtual` nell'editor del registro di sistema, come descritto nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="19de2-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="19de2-116">Per gestire questa chiave del registro di sistema non è disponibile alcuna impostazione di criteri di gruppo, quindi è necessario usare System Center Configuration Manager o un altro sistema ESD (Electronic Software Distribution) oppure modificare manualmente il registro.</span><span class="sxs-lookup"><span data-stu-id="19de2-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="19de2-117">Metodi supportati per la pubblicazione di pacchetti quando si usa RunVirtual</span><span class="sxs-lookup"><span data-stu-id="19de2-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="19de2-118">Versione App-V</span><span class="sxs-lookup"><span data-stu-id="19de2-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="19de2-119">Metodi di pubblicazione supportati</span><span class="sxs-lookup"><span data-stu-id="19de2-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="19de2-120">App-V 5,0 SP3 e App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="19de2-120">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="19de2-121">Pubblicato a livello globale o all'utente</span><span class="sxs-lookup"><span data-stu-id="19de2-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="19de2-122">App-V 5,0 tramite App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="19de2-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="19de2-123">Pubblicato solo a livello globale</span><span class="sxs-lookup"><span data-stu-id="19de2-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="19de2-124">Procedura per creare la sottochiave</span><span class="sxs-lookup"><span data-stu-id="19de2-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="19de2-125">Usando le informazioni nella tabella seguente, creare una nuova chiave del registro di sistema usando il nome del file eseguibile, ad esempio **MyApp.exe**.</span><span class="sxs-lookup"><span data-stu-id="19de2-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="19de2-126">Metodo di pubblicazione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="19de2-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="19de2-127">Dove creare la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="19de2-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="19de2-128">Pubblicazione globale</span><span class="sxs-lookup"><span data-stu-id="19de2-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="19de2-129">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="19de2-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="19de2-130">Esempio </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="19de2-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="19de2-131">Pubblicato per l'utente</span><span class="sxs-lookup"><span data-stu-id="19de2-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="19de2-132">HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="19de2-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="19de2-133">Esempio </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="19de2-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="19de2-134">Il gruppo di connessioni può contenere:</span><span class="sxs-lookup"><span data-stu-id="19de2-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="19de2-135">Pacchetti pubblicati solo a livello globale o solo per l'utente</span><span class="sxs-lookup"><span data-stu-id="19de2-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="19de2-136">Pacchetti pubblicati globalmente e all'utente</span><span class="sxs-lookup"><span data-stu-id="19de2-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="19de2-137">HKEY_LOCAL_MACHINE o HKEY_CURRENT_USER chiave, ma tutte le operazioni seguenti devono essere vere:</span><span class="sxs-lookup"><span data-stu-id="19de2-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="19de2-138">Se si vogliono includere più pacchetti nell'ambiente virtuale, è necessario includerli in un gruppo di connessioni abilitato.</span><span class="sxs-lookup"><span data-stu-id="19de2-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="19de2-139">Creare una sola sottochiave per uno dei pacchetti nel gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="19de2-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="19de2-140">Se ad esempio è presente un pacchetto pubblicato globalmente e un altro pacchetto pubblicato per l'utente, è possibile creare una sottochiave per uno di questi pacchetti, ma non entrambe.</span><span class="sxs-lookup"><span data-stu-id="19de2-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="19de2-141">Anche se crei una sottochiave per solo uno dei pacchetti, tutti i pacchetti nel gruppo connessione, oltre all'applicazione locale, saranno disponibili nell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="19de2-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="19de2-142">La chiave in cui si crea la sottochiave deve corrispondere al metodo di pubblicazione usato per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="19de2-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="19de2-143">Ad esempio, se il pacchetto è stato pubblicato per l'utente, è necessario creare la sottochiave in <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="19de2-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="19de2-144">Imposta il valore della sottochiave del nuovo registro di sistema su PackageId e VersionId del pacchetto, separando i valori con un carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="19de2-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="19de2-145">**Sintassi**: &lt; PackageID &gt; \ _ &lt; VersionId&gt;</span><span class="sxs-lookup"><span data-stu-id="19de2-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="19de2-146">**Esempio**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="19de2-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="19de2-147">L'applicazione nell'esempio precedente produrrebbe un file di esportazione del registro di sistema (file con estensione reg) simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="19de2-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="19de2-148">Cmdlet di PowerShell Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="19de2-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="19de2-149">Puoi usare il cmdlet **Start-AppVVirtualProcess** per recuperare il nome del pacchetto e quindi avviare un processo nell'ambiente virtuale del pacchetto specificato.</span><span class="sxs-lookup"><span data-stu-id="19de2-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="19de2-150">Questo metodo consente di avviare qualsiasi comando nel contesto di un pacchetto di App-V, indipendentemente dal fatto che il pacchetto sia attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="19de2-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="19de2-151">Usa la sintassi di esempio seguente e Sostituisci il nome del pacchetto per il \*\* &lt; pacchetto &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="19de2-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="19de2-152">Se non si conosce il nome esatto del pacchetto, è possibile usare la riga di comando **Get-AppvClientPackage \ \* executable\\** <em> , dove \*\* </em> eseguibile\* è il nome dell'applicazione, ad esempio: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="19de2-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="19de2-153">Opzione della riga di comando/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="19de2-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="19de2-154">Puoi applicare l'opzione \*\*/appvpid: &lt; PID &gt; \*\* a qualsiasi comando, che consente di eseguire il comando in un processo virtuale selezionato specificando il relativo ID processo (PID).</span><span class="sxs-lookup"><span data-stu-id="19de2-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="19de2-155">L'uso di questo metodo avvia il nuovo eseguibile nello stesso ambiente App-V di un eseguibile già in uso.</span><span class="sxs-lookup"><span data-stu-id="19de2-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="19de2-156">Esempio:</span><span class="sxs-lookup"><span data-stu-id="19de2-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="19de2-157">Per trovare l'ID processo (PID) del processo App-V, eseguire il comando **tasklist.exe** da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="19de2-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="19de2-158">Opzione hook della riga di comando/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="19de2-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="19de2-159">Questa opzione consente di eseguire un comando locale nell'ambiente virtuale di un pacchetto di App-V.</span><span class="sxs-lookup"><span data-stu-id="19de2-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="19de2-160">Diversamente dall'opzione **/appvid** , in cui l'ambiente virtuale deve essere già in funzione, questa opzione consente di avviare l'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="19de2-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="19de2-161">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19de2-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="19de2-162">Esempio:</span><span class="sxs-lookup"><span data-stu-id="19de2-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="19de2-163">Per ottenere il GUID del pacchetto e il GUID della versione dell'applicazione, eseguire il cmdlet **Get-AppvClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="19de2-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="19de2-164">Concatenare l'opzione **/appvve** con la seguente:</span><span class="sxs-lookup"><span data-stu-id="19de2-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="19de2-165">I due punti</span><span class="sxs-lookup"><span data-stu-id="19de2-165">A colon</span></span>

-   <span data-ttu-id="19de2-166">GUID del pacchetto del pacchetto desiderato</span><span class="sxs-lookup"><span data-stu-id="19de2-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="19de2-167">Un carattere di sottolineatura</span><span class="sxs-lookup"><span data-stu-id="19de2-167">An underscore</span></span>

-   <span data-ttu-id="19de2-168">ID versione del pacchetto desiderato</span><span class="sxs-lookup"><span data-stu-id="19de2-168">Version ID of the desired package</span></span>

<span data-ttu-id="19de2-169">Se non si conosce il nome esatto del pacchetto, usare la riga di comando **Get-AppvClientPackage \ \* executable\\** <em> , dove \*\*eseguibile </em> \* è il nome dell'applicazione, ad esempio Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="19de2-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="19de2-170">Questo metodo consente di avviare qualsiasi comando nel contesto di un pacchetto di App-V, indipendentemente dal fatto che il pacchetto sia attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="19de2-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="19de2-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19de2-171">Related topics</span></span>


[<span data-ttu-id="19de2-172">Documentazione tecnica per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="19de2-172">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)

 

 





