---
title: Panoramica tecnica di Gestione avanzata Criteri di gruppo
description: Panoramica tecnica di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818296"
---
# <span data-ttu-id="63d9a-103">Panoramica tecnica di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="63d9a-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="63d9a-104">Microsoft Advanced Group Policy Management è un'applicazione client/server.</span><span class="sxs-lookup"><span data-stu-id="63d9a-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="63d9a-105">Il server Advanced Group Policy Management archivia gli oggetti Criteri di gruppo (GPO) offline nell'archivio creato da Advanced Group Policy Management nel file System del server.</span><span class="sxs-lookup"><span data-stu-id="63d9a-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="63d9a-106">Gli amministratori dei criteri di gruppo usano lo snap-in gestione avanzata Criteri di gruppo per gestire la console di Group Policy Management (GPMC) per il funzionamento con gli oggetti GPO nel server che ospita l'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="63d9a-107">Informazioni sulle parti di Advanced Group Policy Management e sugli elementi correlati, sulla modalità di archiviazione degli oggetti Criteri di gruppo nel file System e sul modo in cui le autorizzazioni controllano le azioni disponibili per ogni ruolo utente possono migliorare l'efficacia degli amministratori dei criteri di raggruppamento con Advanced</span><span class="sxs-lookup"><span data-stu-id="63d9a-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="63d9a-108">Terminologia</span><span class="sxs-lookup"><span data-stu-id="63d9a-108">Terminology</span></span>


