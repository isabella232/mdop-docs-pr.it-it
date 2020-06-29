---
title: Come configurare il firewall di Windows Server 2003 per App-V
description: Come configurare il firewall di Windows Server 2003 per App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817726"
---
# <span data-ttu-id="35032-103">Come configurare il firewall di Windows Server 2003 per App-V</span><span class="sxs-lookup"><span data-stu-id="35032-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="35032-104">Usare la procedura seguente per configurare il firewall di WindowsServer 2003 per App-V.</span><span class="sxs-lookup"><span data-stu-id="35032-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="35032-105">Per configurare il firewall di WindowsServer 2003 per App-V</span><span class="sxs-lookup"><span data-stu-id="35032-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="35032-106">Nel **Pannello di controllo**aprire **Windows Firewall**.</span><span class="sxs-lookup"><span data-stu-id="35032-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="35032-107">**Nota**  Se il server non è stato configurato per l'esecuzione del servizio firewall prima di questo passaggio, verrà richiesto di avviare il servizio firewall.</span><span class="sxs-lookup"><span data-stu-id="35032-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="35032-108">Se i file ICO e OSD vengono pubblicati tramite SMB, verificare che la **condivisione di file e stampanti** sia abilitata nella scheda **eccezioni** .</span><span class="sxs-lookup"><span data-stu-id="35032-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="35032-109">**Nota**  Se i file ICO e OSD vengono pubblicati tramite HTTP/HTTPS nel server di gestione, potrebbe essere necessario aggiungere un'eccezione per HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="35032-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="35032-110">Se il server IIS che ospita i file ICO e OSD è ospitato in un computer separato dal server di gestione, è necessario aggiungere l'eccezione a tale computer.</span><span class="sxs-lookup"><span data-stu-id="35032-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="35032-111">Per ottimizzare le prestazioni, è consigliabile ospitare i file ICO e OSD in un server separato dal server di gestione.</span><span class="sxs-lookup"><span data-stu-id="35032-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="35032-112">Aggiungere un'eccezione per `sghwdsptr.exe` il programma, ovvero l'eseguibile del servizio server di gestione.</span><span class="sxs-lookup"><span data-stu-id="35032-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="35032-113">Il percorso predefinito di questo eseguibile è `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="35032-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="35032-114">**Nota**  Se il server di gestione USA RTSP per la comunicazione, è necessario aggiungere anche un'eccezione per il programma `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="35032-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="35032-115">App-V Streaming Server richiede un'eccezione di programma `sglwdsptr.exe` per la comunicazione RTSPS.</span><span class="sxs-lookup"><span data-stu-id="35032-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="35032-116">L'App-V streaming server che usa RTSP per comunicare richiede anche un'eccezione per il programma `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="35032-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="35032-117">Verificare che l'ambito appropriato sia configurato per ogni eccezione.</span><span class="sxs-lookup"><span data-stu-id="35032-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="35032-118">Per ridurre il rischio, rimuovere qualsiasi computer e limitare rigorosamente gli indirizzi IP a cui il server risponderà.</span><span class="sxs-lookup"><span data-stu-id="35032-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="35032-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35032-119">Related topics</span></span>


[<span data-ttu-id="35032-120">Come configurare il firewall di Windows Server 2008 per App-V</span><span class="sxs-lookup"><span data-stu-id="35032-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





