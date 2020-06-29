---
title: Configurazione di IIS per lo streaming sicuro
description: Configurazione di IIS per lo streaming sicuro
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821885"
---
# <span data-ttu-id="643a4-103">Configurazione di IIS per lo streaming sicuro</span><span class="sxs-lookup"><span data-stu-id="643a4-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="643a4-104">Con il rilascio di Microsoft Application Virtualization (App-V) versione 4,5, è possibile usare i protocolli HTTP e HTTPS per la trasmissione di pacchetti di applicazioni ai client App-V.</span><span class="sxs-lookup"><span data-stu-id="643a4-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="643a4-105">Questa opzione consente alle organizzazioni di sfruttare l'ulteriore scalabilità che IIS offre in genere.</span><span class="sxs-lookup"><span data-stu-id="643a4-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="643a4-106">Quando si usa IIS come server di streaming, è possibile proteggere le comunicazioni tra il client e il server tramite HTTPS anziché HTTP.</span><span class="sxs-lookup"><span data-stu-id="643a4-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="643a4-107">**Nota**  Se si vuole eseguire il flusso delle applicazioni da un file server, è consigliabile migliorare la sicurezza delle comunicazioni per i pacchetti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="643a4-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="643a4-108">Questa operazione può essere eseguita tramite IPsec.</span><span class="sxs-lookup"><span data-stu-id="643a4-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="643a4-109">Per altre informazioni, vedere gli argomenti seguenti nella raccolta TechNet:</span><span class="sxs-lookup"><span data-stu-id="643a4-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="643a4-110">Per Windows Server2003,</span><span class="sxs-lookup"><span data-stu-id="643a4-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="643a4-111">Per Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="643a4-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="643a4-112">Tipi MIME</span><span class="sxs-lookup"><span data-stu-id="643a4-112">MIME Types</span></span>


<span data-ttu-id="643a4-113">Quando si usa IIS per eseguire il flusso di applicazioni virtuali con HTTP o HTTPS, per supportare App-V, è necessario aggiungere i seguenti tipi MIME al server IIS:</span><span class="sxs-lookup"><span data-stu-id="643a4-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="643a4-114">. OSD = TXT</span><span class="sxs-lookup"><span data-stu-id="643a4-114">.OSD=TXT</span></span>

-   <span data-ttu-id="643a4-115">. SFT = binario</span><span class="sxs-lookup"><span data-stu-id="643a4-115">.SFT=Binary</span></span>

<span data-ttu-id="643a4-116">Usare gli articoli della Knowledge base seguenti come indicazioni per l'aggiunta di tipi MIME:</span><span class="sxs-lookup"><span data-stu-id="643a4-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="643a4-117">IIS 6,0:</span><span class="sxs-lookup"><span data-stu-id="643a4-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="643a4-118">IIS 7,0:</span><span class="sxs-lookup"><span data-stu-id="643a4-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="643a4-119">Autenticazione Kerberos</span><span class="sxs-lookup"><span data-stu-id="643a4-119">Kerberos Authentication</span></span>


<span data-ttu-id="643a4-120">Quando usi l'autenticazione HTTP o HTTPS e Kerberos per eseguire il flusso di file ICO, OSD o SFT, stai migliorando la sicurezza dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="643a4-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="643a4-121">Tuttavia, per supportare l'autenticazione Kerberos in IIS, è necessario configurare un nome SPN (Service Principal Name) appropriato.</span><span class="sxs-lookup"><span data-stu-id="643a4-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="643a4-122">Lo `setspn.exe` strumento è disponibile per Windows Server2003 dagli strumenti di supporto del CD di installazione ed è incorporato in Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="643a4-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="643a4-123">Per creare un SPN, eseguire `setspn.exe` da un prompt dei comandi durante l'accesso come membro di amministratori di dominio, ad esempio `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="643a4-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="643a4-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="643a4-124">Related topics</span></span>


[<span data-ttu-id="643a4-125">Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione</span><span class="sxs-lookup"><span data-stu-id="643a4-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





