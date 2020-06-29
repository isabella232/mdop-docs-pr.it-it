---
title: Configurazione dell'amministrazione di App-V per un ambiente distribuito
description: Configurazione dell'amministrazione di App-V per un ambiente distribuito
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821915"
---
# <span data-ttu-id="f5628-103">Configurazione dell'amministrazione di App-V per un ambiente distribuito</span><span class="sxs-lookup"><span data-stu-id="f5628-103">Configuring App-V Administration for a Distributed Environment</span></span>


<span data-ttu-id="f5628-104">Quando si progetta l'infrastruttura per la propria organizzazione, è possibile installare il servizio Web di gestione App-V in un computer diverso dal computer in cui si installa l'App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="f5628-104">When designing the infrastructure for your specific organization, you can install the App-V Management Web Service on a computer other than the computer where you install the App-V Management Server.</span></span> <span data-ttu-id="f5628-105">I motivi comuni per separare questi componenti App-V includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5628-105">Common reasons for separating these App-V components include the following:</span></span>

-   <span data-ttu-id="f5628-106">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="f5628-106">Performance</span></span>

-   <span data-ttu-id="f5628-107">Affidabilità</span><span class="sxs-lookup"><span data-stu-id="f5628-107">Reliability</span></span>

-   <span data-ttu-id="f5628-108">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="f5628-108">Availability</span></span>

-   <span data-ttu-id="f5628-109">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="f5628-109">Scalability</span></span>

<span data-ttu-id="f5628-110">La separazione del server di gestione e del servizio Web di gestione richiede una configurazione aggiuntiva per l'infrastruttura per funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5628-110">Separating the Management Server and Management Web Service requires additional configuration for the infrastructure to operate correctly.</span></span> <span data-ttu-id="f5628-111">Quando si separano queste due caratteristiche ma non si completano le procedure descritte in questo argomento, la console di gestione si connette al servizio Web di gestione, ma non sarà in grado di eseguire correttamente l'autenticazione con l'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="f5628-111">When you separate these two features but do not complete the procedures described in this topic, the Management Console will connect to the Management Web Service but will not be able to properly authenticate with the data store.</span></span> <span data-ttu-id="f5628-112">La console di gestione non viene caricata correttamente e l'amministratore non sarà in grado di completare le attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f5628-112">The Management Console will not load properly, and the administrator will not be able to complete any administrative tasks.</span></span>

<span data-ttu-id="f5628-113">Questo comportamento si verifica perché il servizio Web di gestione non può usare le credenziali, passate dalla console di gestione, per accedere all'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="f5628-113">This behavior occurs because the Management Web Service cannot use the credentials, passed to it from the Management Console, to access the data store.</span></span> <span data-ttu-id="f5628-114">La soluzione consiste nel configurare il server del servizio Web di gestione come "attendibile per la delega".</span><span class="sxs-lookup"><span data-stu-id="f5628-114">The solution is to configure the Management Web Service server to be “Trusted for delegation.”</span></span>

## <span data-ttu-id="f5628-115">Configurazione dei servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="f5628-115">Configuring Active Directory Domain Services</span></span>


<span data-ttu-id="f5628-116">È anche necessario configurare correttamente i servizi di dominio Active Directory in modo che funzionino in un ambiente distribuito.</span><span class="sxs-lookup"><span data-stu-id="f5628-116">It is also necessary to configure Active Directory Domain Services properly to work in a distributed environment.</span></span> <span data-ttu-id="f5628-117">Questa sezione include le informazioni necessarie per configurare i servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5628-117">This section includes the information you need configure Active Directory Domain Services.</span></span>

### <span data-ttu-id="f5628-118">Quando SQL Service usa l'account di sistema locale</span><span class="sxs-lookup"><span data-stu-id="f5628-118">When SQL Service Uses Local System account</span></span>

<span data-ttu-id="f5628-119">Per configurare l'ambiente in cui il servizio SQL usa l'account di sistema locale, modificare le proprietà dell'account del computer del servizio Web di gestione come attendibile per la delega.</span><span class="sxs-lookup"><span data-stu-id="f5628-119">To set up the environment where the SQL Service uses the local system account, change the properties of the machine account of the Management Web Service to be trusted for delegation.</span></span> <span data-ttu-id="f5628-120">Per informazioni dettagliate su come eseguire questa operazione, vedere [come configurare il server come attendibile per la delega](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span><span class="sxs-lookup"><span data-stu-id="f5628-120">For detailed procedures about how to do this, see [How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span></span>

### <span data-ttu-id="f5628-121">Quando il servizio SQL usa un account basato su dominio</span><span class="sxs-lookup"><span data-stu-id="f5628-121">When SQL Service Uses Domain-Based Account</span></span>

<span data-ttu-id="f5628-122">Per configurare l'ambiente in cui SQL Server usa account del servizio basati su dominio, è necessario valutare se applicare o meno una varietà di fattori, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5628-122">To set up the environment where SQL Servers use domain-based service accounts, you need to consider whether or not a variety of factors apply, including the following:</span></span>

-   <span data-ttu-id="f5628-123">Raggruppamento di SQL Server</span><span class="sxs-lookup"><span data-stu-id="f5628-123">Clustering of SQL Server</span></span>

-   <span data-ttu-id="f5628-124">Replica</span><span class="sxs-lookup"><span data-stu-id="f5628-124">Replication</span></span>

-   <span data-ttu-id="f5628-125">Attività automatizzate</span><span class="sxs-lookup"><span data-stu-id="f5628-125">Automated tasks</span></span>

-   <span data-ttu-id="f5628-126">Server collegati</span><span class="sxs-lookup"><span data-stu-id="f5628-126">Linked servers</span></span>

<span data-ttu-id="f5628-127">Per informazioni sulla configurazione dei servizi di dominio Active Directory quando il servizio SQL usa un account basato su dominio, vedere <https://go.microsoft.com/fwlink/?LinkId=151968> .</span><span class="sxs-lookup"><span data-stu-id="f5628-127">For information about configuring Active Directory Domain Services when the SQL service uses a domain-based account, see <https://go.microsoft.com/fwlink/?LinkId=151968>.</span></span>

 

 





