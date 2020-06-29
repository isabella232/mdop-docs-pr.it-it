---
title: Panoramica di Application Virtualization
description: Panoramica di Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816065"
---
# <span data-ttu-id="0d704-103">Panoramica di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0d704-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="0d704-104">Microsoft Application Virtualization (App-V) può rendere le applicazioni disponibili per i computer degli utenti finali senza dover installare le applicazioni direttamente in tali computer.</span><span class="sxs-lookup"><span data-stu-id="0d704-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="0d704-105">Ciò viene reso possibile tramite un processo noto come *sequenziamento dell'applicazione*, che consente l'esecuzione di ogni applicazione nel proprio ambiente virtuale autonomo nel computer client.</span><span class="sxs-lookup"><span data-stu-id="0d704-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="0d704-106">Le applicazioni sequenziate vengono isolate l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="0d704-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="0d704-107">In questo articolo vengono eliminati i conflitti di applicazione, ma le applicazioni possono comunque interagire con il computer client.</span><span class="sxs-lookup"><span data-stu-id="0d704-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="0d704-108">Il client App-V è la caratteristica che consente all'utente finale di interagire con le applicazioni dopo che sono state pubblicate nel computer.</span><span class="sxs-lookup"><span data-stu-id="0d704-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="0d704-109">Il client gestisce l'ambiente virtuale in cui vengono eseguite le applicazioni virtualizzate in ogni computer.</span><span class="sxs-lookup"><span data-stu-id="0d704-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="0d704-110">Dopo l'installazione del client in un computer, le applicazioni devono essere messe a disposizione del computer tramite un processo noto come *pubblicazione*, che consente all'utente finale di eseguire le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="0d704-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="0d704-111">Il processo di pubblicazione copia le icone e i tasti di scelta rapida dell'applicazione virtuale nel computer, in genere nel desktop di Windows o nel menu **Start** , e copia anche le informazioni di associazione per la definizione del pacchetto e il tipo di file nel computer.</span><span class="sxs-lookup"><span data-stu-id="0d704-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="0d704-112">La pubblicazione rende inoltre disponibile il contenuto del pacchetto dell'applicazione per il computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="0d704-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="0d704-113">Il contenuto del pacchetto dell'applicazione virtuale può essere copiato in uno o più server di virtualizzazione dell'applicazione in modo che possa essere trasmesso ai client su richiesta e memorizzato nella cache localmente.</span><span class="sxs-lookup"><span data-stu-id="0d704-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="0d704-114">I server di file e i server Web possono essere usati anche come server di streaming oppure il contenuto può essere copiato direttamente nel computer dell'utente finale, ad esempio se si usa un sistema di distribuzione del software elettronico, come Microsoft endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0d704-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="0d704-115">In un'implementazione multiserver, il mantenimento del contenuto del pacchetto e la sua conservazione aggiornata in tutti i server di flusso richiedono una soluzione di gestione dei pacchetti completa.</span><span class="sxs-lookup"><span data-stu-id="0d704-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="0d704-116">A seconda delle dimensioni dell'organizzazione, potrebbe essere necessario disporre di molte applicazioni virtuali disponibili per gli utenti finali dislocate in tutto il mondo.</span><span class="sxs-lookup"><span data-stu-id="0d704-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="0d704-117">La gestione dei pacchetti per garantire che le applicazioni appropriate siano disponibili per tutti gli utenti dove e quando è necessario accedervi è quindi un requisito importante.</span><span class="sxs-lookup"><span data-stu-id="0d704-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="0d704-118">Funzionalità di Microsoft Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="0d704-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="0d704-119">La tabella seguente descrive le caratteristiche principali di Microsoft Application Virtualization Management System.</span><span class="sxs-lookup"><span data-stu-id="0d704-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0d704-120">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="0d704-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="0d704-121">Funzione</span><span class="sxs-lookup"><span data-stu-id="0d704-121">Function</span></span></th>
<th align="left"><span data-ttu-id="0d704-122">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="0d704-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0d704-123">Microsoft Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="0d704-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-124">Responsabile dello streaming del contenuto del pacchetto e della pubblicazione dei collegamenti e delle associazioni di tipi di file al client di Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="0d704-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-125">L'Application Virtualization Management Server supporta l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="0d704-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0d704-126"></strong>Cartella contenuto</span><span class="sxs-lookup"><span data-stu-id="0d704-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-127">Indica la posizione dei pacchetti di virtualizzazione dell'applicazione per il flusso.</span><span class="sxs-lookup"><span data-stu-id="0d704-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-128">Questa cartella può essere posizionata in una condivisione inserita o disattivata dall'Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="0d704-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0d704-129">Microsoft Application Virtualization Management Console</span><span class="sxs-lookup"><span data-stu-id="0d704-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-130">Questa console è uno strumento di gestione dello snap-in MMC 3,0 usato per l'amministrazione di Microsoft Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="0d704-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-131">Questo strumento può essere installato nel server di Microsoft Application Virtualization o in una workstation separata che include Microsoft Management Console (MMC) 3.0 e Microsoft. NETFramework 2,0 installato.</span><span class="sxs-lookup"><span data-stu-id="0d704-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0d704-132">Servizio Web Microsoft Application Virtualization Management</span><span class="sxs-lookup"><span data-stu-id="0d704-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-133">Responsabile della comunicazione delle richieste di lettura e scrittura all'archivio dati di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d704-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-134">Il servizio Web di gestione può essere installato nel server Microsoft Application Virtualization Management o in un computer separato in cui è installato Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="0d704-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0d704-135">Archivio dati di Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0d704-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-136">Database di SQL Server App-V responsabile dell'archiviazione di tutte le informazioni relative all'infrastruttura di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d704-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-137">Queste informazioni includono tutti i record delle applicazioni, le assegnazioni delle applicazioni e i gruppi che hanno la responsabilità di gestire l'ambiente di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d704-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0d704-138">Microsoft Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="0d704-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-139">Responsabile dell'hosting dei pacchetti Application Virtualization per lo streaming ai client in una filiale, in cui il collegamento all'Application Virtualization Management Server è considerato una connessione WAN (Wide Area Networks).</span><span class="sxs-lookup"><span data-stu-id="0d704-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-140">Questo server contiene solo funzionalità di flusso e non fornisce né l'Application Virtualization Management Console né il servizio Web Application Virtualization Management.</span><span class="sxs-lookup"><span data-stu-id="0d704-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0d704-141">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="0d704-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-142">Il sequencer viene usato per monitorare e acquisire l'installazione di applicazioni per creare pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="0d704-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-143">L'output è costituito dalle icone dell'applicazione, un file con estensione OSD che contiene informazioni sulla definizione del pacchetto, un file manifesto del pacchetto e il file SFT che contiene i file di contenuto del programma applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d704-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0d704-144">Microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="0d704-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-145">Il client Desktop Application Virtualization e il client di Application Virtualization per Servizi Desktop remoto consentono di gestire l'ambiente virtuale per le applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="0d704-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0d704-146">Il client Microsoft Application Virtualization gestisce il flusso del pacchetto in cache, aggiornamento della pubblicazione, trasporto e tutte le interazioni con i server di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d704-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





