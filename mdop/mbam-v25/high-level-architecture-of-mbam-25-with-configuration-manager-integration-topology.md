---
title: Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager
description: Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825765"
---
# <span data-ttu-id="8b2f4-103">Architettura di alto livello di MBAM 2,5 con la topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="8b2f4-104">Questo argomento descrive l'architettura consigliata per la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="8b2f4-105">Questa topologia si integra con MBAM con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="8b2f4-106">Per distribuire MBAM con la topologia autonoma, vedere [architettura di alto livello di MBAM 2,5 con topologia](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autonoma.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="8b2f4-107">Per un elenco delle versioni supportate del software menzionato in questo argomento, Vedi le [configurazioni supportate di MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="8b2f4-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="8b2f4-108">**Importante**  Windows to go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si usa Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="8b2f4-109">Numero consigliato di server e numero di client supportati</span><span class="sxs-lookup"><span data-stu-id="8b2f4-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="8b2f4-110">Il numero consigliato di server e il numero di client supportati in un ambiente di produzione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b2f4-111">Architettura consigliata</span><span class="sxs-lookup"><span data-stu-id="8b2f4-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="8b2f4-112">Dettagli</span><span class="sxs-lookup"><span data-stu-id="8b2f4-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b2f4-113">Numero di server e altri computer</span><span class="sxs-lookup"><span data-stu-id="8b2f4-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-114">Tre server</span><span class="sxs-lookup"><span data-stu-id="8b2f4-114">Three servers</span></span></p>
<p><span data-ttu-id="8b2f4-115">Una workstation</span><span class="sxs-lookup"><span data-stu-id="8b2f4-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b2f4-116">Numero di computer client supportati</span><span class="sxs-lookup"><span data-stu-id="8b2f4-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-117">500.000</span><span class="sxs-lookup"><span data-stu-id="8b2f4-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8b2f4-118">Differenze tra l'integrazione di Configuration Manager e le topologie autonome</span><span class="sxs-lookup"><span data-stu-id="8b2f4-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="8b2f4-119">Le principali differenze tra le topologie sono:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="8b2f4-120">Le funzionalità di conformità e creazione di report vengono rimosse da MBAM e si accede da Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="8b2f4-121">I report vengono visualizzati dalla console di gestione di Configuration Manager, ad eccezione del report di controllo del ripristino, che si continua a visualizzare dal sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="8b2f4-122">Consigliabile MBAM architettura di alto livello con la topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="8b2f4-123">Il diagramma e la tabella seguenti descrivono l'architettura di alto livello consigliata per MBAM con la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="8b2f4-124">Le distribuzioni di MBAM multi-Forest richiedono un trust unidirezionale o bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="8b2f4-125">I trust unidirezionali richiedono che il dominio del server si fidi del dominio client.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="8b2f4-127">Server di database</span><span class="sxs-lookup"><span data-stu-id="8b2f4-127">Database server</span></span>

#### <span data-ttu-id="8b2f4-128">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="8b2f4-128">Recovery database</span></span>

<span data-ttu-id="8b2f4-129">Questa funzionalità è configurata in un computer con Windows Server e in un'istanza di SQL Server supportata.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="8b2f4-130">Il **database di ripristino** archivia i dati di recupero raccolti dai computer client di mbam.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="8b2f4-131">Database di controllo</span><span class="sxs-lookup"><span data-stu-id="8b2f4-131">Audit database</span></span>

<span data-ttu-id="8b2f4-132">Questa funzionalità è configurata in un computer con Windows Server e in un'istanza di SQL Server supportata.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="8b2f4-133">Il **database di controllo** archivia i dati delle attività di controllo raccolti da computer client che hanno eseguito l'accesso ai dati di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="8b2f4-134">Rapporti</span><span class="sxs-lookup"><span data-stu-id="8b2f4-134">Reports</span></span>

<span data-ttu-id="8b2f4-135">Questa funzionalità è configurata in un computer con Windows Server e in un'istanza di SQL Server supportata.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="8b2f4-136">I **report** includono dati di controllo del ripristino per i computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="8b2f4-137">È possibile visualizzare i report dalla console di Configuration Manager o direttamente da SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="8b2f4-138">Server del sito primario di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="8b2f4-139">Funzionalità di integrazione di System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="8b2f4-140">Questa caratteristica è configurata nel server del sito primario di Configuration Manager, che è il server di livello superiore nell'infrastruttura di gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="8b2f4-141">Il **Server Configuration Manager** raccoglie le informazioni sull'inventario hardware dai computer client e viene usato per segnalare la conformità di BitLocker dei computer client.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="8b2f4-142">Quando si esegue la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker per installare il software server, la raccolta di computer supportati MBAM, la previsione di configurazione e i report vengono configurati nel server del sito primario di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="8b2f4-143">La **console di Configuration Manager** deve essere installata nello stesso computer in cui si installa il software del server mbam.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="8b2f4-144">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="8b2f4-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="8b2f4-145">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="8b2f4-145">Administration and monitoring website</span></span>

