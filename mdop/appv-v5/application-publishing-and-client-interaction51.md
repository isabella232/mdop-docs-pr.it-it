---
title: Pubblicazione delle applicazioni e interazione dei client
description: Pubblicazione delle applicazioni e interazione dei client
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 69fcf119faaf35e53ae36f386bcb3480e2ee3b0e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805949"
---
# <span data-ttu-id="0b8f4-103">Pubblicazione delle applicazioni e interazione dei client</span><span class="sxs-lookup"><span data-stu-id="0b8f4-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="0b8f4-104">Questo articolo fornisce informazioni tecniche sulle comuni operazioni client App-V e la loro integrazione con il sistema operativo locale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="0b8f4-105">File di pacchetto App-V creati dal sequencer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="0b8f4-106">Cosa contiene il file appv?</span><span class="sxs-lookup"><span data-stu-id="0b8f4-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="0b8f4-107">Percorsi di archiviazione dei dati client App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="0b8f4-108">Registro del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="0b8f4-109">Comportamento dell'archivio pacchetti App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="0b8f4-110">Registro di sistema e dati mobili</span><span class="sxs-lookup"><span data-stu-id="0b8f4-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="0b8f4-111">Gestione del ciclo di vita dell'applicazione client App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="0b8f4-112">Integrazione dei pacchetti App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="0b8f4-113">Elaborazione della configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="0b8f4-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="0b8f4-114">Assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="0b8f4-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="0b8f4-115">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="0b8f4-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="0b8f4-116">Per altre informazioni di riferimento, vedere [pagina di download delle risorse della documentazione di Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="0b8f4-117">File di pacchetto App-V creati dal sequencer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="0b8f4-118">Sequencer crea pacchetti App-V e produce un'applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="0b8f4-119">Il processo di sequenziazione crea i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-120">File</span><span class="sxs-lookup"><span data-stu-id="0b8f4-120">File</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-122">. AppV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-123">Il file del pacchetto principale, che contiene le informazioni relative agli asset e allo stato acquisiti dal processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-124">Architettura del file di pacchetto, informazioni sulla pubblicazione e registro di sistema in una maschera in formato token che può essere riapplicata a un computer e a un utente specifico al momento del recapito.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-125">. MSI</span><span class="sxs-lookup"><span data-stu-id="0b8f4-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-126">Wrapper di distribuzione eseguibile che puoi usare per distribuire file con estensione appv manualmente o usando una piattaforma di distribuzione di terze parti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-128">File usato per personalizzare i parametri di pubblicazione predefiniti per tutte le applicazioni in un pacchetto distribuito globalmente a tutti gli utenti in un computer in cui è in uso il client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-130">File usato per personalizzare i parametri di pubblicazione per tutte le applicazioni in un pacchetto distribuito a un utente specifico in un computer in cui è in uso il client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-132">Riepilogo dei messaggi risultante dal processo di sequenziazione, inclusi i driver omessi, i file e le posizioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-133">. TAXI</span><span class="sxs-lookup"><span data-stu-id="0b8f4-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="0b8f4-134">Facoltativo: </em> file di accelerazione pacchetto usato per ricostruire automaticamente un pacchetto di applicazione virtuale sequenziato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-135">.appvt</span><span class="sxs-lookup"><span data-stu-id="0b8f4-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="0b8f4-136">Facoltativo: </em> file di modello sequencer usato per mantenere le impostazioni di Sequencer comunemente riutilizzate.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0b8f4-137">Per informazioni sulla sequenziazione, vedere [Guida alla sequenziazione della virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkID=269810).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-137">For information about sequencing, see [Application Virtualization Sequencing Guide](https://go.microsoft.com/fwlink/?LinkID=269810).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="0b8f4-138">Cosa contiene il file appv?</span><span class="sxs-lookup"><span data-stu-id="0b8f4-138">What’s in the appv file?</span></span>


<span data-ttu-id="0b8f4-139">Il file appv è un contenitore che archivia i file XML e non XML insieme in una singola entità.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="0b8f4-140">Questo file è compilato dal formato AppX, che si basa sullo standard Open Packaging Conventions (OPC).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="0b8f4-141">Per visualizzare il contenuto del file appv, creare una copia del pacchetto e quindi rinominare il file copiato in un'estensione ZIP.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="0b8f4-142">Il file appv contiene la cartella e i file seguenti, che vengono usati durante la creazione e la pubblicazione di un'applicazione virtuale:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-143">Nome</span><span class="sxs-lookup"><span data-stu-id="0b8f4-143">Name</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b8f4-144">Type</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-146">Root</span><span class="sxs-lookup"><span data-stu-id="0b8f4-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-147">Cartella di file</span><span class="sxs-lookup"><span data-stu-id="0b8f4-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-148">Directory che contiene il file System per l'applicazione virtualizzata acquisita durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-149">[Content_Types]. XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-150">File XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-151">Elenco dei tipi di contenuto principali nel file appv (ad esempio DLL, EXE, BIN).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-153">File XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-154">Layout del file appv, che usa gli elementi file, Block e BlockMap che consentono la posizione e la convalida dei file nel pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-156">File XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-157">Metadati per il pacchetto che contiene le informazioni necessarie per l'aggiunta, la pubblicazione e l'avvio del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="0b8f4-158">Include i punti di estensione (associazioni di tipi di file e tasti di scelta rapida) e i nomi e i GUID associati al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-160">File XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-161">Elenco dei file acquisiti durante la sequenziazione, inclusi gli attributi (ad esempio, directory, file, directory opache, directory vuote e nomi lunghi e brevi).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-163">File XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-164">Informazioni sul computer di sequenziazione (versione del sistema operativo, versione di Internet Explorer, versione di .NET Framework) ed elaborazione (aggiornamento, versione del pacchetto).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-165">Registry. dat</span><span class="sxs-lookup"><span data-stu-id="0b8f4-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-166">File DAT</span><span class="sxs-lookup"><span data-stu-id="0b8f4-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-167">Chiavi del registro di sistema e valori acquisiti durante il processo di sequenziazione per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-169">File XML</span><span class="sxs-lookup"><span data-stu-id="0b8f4-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-170">Elenco di file per il blocco delle caratteristiche primarie e di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="0b8f4-171">Il blocco di funzionalità di pubblicazione contiene i file ICO e le parti necessarie di file (EXE e DLL) per la pubblicazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="0b8f4-172">Quando è presente, il blocco di funzionalità principale include i file che sono stati ottimizzati per lo streaming durante il processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="0b8f4-173">Percorsi di archiviazione dei dati client App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-173">App-V client data storage locations</span></span>


<span data-ttu-id="0b8f4-174">Il client App-V esegue le attività per garantire che le applicazioni virtuali vengano eseguite correttamente e funzioni come le applicazioni installate localmente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="0b8f4-175">Il processo di apertura ed esecuzione delle applicazioni virtuali richiede il mapping dal file system virtuale e dal registro di sistema per garantire che l'applicazione abbia i componenti necessari di un'applicazione tradizionale prevista dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="0b8f4-176">Questa sezione descrive gli asset necessari per eseguire applicazioni virtuali ed elenca la posizione in cui App-V archivia gli asset.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-177">Nome</span><span class="sxs-lookup"><span data-stu-id="0b8f4-177">Name</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-178">Percorso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-178">Location</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-180">Archivio pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-182">Percorso predefinito per i file di pacchetto di sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b8f4-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-183">Catalogo computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="0b8f4-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-185">Contiene documenti di configurazione per computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-186">Catalogo utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="0b8f4-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-188">Contiene documenti di configurazione per utente</span><span class="sxs-lookup"><span data-stu-id="0b8f4-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-189">Backup di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0b8f4-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="0b8f4-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-191">Archivia i punti di integrazione precedenti che consentono di ripristinare il pacchetto Unpublish</span><span class="sxs-lookup"><span data-stu-id="0b8f4-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-192">Copia su scrittura (mucca) roaming</span><span class="sxs-lookup"><span data-stu-id="0b8f4-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="0b8f4-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-194">Posizione di roaming scrivibile per la modifica del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-195">Copia in scrittura (mucca) local</span><span class="sxs-lookup"><span data-stu-id="0b8f4-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="0b8f4-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-197">Posizione di non roaming scrivibile per la modifica del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-198">Registro di sistema del computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-200">Contiene informazioni sullo stato del pacchetto, tra cui ORSAE per computer o pacchetti pubblicati globalmente (hive macchina)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-201">Registro utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-203">Contiene informazioni sullo stato del pacchetto utente, tra cui ORSAE</span><span class="sxs-lookup"><span data-stu-id="0b8f4-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-204">Classi del registro di sistema degli utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-206">Contiene informazioni aggiuntive sullo stato del pacchetto utente</span><span class="sxs-lookup"><span data-stu-id="0b8f4-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0b8f4-207">I dettagli aggiuntivi per la tabella sono disponibili nella sezione seguente e in tutto il documento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="0b8f4-208">Archivio pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-208">Package store</span></span>

