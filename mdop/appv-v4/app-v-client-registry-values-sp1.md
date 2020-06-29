---
title: Valori del Registro di sistema del client App-V
description: Valori del Registro di sistema del client App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819806"
---
# <span data-ttu-id="08247-103">Valori del Registro di sistema del client App-V</span><span class="sxs-lookup"><span data-stu-id="08247-103">App-V Client Registry Values</span></span>


<span data-ttu-id="08247-104">Il client Microsoft Application Virtualization (App-V) archivia la propria configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="08247-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="08247-105">Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client.</span><span class="sxs-lookup"><span data-stu-id="08247-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="08247-106">È anche possibile configurare molte azioni client modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="08247-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="08247-107">Questo argomento elenca tutte le chiavi del registro di sistema di Application Virtualization (App-V) e spiega i loro usi.</span><span class="sxs-lookup"><span data-stu-id="08247-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="08247-108">Importante</span><span class="sxs-lookup"><span data-stu-id="08247-108">Important</span></span>**  
<span data-ttu-id="08247-109">In un computer che utilizza un sistema operativo a 64 bit, le chiavi e i valori descritti nelle sezioni seguenti saranno in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="08247-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="08247-110">Chiave di configurazione</span><span class="sxs-lookup"><span data-stu-id="08247-110">Configuration Key</span></span>