<span data-ttu-id="63d9a-109">Di seguito vengono illustrati i termini di base per la gestione avanzata.</span><span class="sxs-lookup"><span data-stu-id="63d9a-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="63d9a-110">**Client Advanced Group Policy Management:** Computer che esegue lo snap-in Advanced Group Policy Management per la console Gestione criteri di gruppo e da cui gli amministratori dei criteri di gruppo gestiscono GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="63d9a-111">**Snap-in Advanced Group Policy Management:** Il componente software di Advanced Group Policy Management installato nei client Advanced Group Policy Management per poter gestire gli oggetti Criteri di gestione.</span><span class="sxs-lookup"><span data-stu-id="63d9a-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="63d9a-112">**Server Advanced Group Policy Management:** Un server che esegue il servizio Advanced Group Policy Management e gestisce un archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="63d9a-113">Ogni server Advanced Group Policy Management può gestire un solo archivio, ma un server Advanced Group Policy Management può gestire i dati di archiviazione per più domini in un unico archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="63d9a-114">Un archivio può essere ospitato in un computer diverso da un server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="63d9a-115">**Servizio Advanced Group Policy:** Il componente software di Advanced Group Policy Management eseguito in un server Advanced Group Policy Management come servizio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="63d9a-116">Il servizio gestisce i GPO nell'archivio e nell'ambiente di produzione in tale foresta.</span><span class="sxs-lookup"><span data-stu-id="63d9a-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="63d9a-117">**Archivio:** In Advanced Group Policy Management, un archivio centrale che contiene i GPO controllati gestiti dal server Advanced Group Policy Management, oltre alla cronologia di ognuno di questi GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="63d9a-118">Include tutte le versioni precedenti controllate di ogni oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="63d9a-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="63d9a-119">Un archivio è costituito da un file di indice di archiviazione e da dati di archiviazione associati che potrebbero includere dati per gli oggetti Criteri di gruppo in più domini.</span><span class="sxs-lookup"><span data-stu-id="63d9a-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="63d9a-120">Un archivio può essere ospitato in un computer diverso da un server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="63d9a-121">**GPO controllato:** Un GPO gestito da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="63d9a-122">Advanced Group Policy Management gestisce la cronologia e le autorizzazioni degli oggetti Criteri di controllo, che vengono archiviati nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="63d9a-123">**GPO non controllato:** Un GPO nell'ambiente di produzione per un dominio e non gestito da Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="63d9a-124">Quali Advanced Group Policy Management installa, crea e influenza</span><span class="sxs-lookup"><span data-stu-id="63d9a-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="63d9a-125">In un server Advanced Group Policy Management il programma di configurazione Advanced Group Policy Management installa il servizio Advanced Group Policy.</span><span class="sxs-lookup"><span data-stu-id="63d9a-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="63d9a-126">Advanced Group Policy Management non modifica il servizio directory® Active Directory o lo schema.</span><span class="sxs-lookup"><span data-stu-id="63d9a-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="63d9a-127">Per impostazione predefinita, i file di programma del server Advanced Group Policy Management sono installati in%ProgramFiles%\\Microsoft\\AGPM\\Server.</span><span class="sxs-lookup"><span data-stu-id="63d9a-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="63d9a-128">È possibile installare il servizio Advanced Group Policy Management su un controller di dominio, se necessario; Tuttavia, è consigliabile installare il servizio Advanced Group Policy Management in un server membro.</span><span class="sxs-lookup"><span data-stu-id="63d9a-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="63d9a-129">In un client Advanced Group Policy Management, il programma di configurazione Advanced Group Policy Management installa lo snap-in Advanced Group Policy Management, aggiungendo una cartella del **controllo di modifica** a ogni dominio visualizzato in GPMC.</span><span class="sxs-lookup"><span data-stu-id="63d9a-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="63d9a-130">Per impostazione predefinita, i file di programma client Advanced Group Policy Management vengono installati in%ProgramFiles%\\Microsoft\\AGPM\\Client.</span><span class="sxs-lookup"><span data-stu-id="63d9a-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="63d9a-131">La tabella 1 descrive sia gli elementi installati o creati da Advanced Group Policy che le parti del sistema operativo che influiscono sull'operazione Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="63d9a-132">Tabella 1: elementi installati, creati o interessati da Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="63d9a-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63d9a-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="63d9a-133">Item</span></span></th>
<th align="left"><span data-ttu-id="63d9a-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63d9a-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63d9a-135">Servizio Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="63d9a-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-136">Il servizio Advanced Group Policy Management viene eseguito nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="63d9a-137">Il servizio gestisce l'archivio, che contiene GPO offline e i GPO controllati nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="63d9a-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="63d9a-138">La configurazione predefinita del servizio Advanced Group Policy Management è la seguente:</span><span class="sxs-lookup"><span data-stu-id="63d9a-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="63d9a-139">Nome servizio: </strong> Servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="63d9a-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-140">Nome visualizzato: </strong> Servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="63d9a-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-141">Percorso del file eseguibile: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="63d9a-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-142">Avvio: </strong> automatico</span><span class="sxs-lookup"><span data-stu-id="63d9a-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-143">Accedere come: </strong> account del servizio Advanced Group Policy Management specificato durante l'installazione del server Advanced Group Policy Management, che può essere modificato usando <strong> programmi e funzionalità </strong> nel <strong> Pannello di controllo </strong> .</span><span class="sxs-lookup"><span data-stu-id="63d9a-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63d9a-144">Archivio Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="63d9a-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-145">Per impostazione predefinita, Advanced Group Policy Management crea l'archivio in%ProgramData%\Microsoft\AGPM nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="63d9a-146">L'archivio fornisce spazio di archiviazione per gli oggetti Criteri di gruppo offline e può archiviare più versioni di ogni oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="63d9a-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="63d9a-147">Le modifiche apportate da Advanced Group Policy Management agli oggetti Criteri di gruppo nell'archivio non influiscono sull'ambiente di produzione finché un amministratore o un responsabile della gestione avanzata non distribuisce il GPO all'ambiente di produzione e collega il GPO a un'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="63d9a-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63d9a-148">Windows Firewall</span><span class="sxs-lookup"><span data-stu-id="63d9a-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-149">Durante l'installazione, Advanced Group Policy Management consente una regola Windows Firewall in ingresso che consente al client Advanced Group Policy Management di comunicare con il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="63d9a-150">La regola predefinita di Windows Firewall è la seguente:</span><span class="sxs-lookup"><span data-stu-id="63d9a-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="63d9a-151">Nome: </strong> Servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="63d9a-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-152">Azione: </strong> Consenti la connessione</span><span class="sxs-lookup"><span data-stu-id="63d9a-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-153">Programmi: </strong> tutti i programmi che soddisfano le condizioni specificate</span><span class="sxs-lookup"><span data-stu-id="63d9a-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-154">Tipo di protocollo: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="63d9a-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-155">Porta locale: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="63d9a-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-156">Porta remota: </strong> tutte le porte</span><span class="sxs-lookup"><span data-stu-id="63d9a-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-157">Indirizzo IP locale: </strong> qualsiasi</span><span class="sxs-lookup"><span data-stu-id="63d9a-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="63d9a-158">Indirizzo IP remoto: </strong> qualsiasi</span><span class="sxs-lookup"><span data-stu-id="63d9a-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63d9a-159">Server di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="63d9a-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-160">Advanced Group Policy Management usa SMTP (Simple Mail Transfer Protocol) per inviare richieste di posta elettronica agli indirizzi configurati nella <strong> scheda delega del dominio </strong> . Ad esempio, quando un editor richiede la creazione di un nuovo GPO, Advanced Group Policy Management informa ogni indirizzo di posta elettronica specificato nella <strong> scheda delega del dominio </strong> .</span><span class="sxs-lookup"><span data-stu-id="63d9a-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63d9a-161">Snap-in Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="63d9a-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-162">Lo snap-in Advanced Group Policy Management per GPMC viene eseguito nei client Advanced Group Policy Management e viene usato dagli amministratori dei criteri di gruppo per gestire i GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="63d9a-163">Lo snap-in viene visualizzato nella cartella GPMC come <strong> controllo </strong> di modifica in ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="63d9a-164">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="63d9a-164">Additional references</span></span>

