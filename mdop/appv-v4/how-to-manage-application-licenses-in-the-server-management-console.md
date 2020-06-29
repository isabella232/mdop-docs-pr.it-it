---
title: Come gestire le licenze dell'applicazione in Server Management Console
description: Come gestire le licenze dell'applicazione in Server Management Console
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817225"
---
# <span data-ttu-id="9a2b3-103">Come gestire le licenze dell'applicazione in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="9a2b3-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="9a2b3-104">Application Virtualization Server Management Console è l'interfaccia usata per gestire la piattaforma di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="9a2b3-105">Da esso è possibile aggiungere, rimuovere, configurare e controllare i gruppi di licenze applicative.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="9a2b3-106">**Importante**  Se l'impostazione dell'origine dell'applicazione client App-V (ASR) è configurata in modo da usare qualsiasi tipo di origine di flusso diversa da quella del server di gestione, ad esempio un server di flusso, un server IIS o un file server, il server di gestione non è in grado di applicare i criteri di licenza.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="9a2b3-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="9a2b3-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="9a2b3-108">Come creare un gruppo di licenze per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="9a2b3-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="9a2b3-109">Fornisce una procedura per la creazione di una nuova applicazione in un gruppo di licenze.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="9a2b3-110">Come associare un'applicazione a un gruppo di licenze</span><span class="sxs-lookup"><span data-stu-id="9a2b3-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="9a2b3-111">Fornisce una procedura per l'aggiunta di un'applicazione a un gruppo di licenze.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="9a2b3-112">Come rimuovere un'applicazione da un gruppo di licenze</span><span class="sxs-lookup"><span data-stu-id="9a2b3-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="9a2b3-113">Fornisce una procedura per la rimozione di un'applicazione da un gruppo di licenze.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="9a2b3-114">Come rimuovere un gruppo di licenze per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="9a2b3-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="9a2b3-115">Questa sezione include i passaggi necessari per eliminare un gruppo di licenze applicative.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="9a2b3-116">Come configurare un gruppo di licenze illimitate</span><span class="sxs-lookup"><span data-stu-id="9a2b3-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="9a2b3-117">Fornisce una procedura per la creazione di un nuovo gruppo di licenze illimitate, che consente a un numero illimitato di utenti di accedere alle applicazioni nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="9a2b3-118">Come configurare un gruppo di licenze simultanee</span><span class="sxs-lookup"><span data-stu-id="9a2b3-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="9a2b3-119">Fornisce una procedura per la creazione di un nuovo gruppo di licenze simultanee, che consente a un numero specifico di utenti simultanei di accedere alle applicazioni nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="9a2b3-120">Come configurare un gruppo denominato di licenze</span><span class="sxs-lookup"><span data-stu-id="9a2b3-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="9a2b3-121">Fornisce una procedura per la creazione di un nuovo gruppo di licenze illimitate, che consente agli utenti specifici di accedere alle applicazioni nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="9a2b3-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="9a2b3-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a2b3-122">Related topics</span></span>


[<span data-ttu-id="9a2b3-123">Come eseguire attività amministrative in Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="9a2b3-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





