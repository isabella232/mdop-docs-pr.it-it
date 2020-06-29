---
title: Panoramica di uno scenario basato su Application Virtualization Server
description: Panoramica di uno scenario basato su Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822095"
---
# <span data-ttu-id="2d8f8-103">Panoramica di uno scenario basato su Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="2d8f8-104">Se si prevede di usare uno scenario di distribuzione basato su server per l'ambiente di virtualizzazione delle applicazioni Microsoft, è importante comprendere le differenze tra *Application Virtualization Management Server* e *Application Virtualization Streaming Server*.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="2d8f8-105">In questo argomento vengono illustrate le differenze e vengono fornite anche informazioni sui metodi di recapito dei pacchetti, sui protocolli di trasmissione e sui componenti esterni che è necessario considerare mentre si procede alla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="2d8f8-106">Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="2d8f8-107">L'Application Virtualization Management Server esegue sia la funzione Publishing che la funzione streaming.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="2d8f8-108">Il server pubblica le icone delle applicazioni, i collegamenti e le associazioni di tipi di file nei client App-V per gli utenti autorizzati.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="2d8f8-109">Quando vengono ricevute richieste utente per le applicazioni, il server trasmette i dati su richiesta agli utenti autorizzati usando i protocolli RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="2d8f8-110">Nella maggior parte delle configurazioni che usano questo server, uno o più server di gestione condividono un archivio dati comune per le informazioni di configurazione e pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="2d8f8-111">I server di gestione della virtualizzazione delle applicazioni usano i gruppi di Active Directory per gestire l'autorizzazione degli utenti.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="2d8f8-112">Oltre ai servizi di dominio Active Directory, questi server hanno installato SQL Server per la gestione del database e dell'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="2d8f8-113">Il server di gestione viene controllato tramite Application Virtualization Management Console, uno snap-in di Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="2d8f8-114">Dato che le applicazioni di flusso di Application Virtualization Management Server vengono trasmesse agli utenti finali su richiesta, questi server sono ideali per le configurazioni di sistema con LAN affidabili e a larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="2d8f8-115">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="2d8f8-116">Application Virtualization Streaming Server offre le stesse funzionalità di aggiornamento di flusso e pacchetto fornite dal server di gestione, ma senza i requisiti di Active Directory o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="2d8f8-117">Tuttavia, il server di flusso non dispone di un servizio di pubblicazione, né offre licenze o funzionalità di misurazione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="2d8f8-118">Il servizio di pubblicazione di un server di gestione di App-V distinto viene usato in combinazione con App-V Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="2d8f8-119">App-V streaming server risponde alle esigenze delle aziende che vogliono usare la virtualizzazione delle applicazioni in più posizioni con le funzionalità di flusso della configurazione classica del server, ma potrebbero non avere l'infrastruttura per supportare i server di gestione di App-V in ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="2d8f8-120">L'Application Virtualization Streaming Server può essere usato anche in ambienti con un sistema ESD (Electronic Software Distribution System) esistente.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="2d8f8-121">Si usa l'ESD per gestire le applicazioni di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="2d8f8-122">Diversamente dall'Application Virtualization Management Server, il server di streaming non usa SQL o una console di gestione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="2d8f8-123">Questi server usano gli elenchi di controllo di accesso (ACL) per concedere l'autorizzazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="2d8f8-124">Metodi di distribuzione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="2d8f8-124">Package Delivery Methods</span></span>


<span data-ttu-id="2d8f8-125">Se si prevede di usare un Application Virtualization Server come metodo di recapito della pubblicazione, è necessario determinare quale dei seguenti metodi di recapito del pacchetto si applica allo scenario:</span><span class="sxs-lookup"><span data-stu-id="2d8f8-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="2d8f8-126">Recapito dinamico del pacchetto</span><span class="sxs-lookup"><span data-stu-id="2d8f8-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="2d8f8-127">Caricamento da un pacchetto di file</span><span class="sxs-lookup"><span data-stu-id="2d8f8-127">Load from file package delivery</span></span>*

