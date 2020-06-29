---
title: Informazioni sulla scheda Distribuzione
description: Informazioni sulla scheda Distribuzione
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819965"
---
# <span data-ttu-id="5ec6f-103">Informazioni sulla scheda Distribuzione</span><span class="sxs-lookup"><span data-stu-id="5ec6f-103">About the Deployment Tab</span></span>


<span data-ttu-id="5ec6f-104">Usare la scheda **distribuzione** nella console Application Virtualization Sequencer per modificare le informazioni relative a un'applicazione che si sta per eseguire la sequenza.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="5ec6f-105">Questa scheda contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="5ec6f-106">URL del server</span><span class="sxs-lookup"><span data-stu-id="5ec6f-106">Server URL</span></span>


<span data-ttu-id="5ec6f-107">Usare i controlli **URL del server** per specificare le impostazioni di configurazione del server delle applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ec6f-108">Controllo</span><span class="sxs-lookup"><span data-stu-id="5ec6f-108">Control</span></span></th>
<th align="left"><span data-ttu-id="5ec6f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec6f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ec6f-110">Protocollo</span><span class="sxs-lookup"><span data-stu-id="5ec6f-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-111">Consente di selezionare il protocollo che eseguirà il flusso del pacchetto dell'applicazione sequenziata da un server delle applicazioni virtuali a un client Desktop Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="5ec6f-112">Sono disponibili i protocolli seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ec6f-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="5ec6f-113">RTSP </strong> : l'impostazione predefinita specifica che il protocollo di flusso in tempo reale controlla lo scambio di applicazioni abilitate per la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="5ec6f-114">RTSPs </strong> : specifica che il protocollo di streaming in tempo reale con Transport Layer Security controlla lo scambio di un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="5ec6f-115">File </strong> : specifica che l'applicazione sequenziata verrà trasmessa da una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="5ec6f-116">HTTPS </strong> : specifica che il protocollo Secure Hypertext Transport controlla lo scambio di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ec6f-117">Hostname</span><span class="sxs-lookup"><span data-stu-id="5ec6f-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-118">Consente di selezionare il server delle applicazioni virtuali o il bilanciamento del carico davanti a un gruppo di server delle applicazioni virtuali che eseguiranno il flusso del pacchetto software in un client Desktop Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="5ec6f-119">È necessario completare questo elemento per creare un pacchetto di applicazione sequenziata, ma è possibile passare dalla variabile di ambiente% SFT_SOFTGRIDSERVER% predefinita al nome host o all'indirizzo IP effettivo di un server delle applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5ec6f-120">Nota</span><span class="sxs-lookup"><span data-stu-id="5ec6f-120">Note</span></span></strong><br/><p><span data-ttu-id="5ec6f-121">Se si sceglie di non specificare un nome host o un indirizzo IP statico, in ogni client Desktop Application Virtualization è necessario configurare una variabile di ambiente denominata SFT_SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="5ec6f-122">Il relativo valore deve essere il nome host o l'indirizzo IP del server delle applicazioni virtuali o di un bilanciamento del carico che è il client&#39;origine dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="5ec6f-123">Devi impostare questa variabile di ambiente come variabile di sistema anziché come variabile utente.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="5ec6f-124">Qualsiasi sessione client Desktop Application Virtualization che viene eseguita nel computer durante l'assegnazione di questa variabile deve essere chiusa e quindi aperta in modo che la sessione ripresa venga a conoscenza della nuova origine dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ec6f-125">Port</span><span class="sxs-lookup"><span data-stu-id="5ec6f-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-126">Consente di specificare la porta in cui il server delle applicazioni virtuali o il bilanciamento del carico ascolteranno un client Desktop Application Virtualization&#39;richiesta di s per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="5ec6f-127">Queste informazioni sono necessarie per creare un pacchetto, ma è possibile modificarlo.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="5ec6f-128">La porta predefinita è 554.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ec6f-129">Percorso</span><span class="sxs-lookup"><span data-stu-id="5ec6f-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-130">Consente di specificare il percorso relativo nel server delle applicazioni virtuali in cui è archiviato il pacchetto software e da cui verrà trasmesso.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="5ec6f-131">Queste informazioni sono necessarie per creare un pacchetto se il file SFT verrà archiviato in una sottodirectory di contenuto; in caso contrario, queste informazioni non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ec6f-132">Sistemi operativi</span><span class="sxs-lookup"><span data-stu-id="5ec6f-132">Operating Systems</span></span>


<span data-ttu-id="5ec6f-133">USA i controlli **sistemi operativi** per specificare i requisiti del sistema operativo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="5ec6f-134">Se un client Desktop Application Virtualization non supporta alcuno dei sistemi operativi selezionati, l'applicazione non si avvia.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ec6f-135">Controlli</span><span class="sxs-lookup"><span data-stu-id="5ec6f-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="5ec6f-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec6f-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ec6f-137">Sistemi operativi disponibili</span><span class="sxs-lookup"><span data-stu-id="5ec6f-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-138">Visualizza un elenco di sistemi operativi in grado di supportare le applicazioni nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ec6f-139">Sistemi operativi selezionati</span><span class="sxs-lookup"><span data-stu-id="5ec6f-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-140">Visualizza un elenco di sistemi operativi selezionati che supportano le applicazioni nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ec6f-141">Opzioni di output</span><span class="sxs-lookup"><span data-stu-id="5ec6f-141">Output Options</span></span>


<span data-ttu-id="5ec6f-142">USA i controlli delle **Opzioni di output** per specificare le opzioni di output per l'applicazione da installare.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ec6f-143">Controllo</span><span class="sxs-lookup"><span data-stu-id="5ec6f-143">Control</span></span></th>
<th align="left"><span data-ttu-id="5ec6f-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec6f-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ec6f-145">Algoritmo di compressione</span><span class="sxs-lookup"><span data-stu-id="5ec6f-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-146">Consente di selezionare il metodo per comprimere il file SFT per lo streaming in una rete.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="5ec6f-147">Selezionare uno dei metodi di compressione seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ec6f-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="5ec6f-148">Compresso </strong> : specifica che il file SFT deve essere compresso nel <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> formato zlib.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="5ec6f-149">Non compresso </strong> : l'impostazione predefinita; specifica che il file SFT non deve essere compresso.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ec6f-150">Applicare i descrittori di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5ec6f-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-151">Selezionare questa opzione per applicare i descrittori di sicurezza delle applicazioni nel pacchetto dopo la distribuzione nel client.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ec6f-152">Generare il pacchetto di Microsoft Windows Installer (MSI)</span><span class="sxs-lookup"><span data-stu-id="5ec6f-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ec6f-153">Selezionare per installare o distribuire un pacchetto di applicazione sequenziata con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="5ec6f-154">Se sono state apportate modifiche con il sequencer, le modifiche non verranno incluse nel file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="5ec6f-155">Il file di Windows Installer verrà sempre creato usando il file SFT salvato nel disco rigido.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ec6f-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ec6f-156">Related topics</span></span>


[<span data-ttu-id="5ec6f-157">Come modificare le proprietà di distribuzione</span><span class="sxs-lookup"><span data-stu-id="5ec6f-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="5ec6f-158">Console di Sequencer</span><span class="sxs-lookup"><span data-stu-id="5ec6f-158">Sequencer Console</span></span>](sequencer-console.md)









