---
title: Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione
description: Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821876"
---
# <span data-ttu-id="fba37-103">Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="fba37-103">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>


<span data-ttu-id="fba37-104">Se non è stato effettuato il provisioning del certificato corretto prima dell'installazione di App-V Management Server o App-V Streaming Server, l'App-V può essere configurata per una maggiore sicurezza dopo l'installazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="fba37-104">If the proper certificate was not provisioned before the installation of the App-V Management Server or the App-V Streaming Server, App-V can be configured for enhanced security after the initial installation.</span></span> <span data-ttu-id="fba37-105">Puoi configurare App-V Management Server tramite App-V Management Console.</span><span class="sxs-lookup"><span data-stu-id="fba37-105">You can configure the App-V Management Server through the App-V Management Console.</span></span> <span data-ttu-id="fba37-106">Tuttavia, l'App-V Streaming Server viene gestito tramite il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fba37-106">However, the App-V Streaming Server is managed through the registry.</span></span> <span data-ttu-id="fba37-107">In entrambi i casi, il certificato deve includere l' *utilizzo appropriato delle chiavi estese* (EKU) per l'autenticazione del server e il servizio di rete deve avere accesso in lettura alla chiave privata.</span><span class="sxs-lookup"><span data-stu-id="fba37-107">In either case, the certificate must include the proper *extended key usage* (EKU) for Server authentication and the Network Service must have read access to the private key.</span></span>

## <span data-ttu-id="fba37-108">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="fba37-108">In This Section</span></span>


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[<span data-ttu-id="fba37-109">Come configurare la sicurezza di Management Server dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="fba37-109">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)  
<span data-ttu-id="fba37-110">Fornisce una procedura che può essere eseguita dopo l'installazione, usando la console di gestione di App-V, per aggiungere il certificato e configurare App-V Management Server per una maggiore sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fba37-110">Provides a procedure that can be performed post-installation, using the App-V Management Console, to add the certificate and configure the App-V Management Server for enhanced security.</span></span>

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[<span data-ttu-id="fba37-111">Come configurare la sicurezza di Streaming Server dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="fba37-111">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)  
<span data-ttu-id="fba37-112">Fornisce una procedura che può essere eseguita dopo l'installazione, per aggiungere il certificato e configurare App-V Streaming Server per una maggiore sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fba37-112">Provides a procedure that can be performed post-installation, to add the certificate and configure the App-V Streaming Server for enhanced security.</span></span>

<a href="" id="troubleshooting-certificate-permission-issues"></a>[<span data-ttu-id="fba37-113">Risoluzione dei problemi di autorizzazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="fba37-113">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)  
<span data-ttu-id="fba37-114">Fornisce indicazioni per la risoluzione dei problemi quando la chiave privata non è stata configurata con l'ACL appropriato per il servizio di rete.</span><span class="sxs-lookup"><span data-stu-id="fba37-114">Provides troubleshooting guidance for when the private key has not been configured with the proper ACL for the Network Service.</span></span>

 

 





