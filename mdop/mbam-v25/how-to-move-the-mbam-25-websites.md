---
title: Come spostare i siti Web di MBAM 2.5
description: Come spostare i siti Web di MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825746"
---
# <span data-ttu-id="79d8e-103">Come spostare i siti Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="79d8e-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="79d8e-104">Usare queste procedure per trasferire i siti Web di MBAM seguenti da un computer a un altro, ovvero per trasferire le caratteristiche seguenti dal server a al server B:</span><span class="sxs-lookup"><span data-stu-id="79d8e-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="79d8e-105">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="79d8e-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="79d8e-106">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="79d8e-106">Self-Service Portal</span></span>

<span data-ttu-id="79d8e-107">**Importante**  Durante la configurazione di entrambi i siti Web, è necessario specificare la stessa stringa di connessione, l'URL report, gli account di gruppo e l'account di dominio del pool di applicazioni del servizio Web come quelli attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="79d8e-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="79d8e-108">Se non si usano gli stessi valori, non è possibile accedere ad alcuni server.</span><span class="sxs-lookup"><span data-stu-id="79d8e-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="79d8e-109">Per ottenere i valori correnti, usare il cmdlet **Get-MbamWebApplication** di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79d8e-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="79d8e-110">Per trasferire il sito Web di amministrazione e monitoraggio in un altro server</span><span class="sxs-lookup"><span data-stu-id="79d8e-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="79d8e-111">Nel server B installare il software del server MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="79d8e-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="79d8e-112">Per istruzioni, vedere [installazione del software server MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="79d8e-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="79d8e-113">Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica di **amministrazione e monitoraggio del sito Web** .</span><span class="sxs-lookup"><span data-stu-id="79d8e-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="79d8e-114">In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamWebApplication** per configurare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="79d8e-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="79d8e-115">Per istruzioni su come configurare il sito Web di amministrazione e monitoraggio, vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="79d8e-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="79d8e-116">Per trasferire il portale self-service in un altro server</span><span class="sxs-lookup"><span data-stu-id="79d8e-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="79d8e-117">Nel server B installare il software del server MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="79d8e-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="79d8e-118">Per istruzioni, vedere [installazione del software server MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="79d8e-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="79d8e-119">Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **portale self-service** .</span><span class="sxs-lookup"><span data-stu-id="79d8e-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="79d8e-120">In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamWebApplication** per configurare il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="79d8e-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="79d8e-121">Per istruzioni su come configurare il sito Web di amministrazione e monitoraggio, vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="79d8e-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="79d8e-122">Se i computer client dell'organizzazione non hanno accesso alla rete di distribuzione del contenuto Microsoft, è anche necessario trasferire i file JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79d8e-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="79d8e-123">Informazioni [su come configurare il portale self-service quando i computer client non riescono ad accedere alla rete di distribuzione del contenuto Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) .</span><span class="sxs-lookup"><span data-stu-id="79d8e-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="79d8e-124">Personalizzare il portale self-service per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="79d8e-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="79d8e-125">Usare le istruzioni per [personalizzare il portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md) per esaminare le personalizzazioni correnti e per configurare le impostazioni personalizzate nel portale self-server nel server B.</span><span class="sxs-lookup"><span data-stu-id="79d8e-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="79d8e-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79d8e-126">Related topics</span></span>


[<span data-ttu-id="79d8e-127">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="79d8e-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="79d8e-128">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="79d8e-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="79d8e-129">Spostamento delle funzionalità di MBAM 2.5 a un altro server</span><span class="sxs-lookup"><span data-stu-id="79d8e-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="79d8e-130">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="79d8e-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="79d8e-131">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="79d8e-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="79d8e-132">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="79d8e-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