<span data-ttu-id="08247-111">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="08247-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-112">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-112">Name</span></span></th>
<th align="left"><span data-ttu-id="08247-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-113">Type</span></span></th>
<th align="left"><span data-ttu-id="08247-114">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="08247-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="08247-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-117">String</span><span class="sxs-lookup"><span data-stu-id="08247-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-118">Client desktop Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="08247-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-119">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-120">Versione</span><span class="sxs-lookup"><span data-stu-id="08247-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-121">String</span><span class="sxs-lookup"><span data-stu-id="08247-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="08247-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-123">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-124">Driver</span><span class="sxs-lookup"><span data-stu-id="08247-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-125">String</span><span class="sxs-lookup"><span data-stu-id="08247-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="08247-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-127">Se il valore di questo tasto è presente, contiene il nome del driver che ha causato un errore di interruzione l'ultima volta che è stato avviato il core.</span><span class="sxs-lookup"><span data-stu-id="08247-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="08247-128">Dopo aver risolto l'errore di interruzione, è necessario eliminare questo valore di chiave in modo che sftlist possa iniziare.</span><span class="sxs-lookup"><span data-stu-id="08247-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-129">InstallPath</span><span class="sxs-lookup"><span data-stu-id="08247-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-130">String</span><span class="sxs-lookup"><span data-stu-id="08247-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-131">Default = C:\Programmi\Microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="08247-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-132">Posizione in cui è installato il client.</span><span class="sxs-lookup"><span data-stu-id="08247-132">The location where the client is installed.</span></span> <span data-ttu-id="08247-133">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-134">LogFileName</span><span class="sxs-lookup"><span data-stu-id="08247-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-135">String</span><span class="sxs-lookup"><span data-stu-id="08247-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-136">Impostazione predefinita = CSIDL_COMMON_APPDATA virtualizzazione \Microsoft\Application Client\sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="08247-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-137">Il percorso e il nome del file di log del client.</span><span class="sxs-lookup"><span data-stu-id="08247-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="08247-138">Nota</span><span class="sxs-lookup"><span data-stu-id="08247-138">Note</span></span></strong><br/><p><span data-ttu-id="08247-139">Se si esegue una versione precedente rispetto a App-V 4,6, SP1 e si modifica il nome o il percorso del file di log, è necessario riavviare il servizio sftlist affinché la modifica abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="08247-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-140">LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="08247-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-142">Impostazione predefinita = 4, informazioni</span><span class="sxs-lookup"><span data-stu-id="08247-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-143">Controlla i messaggi scritti nel log.</span><span class="sxs-lookup"><span data-stu-id="08247-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="08247-144">Il valore indica una soglia di ciò che viene registrato, ossia tutto il valore minore o uguale a quello viene registrato.</span><span class="sxs-lookup"><span data-stu-id="08247-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="08247-145">Ad esempio, un valore di 0x3 (Warning) indica che vengono registrati gli avvisi (0x3), gli errori (0x2) e gli errori critici (0x1).</span><span class="sxs-lookup"><span data-stu-id="08247-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="08247-146">Intervallo di valori: 0x0 = None, 0x1 = critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (default), 0x5 = verbose.</span><span class="sxs-lookup"><span data-stu-id="08247-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="08247-147">Il livello di log è configurabile dalla console client Application Virtualization (App-V) e dal prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="08247-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="08247-148">Al prompt dei comandi il comando sftlist.exe/Verboselog aumenterà il livello di log in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="08247-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="08247-149">Per altre informazioni sui dettagli della riga di comando, vedere</span><span class="sxs-lookup"><span data-stu-id="08247-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="08247-150">.</span><span class="sxs-lookup"><span data-stu-id="08247-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="08247-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-153">Impostazione predefinita = 4</span><span class="sxs-lookup"><span data-stu-id="08247-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-154">Definisce il numero di copie di backup del file di log che vengono mantenute quando viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="08247-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="08247-155">L'intervallo valido è 0-9999.</span><span class="sxs-lookup"><span data-stu-id="08247-155">The valid range is 0–9999.</span></span> <span data-ttu-id="08247-156">Il valore predefinito è 4.</span><span class="sxs-lookup"><span data-stu-id="08247-156">The default is 4.</span></span> <span data-ttu-id="08247-157">Un valore pari a 0 indica che non verranno mantenute copie.</span><span class="sxs-lookup"><span data-stu-id="08247-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-158">LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="08247-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-160">Impostazione predefinita = 256</span><span class="sxs-lookup"><span data-stu-id="08247-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-161">Definisce la dimensione massima in megabyte (MB) che il file di log può aumentare prima di essere reimpostato.</span><span class="sxs-lookup"><span data-stu-id="08247-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="08247-162">La dimensione predefinita è 256 MB.</span><span class="sxs-lookup"><span data-stu-id="08247-162">The default size is 256 MB.</span></span> <span data-ttu-id="08247-163">Quando questa dimensione viene raggiunta, viene forzata una reimpostazione del log per il successivo tentativo di scrittura.</span><span class="sxs-lookup"><span data-stu-id="08247-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="08247-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-166">Impostazione predefinita = 0x4 (App-V 4,5)</span><span class="sxs-lookup"><span data-stu-id="08247-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="08247-167">Impostazione predefinita = 0x3 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="08247-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-168">Indica il livello di registrazione in cui i messaggi di log vengono scritti nel log eventi di NT.</span><span class="sxs-lookup"><span data-stu-id="08247-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="08247-169">Il valore indica una soglia di ciò che viene registrato, ovvero tutto ciò che è uguale o minore di quel valore viene registrato.</span><span class="sxs-lookup"><span data-stu-id="08247-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="08247-170">Ad esempio, un valore di 0x3 (Warning) indica che vengono registrati gli avvisi (0x3), gli errori (0x2) e gli errori critici (0x1).</span><span class="sxs-lookup"><span data-stu-id="08247-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="08247-171">Intervallo di valori</span><span class="sxs-lookup"><span data-stu-id="08247-171">Value Range</span></span></p>
<p><span data-ttu-id="08247-172">0x0 = None</span><span class="sxs-lookup"><span data-stu-id="08247-172">0x0 = None</span></span></p>
<p><span data-ttu-id="08247-173">0x1 = Critical</span><span class="sxs-lookup"><span data-stu-id="08247-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="08247-174">0x2 = Errore</span><span class="sxs-lookup"><span data-stu-id="08247-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="08247-175">0x3 = avviso</span><span class="sxs-lookup"><span data-stu-id="08247-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="08247-176">0x4 = informazioni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08247-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="08247-177">0x5 = verbose</span><span class="sxs-lookup"><span data-stu-id="08247-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="08247-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-180">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-181">Indica se lo streaming da file verrà abilitato indipendentemente dal modo in cui il client è stato configurato con il parametro APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="08247-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="08247-182">Se impostato su FALSE, il trasporto non consentirà lo streaming da file, anche se l'OSD HREF o il parametro APPLICATIONSOURCEROOT contiene un percorso di file.</span><span class="sxs-lookup"><span data-stu-id="08247-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="08247-183">0x0 = false (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08247-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="08247-184">0x1 = true</span><span class="sxs-lookup"><span data-stu-id="08247-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="08247-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-186">String</span><span class="sxs-lookup"><span data-stu-id="08247-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="08247-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="08247-188">file://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="08247-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="08247-189">file://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="08247-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-190">Consente a un amministratore o a un sistema ESD (Electronic Software Distribution) di garantire il caricamento delle applicazioni in base allo schema di gestione della topologia.</span><span class="sxs-lookup"><span data-stu-id="08247-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="08247-191">Usa questo valore di chiave per eseguire l'override della BASE di codice OSD per l'elemento HREF, ad esempio la posizione di origine, per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="08247-192">La radice dell'origine dell'applicazione supporta gli URL e i formati di percorso UNC (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="08247-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="08247-193">Il formato corretto per il percorso URL è protocollo://nomeserver: [porta] [/path] [/], dove porta e percorso sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="08247-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="08247-194">Se non viene specificata una porta, viene usata la porta predefinita per il protocollo.</span><span class="sxs-lookup"><span data-stu-id="08247-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="08247-195">Viene sostituita solo la parte protocollo://Server: Port dell'URL OSD.</span><span class="sxs-lookup"><span data-stu-id="08247-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="08247-196">Il formato corretto per il percorso UNC è \computername\sharefolder [Folder] [], dove cartella è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="08247-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="08247-197">Il nome del computer può essere un nome di dominio completo (FQDN) o un indirizzo IP e cartellacondivisione può essere una lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="08247-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="08247-198">Viene sostituita solo la parte \computername\sharefolder o lettera dell'unità del percorso OSD.</span><span class="sxs-lookup"><span data-stu-id="08247-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="08247-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-200">String</span><span class="sxs-lookup"><span data-stu-id="08247-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="08247-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="08247-202">\computername\content</span><span class="sxs-lookup"><span data-stu-id="08247-202">\computername\content</span></span></p>
<p><span data-ttu-id="08247-203">C:\NomeCartella</span><span class="sxs-lookup"><span data-stu-id="08247-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="08247-204">Consente a un amministratore di specificare una posizione di origine per il recupero dei file OSD per un pacchetto di applicazione sequenziata durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="08247-205">I formati accettabili per OSDSourceRoot includono percorsi UNC e URL (http o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="08247-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="08247-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-207">String</span><span class="sxs-lookup"><span data-stu-id="08247-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="08247-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="08247-209">\computername\content</span><span class="sxs-lookup"><span data-stu-id="08247-209">\computername\content</span></span></p>
<p><span data-ttu-id="08247-210">C:\NomeCartella</span><span class="sxs-lookup"><span data-stu-id="08247-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="08247-211">Consente a un amministratore di specificare una posizione di origine per il recupero di file di icona per un pacchetto di applicazione sequenziata durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="08247-212">I formati accettabili per IconSourceRoot includono percorsi UNC e URL (http o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="08247-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="08247-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-215">Impostazione predefinita = 5</span><span class="sxs-lookup"><span data-stu-id="08247-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-216">Autoload è un parametro di configurazione dei criteri di runtime client che consente al client di trasmettere automaticamente in background il blocco di funzionalità secondario di un'applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="08247-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="08247-217">I trigger di autoload sono contrassegni per indicare gli eventi che avviano il caricamento automatico delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="08247-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="08247-218">Autoload USA in modo implicito lo streaming in background per consentire il caricamento completo dell'applicazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="08247-219">Il blocco di funzionalità principale verrà caricato per primo e i blocchi di funzionalità rimanenti verranno caricati in background per abilitare le operazioni in primo piano, ad esempio l'interazione dell'utente con le applicazioni, e per ottenere prestazioni percepite ottimali.</span><span class="sxs-lookup"><span data-stu-id="08247-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="08247-220">Valori della maschera di bit:</span><span class="sxs-lookup"><span data-stu-id="08247-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="08247-221">(0) mai: nessun bit viene impostato (il valore è 0), non viene eseguito il caricamento automatico, perché non sono impostati trigger.</span><span class="sxs-lookup"><span data-stu-id="08247-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="08247-222">(1) OnLaunch: il caricamento inizia quando un utente avvia un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="08247-223">(2) OnRefresh: il caricamento inizia quando viene pubblicata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="08247-224">Questo problema si verifica ogni volta che il record del pacchetto viene aggiunto o aggiornato, ad esempio quando si verifica un aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="08247-225">(4) OnLogin: il caricamento inizia quando un utente effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="08247-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="08247-226">(5) OnLaunch e OnLogin: default.</span><span class="sxs-lookup"><span data-stu-id="08247-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="08247-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-229">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-230">Indica cosa verrà caricato automaticamente quando si verificherà un trigger di caricamento automatico specifico.</span><span class="sxs-lookup"><span data-stu-id="08247-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="08247-231">Valori della maschera di bit:</span><span class="sxs-lookup"><span data-stu-id="08247-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="08247-232">(0) None: nessun caricamento automatico, indipendentemente dai trigger che possono essere impostati.</span><span class="sxs-lookup"><span data-stu-id="08247-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="08247-233">(1) PreviouslyUsed (impostazione predefinita): se è abilitato un trigger di caricamento automatico, caricare solo i pacchetti in cui almeno un'applicazione nel pacchetto è stata usata in precedenza, ovvero avviata o prememorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="08247-234">(2) tutti: se è abilitato un trigger di autoload, tutte le applicazioni nel pacchetto (per pacchetto) o tutti i pacchetti (impostati per il client) verranno caricate automaticamente, indipendentemente dal fatto che siano state o meno avviate.</span><span class="sxs-lookup"><span data-stu-id="08247-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="08247-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-237">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-238">Indica che l'autorizzazione è sempre necessaria, indipendentemente dal fatto che un'applicazione sia già nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="08247-239">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="08247-239">Possible values:</span></span></p>
<p><span data-ttu-id="08247-240">0 = false: provare sempre a connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="08247-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="08247-241">Se non è possibile stabilire una connessione al server, il client consente comunque all'utente di avviare un'applicazione precedentemente caricata nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="08247-242">1 = true (impostazione predefinita): l'applicazione deve sempre essere autorizzata all'avvio.</span><span class="sxs-lookup"><span data-stu-id="08247-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="08247-243">Per le applicazioni in streaming RTSP, il token di autorizzazione utente viene inviato al server per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="08247-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="08247-244">Per le applicazioni basate su file, gli ACL dei file controllano se un utente può accedere all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="08247-245">Riavviare il servizio sftlist affinché la modifica abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="08247-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="08247-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-247">String</span><span class="sxs-lookup"><span data-stu-id="08247-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-248">AppData</span><span class="sxs-lookup"><span data-stu-id="08247-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-249">Posizione in cui sono archiviate la cache delle icone e le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="08247-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="08247-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-251">String</span><span class="sxs-lookup"><span data-stu-id="08247-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="08247-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-253">Directory da usare per i dati globali di App-V, incluse le cache per i file OSD, i file di icone, le informazioni di collegamento e le risorse SystemGuard, ad esempio i file ini.</span><span class="sxs-lookup"><span data-stu-id="08247-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="08247-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-256">0 o 1</span><span class="sxs-lookup"><span data-stu-id="08247-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-257">Default = 0: il valore 0 indica che il client cerca di intercettare le eccezioni di programma interne in modo che altre applicazioni utente possano recuperare e continuare quando si verifica un arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="08247-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="08247-258">Il valore 1 indica che il client consente di eseguire le eccezioni del programma interno in modo che possano essere acquisite in un debugger.</span><span class="sxs-lookup"><span data-stu-id="08247-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-261">60</span><span class="sxs-lookup"><span data-stu-id="08247-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-262">Timeout in secondi per le richieste interne di IPC tra core e front-end.</span><span class="sxs-lookup"><span data-stu-id="08247-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="08247-263">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="08247-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-266">10</span><span class="sxs-lookup"><span data-stu-id="08247-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-267">Questo valore viene usato per indicare quanto tempo dopo l'avvio che un programma può arrestare e non generare messaggi di errore quando è in corso un'altra applicazione nella stessa suite.</span><span class="sxs-lookup"><span data-stu-id="08247-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-270">Impostazione predefinita = 60000</span><span class="sxs-lookup"><span data-stu-id="08247-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-271">Definisce il periodo di tempo in millisecondi che il client aspetterà mentre prova a serializzare l'avvio del programma nella stessa suite.</span><span class="sxs-lookup"><span data-stu-id="08247-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="08247-272">Se il client esce in timeout, l'avvio del programma continuerà ma non verrà serializzato.</span><span class="sxs-lookup"><span data-stu-id="08247-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-275">300</span><span class="sxs-lookup"><span data-stu-id="08247-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-276">Timeout predefinito in secondi per gli script nel file OSD se WAIT = TRUE.</span><span class="sxs-lookup"><span data-stu-id="08247-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="08247-277">È possibile specificare i timeout per ogni script con TIMEOUT anziché WAIT.</span><span class="sxs-lookup"><span data-stu-id="08247-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="08247-278">Un valore pari a 0 indica che non ci sono attese e 0xFFFFFFFF significa attendere per sempre.</span><span class="sxs-lookup"><span data-stu-id="08247-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="08247-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-280">String</span><span class="sxs-lookup"><span data-stu-id="08247-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="08247-281">Se, in HKLM o HKCU, questo valore contiene un percorso valido per un file di log, SFTTray scriverà in questo log quando si avviano programmi, si arresta, non si avvia e si immette o si esce dalla modalità disconnessa.</span><span class="sxs-lookup"><span data-stu-id="08247-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="08247-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-284">0x1A (26) errori di avvio del log e attività di entrata e uscita della modalità disconnessa.</span><span class="sxs-lookup"><span data-stu-id="08247-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="08247-285">0x1F (31) registra tutto.</span><span class="sxs-lookup"><span data-stu-id="08247-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="08247-286">0x0 (0) registra Nothing.</span><span class="sxs-lookup"><span data-stu-id="08247-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-287">Specifica quale dei cinque eventi vengono registrati (valori della maschera di scelta):</span><span class="sxs-lookup"><span data-stu-id="08247-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="08247-288">1 per l'avvio del programma</span><span class="sxs-lookup"><span data-stu-id="08247-288">1 for program starts</span></span></p>
<p><span data-ttu-id="08247-289">2 per gli errori di errore di avvio</span><span class="sxs-lookup"><span data-stu-id="08247-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="08247-290">4 per gli arresti</span><span class="sxs-lookup"><span data-stu-id="08247-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="08247-291">8 per l'immissione della modalità disconnessa</span><span class="sxs-lookup"><span data-stu-id="08247-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="08247-292">16 per uscire dalla modalità disconnessa per riconnettersi a un server</span><span class="sxs-lookup"><span data-stu-id="08247-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="08247-293">Aggiungere qualsiasi combinazione di questi numeri per attivare i rispettivi messaggi.</span><span class="sxs-lookup"><span data-stu-id="08247-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="08247-294">Il valore predefinito è 0x1F se non è presente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="08247-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-297">Impostazione predefinita = 3000</span><span class="sxs-lookup"><span data-stu-id="08247-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-298">Specifica in millisecondi il tempo di attesa del cassetto quando si prova a scrivere nel log del record di avvio se un altro processo lo usa.</span><span class="sxs-lookup"><span data-stu-id="08247-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="08247-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-300">String</span><span class="sxs-lookup"><span data-stu-id="08247-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-301">d:\files; C:\Documents and settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="08247-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-302">Un elenco delimitato da un punto e virgola fino a cinque directory per cercare i file portatili SFT prima di richiedere all'utente di selezionare una directory.</span><span class="sxs-lookup"><span data-stu-id="08247-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="08247-303">La barra rovesciata finale nei percorsi è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="08247-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="08247-304">Questo valore non è presente per impostazione predefinita e deve essere impostato manualmente.</span><span class="sxs-lookup"><span data-stu-id="08247-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="08247-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-306">String</span><span class="sxs-lookup"><span data-stu-id="08247-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="08247-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="08247-308">Valido solo in HKCU.</span><span class="sxs-lookup"><span data-stu-id="08247-308">Valid only under HKCU.</span></span> <span data-ttu-id="08247-309">L'ultima posizione in cui l'utente ha esplorato durante la ricerca di un file SFT per l'importazione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="08247-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="08247-310">Imposta automaticamente se SFT viene trovato correttamente.</span><span class="sxs-lookup"><span data-stu-id="08247-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="08247-311">Questo viene usato per le importazioni successive quando si prova a individuare automaticamente i file SFT.</span><span class="sxs-lookup"><span data-stu-id="08247-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-312">Chiave condivisa</span><span class="sxs-lookup"><span data-stu-id="08247-312">Shared Key</span></span>