### <span data-ttu-id="2d8f8-128">Recapito dinamico del pacchetto</span><span class="sxs-lookup"><span data-stu-id="2d8f8-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="2d8f8-129">Durante il recapito dinamico del pacchetto, il server (Application Virtualization Management Server, Application Virtualization Streaming Server o IIS Server) offre le applicazioni virtualizzate agli utenti finali tramite la distribuzione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="2d8f8-130">Il server recapita le applicazioni e i pacchetti virtualizzati a un computer client solo quando un utente tenta prima di avviare un'applicazione (su richiesta).</span><span class="sxs-lookup"><span data-stu-id="2d8f8-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="2d8f8-131">Il server trasmette solo i blocchi necessari per avviare l'applicazione (blocco di funzionalità principale).</span><span class="sxs-lookup"><span data-stu-id="2d8f8-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="2d8f8-132">Dopo che il blocco di funzionalità principale viene recapitato al client, l'applicazione viene eseguita; il client non riceve l'applicazione completa (distribuzione incrementale), a meno che il client non abbia bisogno di accedere a una parte dell'applicazione non inclusa nel blocco di funzionalità principale.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="2d8f8-133">In questo caso, il client esegue una richiesta fuori sequenza e il blocco di funzionalità secondario viene trasmesso al client.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="2d8f8-134">Il recapito dinamico del pacchetto consente l'avvio rapido dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="2d8f8-135">Caricamento da un pacchetto di file</span><span class="sxs-lookup"><span data-stu-id="2d8f8-135">Load from File Package Delivery</span></span>

