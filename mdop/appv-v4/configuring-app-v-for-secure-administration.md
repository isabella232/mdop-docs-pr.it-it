---
title: Configurazione di App-V per l'amministrazione sicura
description: Configurazione di App-V per l'amministrazione sicura
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821905"
---
# <span data-ttu-id="5d776-103">Configurazione di App-V per l'amministrazione sicura</span><span class="sxs-lookup"><span data-stu-id="5d776-103">Configuring App-V for Secure Administration</span></span>


<span data-ttu-id="5d776-104">In un ambiente in cui è importante proteggere le operazioni amministrative, App-V consente la comunicazione sicura tra il servizio di gestione Web App-V e la console di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="5d776-104">In an environment where securing administrative operations is important, App-V allows for secure communication between the App-V Web Management Service and the App-V Management Console.</span></span> <span data-ttu-id="5d776-105">Poiché il servizio di gestione è un'applicazione basata sul Web, è necessario proteggere l'applicazione App-V Management Server nel server Web che ospita il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="5d776-105">Because the Management Service is a Web-based application, it requires securing the App-V Management Server application on the Web server that hosts the Management Service.</span></span> <span data-ttu-id="5d776-106">Come illustrato nella figura seguente, questo processo include l'uso di HTTPS per la comunicazione e la configurazione del server IIS per consentire solo l'autenticazione integrata di Windows.</span><span class="sxs-lookup"><span data-stu-id="5d776-106">As shown in the following illustration, this process includes using HTTPS for communication and configuring the IIS server to allow only Windows Integrated Authentication.</span></span>

![configurazione di rete del servizio Web App-v](images/appvmgmtwebservice.gif)

<span data-ttu-id="5d776-108">Il servizio di gestione Web App-V viene installato come applicazione basata sul Web in IIS.</span><span class="sxs-lookup"><span data-stu-id="5d776-108">The App-V Web Management Service is installed as a Web-based application on IIS.</span></span> <span data-ttu-id="5d776-109">Per il servizio di gestione Web per supportare connessioni sicure (SSL) tra la console di gestione di App-V e il servizio di gestione Web, sarà necessario configurare il server IIS in cui è installato il servizio di gestione Web e configurare App-V Management Console.</span><span class="sxs-lookup"><span data-stu-id="5d776-109">For the Web Management Service to support secure (SSL) connections between the App-V Management Console and the Web Management Service, you will need to configure the IIS server where the Web Management Service is installed and configure the App-V Management Console.</span></span>

## <span data-ttu-id="5d776-110">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="5d776-110">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[<span data-ttu-id="5d776-111">Configurazione dei certificati per supportare il Servizio gestione Web di App-V</span><span class="sxs-lookup"><span data-stu-id="5d776-111">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)  
<span data-ttu-id="5d776-112">Fornisce informazioni utili sulla configurazione dei certificati per il supporto delle connessioni basate su SSL, per facilitare la comunicazione sicura per il servizio di gestione Web App-V.</span><span class="sxs-lookup"><span data-stu-id="5d776-112">Provides helpful information about configuring certificates to support SSL-based connections, to help secure communication for the App-V Web Management Service.</span></span>

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[<span data-ttu-id="5d776-113">Come installare e configurare App-V Management Console per un ambiente più sicuro</span><span class="sxs-lookup"><span data-stu-id="5d776-113">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
<span data-ttu-id="5d776-114">Fornisce una procedura dettagliata per la connessione a un servizio di gestione Web App-V tramite una connessione sicura.</span><span class="sxs-lookup"><span data-stu-id="5d776-114">Provides a step-by-step procedure for connecting to an App-V Web Management Service by using a secure connection.</span></span>

 

 