<span data-ttu-id="08247-313">La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared controlla i valori condivisi tra i componenti App-V.</span><span class="sxs-lookup"><span data-stu-id="08247-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="08247-314">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="08247-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-315">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="08247-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="08247-317">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="08247-318">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-319">DumpPath</span><span class="sxs-lookup"><span data-stu-id="08247-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-320">String</span><span class="sxs-lookup"><span data-stu-id="08247-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-321">Impostazione predefinita = C:</span><span class="sxs-lookup"><span data-stu-id="08247-321">Default=C:</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="08247-322">Percorso predefinito per creare file di dump quando si genera un minidump in un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="08247-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="08247-323">Questo valore predefinito è C:\ Se non specificato.</span><span class="sxs-lookup"><span data-stu-id="08247-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="08247-324">Il programma di installazione client imposta questa chiave per la &lt; directory dei dati globali di virtualizzazione dell'app &gt; \Dumps.</span><span class="sxs-lookup"><span data-stu-id="08247-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="08247-325">Il programma di installazione sequencer imposta questa chiave nella directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="08247-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-326">DumpPathSizeLimit</span><span class="sxs-lookup"><span data-stu-id="08247-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-328">1000</span><span class="sxs-lookup"><span data-stu-id="08247-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-329">Specifica la quantità totale massima di spazio su disco in megabyte che può essere usata per archiviare i minidump.</span><span class="sxs-lookup"><span data-stu-id="08247-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="08247-330">Impostazione predefinita = 1000 MB.</span><span class="sxs-lookup"><span data-stu-id="08247-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-331">Chiave di rete</span><span class="sxs-lookup"><span data-stu-id="08247-331">Network Key</span></span>