<span data-ttu-id="0b8f4-209">Il client App-V gestisce gli asset delle applicazioni montati nell'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="0b8f4-210">Questo percorso di archiviazione predefinito è `%ProgramData%\App-V` , ma è possibile configurarlo durante o dopo la configurazione usando il `Set-AppVClientConfiguration` comando di PowerShell, che modifica il registro di sistema locale ( `PackageInstallationRoot` valore sotto la `HKLM\Software\Microsoft\AppV\Client\Streaming` chiave).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="0b8f4-211">L'archivio pacchetti deve trovarsi in un percorso locale nel sistema operativo client.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="0b8f4-212">I singoli pacchetti vengono archiviati nell'archivio pacchetti in sottodirectory denominati per il GUID del pacchetto e il GUID della versione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="0b8f4-213">Esempio di percorso di un'applicazione specifica:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="0b8f4-214">Per modificare la posizione predefinita dell'archivio pacchetti durante l'installazione, vedere [come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

### <span data-ttu-id="0b8f4-215">Archivio contenuto condiviso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-215">Shared Content Store</span></span>

<span data-ttu-id="0b8f4-216">Se il client App-V è configurato in modalità archivio contenuto condiviso, non vengono scritti dati su disco quando si verifica un errore di flusso, il che significa che i pacchetti richiedono spazio minimo su disco locale (dati di pubblicazione).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="0b8f4-217">L'uso di meno spazio su disco è molto utile in ambienti VDI, in cui l'archiviazione locale può essere limitata e lo streaming delle applicazioni da un percorso di rete ad alte prestazioni, ad esempio un SAN, è preferibile.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="0b8f4-218">Per altre informazioni sulla modalità di archiviazione del contenuto condivisa, vedere <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="0b8f4-219">**Nota**  Il computer e l'archivio pacchetti devono essere posizionati in un'unità locale, anche quando si usano configurazioni di archivio contenuto condiviso per il client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="0b8f4-220">Cataloghi di pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-220">Package catalogs</span></span>

<span data-ttu-id="0b8f4-221">Il client App-V gestisce i due percorsi basati su file seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="0b8f4-222">Cataloghi (utente e computer).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="0b8f4-223">**Posizioni del registro di sistema** -dipende dalla modalità di destinazione del pacchetto per la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="0b8f4-224">È disponibile un catalogo (archivio dati) per il computer e un catalogo per ogni singolo utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="0b8f4-225">Il catalogo computer archivia le informazioni globali applicabili a tutti gli utenti o a qualsiasi utente e il catalogo dell'utente archivia le informazioni applicabili a un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="0b8f4-226">Il catalogo è una raccolta di configurazioni dinamiche e file manifesto; sono disponibili dati discreti sia per file che per il registro di sistema per versione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="0b8f4-227">Catalogo computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-228">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-229">Archivia i documenti del pacchetto disponibili per gli utenti nel computer, quando i pacchetti vengono aggiunti e pubblicati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="0b8f4-230">Tuttavia, se un pacchetto è "globale" in fase di pubblicazione, le integrazioni sono disponibili per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="0b8f4-231">Se un pacchetto non è globale, le integrazioni vengono pubblicate solo per utenti specifici, ma esistono ancora risorse globali modificate e visibili a chiunque nel computer client (ad esempio, la directory del pacchetto si trova in un percorso del disco condiviso).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="0b8f4-232">Se un pacchetto è disponibile per un utente nel computer (globale o non globale), il manifesto viene archiviato nel catalogo computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="0b8f4-233">Quando un pacchetto viene pubblicato globalmente, esiste un file di configurazione dinamica archiviato nel catalogo computer; di conseguenza, la determinazione del fatto che un pacchetto sia globale viene definita in base alla presenza di un file di criteri (file UserDeploymentConfiguration) nel catalogo computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-234">Posizione di archiviazione predefinita</span><span class="sxs-lookup"><span data-stu-id="0b8f4-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="0b8f4-235">Questa posizione non è uguale alla posizione dell'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="0b8f4-236">L'archivio pacchetti è la copia dorata o incontaminata dei file di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-237">File nel catalogo computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-240">UserManifest.xml (pacchetto pubblicato globalmente)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-241">UserDeploymentConfiguration.xml (pacchetto pubblicato globalmente)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-242">Posizione del catalogo computer aggiuntivo, usata quando il pacchetto fa parte di un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-243">La posizione seguente è in aggiunta al percorso specifico del pacchetto menzionato sopra:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-244">File aggiuntivi nel catalogo computer quando il pacchetto fa parte di un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-246">UserPackageGroupDescriptor.xml (gruppo di connessioni pubblicato globalmente)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0b8f4-247">Catalogo utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-248">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-249">Creato durante il processo di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-249">Created during the publishing process.</span></span> <span data-ttu-id="0b8f4-250">Contiene le informazioni usate per la pubblicazione del pacchetto e usate anche all'avvio per verificare che un pacchetto venga provisionato a un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="0b8f4-251">Creato in un percorso di roaming e include informazioni di pubblicazione specifiche per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="0b8f4-252">Quando un pacchetto viene pubblicato per un utente, il file di criteri viene archiviato nel catalogo utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="0b8f4-253">Contemporaneamente, nel catalogo utente viene archiviata anche una copia del manifesto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="0b8f4-254">Quando viene rimosso un diritto del pacchetto per un utente, i file di pacchetto rilevanti vengono rimossi dal catalogo utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="0b8f4-255">Guardando il catalogo degli utenti, un amministratore può visualizzare la presenza di un file di configurazione dinamica, che indica che il pacchetto è autorizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="0b8f4-256">Per gli utenti mobili, il catalogo utente deve essere in una posizione comune o in roaming per mantenere il comportamento legacy di App-V di destinazione degli utenti per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="0b8f4-257">I diritti e i criteri sono collegati a un utente, non a un computer, in modo che debbano eseguire il roaming con l'utente dopo il provisioning.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-258">Posizione di archiviazione predefinita</span><span class="sxs-lookup"><span data-stu-id="0b8f4-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-259">File nel catalogo utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-261">DynamicConfiguration.xml o UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-262">Posizione del catalogo utenti aggiuntiva, usata quando il pacchetto fa parte di un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-263">La posizione seguente è in aggiunta al percorso specifico del pacchetto menzionato sopra:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-264">File aggiuntivo nel catalogo computer quando il pacchetto fa parte di un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0b8f4-265">Backup di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0b8f4-265">Shortcut backups</span></span>

<span data-ttu-id="0b8f4-266">Durante il processo di pubblicazione, il client App-V consente di eseguire il backup di tutti i tasti di scelta rapida e i punti di integrazione di `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` questo supporto per consentire il ripristino di questi punti di integrazione con le versioni precedenti quando il pacchetto non è pubblicato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="0b8f4-267">Copiare i file in scrittura</span><span class="sxs-lookup"><span data-stu-id="0b8f4-267">Copy on Write files</span></span>

<span data-ttu-id="0b8f4-268">L'archivio pacchetti contiene una copia incontaminata dei file di pacchetto che sono stati trasmessi dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="0b8f4-269">Durante il normale funzionamento di un'applicazione App-V, l'utente o il servizio può richiedere modifiche ai file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="0b8f4-270">Queste modifiche non vengono apportate nell'archivio pacchetti per mantenere la possibilità di ripristinare l'applicazione, che rimuove queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="0b8f4-271">Queste posizioni, denominate copia in scrittura (mucca), supportano le posizioni di roaming e non in roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="0b8f4-272">La posizione in cui sono archiviate le modifiche dipende dal punto in cui l'applicazione è stata programmata per scrivere le modifiche in un'esperienza nativa.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="0b8f4-273">Roaming mucca</span><span class="sxs-lookup"><span data-stu-id="0b8f4-273">COW roaming</span></span>

<span data-ttu-id="0b8f4-274">La posizione di roaming mucca descritta sopra memorizza le modifiche apportate ai file e alle directory che sono destinati al percorso tipico% AppData% o alla posizione di \\Users\\{username}\\AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="0b8f4-275">Queste directory e file vengono quindi spostati in roaming in base alle impostazioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="0b8f4-276">MUCCA locale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-276">COW local</span></span>

<span data-ttu-id="0b8f4-277">La posizione locale della mucca è simile alla posizione di roaming, ma le directory e i file non sono in roaming con altri computer, anche se è stato configurato il supporto per il roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="0b8f4-278">La posizione locale COW descritta sopra memorizza le modifiche applicabili alle finestre tipiche e non la posizione% AppData%.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="0b8f4-279">Le directory elencate variano, ma ci saranno due posizioni per tutti i percorsi di Windows tipici, ad esempio AppData comuni e AppData comuni.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="0b8f4-280">La **S** indica la posizione con restrizioni quando il servizio virtuale richiede la modifica come utente elevato diverso dagli utenti connessi.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="0b8f4-281">La posizione non**S** archivia le modifiche basate sull'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="0b8f4-282">Registro del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-282">Package registry</span></span>


<span data-ttu-id="0b8f4-283">Prima che un'applicazione possa accedere ai dati del registro di sistema del pacchetto, il client App-V deve rendere disponibili i dati del registro di sistema per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="0b8f4-284">Il client App-V usa il registro di sistema reale come archivio di backup per tutti i dati del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="0b8f4-285">Quando viene aggiunto un nuovo pacchetto al client App-V, una copia del registro di sistema. Viene creato il file DAT dal pacchetto `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="0b8f4-286">Il nome del file è il GUID della versione con. Estensione DAT.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="0b8f4-287">Il motivo per cui viene eseguita questa copia consiste nel garantire che il file hive effettivo nel pacchetto non sia mai in uso, impedendo così la rimozione del pacchetto in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0b8f4-288">Registry. dat dall'archivio pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0b8f4-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</span><span class="sxs-lookup"><span data-stu-id="0b8f4-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0b8f4-290">Quando la prima applicazione del pacchetto viene avviata nel client, il client fasi o copia il contenuto del file hive, ricreando i dati del registro di sistema in una posizione alternativa `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="0b8f4-291">I dati del registro di sistema a fasi includono due tipi distinti di dati del computer e dati utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="0b8f4-292">I dati del computer vengono condivisi in tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="0b8f4-293">I dati degli utenti vengono inscenati per ogni utente in una posizione userspecific `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="0b8f4-294">I dati del computer vengono rimossi in definitiva al momento della rimozione del pacchetto e i dati dell'utente vengono rimossi in un'operazione di annullamento della pubblicazione da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="0b8f4-295">Staging del registro di sistema del pacchetto e organizzazione del registro di sistema Connection Group</span><span class="sxs-lookup"><span data-stu-id="0b8f4-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="0b8f4-296">Quando i gruppi di connessioni sono presenti, il processo precedente di staging del registro di sistema è vero, ma invece di avere un file hive da elaborare, ce ne sono più di uno.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="0b8f4-297">I file vengono elaborati nell'ordine in cui vengono visualizzati nel codice XML del gruppo di connessioni, con il primo autore che vince i conflitti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="0b8f4-298">Il registro di sistema a fasi viene mantenuto allo stesso modo del caso del singolo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="0b8f4-299">I dati del registro di sistema degli utenti a fasi rimangono per il gruppo di connessioni finché non vengono disabilitati; i dati del registro di sistema a fasi vengono rimossi nella rimozione dei gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="0b8f4-300">Registro di sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-300">Virtual registry</span></span>

<span data-ttu-id="0b8f4-301">Lo scopo del registro di sistema virtuale (ORSAE) consiste nel creare una singola visualizzazione unita del registro di sistema e del registro di sistema nativo delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="0b8f4-302">Offre anche funzionalità di mucca (copy-on-Write), ovvero tutte le modifiche apportate al registro di sistema dal contesto di un processo virtuale vengono effettuate in una posizione di mucca separata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="0b8f4-303">Questo significa che ORSAE deve combinare fino a tre posizioni separate del registro di sistema in una singola visualizzazione in base alle posizioni compilate nel registro di sistema COW- &gt; package- &gt; native.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="0b8f4-304">Quando viene eseguita una richiesta per i dati del registro di sistema verranno individuati in ordine fino a quando non vengono trovati i dati che richiedevano.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="0b8f4-305">Significato se c'è un valore archiviato in una posizione di mucca non procederà ad altre posizioni, tuttavia, se non ci sono dati nella posizione della mucca procederà al pacchetto e quindi alla posizione nativa finché non trova i dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="0b8f4-306">Posizioni del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0b8f4-306">Registry locations</span></span>

<span data-ttu-id="0b8f4-307">Esistono due posizioni del registro dei pacchetti e due posizioni del gruppo di connessioni in cui il client App-V archivia le informazioni del registro di sistema, a seconda che il pacchetto venga pubblicato singolarmente o come parte di un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="0b8f4-308">Esistono tre posizioni di mucca per i pacchetti e tre per i gruppi di connessioni, che vengono creati e gestiti da ORSAE.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="0b8f4-309">Le impostazioni per i pacchetti e i gruppi di connessioni non sono condivise:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="0b8f4-310">ORSAE pacchetto singolo:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0b8f4-311">Percorso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0b8f4-312">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0b8f4-313">MUCCA</span><span class="sxs-lookup"><span data-stu-id="0b8f4-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-314">Registry\Client\Packages\PkgGUID\REGISTRY computer (solo il processo di elevazione può scrivere)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-315">Registry\Client\Packages\PkgGUID\REGISTRY utente (utente che si sposta in un altro elemento scritto in HKCU eccetto Software\Classes</span><span class="sxs-lookup"><span data-stu-id="0b8f4-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-316">Classes\Client\Packages\PkgGUID\REGISTRY del registro di sistema degli utenti (HKCU\Software\Classes scrive e HKLM per processi non elevati)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0b8f4-317">Pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-318">Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine del computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-319">Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry del registro di sistema degli utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0b8f4-320">Nativo</span><span class="sxs-lookup"><span data-stu-id="0b8f4-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-321">Percorso del registro di sistema delle applicazioni native</span><span class="sxs-lookup"><span data-stu-id="0b8f4-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="0b8f4-322">Gruppo di connessioni ORSAE:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0b8f4-323">Percorso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="0b8f4-324">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0b8f4-325">MUCCA</span><span class="sxs-lookup"><span data-stu-id="0b8f4-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-326">Registry\Client\PackageGroups\GrpGUID\REGISTRY computer (solo il processo di elevazione può scrivere)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-327">Registry\Client\PackageGroups\GrpGUID\REGISTRY utente (qualsiasi elemento scritto in HKCU eccetto Software\Classes</span><span class="sxs-lookup"><span data-stu-id="0b8f4-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-328">Classes\Client\PackageGroups\GrpGUID\REGISTRY del registro di sistema degli utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0b8f4-329">Pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-330">Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY del computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-331">Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY del registro di sistema degli utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0b8f4-332">Nativo</span><span class="sxs-lookup"><span data-stu-id="0b8f4-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="0b8f4-333">Percorso del registro di sistema delle applicazioni native</span><span class="sxs-lookup"><span data-stu-id="0b8f4-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="0b8f4-334">Esistono due posizioni della mucca per HKLM; processi sopraelevati e non elevati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="0b8f4-335">I processi elevati scrivono sempre le modifiche HKLM alla mucca sicura in HKLM.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="0b8f4-336">I processi non elevati scrivono sempre le modifiche HKLM alla mucca non sicura in HKCU\\Software\\Classes.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="0b8f4-337">Quando un'applicazione legge le modifiche da HKLM, i processi elevati leggeranno le modifiche apportate dalla mucca sicura in HKLM.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="0b8f4-338">Letture non elevate da entrambi, che favoriscono prima le modifiche apportate alla mucca non sicura.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="0b8f4-339">Tasti pass-through</span><span class="sxs-lookup"><span data-stu-id="0b8f4-339">Pass-through keys</span></span>

<span data-ttu-id="0b8f4-340">I tasti pass-through consentono a un amministratore di configurare determinati tasti in modo che possano essere letti solo dal registro di sistema nativo, ignorando le posizioni del pacchetto e della mucca.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="0b8f4-341">I percorsi di passaggio sono globali per il computer (non specifici del pacchetto) e possono essere configurati aggiungendo il percorso alla chiave, che deve essere considerato come pass-through per il valore **reg \ _MULTI \ _SZ** denominato **PassThroughPaths** della chiave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="0b8f4-342">Qualsiasi chiave visualizzata in questo valore multistringa (e i relativi elementi figlio) verrà considerata come pass-through.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="0b8f4-343">Le posizioni seguenti sono configurate come posizioni passate per impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="0b8f4-344">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="0b8f4-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="0b8f4-345">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="0b8f4-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="0b8f4-346">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span><span class="sxs-lookup"><span data-stu-id="0b8f4-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="0b8f4-347">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span><span class="sxs-lookup"><span data-stu-id="0b8f4-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="0b8f4-348">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span><span class="sxs-lookup"><span data-stu-id="0b8f4-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="0b8f4-349">HKEY \ _CURRENT \ _USER impostazioni \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet</span><span class="sxs-lookup"><span data-stu-id="0b8f4-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="0b8f4-350">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="0b8f4-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="0b8f4-351">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="0b8f4-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="0b8f4-352">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="0b8f4-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="0b8f4-353">Lo scopo delle chiavi pass-through consiste nel garantire che un'applicazione virtuale non scriva i dati del registro di sistema ORSAE necessari per le applicazioni non virtuali per l'operazione o l'integrazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="0b8f4-354">La chiave policy garantisce che le impostazioni basate su criteri di gruppo impostate dall'amministratore vengano usate e non per le impostazioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="0b8f4-355">La chiave AppModel è necessaria per l'integrazione con le applicazioni basate sull'interfaccia utente moderna di Windows.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="0b8f4-356">È consigliabile che le amministrazioni non modifichino i tasti pass-through predefiniti, ma in alcuni casi, in base al comportamento delle applicazioni, potrebbe essere necessario aggiungere ulteriori chiavi pass-through.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="0b8f4-357">Comportamento dell'archivio pacchetti App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-357">App-V package store behavior</span></span>


<span data-ttu-id="0b8f4-358">App-V 5 gestisce l'archivio dei pacchetti, ovvero la posizione in cui sono archiviati i file di asset espansi dal file AppV.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="0b8f4-359">Per impostazione predefinita, questa posizione è archiviata in%ProgramData%\\App-V ed è limitata in termini di funzionalità di archiviazione solo per spazio su disco gratuito.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="0b8f4-360">L'archivio pacchetti è organizzato dai GUID per il pacchetto e la versione come indicato nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="0b8f4-361">Aggiungere pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-361">Add packages</span></span>

<span data-ttu-id="0b8f4-362">I pacchetti App-V vengono assegnati al computer con il client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="0b8f4-363">Il client App-V offre la gestione temporanea su richiesta.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="0b8f4-364">Durante la pubblicazione o un manuale Add-AppVClientPackage, la struttura dei dati viene compilata nell'archivio pacchetti (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="0b8f4-365">I file di pacchetto identificati nel blocco di pubblicazione definiti nella StreamMap.xml vengono aggiunti al sistema e le cartelle di primo livello e i file figlio sono in fase di esecuzione per garantire l'esistenza di asset applicazione corretti all'avvio.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="0b8f4-366">Installazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-366">Mounting packages</span></span>

<span data-ttu-id="0b8f4-367">I pacchetti possono essere caricati in modo esplicito usando PowerShell `Mount-AppVClientPackage` o usando l' **interfaccia utente del client App-V** per scaricare un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="0b8f4-368">Questa operazione carica completamente l'intero pacchetto nell'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="0b8f4-369">Pacchetti di flusso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-369">Streaming packages</span></span>

<span data-ttu-id="0b8f4-370">Il client App-V può essere configurato per modificare il comportamento predefinito del flusso.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="0b8f4-371">Tutti i criteri di flusso sono archiviati nella chiave del registro di sistema seguente: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="0b8f4-372">I criteri vengono impostati tramite il cmdlet di PowerShell `Set-AppvClientConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="0b8f4-373">I criteri seguenti si applicano allo streaming:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-374">Criterio</span><span class="sxs-lookup"><span data-stu-id="0b8f4-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-375">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="0b8f4-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-377">In Windows 8 e versioni successive, consente lo streaming su reti 3G e cellulari</span><span class="sxs-lookup"><span data-stu-id="0b8f4-377">On Windows 8 and later, it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-378">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="0b8f4-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-379">Specifica l'impostazione di caricamento in background:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="0b8f4-380">0 </strong> - disabilitato</span><span class="sxs-lookup"><span data-stu-id="0b8f4-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="0b8f4-381">1 </strong> -solo pacchetti usati in precedenza</span><span class="sxs-lookup"><span data-stu-id="0b8f4-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="0b8f4-382">2 </strong> -tutti i pacchetti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-383">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="0b8f4-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-384">Cartella radice per l'archivio di pacchetti nel computer locale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="0b8f4-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-386">L'override radice in cui devono essere trasmessi i pacchetti da</span><span class="sxs-lookup"><span data-stu-id="0b8f4-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="0b8f4-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-388">Consente l'uso dell'archivio contenuto condiviso per gli scenari VDI</span><span class="sxs-lookup"><span data-stu-id="0b8f4-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="0b8f4-389">Queste impostazioni influiscono sul comportamento degli asset del pacchetto di App-V in streaming al client.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="0b8f4-390">Per impostazione predefinita, App-V Scarica solo gli asset necessari dopo il download dei blocchi di funzionalità primari e di pubblicazione iniziali.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="0b8f4-391">Esistono tre comportamenti specifici per lo streaming di pacchetti che devono essere spiegati:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="0b8f4-392">Flusso di sfondo</span><span class="sxs-lookup"><span data-stu-id="0b8f4-392">Background Streaming</span></span>

-   <span data-ttu-id="0b8f4-393">Flusso ottimizzato</span><span class="sxs-lookup"><span data-stu-id="0b8f4-393">Optimized Streaming</span></span>

-   <span data-ttu-id="0b8f4-394">Errori di flusso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-394">Stream Faults</span></span>

### <span data-ttu-id="0b8f4-395">Flusso di sfondo</span><span class="sxs-lookup"><span data-stu-id="0b8f4-395">Background streaming</span></span>

<span data-ttu-id="0b8f4-396">Il cmdlet `Get-AppvClientConfiguration` di PowerShell può essere usato per determinare la modalità corrente per il flusso dello sfondo con l'impostazione AutoLoad e modificata con il cmdlet Set-AppvClientConfiguration o dal registro di sistema (chiave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="0b8f4-397">Lo streaming in background è un'impostazione predefinita in cui l'impostazione autoload è impostata per il download dei pacchetti usati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="0b8f4-398">Il comportamento basato sull'impostazione predefinita (valore = 1) Scarica i blocchi di dati App-V in background dopo l'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="0b8f4-399">Questa impostazione può essere disabilitata tutti insieme (valore = 0) o abilitata per tutti i pacchetti (valore = 2), indipendentemente dal fatto che siano stati avviati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="0b8f4-400">Flusso ottimizzato</span><span class="sxs-lookup"><span data-stu-id="0b8f4-400">Optimized streaming</span></span>

<span data-ttu-id="0b8f4-401">I pacchetti App-V possono essere configurati con un blocco di funzionalità principale durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="0b8f4-402">Questa impostazione consente all'ingegnere di sequenziazione di monitorare i file di avvio per un'applicazione o applicazioni specifiche e di contrassegnare i blocchi di dati nel pacchetto App-V per lo streaming al primo avvio di qualsiasi applicazione nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="0b8f4-403">Errori di flusso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-403">Stream faults</span></span>

<span data-ttu-id="0b8f4-404">Dopo il flusso iniziale di tutti i dati di pubblicazione e il blocco di funzionalità principale, le richieste di file aggiuntivi eseguono errori di flusso.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="0b8f4-405">Questi blocchi di dati vengono scaricati nell'archivio pacchetti in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="0b8f4-406">In questo modo, un utente deve scaricare solo una piccola parte del pacchetto, in genere sufficiente per avviare il pacchetto ed eseguire attività normali.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="0b8f4-407">Tutti gli altri blocchi vengono scaricati quando un utente avvia un'operazione che richiede dati non attualmente presenti nell'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="0b8f4-408">Per altre informazioni su App-V pacchetto in streaming, visita: <https://go.microsoft.com/fwlink/?LinkId=392770> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="0b8f4-409">La sequenziazione per l'ottimizzazione del flusso è disponibile all'indirizzo: <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="0b8f4-410">Aggiornamenti del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-410">Package upgrades</span></span>

<span data-ttu-id="0b8f4-411">I pacchetti App-V richiedono l'aggiornamento per tutto il ciclo di vita dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="0b8f4-412">Gli aggiornamenti del pacchetto App-V sono simili all'operazione di pubblicazione del pacchetto, poiché ogni versione verrà creata nella propria posizione di PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="0b8f4-413">L'operazione di aggiornamento è ottimizzata creando collegamenti rigidi a file identici e in streaming da altre versioni dello stesso pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="0b8f4-414">Rimozione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-414">Package removal</span></span>

<span data-ttu-id="0b8f4-415">Il comportamento del client App-V quando i pacchetti vengono rimossi dipende dal metodo usato per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="0b8f4-416">Usando un'infrastruttura completa di App-V per annullare la pubblicazione dell'applicazione, i file di catalogo degli utenti (Catalogo macchine per le applicazioni pubblicate a livello globale) vengono rimossi, ma conservano la posizione e le posizioni della mucca nello Store del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="0b8f4-417">Quando `Remove-AppVClientPackge` si usa il cmdlet di PowerShell per rimuovere un pacchetto di App-V, la posizione dell'archivio pacchetti viene pulita.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="0b8f4-418">Tenere presente che l'annullamento della pubblicazione di un pacchetto App-V dal server di gestione non esegue un'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="0b8f4-419">Nessuna delle due operazioni rimuoverà i file del pacchetto di archiviazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="0b8f4-420">Registro di sistema e dati mobili</span><span class="sxs-lookup"><span data-stu-id="0b8f4-420">Roaming registry and data</span></span>


<span data-ttu-id="0b8f4-421">App-V 5 è in grado di creare un'esperienza quasi nativa durante il roaming, a seconda di come viene scritta l'applicazione usata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="0b8f4-422">Per impostazione predefinita, App-V fa roaming AppData archiviato nel percorso di roaming, in base alla configurazione del roaming del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="0b8f4-423">In altre posizioni per l'archiviazione dei dati basati su file non è possibile eseguire il roaming da computer a computer, poiché si trovano in posizioni non in roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="0b8f4-424">Requisiti di roaming e archiviazione dei dati del catalogo degli utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="0b8f4-425">App-V archivia i dati, che rappresentano lo stato del catalogo dell'utente, sotto forma di:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="0b8f4-426">File in%appdata%\\Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="0b8f4-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="0b8f4-427">Impostazioni del registro di sistema in</span><span class="sxs-lookup"><span data-stu-id="0b8f4-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="0b8f4-428">Insieme, questi file e le impostazioni del registro di sistema rappresentano il catalogo dell'utente, quindi entrambi devono essere in roaming oppure non devono essere spostati in roaming per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="0b8f4-429">App-V non supporta il roaming% AppData%, ma non il roaming del profilo dell'utente (registro di sistema) o viceversa.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="0b8f4-430">**Nota**  Il cmdlet **Repair-AppvClientPackage** non ripristina lo stato di pubblicazione dei pacchetti, dove lo stato dell'App-V dell'utente in `HKEY_CURRENT_USER` è mancante o non corrisponde ai dati in% AppData%.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="0b8f4-431">Dati basati sul Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0b8f4-431">Registry-based data</span></span>

<span data-ttu-id="0b8f4-432">Il roaming del registro di sistema di App-V rientra in due scenari, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-433">Scenario</span><span class="sxs-lookup"><span data-stu-id="0b8f4-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-434">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-435">Applicazioni eseguite come utenti standard</span><span class="sxs-lookup"><span data-stu-id="0b8f4-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-436">Quando un utente standard avvia un'applicazione App-V, sia HKLM che HKCU per le applicazioni App-V vengono archiviati nell'hive HKCU nel computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="0b8f4-437">Questo si presenta come due percorsi distinti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="0b8f4-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="0b8f4-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="0b8f4-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="0b8f4-440">Le posizioni sono abilitate per il roaming in base alle impostazioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-441">Applicazioni eseguite con l'elevazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-442">Quando un'applicazione viene avviata con l'elevazione:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="0b8f4-443">I dati HKLM sono archiviati nell'hive HKLM nel computer locale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-444">I dati HKCU vengono archiviati nel percorso del registro di sistema dell'utente</span><span class="sxs-lookup"><span data-stu-id="0b8f4-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="0b8f4-445">In questo scenario, queste impostazioni non vengono spostate in roaming con le normali configurazioni di roaming del sistema operativo e le chiavi e i valori dei registri risultanti sono archiviati nella posizione seguente:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="0b8f4-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="0b8f4-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="0b8f4-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="0b8f4-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0b8f4-448">App-V e reindirizzamento delle cartelle</span><span class="sxs-lookup"><span data-stu-id="0b8f4-448">App-V and folder redirection</span></span>

<span data-ttu-id="0b8f4-449">App-V 5,1 supporta il reindirizzamento delle cartelle della cartella AppData Roaming (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-449">App-V 5.1 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="0b8f4-450">Quando l'ambiente virtuale viene avviato, lo stato di AppData Roaming dalla directory AppData Roaming dell'utente viene copiato nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="0b8f4-451">Viceversa, quando l'ambiente virtuale viene arrestato, la cache locale associata al AppData Roaming di un utente specifico viene trasferita nella posizione effettiva della directory AppData Roaming di tale utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="0b8f4-452">Un pacchetto tipico include diverse posizioni mappate nell'archivio di backup dell'utente per le impostazioni sia in AppData\\Local che in AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="0b8f4-453">Questi percorsi sono la copia nei percorsi di scrittura archiviati per ogni utente nel profilo dell'utente e usati per archiviare le modifiche apportate alle directory del pacchetto VFS e per proteggere il pacchetto VFS predefinito.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="0b8f4-454">La tabella seguente mostra le posizioni locali e di roaming, quando il reindirizzamento delle cartelle non è stato implementato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-455">Directory VFS nel pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-456">Percorso mappato dell'archivio di backup</span><span class="sxs-lookup"><span data-stu-id="0b8f4-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-458">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-460">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-461">Windows</span><span class="sxs-lookup"><span data-stu-id="0b8f4-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-462">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="0b8f4-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="0b8f4-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-464">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="0b8f4-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-465">AppData</span><span class="sxs-lookup"><span data-stu-id="0b8f4-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-466">C:\users\jsmith\AppData &lt; forte &gt; roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="0b8f4-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="0b8f4-467">La tabella seguente mostra le posizioni locali e di roaming, quando il reindirizzamento delle cartelle è stato implementato per% AppData% e la posizione è stata reindirizzata (in genere in un percorso di rete).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-468">Directory VFS nel pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-469">Percorso mappato dell'archivio di backup</span><span class="sxs-lookup"><span data-stu-id="0b8f4-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-471">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-473">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="0b8f4-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-474">Windows</span><span class="sxs-lookup"><span data-stu-id="0b8f4-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-475">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="0b8f4-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="0b8f4-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-477">C:\users\jsmith\AppData &lt; Strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="0b8f4-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-478">AppData</span><span class="sxs-lookup"><span data-stu-id="0b8f4-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="0b8f4-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="0b8f4-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="0b8f4-480">Il driver di App-V client VFS corrente non può scrivere nei percorsi di rete, in modo che il client App-V rilevi la presenza del reindirizzamento delle cartelle e copi i dati nell'unità locale durante la pubblicazione e quando l'ambiente virtuale viene avviato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="0b8f4-481">Dopo che l'utente ha chiuso l'applicazione App-V e il client App-V chiude l'ambiente virtuale, l'archiviazione locale di VFS AppData viene copiata di nuovo nella rete, consentendo il roaming ad altri computer, in cui il processo verrà ripetuto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="0b8f4-482">La procedura dettagliata dei processi è:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="0b8f4-483">Durante l'avvio della pubblicazione o dell'ambiente virtuale, il client App-V rileva la posizione della directory AppData.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="0b8f4-484">Se il percorso AppData Roaming è locale o viene mappato il percorso di AppData\\Roaming, non succede nulla.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="0b8f4-485">Se il percorso AppData Roaming non è locale, la directory VFS AppData viene mappata alla directory AppData locale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="0b8f4-486">Questo processo risolve il problema di un% AppData% non locale che non è supportato dal driver di App-V client VFS.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="0b8f4-487">I dati archiviati in questa nuova posizione non vengono tuttavia spostati in roaming con il reindirizzamento delle cartelle.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="0b8f4-488">Tutte le modifiche durante l'utilizzo dell'applicazione si verificano nella posizione AppData locale e devono essere copiate nella posizione reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="0b8f4-489">I passaggi dettagliati di questo processo sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="0b8f4-490">L'applicazione App-V viene chiusa, che arresta l'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="0b8f4-491">La cache locale della posizione AppData in roaming viene compressa e archiviata in un file ZIP.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="0b8f4-492">Un timestamp alla fine del processo di creazione di pacchetti ZIP viene usato per assegnare un nome al file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="0b8f4-493">Il timestamp viene registrato nel registro di sistema: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime come ultimo timestamp noto di AppData.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="0b8f4-494">Il processo di reindirizzamento delle cartelle viene chiamato per valutare e avviare il file ZIP caricato nella directory AppData Roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="0b8f4-495">Il timestamp viene usato per determinare lo scenario "ultimo autore WINS" se esiste un conflitto e viene usato per ottimizzare il download dei dati quando viene pubblicata l'applicazione App-V o viene avviato l'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="0b8f4-496">Il reindirizzamento delle cartelle rende disponibili i dati da qualsiasi altro client coperto dai criteri di supporto e avvia il processo di archiviazione dei dati di AppData\\Roaming nella posizione AppData locale del client.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="0b8f4-497">I processi dettagliati sono:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="0b8f4-498">L'utente avvia l'ambiente virtuale avviando un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="0b8f4-499">L'ambiente virtuale dell'applicazione controlla l'ora più recente del file ZIP con timbro, se presente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="0b8f4-500">Il registro di sistema viene controllato per l'ultimo timestamp caricato noto, se presente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="0b8f4-501">Il file ZIP più recente viene scaricato a meno che il timestamp dell'ultimo caricamento noto locale sia maggiore o uguale al timestamp del file ZIP.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="0b8f4-502">Se l'ultimo timestamp di caricamento noto locale è precedente rispetto a quello del file ZIP più recente nella posizione AppData in roaming, il file ZIP viene estratto nella directory Temp locale nel profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="0b8f4-503">Dopo che il file ZIP viene estratto correttamente, la cache locale della directory AppData Roaming viene rinominata e i nuovi dati vengono spostati in posizione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="0b8f4-504">La directory rinominata viene eliminata e l'applicazione si apre con i dati comuni di roaming salvati più di recente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="0b8f4-505">Questa operazione completa il roaming corretto delle impostazioni dell'applicazione presenti nei percorsi di AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="0b8f4-506">L'unica altra condizione che deve essere affrontata è un'operazione di ripristino del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="0b8f4-507">I dettagli del processo sono:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-507">The details of the process are:</span></span>

1.  <span data-ttu-id="0b8f4-508">Durante il ripristino, rilevare se il percorso della directory AppData Roaming dell'utente non è locale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="0b8f4-509">Mappare le destinazioni del percorso AppData non locali per il roaming vengono ricreate le posizioni di roaming e AppData locali previste.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="0b8f4-510">Eliminare il timestamp archiviato nel registro di sistema, se presente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="0b8f4-511">Questo processo ricrea sia le posizioni locali che quelle di rete per AppData e rimuove il record del registro di sistema del timestamp.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="0b8f4-512">Gestione del ciclo di vita dell'applicazione client App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="0b8f4-513">In un'infrastruttura completa di App-V, dopo la sequenziazione delle applicazioni, queste vengono gestite e pubblicate in utenti o computer tramite i server di gestione e pubblicazione di App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="0b8f4-514">Questa sezione descrive in dettaglio le operazioni che si verificano durante le operazioni comuni di ciclo di vita delle applicazioni App-V (aggiungere, pubblicare, avviare, aggiornare e rimuovere) e le posizioni di file e del registro di sistema modificate e modificate dal punto di vista del client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="0b8f4-515">Le operazioni client App-V vengono eseguite come una serie di comandi di PowerShell avviati nel computer che esegue il client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="0b8f4-516">Questo documento si incentra sulle soluzioni per l'infrastruttura completa di App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="0b8f4-517">Per informazioni specifiche sull'integrazione di App-V con Configuration Manager 2012, visitare il sito: <https://go.microsoft.com/fwlink/?LinkId=392773> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="0b8f4-518">Le attività del ciclo di vita dell'applicazione App-V vengono attivate all'accesso dell'utente (impostazione predefinita), all'avvio del computer o alle operazioni temporizzate in background.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="0b8f4-519">Le impostazioni per le operazioni client App-V, inclusi i server di pubblicazione, gli intervalli di aggiornamento, l'abilitazione dello script del pacchetto e altre, vengono configurate durante l'installazione del client o post-installazione con i comandi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="0b8f4-520">Vedere la sezione come distribuire il client in TechNet all'indirizzo: [come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md) o utilizzare PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="0b8f4-521">Aggiornamento pubblicazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-521">Publishing refresh</span></span>

<span data-ttu-id="0b8f4-522">Il processo di aggiornamento della pubblicazione è costituito da diverse operazioni più piccole eseguite nel client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="0b8f4-523">Poiché App-V è una tecnologia di virtualizzazione delle applicazioni e non una tecnologia di pianificazione delle attività, l'utilità di pianificazione di Windows viene utilizzata per abilitare il processo all'accesso dell'utente, all'avvio del computer e a intervalli pianificati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="0b8f4-524">La configurazione del client durante l'installazione di cui sopra è il metodo preferito durante la distribuzione del client a un numero elevato di computer con le impostazioni corrette.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="0b8f4-525">Queste impostazioni client possono essere configurate con i cmdlet di PowerShell seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="0b8f4-526">**Add-AppVPublishingServer:** Configura il client con un server di pubblicazione App-V che fornisce pacchetti App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="0b8f4-527">**Set-AppVPublishingServer:** Modifica le impostazioni correnti per il server di pubblicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="0b8f4-528">**Set-AppVClientConfiguration:** Modifica le impostazioni correnti per il client App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="0b8f4-529">**Sincronizzazione-AppVPublishingServer:** Avvia manualmente un processo di aggiornamento della pubblicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="0b8f4-530">Questa operazione viene utilizzata anche nelle attività pianificate create durante la configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="0b8f4-531">Lo stato principale delle sezioni seguenti consiste nel dettaglio delle operazioni che si verificano durante le diverse fasi di un aggiornamento della pubblicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="0b8f4-532">Gli argomenti includono:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-532">The topics include:</span></span>

-   <span data-ttu-id="0b8f4-533">Aggiunta di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="0b8f4-534">Pubblicazione di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="0b8f4-535">Aggiunta di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-535">Adding an App-V package</span></span>

<span data-ttu-id="0b8f4-536">L'aggiunta di un pacchetto App-V al client è il primo passaggio del processo di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="0b8f4-537">Il risultato finale è uguale al `Add-AppVClientPackage` cmdlet in PowerShell, eccetto durante il processo di aggiunta dell'aggiornamento della pubblicazione, il server di pubblicazione configurato viene contattato e passa un elenco di applicazioni di alto livello al client per ottenere informazioni più dettagliate e non una singola operazione di aggiunta di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="0b8f4-538">Il processo continua configurando il client per le aggiunte o gli aggiornamenti del gruppo di connessioni o pacchetti, quindi accede al file AppV.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="0b8f4-539">Il contenuto del file appv viene quindi espanso e inserito nel sistema operativo locale nelle posizioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="0b8f4-540">Di seguito è riportato un flusso di lavoro dettagliato del processo, presupponendo che il pacchetto sia configurato per il flusso di errore.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="0b8f4-541">Come aggiungere un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="0b8f4-542">Avvio manuale tramite l'avvio di PowerShell o sequenza di attività del processo di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="0b8f4-543">Il client App-V effettua una connessione HTTP e richiede un elenco di applicazioni in base alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="0b8f4-544">Il processo di aggiornamento della pubblicazione supporta i computer o gli utenti di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="0b8f4-545">Il server di pubblicazione App-V usa l'identità della destinazione, dell'utente o del computer iniziale e interroga il database per un elenco di applicazioni intitolate.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="0b8f4-546">L'elenco delle applicazioni viene fornito come risposta XML, che il client usa per inviare ulteriori richieste al server per ottenere altre informazioni su una base per pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="0b8f4-547">L'agente di pubblicazione nel client App-V esegue tutte le azioni sotto serializzate.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="0b8f4-548">Valutare eventuali gruppi di connessioni non pubblicati o disabilitati, poiché gli aggiornamenti della versione del pacchetto che fanno parte del gruppo di connessioni non possono essere elaborati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="0b8f4-549">Configurare i pacchetti identificando le operazioni di aggiunta o aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="0b8f4-550">Il client App-V usa l'API AppX da Windows e accede al file appv dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="0b8f4-551">Il file del pacchetto viene aperto e i AppXManifest.xml e StreamMap.xml vengono scaricati nell'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="0b8f4-552">Completamente i dati del blocco di pubblicazione in streaming definiti nella StreamMap.xml.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="0b8f4-553">Archivia i dati del blocco di pubblicazione nel pacchetto Store\\PkgGUID\\VerGUID\\Root.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="0b8f4-554">Icone: destinazioni dei punti di estensione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="0b8f4-555">Intestazioni eseguibili portatili (intestazioni PE): destinazioni di punti di estensione che contengono le informazioni di base sulle esigenze di immagine su disco, accessibili direttamente o tramite tipi di file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="0b8f4-556">Script: scaricare la directory scripts per l'uso durante il processo di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="0b8f4-557">Popolare l'archivio pacchetti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="0b8f4-558">Creare file sparsi su disco che rappresentano il pacchetto estratto per qualsiasi directory elencata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="0b8f4-559">Organizzare file e directory di primo livello in root.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="0b8f4-560">Tutti gli altri file vengono creati quando la directory è elencata come sparsa su disco e trasmessa su richiesta.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="0b8f4-561">Creare le voci del catalogo del computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-561">Create the machine catalog entries.</span></span> <span data-ttu-id="0b8f4-562">Creare la Manifest.xml e DeploymentConfiguration.xml dai file del pacchetto (se non è stato creato alcun file di DeploymentConfiguration.xml nel pacchetto).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="0b8f4-563">Creare la posizione dell'archivio pacchetti nel registro di sistema HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span><span class="sxs-lookup"><span data-stu-id="0b8f4-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="0b8f4-564">Creare il file Registry. dat dall'archivio pacchetti in%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat</span><span class="sxs-lookup"><span data-stu-id="0b8f4-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="0b8f4-565">Registrare il pacchetto con il driver della modalità kernel App-V HKLM\\Microsoft\\Software\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="0b8f4-566">Richiamare gli script dal file AppxManifest.xml o DeploymentConfig.xml per aggiungere un intervallo di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="0b8f4-567">Configurare i gruppi di connessioni aggiungendo e abilitando o disabilitando.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="0b8f4-568">Rimuovere gli oggetti non pubblicati nella destinazione (utente o computer).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="0b8f4-569">**Nota**  In questo modo non verrà eseguita l'eliminazione di un pacchetto, ma si rimuovono i punti di integrazione per il target specifico (utente o computer) e si rimuovono i file di catalogo degli utenti (file catalogo computer per la pubblicazione globale).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="0b8f4-570">Richiamare il supporto del caricamento in background in base alla configurazione client.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="0b8f4-571">I pacchetti che hanno già informazioni sulla pubblicazione per il computer o l'utente vengono immediatamente ripristinati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="0b8f4-572">**Nota**  Questa condizione si verifica come prodotto della rimozione senza l'annullamento della pubblicazione con l'aggiunta di sfondo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="0b8f4-573">Viene completato un pacchetto App-V che aggiunge il processo di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="0b8f4-574">Il passaggio successivo consiste nel pubblicare il pacchetto nella destinazione specifica (computer o utente).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![pacchetto Aggiungi file e dati del registro di sistema](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="0b8f4-576">Pubblicazione di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-576">Publishing an App-V package</span></span>

<span data-ttu-id="0b8f4-577">Durante l'operazione di aggiornamento della pubblicazione, l'operazione di pubblicazione specifica (Publish-AppVClientPackage) aggiunge voci al catalogo utenti, associa l'autorizzazione all'utente, identifica l'archivio locale e termina completando i passaggi di integrazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="0b8f4-578">Di seguito sono illustrati i passaggi dettagliati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="0b8f4-579">Come pubblicare e pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="0b8f4-580">Le voci del pacchetto vengono aggiunte al catalogo utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="0b8f4-581">Pacchetti mirati dall'utente: le UserDeploymentConfiguration.xml e le UserManifest.xml vengono posizionate nel computer del catalogo utenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="0b8f4-582">Pacchetti di destinazione del computer (globali): la UserDeploymentConfiguration.xml viene inserita nel catalogo del computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="0b8f4-583">Registrare il pacchetto con il driver in modalità kernel per l'utente su HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="0b8f4-584">Eseguire attività di integrazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="0b8f4-585">Creare punti di estensione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-585">Create extension points.</span></span>

    2.  <span data-ttu-id="0b8f4-586">Archiviare le informazioni di backup nel registro di sistema e nel profilo di roaming dell'utente (backup dei collegamenti).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="0b8f4-587">**Nota**  Questo consente di ripristinare i punti di estensione se il pacchetto non è pubblicato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="0b8f4-588">Eseguire script mirati per l'intervallo di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="0b8f4-589">La pubblicazione di un pacchetto App-V che fa parte di un gruppo di connessioni è molto simile al processo precedente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="0b8f4-590">Per i gruppi di connessioni, il percorso in cui sono archiviate le informazioni specifiche del catalogo include PackageGroups come elemento figlio della directory del catalogo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="0b8f4-591">Per informazioni dettagliate, vedere il catalogo computer e gli utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-591">Review the machine and users catalog information above for details.</span></span>

![pacchetto Aggiungi file e dati del registro di sistema-globale](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="0b8f4-593">Avvio di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-593">Application launch</span></span>

<span data-ttu-id="0b8f4-594">Dopo il processo di aggiornamento della pubblicazione, l'utente avvia e successivamente riavvia un'applicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="0b8f4-595">Il processo è molto semplice e ottimizzato per l'avvio rapido con un minimo di traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="0b8f4-596">Il client App-V controlla il percorso del catalogo utente per i file creati durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="0b8f4-597">Dopo aver stabilito i diritti per l'avvio del pacchetto, il client App-V crea un ambiente virtuale, inizia a trasmettere i dati necessari e applica i file di configurazione del manifesto e della distribuzione appropriati durante la creazione di ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="0b8f4-598">Con l'ambiente virtuale creato e configurato per il pacchetto e l'applicazione specifici, viene avviata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="0b8f4-599">Come avviare le applicazioni App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="0b8f4-600">L'utente avvia l'applicazione facendo clic su un collegamento o una chiamata di tipo file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="0b8f4-601">Il client App-V Verifica l'esistenza nel catalogo utente per i file seguenti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="0b8f4-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="0b8f4-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="0b8f4-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="0b8f4-604">Se i file sono presenti, l'applicazione ha diritto a tale utente specifico e l'applicazione avvierà il processo per l'avvio.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="0b8f4-605">A questo punto non esiste un traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="0b8f4-606">Il client App-V Verifica quindi che il percorso del pacchetto registrato per il servizio client App-V si trovi nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="0b8f4-607">Dopo aver trovato il percorso dell'archivio pacchetti, viene creato l'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="0b8f4-608">Se si tratta del primo avvio, il blocco di funzionalità principale verrà scaricato se presente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="0b8f4-609">Dopo il download, il servizio client App-V usa i file di configurazione del manifesto e della distribuzione per configurare l'ambiente virtuale e tutti i sottosistemi App-V caricati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="0b8f4-610">L'applicazione viene avviata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-610">The Application launches.</span></span> <span data-ttu-id="0b8f4-611">Per tutti i file mancanti nell'archivio dei pacchetti (file sparsi), l'App-V scaricherà i file in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![pacchetto Aggiungi file e dati del registro di sistema-Stream](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="0b8f4-613">Aggiornamento di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-613">Upgrading an App-V package</span></span>

<span data-ttu-id="0b8f4-614">Il processo di aggiornamento del pacchetto App-V 5 si differenzia dalle versioni precedenti di App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="0b8f4-615">App-V supporta più versioni dello stesso pacchetto in un computer avente diritto a utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="0b8f4-616">Le versioni del pacchetto possono essere aggiunte in qualsiasi momento, in quanto l'archivio dei pacchetti e i cataloghi vengono aggiornati con le nuove risorse.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="0b8f4-617">L'unico processo specifico per l'aggiunta delle nuove risorse della versione è l'ottimizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="0b8f4-618">Durante un aggiornamento, solo i nuovi file vengono aggiunti alla nuova posizione dell'archivio versioni e i collegamenti rigidi vengono creati per i file non modificati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="0b8f4-619">In questo modo si riduce l'archiviazione complessiva solo presentando il file in una posizione del disco e quindi proiettando in tutte le cartelle con una voce di posizione del file sul disco.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="0b8f4-620">I dettagli specifici dell'aggiornamento di un pacchetto App-V sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="0b8f4-621">Come aggiornare un pacchetto di App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="0b8f4-622">Il client App-V esegue un aggiornamento della pubblicazione e individua una versione più recente di un pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="0b8f4-623">Le voci del pacchetto vengono aggiunte al catalogo appropriato per la nuova versione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="0b8f4-624">Pacchetti mirati dall'utente: le UserDeploymentConfiguration.xml e le UserManifest.xml vengono posizionate nel computer nel catalogo utenti in appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="0b8f4-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="0b8f4-625">Pacchetti di destinazione del computer (globali): la UserDeploymentConfiguration.xml viene inserita nel catalogo computer in%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="0b8f4-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="0b8f4-626">Registrare il pacchetto con il driver in modalità kernel per l'utente su HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="0b8f4-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="0b8f4-627">Eseguire attività di integrazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="0b8f4-628">Integrare i punti estensioni (EP) dai file di configurazione manifesto e dinamico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="0b8f4-629">I dati EP basati su file sono archiviati nella cartella AppData che utilizza punti di giunzione dall'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="0b8f4-630">La versione 1 EPs esiste già quando una nuova versione diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="0b8f4-631">I punti di estensione vengono passati alla posizione della versione 2 in cataloghi di computer o utenti per eventuali punti di estensione più recenti o aggiornati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="0b8f4-632">Eseguire script mirati per l'intervallo di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="0b8f4-633">Installare gli assembly affiancati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="0b8f4-634">Aggiornamento di un pacchetto App-V in uso</span><span class="sxs-lookup"><span data-stu-id="0b8f4-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="0b8f4-635">A **partire da App-V 5 SP2**: se si tenta di aggiornare un pacchetto in uso da parte di un utente finale, l'attività di aggiornamento viene inserita in uno stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="0b8f4-636">L'aggiornamento verrà eseguito in un secondo momento, in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-637">Tipo di attività</span><span class="sxs-lookup"><span data-stu-id="0b8f4-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-638">Regola applicabile</span><span class="sxs-lookup"><span data-stu-id="0b8f4-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-639">Attività basata su utenti, ad esempio, pubblicazione di un pacchetto in un utente</span><span class="sxs-lookup"><span data-stu-id="0b8f4-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-640">L'attività in sospeso verrà eseguita dopo la disattivazione dell'utente e quindi il log di nuovo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-641">Attività basata su base globale, ad esempio, che consente a un gruppo di connessioni a livello globale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-642">L'attività in sospeso verrà eseguita quando il computer viene arrestato e quindi riavviato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0b8f4-643">Quando un'attività viene inserita in uno stato in sospeso, il client App-V genera anche una chiave del registro di sistema per l'attività in sospeso, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-644">Attività basata su utenti o globale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-645">Dove viene generata la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0b8f4-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-646">Attività basate sull'utente</span><span class="sxs-lookup"><span data-stu-id="0b8f4-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-647">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="0b8f4-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-648">Attività basate su base globale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-649">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="0b8f4-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0b8f4-650">Le operazioni seguenti devono essere completate prima che gli utenti possano usare la versione più recente del pacchetto:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-651">Attività</span><span class="sxs-lookup"><span data-stu-id="0b8f4-651">Task</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-652">Dettagli</span><span class="sxs-lookup"><span data-stu-id="0b8f4-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-653">Aggiungere il pacchetto al computer</span><span class="sxs-lookup"><span data-stu-id="0b8f4-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-654">Questa attività è specifica del computer ed è possibile eseguirla in qualsiasi momento completando i passaggi della sezione Aggiungi pacchetto precedente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-655">Pubblicare il pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-656">Vedere la sezione pubblicazione del pacchetto sopra per i passaggi.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="0b8f4-657">Questo processo richiede l'aggiornamento dei punti di estensione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="0b8f4-658">Gli utenti finali non possono usare l'applicazione quando si completa questa attività.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0b8f4-659">Usare gli scenari di esempio seguenti come guida per l'aggiornamento dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-660">Scenario</span><span class="sxs-lookup"><span data-stu-id="0b8f4-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-661">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b8f4-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-662">Il pacchetto App-V non è in uso quando si tenta di eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0b8f4-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-663">Nessuno dei componenti seguenti del pacchetto può essere in uso: applicazione virtuale, server COM o estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="0b8f4-664">L'amministratore pubblica una versione più recente del pacchetto e l'aggiornamento funziona la volta successiva che viene avviato un componente o un'applicazione all'interno del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="0b8f4-665">La nuova versione del pacchetto è in streaming ed è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="0b8f4-666">Questo scenario non è stato modificato in App-V 5 SP2 dalle versioni precedenti di App-V 5.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-667">Il pacchetto App-V è in uso quando l'amministratore pubblica una versione più recente del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-668">L'operazione di aggiornamento è impostata su in sospeso dal client App-V, il che significa che viene accodato e eseguito in seguito quando il pacchetto non è in uso.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="0b8f4-669">Se l'applicazione pacchetto è in uso, l'utente arresta l'applicazione virtuale, dopo la quale può essere eseguito l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="0b8f4-670">Se il pacchetto include estensioni della shell (Office 2013), che vengono caricate in modo permanente da Esplora risorse, l'utente non può essere connesso.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="0b8f4-671">Gli utenti devono disconnettersi e accedere di nuovo per avviare l'aggiornamento del pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0b8f4-672">Pubblicazione globale degli utenti vs</span><span class="sxs-lookup"><span data-stu-id="0b8f4-672">Global vs user publishing</span></span>

<span data-ttu-id="0b8f4-673">I pacchetti App-V possono essere pubblicati in uno dei due modi seguenti: Utente che dà diritto a un pacchetto di App-V a un utente o un gruppo di utenti specifico e globale che dà diritto al pacchetto App-V a tutto il computer per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="0b8f4-674">Una volta che un aggiornamento del pacchetto è stato sospeso e il pacchetto App-V non è in uso, prendere in considerazione i due tipi di pubblicazione:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="0b8f4-675">**Pubblicazione globale**: l'applicazione viene pubblicata in un computer; tutti gli utenti del computer possono usarlo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="0b8f4-676">L'aggiornamento avverrà quando viene avviato il servizio client App-V, che significa effettivamente riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="0b8f4-677">**Utente pubblicato**: l'applicazione viene pubblicata in un utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="0b8f4-678">Se nel computer sono presenti più utenti, è possibile che l'applicazione venga pubblicata in un sottoinsieme degli utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="0b8f4-679">L'aggiornamento avverrà quando l'utente accede o quando viene pubblicato di nuovo (periodicamente, ConfigMgr aggiornamento dei criteri e valutazione o una pubblicazione/aggiornamento periodico di App-V o in modo esplicito tramite i comandi di PowerShell).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="0b8f4-680">Rimozione di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-680">Removing an App-V package</span></span>

<span data-ttu-id="0b8f4-681">La rimozione delle applicazioni App-V in un'infrastruttura completa è un'operazione di annullamento della pubblicazione e non esegue una rimozione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="0b8f4-682">Il processo è uguale al processo di pubblicazione precedente, ma invece di aggiungere il processo di rimozione Annulla le modifiche apportate per i pacchetti di App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="0b8f4-683">Ripristino di un pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-683">Repairing an App-V package</span></span>

<span data-ttu-id="0b8f4-684">L'operazione di ripristino è molto semplice, ma può interessare molte posizioni nel computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="0b8f4-685">Vengono rimosse le posizioni di copia in scrittura (mucca) in precedenza e i punti di estensione vengono disintegrati e quindi reintegrati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="0b8f4-686">Esaminare le posizioni di posizionamento dei dati della mucca rivedendo il punto in cui sono registrate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="0b8f4-687">Questa operazione viene eseguita automaticamente e non esiste un controllo amministrativo diverso dall'avvio di un'operazione di ripristino dalla console client App-V o tramite PowerShell (Repair-AppVClientPackage).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="0b8f4-688">Integrazione dei pacchetti App-V</span><span class="sxs-lookup"><span data-stu-id="0b8f4-688">Integration of App-V packages</span></span>


<span data-ttu-id="0b8f4-689">L'architettura client e pacchetto App-V offre un'integrazione specifica con il sistema operativo locale durante l'aggiunta e la pubblicazione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="0b8f4-690">Tre file definiscono i punti di integrazione o di estensione per un pacchetto di App-V:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="0b8f4-691">AppXManifest.xml: archiviato all'interno del pacchetto con le copie di fallback archiviate nell'archivio pacchetti e nel profilo utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="0b8f4-692">Contiene le opzioni create durante il processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="0b8f4-693">DeploymentConfig.xml: fornisce informazioni sulla configurazione dei punti di estensione di integrazione basati su computer e utenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="0b8f4-694">UserConfig.xml: un sottoinsieme della Deploymentconfig.xml che fornisce solo configurazioni basate sull'utente e solo i punti di estensione basati sull'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="0b8f4-695">Regole di integrazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-695">Rules of integration</span></span>

<span data-ttu-id="0b8f4-696">Quando le applicazioni App-V vengono pubblicate in un computer con il client App-V, alcune azioni specifiche avvengono come descritto nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="0b8f4-697">Pubblicazione globale: i tasti di scelta rapida sono archiviati nella posizione tutti i profili degli utenti e altri punti di estensione sono archiviati nel registro di sistema dell'hive HKLM.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="0b8f4-698">Pubblicazione degli utenti: i tasti di scelta rapida sono archiviati nel profilo dell'account utente corrente e altri punti di estensione vengono archiviati nel registro di sistema nell'hive HKCU.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="0b8f4-699">Backup e ripristino: i dati e il registro di sistema esistenti delle applicazioni native (ad esempio le registrazioni FTA) vengono copiati durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="0b8f4-700">I pacchetti App-V vengono assegnati alla proprietà in base all'ultimo pacchetto integrato in cui la proprietà viene passata alla più recente applicazione App-V pubblicata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="0b8f4-701">I trasferimenti di proprietà da un pacchetto di App-V a un altro quando il pacchetto dell'App-V proprietario è inedito.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="0b8f4-702">In questo modo non verrà avviato un ripristino dei dati o del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="0b8f4-703">Ripristinare i dati di cui è stato eseguito il backup quando l'ultimo pacchetto non viene pubblicato o rimosso in base al punto di estensione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="0b8f4-704">Punti di estensione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-704">Extension points</span></span>

<span data-ttu-id="0b8f4-705">I file di pubblicazione App-V (manifesto e configurazione dinamica) offrono diversi punti di estensione che consentono all'applicazione di integrarsi con il sistema operativo locale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="0b8f4-706">Questi punti di estensione eseguono le tipiche attività di installazione delle applicazioni, ad esempio l'immissione di collegamenti, la creazione di associazioni di tipi di file e la registrazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="0b8f4-707">Poiché si tratta di applicazioni virtualizzate che non sono installate allo stesso modo di un'applicazione tradizionale, esistono alcune differenze.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="0b8f4-708">Di seguito è riportato un elenco di punti di estensione descritti in questa sezione:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="0b8f4-709">Scorciatoie</span><span class="sxs-lookup"><span data-stu-id="0b8f4-709">Shortcuts</span></span>

-   <span data-ttu-id="0b8f4-710">Associazioni di tipi di file</span><span class="sxs-lookup"><span data-stu-id="0b8f4-710">File Type Associations</span></span>

-   <span data-ttu-id="0b8f4-711">Estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="0b8f4-711">Shell Extensions</span></span>

-   <span data-ttu-id="0b8f4-712">COM</span><span class="sxs-lookup"><span data-stu-id="0b8f4-712">COM</span></span>

-   <span data-ttu-id="0b8f4-713">Client software</span><span class="sxs-lookup"><span data-stu-id="0b8f4-713">Software Clients</span></span>

-   <span data-ttu-id="0b8f4-714">Funzionalità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-714">Application capabilities</span></span>

-   <span data-ttu-id="0b8f4-715">Gestore protocollo URL</span><span class="sxs-lookup"><span data-stu-id="0b8f4-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="0b8f4-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="0b8f4-716">AppPath</span></span>

-   <span data-ttu-id="0b8f4-717">Applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-717">Virtual Application</span></span>

### <span data-ttu-id="0b8f4-718">Scorciatoie</span><span class="sxs-lookup"><span data-stu-id="0b8f4-718">Shortcuts</span></span>

<span data-ttu-id="0b8f4-719">La scorciatoia è uno degli elementi di base per l'integrazione con il sistema operativo ed è l'interfaccia per l'avvio diretto degli utenti di un'applicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="0b8f4-720">Durante la pubblicazione e l'annullamento della pubblicazione delle applicazioni App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="0b8f4-721">Dal manifesto del pacchetto e dai file XML di configurazione dinamica, il percorso di un eseguibile specifico dell'applicazione può essere trovato in una sezione simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="0b8f4-722">Come accennato in precedenza, i tasti di scelta rapida dell'App-V vengono posizionati per impostazione predefinita nel profilo dell'utente in base all'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="0b8f4-723">Le scelte rapide da tastiera di aggiornamento globale sono memorizzate nel profilo di tutti gli utenti e l'aggiornamento dell'utente viene archiviato nello specifico utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="0b8f4-724">L'eseguibile effettivo viene archiviato nell'archivio pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="0b8f4-725">La posizione del file ICO è una posizione in formato token nel pacchetto App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="0b8f4-726">Associazioni di tipi di file</span><span class="sxs-lookup"><span data-stu-id="0b8f4-726">File type associations</span></span>

<span data-ttu-id="0b8f4-727">Il client App-V gestisce le associazioni dei tipi di file del sistema operativo locale durante la pubblicazione, che consente agli utenti di usare le chiamate di tipo file o di aprire un file con estensione docx specificatamente registrata per avviare un'applicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="0b8f4-728">Le associazioni di tipi di file sono presenti nei file di configurazione manifesto e dinamico come rappresentato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="0b8f4-729">**Nota**  In questo esempio:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="0b8f4-730">è l'estensione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="0b8f4-731">è il valore ProgId (che punta al ProgId adiacente)</span><span class="sxs-lookup"><span data-stu-id="0b8f4-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="0b8f4-732">è la riga di comando, che punta al file eseguibile dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="0b8f4-733">Estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="0b8f4-733">Shell extensions</span></span>

<span data-ttu-id="0b8f4-734">Le estensioni della shell vengono inserite automaticamente nel pacchetto durante il processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="0b8f4-735">Quando il pacchetto viene pubblicato globalmente, l'estensione della Shell offre agli utenti le stesse funzionalità di se l'applicazione è stata installata localmente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="0b8f4-736">L'applicazione non richiede alcuna installazione o configurazione aggiuntiva nel client per abilitare la funzionalità di estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="0b8f4-737">Requisiti per l'uso delle estensioni della shell:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="0b8f4-738">I pacchetti che contengono estensioni della shell incorporata devono essere pubblicati globalmente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="0b8f4-739">Il "bit" dell'applicazione, il sequencer e il client App-V devono corrispondere o le estensioni della shell non funzionano.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="0b8f4-740">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-740">For example:</span></span>

    -   <span data-ttu-id="0b8f4-741">La versione dell'applicazione è 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="0b8f4-742">Il sequencer viene eseguito in un computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="0b8f4-743">Il pacchetto viene recapitato a un computer client App-V a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="0b8f4-744">La tabella seguente mostra le estensioni della shell supportate.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-745">Gestore</span><span class="sxs-lookup"><span data-stu-id="0b8f4-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-746">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-747">Gestore del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0b8f4-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-748">Aggiunge voci di menu al menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="0b8f4-749">Viene chiamata prima che venga visualizzato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-750">Gestore di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-751">Controlla l'azione quando fai clic con il pulsante destro del mouse su trascinamento della selezione e modifica il menu di scelta rapida visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-752">Trascinare il gestore di destinazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-753">Controlla l'azione dopo il trascinamento e l'eliminazione di un oggetto dati su una destinazione di rilascio, ad esempio un file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-754">Gestore oggetti dati</span><span class="sxs-lookup"><span data-stu-id="0b8f4-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-755">Controlla l'azione dopo la copia di un file negli Appunti o il trascinamento della selezione su una destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="0b8f4-756">Può includere altri formati di Appunti nella destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-757">Gestore della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0b8f4-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-758">Sostituisce o aggiunge pagine alla finestra di dialogo delle proprietà di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-759">Gestore infotip</span><span class="sxs-lookup"><span data-stu-id="0b8f4-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-760">Consente di recuperare le informazioni di flag e infotip per un elemento e di visualizzarle all'interno di una descrizione comando popup al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-761">Gestore di colonne</span><span class="sxs-lookup"><span data-stu-id="0b8f4-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-762">Consente la creazione e la visualizzazione di colonne personalizzate nella visualizzazione dettagli di Esplora risorse <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="0b8f4-763">Può essere usato per estendere l'ordinamento e il raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-764">Gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="0b8f4-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-765">Consente di visualizzare un'anteprima di un file nel riquadro di anteprima di Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0b8f4-766">COM</span><span class="sxs-lookup"><span data-stu-id="0b8f4-766">COM</span></span>

<span data-ttu-id="0b8f4-767">Il client App-V supporta le applicazioni di pubblicazione con il supporto per l'integrazione e la virtualizzazione COM.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="0b8f4-768">L'integrazione COM consente al client App-V di registrare oggetti COM nel sistema operativo locale e la virtualizzazione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="0b8f4-769">Per gli scopi di questo documento, l'integrazione di oggetti COM richiede dettagli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="0b8f4-770">App-V supporta la registrazione di oggetti COM dal pacchetto nel sistema operativo locale con due tipi di processo: out-of-process e in-process.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="0b8f4-771">La registrazione di oggetti COM viene eseguita con una o una combinazione di più modalità di operazione per un pacchetto App-V specifico che include disattivato, isolato e integrato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="0b8f4-772">La modalità integrata è configurata per il tipo out-of-process o in-process.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="0b8f4-773">La configurazione delle modalità e dei tipi COM viene eseguita con i file di configurazione dinamici (deploymentconfig.xml o userconfig.xml).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="0b8f4-774">I dettagli sull'integrazione di App-V sono disponibili all'indirizzo: <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="0b8f4-775">Client software e funzionalità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-775">Software clients and application capabilities</span></span>

<span data-ttu-id="0b8f4-776">App-V supporta i client software specifici e i punti di estensione delle funzionalità applicative che consentono di registrare le applicazioni virtualizzate con il client software del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="0b8f4-777">Questo consente agli utenti di selezionare programmi predefiniti per operazioni come la posta elettronica, la messaggistica istantanea e il lettore multimediale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="0b8f4-778">Questa operazione viene eseguita nel pannello di controllo con le impostazioni predefinite per l'accesso ai programmi e i computer e configurata durante la sequenziazione nei file di configurazione manifesto o dinamico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="0b8f4-779">Le funzionalità dell'applicazione sono supportate solo quando le applicazioni App-V vengono pubblicate globalmente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="0b8f4-780">Esempio di registrazione client software di un client di posta elettronica basato su App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="0b8f4-781">**Nota**  In questo esempio:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="0b8f4-782">è l'impostazione complessiva dei client software per integrare i client di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="0b8f4-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="0b8f4-783">è il contrassegno per impostare un determinato client di posta elettronica come client di posta elettronica predefinito</span><span class="sxs-lookup"><span data-stu-id="0b8f4-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="0b8f4-784">è la registrazione della DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="0b8f4-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="0b8f4-785">Gestore protocollo URL</span><span class="sxs-lookup"><span data-stu-id="0b8f4-785">URL Protocol handler</span></span>

<span data-ttu-id="0b8f4-786">Le applicazioni non sempre espressamente denominate applicazioni virtualizzate che usano la chiamata del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="0b8f4-787">Ad esempio, in un'applicazione che supporta l'incorporamento di un collegamento mailto: all'interno di un documento o di una pagina Web, l'utente fa clic su un collegamento mailto: e prevede di ottenere il client di posta elettronica registrato.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="0b8f4-788">App-V supporta i gestori di protocolli URL che possono essere registrati per ogni singolo pacchetto con il sistema operativo locale.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="0b8f4-789">Durante la sequenziazione, i gestori di protocolli URL vengono aggiunti automaticamente al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="0b8f4-790">Per le situazioni in cui sono presenti più applicazioni in grado di registrare il gestore del protocollo URL specifico, è possibile usare i file di configurazione dinamica per modificare il comportamento ed eliminare o disabilitare questa caratteristica per un'applicazione che non deve essere l'applicazione principale avviata.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="0b8f4-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="0b8f4-791">AppPath</span></span>

<span data-ttu-id="0b8f4-792">Il punto di estensione AppPath supporta la chiamata delle applicazioni App-V direttamente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="0b8f4-793">Questa operazione viene in genere eseguita dalla schermata Esegui o Start, a seconda del sistema operativo, che consente agli amministratori di consentire l'accesso alle applicazioni App-V da comandi o script del sistema operativo senza chiamare il percorso specifico dell'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="0b8f4-794">Evita quindi di modificare la variabile di ambiente PATH di sistema in tutti i sistemi, come avviene durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="0b8f4-795">Il punto di estensione AppPath è configurato nel manifesto o nei file di configurazione dinamica e viene archiviato nel registro di sistema nel computer locale durante la pubblicazione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="0b8f4-796">Per altre informazioni su AppPath Review: <https://go.microsoft.com/fwlink/?LinkId=392835> .</span><span class="sxs-lookup"><span data-stu-id="0b8f4-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="0b8f4-797">Applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-797">Virtual application</span></span>

<span data-ttu-id="0b8f4-798">Questo sottosistema fornisce un elenco di applicazioni acquisite durante la sequenziazione che in genere sono usate da altri componenti di App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="0b8f4-799">L'integrazione di punti di estensione appartenenti a una particolare applicazione può essere disabilitata con i file di configurazione dinamici.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="0b8f4-800">Ad esempio, se un pacchetto contiene due applicazioni, è possibile disabilitare tutti i punti di estensione appartenenti a un'applicazione, in modo da consentire solo l'integrazione dei punti di estensione di un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="0b8f4-801">Regole del punto di estensione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-801">Extension point rules</span></span>

<span data-ttu-id="0b8f4-802">I punti di estensione descritti sopra sono integrati nel sistema operativo in base al modo in cui i pacchetti sono stati pubblicati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="0b8f4-803">I punti di estensione per la pubblicazione globale sono ubicati in posizioni macchina pubbliche, in cui i punti di estensione della pubblicazione degli utenti vengono posizionati in</span><span class="sxs-lookup"><span data-stu-id="0b8f4-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="0b8f4-804">Ad esempio, un collegamento creato sul desktop e pubblicato globalmente comporterà i dati del file per il collegamento (%Public%\\Desktop) e i dati del registro di sistema (HKLM\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="0b8f4-805">Lo stesso collegamento avrebbe i dati dei file (%UserProfile%\\Desktop) e i dati del registro di sistema (HKCU\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="0b8f4-806">I punti di estensione non sono tutti pubblicati nello stesso modo, in cui alcuni punti di estensione richiedono la pubblicazione globale e altri richiedono la sequenziazione nel sistema operativo specifico e nell'architettura in cui vengono recapitati.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="0b8f4-807">Di seguito è riportata una tabella che descrive queste due regole chiave.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0b8f4-808">Estensione virtuale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-809">Richiede la sequenziazione del sistema operativo di destinazione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="0b8f4-810">Richiede la pubblicazione globale</span><span class="sxs-lookup"><span data-stu-id="0b8f4-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-811">Collegamento</span><span class="sxs-lookup"><span data-stu-id="0b8f4-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-812">Associazione tipo di file</span><span class="sxs-lookup"><span data-stu-id="0b8f4-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-813">Protocolli URL</span><span class="sxs-lookup"><span data-stu-id="0b8f4-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-814">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="0b8f4-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-816">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-817">Modalità COM</span><span class="sxs-lookup"><span data-stu-id="0b8f4-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-818">Client software</span><span class="sxs-lookup"><span data-stu-id="0b8f4-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-819">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-820">Funzionalità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="0b8f4-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-821">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-822">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-823">Gestore del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0b8f4-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-824">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-825">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-826">Gestore di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-827">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-828">Gestore oggetti dati</span><span class="sxs-lookup"><span data-stu-id="0b8f4-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-829">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-830">Gestore della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0b8f4-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-831">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-832">Gestore infotip</span><span class="sxs-lookup"><span data-stu-id="0b8f4-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-833">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-834">Gestore di colonne</span><span class="sxs-lookup"><span data-stu-id="0b8f4-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-835">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-836">Estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="0b8f4-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-837">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0b8f4-838">Oggetto helper del browser</span><span class="sxs-lookup"><span data-stu-id="0b8f4-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-839">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-840">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0b8f4-841">Oggetto X attivo</span><span class="sxs-lookup"><span data-stu-id="0b8f4-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-842">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="0b8f4-843">X</span><span class="sxs-lookup"><span data-stu-id="0b8f4-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="0b8f4-844">Elaborazione della configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="0b8f4-844">Dynamic configuration processing</span></span>


<span data-ttu-id="0b8f4-845">La distribuzione di pacchetti App-V in un computer o un utente è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="0b8f4-846">Tuttavia, dato che le organizzazioni distribuiscono applicazioni AppV tra le linee aziendali e i confini geografici e politici, la possibilità di sequenziare un'applicazione una sola volta con un set di impostazioni diventa impossibile.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="0b8f4-847">App-V è stato progettato per questo scenario, poiché acquisisce impostazioni e configurazioni specifiche durante la sequenziazione nel file manifesto, ma supporta anche la modifica con i file di configurazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="0b8f4-848">La configurazione dinamica di App-V consente di specificare un criterio per un pacchetto a livello di computer o a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="0b8f4-849">I file di configurazione dinamica consentono agli ingegneri di sequenziazione di modificare la configurazione di un pacchetto, la post-sequenziazione, per soddisfare le esigenze dei singoli gruppi di utenti o computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="0b8f4-850">In alcuni casi potrebbe essere necessario apportare modifiche all'applicazione per offrire funzionalità appropriate nell'ambiente App-V.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="0b8f4-851">Ad esempio, potrebbe essere necessario apportare modifiche ai file \ _ \ \* config.xml per consentire l'esecuzione di determinate azioni in un determinato periodo di tempo, come la disabilitazione di un'estensione mailto per impedire che un'applicazione virtualizzata sovrascriva tale estensione da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="0b8f4-852">I pacchetti App-V contengono il file manifesto all'interno del file del pacchetto appv, che rappresenta le operazioni di sequenziazione ed è il criterio di scelta, a meno che non vengano assegnati file di configurazione dinamici a un pacchetto specifico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="0b8f4-853">Post-sequenziazione, i file di configurazione dinamici possono essere modificati per consentire la pubblicazione di un'applicazione in desktop o utenti diversi con punti di estensione diversi.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="0b8f4-854">I due file di configurazione dinamici sono i file di configurazione della distribuzione dinamica (DDC) e della configurazione degli utenti dinamici (DUC).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="0b8f4-855">Questa sezione si basa sulla combinazione dei file di configurazione manifesto e dinamico.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="0b8f4-856">Esempio per i file di configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="0b8f4-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="0b8f4-857">L'esempio seguente mostra la combinazione del manifesto, della configurazione della distribuzione e dei file di configurazione degli utenti dopo la pubblicazione e durante il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="0b8f4-858">Questi esempi sono esempi abbreviati di ognuno dei file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="0b8f4-859">Lo scopo è mostrare la combinazione dei file solo e non essere una descrizione completa delle categorie specifiche disponibili in ognuno dei file.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="0b8f4-860">Per altre informazioni, vedere la guida alla sequenziazione di App-V 5 all'indirizzo:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="0b8f4-861">Manifesto</span><span class="sxs-lookup"><span data-stu-id="0b8f4-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="0b8f4-862">Configurazione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="0b8f4-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="0b8f4-863">Configurazione utente</span><span class="sxs-lookup"><span data-stu-id="0b8f4-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="0b8f4-864">Assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="0b8f4-864">Side-by-side assemblies</span></span>


<span data-ttu-id="0b8f4-865">App-V supporta la creazione automatica di assembly side-by-Side (SxS) durante la sequenziazione e la distribuzione nel client durante la pubblicazione di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="0b8f4-866">App-V 5 SP2 supporta l'acquisizione di assembly SxS durante la sequenziazione per gli assembly non presenti nel computer di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="0b8f4-867">Per gli assembly costituiti da Visual C++ (versione 8 e successive) e/o da Runtime di MSXML, il sequencer rileverà e catturerà automaticamente queste dipendenze anche se non sono state installate durante il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="0b8f4-868">La caratteristica assiemi affiancati rimuove le limitazioni delle versioni precedenti di App-V, in cui l'App-V Sequencer non ha acquisito gli assembly già presenti nella workstation di sequenziazione e ha privatizzato gli assembly che limitavano la versione di un bit per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="0b8f4-869">Questo comportamento ha provocato le applicazioni App-V distribuite ai client che mancano degli assembly SxS necessari, causando errori di avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="0b8f4-870">In questo modo il processo di creazione del pacchetto è stato costretto a documentare e quindi assicurarsi che tutti gli assembly necessari per i pacchetti fossero installati localmente nel sistema operativo client dell'utente per garantire il supporto per le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="0b8f4-871">In base al numero di assembly e alla mancanza di documentazione dell'applicazione per le dipendenze richieste, questa attività è stata una sfida di gestione e implementazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="0b8f4-872">Il supporto per l'assembly affiancato in App-V include le caratteristiche seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="0b8f4-873">Acquisisce automaticamente l'assembly SxS durante la sequenziazione, indipendentemente dal fatto che l'assembly sia già stato installato nella workstation di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="0b8f4-874">Il client App-V installa automaticamente gli assembly SxS obbligatori nel computer client in fase di pubblicazione quando non sono presenti.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="0b8f4-875">Il sequencer riporta la dipendenza di runtime VC nel meccanismo di creazione di report Sequencer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="0b8f4-876">Il Sequencer consente di non creare il pacchetto degli assembly già installati nel sequencer, sostenendo gli scenari in cui gli assembly sono stati installati in precedenza nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="0b8f4-877">Pubblicazione automatica di assembly SxS</span><span class="sxs-lookup"><span data-stu-id="0b8f4-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="0b8f4-878">Durante la pubblicazione di un pacchetto App-V con gli assembly SxS, il client App-V verificherà la presenza dell'assembly nel computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="0b8f4-879">Se l'assembly non esiste, il client distribuirà l'assembly nel computer.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="0b8f4-880">I pacchetti che fanno parte dei gruppi di connessioni si basano sulle installazioni affiancate di assembly che fanno parte dei pacchetti di base, poiché il gruppo di connessioni non contiene informazioni sull'installazione di assembly.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="0b8f4-881">**Nota**  L'annullamento della pubblicazione o della rimozione di un pacchetto con un assembly non rimuove gli assembly per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="0b8f4-882">Registrazione client</span><span class="sxs-lookup"><span data-stu-id="0b8f4-882">Client logging</span></span>


<span data-ttu-id="0b8f4-883">Il client App-V registra le informazioni nel log eventi di Windows in formato ETW standard.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="0b8f4-884">Gli eventi specifici di App-V si trovano nel Visualizzatore eventi, in applicazioni e servizi Logs\\Microsoft\\AppV\\Client.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="0b8f4-885">**Nota**  In App-V 5,0 SP3 alcuni registri sono stati consolidati e spostati nella posizione seguente:</span><span class="sxs-lookup"><span data-stu-id="0b8f4-885">**Note** In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="0b8f4-886">Per un elenco dei registri spostati, vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="0b8f4-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="0b8f4-887">Sono state registrate tre categorie di eventi specifiche descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="0b8f4-888">**Amministratore**: registra gli eventi per le configurazioni applicate al client App-V e contiene gli avvisi e gli errori principali.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="0b8f4-889">**Operativo**: registra l'esecuzione generale dell'app-v e l'uso dei singoli componenti creando un log di controllo delle operazioni di App-v che sono state completate nel client App-v.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="0b8f4-890">**Applicazione virtuale**: registra i lanci delle applicazioni virtuali e l'uso dei sottosistemi di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0b8f4-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 





