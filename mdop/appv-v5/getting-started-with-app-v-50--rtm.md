---
title: Attività iniziali di App-V 5.0
description: Attività iniziali di App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805812"
---
# <span data-ttu-id="f4ea3-103">Attività iniziali di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-103">Getting Started with App-V 5.0</span></span>


<span data-ttu-id="f4ea3-104">App-V 5,0 consente agli amministratori di distribuire, aggiornare e supportare le applicazioni come servizi in tempo reale, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-104">App-V 5.0 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="f4ea3-105">Le singole applicazioni vengono trasformate da prodotti installati localmente in servizi gestiti centralmente e sono disponibili ovunque sia necessario, senza dover preconfigurare i computer o modificare le impostazioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="f4ea3-106">App-V è costituito dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4ea3-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4ea3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4ea3-107">Element</span></span></th>
<th align="left"><span data-ttu-id="f4ea3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4ea3-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4ea3-109">App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="f4ea3-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f4ea3-110">Fornisce una posizione centrale per la gestione dell'infrastruttura App-V, che offre applicazioni virtuali sia al client desktop di App-V che al client Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="f4ea3-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-111">USA Microsoft SQL Server® per il proprio archivio dati, in cui uno o più server di gestione di App-V possono condividere un singolo archivio dati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-112">Autentica le richieste e fornisce la sicurezza, la misurazione, il monitoraggio e la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="f4ea3-113">Il server usa Active Directory e strumenti di supporto per la gestione di utenti e applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-114">Dispone di un sito di gestione basato su Silverlight®, che consente di configurare l'infrastruttura App-V da qualsiasi computer.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-114">Has a Silverlight®-based management site, which enables you to configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="f4ea3-115">È possibile aggiungere e rimuovere applicazioni, modificare i tasti di scelta rapida, assegnare le autorizzazioni di accesso a utenti e gruppi e creare gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-116">Consente la comunicazione tra la console di gestione Web App-V e l'archivio dati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="f4ea3-117">Questi componenti possono essere installati in un singolo computer server o in uno o più computer separati, a seconda dell'architettura di sistema necessaria.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4ea3-118">App-V Publishing Server</span><span class="sxs-lookup"><span data-stu-id="f4ea3-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f4ea3-119">Fornisce i client App-V con le applicazioni aventi diritto per l'utente specifico</span><span class="sxs-lookup"><span data-stu-id="f4ea3-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-120">Ospita il pacchetto di applicazione virtuale per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4ea3-121">Client Desktop App-V</span><span class="sxs-lookup"><span data-stu-id="f4ea3-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f4ea3-122">Recupera le applicazioni virtuali</span><span class="sxs-lookup"><span data-stu-id="f4ea3-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-123">Pubblica le applicazioni nei client</span><span class="sxs-lookup"><span data-stu-id="f4ea3-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-124">Configura e gestisce automaticamente gli ambienti virtuali in fase di esecuzione sugli endpoint di Windows.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-125">Archivia le impostazioni dell'applicazione virtuale specifiche dell'utente, ad esempio il registro di sistema e le modifiche ai file, in ogni profilo utente&#39;s.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4ea3-126">Client Servizi Desktop remoto (RDS) App-V</span><span class="sxs-lookup"><span data-stu-id="f4ea3-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4ea3-127">Consente ai server Host sessione Desktop remoto di usare le funzionalità del client Desktop App-V per le sessioni desktop condivise.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4ea3-128">Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="f4ea3-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f4ea3-129">È uno strumento basato su una procedura guidata usato per trasformare le applicazioni tradizionali in applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-130">Genera l'applicazione "Package", che è costituita da:</span><span class="sxs-lookup"><span data-stu-id="f4ea3-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="f4ea3-131">un file di applicazione sequenziata (APPV)</span><span class="sxs-lookup"><span data-stu-id="f4ea3-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-132">file di Windows Installer (MSI) che può essere distribuito ai client configurati per l'operazione autonoma</span><span class="sxs-lookup"><span data-stu-id="f4ea3-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="f4ea3-133">Diversi file XML, inclusi Report.XML, PackageName_DeploymentConfig.XML e PackageName_UserConfig.XML.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="f4ea3-134">I file XML UserConfig e DeploymentConfig vengono usati per configurare le modifiche personalizzate al comportamento predefinito del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f4ea3-135">Per altre informazioni su questi elementi, Vedi [architettura ad alto livello per App-V 5,0](high-level-architecture-for-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="f4ea3-135">For more information about these elements, see [High Level Architecture for App-V 5.0](high-level-architecture-for-app-v-50.md).</span></span>

<span data-ttu-id="f4ea3-136">Se si è nuovi a questo prodotto, è consigliabile leggere accuratamente la documentazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="f4ea3-137">Prima di distribuirla in un ambiente di produzione, è consigliabile convalidare il piano di distribuzione in un ambiente di rete di test.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="f4ea3-138">Potresti anche prendere in considerazione l'assunzione di una classe sulle tecnologie rilevanti.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="f4ea3-139">Per altre informazioni sulle opportunità di formazione per Microsoft, vedere Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="f4ea3-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="f4ea3-140">**Nota**  Una versione scaricabile della Guida di questo amministratore non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="f4ea3-141">Tuttavia, è possibile ottenere informazioni su una modalità speciale della raccolta TechNet che consente di selezionare gli articoli, raggrupparli in una raccolta e stamparli o esportarli in un file in <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="f4ea3-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="f4ea3-142">Questa sezione della Guida dell'amministratore di App-V 5,0 include informazioni di alto livello su App-V 5,0 per offrirti una conoscenza di base del prodotto prima di iniziare la pianificazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-142">This section of the App-V 5.0 Administrator’s Guide includes high-level information about App-V 5.0 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="f4ea3-143">Guida introduttiva a App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-143">Getting started with App-V 5.0</span></span>


-   [<span data-ttu-id="f4ea3-144">Informazioni su App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-144">About App-V 5.0</span></span>](about-app-v-50.md)

    <span data-ttu-id="f4ea3-145">Offre una panoramica di alto livello su App-V 5,0 e su come può essere usata nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-145">Provides a high-level overview of App-V 5.0 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="f4ea3-146">Informazioni su App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f4ea3-146">About App-V 5.0 SP1</span></span>](about-app-v-50-sp1.md)

    <span data-ttu-id="f4ea3-147">Offre una panoramica di alto livello su App-V 5.0 SP1 e su come può essere usata nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-147">Provides a high-level overview of App-V 5.0SP1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="f4ea3-148">Informazioni su App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f4ea3-148">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

    <span data-ttu-id="f4ea3-149">Offre una panoramica di alto livello su App-V 5.0 SP2 e su come può essere usata nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-149">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="f4ea3-150">Informazioni su App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="f4ea3-150">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

    <span data-ttu-id="f4ea3-151">Offre una panoramica di alto livello su App-V 5.0 SP2 e su come può essere usata nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-151">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="f4ea3-152">Valutazione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-152">Evaluating App-V 5.0</span></span>](evaluating-app-v-50.md)

    <span data-ttu-id="f4ea3-153">Fornisce informazioni su come valutare al meglio l'App V 5,0 per l'uso nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-153">Provides information about how you can best evaluate App-V 5.0 for use in your organization.</span></span>