<span data-ttu-id="08247-332">La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network controlla diversi parametri correlati alla rete.</span><span class="sxs-lookup"><span data-stu-id="08247-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="08247-333">Questa chiave viene usata principalmente dall'agente di trasporto di rete.</span><span class="sxs-lookup"><span data-stu-id="08247-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="08247-334">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave di rete.</span><span class="sxs-lookup"><span data-stu-id="08247-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-335">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="08247-336">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="08247-337">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="08247-338">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-339">Online</span><span class="sxs-lookup"><span data-stu-id="08247-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-341">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-342">Abilita o Disabilita la modalità offline.</span><span class="sxs-lookup"><span data-stu-id="08247-342">Enables or disables offline mode.</span></span> <span data-ttu-id="08247-343">Se impostato su 0, il client non comunica con i server di gestione App-V o i server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="08247-344">Nelle operazioni disconnesse, il client può avviare un'applicazione caricata anche quando non è connessa a un server di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="08247-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="08247-345">In modalità offline il client non tenta di connettersi a un server di gestione di App-V o a un server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="08247-346">È necessario consentire le operazioni disconnesse per poter funzionare offline.</span><span class="sxs-lookup"><span data-stu-id="08247-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="08247-347">Il valore predefinito è 1 abilitato (online) e 0 è disabilitato (offline).</span><span class="sxs-lookup"><span data-stu-id="08247-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="08247-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-350">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-351">Abilita o Disabilita l'operazione disconnessa.</span><span class="sxs-lookup"><span data-stu-id="08247-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="08247-352">Il valore predefinito è 1 abilitato e 0 è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="08247-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="08247-353">Quando le operazioni disconnesse sono abilitate, il client App-V può avviare un'applicazione caricata anche quando non è connessa a un server di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="08247-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-356">Impostazione predefinita = 1000</span><span class="sxs-lookup"><span data-stu-id="08247-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-357">Questo valore specifica il timeout della connessione TCP in millisecondi per determinare quando andare in modalità operazioni disconnesse.</span><span class="sxs-lookup"><span data-stu-id="08247-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="08247-358">Questo valore può essere usato per eseguire l'override di ConnectTimeout predefinito di 20 secondi (timeout di App-V Connect per le transazioni di rete) o del timeout TCP del sistema di circa 25 secondi.</span><span class="sxs-lookup"><span data-stu-id="08247-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="08247-359">Questo porta rapidamente il client in modalità operativa disconnessa.</span><span class="sxs-lookup"><span data-stu-id="08247-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="08247-360">Applicato alla connessione successiva.</span><span class="sxs-lookup"><span data-stu-id="08247-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="08247-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-363">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-364">Applicabile solo se AllowDisconnectedOperation è 1, Enabled.</span><span class="sxs-lookup"><span data-stu-id="08247-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="08247-365">Questo valore determina se sarà previsto un limite di tempo per quanto tempo il client sarà autorizzato ad operare nelle operazioni disconnesse.</span><span class="sxs-lookup"><span data-stu-id="08247-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="08247-366">1 = limitato.</span><span class="sxs-lookup"><span data-stu-id="08247-366">1=limited.</span></span> <span data-ttu-id="08247-367">0 = illimitato.</span><span class="sxs-lookup"><span data-stu-id="08247-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="08247-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-370">Impostazione predefinita = 129600</span><span class="sxs-lookup"><span data-stu-id="08247-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-371">Indica il numero di minuti in cui un'applicazione può essere usata in modalità operativa disconnessa.</span><span class="sxs-lookup"><span data-stu-id="08247-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="08247-372">I valori validi sono 1-999999 in giorni espressi in minuti (1-1439998560 minuti).</span><span class="sxs-lookup"><span data-stu-id="08247-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="08247-373">Il valore predefinito è 90 giorni o 129.600 minuti.</span><span class="sxs-lookup"><span data-stu-id="08247-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-374">Protocollo</span><span class="sxs-lookup"><span data-stu-id="08247-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-376">Impostazione predefinita = 8</span><span class="sxs-lookup"><span data-stu-id="08247-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-377">Protocollo predefinito da usare (TCP o SSL).</span><span class="sxs-lookup"><span data-stu-id="08247-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="08247-378">Finestra di dialogo Configura in opzioni.</span><span class="sxs-lookup"><span data-stu-id="08247-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-381">20</span><span class="sxs-lookup"><span data-stu-id="08247-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-382">Timeout di lettura per le transazioni di rete in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="08247-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="08247-383">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-386">20</span><span class="sxs-lookup"><span data-stu-id="08247-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-387">Timeout di scrittura per le transazioni di rete, in secondi.</span><span class="sxs-lookup"><span data-stu-id="08247-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="08247-388">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="08247-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-391">20</span><span class="sxs-lookup"><span data-stu-id="08247-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-392">Connettere il timeout per le transazioni di rete in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="08247-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="08247-393">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="08247-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-396">3</span><span class="sxs-lookup"><span data-stu-id="08247-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-397">Numero di volte in cui provare a ristabilire una sessione eliminata.</span><span class="sxs-lookup"><span data-stu-id="08247-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="08247-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-400">15</span><span class="sxs-lookup"><span data-stu-id="08247-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-401">Il numero di secondi di attesa tra i tentativi di ristabilire una sessione eliminata.</span><span class="sxs-lookup"><span data-stu-id="08247-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-402">Chiave http</span><span class="sxs-lookup"><span data-stu-id="08247-402">Http Key</span></span>


