---
title: Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti
description: Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825696"
---
# <span data-ttu-id="94992-103">Come installare l'aggiornamento della versione localizzata di MBAM nei server distribuiti</span><span class="sxs-lookup"><span data-stu-id="94992-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="94992-104">Microsoft BitLocker Administration and Monitoring (MBAM) include quattro ruoli del server che possono essere eseguiti in uno o più computer.</span><span class="sxs-lookup"><span data-stu-id="94992-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="94992-105">Tuttavia, solo due funzionalità di MBAM server richiedono l'aggiornamento per supportare l'installazione della versione del linguaggio MBAM 1,0 e il modello di criteri di mbam.</span><span class="sxs-lookup"><span data-stu-id="94992-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="94992-106">In configurazioni con le funzionalità di MBAM Server installate in più computer, è necessario aggiornare solo le funzionalità del server seguenti:</span><span class="sxs-lookup"><span data-stu-id="94992-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="94992-107">I report di controllo e conformità di MBAM</span><span class="sxs-lookup"><span data-stu-id="94992-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="94992-108">Il server di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="94992-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="94992-109">**Importante**  Le caratteristiche del server MBAM devono essere aggiornate in questo ordine: i report di conformità e controllo prima e quindi il server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="94992-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="94992-110">I modelli di criteri di gruppo di MBAM possono essere aggiornati in qualsiasi momento senza problemi di sequenza.</span><span class="sxs-lookup"><span data-stu-id="94992-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="94992-111">Per installare l'aggiornamento della lingua MBAM nella funzionalità MBAM Compliance and audit report server</span><span class="sxs-lookup"><span data-stu-id="94992-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="94992-112">Nel computer che esegue la funzionalità MBAM Compliance and audit report individuare ed eseguire la configurazione guidata aggiornamento lingua MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="94992-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="94992-113">Completare la procedura guidata per i report di conformità e controllo e quindi chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="94992-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="94992-114">Per installare l'aggiornamento della lingua MBAM nella funzionalità MBAM Administration and Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="94992-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="94992-115">Nel computer in cui è in uso la funzionalità di amministrazione e monitoraggio di MBAM aprire la console di gestione di Internet Information Services (IIS), accedere a **siti**e quindi arrestare il sito Web di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="94992-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="94992-116">Scegliere di modificare i binding per il sito Web di MBAM e quindi modificare i binding del sito.</span><span class="sxs-lookup"><span data-stu-id="94992-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="94992-117">Ad esempio, cambia la porta da 443 a 9443.</span><span class="sxs-lookup"><span data-stu-id="94992-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="94992-118">Individuare ed eseguire la configurazione guidata aggiornamento lingua MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="94992-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="94992-119">Completare la procedura guidata per la funzionalità di amministrazione e monitoraggio Server e quindi chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="94992-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="94992-120">Dopo aver aggiornato il database del server, aprire la console di gestione di IIS ed esaminare i binding del sito Web di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="94992-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="94992-121">Eliminare il binding precedente e verificare che il binding rimanente abbia il nome host, il certificato e il numero di porta corretti per la configurazione di MBAM Enterprise.</span><span class="sxs-lookup"><span data-stu-id="94992-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="94992-122">Riavviare il sito Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="94992-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="94992-123">Testare la funzionalità del sito Web MBAM:</span><span class="sxs-lookup"><span data-stu-id="94992-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="94992-124">Aprire l'interfaccia Web di MBAM e verificare che sia possibile ottenere una chiave di ripristino per un client.</span><span class="sxs-lookup"><span data-stu-id="94992-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="94992-125">Applicare la crittografia di un computer client nuovo o decrittografato manualmente.</span><span class="sxs-lookup"><span data-stu-id="94992-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="94992-126">**Nota**  Il client MBAM si apre solo se può comunicare con il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="94992-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="94992-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94992-127">Related topics</span></span>


[<span data-ttu-id="94992-128">Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="94992-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





