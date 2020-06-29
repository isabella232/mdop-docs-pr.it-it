---
title: Identificare il numero di istanze di MED-V
description: Identificare il numero di istanze di MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824256"
---
# <span data-ttu-id="78cf9-103">Identificare il numero di istanze di MED-V</span><span class="sxs-lookup"><span data-stu-id="78cf9-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="78cf9-104">Devi determinare il numero di istanze di MED-V e definire l'ambito per ogni istanza in modo da poter progettare l'infrastruttura server.</span><span class="sxs-lookup"><span data-stu-id="78cf9-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="78cf9-105">Un'istanza di MED-V include le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="78cf9-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="78cf9-106">Il server MED-V e le aree di lavoro MED-V archiviate nel server, incluse le autorizzazioni di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78cf9-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="78cf9-107">Database di SQL Server che archivia gli eventi client.</span><span class="sxs-lookup"><span data-stu-id="78cf9-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="78cf9-108">Il database può essere condiviso da più istanze di MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="78cf9-109">Archivio immagini per le immagini di MED-V imballate.</span><span class="sxs-lookup"><span data-stu-id="78cf9-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="78cf9-110">Il repository può essere condiviso da più istanze di MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="78cf9-111">Console di gestione utilizzata per creare e comprimere immagini e per creare aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="78cf9-112">La console non può essere usata contemporaneamente da più istanze di MED-V, ma può essere disconnessa da un server MED-V e quindi connessa a un altro server MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="78cf9-113">I client MED-V che ricevono aree di lavoro MED-V e l'autorizzazione per usarli dal server.</span><span class="sxs-lookup"><span data-stu-id="78cf9-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="78cf9-114">Le istanze di MED-V separate non possono essere integrate o condividono aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="78cf9-115">Di conseguenza, ogni istanza aggiuntiva decentralizza la gestione della virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="78cf9-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="78cf9-116">Determinare il numero di istanze MED-V necessarie</span><span class="sxs-lookup"><span data-stu-id="78cf9-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="78cf9-117">Iniziare presupponendo di usare un'istanza di MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="78cf9-118">Prendi in considerazione le condizioni seguenti e Aggiungi altre istanze per ogni condizione che si applica all'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="78cf9-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="78cf9-119">Numero di utenti supportati: ogni istanza di MED-V può supportare fino a 5.000 client attivi concorrentemente.</span><span class="sxs-lookup"><span data-stu-id="78cf9-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="78cf9-120">Attiva contemporaneamente: il client è online con il server MED-V e invia i sondaggi al server per gli aggiornamenti dei criteri e delle immagini, oltre agli eventi.</span><span class="sxs-lookup"><span data-stu-id="78cf9-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="78cf9-121">Se l'infrastruttura includerà più di 5.000 utenti attivi, aggiungere un'istanza per ogni utente di 5.000.</span><span class="sxs-lookup"><span data-stu-id="78cf9-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="78cf9-122">Utenti nei domini non attendibili: le autorizzazioni dell'area di lavoro MED-V Server associa l'attività di SharePoint con utenti e/o gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78cf9-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="78cf9-123">Ciò richiede che gli utenti di MED-V siano presenti all'interno del limite di attendibilità del server MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="78cf9-124">Aggiungere un'istanza MED-V per ogni gruppo di utenti MED-V che si trova in un dominio separato e non attendibile.</span><span class="sxs-lookup"><span data-stu-id="78cf9-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="78cf9-125">Client in reti isolate: determinare se i client si trovano in reti isolate e quindi richiedono un'istanza MED-V separata.</span><span class="sxs-lookup"><span data-stu-id="78cf9-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="78cf9-126">Ad esempio, le organizzazioni spesso isolano le reti Lab dalle reti di produzione.</span><span class="sxs-lookup"><span data-stu-id="78cf9-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="78cf9-127">Aggiungere un'istanza MED-V per ogni rete isolata che conterrà client MED-V.</span><span class="sxs-lookup"><span data-stu-id="78cf9-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="78cf9-128">Requisiti organizzativi: l'organizzazione può richiedere che un gruppo di client venga gestito da un'istanza di MED-V separata per motivi di sicurezza, ad esempio quando le applicazioni riservate vengono recapitate solo a un set limitato di utenti all'interno di un dominio.</span><span class="sxs-lookup"><span data-stu-id="78cf9-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="78cf9-129">Ad esempio, il reparto retribuzioni può impedire agli utenti di altri reparti di accedere all'istanza MED-V che archivia i criteri per l'elaborazione dei salari.</span><span class="sxs-lookup"><span data-stu-id="78cf9-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="78cf9-130">Inoltre, se l'organizzazione usa un modello di gestione distribuita, potrebbe essere necessaria un'istanza di MED-V separata per ogni gruppo aziendale con client MED-V per consentire al gruppo di gestire il proprio ambiente virtualizzato.</span><span class="sxs-lookup"><span data-stu-id="78cf9-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="78cf9-131">Aggiungere un'istanza MED-V per ogni requisito dell'organizzazione separato.</span><span class="sxs-lookup"><span data-stu-id="78cf9-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="78cf9-132">Considerazioni legali: i problemi di sicurezza o di privacy nazionali e le leggi fiduciarie potrebbero richiedere la separazione di determinati dati o impedire che altri dati attraversino i confini nazionali.</span><span class="sxs-lookup"><span data-stu-id="78cf9-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="78cf9-133">Se necessario, aggiungere altre istanze di MED-V per rispondere a questa esigenza.</span><span class="sxs-lookup"><span data-stu-id="78cf9-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="78cf9-134">Dopo aver determinato il numero di istanze MED-V necessarie per l'infrastruttura, nonché il ragionamento per ognuno di essi, specificare un nome per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="78cf9-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 