<span data-ttu-id="08247-403">La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http controlla i parametri correlati al flusso HTTP.</span><span class="sxs-lookup"><span data-stu-id="08247-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="08247-404">Questa chiave viene usata principalmente dall'agente di trasporto di rete.</span><span class="sxs-lookup"><span data-stu-id="08247-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="08247-405">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave http.</span><span class="sxs-lookup"><span data-stu-id="08247-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-406">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="08247-407">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="08247-408">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="08247-409">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="08247-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-412">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-413">Controlla il comportamento del flusso HTTP quando è possibile stabilire una connessione al server HTTP e il file di pacchetto non esiste più nel server HTTP.</span><span class="sxs-lookup"><span data-stu-id="08247-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="08247-414">Se il valore non esiste o non è impostato su 1, il client App-V non consente di avviare un'applicazione precedentemente caricata nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="08247-415">1</span><span class="sxs-lookup"><span data-stu-id="08247-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-416">Se questo valore è impostato su 1, il client App-V consente di avviare un'applicazione precedentemente caricata nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-417">Chiave del file System</span><span class="sxs-lookup"><span data-stu-id="08247-417">File System Key</span></span>


<span data-ttu-id="08247-418">I valori contenuti in HKEY \ _LOCAL \ _MACHINE tasto \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS controllano i parametri del file System per App-V.</span><span class="sxs-lookup"><span data-stu-id="08247-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="08247-419">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave AppFS.</span><span class="sxs-lookup"><span data-stu-id="08247-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-420">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="08247-421">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="08247-422">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="08247-423">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="08247-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-426">4096</span><span class="sxs-lookup"><span data-stu-id="08247-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-427">Dimensioni massime in megabyte di file di cache del file System.</span><span class="sxs-lookup"><span data-stu-id="08247-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="08247-428">Se si modifica questo valore nel registro di sistema, è necessario impostare lo stato su 0 e riavviare.</span><span class="sxs-lookup"><span data-stu-id="08247-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-429">FileName</span><span class="sxs-lookup"><span data-stu-id="08247-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-430">String</span><span class="sxs-lookup"><span data-stu-id="08247-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-431">C:\Utenti\Pubblica\Documenti\SoftGrid Client\sftfs.FSD</span><span class="sxs-lookup"><span data-stu-id="08247-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-432">Posizione del file della cache del file System.</span><span class="sxs-lookup"><span data-stu-id="08247-432">Location of file system cache file.</span></span> <span data-ttu-id="08247-433">Se si modifica questo valore nel registro di sistema, è necessario lasciarlo lo stesso e riavviare o impostare lo stato su 0 e riavviare.</span><span class="sxs-lookup"><span data-stu-id="08247-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-434">LetteraUnità</span><span class="sxs-lookup"><span data-stu-id="08247-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-435">String</span><span class="sxs-lookup"><span data-stu-id="08247-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-436">D:</span><span class="sxs-lookup"><span data-stu-id="08247-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-437">Unità in cui verrà montato il file System App-V, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="08247-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="08247-438">Questo valore viene impostato dal listener o dal programma di installazione e viene letto dal file System.</span><span class="sxs-lookup"><span data-stu-id="08247-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-439">Stato</span><span class="sxs-lookup"><span data-stu-id="08247-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-441">0x100</span><span class="sxs-lookup"><span data-stu-id="08247-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-442">Stato del file System.</span><span class="sxs-lookup"><span data-stu-id="08247-442">State of file system.</span></span> <span data-ttu-id="08247-443">Impostato su 0 e riavvia per cancellare completamente la cache del file System.</span><span class="sxs-lookup"><span data-stu-id="08247-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="08247-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-445">String</span><span class="sxs-lookup"><span data-stu-id="08247-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="08247-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-447">Percorso per collegamenti simbolici, impostato in HKCU.</span><span class="sxs-lookup"><span data-stu-id="08247-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="08247-448">Non modificare (usare la directory dati in configurazione per cambiare).</span><span class="sxs-lookup"><span data-stu-id="08247-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="08247-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-450">String</span><span class="sxs-lookup"><span data-stu-id="08247-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-451">Spazio di archiviazione di C:\Utenti\Pubblica\Documenti\SoftGrid Client\AppFS</span><span class="sxs-lookup"><span data-stu-id="08247-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-452">Percorso per i dati del file System globale.</span><span class="sxs-lookup"><span data-stu-id="08247-452">Path for global file system data.</span></span> <span data-ttu-id="08247-453">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="08247-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-456">Impostazione predefinita = 90</span><span class="sxs-lookup"><span data-stu-id="08247-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-457">Specifica la percentuale massima del file di cache del file System che può essere bloccata.</span><span class="sxs-lookup"><span data-stu-id="08247-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="08247-458">Non modificare.</span><span class="sxs-lookup"><span data-stu-id="08247-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="08247-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-461">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-462">La caratteristica gestione dello spazio della cache del file System usa un algoritmo LRU (least used) ed è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="08247-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="08247-463">Se lo spazio necessario per un nuovo pacchetto supererà lo spazio disponibile nella cache, il client App-V utilizzerà questa caratteristica per determinare i pacchetti esistenti che possono essere eliminati dalla cache per creare spazio per il nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="08247-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="08247-464">Il client elimina il pacchetto con la data di accesso ultimo meno recente, se è precedente al valore specificato nel valore del registro di sistema MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="08247-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="08247-465">I valori sono 0 (disabilitato) e 1 (impostazione predefinita, abilitato).</span><span class="sxs-lookup"><span data-stu-id="08247-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="08247-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-468">1</span><span class="sxs-lookup"><span data-stu-id="08247-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-469">Per determinare quando il pacchetto può essere selezionato per l'eliminazione, imposta il valore del registro di sistema su uguale al numero minimo di giorni che vuoi trascorrere dopo l'ultimo accesso al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="08247-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="08247-470">I pacchetti che sono stati usati più di recente non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="08247-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-471">Tasto autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="08247-471">Permissions Key</span></span>