<span data-ttu-id="63d9a-165">Per altre informazioni sui file installati da Advanced Group Policy Management, vedere la [Guida alla pianificazione per Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=160060).</span><span class="sxs-lookup"><span data-stu-id="63d9a-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="63d9a-166">Archive</span><span class="sxs-lookup"><span data-stu-id="63d9a-166">Archive</span></span>


<span data-ttu-id="63d9a-167">Per impostazione predefinita, il processo di installazione del server Advanced Group Policy Management crea l'archivio nel disco rigido locale del server Advanced Group Policy Management su%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="63d9a-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="63d9a-168">Tuttavia, è possibile modificare il percorso durante l'installazione e persino creare l'archivio in un server diverso da quello della Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="63d9a-169">L'archivio contiene una sottocartella per ogni versione di ogni GPO che contiene l'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="63d9a-170">Il nome di ogni sottocartella è un GUID che identifica una versione dell'oggetto Criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="63d9a-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="63d9a-171">Il file gpostate.xml registra lo stato di ogni oggetto Criteri di stato nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="63d9a-172">Il file è un manifesto che descrive il contenuto dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="63d9a-173">Ad esempio, un GPO può avere molte versioni e ogni versione si trova nella sottocartella dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="63d9a-174">Il file gpostate.xml indica le sottocartelle che contengono versioni diverse di un singolo oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="63d9a-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="63d9a-175">Inoltre, i modelli GPO hanno sottocartelle nell'archivio, ma gpostate.xml indica che si tratta di modelli e GPO non controllati.</span><span class="sxs-lookup"><span data-stu-id="63d9a-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="63d9a-176">Allo stesso modo, quando gli amministratori di criteri di gruppo eliminano i GPO, Advanced Group Policy Management cambia gli stati in gpostate.xml per indicare che si trovano nel **Cestino** , ma non rimuovono effettivamente le sottocartelle degli oggetti GPO dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="63d9a-177">**Attenzione**  Non modificare manualmente gpostate.xml o i GPO che contiene l'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="63d9a-178">Queste informazioni vengono fornite solo per migliorare la comprensione dell'Archivio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="63d9a-179">USA invece lo snap-in Advanced Group Policy Management per modificare i GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="63d9a-180">Quando Advanced Group Policy Management crea l'archivio, fornisce il controllo completo a sistema, agli amministratori e all'account del servizio Advanced Group Policy Management (specificato nella configurazione del server Advanced Group Policy Management).</span><span class="sxs-lookup"><span data-stu-id="63d9a-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="63d9a-181">La modifica delle autorizzazioni tramite l'interfaccia utente di Advanced Group Policy Management nello snap-in Advanced Group Policy Management non modifica le autorizzazioni per l'archivio, perché l'account del servizio Advanced Group Policy Management esegue tutte le operazioni per conto dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="63d9a-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="63d9a-182">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="63d9a-182">Additional references</span></span>