<span data-ttu-id="2d8f8-136">Per il caricamento da un pacchetto di file, il server recapita l'intero pacchetto di applicazioni virtualizzate a un computer client prima che l'utente avvii l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="2d8f8-137">In questo scenario, le applicazioni virtualizzate vengono recapitate come pacchetto completo, anziché tramite il metodo dinamico incrementale usato dal modello di recapito dinamico.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="2d8f8-138">**Nota**  Per ogni metodo di recapito, il processo di recapito dell'applicazione virtuale iniziale e il processo di aggiornamento delle applicazioni virtuali sono gli stessi. il pacchetto di applicazione virtuale aggiornato sostituisce il pacchetto di applicazione originale.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="2d8f8-139">Nella tabella seguente vengono confrontati i vantaggi e gli svantaggi di ogni metodo di recapito del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2d8f8-140">Metodo</span><span class="sxs-lookup"><span data-stu-id="2d8f8-140">Method</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-141">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="2d8f8-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-142">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="2d8f8-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d8f8-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d8f8-144">Recapito dinamico del pacchetto</span><span class="sxs-lookup"><span data-stu-id="2d8f8-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-145">Le applicazioni vengono recapitate e aggiornate su richiesta.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="2d8f8-146">Le applicazioni vengono recapitate e aggiornate in modo incrementale per ottimizzare il tempo di avvio.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="2d8f8-147">Gli aggiornamenti vengono recapitati automaticamente al desktop client.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-148">Maggiore ingombro nella topologia aziendale a causa dei requisiti del server.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="2d8f8-149">Lo streaming delle applicazioni deve essere su una LAN; gli scenari di distribuzione su una rete WAN o che usano una connessione non affidabile o intermittente tra il server e il client potrebbero essere inutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-150">Richiede un'infrastruttura di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="2d8f8-151">Windows Installer usato per distribuire il software client Desktop Application Virtualization per i computer degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="2d8f8-152">Le grandi aziende dovrebbero usare i server di streaming Application Virtualization come punti di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d8f8-153">Caricamento da un pacchetto di file</span><span class="sxs-lookup"><span data-stu-id="2d8f8-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-154">Coerenti con le tipiche procedure di gestione aziendale.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="2d8f8-155">Supporta lo scenario di configurazione autonomo.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="2d8f8-156">Fornisce una soluzione a un problema di micro-filiale aziendale.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-157">Il recapito e l'aggiornamento delle applicazioni non sono possibili su richiesta.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="2d8f8-158">Il recapito e l'aggiornamento delle applicazioni non sono incrementali. aumenta il consumo di risorse rispetto al recapito dinamico.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-159">L'organizzazione IT è spesso responsabile della gestione delle licenze dell'applicazione, dell'autorizzazione dell'utente e dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2d8f8-160">Protocolli e componenti esterni correlati al server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="2d8f8-161">La tabella seguente elenca i tipi di server che possono essere usati in uno scenario basato su Application Virtualization Server, insieme ai relativi protocolli di trasmissione e ai componenti esterni necessari per supportare la configurazione specifica del server.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="2d8f8-162">La tabella include anche il meccanismo di creazione di report e il meccanismo di aggiornamento attivo per ogni tipo di server.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="2d8f8-163">Poiché questi scenari usano tutti il server di gestione della virtualizzazione dell'applicazione, è possibile usare le funzionalità di creazione di report interne integrate nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="2d8f8-164">Se si usa una Application Virtualization Management o un Application Virtualization Streaming Server per consegnare i pacchetti al client, i pacchetti sul server vengono aggiornati automaticamente quando un utente accede al client; Se si usano server IIS o un file per consegnare i pacchetti al client, i pacchetti nel client devono essere aggiornati manualmente.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2d8f8-165">Tipo di server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-166">Protocolli</span><span class="sxs-lookup"><span data-stu-id="2d8f8-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-167">Componenti esterni necessari</span><span class="sxs-lookup"><span data-stu-id="2d8f8-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-168">Creazione di rapporti</span><span class="sxs-lookup"><span data-stu-id="2d8f8-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="2d8f8-169">Aggiornamento attivo</span><span class="sxs-lookup"><span data-stu-id="2d8f8-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d8f8-170">Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-171">RTSP</span><span class="sxs-lookup"><span data-stu-id="2d8f8-171">RTSP</span></span></p>
<p><span data-ttu-id="2d8f8-172">RTSPS</span><span class="sxs-lookup"><span data-stu-id="2d8f8-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-173">Quando si usa HTTPS, usare un server IIS per scaricare i file ICO e OSD e un firewall per proteggere il server dall'esposizione a Internet.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-174">Interna</span><span class="sxs-lookup"><span data-stu-id="2d8f8-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-175">Supportato</span><span class="sxs-lookup"><span data-stu-id="2d8f8-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d8f8-176">Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-177">RTSP</span><span class="sxs-lookup"><span data-stu-id="2d8f8-177">RTSP</span></span></p>
<p><span data-ttu-id="2d8f8-178">RTSPS</span><span class="sxs-lookup"><span data-stu-id="2d8f8-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-179">Usare un meccanismo per sincronizzare il contenuto tra il server di gestione e il server di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="2d8f8-180">Quando si usa HTTPS, usare un server IIS per scaricare i file ICO e OSD e usare un firewall per proteggere il server dall'esposizione a Internet.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-181">Interna</span><span class="sxs-lookup"><span data-stu-id="2d8f8-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-182">Supportato</span><span class="sxs-lookup"><span data-stu-id="2d8f8-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2d8f8-183">Server IIS</span><span class="sxs-lookup"><span data-stu-id="2d8f8-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="2d8f8-184">HTTP</span></span></p>
<p><span data-ttu-id="2d8f8-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="2d8f8-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-186">Usare un meccanismo per sincronizzare il contenuto tra il server di gestione e il server di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="2d8f8-187">Quando si usa HTTP o HTTPS, usare un server IIS per scaricare i file ICO e OSD e un firewall per proteggere il server dall'esposizione a Internet.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-188">Interna</span><span class="sxs-lookup"><span data-stu-id="2d8f8-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-189">Non supportato</span><span class="sxs-lookup"><span data-stu-id="2d8f8-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2d8f8-190">File</span><span class="sxs-lookup"><span data-stu-id="2d8f8-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-191">SMB</span><span class="sxs-lookup"><span data-stu-id="2d8f8-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-192">È necessario un modo per sincronizzare il contenuto tra il server di gestione e il server di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="2d8f8-193">È necessario un computer client con funzionalità di condivisione file o flusso.</span><span class="sxs-lookup"><span data-stu-id="2d8f8-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-194">Interna</span><span class="sxs-lookup"><span data-stu-id="2d8f8-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="2d8f8-195">Non supportato</span><span class="sxs-lookup"><span data-stu-id="2d8f8-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2d8f8-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d8f8-196">Related topics</span></span>


[<span data-ttu-id="2d8f8-197">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="2d8f8-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="2d8f8-198">Come configurare i server per la distribuzione basata su server</span><span class="sxs-lookup"><span data-stu-id="2d8f8-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="2d8f8-199">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="2d8f8-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





