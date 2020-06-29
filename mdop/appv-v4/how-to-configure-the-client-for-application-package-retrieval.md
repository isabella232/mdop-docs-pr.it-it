---
title: Come configurare il client per il recupero del pacchetto dell'applicazione
description: Come configurare il client per il recupero del pacchetto dell'applicazione
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817826"
---
# <span data-ttu-id="74a73-103">Come configurare il client per il recupero del pacchetto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="74a73-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="74a73-104">Quando il client è configurato con un server di gestione di Application Virtualization (App-V) come server di pubblicazione, per impostazione predefinita durante il successivo ciclo di aggiornamento della pubblicazione, il client recupera dal server i file OSD (Open Software Descriptor) e del manifesto del pacchetto per ogni pacchetto che l'utente è autorizzato a usare.</span><span class="sxs-lookup"><span data-stu-id="74a73-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="74a73-105">Il client usa le informazioni di origine del pacchetto definite in questi file per determinare dove trovare il contenuto del pacchetto, le icone e le associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="74a73-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="74a73-106">Se si vuole che il client ottenga il contenuto del pacchetto (file SFT) da un'app locale-V Streaming Server o da un'altra origine alternativa, ad esempio un server Web o un file server, invece che da App-V Management Server, è possibile configurare il valore della chiave del registro di sistema ApplicationSourceRoot nel computer in modo che punti alla condivisione di contenuto locale nell'altro server.</span><span class="sxs-lookup"><span data-stu-id="74a73-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="74a73-107">Il file OSD definisce ancora il percorso di origine originale per il contenuto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="74a73-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="74a73-108">Tuttavia, il client usa il valore dell'impostazione ApplicationSourceRoot al posto del server e la condivisione specificata nel percorso di contenuto nel file OSD.</span><span class="sxs-lookup"><span data-stu-id="74a73-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="74a73-109">Questo reindirizza il client per recuperare il contenuto dall'altro server.</span><span class="sxs-lookup"><span data-stu-id="74a73-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="74a73-110">È anche possibile configurare i valori della chiave del registro di sistema OSDSourceRoot e IconSourceRoot se si vuole eseguire l'override di tali impostazioni nel file manifesto del pacchetto o nei percorsi inviati da un server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="74a73-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="74a73-111">OSDSourceRoot specifica una posizione di origine per il recupero dei file OSD per un pacchetto di applicazione durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="74a73-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="74a73-112">IconSourceRoot specifica una posizione di origine per il recupero di icone per un pacchetto di applicazione durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="74a73-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="74a73-113">Nota</span><span class="sxs-lookup"><span data-stu-id="74a73-113">Note</span></span>**  
-   <span data-ttu-id="74a73-114">Le impostazioni IconSourceRoot e OSDSourceRoot eseguono l'override dei valori nel file manifesto del pacchetto, quindi se tenti di distribuire un pacchetto usando il metodo di file con estensione msi di Windows Installer, eseguirà anche l'override dei valori del file manifesto del pacchetto contenuto all'interno del file MSI.</span><span class="sxs-lookup"><span data-stu-id="74a73-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="74a73-115">Durante le operazioni di pubblicazione e di flusso HTTP (S), i client App-V 4,5 SP1 usano le impostazioni del server proxy configurate in Internet Explorer nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74a73-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="74a73-116">Per configurare il valore della chiave del registro di sistema ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="74a73-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="74a73-117">Configurare ApplicationSourceRoot nel valore della chiave del registro di sistema seguente con un percorso UNC o un URL:</span><span class="sxs-lookup"><span data-stu-id="74a73-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="74a73-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="74a73-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="74a73-119">Il formato corretto per il percorso UNC (Universal Naming Convention) è **\\\\computername\\sharefolder\\\ [Folder \] \ [\ \ \]**, dove **cartella** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="74a73-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="74a73-120">**Nomecomputer** può essere un nome di dominio completo (FQDN) o un indirizzo IP e **cartellacondivisione** può essere una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="74a73-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="74a73-121">Viene sostituita solo la parte **\\\\computername\\sharedfolder** o lettera dell'unità del percorso OSD.</span><span class="sxs-lookup"><span data-stu-id="74a73-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="74a73-122">Il formato corretto per il percorso URL è **Protocol://nomeserver: \ [Port \] \ [/path\] \ [/\]**, dove **porta** e **percorso** sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74a73-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="74a73-123">Se la **porta** non è specificata, viene usata la porta predefinita per il protocollo.</span><span class="sxs-lookup"><span data-stu-id="74a73-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="74a73-124">Viene sostituita solo la parte **protocollo://Server: Port** dell'URL OSD.</span><span class="sxs-lookup"><span data-stu-id="74a73-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="74a73-125">Importante</span><span class="sxs-lookup"><span data-stu-id="74a73-125">Important</span></span>**  
    <span data-ttu-id="74a73-126">Le variabili di ambiente non sono supportate nella definizione ApplicationSourceRoot.</span><span class="sxs-lookup"><span data-stu-id="74a73-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="74a73-127">Per configurare il valore OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="74a73-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="74a73-128">Configurare OSDSourceRoot nel valore della chiave del registro di sistema seguente con un percorso UNC o un URL:</span><span class="sxs-lookup"><span data-stu-id="74a73-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="74a73-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="74a73-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="74a73-130">I formati accettabili per OSDSourceRoot includono percorsi UNC e URL, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="74a73-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="74a73-131">**\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o \*\* &lt; unità &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="74a73-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="74a73-132">**http://computername/productivity/** o**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="74a73-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="74a73-133">Per configurare il valore IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="74a73-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="74a73-134">Configurare IconSourceRoot nel valore della chiave del registro di sistema seguente con un percorso UNC o un URL:</span><span class="sxs-lookup"><span data-stu-id="74a73-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="74a73-135">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="74a73-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="74a73-136">I formati accettabili per IconSourceRoot includono percorsi UNC e URL, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="74a73-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="74a73-137">**\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o \*\* &lt; unità &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="74a73-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="74a73-138">**http://computername/productivity/** o**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="74a73-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="74a73-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74a73-139">Related topics</span></span>


[<span data-ttu-id="74a73-140">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="74a73-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