<span data-ttu-id="63d9a-183">Per informazioni su come eseguire il backup dell'archivio, ripristinare l'archivio da un backup o trasferire sia il server Advanced Group Policy Management che l'archivio, vedere la sezione "esecuzione di attività di amministratore Advanced Group Policy Management" nella [Guida alle operazioni per Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="63d9a-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="63d9a-184">Ruoli e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="63d9a-184">Roles and permissions</span></span>


<span data-ttu-id="63d9a-185">I ruoli semplificano la delega.</span><span class="sxs-lookup"><span data-stu-id="63d9a-185">Roles simplify delegation.</span></span> <span data-ttu-id="63d9a-186">Invece di assegnare autorizzazioni dettagliate agli amministratori dei criteri di gruppo, gli amministratori della Advanced Group Policy Management possono assegnare uno dei quattro ruoli agli amministratori dei criteri di gruppo per consentire loro di eseguire il lavoro correlato a tale ruolo:</span><span class="sxs-lookup"><span data-stu-id="63d9a-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="63d9a-187">**Amministratore Advanced Group Policy Management:** Gli amministratori dei criteri di gruppo assegnati al ruolo amministratore Advanced Group Policy Management (controllo completo) possono eseguire qualsiasi attività in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="63d9a-188">Gli amministratori della gestione avanzata Criteri di amministrazione possono configurare opzioni a livello di dominio e delega ad altri amministratori di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="63d9a-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="63d9a-189">**Approvatore:** Gli amministratori dei criteri di gruppo assegnati al ruolo approvazione possono distribuire GPO nell'ambiente di produzione per un dominio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="63d9a-190">I responsabili approvazione possono anche creare ed eliminare GPO e approvare o rifiutare le richieste dagli editori.</span><span class="sxs-lookup"><span data-stu-id="63d9a-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="63d9a-191">I responsabili approvazione possono visualizzare l'elenco degli oggetti Criteri di dominio, visualizzare le impostazioni dei criteri in GPO e creare e visualizzare i report delle impostazioni di criteri in un GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="63d9a-192">Non è possibile modificare le impostazioni dei criteri in GPO a meno che non venga assegnato anche il ruolo di editor.</span><span class="sxs-lookup"><span data-stu-id="63d9a-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="63d9a-193">**Editor:** Gli amministratori dei criteri di gruppo assegnati al ruolo dell'editor possono visualizzare l'elenco degli oggetti GPO in un dominio, visualizzare le impostazioni dei criteri in GPO, modificare le impostazioni dei criteri in GPO e creare e visualizzare i report delle impostazioni di criteri in un GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="63d9a-194">A meno che non sia anche assegnato il ruolo di approvatore, gli editor non possono creare, distribuire o eliminare GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="63d9a-195">Tuttavia, possono richiedere che i GPO vengano creati, distribuiti o eliminati.</span><span class="sxs-lookup"><span data-stu-id="63d9a-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="63d9a-196">**Revisore:** Gli amministratori dei criteri di gruppo assegnati al ruolo revisore possono visualizzare l'elenco dei GPO in un dominio e creare e visualizzare i report delle impostazioni dei criteri in un GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="63d9a-197">A meno che non sia anche assegnato il ruolo di editor, non possono modificare le impostazioni dei criteri in un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="63d9a-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="63d9a-198">Advanced Group Policy Management offre agli amministratori della gestione avanzata la flessibilità di configurare le autorizzazioni a un livello più dettagliato rispetto ai ruoli usando lo snap-in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="63d9a-199">La tabella 2 descrive queste autorizzazioni e indica le autorizzazioni concesse a ogni ruolo per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="63d9a-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63d9a-200">Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="63d9a-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="63d9a-201">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63d9a-201">Description</span></span></th>
<th align="left"><span data-ttu-id="63d9a-202">Amministratore della Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="63d9a-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="63d9a-203">Responsabile approvazione</span><span class="sxs-lookup"><span data-stu-id="63d9a-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="63d9a-204">Editor</span><span class="sxs-lookup"><span data-stu-id="63d9a-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="63d9a-205">Revisore</span><span class="sxs-lookup"><span data-stu-id="63d9a-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63d9a-206">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="63d9a-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-207">Avere tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="63d9a-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-208">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63d9a-209">Creare un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="63d9a-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-210">Creare GPO in un dominio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-211">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-212">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63d9a-213">Contenuto dell'elenco</span><span class="sxs-lookup"><span data-stu-id="63d9a-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-214">Elencare i GPO in un dominio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-215">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-216">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-217">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-218">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63d9a-219">Impostazioni di lettura</span><span class="sxs-lookup"><span data-stu-id="63d9a-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-220">Leggere le impostazioni dei criteri in un GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-221">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-222">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-223">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-224">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63d9a-225">Modificare le impostazioni</span><span class="sxs-lookup"><span data-stu-id="63d9a-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-226">Modificare le impostazioni dei criteri in un GPO.</span><span class="sxs-lookup"><span data-stu-id="63d9a-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-227">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63d9a-228">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63d9a-229">Elimina GPO</span><span class="sxs-lookup"><span data-stu-id="63d9a-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-230">Eliminare un oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="63d9a-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-231">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-232">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63d9a-233">Modificare la sicurezza</span><span class="sxs-lookup"><span data-stu-id="63d9a-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-234">Delegare l'accesso a livello di dominio, delegare l'accesso a un singolo GPO e delegare l'accesso all'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="63d9a-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-235">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63d9a-236">Distribuire un oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="63d9a-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-237">Distribuire un GPO dall'archivio all'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="63d9a-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-238">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-239">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63d9a-240">Creare un modello</span><span class="sxs-lookup"><span data-stu-id="63d9a-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-241">Creare un modello di GPO in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="63d9a-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-242">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63d9a-243">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63d9a-244">Opzioni di modifica</span><span class="sxs-lookup"><span data-stu-id="63d9a-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-245">Configurare la notifica tramite posta elettronica Advanced Group Policy e limitare le versioni di GPO archiviate nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="63d9a-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-246">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63d9a-247">Esporta GPO</span><span class="sxs-lookup"><span data-stu-id="63d9a-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-248">Esportare un oggetto Criteri di stato in un file.</span><span class="sxs-lookup"><span data-stu-id="63d9a-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-249">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63d9a-250">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63d9a-251">Importa oggetto Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="63d9a-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63d9a-252">Importare un GPO da un file.</span><span class="sxs-lookup"><span data-stu-id="63d9a-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="63d9a-253">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="63d9a-254">Sì</span><span class="sxs-lookup"><span data-stu-id="63d9a-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="63d9a-255">**Nota** 
 Le autorizzazioni **Esporta** GPO e **Importa GPO** non sono disponibili in advanced Group policy Management 3,0 o 2,5.</span><span class="sxs-lookup"><span data-stu-id="63d9a-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="63d9a-256">La possibilità di delegare l'accesso a GPO nell'ambiente di produzione per un dominio e la possibilità di limitare il numero di versioni degli oggetti Criteri di archiviazione non sono disponibili in Advanced Group Policy Management 2,5.</span><span class="sxs-lookup"><span data-stu-id="63d9a-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="63d9a-257">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="63d9a-257">Additional references</span></span>

<span data-ttu-id="63d9a-258">Per informazioni sulle attività che possono essere eseguite dagli amministratori dei criteri di gruppo assegnati a un determinato ruolo o sulle autorizzazioni necessarie per eseguire un'attività specifica, vedere la [Guida alle operazioni per Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="63d9a-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