<span data-ttu-id="08247-472">Per impedire agli utenti di commettere errori, gli amministratori possono usare la chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions per controllare l'accesso ad alcune azioni per gli utenti non amministrativi, ad esempio per impedire agli utenti di scaricare accidentalmente programmi.</span><span class="sxs-lookup"><span data-stu-id="08247-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="08247-473">Gli utenti con diritti amministrativi possono concedersi una qualsiasi di queste autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="08247-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="08247-474">Nei sistemi condivisi, ad esempio in un server Host sessione Desktop remoto (in precedenza Terminal Server), prestare particolare attenzione quando si concedono autorizzazioni aggiuntive agli utenti, perché alcune di queste autorizzazioni consentiranno agli utenti di controllare le applicazioni usate da tutti gli utenti del sistema.</span><span class="sxs-lookup"><span data-stu-id="08247-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="08247-475">I valori possibili per queste impostazioni sono 1 (Consenti) e 0 (non consentito).</span><span class="sxs-lookup"><span data-stu-id="08247-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="08247-476">Le impostazioni del tasto autorizzazioni controllano tutte le interfacce che abilitano le azioni denominate.</span><span class="sxs-lookup"><span data-stu-id="08247-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="08247-477">Questo include la finestra di dialogo Opzioni, SFTTray e SFTMime.</span><span class="sxs-lookup"><span data-stu-id="08247-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="08247-478">Queste impostazioni non influiscono sugli amministratori.</span><span class="sxs-lookup"><span data-stu-id="08247-478">These settings do not affect administrators.</span></span> <span data-ttu-id="08247-479">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="08247-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="08247-480">Nome tipo dati (esempi) Descrizione ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="08247-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="08247-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-481">DWORD</span></span>

<span data-ttu-id="08247-482">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-482">Default=0</span></span>

<span data-ttu-id="08247-483">Il valore 1 consente agli utenti di selezionare una lettera di unità diversa da usare come unità di file System.</span><span class="sxs-lookup"><span data-stu-id="08247-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="08247-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="08247-484">ChangeCacheSize</span></span>

<span data-ttu-id="08247-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-485">DWORD</span></span>

<span data-ttu-id="08247-486">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-486">Default=0</span></span>

<span data-ttu-id="08247-487">Il valore 1 consente agli utenti di modificare le dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="08247-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="08247-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="08247-488">ChangeLogSettings</span></span>

<span data-ttu-id="08247-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-489">DWORD</span></span>

<span data-ttu-id="08247-490">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-490">Default=0</span></span>

<span data-ttu-id="08247-491">Il valore 1 consente agli utenti di modificare il livello di log, modificarne la posizione e reimpostarlo tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="08247-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="08247-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="08247-492">AddApp</span></span>

<span data-ttu-id="08247-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-493">DWORD</span></span>

<span data-ttu-id="08247-494">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-494">Default=0</span></span>

<span data-ttu-id="08247-495">Il valore 1 consente agli utenti di aggiungere applicazioni in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="08247-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="08247-496">Questo non ha alcun effetto sulle applicazioni aggiunte tramite l'aggiornamento della pubblicazione né impedisce agli utenti di avviare (e quindi aggiungere in modo implicito) applicazioni che non sono già state aggiunte.</span><span class="sxs-lookup"><span data-stu-id="08247-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="08247-497">I valori sono 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="08247-497">Values are 0 or 1.</span></span>

<span data-ttu-id="08247-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="08247-498">LoadApp</span></span> 

<span data-ttu-id="08247-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-499">DWORD</span></span> 

<span data-ttu-id="08247-500">0</span><span class="sxs-lookup"><span data-stu-id="08247-500">0</span></span>

<span data-ttu-id="08247-501">Non consente a un utente di caricare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="08247-502">Questa è l'impostazione predefinita per gli host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="08247-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="08247-503">Se si è un utente per dispositivi mobili, è consigliabile caricare completamente le applicazioni nella cache per usarle durante l'operazione disconnessa o la modalità offline.</span><span class="sxs-lookup"><span data-stu-id="08247-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="08247-504">Per eseguire il flusso delle applicazioni dall'App-V Management Server o dall'App-V Streaming Server, è necessario essere connessi a un server per caricare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="08247-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="08247-505">1</span><span class="sxs-lookup"><span data-stu-id="08247-505">1</span></span>

<span data-ttu-id="08247-506">Consente a un utente di caricare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-506">Allows a user to load an application.</span></span> <span data-ttu-id="08247-507">Questa è l'impostazione predefinita per i desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="08247-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="08247-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="08247-508">UnloadApp</span></span> 

<span data-ttu-id="08247-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-509">DWORD</span></span> 

<span data-ttu-id="08247-510">0</span><span class="sxs-lookup"><span data-stu-id="08247-510">0</span></span>

<span data-ttu-id="08247-511">Non consente a un utente di scaricare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="08247-512">Quando carichi o scarichi un pacchetto, tutte le applicazioni nel pacchetto vengono caricate o rimosse dalla cache.</span><span class="sxs-lookup"><span data-stu-id="08247-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="08247-513">1</span><span class="sxs-lookup"><span data-stu-id="08247-513">1</span></span>

<span data-ttu-id="08247-514">Consente a un utente di scaricare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="08247-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="08247-515">LockApp</span></span> 

<span data-ttu-id="08247-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-516">DWORD</span></span> 

<span data-ttu-id="08247-517">0</span><span class="sxs-lookup"><span data-stu-id="08247-517">0</span></span>

<span data-ttu-id="08247-518">Non consente a un utente di bloccare e sbloccare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="08247-519">Questa è l'impostazione predefinita per gli host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="08247-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="08247-520">Non è possibile rimuovere un'applicazione bloccata dalla cache per creare spazio per le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="08247-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="08247-521">Per rimuovere un'applicazione bloccata dalla cache di App-V desktop o client per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario sbloccarla.</span><span class="sxs-lookup"><span data-stu-id="08247-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="08247-522">1</span><span class="sxs-lookup"><span data-stu-id="08247-522">1</span></span>

<span data-ttu-id="08247-523">Consente a un utente di bloccare e sbloccare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="08247-524">Questa è l'impostazione predefinita per i desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="08247-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="08247-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="08247-525">ManageTypes</span></span> 

<span data-ttu-id="08247-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-526">DWORD</span></span> 

