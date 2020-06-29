---
title: Pianificazione per la compatibilità del sistema operativo dell'applicazione
description: Pianificazione per la compatibilità del sistema operativo dell'applicazione
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825466"
---
# <span data-ttu-id="40a6d-103">Pianificazione per la compatibilità del sistema operativo dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="40a6d-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="40a6d-104">Questo argomento consente di determinare come risolvere i problemi di compatibilità dei sistemi operativi delle applicazioni e illustra come funziona Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 come soluzione per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="40a6d-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="40a6d-105">Questo argomento illustra i requisiti aziendali per MED-V e confronta MED-V con la modalità Windows XP e Microsoft Application Virtualization (App-V):</span><span class="sxs-lookup"><span data-stu-id="40a6d-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="40a6d-106">Requisiti aziendali per MED-V</span><span class="sxs-lookup"><span data-stu-id="40a6d-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="40a6d-107">Vantaggi della modalità MED-V versus Windows XP</span><span class="sxs-lookup"><span data-stu-id="40a6d-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="40a6d-108">Vantaggi di MED-V versus App-V</span><span class="sxs-lookup"><span data-stu-id="40a6d-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="40a6d-109">Requisiti aziendali per MED-V</span><span class="sxs-lookup"><span data-stu-id="40a6d-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="40a6d-110">Quando il reparto IT dell'azienda sta determinando se eseguire l'aggiornamento a Windows 7, deve prestare attenzione alle applicazioni line-of-business e alle applicazioni line-of-business basate sul Web per accertarsi che possano essere eseguite nel nuovo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="40a6d-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="40a6d-111">Spesso queste applicazioni e URL sono stati creati per lavorare in modo specifico con una versione precedente di Windows o Internet Explorer e i problemi possono verificarsi quando si prova a usarli nel nuovo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="40a6d-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="40a6d-112">Microsoft offre numerosi metodi diversi per gestire i vari problemi di compatibilità che possono verificarsi durante l'aggiornamento, ad esempio Application Compatibility Toolkit (ACT) e Windows 7 Compatibility Assistant.</span><span class="sxs-lookup"><span data-stu-id="40a6d-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="40a6d-113">Ma anche dopo che tutte le applicazioni sono state testate per la compatibilità e sono state determinate correzioni, alcune applicazioni non funzionano ancora correttamente in Windows 7 o sono troppo costose per risolverlo.</span><span class="sxs-lookup"><span data-stu-id="40a6d-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="40a6d-114">Usando MED-V puoi eseguire queste applicazioni legacy tramite un ambiente Windows Virtual PC in cui è in esecuzione Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40a6d-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="40a6d-115">Dato che non è più necessario testare e convalidare queste applicazioni nel nuovo sistema operativo prima di eseguire l'aggiornamento, la migrazione a Windows 7 è molto più agevole e veloce.</span><span class="sxs-lookup"><span data-stu-id="40a6d-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="40a6d-116">Uso dell'elenco di controllo MED-V</span><span class="sxs-lookup"><span data-stu-id="40a6d-116">Using MED-V Checklist</span></span>

