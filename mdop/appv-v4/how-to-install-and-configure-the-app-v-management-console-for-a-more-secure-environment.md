---
title: Come installare e configurare App-V Management Console per un ambiente più sicuro
description: Come installare e configurare App-V Management Console per un ambiente più sicuro
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817375"
---
# <span data-ttu-id="b920a-103">Come installare e configurare App-V Management Console per un ambiente più sicuro</span><span class="sxs-lookup"><span data-stu-id="b920a-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="b920a-104">L'installazione predefinita di App-V Management Console include il supporto per le comunicazioni sicure.</span><span class="sxs-lookup"><span data-stu-id="b920a-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="b920a-105">Ogni console di gestione è configurata in base alle singole connessioni quando la console viene avviata per la prima volta o quando si connette a un altro servizio di gestione Web App-V.</span><span class="sxs-lookup"><span data-stu-id="b920a-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="b920a-106">La configurazione predefinita Usa SSL sulla porta TCP 443.</span><span class="sxs-lookup"><span data-stu-id="b920a-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="b920a-107">È possibile modificare il numero di porta se il numero di porta è stato modificato nel server.</span><span class="sxs-lookup"><span data-stu-id="b920a-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="b920a-108">Per connettersi a un servizio di gestione Web App-V tramite una connessione sicura, è possibile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="b920a-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="b920a-109">Come connettersi a un servizio di gestione di App-V tramite una connessione SSL</span><span class="sxs-lookup"><span data-stu-id="b920a-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="b920a-110">Avviare l'Application Virtualization Management Console.</span><span class="sxs-lookup"><span data-stu-id="b920a-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="b920a-111">Fare clic su **Configura connessione** nel riquadro azioni della console.</span><span class="sxs-lookup"><span data-stu-id="b920a-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="b920a-112">Digitare il **nome host del servizio Web**e verificare che sia selezionata l'opzione **Usa connessione sicura** .</span><span class="sxs-lookup"><span data-stu-id="b920a-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="b920a-113">**Importante**  Il nome specificato nel nome host del servizio Web deve corrispondere al nome comune del certificato oppure la connessione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b920a-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="b920a-114">Selezionare le credenziali di accesso appropriate e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b920a-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="b920a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b920a-115">Related topics</span></span>


[<span data-ttu-id="b920a-116">Configurazione dei certificati per supportare il Servizio gestione Web di App-V</span><span class="sxs-lookup"><span data-stu-id="b920a-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





