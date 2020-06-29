---
title: Informazioni sulle licenze dell'applicazione
description: Informazioni sulle licenze dell'applicazione
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820096"
---
# <span data-ttu-id="5207f-103">Informazioni sulle licenze dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="5207f-103">About Application Licensing</span></span>


<span data-ttu-id="5207f-104">È possibile gestire le licenze applicative direttamente dalla console di gestione del server Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5207f-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="5207f-105">Tipi di licenza</span><span class="sxs-lookup"><span data-stu-id="5207f-105">License Types</span></span>


<span data-ttu-id="5207f-106">Il sistema di virtualizzazione delle applicazioni di System Center supporta attualmente i seguenti tipi di licenza:</span><span class="sxs-lookup"><span data-stu-id="5207f-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="5207f-107">**Licenza illimitata**: consente l'accesso all'applicazione in base a qualsiasi numero di utenti simultanei.</span><span class="sxs-lookup"><span data-stu-id="5207f-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="5207f-108">Questo metodo di gestione delle licenze è appropriato quando si vuole associare una licenza a livello aziendale a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5207f-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="5207f-109">**Licenza simultanea**: consente di definire il numero massimo di utenti simultanei autorizzati a usare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5207f-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="5207f-110">**Licenza denominata**: consente di assegnare una licenza a un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="5207f-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="5207f-111">Una licenza denominata può essere usata per garantire che un determinato utente sia sempre in grado di eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5207f-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="5207f-112">Puoi combinare licenze simultanee e denominate per la stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="5207f-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="5207f-113">La gestione delle licenze è disabilitata per impostazione predefinita, ma è possibile abilitarla dalla scheda **Pipeline provider** della finestra di dialogo **Proprietà provider** .</span><span class="sxs-lookup"><span data-stu-id="5207f-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="5207f-114">Per informazioni dettagliate sull'abilitazione e la disabilitazione delle licenze, vedere [come configurare o disabilitare le licenze](how-to-set-up-or-disable-application-licensing.md)per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5207f-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="5207f-115">Criteri per i provider</span><span class="sxs-lookup"><span data-stu-id="5207f-115">Provider Policies</span></span>


<span data-ttu-id="5207f-116">I criteri per il provider sono stati sviluppati per il modello ASP (Application Service Provider).</span><span class="sxs-lookup"><span data-stu-id="5207f-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="5207f-117">In questo modello una singola app ASP può ospitare un singolo sistema di virtualizzazione delle applicazioni per più client, in cui ogni client deve rimanere isolato.</span><span class="sxs-lookup"><span data-stu-id="5207f-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="5207f-118">I client potrebbero avere requisiti radicalmente diversi, ad esempio un client potrebbe richiedere l'autenticazione, mentre un altro non lo fa.</span><span class="sxs-lookup"><span data-stu-id="5207f-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="5207f-119">Puoi usare i criteri del provider per associare le autorizzazioni ai client in modo che solo gli utenti approvati possano accedere a ogni applicazione virtuale o pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="5207f-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="5207f-120">Per il cliente aziendale, è possibile usare questa funzionalità quando si hanno requisiti di licenza severi per una o più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5207f-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="5207f-121">In questa situazione, il componente licenza è disabilitato nella scheda **Pipeline provider** della finestra di dialogo **Proprietà provider** .</span><span class="sxs-lookup"><span data-stu-id="5207f-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="5207f-122">La scheda **Pipeline provider** include anche le caselle di controllo per abilitare l'autenticazione, l'autorizzazione (**applicare le impostazioni di autorizzazione di accesso**) e la misurazione (**informazioni sull'utilizzo dei log**).</span><span class="sxs-lookup"><span data-stu-id="5207f-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="5207f-123">Se la tua configurazione ha requisiti speciali, puoi scrivere i tuoi componenti della pipeline e aggiungerli al sistema facendo clic sul pulsante **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="5207f-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="5207f-124">Autorità account</span><span class="sxs-lookup"><span data-stu-id="5207f-124">Account Authorities</span></span>


<span data-ttu-id="5207f-125">L'autorità account è il dominio in cui è installato l'Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="5207f-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="5207f-126">Man mano che si procede con l'installazione del server, viene chiesto di specificare un nome di dominio; il dominio in cui è installato il computer viene rilevato e usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5207f-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="5207f-127">Quando gli utenti tentano di accedere al sistema, vengono richieste le credenziali prima di poter accedere a tale dominio.</span><span class="sxs-lookup"><span data-stu-id="5207f-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="5207f-128">Il sistema di virtualizzazione delle applicazioni supporta più domini.</span><span class="sxs-lookup"><span data-stu-id="5207f-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="5207f-129">Se si stabilisce una relazione di trust tra domini, è possibile concedere l'accesso alle applicazioni ai gruppi di utenti in altri domini.</span><span class="sxs-lookup"><span data-stu-id="5207f-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="5207f-130">Gli utenti devono fornire le credenziali riconosciute da ogni dominio.</span><span class="sxs-lookup"><span data-stu-id="5207f-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="5207f-131">Nella console di gestione di Application Virtualization Server è possibile modificare il dominio principale (autorità account) e le credenziali usate per accedervi.</span><span class="sxs-lookup"><span data-stu-id="5207f-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="5207f-132">Autenticazione</span><span class="sxs-lookup"><span data-stu-id="5207f-132">Authentication</span></span>


<span data-ttu-id="5207f-133">L'autenticazione è il meccanismo usato per confermare l'identità di un utente.</span><span class="sxs-lookup"><span data-stu-id="5207f-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="5207f-134">Qualsiasi utente con un nome utente e una password riconosciuti ha accesso.</span><span class="sxs-lookup"><span data-stu-id="5207f-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="5207f-135">Nel sistema di virtualizzazione dell'applicazione è possibile abilitare o disabilitare l'autenticazione tramite una casella di controllo nella scheda **Pipeline provider** . Per impostazione predefinita, l'autenticazione di Windows è abilitata.</span><span class="sxs-lookup"><span data-stu-id="5207f-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="5207f-136">Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5207f-136">Authorization</span></span>


<span data-ttu-id="5207f-137">L'autorizzazione è il processo usato per confermare l'identità di un utente.</span><span class="sxs-lookup"><span data-stu-id="5207f-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="5207f-138">Dopo aver confermato l'identità dell'utente, il sistema determina se l'utente ha concesso l'accesso al sistema e alle applicazioni a cui l'utente ha concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="5207f-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="5207f-139">La console di gestione di Application Virtualization Server include una casella di controllo **Applica impostazioni di autorizzazione di accesso** nella scheda **pipeline del provider** per abilitare o disabilitare l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5207f-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="5207f-140">Nel sistema di virtualizzazione dell'applicazione, l'accesso viene concesso solo a un gruppo di utenti, non a un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="5207f-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="5207f-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5207f-141">Related topics</span></span>


[<span data-ttu-id="5207f-142">Come gestire le licenze dell'applicazione in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="5207f-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="5207f-143">Come configurare o disabilitare le licenze dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="5207f-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="5207f-144">Server Management Console: Nodo Criteri dei provider</span><span class="sxs-lookup"><span data-stu-id="5207f-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