<span data-ttu-id="08247-527">0</span><span class="sxs-lookup"><span data-stu-id="08247-527">0</span></span>

<span data-ttu-id="08247-528">Non consente a un utente di aggiungere, modificare o rimuovere le associazioni di tipi di file solo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="08247-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="08247-529">Questa è l'impostazione predefinita per gli host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="08247-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="08247-530">1</span><span class="sxs-lookup"><span data-stu-id="08247-530">1</span></span>

<span data-ttu-id="08247-531">Consente a un utente di aggiungere, modificare e rimuovere associazioni di tipi di file solo per l'utente e non a livello globale.</span><span class="sxs-lookup"><span data-stu-id="08247-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="08247-532">Questa è l'impostazione predefinita per i desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="08247-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="08247-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="08247-533">RefreshServer</span></span> 

<span data-ttu-id="08247-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-534">DWORD</span></span> 

<span data-ttu-id="08247-535">0</span><span class="sxs-lookup"><span data-stu-id="08247-535">0</span></span>

<span data-ttu-id="08247-536">Non consente a un utente di attivare l'aggiornamento delle impostazioni MIME.</span><span class="sxs-lookup"><span data-stu-id="08247-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="08247-537">Questa è l'impostazione predefinita per gli host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="08247-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="08247-538">1</span><span class="sxs-lookup"><span data-stu-id="08247-538">1</span></span>

<span data-ttu-id="08247-539">Consente a un utente di attivare un aggiornamento delle impostazioni MIME.</span><span class="sxs-lookup"><span data-stu-id="08247-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="08247-540">Questa è l'impostazione predefinita per i desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="08247-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="08247-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="08247-541">UpdateOSDFile</span></span>

<span data-ttu-id="08247-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-542">DWORD</span></span>

<span data-ttu-id="08247-543">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-543">Default= 0</span></span>

<span data-ttu-id="08247-544">Il valore 1 consente a un utente di usare un file OSD modificato.</span><span class="sxs-lookup"><span data-stu-id="08247-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="08247-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="08247-545">ImportApp</span></span> 

<span data-ttu-id="08247-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-546">DWORD</span></span> 

<span data-ttu-id="08247-547">0</span><span class="sxs-lookup"><span data-stu-id="08247-547">0</span></span>

<span data-ttu-id="08247-548">Non consente a un utente di importare applicazioni nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="08247-549">La differenza tra il caricamento e l'importazione è che quando viene attivato un carico, il client ottiene il pacchetto dalla posizione attualmente configurata contenuta nell'URL OSD, ASR o override.</span><span class="sxs-lookup"><span data-stu-id="08247-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="08247-550">Quando si usa l'importazione, è necessario specificare una posizione in cui ottenere il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="08247-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="08247-551">1</span><span class="sxs-lookup"><span data-stu-id="08247-551">1</span></span>

<span data-ttu-id="08247-552">Consente a un utente di importare applicazioni nella cache.</span><span class="sxs-lookup"><span data-stu-id="08247-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="08247-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="08247-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="08247-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-554">DWORD</span></span>

<span data-ttu-id="08247-555">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-555">Default=0</span></span>

<span data-ttu-id="08247-556">Il valore 1 consente agli utenti di modificare le impostazioni di aggiornamento per i server (aggiornare l'accesso e l'aggiornamento periodico).</span><span class="sxs-lookup"><span data-stu-id="08247-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="08247-557">Ciò non implica che l'utente possa modificare altre impostazioni del server (path, host e così via).</span><span class="sxs-lookup"><span data-stu-id="08247-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="08247-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="08247-558">ManageServers</span></span>

<span data-ttu-id="08247-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-559">DWORD</span></span>

<span data-ttu-id="08247-560">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-560">Default=0</span></span>

<span data-ttu-id="08247-561">Il valore 1 consente all'utente di aggiungere, modificare e rimuovere server, ad eccezione della modifica delle impostazioni di aggiornamento, che è controllata dall'autorizzazione ChangeRefreshSettings.</span><span class="sxs-lookup"><span data-stu-id="08247-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="08247-562">PublishShortcut</span><span class="sxs-lookup"><span data-stu-id="08247-562">PublishShortcut</span></span>

<span data-ttu-id="08247-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-563">DWORD</span></span>

<span data-ttu-id="08247-564">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-564">Default=0</span></span>

<span data-ttu-id="08247-565">Il valore 1 consente agli utenti di pubblicare i collegamenti tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="08247-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="08247-566">Questo non ha alcun effetto sui collegamenti pubblicati durante l'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="08247-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="08247-567">ViewAllApplications</span></span>

<span data-ttu-id="08247-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-568">DWORD</span></span>

<span data-ttu-id="08247-569">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-569">Default=0</span></span>

<span data-ttu-id="08247-570">Il valore 1 Visualizza tutte le applicazioni tramite l'interfaccia utente. in caso contrario, verranno visualizzate solo le applicazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="08247-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="08247-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="08247-571">RepairApp</span></span>

<span data-ttu-id="08247-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-572">DWORD</span></span>

<span data-ttu-id="08247-573">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-573">Default=1</span></span>

<span data-ttu-id="08247-574">Il valore 1 consente all'utente di usare l'azione di ripristino sulle applicazioni in SFTMime o nella console di gestione client.</span><span class="sxs-lookup"><span data-stu-id="08247-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="08247-575">Quando si ripristina un'applicazione, si rimuovono le impostazioni utente personalizzate e si ripristinano le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="08247-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="08247-576">Questa azione non modifica né elimina i collegamenti o le associazioni di tipi di file e non rimuove l'applicazione dalla cache.</span><span class="sxs-lookup"><span data-stu-id="08247-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="08247-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="08247-577">ClearApp</span></span>

<span data-ttu-id="08247-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-578">DWORD</span></span>

<span data-ttu-id="08247-579">Impostazione predefinita = 1</span><span class="sxs-lookup"><span data-stu-id="08247-579">Default=1</span></span>

<span data-ttu-id="08247-580">Il valore 1 consente all'utente di usare l'azione Cancella sulle applicazioni in SFTMime o nella console di gestione client.</span><span class="sxs-lookup"><span data-stu-id="08247-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="08247-581">Quando si deseleziona un'applicazione dalla console, non è più possibile usare tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="08247-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="08247-582">Tuttavia, l'applicazione rimane nella cache ed è ancora disponibile per altri utenti nello stesso sistema.</span><span class="sxs-lookup"><span data-stu-id="08247-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="08247-583">Dopo un aggiornamento della pubblicazione, le applicazioni deselezionate diventeranno di nuovo disponibili.</span><span class="sxs-lookup"><span data-stu-id="08247-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="08247-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="08247-584">DeleteApp</span></span>

<span data-ttu-id="08247-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-585">DWORD</span></span>