<span data-ttu-id="8b2f4-146">Questa caratteristica è configurata in un computer che gestisce Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="8b2f4-147">Il **sito Web di amministrazione e monitoraggio** viene usato per:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="8b2f4-148">Aiutare gli utenti finali a recuperare l'accesso ai propri computer quando sono bloccati. (L'area del sito Web viene comunemente chiamata Help desk).</span><span class="sxs-lookup"><span data-stu-id="8b2f4-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="8b2f4-149">Visualizzare il report di controllo del ripristino, che mostra l'attività di ripristino per i computer client.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="8b2f4-150">Altri report vengono visualizzati dalla console di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="8b2f4-151">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="8b2f4-151">Self-service portal</span></span>

<span data-ttu-id="8b2f4-152">Questa caratteristica è configurata in un computer che gestisce Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="8b2f4-153">Il **portale self-service** è un sito Web che consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="8b2f4-154">Monitoraggio dei servizi Web per questo sito Web</span><span class="sxs-lookup"><span data-stu-id="8b2f4-154">Monitoring web services for this website</span></span>

<span data-ttu-id="8b2f4-155">Questa funzionalità è installata in un computer che gestisce Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="8b2f4-156">I **servizi Web di monitoraggio** vengono usati dal client mbam e dai siti Web per comunicare con il database.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="8b2f4-157">Importante</span><span class="sxs-lookup"><span data-stu-id="8b2f4-157">Important</span></span>**<br><span data-ttu-id="8b2f4-158">Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 dato che i siti Web di MBAM comunicano direttamente con il database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="8b2f4-159">Workstation di gestione</span><span class="sxs-lookup"><span data-stu-id="8b2f4-159">Management workstation</span></span>

#### <span data-ttu-id="8b2f4-160">Modelli di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="8b2f4-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="8b2f4-161">I **modelli dei criteri di gruppo di mbam** sono impostazioni di criteri di gruppo che definiscono le impostazioni di implementazione per mbam, che consentono di gestire la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="8b2f4-162">Prima di eseguire MBAM, è necessario scaricare i modelli di criteri di gruppo da [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation che esegue un sistema operativo Windows Server o Windows supportato.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="8b2f4-163">NOTA</span><span class="sxs-lookup"><span data-stu-id="8b2f4-163">NOTE</span></span>**<br><span data-ttu-id="8b2f4-164">La workstation non deve essere un computer dedicato.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="8b2f4-165">Client MBAM e computer client di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="8b2f4-166">Software client MBAM</span><span class="sxs-lookup"><span data-stu-id="8b2f4-166">MBAM Client software</span></span>

<span data-ttu-id="8b2f4-167">Il **client mbam**:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="8b2f4-168">USA gli oggetti Criteri di gruppo per applicare la crittografia unità BitLocker nei computer client dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="8b2f4-169">Raccoglie la chiave di ripristino di BitLocker per tre tipi di unità dati: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).</span><span class="sxs-lookup"><span data-stu-id="8b2f4-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="8b2f4-170">Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="8b2f4-171">Client di Gestione configurazione</span><span class="sxs-lookup"><span data-stu-id="8b2f4-171">Configuration Manager Client</span></span>

