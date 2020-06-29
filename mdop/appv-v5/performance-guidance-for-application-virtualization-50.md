---
title: Linee guida sulle prestazioni di Application Virtualization 5.0
description: Linee guida sulle prestazioni di Application Virtualization 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805050"
---
# <span data-ttu-id="7b4e2-103">Linee guida sulle prestazioni di Application Virtualization 5.0</span><span class="sxs-lookup"><span data-stu-id="7b4e2-103">Performance Guidance for Application Virtualization 5.0</span></span>


<span data-ttu-id="7b4e2-104">Scopri come configurare App-V 5,0 per ottenere prestazioni ottimali, ottimizzare i pacchetti di app virtuali e migliorare l'esperienza utente con RDS e VDI.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-104">Learn how to configure App-V 5.0 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="7b4e2-105">L'implementazione di più metodi può aiutare a migliorare l'esperienza dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="7b4e2-106">Tuttavia, l'ambiente potrebbe non supportare tutti i metodi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="7b4e2-107">Prima di leggere il documento, leggere e comprendere le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="7b4e2-108">Guida dell'amministratore di Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="7b4e2-108">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="7b4e2-109">Pubblicazione di applicazioni App-V 5 SP2 e interazione client</span><span class="sxs-lookup"><span data-stu-id="7b4e2-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="7b4e2-110">Guida alla sequenziazione di Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="7b4e2-110">Microsoft Application Virtualization 5.0 Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="7b4e2-111">Nota</span><span class="sxs-lookup"><span data-stu-id="7b4e2-111">Note</span></span>**  
<span data-ttu-id="7b4e2-112">Alcuni termini usati in questo documento possono avere significati diversi a seconda dell'origine esterna e del contesto.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="7b4e2-113">Per altre informazioni sui termini usati in questo documento seguiti da un asterisco **\\** \*, vedere la sezione [terminologia dell'applicazione per la virtualizzazione delle prestazioni](#bkmk-terms1) di questo documento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="7b4e2-114">Infine, questo documento ti fornirà le informazioni per configurare il computer che gestisce il client App-V 5,0 e l'ambiente per ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-114">Finally, this document will provide you with the information to configure the computer running App-V 5.0 client and the environment for optimal performance.</span></span> <span data-ttu-id="7b4e2-115">Ottimizza i pacchetti di applicazioni virtuali per le prestazioni usando il sequencer e per capire come usare la virtualizzazione dell'esperienza utente (UE-V) o altre tecnologie di gestione dell'ambiente utente per ottenere un'esperienza utente ottimale con App-V 5,0 sia in Servizi Desktop remoto che in infrastrutture desktop virtuali non permanenti (VDI).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.0 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="7b4e2-116">Per determinare quali informazioni sono rilevanti per l'ambiente, è necessario rivedere la breve panoramica di ogni sezione e l'elenco di controllo dell'applicabilità.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="7b4e2-117">App-V 5,0 in stato \ \* distribuzioni non persistenti</span><span class="sxs-lookup"><span data-stu-id="7b4e2-117">App-V 5.0 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="7b4e2-118">In questa sezione vengono fornite informazioni su un approccio che consente di garantire che un utente possa accedere a tutte le applicazioni virtuali in pochi secondi dopo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="7b4e2-119">Questa operazione viene eseguita per affrontare in modo univoco l'aggiornamento della pubblicazione di App V 5,0 spesso a lunga durata.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-119">This is achieved by uniquely addressing the often long-running App-V 5.0 publishing refresh.</span></span> <span data-ttu-id="7b4e2-120">Man mano che si scoprirà la base dell'approccio, l'aggiornamento della pubblicazione più veloce è uno che non deve effettivamente eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="7b4e2-121">È necessario rispettare una serie di condizioni e seguire i passaggi per ottenere un'esperienza utente ottimale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="7b4e2-122">Per altre informazioni, usare le informazioni nella sezione seguente:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="7b4e2-123">[Scenari di utilizzo](#bkmk-us) : durante la revisione dei due scenari, tieni presente che questi sono gli estremi di approccio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="7b4e2-124">In base ai requisiti di utilizzo, è possibile scegliere di applicare questi passaggi a un sottoinsieme di utenti e/o pacchetti di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="7b4e2-125">Ottimizzato per le prestazioni: per offrire un'esperienza ottimale, è possibile prevedere che l'immagine di base includa parte del pacchetto di applicazione virtuale App-V.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="7b4e2-126">Questo e altri requisiti vengono discussi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="7b4e2-127">Ottimizzato per lo spazio di archiviazione: se si è interessati all'impatto dello spazio di archiviazione, seguire questo scenario consentirà di risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="7b4e2-128">Preparazione dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="7b4e2-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="7b4e2-129">Procedura per preparare l'immagine di base: in un ambiente VDI o RDSH non persistente, è necessario completare solo pochi passaggi nell'immagine di base per abilitare questo approccio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="7b4e2-130">USA UE-V 2,0 come soluzione di gestione dei profili utente (UPM) per l'approccio App-V-la pietra angolare di questo approccio è la capacità di una soluzione UEM di rendere persistente il contenuto di pochi percorsi di registro e file.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-130">Use UE-V 2.0 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="7b4e2-131">Queste posizioni costituiscono le integrazioni degli utenti \ \*.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="7b4e2-132">Assicurarsi di esaminare i requisiti specifici per la soluzione UPM.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="7b4e2-133">Esperienza utente walk-through</span><span class="sxs-lookup"><span data-stu-id="7b4e2-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="7b4e2-134">Walk-through: si tratta di una procedura dettagliata per le operazioni di App-V e UE-V e per le aspettative che gli utenti devono avere.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="7b4e2-135">Risultato: descrive i risultati previsti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="7b4e2-136">Impatto sul ciclo di vita del pacchetto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="7b4e2-137">Migliorare l'esperienza VDI attraverso ottimizzazione delle prestazioni/ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="7b4e2-138">Elenco di controllo applicabilità</span><span class="sxs-lookup"><span data-stu-id="7b4e2-138">Applicability Checklist</span></span>

<span data-ttu-id="7b4e2-139">Ambiente di distribuzione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7b4e2-140">VDI o RDSH non persistente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7b4e2-141">Virtualizzazione dell'esperienza utente (UE-V), altre soluzioni UPM o disk del profilo utente (UPD).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7b4e2-142">Configurazione prevista</span><span class="sxs-lookup"><span data-stu-id="7b4e2-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7b4e2-143">User Experience Virtualization (UE-V) con il modello di stato utente App-V abilitato o con il software UPM (User Profile Management).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="7b4e2-144">Il software UPM non UE-V deve essere in grado di attivare l'accesso o l'inizio e la disconnessione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7b4e2-145">App-V Shared Content Store (SCS) è configurato o può essere configurato.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7b4e2-146">Amministrazione IT</span><span class="sxs-lookup"><span data-stu-id="7b4e2-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="7b4e2-147">L'amministratore potrebbe dover aggiornare regolarmente l'immagine di base di VM per garantire prestazioni ottimali o l'amministratore potrebbe dover gestire più immagini per gruppi di utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="7b4e2-148">Scenario di utilizzo</span><span class="sxs-lookup"><span data-stu-id="7b4e2-148">Usage Scenario</span></span>

<span data-ttu-id="7b4e2-149">Mentre esaminiamo i due scenari, tieni presente che questi approcci si avvicinano agli estremi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="7b4e2-150">In base ai requisiti di utilizzo, è possibile scegliere di applicare questi passaggi a un sottoinsieme di utenti, pacchetti di applicazioni virtuali o entrambi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-151">Ottimizzato per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-152">Ottimizzato per lo spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-153">Per offrire un'esperienza utente ottimale, questo approccio sfrutta le funzionalità di una soluzione UPM e richiede ulteriore preparazione delle immagini e può incorrere in un sovraccarico di gestione delle immagini aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="7b4e2-154">Di seguito vengono illustrati molti miglioramenti delle prestazioni nelle distribuzioni non permanenti con stato.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="7b4e2-155">Per altre informazioni, vedere la <strong> procedura di sequenziazione per ottimizzare i pacchetti per la pubblicazione delle prestazioni </strong> e il riferimento alla <strong> Guida alla sequenziazione di App-V 5,0 </strong> nella <strong> sezione vedere anche di questo documento </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V 5.0 Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-156">Le aspettative generali dello scenario precedente si applicano ancora qui.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="7b4e2-157">Tuttavia, tieni presente che le immagini VM sono in genere archiviate in matrici molto costose; è stata apportata una lieve modifica all'approccio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="7b4e2-158">Non preconfigurare pacchetti di applicazioni virtuali mirati dall'utente nell'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="7b4e2-159">L'impatto di questa alterazione è dettagliato nella sezione relativa all'esperienza utente di questo documento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="7b4e2-160">Preparazione dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="7b4e2-160">Preparing your Environment</span></span>

<span data-ttu-id="7b4e2-161">Nella tabella seguente vengono illustrati i passaggi necessari per preparare l'immagine di base e l'UE-V o un'altra soluzione UPM per l'approccio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="7b4e2-162">Preparare l'immagine di base</span><span class="sxs-lookup"><span data-stu-id="7b4e2-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-163">Ottimizzato per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-164">Ottimizzato per lo spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7b4e2-165">Installare il pacchetto hotfix 4 per la versione client Application Virtualization 5,0 SP2 del client.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-165">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-166">Installare UE-V e scaricare il modello di impostazioni app-V dalla raccolta modelli UE-V, vedere i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-167">Configurare la modalità SCS (Shared Content Store).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="7b4e2-168">Per altre informazioni <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> , vedere come installare il client App-V 5,0 per la modalità di archiviazione del contenuto condiviso </a> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-168">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-169">Configurare Mantieni le integrazioni degli utenti nel DWORD del registro di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-170">Preconfigurare tutti i pacchetti con destinazione globale e utente, ad esempio <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-171">Preconfigurare tutti i gruppi di connessioni mirati dall'utente e globale, ad esempio <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-172">Pre-pubblicare tutti i pacchetti di destinazione globale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="7b4e2-173">Alternativamente</span><span class="sxs-lookup"><span data-stu-id="7b4e2-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-174">Eseguire una pubblicazione/aggiornamento globale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-175">Eseguire una pubblicazione/aggiornamento degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-176">Annullare la pubblicazione di tutti i pacchetti mirati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-177">Eliminare le voci VFS (User-Virtual File System) seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7b4e2-178">Installare il pacchetto hotfix 4 per la versione client Application Virtualization 5,0 SP2 del client.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-178">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-179">Installare UE-V e scaricare il modello di impostazioni app-V dalla raccolta modelli UE-V, vedere i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-180">Configurare la modalità SCS (Shared Content Store).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="7b4e2-181">Per altre informazioni <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> , vedere come installare il client App-V 5,0 per la modalità di archiviazione del contenuto condiviso </a> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-181">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-182">Configurare Mantieni le integrazioni degli utenti nel DWORD del registro di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-183">Preconfigura tutti i pacchetti di destinazione globale, ad esempio <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-184">Preconfigurare tutti i gruppi di connessioni con destinazione globale, ad esempio <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-185">Pre-pubblicare tutti i pacchetti di destinazione globale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7b4e2-186">**Configurazioni** -per le configurazioni client App-V critiche e per un po' più di contesto e procedure, esaminare le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-187">Impostazione di configurazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-188">Che cosa fa questo?</span><span class="sxs-lookup"><span data-stu-id="7b4e2-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-189">Come si usa?</span><span class="sxs-lookup"><span data-stu-id="7b4e2-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-190">Modalità SCS (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-191">Configurabile in PowerShell tramite <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> oppure</span><span class="sxs-lookup"><span data-stu-id="7b4e2-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-192">Durante l'installazione del client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-192">During installation of the App-V 5.0 client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7b4e2-193">Quando si esegua l'archiviazione del contenuto condiviso, solo i dati vengono mantenuti nel disco rigido; altri asset delle applicazioni virtuali vengono mantenuti in memoria (RAM).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="7b4e2-194">In questo modo è possibile risparmiare spazio di archiviazione locale e ridurre a icona I/O del disco al secondo (IOPS).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-195">Questa operazione è consigliata quando sono disponibili connessioni a bassa latenza tra l'endpoint client App-V e il server del contenuto SCS, SAN.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b4e2-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="7b4e2-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-197">Configurare il registro di sistema in <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> software </strong>  \  <strong> Microsoft </strong>  \  <strong> appv </strong>  \  <strong> client </strong>  \  <strong> Integration </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-198">Creare il valore DWORD <strong> PreserveUserIntegrationsOnLogin </strong> con un valore pari a <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-199">Riavviare il servizio client App-V o riavviare il computer in cui è in uso il client App-V.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7b4e2-200">Se non è già stato configurato ( <strong> Add-AppvClientPackage </strong> ) un pacchetto specifico e questa impostazione non è configurata, il client App-V disintegrerà \* le integrazioni permanenti degli utenti e quindi reintegrerà \*.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="7b4e2-201">Per ogni pacchetto che soddisfa le condizioni precedenti, il lavoro verrà eseguito due volte durante la pubblicazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-202">Se non si prevede di pre-configurare ogni pacchetto utente disponibile nell'immagine di base, usare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="7b4e2-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-204">Configurare il registro di sistema in <strong> HKEY_LOCAL_MACHINE </strong> &lt; &gt; software </strong>  \  <strong> Microsoft </strong>  \  <strong> appv Strong </strong> &lt; &gt; client </strong>  \  <strong> Publishing </strong> .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-205">Crea il valore DWORD <strong> MaxConcurrentPublishingrefresh </strong> con il numero massimo desiderato di aggiornamenti per la pubblicazione simultanea.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-206">Il servizio client App-V e il computer non devono essere riavviati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7b4e2-207">Questa impostazione determina il numero di utenti che possono eseguire una sincronizzazione/aggiornamento della pubblicazione simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="7b4e2-208">L'impostazione predefinita non è limite.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-209">Se si limita il numero di aggiornamenti simultanei della pubblicazione, viene impedito un uso eccessivo della CPU che potrebbe influire sulle prestazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="7b4e2-210">Questo limite è consigliato in un ambiente RDS, in cui più utenti possono accedere allo stesso computer contemporaneamente ed eseguire una sincronizzazione di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="7b4e2-211">Se viene raggiunta la soglia di aggiornamento della pubblicazione simultanea, il tempo necessario per pubblicare le nuove applicazioni e renderle disponibili per gli utenti finali dopo l'accesso potrebbe richiedere un periodo di tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7b4e2-212">Configurare la soluzione UE-V per l'approccio App-V</span><span class="sxs-lookup"><span data-stu-id="7b4e2-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="7b4e2-213">Ti consigliamo di usare Microsoft User Experience Virtualization (UE-V) per acquisire e centralizzare le impostazioni delle applicazioni e le impostazioni del sistema operativo Windows per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="7b4e2-214">Queste impostazioni vengono quindi applicate ai diversi computer a cui si accede dall'utente, inclusi i computer desktop, i computer portatili e le sessioni VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="7b4e2-215">UE-V è ottimizzato per gli scenari RDS e VDI.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="7b4e2-216">Per altre informazioni, vedere [Introduzione alla virtualizzazione dell'esperienza utente 2,0](https://technet.microsoft.com/library/dn458936.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458936.aspx)</span></span>

<span data-ttu-id="7b4e2-217">In sostanza, tutto ciò che è necessario è installare il client UE-V e scaricare il modello di impostazioni di App-V di Microsoft authored seguente dalla [raccolta di modelli Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="7b4e2-218">Registrare il modello.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-218">Register the template.</span></span> <span data-ttu-id="7b4e2-219">Per altre informazioni sui modelli UE-V, vedere [la risorsa specifica UE-v per l'acquisizione e la registrazione del modello](https://technet.microsoft.com/library/dn458936.aspx).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458936.aspx).</span></span>

**<span data-ttu-id="7b4e2-220">Nota</span><span class="sxs-lookup"><span data-stu-id="7b4e2-220">Note</span></span>**  
<span data-ttu-id="7b4e2-221">Senza eseguire un ulteriore passaggio di configurazione, Microsoft User Environment Virtualization (UE-V) non sarà in grado di sincronizzare i tasti di scelta rapida del menu Start (file lnk) nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="7b4e2-222">Il tipo di file lnk è escluso per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="7b4e2-223">UE-V supporta solo la rimozione del tipo di file lnk dall'elenco di esclusione negli scenari RDS e VDI, in cui ogni dispositivo dell'utente avrà lo stesso set di applicazioni installato nella stessa posizione e ogni file lnk è valido per tutti i dispositivi degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="7b4e2-224">Ad esempio, UE-V non supporta attualmente i due scenari seguenti, perché il risultato netto sarà che il collegamento sarà valido in uno ma non in tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="7b4e2-225">Se un utente ha un'applicazione installata in un dispositivo con i file lnk abilitati e la stessa applicazione nativa installata in un altro dispositivo a una radice di installazione diversa con i file lnk abilitati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="7b4e2-226">Se un utente ha un'applicazione installata in un dispositivo ma non in un altro con i file lnk abilitati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="7b4e2-227">Importante</span><span class="sxs-lookup"><span data-stu-id="7b4e2-227">Important</span></span>**  
<span data-ttu-id="7b4e2-228">Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="7b4e2-229">Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="7b4e2-230">Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="7b4e2-231">Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="7b4e2-232">Cambiare il registro di sistema a proprio rischio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="7b4e2-233">Con l'editor del registro di sistema Microsoft (regedit.exe), passare a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** e Remove **. lnk** dai tipi di file esclusi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="7b4e2-234">Configurare un'altra soluzione UPM (User Profile Management) per l'approccio App-V</span><span class="sxs-lookup"><span data-stu-id="7b4e2-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="7b4e2-235">L'aspettativa in un ambiente con stato è che una soluzione UPM è implementata e può supportare la persistenza dei dati degli utenti tra le sessioni e tra gli account di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="7b4e2-236">I requisiti per la soluzione UPM sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="7b4e2-237">Per abilitare un'esperienza di accesso ottimizzata, ad esempio l'approccio App-V 5,0 per l'utente, la soluzione deve essere in grado di:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-237">To enable an optimized login experience, for example the App-V 5.0 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="7b4e2-238">Rendere persistenti le integrazioni seguenti degli utenti nell'ambito del profilo utente/persona.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="7b4e2-239">Attivazione di una sincronizzazione del profilo utente per l'accesso (o l'avvio dell'applicazione), che può garantire che tutte le integrazioni degli utenti vengano applicate prima dell'inizio della pubblicazione/aggiornamento o,</span><span class="sxs-lookup"><span data-stu-id="7b4e2-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="7b4e2-240">Allegare e scollegare un disco di profilo utente (UPD) o una tecnologia simile che contiene le integrazioni degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

-   <span data-ttu-id="7b4e2-241">Acquisizione delle modifiche apportate alle posizioni, che costituiscono le integrazioni degli utenti, prima della disconnessione della sessione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-241">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="7b4e2-242">Con App-V 5,0 quando si aggiunge un server di pubblicazione (**Add-AppvPublishingServer**) è possibile configurare la sincronizzazione, ad esempio aggiorna durante l'accesso e/o dopo un intervallo di aggiornamento specificato.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-242">With App-V 5.0 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="7b4e2-243">In entrambi i casi viene creata un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-243">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="7b4e2-244">Nelle versioni precedenti di App-V 5,0 sono state configurate entrambe le attività pianificate usando un VBScript che avviava l'utente e l'aggiornamento globale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-244">In previous versions of App-V 5.0, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="7b4e2-245">Con il pacchetto hotfix 4 per Application Virtualization 5,0 SP2 l'aggiornamento dell'utente in accesso viene avviato da **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-245">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on is initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="7b4e2-246">Questa modifica è stata introdotta per dare alle soluzioni UPM un processo di trigger.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-246">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="7b4e2-247">Questo processo ritarderà la pubblicazione di/Refresh per consentire alla soluzione UPM di applicare le integrazioni degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-247">This process will delay the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="7b4e2-248">Verrà chiusa una volta completata la pubblicazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-248">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="7b4e2-249">Integrazioni degli utenti</span><span class="sxs-lookup"><span data-stu-id="7b4e2-249">User Integrations</span></span>**

<span data-ttu-id="7b4e2-250">Registro di sistema-HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="7b4e2-250">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="7b4e2-251">Path-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="7b4e2-251">Path - Software\\Classes</span></span>

    <span data-ttu-id="7b4e2-252">Exclude: impostazioni locali, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="7b4e2-252">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="7b4e2-253">Path-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="7b4e2-253">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="7b4e2-254">Path-percorsi Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="7b4e2-254">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="7b4e2-255">Percorsi di file</span><span class="sxs-lookup"><span data-stu-id="7b4e2-255">File Locations</span></span>**

-   <span data-ttu-id="7b4e2-256">Radice-"variabile di ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="7b4e2-256">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="7b4e2-257">Path-Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="7b4e2-257">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="7b4e2-258">Radice-"variabile di ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="7b4e2-258">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="7b4e2-259">Path-Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="7b4e2-259">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="7b4e2-260">Radice-"variabile di ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="7b4e2-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="7b4e2-261">Path-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="7b4e2-261">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="7b4e2-262">(Per rendere persistenti tutti i collegamenti desktop, virtuali e non virtuali)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-262">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="7b4e2-263">Radice-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="7b4e2-263">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="7b4e2-264">Virtualizzazione di Microsoft User Experience (UE-V)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-264">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="7b4e2-265">Inoltre, ti consigliamo di usare Microsoft User Experience Virtualization (UE-V) per acquisire e centralizzare le impostazioni delle applicazioni e le impostazioni del sistema operativo Windows per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-265">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="7b4e2-266">Queste impostazioni vengono quindi applicate ai diversi computer a cui si accede dall'utente, inclusi i computer desktop, i computer portatili e le sessioni VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-266">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="7b4e2-267">Per altre informazioni, vedere [Introduzione a User Experience Virtualization 1,0](https://technet.microsoft.com/library/jj680015.aspx) e [modelli di posizione di condivisione delle impostazioni con la raccolta di modelli UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-267">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="7b4e2-268">Esperienza utente walk-through</span><span class="sxs-lookup"><span data-stu-id="7b4e2-268">User Experience Walk-through</span></span>

<span data-ttu-id="7b4e2-269">Di seguito è riportata una procedura dettagliata delle operazioni di App-V e UPM e le aspettative che gli utenti dovrebbero aspettarsi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-269">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-270">Ottimizzato per le prestazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-270">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-271">Ottimizzato per lo spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-271">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-272">Dopo aver implementato questo approccio nell'ambiente VDI/RDSH, al primo accesso</span><span class="sxs-lookup"><span data-stu-id="7b4e2-272">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-273">Operazione Viene avviata la pubblicazione/aggiornamento degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-273">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="7b4e2-274">Presupposto Se è la prima volta che un utente ha pubblicato applicazioni virtuali (ad esempio non persistenti), la durata consueta di una pubblicazione/aggiornamento sarà la solita.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-274">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-275">Operazione Dopo la pubblicazione/aggiornamento, la soluzione UPM acquisisce le integrazioni degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-275">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="7b4e2-276">Presupposto A seconda di come è configurata la soluzione UPM, questa operazione può essere eseguita durante il processo di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-276">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="7b4e2-277">Questo comporterà lo stesso overhead/simile a quello di persistenza dello stato utente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-277">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="7b4e2-278">Sugli accessi successivi:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-278">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-279">Operazione La soluzione UPM applica le integrazioni degli utenti al sistema prima della pubblicazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-279">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="7b4e2-280">Presupposto Sul desktop saranno presenti tasti di scelta rapida, oppure nel menu Start, che funzionano immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-280">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="7b4e2-281">Quando il completamento della pubblicazione/aggiornamento (ad esempio, i diritti del pacchetto cambiano), alcuni potrebbero andarsene.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-281">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-282">Operazione La pubblicazione/aggiornamento elaborerà le operazioni di annullamento della pubblicazione e pubblicazione per le modifiche apportate ai pacchetti utente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-282">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="7b4e2-283">Presupposto Se non sono presenti modifiche al diritto, publishing1 verrà completato in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-283">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="7b4e2-284">In caso contrario, la pubblicazione/aggiornamento aumenterà in relazione al numero e alla complessità \* delle applicazioni virtuali</span><span class="sxs-lookup"><span data-stu-id="7b4e2-284">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-285">Operazione La soluzione UPM acquisirà di nuovo le integrazioni degli utenti alla disconnessione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-285">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="7b4e2-286">Presupposto Uguale a precedente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-286">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="7b4e2-287">¹ l'operazione di pubblicazione ( <strong> Publish-AppVClientPackage </strong> ) aggiunge voci al catalogo dell'utente, associa il diritto all'utente, identifica l'archivio locale e termina completando i passaggi di integrazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-287">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-288">Dopo aver implementato questo approccio nell'ambiente VDI/RDSH, al primo accesso</span><span class="sxs-lookup"><span data-stu-id="7b4e2-288">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-289">Operazione Viene avviata la pubblicazione/aggiornamento degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-289">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="7b4e2-290">Presupposto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-290">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-291">Se è la prima volta che un utente ha pubblicato applicazioni virtuali (ad esempio, non persistenti), la durata normale di una pubblicazione/aggiornamento sarà la consueta.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-291">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-292">I primi e gli accessi successivi saranno interessati dalla preconfigurazione dei pacchetti (Aggiungi/Aggiorna).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-292">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="7b4e2-293">Operazione Dopo la pubblicazione/aggiornamento, la soluzione UPM acquisisce le integrazioni degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-293">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="7b4e2-294">Presupposto A seconda di come è configurata la soluzione UPM, questa operazione può essere eseguita durante il processo di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-294">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="7b4e2-295">Questo comporterà lo stesso overhead/simile a quello di persistenza dello stato utente</span><span class="sxs-lookup"><span data-stu-id="7b4e2-295">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="7b4e2-296">Sugli accessi successivi:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-296">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-297">Operazione La soluzione UPM applica le integrazioni degli utenti al sistema prima della pubblicazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-297">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-298">Operazione L'aggiunta/aggiornamento deve preconfigurare tutte le applicazioni di destinazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-298">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="7b4e2-299">Presupposto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-299">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-300">In questo modo è possibile aumentare significativamente la disponibilità dell'applicazione (nell'ordine di 10 secondi).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-300">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-301">In questo modo si aumenta il tempo di aggiornamento della pubblicazione relativo al numero e alla complessità \* delle applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-301">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="7b4e2-302">Operazione La pubblicazione/aggiornamento elaborerà le operazioni di annullamento della pubblicazione e pubblicazione per le modifiche apportate ai diritti del pacchetto utente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-302">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-303">Risultato</span><span class="sxs-lookup"><span data-stu-id="7b4e2-303">Outcome</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-304">Risultato</span><span class="sxs-lookup"><span data-stu-id="7b4e2-304">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7b4e2-305">Dato che le integrazioni degli utenti sono completamente conservate, ad esempio, l'integrazione per la pubblicazione/aggiornamento verrà completata.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-305">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="7b4e2-306">Tutte le applicazioni virtuali saranno disponibili entro pochi secondi dall'accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-306">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-307">La pubblicazione/aggiornamento elaborerà le modifiche apportate agli utenti aventi diritto alle applicazioni virtuali che hanno un impatto sull'esperienza.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-307">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7b4e2-308">Poiché il componente aggiuntivo/aggiornamento deve riconfigurare tutte le applicazioni virtuali nella VM, il tempo di aggiornamento della pubblicazione su ogni account di accesso verrà esteso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-308">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="7b4e2-309">Impatto sul ciclo di vita del pacchetto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-309">Impact to Package Life Cycle</span></span>

<span data-ttu-id="7b4e2-310">L'aggiornamento di un pacchetto è un aspetto cruciale del ciclo di vita del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-310">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="7b4e2-311">Per garantire agli utenti l'accesso ai pacchetti di applicazioni virtuali (pubblicati) o declassati (non pubblicati) appropriati, è consigliabile aggiornare l'immagine di base in modo che corrispondano alle modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-311">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="7b4e2-312">Per capire perché rivedere la sezione seguente:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-312">To understand why review the following section:</span></span>

<span data-ttu-id="7b4e2-313">App-V 5,0 SP2 ha introdotto il concetto di stati in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-313">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="7b4e2-314">In passato,</span><span class="sxs-lookup"><span data-stu-id="7b4e2-314">In the past,</span></span>

-   <span data-ttu-id="7b4e2-315">Se un amministratore ha modificato i diritti o ha creato una nuova versione di un pacchetto (aggiornato) e durante una pubblicazione/aggiornamento il pacchetto è stato usato, l'operazione di annullamento della pubblicazione o di pubblicazione, rispettivamente, non riesce.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-315">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="7b4e2-316">A questo punto, se un pacchetto è in uso, l'operazione verrà sospesa.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-316">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="7b4e2-317">Le operazioni di annullamento della pubblicazione e pubblicazione in sospeso verranno elaborate nel riavvio del servizio o se viene emesso un altro comando pubblica o non pubblica.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-317">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="7b4e2-318">In quest'ultimo caso, se l'applicazione virtuale è in uso in caso contrario, l'applicazione virtuale resterà in uno stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-318">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="7b4e2-319">Per i pacchetti pubblicati a livello globale, è spesso necessario riavviare o riavviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-319">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="7b4e2-320">In un ambiente non persistente è improbabile che le operazioni in sospeso vengano elaborate.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-320">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="7b4e2-321">Le operazioni in sospeso, ad esempio le attività vengono acquisite in **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **appv**  \\  **client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-321">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="7b4e2-322">Anche se questa posizione viene mantenuta dalla soluzione UPM, se non viene applicata all'ambiente prima di eseguire l'accesso, non verrà elaborata.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-322">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="7b4e2-323">Migliorare l'esperienza VDI attraverso l'ottimizzazione delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-323">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="7b4e2-324">La sezione seguente contiene elenchi con informazioni su documentazione e download Microsoft che potrebbero risultare utili per ottimizzare l'ambiente per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-324">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="7b4e2-325">Blog e script di NGEN .NET (altamente consigliato)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-325">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="7b4e2-326">Informazioni sulla tecnologia NGEN</span><span class="sxs-lookup"><span data-stu-id="7b4e2-326">About NGEN technology</span></span>

-   [<span data-ttu-id="7b4e2-327">Come velocizzare l'ottimizzazione NGEN</span><span class="sxs-lookup"><span data-stu-id="7b4e2-327">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="7b4e2-328">Script</span><span class="sxs-lookup"><span data-stu-id="7b4e2-328">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="7b4e2-329">Ruoli di Windows Server e server</span><span class="sxs-lookup"><span data-stu-id="7b4e2-329">Windows Server and Server Roles</span></span>**

<span data-ttu-id="7b4e2-330">Linee guida per l'ottimizzazione delle prestazioni del server</span><span class="sxs-lookup"><span data-stu-id="7b4e2-330">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="7b4e2-331">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7b4e2-331">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="7b4e2-332">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b4e2-332">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="7b4e2-333">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b4e2-333">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="7b4e2-334">Ruoli del server</span><span class="sxs-lookup"><span data-stu-id="7b4e2-334">Server Roles</span></span>**

-   [<span data-ttu-id="7b4e2-335">Host di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-335">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="7b4e2-336">Host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-336">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="7b4e2-337">Pertinenza di IIS: gestione di App-V, pubblicazione, servizi Web per la creazione di report</span><span class="sxs-lookup"><span data-stu-id="7b4e2-337">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="7b4e2-338">Pertinenza del file server (SMB): se usato per l'archiviazione e il recapito del contenuto di App-V in modalità SCS</span><span class="sxs-lookup"><span data-stu-id="7b4e2-338">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="7b4e2-339">Istruzioni per l'ottimizzazione delle prestazioni del client Windows (sistema operativo guest)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-339">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="7b4e2-340">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b4e2-340">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="7b4e2-341">Script di ottimizzazione: (fornito dal supporto Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-341">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="7b4e2-342">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="7b4e2-342">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="7b4e2-343">Script di ottimizzazione: (fornito dal supporto Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-343">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="7b4e2-344">Sequenziazione dei passaggi per ottimizzare i pacchetti per le prestazioni di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-344">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="7b4e2-345">App-V 5,0 e App-V 5,0 SP2 conferiscono un valore significativo alle rispettive versioni.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-345">App-V 5.0 and App-V 5.0 SP2 provide significant value in their respective releases.</span></span> <span data-ttu-id="7b4e2-346">Diverse funzionalità consentono di semplificare nuovi scenari o di attivare nuovi scenari di distribuzione dei clienti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-346">Several features facilitate new scenarios or enabled new customer deployment scenarios.</span></span> <span data-ttu-id="7b4e2-347">Queste caratteristiche seguenti possono influire sulle prestazioni delle operazioni di pubblicazione e avvio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-347">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-348">Passaggio</span><span class="sxs-lookup"><span data-stu-id="7b4e2-348">Step</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-349">Considerazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-349">Consideration</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-350">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b4e2-350">Benefits</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-351">Sui compromessi nella</span><span class="sxs-lookup"><span data-stu-id="7b4e2-351">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-352">Nessun blocco di funzionalità 1 (FB1, noto anche come FB principale)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-352">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-353">Nessun FB1 indica che l'applicazione verrà avviata immediatamente e il flusso di errore (applicazione richiede file, DLL e deve essere abbattuti in rete) durante il lancio. Se sono presenti limitazioni di rete, FB1 sarà:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-353">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="7b4e2-354">Ridurre il numero di errori di flusso e larghezza di banda della rete usati quando si avvia un'applicazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-354">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="7b4e2-355">Posticipa il lancio fino a quando l'intero FB1 non è stato trasmesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-355">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7b4e2-356">Il flusso di errore riduce il tempo di avvio.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-356">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-357">I pacchetti di applicazioni virtuali con FB1 configurati dovranno essere risequenziati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-357">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7b4e2-358">Rimozione di FB1</span><span class="sxs-lookup"><span data-stu-id="7b4e2-358">Removing FB1</span></span>

<span data-ttu-id="7b4e2-359">La rimozione di FB1 non richiede il programma di installazione dell'applicazione originale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-359">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="7b4e2-360">Dopo aver completato i passaggi seguenti, è consigliabile ripristinare il computer in cui è in esecuzione il sequencer in uno snapshot pulito.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-360">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="7b4e2-361">**Interfaccia utente di Sequencer** : crea un nuovo pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-361">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="7b4e2-362">Completare i passaggi di sequenziazione fino a Personalizza- &gt; streaming.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-362">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="7b4e2-363">Durante il passaggio di flusso, non selezionare **ottimizza il pacchetto per la distribuzione su rete lenta o non affidabile**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-363">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="7b4e2-364">Se lo si desidera, passa al **sistema operativo di destinazione**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-364">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="7b4e2-365">Modificare un pacchetto di applicazione virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="7b4e2-365">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="7b4e2-366">Completare i passaggi di sequenziazione fino allo streaming.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-366">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="7b4e2-367">Non selezionare **ottimizza il pacchetto per la distribuzione in una rete lenta o inaffidabile**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-367">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="7b4e2-368">Passa a **Crea pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-368">Move to **Create Package**.</span></span>

<span data-ttu-id="7b4e2-369">**PowerShell** -aggiornare un pacchetto di applicazione virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-369">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="7b4e2-370">Aprire una sessione di PowerShell con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-370">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="7b4e2-371">Import-Module **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-371">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="7b4e2-372">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="7b4e2-372">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="7b4e2-373">"C:\\Packages\\MyPackage.appv"-programma di installazione</span><span class="sxs-lookup"><span data-stu-id="7b4e2-373">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="7b4e2-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="7b4e2-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="7b4e2-375">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="7b4e2-375">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="7b4e2-376">Nota</span><span class="sxs-lookup"><span data-stu-id="7b4e2-376">Note</span></span>**  
    <span data-ttu-id="7b4e2-377">Questo cmdlet richiede un file eseguibile (con estensione exe) o batch (. bat).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-377">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="7b4e2-378">Devi specificare un file eseguibile o batch vuoto (Nothing).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-378">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-379">Passaggio</span><span class="sxs-lookup"><span data-stu-id="7b4e2-379">Step</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-380">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-380">Considerations</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-381">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b4e2-381">Benefits</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-382">Sui compromessi nella</span><span class="sxs-lookup"><span data-stu-id="7b4e2-382">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-383">Nessuna installazione di SXS in pubblicazione (pre-installare gli assembly SxS)</span><span class="sxs-lookup"><span data-stu-id="7b4e2-383">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-384">I pacchetti di applicazioni virtuali non devono essere risequenziati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-384">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="7b4e2-385">Gli assembly SxS possono rimanere nel pacchetto dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-385">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-386">Le dipendenze dell'assembly SxS non verranno installate in fase di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-386">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-387">Le dipendenze dell'assembly SxS devono essere preinstallate.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-387">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7b4e2-388">Creazione di un nuovo pacchetto di applicazione virtuale nel sequencer</span><span class="sxs-lookup"><span data-stu-id="7b4e2-388">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="7b4e2-389">Se durante il monitoraggio del sequencer viene installato un assembly SxS, ad esempio un runtime VC + +, come parte dell'installazione di un'applicazione, l'assembly SxS verrà rilevato e incluso automaticamente nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-389">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="7b4e2-390">L'amministratore riceverà una notifica e avrà l'opzione di escludere l'assembly SxS.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-390">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="7b4e2-391">**Lato client**:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-391">**Client Side**:</span></span>

<span data-ttu-id="7b4e2-392">Quando si pubblica un pacchetto di applicazione virtuale, il client App-V 5,0 SP2 rileverà se è già installata una dipendenza di SxS necessaria.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-392">When publishing a virtual application package, the App-V 5.0 SP2 Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="7b4e2-393">Se la dipendenza non è disponibile nel computer ed è inclusa nel pacchetto, un Windows Installer tradizionale (.\*\* MSI\*\*) verrà avviata l'installazione dell'assembly SxS.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-393">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="7b4e2-394">Come descritto in precedenza, è sufficiente installare la dipendenza dal computer in cui viene eseguito il client per verificare che l'installazione di Windows Installer (con estensione msi) non si verifichi.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-394">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-395">Passaggio</span><span class="sxs-lookup"><span data-stu-id="7b4e2-395">Step</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-396">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-396">Considerations</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-397">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b4e2-397">Benefits</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-398">Sui compromessi nella</span><span class="sxs-lookup"><span data-stu-id="7b4e2-398">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-399">Usare i file di configurazione dinamica in modo selettivo</span><span class="sxs-lookup"><span data-stu-id="7b4e2-399">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-400">Il client App-V 5,0 deve analizzare ed elaborare questi file di configurazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-400">The App-V 5.0 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="7b4e2-401">Essere consapevoli delle dimensioni e della complessità (esecuzione di script, inclusioni/esclusioni di ORSAE) del file.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-401">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="7b4e2-402">I numerosi pacchetti di applicazioni virtuali possono avere già file di configurazioni dinamiche specifici dell'utente o del computer.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-402">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-403">Gli orari di pubblicazione migliorano se questi file vengono usati in modo selettivo o non.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-403">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-404">I pacchetti di applicazioni virtuali devono essere riconfigurati singolarmente o tramite la console di gestione di App-V Server per rimuovere i file di configurazione dinamica associati.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-404">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7b4e2-405">Disabilitazione di una configurazione dinamica tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b4e2-405">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="7b4e2-406">Per i pacchetti già pubblicati, è possibile usare `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` senza</span><span class="sxs-lookup"><span data-stu-id="7b4e2-406">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="7b4e2-407">Parametro **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="7b4e2-407">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="7b4e2-408">Allo stesso modo, quando si aggiungono nuovi pacchetti in uso `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , non usare la</span><span class="sxs-lookup"><span data-stu-id="7b4e2-408">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="7b4e2-409">**-Parametro DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-409">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="7b4e2-410">Per la documentazione su come applicare una configurazione dinamica, vedere:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-410">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="7b4e2-411">Come applicare il file di configurazione utente con PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b4e2-411">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [<span data-ttu-id="7b4e2-412">Come applicare il file di configurazione della distribuzione con PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b4e2-412">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7b4e2-413">Passaggio</span><span class="sxs-lookup"><span data-stu-id="7b4e2-413">Step</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-414">Considerazioni</span><span class="sxs-lookup"><span data-stu-id="7b4e2-414">Considerations</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-415">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="7b4e2-415">Benefits</span></span></th>
<th align="left"><span data-ttu-id="7b4e2-416">Sui compromessi nella</span><span class="sxs-lookup"><span data-stu-id="7b4e2-416">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7b4e2-417">Account per l'esecuzione di script sincroni durante il ciclo di vita del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-417">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-418">Se la garanzia di script è incorporata nel pacchetto, Add (PowerShell) potrebbe essere significativamente più lento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-418">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="7b4e2-419">L'esecuzione di script durante l'avvio dell'applicazione virtuale (StartVirtualEnvironment, StartProcess quale nome) e/o Add + Publish avrà un impatto sulle prestazioni percepite durante una o più delle operazioni del ciclo di vita.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-419">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-420">L'uso di script asincroni (non bloccanti) assicura che le operazioni di ciclo di vita vengano completate in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-420">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-421">Questo passaggio richiede la conoscenza della gestione di tutti i pacchetti di applicazioni virtuali con garanzie di script incorporato, che hanno associato file di configurazioni dinamiche e che fanno riferimento ed eseguono script in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-421">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7b4e2-422">Rimuovere i tipi di carattere virtuali estranei dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-422">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-423">La maggior parte delle applicazioni esaminate dal team di prodotti App-V conteneva un numero limitato di tipi di carattere, in genere meno di 20.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-423">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-424">I tipi di carattere virtuali incidono sulle prestazioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-424">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7b4e2-425">I tipi di carattere desiderati devono essere abilitati/installati in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-425">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="7b4e2-426">Per istruzioni, vedere installare o disinstallare tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-426">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="7b4e2-427">Determinazione dei tipi di carattere virtuali presenti nel pacchetto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-427">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="7b4e2-428">Creare una copia del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-428">Make a copy of the package.</span></span>

-   <span data-ttu-id="7b4e2-429">Rinomina pacchetto \ _copy. AppV in Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="7b4e2-429">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="7b4e2-430">Aprire AppxManifest.xml e individuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-430">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="7b4e2-431">&lt;appv: Extension Category = "AppV. fonts"&gt;</span><span class="sxs-lookup"><span data-stu-id="7b4e2-431">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="7b4e2-432">&lt;appv: tipi di carattere&gt;</span><span class="sxs-lookup"><span data-stu-id="7b4e2-432">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="7b4e2-433">&lt;appv: font path = "\ [{fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /appv: tipo di carattere&gt;</span><span class="sxs-lookup"><span data-stu-id="7b4e2-433">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="7b4e2-434">Nota</span><span class="sxs-lookup"><span data-stu-id="7b4e2-434">Note</span></span>**  
    <span data-ttu-id="7b4e2-435">Se sono presenti tipi di carattere contrassegnati come **DelayLoad**, il primo avvio non verrà influenzato.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-435">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="7b4e2-436">Esclusione di tipi di carattere virtuali dal pacchetto</span><span class="sxs-lookup"><span data-stu-id="7b4e2-436">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="7b4e2-437">Usare il file di configurazione dinamica più adatto per l'ambito utente, ovvero la configurazione della distribuzione per tutti gli utenti del computer, la configurazione utente per utente o utenti specifici.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-437">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="7b4e2-438">Disabilitare i tipi di carattere con la configurazione di distribuzione o utente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-438">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="7b4e2-439">Tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="7b4e2-439">Fonts</span></span>

--&gt;

<span data-ttu-id="7b4e2-440">&lt;Tipi di carattere abilitati = "falso"/&gt;</span><span class="sxs-lookup"><span data-stu-id="7b4e2-440">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="7b4e2-441">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="7b4e2-441">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="7b4e2-442">Terminologia di guida alle prestazioni di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7b4e2-442">App-V 5.0 Performance Guidance Terminology</span></span>


<span data-ttu-id="7b4e2-443">I termini seguenti vengono usati per descrivere concetti e azioni correlati all'ottimizzazione delle prestazioni di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-443">The following terms are used when describing concepts and actions related to App-V 5.0 performance optimization.</span></span>

-   <span data-ttu-id="7b4e2-444">**Complessità** : si riferisce a una o più caratteristiche del pacchetto che potrebbero avere un impatto sulle prestazioni durante la configurazione preliminare (**Add-AppvClientPackage**) o Integration (**Publish-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-444">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="7b4e2-445">Alcune caratteristiche dell'esempio sono: dimensione del manifesto, numero di tipi di carattere virtuali, numero di file.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-445">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="7b4e2-446">**De-integrare** : rimuove le integrazioni degli utenti</span><span class="sxs-lookup"><span data-stu-id="7b4e2-446">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="7b4e2-447">**Reintegrarsi** : applica le integrazioni degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-447">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="7b4e2-448">**Non persistente, in pool** : crea un computer che gestisce un ambiente virtuale ogni volta che effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-448">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="7b4e2-449">**Persistente, personale,** un computer che gestisce un ambiente virtuale che rimane invariato per ogni account di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-449">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="7b4e2-450">Con **stato** -per questo documento, implica che le integrazioni degli utenti vengano rese persistenti tra le sessioni e che una tecnologia di gestione dell'ambiente utente venga usata in combinazione con RDSH non persistente o VDI.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-450">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="7b4e2-451">**Apolide** : rappresenta uno scenario in cui nessun stato utente viene mantenuto tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-451">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="7b4e2-452">**Trigger** -(o trigger di azione nativa).</span><span class="sxs-lookup"><span data-stu-id="7b4e2-452">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="7b4e2-453">UPM usa questi tipi di trigger per avviare operazioni di monitoraggio o sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-453">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="7b4e2-454">**User Experience** -nel contesto dell'App-V 5,0, l'esperienza utente, quantitativamente, è la somma delle parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b4e2-454">**User Experience** - In the context of App-V 5.0, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="7b4e2-455">Dal punto in cui gli utenti avviano un log-in quando sono in grado di manipolare il desktop.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-455">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="7b4e2-456">Dal punto in cui il desktop può essere interagito con il punto di inizio di un aggiornamento della pubblicazione (in termini di PowerShell, sincronizzazione) quando si usa l'infrastruttura di server completo di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-456">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.0 full server infrastructure.</span></span> <span data-ttu-id="7b4e2-457">In istanze autonome, è il momento in cui vengono avviati i comandi di PowerShell **Add-AppVClientPackage** e **Publish-AppVClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="7b4e2-457">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="7b4e2-458">Dall'inizio al completamento dell'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-458">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="7b4e2-459">In istanze autonome questa è la prima dell'ultima applicazione virtuale pubblicata.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-459">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="7b4e2-460">Dal punto in cui è disponibile l'applicazione virtuale per l'avvio da un collegamento.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-460">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="7b4e2-461">In alternativa, è il punto in cui è registrata l'associazione del tipo di file e verrà avviata un'applicazione virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-461">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="7b4e2-462">**Gestione dei profili utente** : approccio controllato e strutturato per la gestione dei componenti utente associati all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-462">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="7b4e2-463">Ad esempio, i profili utente, la gestione delle preferenze e dei criteri, il controllo delle applicazioni e la distribuzione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-463">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="7b4e2-464">Puoi usare le soluzioni di scripting o di terze parti per configurare l'ambiente in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7b4e2-464">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="7b4e2-465">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b4e2-465">Related topics</span></span>


[<span data-ttu-id="7b4e2-466">Guida dell'amministratore di Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="7b4e2-466">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)









