---
title: Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo
description: Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824755"
---
# <span data-ttu-id="14062-103">Come installare l'aggiornamento della versione localizzata di MBAM in un server singolo</span><span class="sxs-lookup"><span data-stu-id="14062-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="14062-104">Microsoft BitLocker Administration and Monitoring (MBAM) include quattro ruoli del server che possono essere eseguiti in uno o più computer.</span><span class="sxs-lookup"><span data-stu-id="14062-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="14062-105">Tuttavia, solo due funzionalità di MBAM server richiedono l'aggiornamento per supportare l'installazione della versione del linguaggio MBAM 1,0 e il modello di criteri di mbam.</span><span class="sxs-lookup"><span data-stu-id="14062-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="14062-106">Per aggiornare tutte e tre le funzionalità di MBAM necessarie per l'installazione in un computer, eseguire i passaggi descritti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="14062-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="14062-107">Per installare l'aggiornamento della lingua MBAM in un singolo server</span><span class="sxs-lookup"><span data-stu-id="14062-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="14062-108">Aprire la console di gestione di Internet Information Services (IIS), accedere a **siti**e quindi arrestare il sito Web di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="14062-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="14062-109">Modificare i binding per il sito Web di MBAM e quindi modificare temporaneamente i binding del sito.</span><span class="sxs-lookup"><span data-stu-id="14062-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="14062-110">Ad esempio, cambia la porta da 443 a 9443.</span><span class="sxs-lookup"><span data-stu-id="14062-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="14062-111">Individuare ed eseguire la configurazione guidata di MBAM (MBAMsetup.exe) e selezionare le tre caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="14062-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="14062-112">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="14062-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="14062-113">Server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="14062-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="14062-114">Modelli di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="14062-114">Group Policy Templates</span></span>

    <span data-ttu-id="14062-115">**Importante**  Le caratteristiche del server MBAM devono essere aggiornate nell'ordine seguente: report di conformità e controllo prima, quindi Amministrazione e monitoraggio Server.</span><span class="sxs-lookup"><span data-stu-id="14062-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="14062-116">I modelli di criteri di gruppo possono essere aggiornati in qualsiasi momento senza problemi di sequenza.</span><span class="sxs-lookup"><span data-stu-id="14062-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="14062-117">Dopo aver aggiornato il database del server, aprire la console di gestione di IIS ed esaminare i binding del sito Web di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="14062-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="14062-118">Eliminare uno dei binding e verificare che il binding rimanente abbia il nome host, il certificato e il numero di porta corretti per la configurazione di MBAM Enterprise.</span><span class="sxs-lookup"><span data-stu-id="14062-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="14062-119">Riavviare il sito Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="14062-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="14062-120">Testare la funzionalità del sito Web MBAM:</span><span class="sxs-lookup"><span data-stu-id="14062-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="14062-121">Aprire l'interfaccia Web di MBAM e verificare che sia possibile recuperare una chiave di ripristino per un client.</span><span class="sxs-lookup"><span data-stu-id="14062-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="14062-122">Applicare la crittografia di un computer client nuovo o decrittografato manualmente.</span><span class="sxs-lookup"><span data-stu-id="14062-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="14062-123">**Nota**  Il client MBAM si apre solo se può comunicare con il database di ripristino e hardware.</span><span class="sxs-lookup"><span data-stu-id="14062-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="14062-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14062-124">Related topics</span></span>


[<span data-ttu-id="14062-125">Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="14062-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