<span data-ttu-id="8b2f4-172">Il **client Configuration Manager** consente a Gestione configurazione di raccogliere i dati di compatibilità hardware relativi ai computer client e di segnalare le informazioni sulla conformità.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="8b2f4-173">Differenze nella distribuzione di MBAM per le versioni supportate di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="8b2f4-174">Quando si distribuisce MBAM con la topologia di integrazione di Configuration Manager, è possibile installare MBAM in un server del sito principale.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="8b2f4-175">Tuttavia, l'installazione di MBAM funziona in modo diverso per System Center2012 Configuration Manager e Configuration Manager2007.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b2f4-176">Versione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="8b2f4-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b2f4-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b2f4-178">System Center2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="8b2f4-179">Gestione configurazione di sistema Center2012</span><span class="sxs-lookup"><span data-stu-id="8b2f4-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-180">Se si installa MBAM in un server del sito principale o in un server di amministrazione centrale, MBAM esegue tutte le operazioni di installazione nel server del sito.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b2f4-181">Configurazione Manager2007 R2</span><span class="sxs-lookup"><span data-stu-id="8b2f4-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="8b2f4-182">Configurazione Manager2007</span><span class="sxs-lookup"><span data-stu-id="8b2f4-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-183">Se si installa MBAM in un server del sito principale che fa parte di una gerarchia di gestione configurazione più grande con un server padre del sito centrale, MBAM identifica il server padre del sito centrale ed esegue tutte le azioni di installazione nel server padre.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="8b2f4-184">L'installazione include il controllo dei prerequisiti e l'installazione di oggetti e report di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="8b2f4-185">Ad esempio, se si installa MBAM in un server del sito principale che è un elemento figlio di un server padre del sito centrale, MBAM installa tutti gli oggetti e i report di Configuration Manager nel server padre.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="8b2f4-186">Se si installa MBAM nel server padre, MBAM esegue tutte le operazioni di installazione in tale server padre.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8b2f4-187">Funzionamento di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="8b2f4-188">L'integrazione di MBAM con Configuration Manager si basa su un pacchetto di configurazione che installa gli elementi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b2f4-189">Elementi installati in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8b2f4-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="8b2f4-190">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b2f4-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b2f4-191">Dati di configurazione</span><span class="sxs-lookup"><span data-stu-id="8b2f4-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-192">I dati di configurazione installano una previsione di configurazione, denominata "protezione BitLocker", che contiene due elementi di configurazione:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="8b2f4-193">Protezione unità sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="8b2f4-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="8b2f4-194">Protezione delle unità dati fisse di BitLocker</span><span class="sxs-lookup"><span data-stu-id="8b2f4-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="8b2f4-195">La linea di base della configurazione viene distribuita nella raccolta di computer supportati MBAM, che viene creata anche quando MBAM è installato.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="8b2f4-196">I due elementi di configurazione costituiscono la base per valutare lo stato di conformità dei computer client.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="8b2f4-197">Queste informazioni vengono acquisite, archiviate e valutate in Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="8b2f4-198">Gli elementi di configurazione si basano sui requisiti di conformità per le unità del sistema operativo e le unità dati fisse.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="8b2f4-199">I dettagli necessari per i computer distribuiti vengono raccolti in modo da poter valutare la conformità per tali tipi di unità.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="8b2f4-200">Per impostazione predefinita, la linea di base della configurazione valuta lo stato di conformità every12 ore e invia i dati di conformità a Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b2f4-201">Raccolta di computer supportati MBAM</span><span class="sxs-lookup"><span data-stu-id="8b2f4-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-202">MBAM crea una raccolta che si chiama MBAM computer supportati.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="8b2f4-203">La linea di base della configurazione è destinata ai computer client inclusi in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="8b2f4-204">Si tratta di una raccolta dinamica.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-204">This is a dynamic collection.</span></span> <span data-ttu-id="8b2f4-205">Per impostazione predefinita, esegue every12 ore e valuta l'appartenenza, in base a tre criteri:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="8b2f4-206">Il computer è una versione supportata del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="8b2f4-207">Il computer è un computer fisico.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-207">The computer is a physical computer.</span></span> <span data-ttu-id="8b2f4-208">Le macchine virtuali non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="8b2f4-209">Il computer ha un modulo TPM (Trusted Platform Module) disponibile.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="8b2f4-210">Per Windows7 è necessaria una versione compatibile del TPM 1.2 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="8b2f4-211">Windows10, Windows 8.1, Windows8 e Windows to go non richiedono un TPM.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="8b2f4-212">La raccolta viene valutata in tutti i computer e viene creato un sottoinsieme di computer compatibili, che fornisce la base per la valutazione della conformità e la creazione di report per l'integrazione con MBAM.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b2f4-213">Rapporti</span><span class="sxs-lookup"><span data-stu-id="8b2f4-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-214">Quando si configura MBAM con la topologia di integrazione di Configuration Manager, è possibile visualizzare tutti i report di Configuration Manager, eccetto il report di controllo di ripristino, il secondo dei quali si continua a visualizzare nel sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="8b2f4-215">I report disponibili in Gestione configurazione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b2f4-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b2f4-216">Rapporto</span><span class="sxs-lookup"><span data-stu-id="8b2f4-216">Report</span></span></th>
<th align="left"><span data-ttu-id="8b2f4-217">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b2f4-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b2f4-218">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8b2f4-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-219">Assegna agli amministratori IT tre visualizzazioni delle informazioni in un singolo report: distribuzione dello stato di conformità, distribuzione degli errori non conforme e distribuzione dello stato di conformità per tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="8b2f4-220">Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b2f4-221">Dettagli di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8b2f4-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-222">Consente agli amministratori IT di visualizzare informazioni sullo stato di conformità della crittografia BitLocker dell'organizzazione e include lo stato di conformità per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="8b2f4-223">Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b2f4-224">Conformità al computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="8b2f4-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-225">Consente agli amministratori IT di visualizzare un singolo computer e determinare il motivo per cui è stato segnalato con uno stato conforme o non conforme.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="8b2f4-226">Il report visualizza anche lo stato di crittografia delle unità del sistema operativo e delle unità dati fisse.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b2f4-227">Riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8b2f4-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b2f4-228">Consente agli amministratori IT di visualizzare lo stato della conformità ai criteri di MBAM nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="8b2f4-229">Lo stato di ogni computer viene valutato e il report Mostra un riepilogo della conformità di tutti i computer dell'organizzazione rispetto al criterio.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="8b2f4-230">Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="8b2f4-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="8b2f4-231">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b2f4-231">Related topics</span></span>


[<span data-ttu-id="8b2f4-232">Attività iniziali di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8b2f4-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="8b2f4-233">Architettura di alto livello di MBAM 2.5 con topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="8b2f4-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="8b2f4-234">Funzionalità illustrate di una distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8b2f4-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="8b2f4-235">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="8b2f4-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8b2f4-236">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8b2f4-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8b2f4-237">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8b2f4-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