<span data-ttu-id="40a6d-117">Considerare MED-V se si applicano gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="40a6d-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="40a6d-118">Si è un'organizzazione di grandi dimensioni (ad esempio gli utenti di 500 e altro), si ha un accordo aziendale con Microsoft e si prevede di eseguire l'aggiornamento a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40a6d-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="40a6d-119">Hai testato le tue applicazioni line-of-business e ne hai trovate alcune che non sono compatibili con Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40a6d-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="40a6d-120">Sono stati risolti i problemi di compatibilità per alcune di queste applicazioni di problemi aggiornando l'applicazione o usando uno shim fornito da Microsoft, ad esempio Application Compatibility Toolkit (ACT), ma i problemi di compatibilità rimangono per alcune applicazioni.</span><span class="sxs-lookup"><span data-stu-id="40a6d-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="40a6d-121">Hai considerato App-V come opzione per il recapito delle applicazioni incompatibili e hai concluso che anche dopo aver implementato App-V, hai ancora problemi di compatibilità del sistema operativo per le applicazioni che devi affrontare.</span><span class="sxs-lookup"><span data-stu-id="40a6d-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="40a6d-122">È stata considerata una soluzione la modalità Windows XP e si è stabilito che non è un'opzione efficiente perché:</span><span class="sxs-lookup"><span data-stu-id="40a6d-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="40a6d-123">Si vuole essere in grado di distribuire immagini virtuali che contengono le applicazioni di problemi a tutti gli utenti finali contemporaneamente, invece che individualmente, e che le immagini virtuali vengano unite automaticamente al dominio.</span><span class="sxs-lookup"><span data-stu-id="40a6d-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="40a6d-124">Hai deciso che è molto più conveniente gestire queste applicazioni legacy (che vengono recapitate virtualmente) e controllare le impostazioni di Windows Virtual PC da una posizione centralizzata invece che dal desktop di ogni utente finale.</span><span class="sxs-lookup"><span data-stu-id="40a6d-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="40a6d-125">Si vuole essere in grado di aggiornare e supportare le macchine virtuali in scala anziché per desktop.</span><span class="sxs-lookup"><span data-stu-id="40a6d-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="40a6d-126">Si vuole avere la possibilità di reindirizzare gli URL che vengono eseguiti meglio in una versione precedente di Internet Explorer per le macchine virtuali e di gestire facilmente il reindirizzamento degli URL in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="40a6d-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="40a6d-127">È stato stabilito che sarebbe stato più conveniente e utile eseguire l'aggiornamento a Windows 7 il più presto possibile e aver deciso di rinviare la risoluzione dei problemi di compatibilità delle applicazioni rimanenti fino a una data successiva, sapendo di avere una soluzione disponibile in MED-V.</span><span class="sxs-lookup"><span data-stu-id="40a6d-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="40a6d-128">Vantaggi della modalità MED-V versus Windows XP</span><span class="sxs-lookup"><span data-stu-id="40a6d-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="40a6d-129">Windows Virtual PC per Windows 7 consente di eseguire contemporaneamente versioni diverse di un sistema operativo su un singolo dispositivo ed è incluso in Windows 7 Professional Edition e successive.</span><span class="sxs-lookup"><span data-stu-id="40a6d-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="40a6d-130">La funzionalità modalità Windows XP sfrutta Windows Virtual PC fornendo un'immagine di Windows XP preconfigurata che consente di creare un ambiente Windows XP virtuale.</span><span class="sxs-lookup"><span data-stu-id="40a6d-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="40a6d-131">In questo ambiente virtuale è possibile installare manualmente le applicazioni che non sono compatibili con Windows 7 e che vengono eseguite senza problemi dal desktop tramite Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="40a6d-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="40a6d-132">Usando la modalità Windows XP, è possibile eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="40a6d-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="40a6d-133">Eseguire applicazioni compatibili con Windows XP all'interno di una macchina virtuale eseguita in Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="40a6d-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="40a6d-134">Pubblicare queste applicazioni nel menu del desktop o del programma dell'host.</span><span class="sxs-lookup"><span data-stu-id="40a6d-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="40a6d-135">Quando si vuole consegnare queste macchine virtuali su larga scala come parte di una migrazione aziendale a Windows 7, è necessario essere in grado di distribuire le macchine virtuali in modo rapido, provisionare e personalizzarle in modo efficiente, controllarne le impostazioni e supportarle facilmente.</span><span class="sxs-lookup"><span data-stu-id="40a6d-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="40a6d-136">MED-V si basa sulla modalità Windows XP per garantire la compatibilità delle applicazioni a livello aziendale.</span><span class="sxs-lookup"><span data-stu-id="40a6d-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="40a6d-137">Mentre la modalità Windows XP si limita a fornire funzionalità di applicazione virtuale a utenti privati e piccole imprese, MED-V consente distribuzioni su larga scala di immagini di Windows XP preconfigurate in tutta la rete aziendale.</span><span class="sxs-lookup"><span data-stu-id="40a6d-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="40a6d-138">Offre una soluzione di gestione aziendale pronta per la configurazione, la distribuzione e la manutenzione di queste aree di lavoro virtuali MED-V.</span><span class="sxs-lookup"><span data-stu-id="40a6d-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="40a6d-139">MED-V offre anche a enterpriseadministrators un set di criteri per controllare l'uso delle immagini.</span><span class="sxs-lookup"><span data-stu-id="40a6d-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="40a6d-140">Ciò include gli utenti che avranno accesso a quali applicazioni specifiche all'interno di queste immagini.</span><span class="sxs-lookup"><span data-stu-id="40a6d-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="40a6d-141">Usando MED-V, è possibile eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="40a6d-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="40a6d-142">Eseguire l'aggiornamento al nuovo sistema operativo senza dover testare e risolvere tutte le applicazioni e gli URL non compatibili.</span><span class="sxs-lookup"><span data-stu-id="40a6d-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="40a6d-143">Distribuire immagini virtuali di Windows XP che vengono automaticamente unite al dominio e personalizzate per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="40a6d-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="40a6d-144">Eseguire il provisioning delle applicazioni e del reindirizzamento degli URL agli utenti.</span><span class="sxs-lookup"><span data-stu-id="40a6d-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="40a6d-145">Controllare le impostazioni di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="40a6d-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="40a6d-146">Gestire e supportare gli endpoint tramite il monitoraggio e la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="40a6d-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="40a6d-147">Assicurarsi che i computer guest siano corretti, anche se in stato sospesa.</span><span class="sxs-lookup"><span data-stu-id="40a6d-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="40a6d-148">Automatizzare la creazione di macchine virtuali per utente e l'inizializzazione di Sysprep.</span><span class="sxs-lookup"><span data-stu-id="40a6d-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="40a6d-149">Diagnosticare facilmente i problemi nei computer host e Guest.</span><span class="sxs-lookup"><span data-stu-id="40a6d-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="40a6d-150">Gestire senza problemi i computer guest connessi tramite la modalità NAT di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="40a6d-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="40a6d-151">Vantaggi di MED-V versus App-V</span><span class="sxs-lookup"><span data-stu-id="40a6d-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="40a6d-152">MED-V e App-V sono due tecnologie molto diverse che possono collaborare facilmente per risolvere i problemi di compatibilità dei sistemi operativi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40a6d-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="40a6d-153">Usando App-V, crei un pacchetto individualizzato per ogni applicazione, ognuno dei quali viene quindi mantenuto separato dagli altri.</span><span class="sxs-lookup"><span data-stu-id="40a6d-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="40a6d-154">Ogni applicazione virtuale può quindi essere immediatamente recapitata all'utente finale, che è molto utile per una strategia di distribuzione di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40a6d-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="40a6d-155">MED-V non gestisce le applicazioni singolarmente.</span><span class="sxs-lookup"><span data-stu-id="40a6d-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="40a6d-156">Crea invece un'ulteriore istanza di Windows XP nello stesso desktop in cui è in uso Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40a6d-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="40a6d-157">È possibile installare tutte le applicazioni necessarie in questa immagine virtuale e gestire l'immagine così come si farebbe con qualsiasi altro desktop dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="40a6d-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="40a6d-158">Inoltre, puoi usare MED-V insieme a App-V in modo che le applicazioni virtuali sequenziate tramite App-V vengano installate, pubblicate e gestite tramite MED-V.</span><span class="sxs-lookup"><span data-stu-id="40a6d-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="40a6d-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40a6d-159">Related topics</span></span>


[<span data-ttu-id="40a6d-160">Definire e pianificare la distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="40a6d-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 