<span data-ttu-id="08247-586">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-586">Default=0</span></span>

<span data-ttu-id="08247-587">Il valore 1 consente all'utente di usare l'azione Elimina sulle applicazioni in SFTMime o nella console di gestione client.</span><span class="sxs-lookup"><span data-stu-id="08247-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="08247-588">Quando si elimina un'applicazione, l'applicazione selezionata non sarà più disponibile per gli utenti di tale client.</span><span class="sxs-lookup"><span data-stu-id="08247-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="08247-589">I tasti di scelta rapida e le associazioni di tipi di file vengono eliminati e l'applicazione viene eliminata dalla cache.</span><span class="sxs-lookup"><span data-stu-id="08247-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="08247-590">Tuttavia, se un'altra applicazione fa riferimento ai dati nella cache del file System o ai dati delle impostazioni per l'applicazione selezionata, questi elementi non verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="08247-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="08247-591">Dopo un aggiornamento della pubblicazione, le applicazioni eliminate diventeranno di nuovo disponibili.</span><span class="sxs-lookup"><span data-stu-id="08247-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="08247-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="08247-592">ToggleOfflineMode</span></span>

<span data-ttu-id="08247-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-593">DWORD</span></span>

<span data-ttu-id="08247-594">Il valore 1 consente agli utenti di selezionare l'esecuzione del client in modalità offline.</span><span class="sxs-lookup"><span data-stu-id="08247-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="08247-595">In modalità offline l'Application Virtualization Client può avviare un'applicazione caricata anche quando non è connessa a un Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="08247-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="08247-596">Impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="08247-596">Custom Settings</span></span>


<span data-ttu-id="08247-597">La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contiene valori specifici per i componenti front-end.</span><span class="sxs-lookup"><span data-stu-id="08247-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="08247-598">Tutte le impostazioni personalizzate vengono archiviate come stringhe.</span><span class="sxs-lookup"><span data-stu-id="08247-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="08247-599">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave CustomSettings.</span><span class="sxs-lookup"><span data-stu-id="08247-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-600">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="08247-601">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="08247-602">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="08247-603">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="08247-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-606">Impostazione predefinita = 30</span><span class="sxs-lookup"><span data-stu-id="08247-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-607">Ora in secondi che l'area di notifica di Application Virtualization visualizzerà i messaggi di errore, ad esempio &quot; Avvia non riuscito &quot; .</span><span class="sxs-lookup"><span data-stu-id="08247-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="08247-608">Valore minimo di 1.</span><span class="sxs-lookup"><span data-stu-id="08247-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="08247-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-611">Impostazione predefinita = 10</span><span class="sxs-lookup"><span data-stu-id="08247-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="08247-612">Ora in secondi che l'area di notifica di appvmed visualizzerà i messaggi di successo, ad esempio &quot; Word launched &quot; o &quot; Excel Shut down &quot; .</span><span class="sxs-lookup"><span data-stu-id="08247-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="08247-613">Se 0, questi messaggi verranno soppressi.</span><span class="sxs-lookup"><span data-stu-id="08247-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="08247-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-616">Impostazione predefinita = 0</span><span class="sxs-lookup"><span data-stu-id="08247-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-617">0 = Mostra il vassoio quando le applicazioni virtualizzate sono in uso.</span><span class="sxs-lookup"><span data-stu-id="08247-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="08247-618">1 = Mostra sempre il vassoio.</span><span class="sxs-lookup"><span data-stu-id="08247-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="08247-619">2 = non mostrare mai il vassoio.</span><span class="sxs-lookup"><span data-stu-id="08247-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="08247-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="08247-622">Quando è presente e impostato su un valore pari a 1, le applicazioni di aggiornamento delle voci di menu vengono visualizzate nel menu vassoio ed è accessibile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="08247-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="08247-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="08247-625">Quando è presente e impostato su un valore pari a 1, consente di visualizzare le applicazioni di caricamento delle voci di menu nel menu vassoio ed è accessibile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="08247-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-626">Impostazioni per la creazione di report</span><span class="sxs-lookup"><span data-stu-id="08247-626">Reporting Settings</span></span>


<span data-ttu-id="08247-627">La chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contiene valori specifici per la creazione di report in un server di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="08247-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="08247-628">La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="08247-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08247-629">Nome</span><span class="sxs-lookup"><span data-stu-id="08247-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="08247-630">Tipo</span><span class="sxs-lookup"><span data-stu-id="08247-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="08247-631">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="08247-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="08247-632">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08247-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08247-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="08247-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-635">Impostazione predefinita = 20</span><span class="sxs-lookup"><span data-stu-id="08247-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-636">Questo valore specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="08247-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="08247-637">Le dimensioni si applicano alla cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="08247-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="08247-638">Quando viene raggiunto il limite, il file di log verrà ribaltato.</span><span class="sxs-lookup"><span data-stu-id="08247-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="08247-639">Quando viene aggiunto un nuovo record (nella parte inferiore dell'elenco), uno o più record meno recenti (inizio elenco) verranno eliminati per creare spazio.</span><span class="sxs-lookup"><span data-stu-id="08247-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="08247-640">Un avviso verrà registrato nel log del client e nel log eventi la prima volta che si verificherà e non verrà più registrato fino a quando la cache non sarà stata cancellata e il log si riempirà di nuovo.</span><span class="sxs-lookup"><span data-stu-id="08247-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08247-641">DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="08247-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="08247-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-643">Impostazione predefinita = 65536</span><span class="sxs-lookup"><span data-stu-id="08247-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="08247-644">Questo valore specifica la dimensione massima in byte da trasmettere al server contemporaneamente durante l'aggiornamento della pubblicazione, per evitare errori di trasmissione permanenti quando il log ha raggiunto una dimensione significativa.</span><span class="sxs-lookup"><span data-stu-id="08247-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="08247-645">Il valore predefinito è 65536.</span><span class="sxs-lookup"><span data-stu-id="08247-645">The default value is 65536.</span></span> <span data-ttu-id="08247-646">Quando si trasmettono i dati del report sul server, un blocco di record dell'applicazione, minore o uguale alla dimensione del blocco in byte di dati XML, verrà rimosso dalla cache e inviato al server.</span><span class="sxs-lookup"><span data-stu-id="08247-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="08247-647">Ogni blocco avrà i dati generali del client e i dati dell'elenco globale dei pacchetti preceduto e questi non verranno fattorizzati nei calcoli delle dimensioni dei blocchi. il potenziale esiste per un elenco di pacchetti estremamente grande per provocare errori di trasmissione su connessioni a larghezza di banda ridotta o inaffidabili.</span><span class="sxs-lookup"><span data-stu-id="08247-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="08247-648">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08247-648">Related topics</span></span>


[<span data-ttu-id="08247-649">Riferimento per Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="08247-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)