-   [<span data-ttu-id="f4ea3-154">Architettura di alto livello per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-154">High Level Architecture for App-V 5.0</span></span>](high-level-architecture-for-app-v-50.md)

    <span data-ttu-id="f4ea3-155">Fornisce una descrizione delle caratteristiche dell'App-V 5,0 e della loro collaborazione.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-155">Provides a description of the App-V 5.0 features and how they work together.</span></span>

-   [<span data-ttu-id="f4ea3-156">Accessibilità per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-156">Accessibility for App-V 5.0</span></span>](accessibility-for-app-v-50.md)

    <span data-ttu-id="f4ea3-157">Fornisce informazioni sulle caratteristiche e i servizi che rendono questo prodotto e la relativa documentazione più accessibile per gli utenti con disabilità.</span><span class="sxs-lookup"><span data-stu-id="f4ea3-157">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="f4ea3-158">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="f4ea3-158">Other resources for this product</span></span>


-   [<span data-ttu-id="f4ea3-159">Guida dell'amministratore di Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-159">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="f4ea3-160">Pianificazione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-160">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

-   [<span data-ttu-id="f4ea3-161">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-161">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

-   [<span data-ttu-id="f4ea3-162">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-162">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

-   [<span data-ttu-id="f4ea3-163">Risoluzione dei problemi relativi ad App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f4ea3-163">Troubleshooting App-V 5.0</span></span>](troubleshooting-app-v-50.md)






 

 





