---
title: Distribuzione del server App-V 5.0
description: Distribuzione del server App-V 5.0
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805829"
---
# <span data-ttu-id="aa68c-103">Distribuzione del server App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="aa68c-103">Deploying the App-V 5.0 Server</span></span>


<span data-ttu-id="aa68c-104">È possibile installare le caratteristiche del server App-V 5,0 usando configurazioni di distribuzione diverse, descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="aa68c-104">You can install the App-V 5.0 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="aa68c-105">Prima di installare le funzionalità del server, esaminare la sezione server delle [considerazioni sulla sicurezza di App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="aa68c-105">Before you install the server features, review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

<span data-ttu-id="aa68c-106">Per informazioni sulla distribuzione del server App-V 5,0 SP3, vedere [informazioni su App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="aa68c-106">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

<span data-ttu-id="aa68c-107">**Importante**  Prima di installare e configurare i server App-V 5,0, è necessario specificare una porta in cui verranno ospitati tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="aa68c-107">**Important** Before you install and configure the App-V 5.0 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="aa68c-108">Devi anche aggiungere le regole del firewall associate per consentire alle richieste in arrivo di accedere alle porte specificate.</span><span class="sxs-lookup"><span data-stu-id="aa68c-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="aa68c-109">Il programma di installazione non modifica le impostazioni del firewall.</span><span class="sxs-lookup"><span data-stu-id="aa68c-109">The installer does not modify firewall settings.</span></span>

 

## <a href="" id="---------app-v-5-0-server-overview"></a> <span data-ttu-id="aa68c-110">Panoramica del server App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aa68c-110">App-V 5.0 Server overview</span></span>


<span data-ttu-id="aa68c-111">Il server App-V 5,0 è costituito da cinque componenti.</span><span class="sxs-lookup"><span data-stu-id="aa68c-111">The App-V 5.0 Server is made up of five components.</span></span> <span data-ttu-id="aa68c-112">Ogni componente offre uno scopo diverso nell'ambiente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-112">Each component serves a different purpose within the App-V 5.0 environment.</span></span> <span data-ttu-id="aa68c-113">Ognuno dei cinque componenti è brevemente descritto qui:</span><span class="sxs-lookup"><span data-stu-id="aa68c-113">Each of the five components is briefly described here:</span></span>

-   <span data-ttu-id="aa68c-114">Server di gestione: offre funzionalità di gestione complessive per l'infrastruttura App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-114">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="aa68c-115">Database di gestione: consente di semplificare le predistribuzioni di database per la gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-115">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="aa68c-116">Publishing Server: offre funzionalità di hosting e flusso per le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="aa68c-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="aa68c-117">Reporting Server: offre app-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="aa68c-117">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="aa68c-118">Database delle relazioni: consente di semplificare le predistribuzioni di database per la creazione di report in App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-118">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> <span data-ttu-id="aa68c-119">Implementazione autonoma di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aa68c-119">App-V 5.0 stand-alone deployment</span></span>


<span data-ttu-id="aa68c-120">La distribuzione autonoma di App-V 5,0 offre una buona topologia per una distribuzione di piccole dimensioni o un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="aa68c-120">The App-V 5.0 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="aa68c-121">Quando si usa questo tipo di implementazione, tutti i componenti del server vengono distribuiti in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="aa68c-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="aa68c-122">I servizi e i database associati verranno confrontati per le risorse nel computer che esegue i componenti dell'App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.0 components.</span></span> <span data-ttu-id="aa68c-123">Di conseguenza, non è consigliabile usare questa topologia per distribuzioni più grandi.</span><span class="sxs-lookup"><span data-stu-id="aa68c-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="aa68c-124">Come distribuire il server App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="aa68c-124">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)

[<span data-ttu-id="aa68c-125">Come distribuire il server App-V 5.0 con uno script</span><span class="sxs-lookup"><span data-stu-id="aa68c-125">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> <span data-ttu-id="aa68c-126">Implementazione distribuita del server App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aa68c-126">App-V 5.0 Server distributed deployment</span></span>


<span data-ttu-id="aa68c-127">La topologia di distribuzione distribuita può supportare una grande base client App-V 5,0 e consente di gestire e ridimensionare più facilmente l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="aa68c-127">The distributed deployment topology can support a large App-V 5.0 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="aa68c-128">Quando si usa questo tipo di distribuzione, i componenti del server App-V 5,0 vengono distribuiti in più computer, in base alla struttura e ai requisiti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="aa68c-128">When you use this type of deployment, the App-V 5.0 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="aa68c-129">Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report</span><span class="sxs-lookup"><span data-stu-id="aa68c-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="aa68c-130">Come installare il server di report in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="aa68c-130">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[<span data-ttu-id="aa68c-131">Come distribuire il server App-V 5.0 con uno script</span><span class="sxs-lookup"><span data-stu-id="aa68c-131">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="aa68c-132">Come installare il server di pubblicazione in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="aa68c-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="aa68c-133">Come installare il server di gestione in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="aa68c-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## <span data-ttu-id="aa68c-134">Uso di una soluzione ESD (Enterprise Software Distribution) e di un'app-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aa68c-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.0</span></span>


<span data-ttu-id="aa68c-135">Puoi anche distribuire i client e i pacchetti App-V 5,0 usando un ESD senza dover distribuire App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-135">You can also deploy the App-V 5.0 clients and packages by using an ESD without having to deploy App-V 5.0.</span></span> <span data-ttu-id="aa68c-136">Le funzionalità complete per l'integrazione variano a seconda dell'ESD usato.</span><span class="sxs-lookup"><span data-stu-id="aa68c-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

<span data-ttu-id="aa68c-137">**Nota**  Il server di report e il database di report di App-V 5,0 possono comunque essere distribuiti insieme all'ESD per raccogliere i dati dei report dai client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-137">**Note** The App-V 5.0 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.0 clients.</span></span> <span data-ttu-id="aa68c-138">Tuttavia, gli altri tre componenti del server non devono essere distribuiti perché si scontrano con la funzionalità ESD.</span><span class="sxs-lookup"><span data-stu-id="aa68c-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

 

[<span data-ttu-id="aa68c-139">Distribuzione di pacchetti App-V 5.0 con una soluzione di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="aa68c-139">Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> <span data-ttu-id="aa68c-140">Log del server App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aa68c-140">App-V 5.0 Server logs</span></span>


<span data-ttu-id="aa68c-141">Puoi usare le informazioni sul log di App-V 5,0 per risolvere i problemi relativi all'installazione e agli eventi operativi del server durante l'uso di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-141">You can use App-V 5.0 server log information to help troubleshoot the server installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="aa68c-142">Le informazioni del log correlate al server possono essere esaminate con il **Visualizzatore eventi**.</span><span class="sxs-lookup"><span data-stu-id="aa68c-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="aa68c-143">Nella riga seguente viene visualizzato il percorso specifico per gli eventi correlati al server:</span><span class="sxs-lookup"><span data-stu-id="aa68c-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="aa68c-144">Visualizzatore eventi \ \ applicazioni e registri Servizi \ \ Microsoft \ \ App V</span><span class="sxs-lookup"><span data-stu-id="aa68c-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="aa68c-145">I registri di configurazione associati vengono salvati nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="aa68c-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="aa68c-146">Temp</span><span class="sxs-lookup"><span data-stu-id="aa68c-146">%temp%</span></span>**

<span data-ttu-id="aa68c-147">In App-V 5,0 SP3 alcuni registri sono stati consolidati e spostati.</span><span class="sxs-lookup"><span data-stu-id="aa68c-147">In App-V 5.0 SP3, some logs have been consolidated and moved.</span></span> <span data-ttu-id="aa68c-148">Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="aa68c-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-0-reporting"></a> <span data-ttu-id="aa68c-149">Creazione di report in App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aa68c-149">App-V 5.0 reporting</span></span>


<span data-ttu-id="aa68c-150">La creazione di report in App-V 5,0 consente ai client App-V 5,0 di raccogliere dati e quindi di inviarli di nuovo per essere archiviati in un repository centrale.</span><span class="sxs-lookup"><span data-stu-id="aa68c-150">App-V 5.0 reporting allows App-V 5.0 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="aa68c-151">Puoi usare queste informazioni per ottenere una migliore visualizzazione dell'utilizzo dell'applicazione virtuale all'interno dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="aa68c-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="aa68c-152">L'elenco seguente mostra alcuni tipi di informazioni raccolte dal client App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="aa68c-152">The following list displays some of the types of information the App-V 5.0 client collects:</span></span>

-   <span data-ttu-id="aa68c-153">Informazioni sul computer in cui viene eseguito il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-153">Information about the computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="aa68c-154">Informazioni sui pacchetti virtualizzati in uno specifico computer in cui viene eseguito il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aa68c-154">Information about virtualized packages on a specific computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="aa68c-155">Informazioni sul pacchetto aperto e Shutdown per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="aa68c-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="aa68c-156">Le informazioni di report verranno mantenute fino a quando non vengono inviate correttamente al database del server di report.</span><span class="sxs-lookup"><span data-stu-id="aa68c-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="aa68c-157">Dopo che i dati sono presenti nel database, è possibile usare Microsoft SQL Server Reporting Services per generare i report necessari.</span><span class="sxs-lookup"><span data-stu-id="aa68c-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="aa68c-158">Se si vogliono recuperare le informazioni del report, è necessario usare Microsoft SQL Server Reporting Services (SSRS), disponibile in Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="aa68c-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="aa68c-159">SSRS non viene installato quando si installa il server di report App-V 5,0 e deve essere distribuito separatamente per generare i report associati.</span><span class="sxs-lookup"><span data-stu-id="aa68c-159">SSRS is not installed when you install the App-V 5.0 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="aa68c-160">Usare il collegamento seguente per altre informazioni [sulla creazione di report di App-V 5,0](about-app-v-50-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="aa68c-160">Use the following link for more information [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>

[<span data-ttu-id="aa68c-161">Come abilitare la creazione di report nel client App-V 5.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa68c-161">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## <span data-ttu-id="aa68c-162">Altre risorse per l'App-V Server</span><span class="sxs-lookup"><span data-stu-id="aa68c-162">Other resources for the App-V server</span></span>


[<span data-ttu-id="aa68c-163">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="aa68c-163">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)






 

 





